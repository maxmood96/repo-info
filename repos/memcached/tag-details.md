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
$ docker pull memcached@sha256:abcf6f9aa41d318eec8545d95d7617bf392a2548b494ba91502da544ce156c67
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
$ docker pull memcached@sha256:fe6175b895bf327f0a49f18f24f6d63fdff1244d2bb01b66be828dd242a8c896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31972673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd546324997c0a40f0c03f0517211bfe65c08348d50f63548f81fe77b85e4ced`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sun, 02 Feb 2025 07:54:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fedffee92af44a379d24a5aa33a3ba6b7c2506c5f5364f7176ade65d9524bc`  
		Last Modified: Tue, 04 Feb 2025 04:28:58 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c2f9f9913f583649e29a3a2d436a5ae83f661daa9a4a3ec851d0e59fd9df89`  
		Last Modified: Tue, 04 Feb 2025 04:28:58 GMT  
		Size: 2.5 MB (2491785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbec463a35a75ca82fc40395dc573259b68925a58c1d807b30369d1aa0ae0b6b`  
		Last Modified: Tue, 04 Feb 2025 04:28:58 GMT  
		Size: 1.3 MB (1267074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1639ac6067c6a735763a45940530325312576704c8d26ebbfe6ed98cbdcec6`  
		Last Modified: Tue, 04 Feb 2025 04:28:58 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e075c77694a0d33203ecd6f3013d1db8992d1805e1d2b2f0ae7e5844e818e1`  
		Last Modified: Tue, 04 Feb 2025 04:28:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:0c5685395f6f2c3ccba97d1243d14b1b76ced16fa604c5dd74ff526d9ae21669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f96994adb795e76f47fa54962705d27228878c09c30dbb5cc78dfda05a0e810c`

```dockerfile
```

-	Layers:
	-	`sha256:776bdd6252940f9f9beec60d69803e592d9f81c6f6ac3af63ac8c8286b7d5231`  
		Last Modified: Tue, 04 Feb 2025 04:28:58 GMT  
		Size: 2.3 MB (2289307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ae8c4ca198567328bf1e310d5250ead344a3f33e5e25f7ebaaf6f85953fa2f8`  
		Last Modified: Tue, 04 Feb 2025 04:28:58 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v5

```console
$ docker pull memcached@sha256:3e23b25ff5492ba265c6beb3f7b66439db09a21058605ec99fa81439625177e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29079320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bda06acae7b451db750946fe903698d277afa7242f5ca0c376b741329963c34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sun, 02 Feb 2025 07:54:12 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aa8576c673e5a651f7450bee7603a12ac6168051fdd5b2411678987e180cad6e`  
		Last Modified: Tue, 04 Feb 2025 01:38:28 GMT  
		Size: 25.7 MB (25736549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d03c1f12f429fcd661498f32bc4e1c1e6a1e4189bd6014e71da057147e2286`  
		Last Modified: Tue, 04 Feb 2025 04:58:18 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7e25c626324a280a0e7be83a5642bb48a551515d4c38cb544c66904fcf10bb`  
		Last Modified: Tue, 04 Feb 2025 04:58:19 GMT  
		Size: 2.1 MB (2096073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e66403ec68cf3c2e1ff6271437414ce28660419f8d6c31f24edf02c56043262`  
		Last Modified: Tue, 04 Feb 2025 04:58:19 GMT  
		Size: 1.2 MB (1245186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f749b98d44a3942a1e45b8f89dc5b9b45b3305ce5bfa145f543463bcf50eb7b`  
		Last Modified: Tue, 04 Feb 2025 04:58:18 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:703069b289a6d2efdf95eef836d36ea4221f0d8e81a15ea1d1c57de352a39674`  
		Last Modified: Tue, 04 Feb 2025 04:58:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:aa7da31c13e723cc51b38e05c1d6e83ea69c4681b2c0c2d799c80fb66c1b4785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d4e5a0b18ec46d6e5b2f35fcc7b750e3caff802347cd8ae31c822368dee1882`

```dockerfile
```

-	Layers:
	-	`sha256:48a6ab4752d86991553683ca36c648def5b52c5c695e8b1647ab32b21c4d9729`  
		Last Modified: Tue, 04 Feb 2025 04:58:19 GMT  
		Size: 2.3 MB (2292845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c4499883bd4502cc0726091a993acdeada7afd3e77f04c3b57e639ec56412a7`  
		Last Modified: Tue, 04 Feb 2025 04:58:18 GMT  
		Size: 21.4 KB (21368 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:fc1b1df1cc951fa0c913d4130b817fbf6f2e471598ffabe70cc99a1517810f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31658229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4edc43a8d642cf5350fa9c2bdcd33cd413c992506a36a31c16473b2865332b34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sun, 02 Feb 2025 07:54:12 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be3b898de6ed2c686c435db2ea65d18020b171ffb60cbe49d3e443270a750c5`  
		Last Modified: Tue, 04 Feb 2025 05:12:27 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f228ff9270a43bec782505e8c0498a642411d336d532a20f2d9f5c75ff729440`  
		Last Modified: Tue, 04 Feb 2025 05:12:27 GMT  
		Size: 2.4 MB (2355305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1bdfd0bf72ae4f3963e64b34d95501e0d2519f1fddf366859182d3cbc30fd9`  
		Last Modified: Tue, 04 Feb 2025 05:12:27 GMT  
		Size: 1.3 MB (1260531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49345faedbef95e78c7480c3e88bd390e45ff60b758a8ae1f768bd4ceada482`  
		Last Modified: Tue, 04 Feb 2025 05:12:27 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bf52a3188788cbb838b8d4a75624fc409328a3f2168c02f63ba3f6adc4ddd8`  
		Last Modified: Tue, 04 Feb 2025 05:12:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:dd3a185dcbb98130c88a3525aa9e7697df859c3c4f9cf0a28481500d4ce9f96a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dda5672c78a463481b13d1a9dd18e83c8cb05d4b901cb9609b3bba27dfe31230`

```dockerfile
```

-	Layers:
	-	`sha256:0b1bc32d1fda8af809796a1814f321de4bbfca145293aca905206f7d57f70077`  
		Last Modified: Tue, 04 Feb 2025 05:12:27 GMT  
		Size: 2.3 MB (2289622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38e4993eec3a8b75af870e911804786af2a7938874d6f0cdf2157d77dd395e75`  
		Last Modified: Tue, 04 Feb 2025 05:12:27 GMT  
		Size: 21.4 KB (21419 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:99e98590099d2d337986980eeb79c3be0410599530aedcb0565f1b0fd7a7cd26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32955938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:218fe1071938e177eaf04cd6fafbdc37a820e5600e864659206f847e6457d2d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sun, 02 Feb 2025 07:54:12 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3e0bbec4e230ba69d1863d0cfc4bb4ffd41f22f10ffc6acdc5e7b83ecde34c`  
		Last Modified: Tue, 04 Feb 2025 04:28:42 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9dd28ef3cfec128e7a1800f6f22aaa8ea274fb08d0461d882a3cfd4f2186d4`  
		Last Modified: Tue, 04 Feb 2025 04:28:42 GMT  
		Size: 2.5 MB (2500678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e809c489bd7a749f8dd5e42f875574f90c71a4a1aeb4a6d5f78fb38f4dfe91c`  
		Last Modified: Tue, 04 Feb 2025 04:28:42 GMT  
		Size: 1.3 MB (1266291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0569ca3484d7c418601aa4a1d9c03b3a201ae7a07615a5177306ffb6706d0e69`  
		Last Modified: Tue, 04 Feb 2025 04:28:42 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96ec23ce107bcd0877feb48601e1a40ecb123ecd1a8a830fd10bbba4a1ce72a`  
		Last Modified: Tue, 04 Feb 2025 04:28:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:966e032dabd37972613a5886d18a681f7e24e3fee197935b5caf17fb36e21b64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e416fe378dee459251a62a2b5b653c4e2743cecc04e7e5219b1c75c5c4685e0`

```dockerfile
```

-	Layers:
	-	`sha256:d0e0a2e88cc36444c10da305fb5dac611a00828958609797a27fe6be0f7144a5`  
		Last Modified: Tue, 04 Feb 2025 04:28:42 GMT  
		Size: 2.3 MB (2286406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3cbad4006e7b93580c2af2558bc8cf21cfe19addf8bf173de3a234902191e69`  
		Last Modified: Tue, 04 Feb 2025 04:28:42 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; mips64le

```console
$ docker pull memcached@sha256:fcaa4f5ef9712e2ddca14e6857f1b53fa20672b914cd7b88b6b65445f1832a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31692137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:719403932d2bf7fe31ce1da2e00837219fc634598515ea22717f233d4c45b21c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sun, 02 Feb 2025 07:54:12 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1738540800'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:60fe4951c23056512065fcf1948d3167c5aa5d83d4bfd2829494b7d09b4fe661`  
		Last Modified: Tue, 04 Feb 2025 01:38:47 GMT  
		Size: 28.5 MB (28486581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006e6bf1f5c579c425dd6a7045b45795f463f886bf4ee3532c5964da484e77c4`  
		Last Modified: Tue, 04 Feb 2025 05:36:04 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4620497505845e0aede51939832fe2feb1e84e662ca22647506c9e403a4630`  
		Last Modified: Tue, 04 Feb 2025 05:36:05 GMT  
		Size: 1.9 MB (1943191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbe6e63eb850a0d15f3fb3ce772dc8a193c1b9ead3f64bc87ea9db83a818e31`  
		Last Modified: Tue, 04 Feb 2025 05:36:05 GMT  
		Size: 1.3 MB (1260854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40e7ec508708863f095d5fd6aeac52dffd7f20c336c28d94a7fad02f2f51a29`  
		Last Modified: Tue, 04 Feb 2025 05:36:05 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd558b6f1714e94bee89e0cf11e0ea1af8a90cc74c1b99553e6313974bea9d6`  
		Last Modified: Tue, 04 Feb 2025 05:36:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:10a2ecdde0367c592a37e2094ddcfc7edb98d5d73d5bbdfd7d7069f11468f41b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a6d8d3fb499ac955955b2c9f4e9776ff914141d14adeea588a371ce4cff3bd`

```dockerfile
```

-	Layers:
	-	`sha256:e0a5ca44660b9368be372266be4aefc4be704e101067286cf36e1b06e2f07cdb`  
		Last Modified: Tue, 04 Feb 2025 05:36:04 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:31e531e504071c6297e43ec0359e37dd60aafa37b23f2cfd572d6992a4a8f699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36085904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029e8e5e0f017ebe180b7e7e42e69b8469d48d66dccc36f4ee94cc70531ce2ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sun, 02 Feb 2025 07:54:12 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 01:38:01 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2554b2c9b1b0eaccf71963ebdaa720beba7c4729f900596b8bb7e99b6919b1`  
		Last Modified: Tue, 04 Feb 2025 04:54:07 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26b95187bf5085dc8573c96b467801af0c38567ad032cafcf7565bc83e8c10c`  
		Last Modified: Tue, 04 Feb 2025 04:54:07 GMT  
		Size: 2.7 MB (2708613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229261d8ebd7f1a31858565844b84e86a020984fbe64d3a62b3d685417159948`  
		Last Modified: Tue, 04 Feb 2025 04:54:07 GMT  
		Size: 1.3 MB (1330999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9891f8d1e557cafb091f637b3db5cdb8b11696ed2c249fdfb769b4a33d3078`  
		Last Modified: Tue, 04 Feb 2025 04:54:07 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25470058ddabb0f895e9d1799ac944c98f6b75317f06a627f30187b8fdfb0a36`  
		Last Modified: Tue, 04 Feb 2025 04:54:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:f914e538671a572729170958d470dfabd855aa80ce53b25a0d7a5204c1b33a0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c38e1164115528d1af0164fb9dc030c96e5f940b1dc40e46c04e9dcf03b3df0`

```dockerfile
```

-	Layers:
	-	`sha256:1f9e966fff09eb8597e726dee37d8077951c4a8388ca91a79ec2ce5e5e913c60`  
		Last Modified: Tue, 04 Feb 2025 04:54:07 GMT  
		Size: 2.3 MB (2293679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd28c7586277dc4f00031d57a5fe00d338e5418c714bd57259f440b8bcbc728c`  
		Last Modified: Tue, 04 Feb 2025 04:54:07 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:682eb0a0e7d4cd11f8b9a3e1290057c1e796788a4618a3ac5c82cb7df58933d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30261734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df80d341f0efbcde25b92f3e1b797f27625a16d555bfca98f22061de2f298a69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sun, 02 Feb 2025 07:54:12 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe1d1bee073fc6fc7edf8762994dd33eb7f445c49d726accfb91332a242d958`  
		Last Modified: Tue, 04 Feb 2025 04:55:22 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8785d74590885c81503a45644906e34c354e69c862dad662a22f498c866adece`  
		Last Modified: Tue, 04 Feb 2025 04:55:23 GMT  
		Size: 2.2 MB (2156364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b1bdeb9a486655fb1fbc129ff4907a4c86b484a6c915d9a05aa040888c89e7`  
		Last Modified: Tue, 04 Feb 2025 04:55:23 GMT  
		Size: 1.2 MB (1245232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5b08891d9cb8dac889b466249456f8845d8eb3f7434466b96b09d5431e01a4`  
		Last Modified: Tue, 04 Feb 2025 04:55:23 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a8546468c2d277e130e611d05861380d2da0d3147183727229235f1e512e35`  
		Last Modified: Tue, 04 Feb 2025 04:55:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:f0f959f8ecfee4cbf470f9361e8b57b4e533448ff02939b9502eab73afb04b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e145048ce46bf258188b341bfa77adce8eb7da0fbb8839645158ffc3497c4c9a`

```dockerfile
```

-	Layers:
	-	`sha256:517488b2faa7932817aca91e747eb050e4f797d147f86ea3652de77ba7bb9518`  
		Last Modified: Tue, 04 Feb 2025 04:55:23 GMT  
		Size: 2.3 MB (2289021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94edb64050cfbde612663e71dc905e22225a42f70f6a8d44f18e0667df39e53c`  
		Last Modified: Tue, 04 Feb 2025 04:55:23 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:b093f7f64a39f20b8f4a671f9c6656eff26821a3c97037a8019448040d6298bd
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
$ docker pull memcached@sha256:c497fc5a323c178e0914eca2500dcf9fa3b21ca2f9932dbc92b51ef6145cf2be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4716328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d2b29f4542cd1fc099ca3146ac53cc0eab71776ce1c029fee5d58a57c38a52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9604a91067e8818541aa31757690c9f8ebf60c58be004baded0767c0999267b8`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592b1cc3d47258eaa3cb466a887cb58e0b2a4176818d1c9a721698abf9337d94`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 104.7 KB (104686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5a55a29aba2a2a27962f2b36f259f5fac81a49009fc7c06020fc992eb6d5da`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 968.6 KB (968568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4786022d0e1453ad1d978f79f50839ba76e4f7c73310640921e5bc212537d6e`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da16032c7fbc5aedc09cd3d43a996943828a731b3ed781664abcf257bdfb65c`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:f4b6389438043b9d6191b9e22e19659d23258e22f0e414f51cb0945287141162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e696a02855f507b1b926a60cf07265433c5ab415467633243c2536753b3090`

```dockerfile
```

-	Layers:
	-	`sha256:16a139d5ff76ba43b3c520a2be58514f36e0ad4a7b0f9adfb6b9c80acb97219d`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 93.6 KB (93627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d8f0efc7a1d5a7dc78219efc6849e55d842b9a5e34ff6bee956735b7cbe2967`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:4d52a91c9cf3612ab9f44d1ecc192f150659288c8826932187c7ab3ed5f8dc9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5082815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef0a8813bf35c3ce3d0d0f9967d27c56db3fb8dc2fd7f31ab4cd3fc1f7cd209`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a202407430ec08b7a5bfb94689fc70aed855fbc1cd8b62ce145147fc5278b7a8`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82c0f1024964e8e055db8178bb0d2595a4a66f7398bffe83d6176cc192ac77e`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 120.8 KB (120783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46624d73285a34a525d44fb1f293cdb9fc95ebfb5b305918bc6a1ff77019fda`  
		Last Modified: Mon, 03 Feb 2025 23:32:18 GMT  
		Size: 968.3 KB (968310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099e6e9c12eb4dfbd63c3bc7cec8de6eb251173a42983594f30413921e56380a`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348cf5001affc34a6f03be6a7f413a6cc377fa11350026995dd53f7db78b85a1`  
		Last Modified: Mon, 03 Feb 2025 23:32:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:631105e348c97a01de96919b82284f666d3283712a23e1b5670c31c88810f40c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff4582dcb2cdec3cfb7590e5b6ade8162439d38a001ff6c08fa81f7d08c669e`

```dockerfile
```

-	Layers:
	-	`sha256:8f4375fd6e27a5ee655f47249469c2214b367ec0146b4e8769a97c6afa3d2829`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 93.7 KB (93731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4bf5d12011dbaae039aec13c76a68a64809e478a3b79d0090ba407f1d4f7c61`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:1f1e5941bca8da9b3aeabcc13c55fe90fc40f9c6476645c19172e508e5302723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4534153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2936f0dd081882d9f0da9ea6113e9780627d3a665a9d909de817c696fac9620`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300aaa75d91b0206b7556a721baaed9f7000ccf73ab8deda59e1cb428ec870f9`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ac94f71cda4f155944d630f60f3e31780c4a97ced13f6c61385dc7e95df429`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 109.5 KB (109465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73b7528b6c4fdfdf4075a75f9e28334049f5461f39426f3b2f983792188c971`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 960.2 KB (960204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb441509973ed0be28152c5ef6c85917a0de941839cd68559be4ecfcc273b17`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e6efaa8bc767e6ef9d48f3b7547a57b7d72964bbb765d7a66481f3f3b36dd1`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:0de21b11722d02a9d2cfc6acf661c6d755de360f4c1f70e7af549cac29e5aef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10be0a79af6bc5d121d12aa89f8e2191eb25f2533cfb4e1de067b3e0bbe82834`

```dockerfile
```

-	Layers:
	-	`sha256:c57cf3137ea2641a839877ddcf3a6065504f38c2ea4f2b7671c1776008e2cfcf`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 93.6 KB (93582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdf7d0d4ee2052676f3563869639942945b1cba543484223915cb33df997a5f0`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 19.5 KB (19512 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:913b5bd251bfe9202c3f0302d3c8c5a4ea3fb7f40f73e8561542c93db1c9d6c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4706076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8083b854e648814b258458b24e3039ade25fa9e63e50b6fb79db7cb05d2ee3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a841f248cda34139a77fd6ab9691e34b7d7dae6dfaedc45a2304aa25c07536`  
		Last Modified: Mon, 03 Feb 2025 23:32:07 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ccea169aa483a5ea29ebe89aa46469affffa54252ac8df2ee75acc10eca2e0`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 124.3 KB (124280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f40e8d115f7e602d9931eaa3e7f41c17dc35a40994befa787615cbd877d430`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 1.0 MB (1006836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf17c8f5e90551f91b3474eb46d197d4ac28e21bf5cb9aaa79eea5b851db371`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9971977dd87dcc447ad6eccbe529fc3c7d6b7dc6b74a4d74fb519c86565318f4`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:04513dfc421f21abd4cd316a69b57cdbfd9d92844a16e9d55eec6a4592cd22d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569bb3d3624a47ed75650ef0a92bfc59d63af78afe540637c817793e9cf4b6d6`

```dockerfile
```

-	Layers:
	-	`sha256:ba709bd16c5785bcfce6f9a8fd6e1d834e101c00d1ed2e018a68a999ec43825b`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 91.7 KB (91734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bc2aa4695d41b4a46d039e0e91f623f3f7aadfd866f0e477637054a37fc5127`  
		Last Modified: Mon, 03 Feb 2025 23:32:07 GMT  
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
$ docker pull memcached@sha256:624036093e557f56a4d500c780f34193af25d5c3b73f8bb08329b579e72b7d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4570369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e3d248b914c5043ad7dc370403b9ea51bf62f972a6f7cf694a023ce14ac2d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223127e71140d5e120db85abbcc459b2ca368e042d165466a1ab8b72ada743f8`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf0ecced8267cdc41066ee8044aa4a0e35e951cba2f51a411ecbfb2cee29819`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 113.5 KB (113450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b7e62f8ce2395ffab9dff807ea14960a2cfa247d7c8a418a5e92d3b4d883f8`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 988.7 KB (988692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed293040c38a686b287b82c3a47615ca2f9034912964f5ce7e832241db526879`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1254936a9326dadc90d0b29d805e446f753a49826f2d9ea9308f5e847d6b7d4`  
		Last Modified: Mon, 03 Feb 2025 23:34:11 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:51c253df33d2a17a62bac93fdc69e4be991e6f4b9e6015eff29ad965c1e58628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 KB (111245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4b6a687d069c6e737d3a9cfa50af30753d0165aa04019517f2f6951bad7feb6`

```dockerfile
```

-	Layers:
	-	`sha256:4e1be19ae90b5f3b2e2b65ad7605851c11804d593bec1671c444bd7aadc3063d`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 91.7 KB (91676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:415673db52745ddb45aa4c05424023581f2903f3acd2578ac008e4857c8ca11b`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 19.6 KB (19569 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine3.21`

```console
$ docker pull memcached@sha256:918f8d596494e94538b93f92d629c3d20efa4d5ca8b0302bf672b65f974c5617
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
$ docker pull memcached@sha256:c497fc5a323c178e0914eca2500dcf9fa3b21ca2f9932dbc92b51ef6145cf2be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4716328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d2b29f4542cd1fc099ca3146ac53cc0eab71776ce1c029fee5d58a57c38a52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9604a91067e8818541aa31757690c9f8ebf60c58be004baded0767c0999267b8`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592b1cc3d47258eaa3cb466a887cb58e0b2a4176818d1c9a721698abf9337d94`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 104.7 KB (104686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5a55a29aba2a2a27962f2b36f259f5fac81a49009fc7c06020fc992eb6d5da`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 968.6 KB (968568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4786022d0e1453ad1d978f79f50839ba76e4f7c73310640921e5bc212537d6e`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da16032c7fbc5aedc09cd3d43a996943828a731b3ed781664abcf257bdfb65c`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:f4b6389438043b9d6191b9e22e19659d23258e22f0e414f51cb0945287141162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e696a02855f507b1b926a60cf07265433c5ab415467633243c2536753b3090`

```dockerfile
```

-	Layers:
	-	`sha256:16a139d5ff76ba43b3c520a2be58514f36e0ad4a7b0f9adfb6b9c80acb97219d`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 93.6 KB (93627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d8f0efc7a1d5a7dc78219efc6849e55d842b9a5e34ff6bee956735b7cbe2967`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:4d52a91c9cf3612ab9f44d1ecc192f150659288c8826932187c7ab3ed5f8dc9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5082815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef0a8813bf35c3ce3d0d0f9967d27c56db3fb8dc2fd7f31ab4cd3fc1f7cd209`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a202407430ec08b7a5bfb94689fc70aed855fbc1cd8b62ce145147fc5278b7a8`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82c0f1024964e8e055db8178bb0d2595a4a66f7398bffe83d6176cc192ac77e`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 120.8 KB (120783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46624d73285a34a525d44fb1f293cdb9fc95ebfb5b305918bc6a1ff77019fda`  
		Last Modified: Mon, 03 Feb 2025 23:32:18 GMT  
		Size: 968.3 KB (968310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099e6e9c12eb4dfbd63c3bc7cec8de6eb251173a42983594f30413921e56380a`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348cf5001affc34a6f03be6a7f413a6cc377fa11350026995dd53f7db78b85a1`  
		Last Modified: Mon, 03 Feb 2025 23:32:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:631105e348c97a01de96919b82284f666d3283712a23e1b5670c31c88810f40c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff4582dcb2cdec3cfb7590e5b6ade8162439d38a001ff6c08fa81f7d08c669e`

```dockerfile
```

-	Layers:
	-	`sha256:8f4375fd6e27a5ee655f47249469c2214b367ec0146b4e8769a97c6afa3d2829`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 93.7 KB (93731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4bf5d12011dbaae039aec13c76a68a64809e478a3b79d0090ba407f1d4f7c61`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; 386

```console
$ docker pull memcached@sha256:1f1e5941bca8da9b3aeabcc13c55fe90fc40f9c6476645c19172e508e5302723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4534153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2936f0dd081882d9f0da9ea6113e9780627d3a665a9d909de817c696fac9620`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300aaa75d91b0206b7556a721baaed9f7000ccf73ab8deda59e1cb428ec870f9`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ac94f71cda4f155944d630f60f3e31780c4a97ced13f6c61385dc7e95df429`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 109.5 KB (109465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73b7528b6c4fdfdf4075a75f9e28334049f5461f39426f3b2f983792188c971`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 960.2 KB (960204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb441509973ed0be28152c5ef6c85917a0de941839cd68559be4ecfcc273b17`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e6efaa8bc767e6ef9d48f3b7547a57b7d72964bbb765d7a66481f3f3b36dd1`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:0de21b11722d02a9d2cfc6acf661c6d755de360f4c1f70e7af549cac29e5aef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10be0a79af6bc5d121d12aa89f8e2191eb25f2533cfb4e1de067b3e0bbe82834`

```dockerfile
```

-	Layers:
	-	`sha256:c57cf3137ea2641a839877ddcf3a6065504f38c2ea4f2b7671c1776008e2cfcf`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 93.6 KB (93582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdf7d0d4ee2052676f3563869639942945b1cba543484223915cb33df997a5f0`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 19.5 KB (19512 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; ppc64le

```console
$ docker pull memcached@sha256:913b5bd251bfe9202c3f0302d3c8c5a4ea3fb7f40f73e8561542c93db1c9d6c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4706076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8083b854e648814b258458b24e3039ade25fa9e63e50b6fb79db7cb05d2ee3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a841f248cda34139a77fd6ab9691e34b7d7dae6dfaedc45a2304aa25c07536`  
		Last Modified: Mon, 03 Feb 2025 23:32:07 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ccea169aa483a5ea29ebe89aa46469affffa54252ac8df2ee75acc10eca2e0`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 124.3 KB (124280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f40e8d115f7e602d9931eaa3e7f41c17dc35a40994befa787615cbd877d430`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 1.0 MB (1006836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf17c8f5e90551f91b3474eb46d197d4ac28e21bf5cb9aaa79eea5b851db371`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9971977dd87dcc447ad6eccbe529fc3c7d6b7dc6b74a4d74fb519c86565318f4`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:04513dfc421f21abd4cd316a69b57cdbfd9d92844a16e9d55eec6a4592cd22d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569bb3d3624a47ed75650ef0a92bfc59d63af78afe540637c817793e9cf4b6d6`

```dockerfile
```

-	Layers:
	-	`sha256:ba709bd16c5785bcfce6f9a8fd6e1d834e101c00d1ed2e018a68a999ec43825b`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 91.7 KB (91734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bc2aa4695d41b4a46d039e0e91f623f3f7aadfd866f0e477637054a37fc5127`  
		Last Modified: Mon, 03 Feb 2025 23:32:07 GMT  
		Size: 19.6 KB (19648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; s390x

```console
$ docker pull memcached@sha256:624036093e557f56a4d500c780f34193af25d5c3b73f8bb08329b579e72b7d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4570369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e3d248b914c5043ad7dc370403b9ea51bf62f972a6f7cf694a023ce14ac2d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223127e71140d5e120db85abbcc459b2ca368e042d165466a1ab8b72ada743f8`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf0ecced8267cdc41066ee8044aa4a0e35e951cba2f51a411ecbfb2cee29819`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 113.5 KB (113450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b7e62f8ce2395ffab9dff807ea14960a2cfa247d7c8a418a5e92d3b4d883f8`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 988.7 KB (988692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed293040c38a686b287b82c3a47615ca2f9034912964f5ce7e832241db526879`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1254936a9326dadc90d0b29d805e446f753a49826f2d9ea9308f5e847d6b7d4`  
		Last Modified: Mon, 03 Feb 2025 23:34:11 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:51c253df33d2a17a62bac93fdc69e4be991e6f4b9e6015eff29ad965c1e58628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 KB (111245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4b6a687d069c6e737d3a9cfa50af30753d0165aa04019517f2f6951bad7feb6`

```dockerfile
```

-	Layers:
	-	`sha256:4e1be19ae90b5f3b2e2b65ad7605851c11804d593bec1671c444bd7aadc3063d`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 91.7 KB (91676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:415673db52745ddb45aa4c05424023581f2903f3acd2578ac008e4857c8ca11b`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 19.6 KB (19569 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-bookworm`

```console
$ docker pull memcached@sha256:abcf6f9aa41d318eec8545d95d7617bf392a2548b494ba91502da544ce156c67
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
$ docker pull memcached@sha256:fe6175b895bf327f0a49f18f24f6d63fdff1244d2bb01b66be828dd242a8c896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31972673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd546324997c0a40f0c03f0517211bfe65c08348d50f63548f81fe77b85e4ced`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sun, 02 Feb 2025 07:54:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fedffee92af44a379d24a5aa33a3ba6b7c2506c5f5364f7176ade65d9524bc`  
		Last Modified: Tue, 04 Feb 2025 04:28:58 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c2f9f9913f583649e29a3a2d436a5ae83f661daa9a4a3ec851d0e59fd9df89`  
		Last Modified: Tue, 04 Feb 2025 04:28:58 GMT  
		Size: 2.5 MB (2491785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbec463a35a75ca82fc40395dc573259b68925a58c1d807b30369d1aa0ae0b6b`  
		Last Modified: Tue, 04 Feb 2025 04:28:58 GMT  
		Size: 1.3 MB (1267074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1639ac6067c6a735763a45940530325312576704c8d26ebbfe6ed98cbdcec6`  
		Last Modified: Tue, 04 Feb 2025 04:28:58 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e075c77694a0d33203ecd6f3013d1db8992d1805e1d2b2f0ae7e5844e818e1`  
		Last Modified: Tue, 04 Feb 2025 04:28:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:0c5685395f6f2c3ccba97d1243d14b1b76ced16fa604c5dd74ff526d9ae21669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f96994adb795e76f47fa54962705d27228878c09c30dbb5cc78dfda05a0e810c`

```dockerfile
```

-	Layers:
	-	`sha256:776bdd6252940f9f9beec60d69803e592d9f81c6f6ac3af63ac8c8286b7d5231`  
		Last Modified: Tue, 04 Feb 2025 04:28:58 GMT  
		Size: 2.3 MB (2289307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ae8c4ca198567328bf1e310d5250ead344a3f33e5e25f7ebaaf6f85953fa2f8`  
		Last Modified: Tue, 04 Feb 2025 04:28:58 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:3e23b25ff5492ba265c6beb3f7b66439db09a21058605ec99fa81439625177e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29079320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bda06acae7b451db750946fe903698d277afa7242f5ca0c376b741329963c34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sun, 02 Feb 2025 07:54:12 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aa8576c673e5a651f7450bee7603a12ac6168051fdd5b2411678987e180cad6e`  
		Last Modified: Tue, 04 Feb 2025 01:38:28 GMT  
		Size: 25.7 MB (25736549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d03c1f12f429fcd661498f32bc4e1c1e6a1e4189bd6014e71da057147e2286`  
		Last Modified: Tue, 04 Feb 2025 04:58:18 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7e25c626324a280a0e7be83a5642bb48a551515d4c38cb544c66904fcf10bb`  
		Last Modified: Tue, 04 Feb 2025 04:58:19 GMT  
		Size: 2.1 MB (2096073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e66403ec68cf3c2e1ff6271437414ce28660419f8d6c31f24edf02c56043262`  
		Last Modified: Tue, 04 Feb 2025 04:58:19 GMT  
		Size: 1.2 MB (1245186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f749b98d44a3942a1e45b8f89dc5b9b45b3305ce5bfa145f543463bcf50eb7b`  
		Last Modified: Tue, 04 Feb 2025 04:58:18 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:703069b289a6d2efdf95eef836d36ea4221f0d8e81a15ea1d1c57de352a39674`  
		Last Modified: Tue, 04 Feb 2025 04:58:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:aa7da31c13e723cc51b38e05c1d6e83ea69c4681b2c0c2d799c80fb66c1b4785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d4e5a0b18ec46d6e5b2f35fcc7b750e3caff802347cd8ae31c822368dee1882`

```dockerfile
```

-	Layers:
	-	`sha256:48a6ab4752d86991553683ca36c648def5b52c5c695e8b1647ab32b21c4d9729`  
		Last Modified: Tue, 04 Feb 2025 04:58:19 GMT  
		Size: 2.3 MB (2292845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c4499883bd4502cc0726091a993acdeada7afd3e77f04c3b57e639ec56412a7`  
		Last Modified: Tue, 04 Feb 2025 04:58:18 GMT  
		Size: 21.4 KB (21368 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:fc1b1df1cc951fa0c913d4130b817fbf6f2e471598ffabe70cc99a1517810f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31658229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4edc43a8d642cf5350fa9c2bdcd33cd413c992506a36a31c16473b2865332b34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sun, 02 Feb 2025 07:54:12 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be3b898de6ed2c686c435db2ea65d18020b171ffb60cbe49d3e443270a750c5`  
		Last Modified: Tue, 04 Feb 2025 05:12:27 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f228ff9270a43bec782505e8c0498a642411d336d532a20f2d9f5c75ff729440`  
		Last Modified: Tue, 04 Feb 2025 05:12:27 GMT  
		Size: 2.4 MB (2355305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1bdfd0bf72ae4f3963e64b34d95501e0d2519f1fddf366859182d3cbc30fd9`  
		Last Modified: Tue, 04 Feb 2025 05:12:27 GMT  
		Size: 1.3 MB (1260531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49345faedbef95e78c7480c3e88bd390e45ff60b758a8ae1f768bd4ceada482`  
		Last Modified: Tue, 04 Feb 2025 05:12:27 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bf52a3188788cbb838b8d4a75624fc409328a3f2168c02f63ba3f6adc4ddd8`  
		Last Modified: Tue, 04 Feb 2025 05:12:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:dd3a185dcbb98130c88a3525aa9e7697df859c3c4f9cf0a28481500d4ce9f96a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dda5672c78a463481b13d1a9dd18e83c8cb05d4b901cb9609b3bba27dfe31230`

```dockerfile
```

-	Layers:
	-	`sha256:0b1bc32d1fda8af809796a1814f321de4bbfca145293aca905206f7d57f70077`  
		Last Modified: Tue, 04 Feb 2025 05:12:27 GMT  
		Size: 2.3 MB (2289622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38e4993eec3a8b75af870e911804786af2a7938874d6f0cdf2157d77dd395e75`  
		Last Modified: Tue, 04 Feb 2025 05:12:27 GMT  
		Size: 21.4 KB (21419 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:99e98590099d2d337986980eeb79c3be0410599530aedcb0565f1b0fd7a7cd26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32955938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:218fe1071938e177eaf04cd6fafbdc37a820e5600e864659206f847e6457d2d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sun, 02 Feb 2025 07:54:12 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3e0bbec4e230ba69d1863d0cfc4bb4ffd41f22f10ffc6acdc5e7b83ecde34c`  
		Last Modified: Tue, 04 Feb 2025 04:28:42 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9dd28ef3cfec128e7a1800f6f22aaa8ea274fb08d0461d882a3cfd4f2186d4`  
		Last Modified: Tue, 04 Feb 2025 04:28:42 GMT  
		Size: 2.5 MB (2500678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e809c489bd7a749f8dd5e42f875574f90c71a4a1aeb4a6d5f78fb38f4dfe91c`  
		Last Modified: Tue, 04 Feb 2025 04:28:42 GMT  
		Size: 1.3 MB (1266291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0569ca3484d7c418601aa4a1d9c03b3a201ae7a07615a5177306ffb6706d0e69`  
		Last Modified: Tue, 04 Feb 2025 04:28:42 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96ec23ce107bcd0877feb48601e1a40ecb123ecd1a8a830fd10bbba4a1ce72a`  
		Last Modified: Tue, 04 Feb 2025 04:28:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:966e032dabd37972613a5886d18a681f7e24e3fee197935b5caf17fb36e21b64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e416fe378dee459251a62a2b5b653c4e2743cecc04e7e5219b1c75c5c4685e0`

```dockerfile
```

-	Layers:
	-	`sha256:d0e0a2e88cc36444c10da305fb5dac611a00828958609797a27fe6be0f7144a5`  
		Last Modified: Tue, 04 Feb 2025 04:28:42 GMT  
		Size: 2.3 MB (2286406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3cbad4006e7b93580c2af2558bc8cf21cfe19addf8bf173de3a234902191e69`  
		Last Modified: Tue, 04 Feb 2025 04:28:42 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:fcaa4f5ef9712e2ddca14e6857f1b53fa20672b914cd7b88b6b65445f1832a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31692137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:719403932d2bf7fe31ce1da2e00837219fc634598515ea22717f233d4c45b21c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sun, 02 Feb 2025 07:54:12 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1738540800'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:60fe4951c23056512065fcf1948d3167c5aa5d83d4bfd2829494b7d09b4fe661`  
		Last Modified: Tue, 04 Feb 2025 01:38:47 GMT  
		Size: 28.5 MB (28486581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006e6bf1f5c579c425dd6a7045b45795f463f886bf4ee3532c5964da484e77c4`  
		Last Modified: Tue, 04 Feb 2025 05:36:04 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4620497505845e0aede51939832fe2feb1e84e662ca22647506c9e403a4630`  
		Last Modified: Tue, 04 Feb 2025 05:36:05 GMT  
		Size: 1.9 MB (1943191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbe6e63eb850a0d15f3fb3ce772dc8a193c1b9ead3f64bc87ea9db83a818e31`  
		Last Modified: Tue, 04 Feb 2025 05:36:05 GMT  
		Size: 1.3 MB (1260854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40e7ec508708863f095d5fd6aeac52dffd7f20c336c28d94a7fad02f2f51a29`  
		Last Modified: Tue, 04 Feb 2025 05:36:05 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd558b6f1714e94bee89e0cf11e0ea1af8a90cc74c1b99553e6313974bea9d6`  
		Last Modified: Tue, 04 Feb 2025 05:36:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:10a2ecdde0367c592a37e2094ddcfc7edb98d5d73d5bbdfd7d7069f11468f41b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a6d8d3fb499ac955955b2c9f4e9776ff914141d14adeea588a371ce4cff3bd`

```dockerfile
```

-	Layers:
	-	`sha256:e0a5ca44660b9368be372266be4aefc4be704e101067286cf36e1b06e2f07cdb`  
		Last Modified: Tue, 04 Feb 2025 05:36:04 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:31e531e504071c6297e43ec0359e37dd60aafa37b23f2cfd572d6992a4a8f699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36085904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029e8e5e0f017ebe180b7e7e42e69b8469d48d66dccc36f4ee94cc70531ce2ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sun, 02 Feb 2025 07:54:12 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 01:38:01 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2554b2c9b1b0eaccf71963ebdaa720beba7c4729f900596b8bb7e99b6919b1`  
		Last Modified: Tue, 04 Feb 2025 04:54:07 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26b95187bf5085dc8573c96b467801af0c38567ad032cafcf7565bc83e8c10c`  
		Last Modified: Tue, 04 Feb 2025 04:54:07 GMT  
		Size: 2.7 MB (2708613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229261d8ebd7f1a31858565844b84e86a020984fbe64d3a62b3d685417159948`  
		Last Modified: Tue, 04 Feb 2025 04:54:07 GMT  
		Size: 1.3 MB (1330999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9891f8d1e557cafb091f637b3db5cdb8b11696ed2c249fdfb769b4a33d3078`  
		Last Modified: Tue, 04 Feb 2025 04:54:07 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25470058ddabb0f895e9d1799ac944c98f6b75317f06a627f30187b8fdfb0a36`  
		Last Modified: Tue, 04 Feb 2025 04:54:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f914e538671a572729170958d470dfabd855aa80ce53b25a0d7a5204c1b33a0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c38e1164115528d1af0164fb9dc030c96e5f940b1dc40e46c04e9dcf03b3df0`

```dockerfile
```

-	Layers:
	-	`sha256:1f9e966fff09eb8597e726dee37d8077951c4a8388ca91a79ec2ce5e5e913c60`  
		Last Modified: Tue, 04 Feb 2025 04:54:07 GMT  
		Size: 2.3 MB (2293679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd28c7586277dc4f00031d57a5fe00d338e5418c714bd57259f440b8bcbc728c`  
		Last Modified: Tue, 04 Feb 2025 04:54:07 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:682eb0a0e7d4cd11f8b9a3e1290057c1e796788a4618a3ac5c82cb7df58933d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30261734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df80d341f0efbcde25b92f3e1b797f27625a16d555bfca98f22061de2f298a69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sun, 02 Feb 2025 07:54:12 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe1d1bee073fc6fc7edf8762994dd33eb7f445c49d726accfb91332a242d958`  
		Last Modified: Tue, 04 Feb 2025 04:55:22 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8785d74590885c81503a45644906e34c354e69c862dad662a22f498c866adece`  
		Last Modified: Tue, 04 Feb 2025 04:55:23 GMT  
		Size: 2.2 MB (2156364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b1bdeb9a486655fb1fbc129ff4907a4c86b484a6c915d9a05aa040888c89e7`  
		Last Modified: Tue, 04 Feb 2025 04:55:23 GMT  
		Size: 1.2 MB (1245232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5b08891d9cb8dac889b466249456f8845d8eb3f7434466b96b09d5431e01a4`  
		Last Modified: Tue, 04 Feb 2025 04:55:23 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a8546468c2d277e130e611d05861380d2da0d3147183727229235f1e512e35`  
		Last Modified: Tue, 04 Feb 2025 04:55:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f0f959f8ecfee4cbf470f9361e8b57b4e533448ff02939b9502eab73afb04b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e145048ce46bf258188b341bfa77adce8eb7da0fbb8839645158ffc3497c4c9a`

```dockerfile
```

-	Layers:
	-	`sha256:517488b2faa7932817aca91e747eb050e4f797d147f86ea3652de77ba7bb9518`  
		Last Modified: Tue, 04 Feb 2025 04:55:23 GMT  
		Size: 2.3 MB (2289021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94edb64050cfbde612663e71dc905e22225a42f70f6a8d44f18e0667df39e53c`  
		Last Modified: Tue, 04 Feb 2025 04:55:23 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6`

```console
$ docker pull memcached@sha256:abcf6f9aa41d318eec8545d95d7617bf392a2548b494ba91502da544ce156c67
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
$ docker pull memcached@sha256:fe6175b895bf327f0a49f18f24f6d63fdff1244d2bb01b66be828dd242a8c896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31972673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd546324997c0a40f0c03f0517211bfe65c08348d50f63548f81fe77b85e4ced`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sun, 02 Feb 2025 07:54:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fedffee92af44a379d24a5aa33a3ba6b7c2506c5f5364f7176ade65d9524bc`  
		Last Modified: Tue, 04 Feb 2025 04:28:58 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c2f9f9913f583649e29a3a2d436a5ae83f661daa9a4a3ec851d0e59fd9df89`  
		Last Modified: Tue, 04 Feb 2025 04:28:58 GMT  
		Size: 2.5 MB (2491785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbec463a35a75ca82fc40395dc573259b68925a58c1d807b30369d1aa0ae0b6b`  
		Last Modified: Tue, 04 Feb 2025 04:28:58 GMT  
		Size: 1.3 MB (1267074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1639ac6067c6a735763a45940530325312576704c8d26ebbfe6ed98cbdcec6`  
		Last Modified: Tue, 04 Feb 2025 04:28:58 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e075c77694a0d33203ecd6f3013d1db8992d1805e1d2b2f0ae7e5844e818e1`  
		Last Modified: Tue, 04 Feb 2025 04:28:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:0c5685395f6f2c3ccba97d1243d14b1b76ced16fa604c5dd74ff526d9ae21669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f96994adb795e76f47fa54962705d27228878c09c30dbb5cc78dfda05a0e810c`

```dockerfile
```

-	Layers:
	-	`sha256:776bdd6252940f9f9beec60d69803e592d9f81c6f6ac3af63ac8c8286b7d5231`  
		Last Modified: Tue, 04 Feb 2025 04:28:58 GMT  
		Size: 2.3 MB (2289307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ae8c4ca198567328bf1e310d5250ead344a3f33e5e25f7ebaaf6f85953fa2f8`  
		Last Modified: Tue, 04 Feb 2025 04:28:58 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:3e23b25ff5492ba265c6beb3f7b66439db09a21058605ec99fa81439625177e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29079320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bda06acae7b451db750946fe903698d277afa7242f5ca0c376b741329963c34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sun, 02 Feb 2025 07:54:12 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aa8576c673e5a651f7450bee7603a12ac6168051fdd5b2411678987e180cad6e`  
		Last Modified: Tue, 04 Feb 2025 01:38:28 GMT  
		Size: 25.7 MB (25736549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d03c1f12f429fcd661498f32bc4e1c1e6a1e4189bd6014e71da057147e2286`  
		Last Modified: Tue, 04 Feb 2025 04:58:18 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7e25c626324a280a0e7be83a5642bb48a551515d4c38cb544c66904fcf10bb`  
		Last Modified: Tue, 04 Feb 2025 04:58:19 GMT  
		Size: 2.1 MB (2096073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e66403ec68cf3c2e1ff6271437414ce28660419f8d6c31f24edf02c56043262`  
		Last Modified: Tue, 04 Feb 2025 04:58:19 GMT  
		Size: 1.2 MB (1245186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f749b98d44a3942a1e45b8f89dc5b9b45b3305ce5bfa145f543463bcf50eb7b`  
		Last Modified: Tue, 04 Feb 2025 04:58:18 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:703069b289a6d2efdf95eef836d36ea4221f0d8e81a15ea1d1c57de352a39674`  
		Last Modified: Tue, 04 Feb 2025 04:58:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:aa7da31c13e723cc51b38e05c1d6e83ea69c4681b2c0c2d799c80fb66c1b4785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d4e5a0b18ec46d6e5b2f35fcc7b750e3caff802347cd8ae31c822368dee1882`

```dockerfile
```

-	Layers:
	-	`sha256:48a6ab4752d86991553683ca36c648def5b52c5c695e8b1647ab32b21c4d9729`  
		Last Modified: Tue, 04 Feb 2025 04:58:19 GMT  
		Size: 2.3 MB (2292845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c4499883bd4502cc0726091a993acdeada7afd3e77f04c3b57e639ec56412a7`  
		Last Modified: Tue, 04 Feb 2025 04:58:18 GMT  
		Size: 21.4 KB (21368 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:fc1b1df1cc951fa0c913d4130b817fbf6f2e471598ffabe70cc99a1517810f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31658229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4edc43a8d642cf5350fa9c2bdcd33cd413c992506a36a31c16473b2865332b34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sun, 02 Feb 2025 07:54:12 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be3b898de6ed2c686c435db2ea65d18020b171ffb60cbe49d3e443270a750c5`  
		Last Modified: Tue, 04 Feb 2025 05:12:27 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f228ff9270a43bec782505e8c0498a642411d336d532a20f2d9f5c75ff729440`  
		Last Modified: Tue, 04 Feb 2025 05:12:27 GMT  
		Size: 2.4 MB (2355305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1bdfd0bf72ae4f3963e64b34d95501e0d2519f1fddf366859182d3cbc30fd9`  
		Last Modified: Tue, 04 Feb 2025 05:12:27 GMT  
		Size: 1.3 MB (1260531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49345faedbef95e78c7480c3e88bd390e45ff60b758a8ae1f768bd4ceada482`  
		Last Modified: Tue, 04 Feb 2025 05:12:27 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bf52a3188788cbb838b8d4a75624fc409328a3f2168c02f63ba3f6adc4ddd8`  
		Last Modified: Tue, 04 Feb 2025 05:12:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:dd3a185dcbb98130c88a3525aa9e7697df859c3c4f9cf0a28481500d4ce9f96a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dda5672c78a463481b13d1a9dd18e83c8cb05d4b901cb9609b3bba27dfe31230`

```dockerfile
```

-	Layers:
	-	`sha256:0b1bc32d1fda8af809796a1814f321de4bbfca145293aca905206f7d57f70077`  
		Last Modified: Tue, 04 Feb 2025 05:12:27 GMT  
		Size: 2.3 MB (2289622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38e4993eec3a8b75af870e911804786af2a7938874d6f0cdf2157d77dd395e75`  
		Last Modified: Tue, 04 Feb 2025 05:12:27 GMT  
		Size: 21.4 KB (21419 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; 386

```console
$ docker pull memcached@sha256:99e98590099d2d337986980eeb79c3be0410599530aedcb0565f1b0fd7a7cd26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32955938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:218fe1071938e177eaf04cd6fafbdc37a820e5600e864659206f847e6457d2d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sun, 02 Feb 2025 07:54:12 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3e0bbec4e230ba69d1863d0cfc4bb4ffd41f22f10ffc6acdc5e7b83ecde34c`  
		Last Modified: Tue, 04 Feb 2025 04:28:42 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9dd28ef3cfec128e7a1800f6f22aaa8ea274fb08d0461d882a3cfd4f2186d4`  
		Last Modified: Tue, 04 Feb 2025 04:28:42 GMT  
		Size: 2.5 MB (2500678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e809c489bd7a749f8dd5e42f875574f90c71a4a1aeb4a6d5f78fb38f4dfe91c`  
		Last Modified: Tue, 04 Feb 2025 04:28:42 GMT  
		Size: 1.3 MB (1266291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0569ca3484d7c418601aa4a1d9c03b3a201ae7a07615a5177306ffb6706d0e69`  
		Last Modified: Tue, 04 Feb 2025 04:28:42 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96ec23ce107bcd0877feb48601e1a40ecb123ecd1a8a830fd10bbba4a1ce72a`  
		Last Modified: Tue, 04 Feb 2025 04:28:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:966e032dabd37972613a5886d18a681f7e24e3fee197935b5caf17fb36e21b64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e416fe378dee459251a62a2b5b653c4e2743cecc04e7e5219b1c75c5c4685e0`

```dockerfile
```

-	Layers:
	-	`sha256:d0e0a2e88cc36444c10da305fb5dac611a00828958609797a27fe6be0f7144a5`  
		Last Modified: Tue, 04 Feb 2025 04:28:42 GMT  
		Size: 2.3 MB (2286406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3cbad4006e7b93580c2af2558bc8cf21cfe19addf8bf173de3a234902191e69`  
		Last Modified: Tue, 04 Feb 2025 04:28:42 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; mips64le

```console
$ docker pull memcached@sha256:fcaa4f5ef9712e2ddca14e6857f1b53fa20672b914cd7b88b6b65445f1832a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31692137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:719403932d2bf7fe31ce1da2e00837219fc634598515ea22717f233d4c45b21c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sun, 02 Feb 2025 07:54:12 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1738540800'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:60fe4951c23056512065fcf1948d3167c5aa5d83d4bfd2829494b7d09b4fe661`  
		Last Modified: Tue, 04 Feb 2025 01:38:47 GMT  
		Size: 28.5 MB (28486581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006e6bf1f5c579c425dd6a7045b45795f463f886bf4ee3532c5964da484e77c4`  
		Last Modified: Tue, 04 Feb 2025 05:36:04 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4620497505845e0aede51939832fe2feb1e84e662ca22647506c9e403a4630`  
		Last Modified: Tue, 04 Feb 2025 05:36:05 GMT  
		Size: 1.9 MB (1943191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbe6e63eb850a0d15f3fb3ce772dc8a193c1b9ead3f64bc87ea9db83a818e31`  
		Last Modified: Tue, 04 Feb 2025 05:36:05 GMT  
		Size: 1.3 MB (1260854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40e7ec508708863f095d5fd6aeac52dffd7f20c336c28d94a7fad02f2f51a29`  
		Last Modified: Tue, 04 Feb 2025 05:36:05 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd558b6f1714e94bee89e0cf11e0ea1af8a90cc74c1b99553e6313974bea9d6`  
		Last Modified: Tue, 04 Feb 2025 05:36:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:10a2ecdde0367c592a37e2094ddcfc7edb98d5d73d5bbdfd7d7069f11468f41b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a6d8d3fb499ac955955b2c9f4e9776ff914141d14adeea588a371ce4cff3bd`

```dockerfile
```

-	Layers:
	-	`sha256:e0a5ca44660b9368be372266be4aefc4be704e101067286cf36e1b06e2f07cdb`  
		Last Modified: Tue, 04 Feb 2025 05:36:04 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:31e531e504071c6297e43ec0359e37dd60aafa37b23f2cfd572d6992a4a8f699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36085904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029e8e5e0f017ebe180b7e7e42e69b8469d48d66dccc36f4ee94cc70531ce2ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sun, 02 Feb 2025 07:54:12 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 01:38:01 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2554b2c9b1b0eaccf71963ebdaa720beba7c4729f900596b8bb7e99b6919b1`  
		Last Modified: Tue, 04 Feb 2025 04:54:07 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26b95187bf5085dc8573c96b467801af0c38567ad032cafcf7565bc83e8c10c`  
		Last Modified: Tue, 04 Feb 2025 04:54:07 GMT  
		Size: 2.7 MB (2708613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229261d8ebd7f1a31858565844b84e86a020984fbe64d3a62b3d685417159948`  
		Last Modified: Tue, 04 Feb 2025 04:54:07 GMT  
		Size: 1.3 MB (1330999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9891f8d1e557cafb091f637b3db5cdb8b11696ed2c249fdfb769b4a33d3078`  
		Last Modified: Tue, 04 Feb 2025 04:54:07 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25470058ddabb0f895e9d1799ac944c98f6b75317f06a627f30187b8fdfb0a36`  
		Last Modified: Tue, 04 Feb 2025 04:54:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:f914e538671a572729170958d470dfabd855aa80ce53b25a0d7a5204c1b33a0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c38e1164115528d1af0164fb9dc030c96e5f940b1dc40e46c04e9dcf03b3df0`

```dockerfile
```

-	Layers:
	-	`sha256:1f9e966fff09eb8597e726dee37d8077951c4a8388ca91a79ec2ce5e5e913c60`  
		Last Modified: Tue, 04 Feb 2025 04:54:07 GMT  
		Size: 2.3 MB (2293679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd28c7586277dc4f00031d57a5fe00d338e5418c714bd57259f440b8bcbc728c`  
		Last Modified: Tue, 04 Feb 2025 04:54:07 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; s390x

```console
$ docker pull memcached@sha256:682eb0a0e7d4cd11f8b9a3e1290057c1e796788a4618a3ac5c82cb7df58933d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30261734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df80d341f0efbcde25b92f3e1b797f27625a16d555bfca98f22061de2f298a69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sun, 02 Feb 2025 07:54:12 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe1d1bee073fc6fc7edf8762994dd33eb7f445c49d726accfb91332a242d958`  
		Last Modified: Tue, 04 Feb 2025 04:55:22 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8785d74590885c81503a45644906e34c354e69c862dad662a22f498c866adece`  
		Last Modified: Tue, 04 Feb 2025 04:55:23 GMT  
		Size: 2.2 MB (2156364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b1bdeb9a486655fb1fbc129ff4907a4c86b484a6c915d9a05aa040888c89e7`  
		Last Modified: Tue, 04 Feb 2025 04:55:23 GMT  
		Size: 1.2 MB (1245232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5b08891d9cb8dac889b466249456f8845d8eb3f7434466b96b09d5431e01a4`  
		Last Modified: Tue, 04 Feb 2025 04:55:23 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a8546468c2d277e130e611d05861380d2da0d3147183727229235f1e512e35`  
		Last Modified: Tue, 04 Feb 2025 04:55:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:f0f959f8ecfee4cbf470f9361e8b57b4e533448ff02939b9502eab73afb04b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e145048ce46bf258188b341bfa77adce8eb7da0fbb8839645158ffc3497c4c9a`

```dockerfile
```

-	Layers:
	-	`sha256:517488b2faa7932817aca91e747eb050e4f797d147f86ea3652de77ba7bb9518`  
		Last Modified: Tue, 04 Feb 2025 04:55:23 GMT  
		Size: 2.3 MB (2289021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94edb64050cfbde612663e71dc905e22225a42f70f6a8d44f18e0667df39e53c`  
		Last Modified: Tue, 04 Feb 2025 04:55:23 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine`

```console
$ docker pull memcached@sha256:b093f7f64a39f20b8f4a671f9c6656eff26821a3c97037a8019448040d6298bd
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
$ docker pull memcached@sha256:c497fc5a323c178e0914eca2500dcf9fa3b21ca2f9932dbc92b51ef6145cf2be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4716328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d2b29f4542cd1fc099ca3146ac53cc0eab71776ce1c029fee5d58a57c38a52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9604a91067e8818541aa31757690c9f8ebf60c58be004baded0767c0999267b8`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592b1cc3d47258eaa3cb466a887cb58e0b2a4176818d1c9a721698abf9337d94`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 104.7 KB (104686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5a55a29aba2a2a27962f2b36f259f5fac81a49009fc7c06020fc992eb6d5da`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 968.6 KB (968568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4786022d0e1453ad1d978f79f50839ba76e4f7c73310640921e5bc212537d6e`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da16032c7fbc5aedc09cd3d43a996943828a731b3ed781664abcf257bdfb65c`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:f4b6389438043b9d6191b9e22e19659d23258e22f0e414f51cb0945287141162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e696a02855f507b1b926a60cf07265433c5ab415467633243c2536753b3090`

```dockerfile
```

-	Layers:
	-	`sha256:16a139d5ff76ba43b3c520a2be58514f36e0ad4a7b0f9adfb6b9c80acb97219d`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 93.6 KB (93627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d8f0efc7a1d5a7dc78219efc6849e55d842b9a5e34ff6bee956735b7cbe2967`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:4d52a91c9cf3612ab9f44d1ecc192f150659288c8826932187c7ab3ed5f8dc9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5082815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef0a8813bf35c3ce3d0d0f9967d27c56db3fb8dc2fd7f31ab4cd3fc1f7cd209`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a202407430ec08b7a5bfb94689fc70aed855fbc1cd8b62ce145147fc5278b7a8`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82c0f1024964e8e055db8178bb0d2595a4a66f7398bffe83d6176cc192ac77e`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 120.8 KB (120783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46624d73285a34a525d44fb1f293cdb9fc95ebfb5b305918bc6a1ff77019fda`  
		Last Modified: Mon, 03 Feb 2025 23:32:18 GMT  
		Size: 968.3 KB (968310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099e6e9c12eb4dfbd63c3bc7cec8de6eb251173a42983594f30413921e56380a`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348cf5001affc34a6f03be6a7f413a6cc377fa11350026995dd53f7db78b85a1`  
		Last Modified: Mon, 03 Feb 2025 23:32:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:631105e348c97a01de96919b82284f666d3283712a23e1b5670c31c88810f40c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff4582dcb2cdec3cfb7590e5b6ade8162439d38a001ff6c08fa81f7d08c669e`

```dockerfile
```

-	Layers:
	-	`sha256:8f4375fd6e27a5ee655f47249469c2214b367ec0146b4e8769a97c6afa3d2829`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 93.7 KB (93731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4bf5d12011dbaae039aec13c76a68a64809e478a3b79d0090ba407f1d4f7c61`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:1f1e5941bca8da9b3aeabcc13c55fe90fc40f9c6476645c19172e508e5302723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4534153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2936f0dd081882d9f0da9ea6113e9780627d3a665a9d909de817c696fac9620`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300aaa75d91b0206b7556a721baaed9f7000ccf73ab8deda59e1cb428ec870f9`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ac94f71cda4f155944d630f60f3e31780c4a97ced13f6c61385dc7e95df429`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 109.5 KB (109465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73b7528b6c4fdfdf4075a75f9e28334049f5461f39426f3b2f983792188c971`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 960.2 KB (960204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb441509973ed0be28152c5ef6c85917a0de941839cd68559be4ecfcc273b17`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e6efaa8bc767e6ef9d48f3b7547a57b7d72964bbb765d7a66481f3f3b36dd1`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:0de21b11722d02a9d2cfc6acf661c6d755de360f4c1f70e7af549cac29e5aef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10be0a79af6bc5d121d12aa89f8e2191eb25f2533cfb4e1de067b3e0bbe82834`

```dockerfile
```

-	Layers:
	-	`sha256:c57cf3137ea2641a839877ddcf3a6065504f38c2ea4f2b7671c1776008e2cfcf`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 93.6 KB (93582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdf7d0d4ee2052676f3563869639942945b1cba543484223915cb33df997a5f0`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 19.5 KB (19512 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:913b5bd251bfe9202c3f0302d3c8c5a4ea3fb7f40f73e8561542c93db1c9d6c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4706076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8083b854e648814b258458b24e3039ade25fa9e63e50b6fb79db7cb05d2ee3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a841f248cda34139a77fd6ab9691e34b7d7dae6dfaedc45a2304aa25c07536`  
		Last Modified: Mon, 03 Feb 2025 23:32:07 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ccea169aa483a5ea29ebe89aa46469affffa54252ac8df2ee75acc10eca2e0`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 124.3 KB (124280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f40e8d115f7e602d9931eaa3e7f41c17dc35a40994befa787615cbd877d430`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 1.0 MB (1006836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf17c8f5e90551f91b3474eb46d197d4ac28e21bf5cb9aaa79eea5b851db371`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9971977dd87dcc447ad6eccbe529fc3c7d6b7dc6b74a4d74fb519c86565318f4`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:04513dfc421f21abd4cd316a69b57cdbfd9d92844a16e9d55eec6a4592cd22d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569bb3d3624a47ed75650ef0a92bfc59d63af78afe540637c817793e9cf4b6d6`

```dockerfile
```

-	Layers:
	-	`sha256:ba709bd16c5785bcfce6f9a8fd6e1d834e101c00d1ed2e018a68a999ec43825b`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 91.7 KB (91734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bc2aa4695d41b4a46d039e0e91f623f3f7aadfd866f0e477637054a37fc5127`  
		Last Modified: Mon, 03 Feb 2025 23:32:07 GMT  
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
$ docker pull memcached@sha256:624036093e557f56a4d500c780f34193af25d5c3b73f8bb08329b579e72b7d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4570369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e3d248b914c5043ad7dc370403b9ea51bf62f972a6f7cf694a023ce14ac2d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223127e71140d5e120db85abbcc459b2ca368e042d165466a1ab8b72ada743f8`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf0ecced8267cdc41066ee8044aa4a0e35e951cba2f51a411ecbfb2cee29819`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 113.5 KB (113450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b7e62f8ce2395ffab9dff807ea14960a2cfa247d7c8a418a5e92d3b4d883f8`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 988.7 KB (988692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed293040c38a686b287b82c3a47615ca2f9034912964f5ce7e832241db526879`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1254936a9326dadc90d0b29d805e446f753a49826f2d9ea9308f5e847d6b7d4`  
		Last Modified: Mon, 03 Feb 2025 23:34:11 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:51c253df33d2a17a62bac93fdc69e4be991e6f4b9e6015eff29ad965c1e58628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 KB (111245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4b6a687d069c6e737d3a9cfa50af30753d0165aa04019517f2f6951bad7feb6`

```dockerfile
```

-	Layers:
	-	`sha256:4e1be19ae90b5f3b2e2b65ad7605851c11804d593bec1671c444bd7aadc3063d`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 91.7 KB (91676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:415673db52745ddb45aa4c05424023581f2903f3acd2578ac008e4857c8ca11b`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 19.6 KB (19569 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine3.21`

```console
$ docker pull memcached@sha256:918f8d596494e94538b93f92d629c3d20efa4d5ca8b0302bf672b65f974c5617
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
$ docker pull memcached@sha256:c497fc5a323c178e0914eca2500dcf9fa3b21ca2f9932dbc92b51ef6145cf2be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4716328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d2b29f4542cd1fc099ca3146ac53cc0eab71776ce1c029fee5d58a57c38a52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9604a91067e8818541aa31757690c9f8ebf60c58be004baded0767c0999267b8`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592b1cc3d47258eaa3cb466a887cb58e0b2a4176818d1c9a721698abf9337d94`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 104.7 KB (104686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5a55a29aba2a2a27962f2b36f259f5fac81a49009fc7c06020fc992eb6d5da`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 968.6 KB (968568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4786022d0e1453ad1d978f79f50839ba76e4f7c73310640921e5bc212537d6e`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da16032c7fbc5aedc09cd3d43a996943828a731b3ed781664abcf257bdfb65c`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:f4b6389438043b9d6191b9e22e19659d23258e22f0e414f51cb0945287141162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e696a02855f507b1b926a60cf07265433c5ab415467633243c2536753b3090`

```dockerfile
```

-	Layers:
	-	`sha256:16a139d5ff76ba43b3c520a2be58514f36e0ad4a7b0f9adfb6b9c80acb97219d`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 93.6 KB (93627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d8f0efc7a1d5a7dc78219efc6849e55d842b9a5e34ff6bee956735b7cbe2967`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:4d52a91c9cf3612ab9f44d1ecc192f150659288c8826932187c7ab3ed5f8dc9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5082815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef0a8813bf35c3ce3d0d0f9967d27c56db3fb8dc2fd7f31ab4cd3fc1f7cd209`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a202407430ec08b7a5bfb94689fc70aed855fbc1cd8b62ce145147fc5278b7a8`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82c0f1024964e8e055db8178bb0d2595a4a66f7398bffe83d6176cc192ac77e`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 120.8 KB (120783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46624d73285a34a525d44fb1f293cdb9fc95ebfb5b305918bc6a1ff77019fda`  
		Last Modified: Mon, 03 Feb 2025 23:32:18 GMT  
		Size: 968.3 KB (968310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099e6e9c12eb4dfbd63c3bc7cec8de6eb251173a42983594f30413921e56380a`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348cf5001affc34a6f03be6a7f413a6cc377fa11350026995dd53f7db78b85a1`  
		Last Modified: Mon, 03 Feb 2025 23:32:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:631105e348c97a01de96919b82284f666d3283712a23e1b5670c31c88810f40c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff4582dcb2cdec3cfb7590e5b6ade8162439d38a001ff6c08fa81f7d08c669e`

```dockerfile
```

-	Layers:
	-	`sha256:8f4375fd6e27a5ee655f47249469c2214b367ec0146b4e8769a97c6afa3d2829`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 93.7 KB (93731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4bf5d12011dbaae039aec13c76a68a64809e478a3b79d0090ba407f1d4f7c61`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.21` - linux; 386

```console
$ docker pull memcached@sha256:1f1e5941bca8da9b3aeabcc13c55fe90fc40f9c6476645c19172e508e5302723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4534153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2936f0dd081882d9f0da9ea6113e9780627d3a665a9d909de817c696fac9620`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300aaa75d91b0206b7556a721baaed9f7000ccf73ab8deda59e1cb428ec870f9`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ac94f71cda4f155944d630f60f3e31780c4a97ced13f6c61385dc7e95df429`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 109.5 KB (109465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73b7528b6c4fdfdf4075a75f9e28334049f5461f39426f3b2f983792188c971`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 960.2 KB (960204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb441509973ed0be28152c5ef6c85917a0de941839cd68559be4ecfcc273b17`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e6efaa8bc767e6ef9d48f3b7547a57b7d72964bbb765d7a66481f3f3b36dd1`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:0de21b11722d02a9d2cfc6acf661c6d755de360f4c1f70e7af549cac29e5aef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10be0a79af6bc5d121d12aa89f8e2191eb25f2533cfb4e1de067b3e0bbe82834`

```dockerfile
```

-	Layers:
	-	`sha256:c57cf3137ea2641a839877ddcf3a6065504f38c2ea4f2b7671c1776008e2cfcf`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 93.6 KB (93582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdf7d0d4ee2052676f3563869639942945b1cba543484223915cb33df997a5f0`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 19.5 KB (19512 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.21` - linux; ppc64le

```console
$ docker pull memcached@sha256:913b5bd251bfe9202c3f0302d3c8c5a4ea3fb7f40f73e8561542c93db1c9d6c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4706076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8083b854e648814b258458b24e3039ade25fa9e63e50b6fb79db7cb05d2ee3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a841f248cda34139a77fd6ab9691e34b7d7dae6dfaedc45a2304aa25c07536`  
		Last Modified: Mon, 03 Feb 2025 23:32:07 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ccea169aa483a5ea29ebe89aa46469affffa54252ac8df2ee75acc10eca2e0`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 124.3 KB (124280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f40e8d115f7e602d9931eaa3e7f41c17dc35a40994befa787615cbd877d430`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 1.0 MB (1006836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf17c8f5e90551f91b3474eb46d197d4ac28e21bf5cb9aaa79eea5b851db371`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9971977dd87dcc447ad6eccbe529fc3c7d6b7dc6b74a4d74fb519c86565318f4`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:04513dfc421f21abd4cd316a69b57cdbfd9d92844a16e9d55eec6a4592cd22d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569bb3d3624a47ed75650ef0a92bfc59d63af78afe540637c817793e9cf4b6d6`

```dockerfile
```

-	Layers:
	-	`sha256:ba709bd16c5785bcfce6f9a8fd6e1d834e101c00d1ed2e018a68a999ec43825b`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 91.7 KB (91734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bc2aa4695d41b4a46d039e0e91f623f3f7aadfd866f0e477637054a37fc5127`  
		Last Modified: Mon, 03 Feb 2025 23:32:07 GMT  
		Size: 19.6 KB (19648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.21` - linux; s390x

```console
$ docker pull memcached@sha256:624036093e557f56a4d500c780f34193af25d5c3b73f8bb08329b579e72b7d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4570369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e3d248b914c5043ad7dc370403b9ea51bf62f972a6f7cf694a023ce14ac2d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223127e71140d5e120db85abbcc459b2ca368e042d165466a1ab8b72ada743f8`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf0ecced8267cdc41066ee8044aa4a0e35e951cba2f51a411ecbfb2cee29819`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 113.5 KB (113450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b7e62f8ce2395ffab9dff807ea14960a2cfa247d7c8a418a5e92d3b4d883f8`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 988.7 KB (988692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed293040c38a686b287b82c3a47615ca2f9034912964f5ce7e832241db526879`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1254936a9326dadc90d0b29d805e446f753a49826f2d9ea9308f5e847d6b7d4`  
		Last Modified: Mon, 03 Feb 2025 23:34:11 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:51c253df33d2a17a62bac93fdc69e4be991e6f4b9e6015eff29ad965c1e58628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 KB (111245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4b6a687d069c6e737d3a9cfa50af30753d0165aa04019517f2f6951bad7feb6`

```dockerfile
```

-	Layers:
	-	`sha256:4e1be19ae90b5f3b2e2b65ad7605851c11804d593bec1671c444bd7aadc3063d`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 91.7 KB (91676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:415673db52745ddb45aa4c05424023581f2903f3acd2578ac008e4857c8ca11b`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 19.6 KB (19569 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-bookworm`

```console
$ docker pull memcached@sha256:abcf6f9aa41d318eec8545d95d7617bf392a2548b494ba91502da544ce156c67
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
$ docker pull memcached@sha256:fe6175b895bf327f0a49f18f24f6d63fdff1244d2bb01b66be828dd242a8c896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31972673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd546324997c0a40f0c03f0517211bfe65c08348d50f63548f81fe77b85e4ced`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sun, 02 Feb 2025 07:54:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fedffee92af44a379d24a5aa33a3ba6b7c2506c5f5364f7176ade65d9524bc`  
		Last Modified: Tue, 04 Feb 2025 04:28:58 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c2f9f9913f583649e29a3a2d436a5ae83f661daa9a4a3ec851d0e59fd9df89`  
		Last Modified: Tue, 04 Feb 2025 04:28:58 GMT  
		Size: 2.5 MB (2491785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbec463a35a75ca82fc40395dc573259b68925a58c1d807b30369d1aa0ae0b6b`  
		Last Modified: Tue, 04 Feb 2025 04:28:58 GMT  
		Size: 1.3 MB (1267074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1639ac6067c6a735763a45940530325312576704c8d26ebbfe6ed98cbdcec6`  
		Last Modified: Tue, 04 Feb 2025 04:28:58 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e075c77694a0d33203ecd6f3013d1db8992d1805e1d2b2f0ae7e5844e818e1`  
		Last Modified: Tue, 04 Feb 2025 04:28:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:0c5685395f6f2c3ccba97d1243d14b1b76ced16fa604c5dd74ff526d9ae21669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f96994adb795e76f47fa54962705d27228878c09c30dbb5cc78dfda05a0e810c`

```dockerfile
```

-	Layers:
	-	`sha256:776bdd6252940f9f9beec60d69803e592d9f81c6f6ac3af63ac8c8286b7d5231`  
		Last Modified: Tue, 04 Feb 2025 04:28:58 GMT  
		Size: 2.3 MB (2289307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ae8c4ca198567328bf1e310d5250ead344a3f33e5e25f7ebaaf6f85953fa2f8`  
		Last Modified: Tue, 04 Feb 2025 04:28:58 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:3e23b25ff5492ba265c6beb3f7b66439db09a21058605ec99fa81439625177e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29079320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bda06acae7b451db750946fe903698d277afa7242f5ca0c376b741329963c34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sun, 02 Feb 2025 07:54:12 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aa8576c673e5a651f7450bee7603a12ac6168051fdd5b2411678987e180cad6e`  
		Last Modified: Tue, 04 Feb 2025 01:38:28 GMT  
		Size: 25.7 MB (25736549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d03c1f12f429fcd661498f32bc4e1c1e6a1e4189bd6014e71da057147e2286`  
		Last Modified: Tue, 04 Feb 2025 04:58:18 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7e25c626324a280a0e7be83a5642bb48a551515d4c38cb544c66904fcf10bb`  
		Last Modified: Tue, 04 Feb 2025 04:58:19 GMT  
		Size: 2.1 MB (2096073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e66403ec68cf3c2e1ff6271437414ce28660419f8d6c31f24edf02c56043262`  
		Last Modified: Tue, 04 Feb 2025 04:58:19 GMT  
		Size: 1.2 MB (1245186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f749b98d44a3942a1e45b8f89dc5b9b45b3305ce5bfa145f543463bcf50eb7b`  
		Last Modified: Tue, 04 Feb 2025 04:58:18 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:703069b289a6d2efdf95eef836d36ea4221f0d8e81a15ea1d1c57de352a39674`  
		Last Modified: Tue, 04 Feb 2025 04:58:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:aa7da31c13e723cc51b38e05c1d6e83ea69c4681b2c0c2d799c80fb66c1b4785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d4e5a0b18ec46d6e5b2f35fcc7b750e3caff802347cd8ae31c822368dee1882`

```dockerfile
```

-	Layers:
	-	`sha256:48a6ab4752d86991553683ca36c648def5b52c5c695e8b1647ab32b21c4d9729`  
		Last Modified: Tue, 04 Feb 2025 04:58:19 GMT  
		Size: 2.3 MB (2292845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c4499883bd4502cc0726091a993acdeada7afd3e77f04c3b57e639ec56412a7`  
		Last Modified: Tue, 04 Feb 2025 04:58:18 GMT  
		Size: 21.4 KB (21368 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:fc1b1df1cc951fa0c913d4130b817fbf6f2e471598ffabe70cc99a1517810f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31658229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4edc43a8d642cf5350fa9c2bdcd33cd413c992506a36a31c16473b2865332b34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sun, 02 Feb 2025 07:54:12 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be3b898de6ed2c686c435db2ea65d18020b171ffb60cbe49d3e443270a750c5`  
		Last Modified: Tue, 04 Feb 2025 05:12:27 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f228ff9270a43bec782505e8c0498a642411d336d532a20f2d9f5c75ff729440`  
		Last Modified: Tue, 04 Feb 2025 05:12:27 GMT  
		Size: 2.4 MB (2355305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1bdfd0bf72ae4f3963e64b34d95501e0d2519f1fddf366859182d3cbc30fd9`  
		Last Modified: Tue, 04 Feb 2025 05:12:27 GMT  
		Size: 1.3 MB (1260531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49345faedbef95e78c7480c3e88bd390e45ff60b758a8ae1f768bd4ceada482`  
		Last Modified: Tue, 04 Feb 2025 05:12:27 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bf52a3188788cbb838b8d4a75624fc409328a3f2168c02f63ba3f6adc4ddd8`  
		Last Modified: Tue, 04 Feb 2025 05:12:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:dd3a185dcbb98130c88a3525aa9e7697df859c3c4f9cf0a28481500d4ce9f96a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dda5672c78a463481b13d1a9dd18e83c8cb05d4b901cb9609b3bba27dfe31230`

```dockerfile
```

-	Layers:
	-	`sha256:0b1bc32d1fda8af809796a1814f321de4bbfca145293aca905206f7d57f70077`  
		Last Modified: Tue, 04 Feb 2025 05:12:27 GMT  
		Size: 2.3 MB (2289622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38e4993eec3a8b75af870e911804786af2a7938874d6f0cdf2157d77dd395e75`  
		Last Modified: Tue, 04 Feb 2025 05:12:27 GMT  
		Size: 21.4 KB (21419 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:99e98590099d2d337986980eeb79c3be0410599530aedcb0565f1b0fd7a7cd26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32955938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:218fe1071938e177eaf04cd6fafbdc37a820e5600e864659206f847e6457d2d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sun, 02 Feb 2025 07:54:12 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3e0bbec4e230ba69d1863d0cfc4bb4ffd41f22f10ffc6acdc5e7b83ecde34c`  
		Last Modified: Tue, 04 Feb 2025 04:28:42 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9dd28ef3cfec128e7a1800f6f22aaa8ea274fb08d0461d882a3cfd4f2186d4`  
		Last Modified: Tue, 04 Feb 2025 04:28:42 GMT  
		Size: 2.5 MB (2500678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e809c489bd7a749f8dd5e42f875574f90c71a4a1aeb4a6d5f78fb38f4dfe91c`  
		Last Modified: Tue, 04 Feb 2025 04:28:42 GMT  
		Size: 1.3 MB (1266291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0569ca3484d7c418601aa4a1d9c03b3a201ae7a07615a5177306ffb6706d0e69`  
		Last Modified: Tue, 04 Feb 2025 04:28:42 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96ec23ce107bcd0877feb48601e1a40ecb123ecd1a8a830fd10bbba4a1ce72a`  
		Last Modified: Tue, 04 Feb 2025 04:28:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:966e032dabd37972613a5886d18a681f7e24e3fee197935b5caf17fb36e21b64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e416fe378dee459251a62a2b5b653c4e2743cecc04e7e5219b1c75c5c4685e0`

```dockerfile
```

-	Layers:
	-	`sha256:d0e0a2e88cc36444c10da305fb5dac611a00828958609797a27fe6be0f7144a5`  
		Last Modified: Tue, 04 Feb 2025 04:28:42 GMT  
		Size: 2.3 MB (2286406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3cbad4006e7b93580c2af2558bc8cf21cfe19addf8bf173de3a234902191e69`  
		Last Modified: Tue, 04 Feb 2025 04:28:42 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:fcaa4f5ef9712e2ddca14e6857f1b53fa20672b914cd7b88b6b65445f1832a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31692137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:719403932d2bf7fe31ce1da2e00837219fc634598515ea22717f233d4c45b21c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sun, 02 Feb 2025 07:54:12 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1738540800'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:60fe4951c23056512065fcf1948d3167c5aa5d83d4bfd2829494b7d09b4fe661`  
		Last Modified: Tue, 04 Feb 2025 01:38:47 GMT  
		Size: 28.5 MB (28486581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006e6bf1f5c579c425dd6a7045b45795f463f886bf4ee3532c5964da484e77c4`  
		Last Modified: Tue, 04 Feb 2025 05:36:04 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4620497505845e0aede51939832fe2feb1e84e662ca22647506c9e403a4630`  
		Last Modified: Tue, 04 Feb 2025 05:36:05 GMT  
		Size: 1.9 MB (1943191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbe6e63eb850a0d15f3fb3ce772dc8a193c1b9ead3f64bc87ea9db83a818e31`  
		Last Modified: Tue, 04 Feb 2025 05:36:05 GMT  
		Size: 1.3 MB (1260854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40e7ec508708863f095d5fd6aeac52dffd7f20c336c28d94a7fad02f2f51a29`  
		Last Modified: Tue, 04 Feb 2025 05:36:05 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd558b6f1714e94bee89e0cf11e0ea1af8a90cc74c1b99553e6313974bea9d6`  
		Last Modified: Tue, 04 Feb 2025 05:36:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:10a2ecdde0367c592a37e2094ddcfc7edb98d5d73d5bbdfd7d7069f11468f41b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a6d8d3fb499ac955955b2c9f4e9776ff914141d14adeea588a371ce4cff3bd`

```dockerfile
```

-	Layers:
	-	`sha256:e0a5ca44660b9368be372266be4aefc4be704e101067286cf36e1b06e2f07cdb`  
		Last Modified: Tue, 04 Feb 2025 05:36:04 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:31e531e504071c6297e43ec0359e37dd60aafa37b23f2cfd572d6992a4a8f699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36085904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029e8e5e0f017ebe180b7e7e42e69b8469d48d66dccc36f4ee94cc70531ce2ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sun, 02 Feb 2025 07:54:12 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 01:38:01 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2554b2c9b1b0eaccf71963ebdaa720beba7c4729f900596b8bb7e99b6919b1`  
		Last Modified: Tue, 04 Feb 2025 04:54:07 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26b95187bf5085dc8573c96b467801af0c38567ad032cafcf7565bc83e8c10c`  
		Last Modified: Tue, 04 Feb 2025 04:54:07 GMT  
		Size: 2.7 MB (2708613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229261d8ebd7f1a31858565844b84e86a020984fbe64d3a62b3d685417159948`  
		Last Modified: Tue, 04 Feb 2025 04:54:07 GMT  
		Size: 1.3 MB (1330999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9891f8d1e557cafb091f637b3db5cdb8b11696ed2c249fdfb769b4a33d3078`  
		Last Modified: Tue, 04 Feb 2025 04:54:07 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25470058ddabb0f895e9d1799ac944c98f6b75317f06a627f30187b8fdfb0a36`  
		Last Modified: Tue, 04 Feb 2025 04:54:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f914e538671a572729170958d470dfabd855aa80ce53b25a0d7a5204c1b33a0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c38e1164115528d1af0164fb9dc030c96e5f940b1dc40e46c04e9dcf03b3df0`

```dockerfile
```

-	Layers:
	-	`sha256:1f9e966fff09eb8597e726dee37d8077951c4a8388ca91a79ec2ce5e5e913c60`  
		Last Modified: Tue, 04 Feb 2025 04:54:07 GMT  
		Size: 2.3 MB (2293679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd28c7586277dc4f00031d57a5fe00d338e5418c714bd57259f440b8bcbc728c`  
		Last Modified: Tue, 04 Feb 2025 04:54:07 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:682eb0a0e7d4cd11f8b9a3e1290057c1e796788a4618a3ac5c82cb7df58933d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30261734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df80d341f0efbcde25b92f3e1b797f27625a16d555bfca98f22061de2f298a69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sun, 02 Feb 2025 07:54:12 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe1d1bee073fc6fc7edf8762994dd33eb7f445c49d726accfb91332a242d958`  
		Last Modified: Tue, 04 Feb 2025 04:55:22 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8785d74590885c81503a45644906e34c354e69c862dad662a22f498c866adece`  
		Last Modified: Tue, 04 Feb 2025 04:55:23 GMT  
		Size: 2.2 MB (2156364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b1bdeb9a486655fb1fbc129ff4907a4c86b484a6c915d9a05aa040888c89e7`  
		Last Modified: Tue, 04 Feb 2025 04:55:23 GMT  
		Size: 1.2 MB (1245232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5b08891d9cb8dac889b466249456f8845d8eb3f7434466b96b09d5431e01a4`  
		Last Modified: Tue, 04 Feb 2025 04:55:23 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a8546468c2d277e130e611d05861380d2da0d3147183727229235f1e512e35`  
		Last Modified: Tue, 04 Feb 2025 04:55:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f0f959f8ecfee4cbf470f9361e8b57b4e533448ff02939b9502eab73afb04b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e145048ce46bf258188b341bfa77adce8eb7da0fbb8839645158ffc3497c4c9a`

```dockerfile
```

-	Layers:
	-	`sha256:517488b2faa7932817aca91e747eb050e4f797d147f86ea3652de77ba7bb9518`  
		Last Modified: Tue, 04 Feb 2025 04:55:23 GMT  
		Size: 2.3 MB (2289021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94edb64050cfbde612663e71dc905e22225a42f70f6a8d44f18e0667df39e53c`  
		Last Modified: Tue, 04 Feb 2025 04:55:23 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.36`

**does not exist** (yet?)

## `memcached:1.6.36-alpine`

**does not exist** (yet?)

## `memcached:1.6.36-alpine3.21`

**does not exist** (yet?)

## `memcached:1.6.36-bookworm`

**does not exist** (yet?)

## `memcached:alpine`

```console
$ docker pull memcached@sha256:b093f7f64a39f20b8f4a671f9c6656eff26821a3c97037a8019448040d6298bd
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
$ docker pull memcached@sha256:c497fc5a323c178e0914eca2500dcf9fa3b21ca2f9932dbc92b51ef6145cf2be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4716328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d2b29f4542cd1fc099ca3146ac53cc0eab71776ce1c029fee5d58a57c38a52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9604a91067e8818541aa31757690c9f8ebf60c58be004baded0767c0999267b8`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592b1cc3d47258eaa3cb466a887cb58e0b2a4176818d1c9a721698abf9337d94`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 104.7 KB (104686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5a55a29aba2a2a27962f2b36f259f5fac81a49009fc7c06020fc992eb6d5da`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 968.6 KB (968568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4786022d0e1453ad1d978f79f50839ba76e4f7c73310640921e5bc212537d6e`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da16032c7fbc5aedc09cd3d43a996943828a731b3ed781664abcf257bdfb65c`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:f4b6389438043b9d6191b9e22e19659d23258e22f0e414f51cb0945287141162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e696a02855f507b1b926a60cf07265433c5ab415467633243c2536753b3090`

```dockerfile
```

-	Layers:
	-	`sha256:16a139d5ff76ba43b3c520a2be58514f36e0ad4a7b0f9adfb6b9c80acb97219d`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 93.6 KB (93627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d8f0efc7a1d5a7dc78219efc6849e55d842b9a5e34ff6bee956735b7cbe2967`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:4d52a91c9cf3612ab9f44d1ecc192f150659288c8826932187c7ab3ed5f8dc9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5082815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef0a8813bf35c3ce3d0d0f9967d27c56db3fb8dc2fd7f31ab4cd3fc1f7cd209`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a202407430ec08b7a5bfb94689fc70aed855fbc1cd8b62ce145147fc5278b7a8`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82c0f1024964e8e055db8178bb0d2595a4a66f7398bffe83d6176cc192ac77e`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 120.8 KB (120783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46624d73285a34a525d44fb1f293cdb9fc95ebfb5b305918bc6a1ff77019fda`  
		Last Modified: Mon, 03 Feb 2025 23:32:18 GMT  
		Size: 968.3 KB (968310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099e6e9c12eb4dfbd63c3bc7cec8de6eb251173a42983594f30413921e56380a`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348cf5001affc34a6f03be6a7f413a6cc377fa11350026995dd53f7db78b85a1`  
		Last Modified: Mon, 03 Feb 2025 23:32:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:631105e348c97a01de96919b82284f666d3283712a23e1b5670c31c88810f40c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff4582dcb2cdec3cfb7590e5b6ade8162439d38a001ff6c08fa81f7d08c669e`

```dockerfile
```

-	Layers:
	-	`sha256:8f4375fd6e27a5ee655f47249469c2214b367ec0146b4e8769a97c6afa3d2829`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 93.7 KB (93731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4bf5d12011dbaae039aec13c76a68a64809e478a3b79d0090ba407f1d4f7c61`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:1f1e5941bca8da9b3aeabcc13c55fe90fc40f9c6476645c19172e508e5302723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4534153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2936f0dd081882d9f0da9ea6113e9780627d3a665a9d909de817c696fac9620`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300aaa75d91b0206b7556a721baaed9f7000ccf73ab8deda59e1cb428ec870f9`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ac94f71cda4f155944d630f60f3e31780c4a97ced13f6c61385dc7e95df429`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 109.5 KB (109465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73b7528b6c4fdfdf4075a75f9e28334049f5461f39426f3b2f983792188c971`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 960.2 KB (960204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb441509973ed0be28152c5ef6c85917a0de941839cd68559be4ecfcc273b17`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e6efaa8bc767e6ef9d48f3b7547a57b7d72964bbb765d7a66481f3f3b36dd1`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:0de21b11722d02a9d2cfc6acf661c6d755de360f4c1f70e7af549cac29e5aef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10be0a79af6bc5d121d12aa89f8e2191eb25f2533cfb4e1de067b3e0bbe82834`

```dockerfile
```

-	Layers:
	-	`sha256:c57cf3137ea2641a839877ddcf3a6065504f38c2ea4f2b7671c1776008e2cfcf`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 93.6 KB (93582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdf7d0d4ee2052676f3563869639942945b1cba543484223915cb33df997a5f0`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 19.5 KB (19512 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:913b5bd251bfe9202c3f0302d3c8c5a4ea3fb7f40f73e8561542c93db1c9d6c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4706076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8083b854e648814b258458b24e3039ade25fa9e63e50b6fb79db7cb05d2ee3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a841f248cda34139a77fd6ab9691e34b7d7dae6dfaedc45a2304aa25c07536`  
		Last Modified: Mon, 03 Feb 2025 23:32:07 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ccea169aa483a5ea29ebe89aa46469affffa54252ac8df2ee75acc10eca2e0`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 124.3 KB (124280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f40e8d115f7e602d9931eaa3e7f41c17dc35a40994befa787615cbd877d430`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 1.0 MB (1006836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf17c8f5e90551f91b3474eb46d197d4ac28e21bf5cb9aaa79eea5b851db371`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9971977dd87dcc447ad6eccbe529fc3c7d6b7dc6b74a4d74fb519c86565318f4`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:04513dfc421f21abd4cd316a69b57cdbfd9d92844a16e9d55eec6a4592cd22d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569bb3d3624a47ed75650ef0a92bfc59d63af78afe540637c817793e9cf4b6d6`

```dockerfile
```

-	Layers:
	-	`sha256:ba709bd16c5785bcfce6f9a8fd6e1d834e101c00d1ed2e018a68a999ec43825b`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 91.7 KB (91734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bc2aa4695d41b4a46d039e0e91f623f3f7aadfd866f0e477637054a37fc5127`  
		Last Modified: Mon, 03 Feb 2025 23:32:07 GMT  
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
$ docker pull memcached@sha256:624036093e557f56a4d500c780f34193af25d5c3b73f8bb08329b579e72b7d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4570369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e3d248b914c5043ad7dc370403b9ea51bf62f972a6f7cf694a023ce14ac2d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223127e71140d5e120db85abbcc459b2ca368e042d165466a1ab8b72ada743f8`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf0ecced8267cdc41066ee8044aa4a0e35e951cba2f51a411ecbfb2cee29819`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 113.5 KB (113450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b7e62f8ce2395ffab9dff807ea14960a2cfa247d7c8a418a5e92d3b4d883f8`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 988.7 KB (988692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed293040c38a686b287b82c3a47615ca2f9034912964f5ce7e832241db526879`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1254936a9326dadc90d0b29d805e446f753a49826f2d9ea9308f5e847d6b7d4`  
		Last Modified: Mon, 03 Feb 2025 23:34:11 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:51c253df33d2a17a62bac93fdc69e4be991e6f4b9e6015eff29ad965c1e58628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 KB (111245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4b6a687d069c6e737d3a9cfa50af30753d0165aa04019517f2f6951bad7feb6`

```dockerfile
```

-	Layers:
	-	`sha256:4e1be19ae90b5f3b2e2b65ad7605851c11804d593bec1671c444bd7aadc3063d`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 91.7 KB (91676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:415673db52745ddb45aa4c05424023581f2903f3acd2578ac008e4857c8ca11b`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 19.6 KB (19569 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine3.21`

```console
$ docker pull memcached@sha256:918f8d596494e94538b93f92d629c3d20efa4d5ca8b0302bf672b65f974c5617
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
$ docker pull memcached@sha256:c497fc5a323c178e0914eca2500dcf9fa3b21ca2f9932dbc92b51ef6145cf2be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4716328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d2b29f4542cd1fc099ca3146ac53cc0eab71776ce1c029fee5d58a57c38a52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9604a91067e8818541aa31757690c9f8ebf60c58be004baded0767c0999267b8`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592b1cc3d47258eaa3cb466a887cb58e0b2a4176818d1c9a721698abf9337d94`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 104.7 KB (104686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5a55a29aba2a2a27962f2b36f259f5fac81a49009fc7c06020fc992eb6d5da`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 968.6 KB (968568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4786022d0e1453ad1d978f79f50839ba76e4f7c73310640921e5bc212537d6e`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da16032c7fbc5aedc09cd3d43a996943828a731b3ed781664abcf257bdfb65c`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:f4b6389438043b9d6191b9e22e19659d23258e22f0e414f51cb0945287141162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e696a02855f507b1b926a60cf07265433c5ab415467633243c2536753b3090`

```dockerfile
```

-	Layers:
	-	`sha256:16a139d5ff76ba43b3c520a2be58514f36e0ad4a7b0f9adfb6b9c80acb97219d`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 93.6 KB (93627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d8f0efc7a1d5a7dc78219efc6849e55d842b9a5e34ff6bee956735b7cbe2967`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:4d52a91c9cf3612ab9f44d1ecc192f150659288c8826932187c7ab3ed5f8dc9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5082815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef0a8813bf35c3ce3d0d0f9967d27c56db3fb8dc2fd7f31ab4cd3fc1f7cd209`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a202407430ec08b7a5bfb94689fc70aed855fbc1cd8b62ce145147fc5278b7a8`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82c0f1024964e8e055db8178bb0d2595a4a66f7398bffe83d6176cc192ac77e`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 120.8 KB (120783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46624d73285a34a525d44fb1f293cdb9fc95ebfb5b305918bc6a1ff77019fda`  
		Last Modified: Mon, 03 Feb 2025 23:32:18 GMT  
		Size: 968.3 KB (968310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099e6e9c12eb4dfbd63c3bc7cec8de6eb251173a42983594f30413921e56380a`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348cf5001affc34a6f03be6a7f413a6cc377fa11350026995dd53f7db78b85a1`  
		Last Modified: Mon, 03 Feb 2025 23:32:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:631105e348c97a01de96919b82284f666d3283712a23e1b5670c31c88810f40c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff4582dcb2cdec3cfb7590e5b6ade8162439d38a001ff6c08fa81f7d08c669e`

```dockerfile
```

-	Layers:
	-	`sha256:8f4375fd6e27a5ee655f47249469c2214b367ec0146b4e8769a97c6afa3d2829`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 93.7 KB (93731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4bf5d12011dbaae039aec13c76a68a64809e478a3b79d0090ba407f1d4f7c61`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.21` - linux; 386

```console
$ docker pull memcached@sha256:1f1e5941bca8da9b3aeabcc13c55fe90fc40f9c6476645c19172e508e5302723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4534153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2936f0dd081882d9f0da9ea6113e9780627d3a665a9d909de817c696fac9620`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300aaa75d91b0206b7556a721baaed9f7000ccf73ab8deda59e1cb428ec870f9`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ac94f71cda4f155944d630f60f3e31780c4a97ced13f6c61385dc7e95df429`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 109.5 KB (109465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73b7528b6c4fdfdf4075a75f9e28334049f5461f39426f3b2f983792188c971`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 960.2 KB (960204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb441509973ed0be28152c5ef6c85917a0de941839cd68559be4ecfcc273b17`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e6efaa8bc767e6ef9d48f3b7547a57b7d72964bbb765d7a66481f3f3b36dd1`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:0de21b11722d02a9d2cfc6acf661c6d755de360f4c1f70e7af549cac29e5aef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10be0a79af6bc5d121d12aa89f8e2191eb25f2533cfb4e1de067b3e0bbe82834`

```dockerfile
```

-	Layers:
	-	`sha256:c57cf3137ea2641a839877ddcf3a6065504f38c2ea4f2b7671c1776008e2cfcf`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 93.6 KB (93582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdf7d0d4ee2052676f3563869639942945b1cba543484223915cb33df997a5f0`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 19.5 KB (19512 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.21` - linux; ppc64le

```console
$ docker pull memcached@sha256:913b5bd251bfe9202c3f0302d3c8c5a4ea3fb7f40f73e8561542c93db1c9d6c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4706076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8083b854e648814b258458b24e3039ade25fa9e63e50b6fb79db7cb05d2ee3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a841f248cda34139a77fd6ab9691e34b7d7dae6dfaedc45a2304aa25c07536`  
		Last Modified: Mon, 03 Feb 2025 23:32:07 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ccea169aa483a5ea29ebe89aa46469affffa54252ac8df2ee75acc10eca2e0`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 124.3 KB (124280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f40e8d115f7e602d9931eaa3e7f41c17dc35a40994befa787615cbd877d430`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 1.0 MB (1006836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf17c8f5e90551f91b3474eb46d197d4ac28e21bf5cb9aaa79eea5b851db371`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9971977dd87dcc447ad6eccbe529fc3c7d6b7dc6b74a4d74fb519c86565318f4`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:04513dfc421f21abd4cd316a69b57cdbfd9d92844a16e9d55eec6a4592cd22d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569bb3d3624a47ed75650ef0a92bfc59d63af78afe540637c817793e9cf4b6d6`

```dockerfile
```

-	Layers:
	-	`sha256:ba709bd16c5785bcfce6f9a8fd6e1d834e101c00d1ed2e018a68a999ec43825b`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 91.7 KB (91734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bc2aa4695d41b4a46d039e0e91f623f3f7aadfd866f0e477637054a37fc5127`  
		Last Modified: Mon, 03 Feb 2025 23:32:07 GMT  
		Size: 19.6 KB (19648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.21` - linux; s390x

```console
$ docker pull memcached@sha256:624036093e557f56a4d500c780f34193af25d5c3b73f8bb08329b579e72b7d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4570369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e3d248b914c5043ad7dc370403b9ea51bf62f972a6f7cf694a023ce14ac2d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223127e71140d5e120db85abbcc459b2ca368e042d165466a1ab8b72ada743f8`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf0ecced8267cdc41066ee8044aa4a0e35e951cba2f51a411ecbfb2cee29819`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 113.5 KB (113450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b7e62f8ce2395ffab9dff807ea14960a2cfa247d7c8a418a5e92d3b4d883f8`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 988.7 KB (988692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed293040c38a686b287b82c3a47615ca2f9034912964f5ce7e832241db526879`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1254936a9326dadc90d0b29d805e446f753a49826f2d9ea9308f5e847d6b7d4`  
		Last Modified: Mon, 03 Feb 2025 23:34:11 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:51c253df33d2a17a62bac93fdc69e4be991e6f4b9e6015eff29ad965c1e58628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 KB (111245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4b6a687d069c6e737d3a9cfa50af30753d0165aa04019517f2f6951bad7feb6`

```dockerfile
```

-	Layers:
	-	`sha256:4e1be19ae90b5f3b2e2b65ad7605851c11804d593bec1671c444bd7aadc3063d`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 91.7 KB (91676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:415673db52745ddb45aa4c05424023581f2903f3acd2578ac008e4857c8ca11b`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 19.6 KB (19569 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:bookworm`

```console
$ docker pull memcached@sha256:abcf6f9aa41d318eec8545d95d7617bf392a2548b494ba91502da544ce156c67
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
$ docker pull memcached@sha256:fe6175b895bf327f0a49f18f24f6d63fdff1244d2bb01b66be828dd242a8c896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31972673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd546324997c0a40f0c03f0517211bfe65c08348d50f63548f81fe77b85e4ced`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sun, 02 Feb 2025 07:54:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fedffee92af44a379d24a5aa33a3ba6b7c2506c5f5364f7176ade65d9524bc`  
		Last Modified: Tue, 04 Feb 2025 04:28:58 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c2f9f9913f583649e29a3a2d436a5ae83f661daa9a4a3ec851d0e59fd9df89`  
		Last Modified: Tue, 04 Feb 2025 04:28:58 GMT  
		Size: 2.5 MB (2491785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbec463a35a75ca82fc40395dc573259b68925a58c1d807b30369d1aa0ae0b6b`  
		Last Modified: Tue, 04 Feb 2025 04:28:58 GMT  
		Size: 1.3 MB (1267074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1639ac6067c6a735763a45940530325312576704c8d26ebbfe6ed98cbdcec6`  
		Last Modified: Tue, 04 Feb 2025 04:28:58 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e075c77694a0d33203ecd6f3013d1db8992d1805e1d2b2f0ae7e5844e818e1`  
		Last Modified: Tue, 04 Feb 2025 04:28:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:0c5685395f6f2c3ccba97d1243d14b1b76ced16fa604c5dd74ff526d9ae21669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f96994adb795e76f47fa54962705d27228878c09c30dbb5cc78dfda05a0e810c`

```dockerfile
```

-	Layers:
	-	`sha256:776bdd6252940f9f9beec60d69803e592d9f81c6f6ac3af63ac8c8286b7d5231`  
		Last Modified: Tue, 04 Feb 2025 04:28:58 GMT  
		Size: 2.3 MB (2289307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ae8c4ca198567328bf1e310d5250ead344a3f33e5e25f7ebaaf6f85953fa2f8`  
		Last Modified: Tue, 04 Feb 2025 04:28:58 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:3e23b25ff5492ba265c6beb3f7b66439db09a21058605ec99fa81439625177e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29079320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bda06acae7b451db750946fe903698d277afa7242f5ca0c376b741329963c34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sun, 02 Feb 2025 07:54:12 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aa8576c673e5a651f7450bee7603a12ac6168051fdd5b2411678987e180cad6e`  
		Last Modified: Tue, 04 Feb 2025 01:38:28 GMT  
		Size: 25.7 MB (25736549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d03c1f12f429fcd661498f32bc4e1c1e6a1e4189bd6014e71da057147e2286`  
		Last Modified: Tue, 04 Feb 2025 04:58:18 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7e25c626324a280a0e7be83a5642bb48a551515d4c38cb544c66904fcf10bb`  
		Last Modified: Tue, 04 Feb 2025 04:58:19 GMT  
		Size: 2.1 MB (2096073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e66403ec68cf3c2e1ff6271437414ce28660419f8d6c31f24edf02c56043262`  
		Last Modified: Tue, 04 Feb 2025 04:58:19 GMT  
		Size: 1.2 MB (1245186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f749b98d44a3942a1e45b8f89dc5b9b45b3305ce5bfa145f543463bcf50eb7b`  
		Last Modified: Tue, 04 Feb 2025 04:58:18 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:703069b289a6d2efdf95eef836d36ea4221f0d8e81a15ea1d1c57de352a39674`  
		Last Modified: Tue, 04 Feb 2025 04:58:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:aa7da31c13e723cc51b38e05c1d6e83ea69c4681b2c0c2d799c80fb66c1b4785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d4e5a0b18ec46d6e5b2f35fcc7b750e3caff802347cd8ae31c822368dee1882`

```dockerfile
```

-	Layers:
	-	`sha256:48a6ab4752d86991553683ca36c648def5b52c5c695e8b1647ab32b21c4d9729`  
		Last Modified: Tue, 04 Feb 2025 04:58:19 GMT  
		Size: 2.3 MB (2292845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c4499883bd4502cc0726091a993acdeada7afd3e77f04c3b57e639ec56412a7`  
		Last Modified: Tue, 04 Feb 2025 04:58:18 GMT  
		Size: 21.4 KB (21368 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:fc1b1df1cc951fa0c913d4130b817fbf6f2e471598ffabe70cc99a1517810f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31658229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4edc43a8d642cf5350fa9c2bdcd33cd413c992506a36a31c16473b2865332b34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sun, 02 Feb 2025 07:54:12 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be3b898de6ed2c686c435db2ea65d18020b171ffb60cbe49d3e443270a750c5`  
		Last Modified: Tue, 04 Feb 2025 05:12:27 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f228ff9270a43bec782505e8c0498a642411d336d532a20f2d9f5c75ff729440`  
		Last Modified: Tue, 04 Feb 2025 05:12:27 GMT  
		Size: 2.4 MB (2355305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1bdfd0bf72ae4f3963e64b34d95501e0d2519f1fddf366859182d3cbc30fd9`  
		Last Modified: Tue, 04 Feb 2025 05:12:27 GMT  
		Size: 1.3 MB (1260531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49345faedbef95e78c7480c3e88bd390e45ff60b758a8ae1f768bd4ceada482`  
		Last Modified: Tue, 04 Feb 2025 05:12:27 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bf52a3188788cbb838b8d4a75624fc409328a3f2168c02f63ba3f6adc4ddd8`  
		Last Modified: Tue, 04 Feb 2025 05:12:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:dd3a185dcbb98130c88a3525aa9e7697df859c3c4f9cf0a28481500d4ce9f96a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dda5672c78a463481b13d1a9dd18e83c8cb05d4b901cb9609b3bba27dfe31230`

```dockerfile
```

-	Layers:
	-	`sha256:0b1bc32d1fda8af809796a1814f321de4bbfca145293aca905206f7d57f70077`  
		Last Modified: Tue, 04 Feb 2025 05:12:27 GMT  
		Size: 2.3 MB (2289622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38e4993eec3a8b75af870e911804786af2a7938874d6f0cdf2157d77dd395e75`  
		Last Modified: Tue, 04 Feb 2025 05:12:27 GMT  
		Size: 21.4 KB (21419 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; 386

```console
$ docker pull memcached@sha256:99e98590099d2d337986980eeb79c3be0410599530aedcb0565f1b0fd7a7cd26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32955938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:218fe1071938e177eaf04cd6fafbdc37a820e5600e864659206f847e6457d2d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sun, 02 Feb 2025 07:54:12 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3e0bbec4e230ba69d1863d0cfc4bb4ffd41f22f10ffc6acdc5e7b83ecde34c`  
		Last Modified: Tue, 04 Feb 2025 04:28:42 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9dd28ef3cfec128e7a1800f6f22aaa8ea274fb08d0461d882a3cfd4f2186d4`  
		Last Modified: Tue, 04 Feb 2025 04:28:42 GMT  
		Size: 2.5 MB (2500678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e809c489bd7a749f8dd5e42f875574f90c71a4a1aeb4a6d5f78fb38f4dfe91c`  
		Last Modified: Tue, 04 Feb 2025 04:28:42 GMT  
		Size: 1.3 MB (1266291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0569ca3484d7c418601aa4a1d9c03b3a201ae7a07615a5177306ffb6706d0e69`  
		Last Modified: Tue, 04 Feb 2025 04:28:42 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96ec23ce107bcd0877feb48601e1a40ecb123ecd1a8a830fd10bbba4a1ce72a`  
		Last Modified: Tue, 04 Feb 2025 04:28:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:966e032dabd37972613a5886d18a681f7e24e3fee197935b5caf17fb36e21b64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e416fe378dee459251a62a2b5b653c4e2743cecc04e7e5219b1c75c5c4685e0`

```dockerfile
```

-	Layers:
	-	`sha256:d0e0a2e88cc36444c10da305fb5dac611a00828958609797a27fe6be0f7144a5`  
		Last Modified: Tue, 04 Feb 2025 04:28:42 GMT  
		Size: 2.3 MB (2286406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3cbad4006e7b93580c2af2558bc8cf21cfe19addf8bf173de3a234902191e69`  
		Last Modified: Tue, 04 Feb 2025 04:28:42 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:fcaa4f5ef9712e2ddca14e6857f1b53fa20672b914cd7b88b6b65445f1832a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31692137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:719403932d2bf7fe31ce1da2e00837219fc634598515ea22717f233d4c45b21c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sun, 02 Feb 2025 07:54:12 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1738540800'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:60fe4951c23056512065fcf1948d3167c5aa5d83d4bfd2829494b7d09b4fe661`  
		Last Modified: Tue, 04 Feb 2025 01:38:47 GMT  
		Size: 28.5 MB (28486581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006e6bf1f5c579c425dd6a7045b45795f463f886bf4ee3532c5964da484e77c4`  
		Last Modified: Tue, 04 Feb 2025 05:36:04 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4620497505845e0aede51939832fe2feb1e84e662ca22647506c9e403a4630`  
		Last Modified: Tue, 04 Feb 2025 05:36:05 GMT  
		Size: 1.9 MB (1943191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbe6e63eb850a0d15f3fb3ce772dc8a193c1b9ead3f64bc87ea9db83a818e31`  
		Last Modified: Tue, 04 Feb 2025 05:36:05 GMT  
		Size: 1.3 MB (1260854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40e7ec508708863f095d5fd6aeac52dffd7f20c336c28d94a7fad02f2f51a29`  
		Last Modified: Tue, 04 Feb 2025 05:36:05 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd558b6f1714e94bee89e0cf11e0ea1af8a90cc74c1b99553e6313974bea9d6`  
		Last Modified: Tue, 04 Feb 2025 05:36:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:10a2ecdde0367c592a37e2094ddcfc7edb98d5d73d5bbdfd7d7069f11468f41b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a6d8d3fb499ac955955b2c9f4e9776ff914141d14adeea588a371ce4cff3bd`

```dockerfile
```

-	Layers:
	-	`sha256:e0a5ca44660b9368be372266be4aefc4be704e101067286cf36e1b06e2f07cdb`  
		Last Modified: Tue, 04 Feb 2025 05:36:04 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:31e531e504071c6297e43ec0359e37dd60aafa37b23f2cfd572d6992a4a8f699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36085904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029e8e5e0f017ebe180b7e7e42e69b8469d48d66dccc36f4ee94cc70531ce2ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sun, 02 Feb 2025 07:54:12 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 01:38:01 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2554b2c9b1b0eaccf71963ebdaa720beba7c4729f900596b8bb7e99b6919b1`  
		Last Modified: Tue, 04 Feb 2025 04:54:07 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26b95187bf5085dc8573c96b467801af0c38567ad032cafcf7565bc83e8c10c`  
		Last Modified: Tue, 04 Feb 2025 04:54:07 GMT  
		Size: 2.7 MB (2708613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229261d8ebd7f1a31858565844b84e86a020984fbe64d3a62b3d685417159948`  
		Last Modified: Tue, 04 Feb 2025 04:54:07 GMT  
		Size: 1.3 MB (1330999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9891f8d1e557cafb091f637b3db5cdb8b11696ed2c249fdfb769b4a33d3078`  
		Last Modified: Tue, 04 Feb 2025 04:54:07 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25470058ddabb0f895e9d1799ac944c98f6b75317f06a627f30187b8fdfb0a36`  
		Last Modified: Tue, 04 Feb 2025 04:54:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f914e538671a572729170958d470dfabd855aa80ce53b25a0d7a5204c1b33a0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c38e1164115528d1af0164fb9dc030c96e5f940b1dc40e46c04e9dcf03b3df0`

```dockerfile
```

-	Layers:
	-	`sha256:1f9e966fff09eb8597e726dee37d8077951c4a8388ca91a79ec2ce5e5e913c60`  
		Last Modified: Tue, 04 Feb 2025 04:54:07 GMT  
		Size: 2.3 MB (2293679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd28c7586277dc4f00031d57a5fe00d338e5418c714bd57259f440b8bcbc728c`  
		Last Modified: Tue, 04 Feb 2025 04:54:07 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:682eb0a0e7d4cd11f8b9a3e1290057c1e796788a4618a3ac5c82cb7df58933d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30261734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df80d341f0efbcde25b92f3e1b797f27625a16d555bfca98f22061de2f298a69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sun, 02 Feb 2025 07:54:12 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe1d1bee073fc6fc7edf8762994dd33eb7f445c49d726accfb91332a242d958`  
		Last Modified: Tue, 04 Feb 2025 04:55:22 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8785d74590885c81503a45644906e34c354e69c862dad662a22f498c866adece`  
		Last Modified: Tue, 04 Feb 2025 04:55:23 GMT  
		Size: 2.2 MB (2156364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b1bdeb9a486655fb1fbc129ff4907a4c86b484a6c915d9a05aa040888c89e7`  
		Last Modified: Tue, 04 Feb 2025 04:55:23 GMT  
		Size: 1.2 MB (1245232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5b08891d9cb8dac889b466249456f8845d8eb3f7434466b96b09d5431e01a4`  
		Last Modified: Tue, 04 Feb 2025 04:55:23 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a8546468c2d277e130e611d05861380d2da0d3147183727229235f1e512e35`  
		Last Modified: Tue, 04 Feb 2025 04:55:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f0f959f8ecfee4cbf470f9361e8b57b4e533448ff02939b9502eab73afb04b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e145048ce46bf258188b341bfa77adce8eb7da0fbb8839645158ffc3497c4c9a`

```dockerfile
```

-	Layers:
	-	`sha256:517488b2faa7932817aca91e747eb050e4f797d147f86ea3652de77ba7bb9518`  
		Last Modified: Tue, 04 Feb 2025 04:55:23 GMT  
		Size: 2.3 MB (2289021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94edb64050cfbde612663e71dc905e22225a42f70f6a8d44f18e0667df39e53c`  
		Last Modified: Tue, 04 Feb 2025 04:55:23 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:latest`

```console
$ docker pull memcached@sha256:abcf6f9aa41d318eec8545d95d7617bf392a2548b494ba91502da544ce156c67
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
$ docker pull memcached@sha256:fe6175b895bf327f0a49f18f24f6d63fdff1244d2bb01b66be828dd242a8c896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31972673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd546324997c0a40f0c03f0517211bfe65c08348d50f63548f81fe77b85e4ced`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sun, 02 Feb 2025 07:54:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fedffee92af44a379d24a5aa33a3ba6b7c2506c5f5364f7176ade65d9524bc`  
		Last Modified: Tue, 04 Feb 2025 04:28:58 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c2f9f9913f583649e29a3a2d436a5ae83f661daa9a4a3ec851d0e59fd9df89`  
		Last Modified: Tue, 04 Feb 2025 04:28:58 GMT  
		Size: 2.5 MB (2491785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbec463a35a75ca82fc40395dc573259b68925a58c1d807b30369d1aa0ae0b6b`  
		Last Modified: Tue, 04 Feb 2025 04:28:58 GMT  
		Size: 1.3 MB (1267074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1639ac6067c6a735763a45940530325312576704c8d26ebbfe6ed98cbdcec6`  
		Last Modified: Tue, 04 Feb 2025 04:28:58 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e075c77694a0d33203ecd6f3013d1db8992d1805e1d2b2f0ae7e5844e818e1`  
		Last Modified: Tue, 04 Feb 2025 04:28:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:0c5685395f6f2c3ccba97d1243d14b1b76ced16fa604c5dd74ff526d9ae21669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f96994adb795e76f47fa54962705d27228878c09c30dbb5cc78dfda05a0e810c`

```dockerfile
```

-	Layers:
	-	`sha256:776bdd6252940f9f9beec60d69803e592d9f81c6f6ac3af63ac8c8286b7d5231`  
		Last Modified: Tue, 04 Feb 2025 04:28:58 GMT  
		Size: 2.3 MB (2289307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ae8c4ca198567328bf1e310d5250ead344a3f33e5e25f7ebaaf6f85953fa2f8`  
		Last Modified: Tue, 04 Feb 2025 04:28:58 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:3e23b25ff5492ba265c6beb3f7b66439db09a21058605ec99fa81439625177e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29079320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bda06acae7b451db750946fe903698d277afa7242f5ca0c376b741329963c34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sun, 02 Feb 2025 07:54:12 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aa8576c673e5a651f7450bee7603a12ac6168051fdd5b2411678987e180cad6e`  
		Last Modified: Tue, 04 Feb 2025 01:38:28 GMT  
		Size: 25.7 MB (25736549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d03c1f12f429fcd661498f32bc4e1c1e6a1e4189bd6014e71da057147e2286`  
		Last Modified: Tue, 04 Feb 2025 04:58:18 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7e25c626324a280a0e7be83a5642bb48a551515d4c38cb544c66904fcf10bb`  
		Last Modified: Tue, 04 Feb 2025 04:58:19 GMT  
		Size: 2.1 MB (2096073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e66403ec68cf3c2e1ff6271437414ce28660419f8d6c31f24edf02c56043262`  
		Last Modified: Tue, 04 Feb 2025 04:58:19 GMT  
		Size: 1.2 MB (1245186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f749b98d44a3942a1e45b8f89dc5b9b45b3305ce5bfa145f543463bcf50eb7b`  
		Last Modified: Tue, 04 Feb 2025 04:58:18 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:703069b289a6d2efdf95eef836d36ea4221f0d8e81a15ea1d1c57de352a39674`  
		Last Modified: Tue, 04 Feb 2025 04:58:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:aa7da31c13e723cc51b38e05c1d6e83ea69c4681b2c0c2d799c80fb66c1b4785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d4e5a0b18ec46d6e5b2f35fcc7b750e3caff802347cd8ae31c822368dee1882`

```dockerfile
```

-	Layers:
	-	`sha256:48a6ab4752d86991553683ca36c648def5b52c5c695e8b1647ab32b21c4d9729`  
		Last Modified: Tue, 04 Feb 2025 04:58:19 GMT  
		Size: 2.3 MB (2292845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c4499883bd4502cc0726091a993acdeada7afd3e77f04c3b57e639ec56412a7`  
		Last Modified: Tue, 04 Feb 2025 04:58:18 GMT  
		Size: 21.4 KB (21368 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:fc1b1df1cc951fa0c913d4130b817fbf6f2e471598ffabe70cc99a1517810f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31658229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4edc43a8d642cf5350fa9c2bdcd33cd413c992506a36a31c16473b2865332b34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sun, 02 Feb 2025 07:54:12 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be3b898de6ed2c686c435db2ea65d18020b171ffb60cbe49d3e443270a750c5`  
		Last Modified: Tue, 04 Feb 2025 05:12:27 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f228ff9270a43bec782505e8c0498a642411d336d532a20f2d9f5c75ff729440`  
		Last Modified: Tue, 04 Feb 2025 05:12:27 GMT  
		Size: 2.4 MB (2355305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1bdfd0bf72ae4f3963e64b34d95501e0d2519f1fddf366859182d3cbc30fd9`  
		Last Modified: Tue, 04 Feb 2025 05:12:27 GMT  
		Size: 1.3 MB (1260531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49345faedbef95e78c7480c3e88bd390e45ff60b758a8ae1f768bd4ceada482`  
		Last Modified: Tue, 04 Feb 2025 05:12:27 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bf52a3188788cbb838b8d4a75624fc409328a3f2168c02f63ba3f6adc4ddd8`  
		Last Modified: Tue, 04 Feb 2025 05:12:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:dd3a185dcbb98130c88a3525aa9e7697df859c3c4f9cf0a28481500d4ce9f96a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dda5672c78a463481b13d1a9dd18e83c8cb05d4b901cb9609b3bba27dfe31230`

```dockerfile
```

-	Layers:
	-	`sha256:0b1bc32d1fda8af809796a1814f321de4bbfca145293aca905206f7d57f70077`  
		Last Modified: Tue, 04 Feb 2025 05:12:27 GMT  
		Size: 2.3 MB (2289622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38e4993eec3a8b75af870e911804786af2a7938874d6f0cdf2157d77dd395e75`  
		Last Modified: Tue, 04 Feb 2025 05:12:27 GMT  
		Size: 21.4 KB (21419 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:99e98590099d2d337986980eeb79c3be0410599530aedcb0565f1b0fd7a7cd26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32955938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:218fe1071938e177eaf04cd6fafbdc37a820e5600e864659206f847e6457d2d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sun, 02 Feb 2025 07:54:12 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3e0bbec4e230ba69d1863d0cfc4bb4ffd41f22f10ffc6acdc5e7b83ecde34c`  
		Last Modified: Tue, 04 Feb 2025 04:28:42 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9dd28ef3cfec128e7a1800f6f22aaa8ea274fb08d0461d882a3cfd4f2186d4`  
		Last Modified: Tue, 04 Feb 2025 04:28:42 GMT  
		Size: 2.5 MB (2500678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e809c489bd7a749f8dd5e42f875574f90c71a4a1aeb4a6d5f78fb38f4dfe91c`  
		Last Modified: Tue, 04 Feb 2025 04:28:42 GMT  
		Size: 1.3 MB (1266291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0569ca3484d7c418601aa4a1d9c03b3a201ae7a07615a5177306ffb6706d0e69`  
		Last Modified: Tue, 04 Feb 2025 04:28:42 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96ec23ce107bcd0877feb48601e1a40ecb123ecd1a8a830fd10bbba4a1ce72a`  
		Last Modified: Tue, 04 Feb 2025 04:28:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:966e032dabd37972613a5886d18a681f7e24e3fee197935b5caf17fb36e21b64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e416fe378dee459251a62a2b5b653c4e2743cecc04e7e5219b1c75c5c4685e0`

```dockerfile
```

-	Layers:
	-	`sha256:d0e0a2e88cc36444c10da305fb5dac611a00828958609797a27fe6be0f7144a5`  
		Last Modified: Tue, 04 Feb 2025 04:28:42 GMT  
		Size: 2.3 MB (2286406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3cbad4006e7b93580c2af2558bc8cf21cfe19addf8bf173de3a234902191e69`  
		Last Modified: Tue, 04 Feb 2025 04:28:42 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; mips64le

```console
$ docker pull memcached@sha256:fcaa4f5ef9712e2ddca14e6857f1b53fa20672b914cd7b88b6b65445f1832a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31692137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:719403932d2bf7fe31ce1da2e00837219fc634598515ea22717f233d4c45b21c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sun, 02 Feb 2025 07:54:12 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1738540800'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:60fe4951c23056512065fcf1948d3167c5aa5d83d4bfd2829494b7d09b4fe661`  
		Last Modified: Tue, 04 Feb 2025 01:38:47 GMT  
		Size: 28.5 MB (28486581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006e6bf1f5c579c425dd6a7045b45795f463f886bf4ee3532c5964da484e77c4`  
		Last Modified: Tue, 04 Feb 2025 05:36:04 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4620497505845e0aede51939832fe2feb1e84e662ca22647506c9e403a4630`  
		Last Modified: Tue, 04 Feb 2025 05:36:05 GMT  
		Size: 1.9 MB (1943191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbe6e63eb850a0d15f3fb3ce772dc8a193c1b9ead3f64bc87ea9db83a818e31`  
		Last Modified: Tue, 04 Feb 2025 05:36:05 GMT  
		Size: 1.3 MB (1260854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40e7ec508708863f095d5fd6aeac52dffd7f20c336c28d94a7fad02f2f51a29`  
		Last Modified: Tue, 04 Feb 2025 05:36:05 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd558b6f1714e94bee89e0cf11e0ea1af8a90cc74c1b99553e6313974bea9d6`  
		Last Modified: Tue, 04 Feb 2025 05:36:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:10a2ecdde0367c592a37e2094ddcfc7edb98d5d73d5bbdfd7d7069f11468f41b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a6d8d3fb499ac955955b2c9f4e9776ff914141d14adeea588a371ce4cff3bd`

```dockerfile
```

-	Layers:
	-	`sha256:e0a5ca44660b9368be372266be4aefc4be704e101067286cf36e1b06e2f07cdb`  
		Last Modified: Tue, 04 Feb 2025 05:36:04 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:31e531e504071c6297e43ec0359e37dd60aafa37b23f2cfd572d6992a4a8f699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36085904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029e8e5e0f017ebe180b7e7e42e69b8469d48d66dccc36f4ee94cc70531ce2ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sun, 02 Feb 2025 07:54:12 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 01:38:01 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2554b2c9b1b0eaccf71963ebdaa720beba7c4729f900596b8bb7e99b6919b1`  
		Last Modified: Tue, 04 Feb 2025 04:54:07 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26b95187bf5085dc8573c96b467801af0c38567ad032cafcf7565bc83e8c10c`  
		Last Modified: Tue, 04 Feb 2025 04:54:07 GMT  
		Size: 2.7 MB (2708613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229261d8ebd7f1a31858565844b84e86a020984fbe64d3a62b3d685417159948`  
		Last Modified: Tue, 04 Feb 2025 04:54:07 GMT  
		Size: 1.3 MB (1330999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9891f8d1e557cafb091f637b3db5cdb8b11696ed2c249fdfb769b4a33d3078`  
		Last Modified: Tue, 04 Feb 2025 04:54:07 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25470058ddabb0f895e9d1799ac944c98f6b75317f06a627f30187b8fdfb0a36`  
		Last Modified: Tue, 04 Feb 2025 04:54:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:f914e538671a572729170958d470dfabd855aa80ce53b25a0d7a5204c1b33a0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c38e1164115528d1af0164fb9dc030c96e5f940b1dc40e46c04e9dcf03b3df0`

```dockerfile
```

-	Layers:
	-	`sha256:1f9e966fff09eb8597e726dee37d8077951c4a8388ca91a79ec2ce5e5e913c60`  
		Last Modified: Tue, 04 Feb 2025 04:54:07 GMT  
		Size: 2.3 MB (2293679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd28c7586277dc4f00031d57a5fe00d338e5418c714bd57259f440b8bcbc728c`  
		Last Modified: Tue, 04 Feb 2025 04:54:07 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:682eb0a0e7d4cd11f8b9a3e1290057c1e796788a4618a3ac5c82cb7df58933d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30261734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df80d341f0efbcde25b92f3e1b797f27625a16d555bfca98f22061de2f298a69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sun, 02 Feb 2025 07:54:12 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe1d1bee073fc6fc7edf8762994dd33eb7f445c49d726accfb91332a242d958`  
		Last Modified: Tue, 04 Feb 2025 04:55:22 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8785d74590885c81503a45644906e34c354e69c862dad662a22f498c866adece`  
		Last Modified: Tue, 04 Feb 2025 04:55:23 GMT  
		Size: 2.2 MB (2156364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b1bdeb9a486655fb1fbc129ff4907a4c86b484a6c915d9a05aa040888c89e7`  
		Last Modified: Tue, 04 Feb 2025 04:55:23 GMT  
		Size: 1.2 MB (1245232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5b08891d9cb8dac889b466249456f8845d8eb3f7434466b96b09d5431e01a4`  
		Last Modified: Tue, 04 Feb 2025 04:55:23 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a8546468c2d277e130e611d05861380d2da0d3147183727229235f1e512e35`  
		Last Modified: Tue, 04 Feb 2025 04:55:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:f0f959f8ecfee4cbf470f9361e8b57b4e533448ff02939b9502eab73afb04b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e145048ce46bf258188b341bfa77adce8eb7da0fbb8839645158ffc3497c4c9a`

```dockerfile
```

-	Layers:
	-	`sha256:517488b2faa7932817aca91e747eb050e4f797d147f86ea3652de77ba7bb9518`  
		Last Modified: Tue, 04 Feb 2025 04:55:23 GMT  
		Size: 2.3 MB (2289021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94edb64050cfbde612663e71dc905e22225a42f70f6a8d44f18e0667df39e53c`  
		Last Modified: Tue, 04 Feb 2025 04:55:23 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json
