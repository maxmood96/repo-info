<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `memcached`

-	[`memcached:1`](#memcached1)
-	[`memcached:1-alpine`](#memcached1-alpine)
-	[`memcached:1-alpine3.22`](#memcached1-alpine322)
-	[`memcached:1-trixie`](#memcached1-trixie)
-	[`memcached:1.6`](#memcached16)
-	[`memcached:1.6-alpine`](#memcached16-alpine)
-	[`memcached:1.6-alpine3.22`](#memcached16-alpine322)
-	[`memcached:1.6-trixie`](#memcached16-trixie)
-	[`memcached:1.6.39`](#memcached1639)
-	[`memcached:1.6.39-alpine`](#memcached1639-alpine)
-	[`memcached:1.6.39-alpine3.22`](#memcached1639-alpine322)
-	[`memcached:1.6.39-trixie`](#memcached1639-trixie)
-	[`memcached:alpine`](#memcachedalpine)
-	[`memcached:alpine3.22`](#memcachedalpine322)
-	[`memcached:latest`](#memcachedlatest)
-	[`memcached:trixie`](#memcachedtrixie)

## `memcached:1`

```console
$ docker pull memcached@sha256:c8b53d421310f274ece68507406126575bfc2af3ddc66b72709f81ede5fbe2a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:1` - linux; amd64

```console
$ docker pull memcached@sha256:489c2e770f5baac8e88e7b0fc7bd9ec7482c560232093860fa776480fd535059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32204915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09da43b5484edc83f2f153e8f750eae1edfc09a59f9c3c8a0d1543ad028f7702`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebfc0a813c97c15541bf6e00db67cec64e96bf712ccfedb445eff79095d78dd6`  
		Last Modified: Wed, 13 Aug 2025 21:21:18 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d44cb640c5a78307f95a5ba37e9b3ff77e080db5144ad044331bdd27e2ac3b8`  
		Last Modified: Wed, 13 Aug 2025 21:21:32 GMT  
		Size: 136.6 KB (136560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c2449a0115fae5ca7c26d3857bdae261f4168d8334ad67cb6c3461a0910fc6`  
		Last Modified: Wed, 13 Aug 2025 21:21:36 GMT  
		Size: 2.3 MB (2293557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9bbdd035dc48ae794ba5af4721f9afdab19142a19ba004aa4b42738ef8758d8`  
		Last Modified: Wed, 13 Aug 2025 21:21:42 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc99f3761e7cd9c6f00023c8aa0d889222b7b233949d24870d0f9b7ad10f58dd`  
		Last Modified: Wed, 13 Aug 2025 21:21:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:98607b9259666dec40f29b040ae0cac2276fac6541257d7f3a4d2fa8d30e3ae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2029528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ad42f4e39d2637475a5aaa10a446b94d8cb9b730bd194a0f995abf19ecba3e7`

```dockerfile
```

-	Layers:
	-	`sha256:249ac3e00cc732e2b029808c9c00d3520da2cdf38b1fc01081a592ea90a5e050`  
		Last Modified: Wed, 13 Aug 2025 21:34:23 GMT  
		Size: 2.0 MB (2007332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fdd95540cec834ae6e6c6bf9ad1d03f83f75af3a4d5bc52a9b7018dd212823a`  
		Last Modified: Wed, 13 Aug 2025 21:34:24 GMT  
		Size: 22.2 KB (22196 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v5

```console
$ docker pull memcached@sha256:11a993750bd36cfb7d37197d06ccbf217f829c9012146de0d45d0e3494add433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30314569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c2cfe621133fc4a453c7272eacac5ac0ae1cd214c7f7076d785ec3ed0fb6554`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:498399880872f14c562c46bd2a1ef4cfcf3c2a1453514ff0d0f6b7d89f8010dd`  
		Last Modified: Tue, 12 Aug 2025 22:02:01 GMT  
		Size: 27.9 MB (27941706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a99137a20a1adabf0ea411a3bed51f642b1fd51a7c56596ed760ece4727e8c3`  
		Last Modified: Wed, 13 Aug 2025 23:01:56 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7528817abdc345977b6df3988bcacfd622b20f1e6b64e6c01f3c3203275806`  
		Last Modified: Wed, 13 Aug 2025 23:01:57 GMT  
		Size: 144.0 KB (144046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5147466300d5970b08521247c1dcffd9c72644b33c0c4c7a7455293fdaa7514d`  
		Last Modified: Wed, 13 Aug 2025 23:01:58 GMT  
		Size: 2.2 MB (2227304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403dfb443663282b32ef64dddd4d9ece2badd91a91669659aad2213ef1db444c`  
		Last Modified: Wed, 13 Aug 2025 23:00:39 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ac9453a3752c151d9eb3d487d5be8ee9971ce482aa48cbcbffa05e594977ac`  
		Last Modified: Wed, 13 Aug 2025 23:01:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:99d7cc2296b1fdf18d0156098b6c8db466fa371221860e1628d6da1f33862b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe55e32abc4c444556bb77a6cd989bc4c29ae0720781b045162ad41710f332b0`

```dockerfile
```

-	Layers:
	-	`sha256:49bb7a93a18c7972be0483acacb6a99b49edc4bf097a764ed976c48c0516bc14`  
		Last Modified: Thu, 14 Aug 2025 00:34:25 GMT  
		Size: 2.0 MB (2010335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b1896ac27634d50430d62234a56bf5e22627fb59bbe9e2f974832c3f5823cfd`  
		Last Modified: Thu, 14 Aug 2025 00:34:26 GMT  
		Size: 22.3 KB (22343 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v7

```console
$ docker pull memcached@sha256:4b9bce762cb0cd433a31cf56c571b0a5bb7789813cbb111958bf806cba8b87af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28526851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a10eddf8fe36bdc9bc58ad2f45be5555dd9f6f746d916f9ce491ee5f8239bf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc714abeba0eb64ab96f4d3b22e0750d8fb5ca04c15135a1da25d7f28cb90c8`  
		Last Modified: Thu, 14 Aug 2025 03:26:02 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b548feee9753e7f47e9e09d371fbbc5da58c093655fbe6a70e9e8ce1792c6ddc`  
		Last Modified: Thu, 14 Aug 2025 03:26:02 GMT  
		Size: 135.3 KB (135298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9fd10cb429ca884c5738921b455ecc2d83781179e716d4003166bdc8c44e27`  
		Last Modified: Thu, 14 Aug 2025 03:26:01 GMT  
		Size: 2.2 MB (2182550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59893ea711e5a2631eada91282e598b013d3173b17a0edb0fdbe97d67d122e7`  
		Last Modified: Thu, 14 Aug 2025 03:26:02 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8512db29f6abd27987969691ca0de8c6cc141db19a00f2e80bd8996e6cb5de`  
		Last Modified: Thu, 14 Aug 2025 03:26:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:f4b425f37419b579837d2d7857c8ed429c6b2356824bf7c3f83036db9125cc20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f026c9ae0860a234d056b9a6607c5d4673b4e40c52e93c31e76e3cf463fa3c45`

```dockerfile
```

-	Layers:
	-	`sha256:58eba98bd420cdad2a71753e58bb1b1a587f0039d88944045180d74e4c08996c`  
		Last Modified: Thu, 14 Aug 2025 06:34:23 GMT  
		Size: 2.0 MB (2008792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab426c3e7d709a71c837bd5c98de92c219718788268a0700d3c8305f5117b7b8`  
		Last Modified: Thu, 14 Aug 2025 06:34:24 GMT  
		Size: 22.3 KB (22342 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:78a21084b1c4e79dc2fffab373fb465acb723f351bffdc0639a504a5bdc6a2d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32566079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717e9950cc2b302a7f75cdc9919226e0160142934f76014b1a905aa5e39c4046`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d84227403935277ab9817ff62ad9fca6d45f7c109953945d36caa72d73813d0`  
		Last Modified: Wed, 13 Aug 2025 23:02:57 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb0aae300c3cd52b99acd2ae25cb8bf507859ae7b182097672be779a7337fd4`  
		Last Modified: Wed, 13 Aug 2025 23:02:58 GMT  
		Size: 153.4 KB (153369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd2017b19819b1012be52dad0541d85c7797897955d5d0b747b8b86f08da76e`  
		Last Modified: Wed, 13 Aug 2025 23:03:00 GMT  
		Size: 2.3 MB (2275152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad146d7e60bd2063118973d72ff4507de475a826636f2b8fc3bdf36633379d07`  
		Last Modified: Wed, 13 Aug 2025 23:02:59 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fe42a1afd3681fa0efd222132b453c718236f571b4b56018cf362f2333cfb7`  
		Last Modified: Wed, 13 Aug 2025 23:02:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:f34a398dc1f988e0076ebc490e58021e7dc24976392ab10fb871628e11888166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98dee621777b57d248833b652d7622be9c6c901776820489ce629be6f59e5d5f`

```dockerfile
```

-	Layers:
	-	`sha256:4b5fb9727c43d6c906cc0c58b470a99299321ac1e3bcc6a9ea9ec90086d4260d`  
		Last Modified: Thu, 14 Aug 2025 00:34:33 GMT  
		Size: 2.0 MB (2007648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a88652c31f79e7599a31a3fe7d0341deeb4915c7ae0dab214e3c4768ec058300`  
		Last Modified: Thu, 14 Aug 2025 00:34:33 GMT  
		Size: 22.4 KB (22393 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:5b9ccecd7eb2ba800cc927d7dfaa5941d25387818d57d8583260ed7d5ea2ef8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33682664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c160d159b0b83b9824df1d8b4cbe201c4c67902d0171a4a03282d3e230939d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:346d0c953bdbc38917a27a6f30726e5b46419d98ecaf4d2d8f201bc3b7025e57`  
		Last Modified: Tue, 12 Aug 2025 20:45:00 GMT  
		Size: 31.3 MB (31289378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1f928fbfcc7da63ca647a381869549b7db17d2971110bc771c27aeed80b33c`  
		Last Modified: Wed, 13 Aug 2025 21:09:56 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49988f067cdbb2558e23451192304fe7f89c2cbe23fcf5463b9e0b80dfbd2a36`  
		Last Modified: Wed, 13 Aug 2025 21:09:56 GMT  
		Size: 147.4 KB (147419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19f3e01a2ee783f4cf292ba84f151492df7a0170128094f4d011075d629af43`  
		Last Modified: Wed, 13 Aug 2025 21:09:56 GMT  
		Size: 2.2 MB (2244354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2288d51449876e6f7fb89b6cac2eda51fef5f03deb3722ef32bf3a9bdc2f5e17`  
		Last Modified: Wed, 13 Aug 2025 21:09:56 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3668cc13fc1544b7319b7b3307e0d74b4e82d36ca065c5a3be7d080267054267`  
		Last Modified: Wed, 13 Aug 2025 21:09:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:df8cca141522937dd5415946521e71f57731ecc574e78d3175b26ce6260dcd46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2026627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff448533f7fe52a0dc6195d7b9320b996bd2623b7c1e7a5b02f7f5cee32b92a4`

```dockerfile
```

-	Layers:
	-	`sha256:80c0a6ea529144e269d6dc30e72d370cfbc53736314c92cca55d737de9562dd6`  
		Last Modified: Wed, 13 Aug 2025 21:34:31 GMT  
		Size: 2.0 MB (2004489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32faf37cac7f889e11009fc41358994c9714a5ebc9aed8843e1fb57a3de6d243`  
		Last Modified: Wed, 13 Aug 2025 21:34:32 GMT  
		Size: 22.1 KB (22138 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:dcc628faf353367b245beec24d23d1b3103986479dff33e10653c5ef2d8b54b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36182904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d113eca2d57658d5e20bd62171298229010cdbce2c33479664dcad6be5ec2acd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26c42ec1bf9e33e4a6a75b57802a57b9d166fccf4b2e5b13cef2b9742fc5025`  
		Last Modified: Thu, 14 Aug 2025 02:32:42 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a82df09860007e05001d706e92e1aa450bfd12fc72a24522ccca5edc6f43cd`  
		Last Modified: Thu, 14 Aug 2025 02:32:42 GMT  
		Size: 170.2 KB (170241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f425e49b56f20bc4209bec20b1ab8671bd728a94104369def1c947c90134052`  
		Last Modified: Thu, 14 Aug 2025 02:32:42 GMT  
		Size: 2.4 MB (2416933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b832c8b1a0256fd9b38e9fd823309571e179c77a2f44d5115f06ae282b7972f`  
		Last Modified: Thu, 14 Aug 2025 02:32:42 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da165b338847a53b7c8a0a0a08c089c86721f3997c5f507291c4737245ade82f`  
		Last Modified: Thu, 14 Aug 2025 02:32:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:d11fb93c72d4e4416799b886acc2230eefbe26e6381d65c674a1a47f310f22ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2154e1260dfec440f34afa1451b8e89c13a23e1eb451b2250766c9c88cf993a`

```dockerfile
```

-	Layers:
	-	`sha256:3c0cb7a63a69d321f183e466c5c0a934dd9a09173b6e174e2f17a9a24e241dee`  
		Last Modified: Thu, 14 Aug 2025 03:34:34 GMT  
		Size: 2.0 MB (2010933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e4dcd6c60091d8eaa78af8659654106ffc91270b3f5b4b6e166f41e295e361f`  
		Last Modified: Thu, 14 Aug 2025 03:34:35 GMT  
		Size: 22.3 KB (22269 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:c7b8d8a8065d2a0ea3bdaaadd564986a39a88ad9d9ef599faf4f923888bb9126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32288745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6fca6b4af0e7ae24559fc296fb0ce831a94645f64b986956f57f9306df1ed22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024aba4218861d2cdfa6f7186fcca6f2f2041ce6c7210cd258e28d55a2c1fa16`  
		Last Modified: Thu, 14 Aug 2025 02:58:06 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2b32b5cc5f77750b103e7bdeb63810088dca53dae4f8b6eed4e17f219a5826`  
		Last Modified: Thu, 14 Aug 2025 02:58:05 GMT  
		Size: 140.4 KB (140388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a046ba92157d2c0b391049e3f702ebcac682b0c6ee6e651f44d940e5d9bd8cd7`  
		Last Modified: Thu, 14 Aug 2025 02:58:07 GMT  
		Size: 2.3 MB (2313787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd7d0eef9a2ce528ea647334f74bfda29496059b15274182ae0d16fb7e5f28d`  
		Last Modified: Thu, 14 Aug 2025 02:58:06 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c5230e4318cec0912586827ea533d6abfaed20ff08b3662b6cf6871a9abae1`  
		Last Modified: Thu, 14 Aug 2025 02:58:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:88badce3b30eeb4fdb00156647e4a3479b0c7cf8dddb286e0bd07105084f4e5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7704cd55751a22fc58eb4a349020abdd760508cd1b9344ccb0df28dc62d35f98`

```dockerfile
```

-	Layers:
	-	`sha256:91e3962d713f291258d33cdc619c48c657c3a72b3a6c808786e3b209389502b2`  
		Last Modified: Thu, 14 Aug 2025 03:34:39 GMT  
		Size: 2.0 MB (2008769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76baa03c0dea63878577ee4ab27db735c1db244cbefee8f9c7b5d5eb4d3887f1`  
		Last Modified: Thu, 14 Aug 2025 03:34:39 GMT  
		Size: 22.2 KB (22196 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:b50070f2faf253d8aacd530742e8e71791a39222c75abcdbcc442dbb7a2f3f25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
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
$ docker pull memcached@sha256:033134f4dd9f45d4e22b6e98b040ea3fccf0dca740af3c949b44bebf458b04d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5904246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca259aa2216a248c482fc8a069d48b1e70b087529d2c3de97154bfa458dbb7a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fb46bc7dee2beda6f5f6f567aecd4d7d7698b9749ed917988a859b7dd96e30`  
		Last Modified: Tue, 29 Jul 2025 16:32:22 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48faf8c85515fb9d17e0752e77d8241f223d53b1adc90439c606d17daabd0ae`  
		Last Modified: Tue, 29 Jul 2025 16:32:24 GMT  
		Size: 104.7 KB (104725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d552a2d777fd444b41cb79438f9f1b441821162e78d73e96dc848a773cf43892`  
		Last Modified: Tue, 29 Jul 2025 16:32:24 GMT  
		Size: 2.0 MB (1998477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c70665f30f3e15975d429b494cb17b21c5d4630c1800cb0addc3fce3a11aa29`  
		Last Modified: Tue, 29 Jul 2025 16:32:20 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ff68520caaf588cec750ad7c403cf55d79eecfff4b7a4ac5eb3910c90c2817`  
		Last Modified: Tue, 29 Jul 2025 16:32:21 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7b27e0df383f45d6d523345a078898524a69cee4d6978cf64bf26532b8679dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 KB (116752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb88e7ee6d3e67b2e4f307c081504a685666917ddf50770fe8beb5abd60a3dc5`

```dockerfile
```

-	Layers:
	-	`sha256:2cf00a09ffccb2c00421311314137de90d0586c126b79dbe5315ce321c168b34`  
		Last Modified: Tue, 29 Jul 2025 18:35:07 GMT  
		Size: 96.2 KB (96180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55325ecc9b276e9c55badf949ed4f06840c34aa8baf0aa6f974e0b90dc5d4e0d`  
		Last Modified: Tue, 29 Jul 2025 18:35:07 GMT  
		Size: 20.6 KB (20572 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:78b59dd3af5a55e950f5106869e642af122a7dc470545f4ba533f6833d83b62c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5550795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb09d5ce1b7010f7a36d77494bc5358d666339628c183692906db6a961373847`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c710b5ddcc2882c5014d0c8cb93aec2bd8b6cc3c59fd42b40c87d94f89a7bc7f`  
		Last Modified: Wed, 23 Jul 2025 22:59:16 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c42040d822a4af7f05f9ccd4d18a7a5e4712b118b7f18d1a7969761029a9d2`  
		Last Modified: Wed, 23 Jul 2025 22:59:16 GMT  
		Size: 101.5 KB (101533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3095e18cd24048696efd57ac64d04dde381a3abde625964e02165c7364eb5633`  
		Last Modified: Tue, 29 Jul 2025 16:50:12 GMT  
		Size: 1.9 MB (1947003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0436ec50f04ed972ff0dd760f7e820f192236e5e720bddb6173f65159c7c36`  
		Last Modified: Tue, 29 Jul 2025 16:50:11 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671c24aae36bb04a32e05bd64e1371384f594889cdbbc41029c916447666d402`  
		Last Modified: Tue, 29 Jul 2025 16:50:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c2a050c6822d834285577c3a001fdfcf9949b7f5a483a4a76a49b549bea19641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54e8bda3e734528caeab4505f084ca7a3076d5ec2273287f66954b5e91af42f`

```dockerfile
```

-	Layers:
	-	`sha256:0d86924831d61ce8b792b25421e9ff0fa2eda9ab940eba5309d44d0eeada7e8e`  
		Last Modified: Tue, 29 Jul 2025 18:35:11 GMT  
		Size: 20.5 KB (20506 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:c9f5db2389b9b0b4a2cd199c4417a9f49a60c42d616e8421177e662d4830de07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9421ed030d4b6b6405714612b8858bda87bc53ac8b0c5ed65c582119527f2d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251060498ca8f0484e20714689b9caba533d09c1b74ed8f2a06780db515a28e2`  
		Last Modified: Thu, 24 Jul 2025 00:27:37 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2293bd2fb47d57e5869c197133067e17f9b1e51ea0f298af1e480e7fd33d681`  
		Last Modified: Thu, 24 Jul 2025 00:27:38 GMT  
		Size: 91.3 KB (91313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ae82f2bac2f7e6fe57f8cb7006fc227c972da1ae5749eba9f5f73e6f3248ec`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 1.9 MB (1905692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e60bf2b2164c620b69e40bdcb64d4104d02eab86c96ea6e170a3601b9ecfd82`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665fe4cd856f1a5c2193568e756c572656949b17c381fc8d43efaa823e18cfa7`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:376a71bc0fef7741e92fdae8b96c825c4622e980de01e724b1a3a0bec3d95f20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 KB (116963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22b574f6c6d021a917c0e99ff4800d8ac3c22fb94b94f88c404cc7609f562fb5`

```dockerfile
```

-	Layers:
	-	`sha256:58ebd4bc7ee5888c552e0fa618f93aefbdb1d15a56ecd3abef19a46ce2f93eee`  
		Last Modified: Tue, 29 Jul 2025 18:35:15 GMT  
		Size: 96.2 KB (96248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d432ed2053ed8249834dd5016fe3199bbc3f82dc7013027c3ead9efe2a007b98`  
		Last Modified: Tue, 29 Jul 2025 18:35:16 GMT  
		Size: 20.7 KB (20715 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b5e4ecc3e927ee30e5cfcfc8aa044960631c75eb8abed9d0fcee6232aa5fdf79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6241700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c880dc2c785861dc9010b813bb6f533f30518443a3bb7e7f477bc96af14582`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbfeb6ac9fd2045c5bea10a301ad554c1f703ffc2885c41520dd5e42eb4a59a`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47acaa5035f94aed634b9d7ecae02fb3838f19e38f8e752ecd6cfba97699b31`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 120.8 KB (120812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8160f3136c6863b52f0dec4f9918b91b8a509700b2071ec0aecd5a6231f00f2a`  
		Last Modified: Tue, 29 Jul 2025 16:41:09 GMT  
		Size: 2.0 MB (1988782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff22f0cad01950efb78a7a862b0becb8b2fd22d795b585f97dad66c091c3dd7`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed19cbfb574c7d8cab364e2ec072c0e03f694468ada41cd70bfcd35392df9e7`  
		Last Modified: Tue, 29 Jul 2025 16:41:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b4c81c7ababb91ecdda3b7d70514d16818602199d759eb2aadd74de732d52960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 KB (117055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80452fd4f79f6e7a0dab0beebf5c144f9df7c257255cdd3cb93ccbff77001fd6`

```dockerfile
```

-	Layers:
	-	`sha256:f11d2a322f6088804ee63ae1a77b9d5ddcdfdc0c65c22e7a70b7ee67cf4532ed`  
		Last Modified: Tue, 29 Jul 2025 18:35:20 GMT  
		Size: 96.3 KB (96284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e225dd6ea14146ddf445598f24189c065ec684fbeb92e7d053a0211a7d60efda`  
		Last Modified: Tue, 29 Jul 2025 18:35:21 GMT  
		Size: 20.8 KB (20771 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:c58767364161c180098aa6daf4620c8c55ad8713deb64ca620668e7bb829bb41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5683246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac911958149764a83bf951afae4135a482e9064dd0c7dbee61474116cf4bc68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1f621f1e5b25aa798d604ab87259f546a42e522b1311f962484669d45183fa`  
		Last Modified: Tue, 29 Jul 2025 16:32:40 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7cf471d76eab33abc760b1edf151f0e3d4d73732c3f002c74ef629f8ded5f9`  
		Last Modified: Tue, 29 Jul 2025 16:32:39 GMT  
		Size: 109.5 KB (109523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a287f0dc98767a99d5c18925da988244c99243b51f5870a4ed36648b93518402`  
		Last Modified: Tue, 29 Jul 2025 16:32:42 GMT  
		Size: 2.0 MB (1957368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101df272f2e8c1be378c334f0d3d2de9dcd2c58db6fe3580d4451396deef84de`  
		Last Modified: Tue, 29 Jul 2025 16:32:41 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f870cbd8529325263ac998fe634981f154a171a39da706e91a9ea2d91038d361`  
		Last Modified: Tue, 29 Jul 2025 16:32:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:837e0ff5feebc7262c78ddd6b4bece1b5b4c3c22b0eb71b71bf9c6c9d154b416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.7 KB (116651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf22108f9222361c74085ca0633d2876cf3187ccaeb4353499f02fc7a24cc51b`

```dockerfile
```

-	Layers:
	-	`sha256:5143c40f563e8ee15ea82be605c093d36fd7445bcd1cedc45d0754c52b6d3f9d`  
		Last Modified: Tue, 29 Jul 2025 18:35:24 GMT  
		Size: 96.1 KB (96135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fcabff32e4e745d2c95395b620e73b812d1c38929ba82167c1d76583a2f4150`  
		Last Modified: Tue, 29 Jul 2025 18:35:25 GMT  
		Size: 20.5 KB (20516 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:04386ede5dcbf35cabad144bcdc951cc64882f7b9727f2d09927fe0d5551dd19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5942089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8252590eee78d67456ac83fd8279259aaea4d2a555c8bc20b173663fcaa2883`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc22e0cec7e7fe8cff10539bca58363ad6749e2de4f878015c25b5f2b6ecadb9`  
		Last Modified: Tue, 29 Jul 2025 16:33:46 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992ebe18219bd78e59e7e56661aae22f700927f47bc7ad1dfe7717093b371c15`  
		Last Modified: Tue, 29 Jul 2025 16:33:49 GMT  
		Size: 124.3 KB (124315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953f5a37d23881d59809ea64dc6ebf1a152a1ff8929f51befb10577771755f5d`  
		Last Modified: Tue, 29 Jul 2025 16:33:49 GMT  
		Size: 2.1 MB (2089310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b62870a2d7b266495d83cfd72dcf702c91c5c60a7e29836bd9bdac776511a7`  
		Last Modified: Tue, 29 Jul 2025 16:33:47 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1cc8c0fe9a4ef7e2ef70e32ddbfbd2fd68985dd452630a8f390c5b41c654f8`  
		Last Modified: Tue, 29 Jul 2025 16:33:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:cf7e9735e4ef5d00dc25928653b808214f070708e9d879ef54afc4d77ce9db2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcceb455cfdb86bdb0c165af3bc54cbab794d56fef1dbae2b484d28027db791c`

```dockerfile
```

-	Layers:
	-	`sha256:a40704a0afb5cf1b90c0fbdf73c5218a4d8f0e93bb39014507b5fa5f8c7265dd`  
		Last Modified: Tue, 29 Jul 2025 18:35:29 GMT  
		Size: 94.3 KB (94287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da22397f364310e72420738395739c36e25b4e4813bbc5da197582a91bb55ac9`  
		Last Modified: Tue, 29 Jul 2025 18:35:29 GMT  
		Size: 20.6 KB (20648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:d55b98c34ba1c2f546461bd57477d46ab868f9de6b107ffb8f20e06dab1e10d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1034dde2661f43165e85db9a13ff0e10d237d14d4b1b7ee1d4570f19d7df4e69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bbdcecb4dec3cbaba0500f9425897948884cfd8db95ccdf9b824d448b24049`  
		Last Modified: Wed, 23 Jul 2025 23:54:15 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c18051d55886d147cafcee8f9e220087c0b60c0e11ec8898a4005352ee0f7e4`  
		Last Modified: Wed, 23 Jul 2025 23:50:14 GMT  
		Size: 107.9 KB (107902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953c2b44fe537b63907764cf78cbb294c6a1133eacb39c62d35ee5d4914779cb`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 1.9 MB (1932977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d69b2f63abf91684a15b9de7b5e617996762376da3fdda50c4e20c2f1e0f4da`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57c134601fc15e8f2cf183cfd9a3057731ad48b915988217f51df31b5d3cf38`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d50b42de80ef3381b05da20cef4ba6ab4491facb607528e075c034257fe9d327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27766c161110b7e46063a39ce6e176f87233fd6722a825ec338e1568892a77a3`

```dockerfile
```

-	Layers:
	-	`sha256:f933f968a4a14795196607a1337a19431e9f61db78bb49c5c2f89f64a17a1d89`  
		Last Modified: Tue, 29 Jul 2025 18:35:33 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffc41094fe9f57bca69da70bbb18eca52aaf6d27d0fb6d79eda79f9e011a157a`  
		Last Modified: Tue, 29 Jul 2025 18:35:33 GMT  
		Size: 20.6 KB (20647 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:cfd223eb11df3d2297224d458caf974f3f0aae4742ff917812f1b8c84c84e705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5797268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e23f18e891a12e72ef84139504baf8783a7db21d4976fc0b607f8e9bbf736f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00131fb0ca26b15f1ac64b82554fc342b19f8c1ef38312a75addb6686f7bc24`  
		Last Modified: Tue, 29 Jul 2025 16:41:40 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e54da6ab620e035fd78987688d45401e87278ec8a5c02cef8a57e4ea9fd286`  
		Last Modified: Tue, 29 Jul 2025 16:41:42 GMT  
		Size: 113.5 KB (113499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6160f9fac1fd86eda224e9ce4740ea46f7e23dc7edb6d1fe9d830001313e63a`  
		Last Modified: Tue, 29 Jul 2025 16:41:46 GMT  
		Size: 2.0 MB (2037446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d01cd71d33b01b420652f4ad9275f1475f4f0bf253dc0a1b48198df2010be5`  
		Last Modified: Tue, 29 Jul 2025 16:41:52 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831dd5e3c39dd2744dc8823190095f709c36020b55ccdaf85f62a146582c7d9d`  
		Last Modified: Tue, 29 Jul 2025 16:41:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:79f0de7e4dcc9afdbfa1fa22250cf3e544d6f3c33174246b427d2865c7e343d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71dad4d71741d8d354038cb6898389aebb54c956dfcd865d57f78dcc3b238bf8`

```dockerfile
```

-	Layers:
	-	`sha256:f942bbb9520308ae352a056c148fdce8f6b09672c257e0a769aa2504bacf1845`  
		Last Modified: Tue, 29 Jul 2025 18:35:37 GMT  
		Size: 94.2 KB (94229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c46680ef7cf08a43965ab9c7727cc70268ee89e366a1ce1806d0f7980b4ad812`  
		Last Modified: Tue, 29 Jul 2025 18:35:38 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine3.22`

```console
$ docker pull memcached@sha256:b50070f2faf253d8aacd530742e8e71791a39222c75abcdbcc442dbb7a2f3f25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
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

### `memcached:1-alpine3.22` - linux; amd64

```console
$ docker pull memcached@sha256:033134f4dd9f45d4e22b6e98b040ea3fccf0dca740af3c949b44bebf458b04d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5904246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca259aa2216a248c482fc8a069d48b1e70b087529d2c3de97154bfa458dbb7a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fb46bc7dee2beda6f5f6f567aecd4d7d7698b9749ed917988a859b7dd96e30`  
		Last Modified: Tue, 29 Jul 2025 16:32:22 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48faf8c85515fb9d17e0752e77d8241f223d53b1adc90439c606d17daabd0ae`  
		Last Modified: Tue, 29 Jul 2025 16:32:24 GMT  
		Size: 104.7 KB (104725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d552a2d777fd444b41cb79438f9f1b441821162e78d73e96dc848a773cf43892`  
		Last Modified: Tue, 29 Jul 2025 16:32:24 GMT  
		Size: 2.0 MB (1998477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c70665f30f3e15975d429b494cb17b21c5d4630c1800cb0addc3fce3a11aa29`  
		Last Modified: Tue, 29 Jul 2025 16:32:20 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ff68520caaf588cec750ad7c403cf55d79eecfff4b7a4ac5eb3910c90c2817`  
		Last Modified: Tue, 29 Jul 2025 16:32:21 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:7b27e0df383f45d6d523345a078898524a69cee4d6978cf64bf26532b8679dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 KB (116752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb88e7ee6d3e67b2e4f307c081504a685666917ddf50770fe8beb5abd60a3dc5`

```dockerfile
```

-	Layers:
	-	`sha256:2cf00a09ffccb2c00421311314137de90d0586c126b79dbe5315ce321c168b34`  
		Last Modified: Tue, 29 Jul 2025 18:35:07 GMT  
		Size: 96.2 KB (96180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55325ecc9b276e9c55badf949ed4f06840c34aa8baf0aa6f974e0b90dc5d4e0d`  
		Last Modified: Tue, 29 Jul 2025 18:35:07 GMT  
		Size: 20.6 KB (20572 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.22` - linux; arm variant v6

```console
$ docker pull memcached@sha256:78b59dd3af5a55e950f5106869e642af122a7dc470545f4ba533f6833d83b62c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5550795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb09d5ce1b7010f7a36d77494bc5358d666339628c183692906db6a961373847`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c710b5ddcc2882c5014d0c8cb93aec2bd8b6cc3c59fd42b40c87d94f89a7bc7f`  
		Last Modified: Wed, 23 Jul 2025 22:59:16 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c42040d822a4af7f05f9ccd4d18a7a5e4712b118b7f18d1a7969761029a9d2`  
		Last Modified: Wed, 23 Jul 2025 22:59:16 GMT  
		Size: 101.5 KB (101533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3095e18cd24048696efd57ac64d04dde381a3abde625964e02165c7364eb5633`  
		Last Modified: Tue, 29 Jul 2025 16:50:12 GMT  
		Size: 1.9 MB (1947003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0436ec50f04ed972ff0dd760f7e820f192236e5e720bddb6173f65159c7c36`  
		Last Modified: Tue, 29 Jul 2025 16:50:11 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671c24aae36bb04a32e05bd64e1371384f594889cdbbc41029c916447666d402`  
		Last Modified: Tue, 29 Jul 2025 16:50:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:c2a050c6822d834285577c3a001fdfcf9949b7f5a483a4a76a49b549bea19641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54e8bda3e734528caeab4505f084ca7a3076d5ec2273287f66954b5e91af42f`

```dockerfile
```

-	Layers:
	-	`sha256:0d86924831d61ce8b792b25421e9ff0fa2eda9ab940eba5309d44d0eeada7e8e`  
		Last Modified: Tue, 29 Jul 2025 18:35:11 GMT  
		Size: 20.5 KB (20506 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.22` - linux; arm variant v7

```console
$ docker pull memcached@sha256:c9f5db2389b9b0b4a2cd199c4417a9f49a60c42d616e8421177e662d4830de07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9421ed030d4b6b6405714612b8858bda87bc53ac8b0c5ed65c582119527f2d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251060498ca8f0484e20714689b9caba533d09c1b74ed8f2a06780db515a28e2`  
		Last Modified: Thu, 24 Jul 2025 00:27:37 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2293bd2fb47d57e5869c197133067e17f9b1e51ea0f298af1e480e7fd33d681`  
		Last Modified: Thu, 24 Jul 2025 00:27:38 GMT  
		Size: 91.3 KB (91313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ae82f2bac2f7e6fe57f8cb7006fc227c972da1ae5749eba9f5f73e6f3248ec`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 1.9 MB (1905692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e60bf2b2164c620b69e40bdcb64d4104d02eab86c96ea6e170a3601b9ecfd82`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665fe4cd856f1a5c2193568e756c572656949b17c381fc8d43efaa823e18cfa7`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:376a71bc0fef7741e92fdae8b96c825c4622e980de01e724b1a3a0bec3d95f20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 KB (116963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22b574f6c6d021a917c0e99ff4800d8ac3c22fb94b94f88c404cc7609f562fb5`

```dockerfile
```

-	Layers:
	-	`sha256:58ebd4bc7ee5888c552e0fa618f93aefbdb1d15a56ecd3abef19a46ce2f93eee`  
		Last Modified: Tue, 29 Jul 2025 18:35:15 GMT  
		Size: 96.2 KB (96248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d432ed2053ed8249834dd5016fe3199bbc3f82dc7013027c3ead9efe2a007b98`  
		Last Modified: Tue, 29 Jul 2025 18:35:16 GMT  
		Size: 20.7 KB (20715 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b5e4ecc3e927ee30e5cfcfc8aa044960631c75eb8abed9d0fcee6232aa5fdf79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6241700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c880dc2c785861dc9010b813bb6f533f30518443a3bb7e7f477bc96af14582`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbfeb6ac9fd2045c5bea10a301ad554c1f703ffc2885c41520dd5e42eb4a59a`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47acaa5035f94aed634b9d7ecae02fb3838f19e38f8e752ecd6cfba97699b31`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 120.8 KB (120812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8160f3136c6863b52f0dec4f9918b91b8a509700b2071ec0aecd5a6231f00f2a`  
		Last Modified: Tue, 29 Jul 2025 16:41:09 GMT  
		Size: 2.0 MB (1988782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff22f0cad01950efb78a7a862b0becb8b2fd22d795b585f97dad66c091c3dd7`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed19cbfb574c7d8cab364e2ec072c0e03f694468ada41cd70bfcd35392df9e7`  
		Last Modified: Tue, 29 Jul 2025 16:41:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:b4c81c7ababb91ecdda3b7d70514d16818602199d759eb2aadd74de732d52960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 KB (117055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80452fd4f79f6e7a0dab0beebf5c144f9df7c257255cdd3cb93ccbff77001fd6`

```dockerfile
```

-	Layers:
	-	`sha256:f11d2a322f6088804ee63ae1a77b9d5ddcdfdc0c65c22e7a70b7ee67cf4532ed`  
		Last Modified: Tue, 29 Jul 2025 18:35:20 GMT  
		Size: 96.3 KB (96284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e225dd6ea14146ddf445598f24189c065ec684fbeb92e7d053a0211a7d60efda`  
		Last Modified: Tue, 29 Jul 2025 18:35:21 GMT  
		Size: 20.8 KB (20771 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.22` - linux; 386

```console
$ docker pull memcached@sha256:c58767364161c180098aa6daf4620c8c55ad8713deb64ca620668e7bb829bb41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5683246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac911958149764a83bf951afae4135a482e9064dd0c7dbee61474116cf4bc68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1f621f1e5b25aa798d604ab87259f546a42e522b1311f962484669d45183fa`  
		Last Modified: Tue, 29 Jul 2025 16:32:40 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7cf471d76eab33abc760b1edf151f0e3d4d73732c3f002c74ef629f8ded5f9`  
		Last Modified: Tue, 29 Jul 2025 16:32:39 GMT  
		Size: 109.5 KB (109523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a287f0dc98767a99d5c18925da988244c99243b51f5870a4ed36648b93518402`  
		Last Modified: Tue, 29 Jul 2025 16:32:42 GMT  
		Size: 2.0 MB (1957368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101df272f2e8c1be378c334f0d3d2de9dcd2c58db6fe3580d4451396deef84de`  
		Last Modified: Tue, 29 Jul 2025 16:32:41 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f870cbd8529325263ac998fe634981f154a171a39da706e91a9ea2d91038d361`  
		Last Modified: Tue, 29 Jul 2025 16:32:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:837e0ff5feebc7262c78ddd6b4bece1b5b4c3c22b0eb71b71bf9c6c9d154b416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.7 KB (116651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf22108f9222361c74085ca0633d2876cf3187ccaeb4353499f02fc7a24cc51b`

```dockerfile
```

-	Layers:
	-	`sha256:5143c40f563e8ee15ea82be605c093d36fd7445bcd1cedc45d0754c52b6d3f9d`  
		Last Modified: Tue, 29 Jul 2025 18:35:24 GMT  
		Size: 96.1 KB (96135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fcabff32e4e745d2c95395b620e73b812d1c38929ba82167c1d76583a2f4150`  
		Last Modified: Tue, 29 Jul 2025 18:35:25 GMT  
		Size: 20.5 KB (20516 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.22` - linux; ppc64le

```console
$ docker pull memcached@sha256:04386ede5dcbf35cabad144bcdc951cc64882f7b9727f2d09927fe0d5551dd19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5942089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8252590eee78d67456ac83fd8279259aaea4d2a555c8bc20b173663fcaa2883`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc22e0cec7e7fe8cff10539bca58363ad6749e2de4f878015c25b5f2b6ecadb9`  
		Last Modified: Tue, 29 Jul 2025 16:33:46 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992ebe18219bd78e59e7e56661aae22f700927f47bc7ad1dfe7717093b371c15`  
		Last Modified: Tue, 29 Jul 2025 16:33:49 GMT  
		Size: 124.3 KB (124315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953f5a37d23881d59809ea64dc6ebf1a152a1ff8929f51befb10577771755f5d`  
		Last Modified: Tue, 29 Jul 2025 16:33:49 GMT  
		Size: 2.1 MB (2089310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b62870a2d7b266495d83cfd72dcf702c91c5c60a7e29836bd9bdac776511a7`  
		Last Modified: Tue, 29 Jul 2025 16:33:47 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1cc8c0fe9a4ef7e2ef70e32ddbfbd2fd68985dd452630a8f390c5b41c654f8`  
		Last Modified: Tue, 29 Jul 2025 16:33:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:cf7e9735e4ef5d00dc25928653b808214f070708e9d879ef54afc4d77ce9db2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcceb455cfdb86bdb0c165af3bc54cbab794d56fef1dbae2b484d28027db791c`

```dockerfile
```

-	Layers:
	-	`sha256:a40704a0afb5cf1b90c0fbdf73c5218a4d8f0e93bb39014507b5fa5f8c7265dd`  
		Last Modified: Tue, 29 Jul 2025 18:35:29 GMT  
		Size: 94.3 KB (94287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da22397f364310e72420738395739c36e25b4e4813bbc5da197582a91bb55ac9`  
		Last Modified: Tue, 29 Jul 2025 18:35:29 GMT  
		Size: 20.6 KB (20648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.22` - linux; riscv64

```console
$ docker pull memcached@sha256:d55b98c34ba1c2f546461bd57477d46ab868f9de6b107ffb8f20e06dab1e10d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1034dde2661f43165e85db9a13ff0e10d237d14d4b1b7ee1d4570f19d7df4e69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bbdcecb4dec3cbaba0500f9425897948884cfd8db95ccdf9b824d448b24049`  
		Last Modified: Wed, 23 Jul 2025 23:54:15 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c18051d55886d147cafcee8f9e220087c0b60c0e11ec8898a4005352ee0f7e4`  
		Last Modified: Wed, 23 Jul 2025 23:50:14 GMT  
		Size: 107.9 KB (107902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953c2b44fe537b63907764cf78cbb294c6a1133eacb39c62d35ee5d4914779cb`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 1.9 MB (1932977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d69b2f63abf91684a15b9de7b5e617996762376da3fdda50c4e20c2f1e0f4da`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57c134601fc15e8f2cf183cfd9a3057731ad48b915988217f51df31b5d3cf38`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:d50b42de80ef3381b05da20cef4ba6ab4491facb607528e075c034257fe9d327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27766c161110b7e46063a39ce6e176f87233fd6722a825ec338e1568892a77a3`

```dockerfile
```

-	Layers:
	-	`sha256:f933f968a4a14795196607a1337a19431e9f61db78bb49c5c2f89f64a17a1d89`  
		Last Modified: Tue, 29 Jul 2025 18:35:33 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffc41094fe9f57bca69da70bbb18eca52aaf6d27d0fb6d79eda79f9e011a157a`  
		Last Modified: Tue, 29 Jul 2025 18:35:33 GMT  
		Size: 20.6 KB (20647 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.22` - linux; s390x

```console
$ docker pull memcached@sha256:cfd223eb11df3d2297224d458caf974f3f0aae4742ff917812f1b8c84c84e705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5797268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e23f18e891a12e72ef84139504baf8783a7db21d4976fc0b607f8e9bbf736f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00131fb0ca26b15f1ac64b82554fc342b19f8c1ef38312a75addb6686f7bc24`  
		Last Modified: Tue, 29 Jul 2025 16:41:40 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e54da6ab620e035fd78987688d45401e87278ec8a5c02cef8a57e4ea9fd286`  
		Last Modified: Tue, 29 Jul 2025 16:41:42 GMT  
		Size: 113.5 KB (113499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6160f9fac1fd86eda224e9ce4740ea46f7e23dc7edb6d1fe9d830001313e63a`  
		Last Modified: Tue, 29 Jul 2025 16:41:46 GMT  
		Size: 2.0 MB (2037446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d01cd71d33b01b420652f4ad9275f1475f4f0bf253dc0a1b48198df2010be5`  
		Last Modified: Tue, 29 Jul 2025 16:41:52 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831dd5e3c39dd2744dc8823190095f709c36020b55ccdaf85f62a146582c7d9d`  
		Last Modified: Tue, 29 Jul 2025 16:41:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:79f0de7e4dcc9afdbfa1fa22250cf3e544d6f3c33174246b427d2865c7e343d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71dad4d71741d8d354038cb6898389aebb54c956dfcd865d57f78dcc3b238bf8`

```dockerfile
```

-	Layers:
	-	`sha256:f942bbb9520308ae352a056c148fdce8f6b09672c257e0a769aa2504bacf1845`  
		Last Modified: Tue, 29 Jul 2025 18:35:37 GMT  
		Size: 94.2 KB (94229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c46680ef7cf08a43965ab9c7727cc70268ee89e366a1ce1806d0f7980b4ad812`  
		Last Modified: Tue, 29 Jul 2025 18:35:38 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-trixie`

```console
$ docker pull memcached@sha256:c8b53d421310f274ece68507406126575bfc2af3ddc66b72709f81ede5fbe2a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:1-trixie` - linux; amd64

```console
$ docker pull memcached@sha256:489c2e770f5baac8e88e7b0fc7bd9ec7482c560232093860fa776480fd535059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32204915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09da43b5484edc83f2f153e8f750eae1edfc09a59f9c3c8a0d1543ad028f7702`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebfc0a813c97c15541bf6e00db67cec64e96bf712ccfedb445eff79095d78dd6`  
		Last Modified: Wed, 13 Aug 2025 21:21:18 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d44cb640c5a78307f95a5ba37e9b3ff77e080db5144ad044331bdd27e2ac3b8`  
		Last Modified: Wed, 13 Aug 2025 21:21:32 GMT  
		Size: 136.6 KB (136560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c2449a0115fae5ca7c26d3857bdae261f4168d8334ad67cb6c3461a0910fc6`  
		Last Modified: Wed, 13 Aug 2025 21:21:36 GMT  
		Size: 2.3 MB (2293557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9bbdd035dc48ae794ba5af4721f9afdab19142a19ba004aa4b42738ef8758d8`  
		Last Modified: Wed, 13 Aug 2025 21:21:42 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc99f3761e7cd9c6f00023c8aa0d889222b7b233949d24870d0f9b7ad10f58dd`  
		Last Modified: Wed, 13 Aug 2025 21:21:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:98607b9259666dec40f29b040ae0cac2276fac6541257d7f3a4d2fa8d30e3ae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2029528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ad42f4e39d2637475a5aaa10a446b94d8cb9b730bd194a0f995abf19ecba3e7`

```dockerfile
```

-	Layers:
	-	`sha256:249ac3e00cc732e2b029808c9c00d3520da2cdf38b1fc01081a592ea90a5e050`  
		Last Modified: Wed, 13 Aug 2025 21:34:23 GMT  
		Size: 2.0 MB (2007332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fdd95540cec834ae6e6c6bf9ad1d03f83f75af3a4d5bc52a9b7018dd212823a`  
		Last Modified: Wed, 13 Aug 2025 21:34:24 GMT  
		Size: 22.2 KB (22196 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:11a993750bd36cfb7d37197d06ccbf217f829c9012146de0d45d0e3494add433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30314569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c2cfe621133fc4a453c7272eacac5ac0ae1cd214c7f7076d785ec3ed0fb6554`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:498399880872f14c562c46bd2a1ef4cfcf3c2a1453514ff0d0f6b7d89f8010dd`  
		Last Modified: Tue, 12 Aug 2025 22:02:01 GMT  
		Size: 27.9 MB (27941706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a99137a20a1adabf0ea411a3bed51f642b1fd51a7c56596ed760ece4727e8c3`  
		Last Modified: Wed, 13 Aug 2025 23:01:56 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7528817abdc345977b6df3988bcacfd622b20f1e6b64e6c01f3c3203275806`  
		Last Modified: Wed, 13 Aug 2025 23:01:57 GMT  
		Size: 144.0 KB (144046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5147466300d5970b08521247c1dcffd9c72644b33c0c4c7a7455293fdaa7514d`  
		Last Modified: Wed, 13 Aug 2025 23:01:58 GMT  
		Size: 2.2 MB (2227304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403dfb443663282b32ef64dddd4d9ece2badd91a91669659aad2213ef1db444c`  
		Last Modified: Wed, 13 Aug 2025 23:00:39 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ac9453a3752c151d9eb3d487d5be8ee9971ce482aa48cbcbffa05e594977ac`  
		Last Modified: Wed, 13 Aug 2025 23:01:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:99d7cc2296b1fdf18d0156098b6c8db466fa371221860e1628d6da1f33862b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe55e32abc4c444556bb77a6cd989bc4c29ae0720781b045162ad41710f332b0`

```dockerfile
```

-	Layers:
	-	`sha256:49bb7a93a18c7972be0483acacb6a99b49edc4bf097a764ed976c48c0516bc14`  
		Last Modified: Thu, 14 Aug 2025 00:34:25 GMT  
		Size: 2.0 MB (2010335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b1896ac27634d50430d62234a56bf5e22627fb59bbe9e2f974832c3f5823cfd`  
		Last Modified: Thu, 14 Aug 2025 00:34:26 GMT  
		Size: 22.3 KB (22343 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:4b9bce762cb0cd433a31cf56c571b0a5bb7789813cbb111958bf806cba8b87af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28526851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a10eddf8fe36bdc9bc58ad2f45be5555dd9f6f746d916f9ce491ee5f8239bf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc714abeba0eb64ab96f4d3b22e0750d8fb5ca04c15135a1da25d7f28cb90c8`  
		Last Modified: Thu, 14 Aug 2025 03:26:02 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b548feee9753e7f47e9e09d371fbbc5da58c093655fbe6a70e9e8ce1792c6ddc`  
		Last Modified: Thu, 14 Aug 2025 03:26:02 GMT  
		Size: 135.3 KB (135298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9fd10cb429ca884c5738921b455ecc2d83781179e716d4003166bdc8c44e27`  
		Last Modified: Thu, 14 Aug 2025 03:26:01 GMT  
		Size: 2.2 MB (2182550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59893ea711e5a2631eada91282e598b013d3173b17a0edb0fdbe97d67d122e7`  
		Last Modified: Thu, 14 Aug 2025 03:26:02 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8512db29f6abd27987969691ca0de8c6cc141db19a00f2e80bd8996e6cb5de`  
		Last Modified: Thu, 14 Aug 2025 03:26:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:f4b425f37419b579837d2d7857c8ed429c6b2356824bf7c3f83036db9125cc20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f026c9ae0860a234d056b9a6607c5d4673b4e40c52e93c31e76e3cf463fa3c45`

```dockerfile
```

-	Layers:
	-	`sha256:58eba98bd420cdad2a71753e58bb1b1a587f0039d88944045180d74e4c08996c`  
		Last Modified: Thu, 14 Aug 2025 06:34:23 GMT  
		Size: 2.0 MB (2008792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab426c3e7d709a71c837bd5c98de92c219718788268a0700d3c8305f5117b7b8`  
		Last Modified: Thu, 14 Aug 2025 06:34:24 GMT  
		Size: 22.3 KB (22342 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:78a21084b1c4e79dc2fffab373fb465acb723f351bffdc0639a504a5bdc6a2d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32566079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717e9950cc2b302a7f75cdc9919226e0160142934f76014b1a905aa5e39c4046`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d84227403935277ab9817ff62ad9fca6d45f7c109953945d36caa72d73813d0`  
		Last Modified: Wed, 13 Aug 2025 23:02:57 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb0aae300c3cd52b99acd2ae25cb8bf507859ae7b182097672be779a7337fd4`  
		Last Modified: Wed, 13 Aug 2025 23:02:58 GMT  
		Size: 153.4 KB (153369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd2017b19819b1012be52dad0541d85c7797897955d5d0b747b8b86f08da76e`  
		Last Modified: Wed, 13 Aug 2025 23:03:00 GMT  
		Size: 2.3 MB (2275152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad146d7e60bd2063118973d72ff4507de475a826636f2b8fc3bdf36633379d07`  
		Last Modified: Wed, 13 Aug 2025 23:02:59 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fe42a1afd3681fa0efd222132b453c718236f571b4b56018cf362f2333cfb7`  
		Last Modified: Wed, 13 Aug 2025 23:02:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:f34a398dc1f988e0076ebc490e58021e7dc24976392ab10fb871628e11888166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98dee621777b57d248833b652d7622be9c6c901776820489ce629be6f59e5d5f`

```dockerfile
```

-	Layers:
	-	`sha256:4b5fb9727c43d6c906cc0c58b470a99299321ac1e3bcc6a9ea9ec90086d4260d`  
		Last Modified: Thu, 14 Aug 2025 00:34:33 GMT  
		Size: 2.0 MB (2007648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a88652c31f79e7599a31a3fe7d0341deeb4915c7ae0dab214e3c4768ec058300`  
		Last Modified: Thu, 14 Aug 2025 00:34:33 GMT  
		Size: 22.4 KB (22393 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; 386

```console
$ docker pull memcached@sha256:5b9ccecd7eb2ba800cc927d7dfaa5941d25387818d57d8583260ed7d5ea2ef8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33682664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c160d159b0b83b9824df1d8b4cbe201c4c67902d0171a4a03282d3e230939d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:346d0c953bdbc38917a27a6f30726e5b46419d98ecaf4d2d8f201bc3b7025e57`  
		Last Modified: Tue, 12 Aug 2025 20:45:00 GMT  
		Size: 31.3 MB (31289378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1f928fbfcc7da63ca647a381869549b7db17d2971110bc771c27aeed80b33c`  
		Last Modified: Wed, 13 Aug 2025 21:09:56 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49988f067cdbb2558e23451192304fe7f89c2cbe23fcf5463b9e0b80dfbd2a36`  
		Last Modified: Wed, 13 Aug 2025 21:09:56 GMT  
		Size: 147.4 KB (147419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19f3e01a2ee783f4cf292ba84f151492df7a0170128094f4d011075d629af43`  
		Last Modified: Wed, 13 Aug 2025 21:09:56 GMT  
		Size: 2.2 MB (2244354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2288d51449876e6f7fb89b6cac2eda51fef5f03deb3722ef32bf3a9bdc2f5e17`  
		Last Modified: Wed, 13 Aug 2025 21:09:56 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3668cc13fc1544b7319b7b3307e0d74b4e82d36ca065c5a3be7d080267054267`  
		Last Modified: Wed, 13 Aug 2025 21:09:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:df8cca141522937dd5415946521e71f57731ecc574e78d3175b26ce6260dcd46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2026627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff448533f7fe52a0dc6195d7b9320b996bd2623b7c1e7a5b02f7f5cee32b92a4`

```dockerfile
```

-	Layers:
	-	`sha256:80c0a6ea529144e269d6dc30e72d370cfbc53736314c92cca55d737de9562dd6`  
		Last Modified: Wed, 13 Aug 2025 21:34:31 GMT  
		Size: 2.0 MB (2004489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32faf37cac7f889e11009fc41358994c9714a5ebc9aed8843e1fb57a3de6d243`  
		Last Modified: Wed, 13 Aug 2025 21:34:32 GMT  
		Size: 22.1 KB (22138 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:dcc628faf353367b245beec24d23d1b3103986479dff33e10653c5ef2d8b54b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36182904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d113eca2d57658d5e20bd62171298229010cdbce2c33479664dcad6be5ec2acd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26c42ec1bf9e33e4a6a75b57802a57b9d166fccf4b2e5b13cef2b9742fc5025`  
		Last Modified: Thu, 14 Aug 2025 02:32:42 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a82df09860007e05001d706e92e1aa450bfd12fc72a24522ccca5edc6f43cd`  
		Last Modified: Thu, 14 Aug 2025 02:32:42 GMT  
		Size: 170.2 KB (170241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f425e49b56f20bc4209bec20b1ab8671bd728a94104369def1c947c90134052`  
		Last Modified: Thu, 14 Aug 2025 02:32:42 GMT  
		Size: 2.4 MB (2416933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b832c8b1a0256fd9b38e9fd823309571e179c77a2f44d5115f06ae282b7972f`  
		Last Modified: Thu, 14 Aug 2025 02:32:42 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da165b338847a53b7c8a0a0a08c089c86721f3997c5f507291c4737245ade82f`  
		Last Modified: Thu, 14 Aug 2025 02:32:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:d11fb93c72d4e4416799b886acc2230eefbe26e6381d65c674a1a47f310f22ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2154e1260dfec440f34afa1451b8e89c13a23e1eb451b2250766c9c88cf993a`

```dockerfile
```

-	Layers:
	-	`sha256:3c0cb7a63a69d321f183e466c5c0a934dd9a09173b6e174e2f17a9a24e241dee`  
		Last Modified: Thu, 14 Aug 2025 03:34:34 GMT  
		Size: 2.0 MB (2010933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e4dcd6c60091d8eaa78af8659654106ffc91270b3f5b4b6e166f41e295e361f`  
		Last Modified: Thu, 14 Aug 2025 03:34:35 GMT  
		Size: 22.3 KB (22269 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:c7b8d8a8065d2a0ea3bdaaadd564986a39a88ad9d9ef599faf4f923888bb9126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32288745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6fca6b4af0e7ae24559fc296fb0ce831a94645f64b986956f57f9306df1ed22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024aba4218861d2cdfa6f7186fcca6f2f2041ce6c7210cd258e28d55a2c1fa16`  
		Last Modified: Thu, 14 Aug 2025 02:58:06 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2b32b5cc5f77750b103e7bdeb63810088dca53dae4f8b6eed4e17f219a5826`  
		Last Modified: Thu, 14 Aug 2025 02:58:05 GMT  
		Size: 140.4 KB (140388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a046ba92157d2c0b391049e3f702ebcac682b0c6ee6e651f44d940e5d9bd8cd7`  
		Last Modified: Thu, 14 Aug 2025 02:58:07 GMT  
		Size: 2.3 MB (2313787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd7d0eef9a2ce528ea647334f74bfda29496059b15274182ae0d16fb7e5f28d`  
		Last Modified: Thu, 14 Aug 2025 02:58:06 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c5230e4318cec0912586827ea533d6abfaed20ff08b3662b6cf6871a9abae1`  
		Last Modified: Thu, 14 Aug 2025 02:58:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:88badce3b30eeb4fdb00156647e4a3479b0c7cf8dddb286e0bd07105084f4e5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7704cd55751a22fc58eb4a349020abdd760508cd1b9344ccb0df28dc62d35f98`

```dockerfile
```

-	Layers:
	-	`sha256:91e3962d713f291258d33cdc619c48c657c3a72b3a6c808786e3b209389502b2`  
		Last Modified: Thu, 14 Aug 2025 03:34:39 GMT  
		Size: 2.0 MB (2008769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76baa03c0dea63878577ee4ab27db735c1db244cbefee8f9c7b5d5eb4d3887f1`  
		Last Modified: Thu, 14 Aug 2025 03:34:39 GMT  
		Size: 22.2 KB (22196 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6`

```console
$ docker pull memcached@sha256:c8b53d421310f274ece68507406126575bfc2af3ddc66b72709f81ede5fbe2a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:1.6` - linux; amd64

```console
$ docker pull memcached@sha256:489c2e770f5baac8e88e7b0fc7bd9ec7482c560232093860fa776480fd535059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32204915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09da43b5484edc83f2f153e8f750eae1edfc09a59f9c3c8a0d1543ad028f7702`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebfc0a813c97c15541bf6e00db67cec64e96bf712ccfedb445eff79095d78dd6`  
		Last Modified: Wed, 13 Aug 2025 21:21:18 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d44cb640c5a78307f95a5ba37e9b3ff77e080db5144ad044331bdd27e2ac3b8`  
		Last Modified: Wed, 13 Aug 2025 21:21:32 GMT  
		Size: 136.6 KB (136560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c2449a0115fae5ca7c26d3857bdae261f4168d8334ad67cb6c3461a0910fc6`  
		Last Modified: Wed, 13 Aug 2025 21:21:36 GMT  
		Size: 2.3 MB (2293557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9bbdd035dc48ae794ba5af4721f9afdab19142a19ba004aa4b42738ef8758d8`  
		Last Modified: Wed, 13 Aug 2025 21:21:42 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc99f3761e7cd9c6f00023c8aa0d889222b7b233949d24870d0f9b7ad10f58dd`  
		Last Modified: Wed, 13 Aug 2025 21:21:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:98607b9259666dec40f29b040ae0cac2276fac6541257d7f3a4d2fa8d30e3ae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2029528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ad42f4e39d2637475a5aaa10a446b94d8cb9b730bd194a0f995abf19ecba3e7`

```dockerfile
```

-	Layers:
	-	`sha256:249ac3e00cc732e2b029808c9c00d3520da2cdf38b1fc01081a592ea90a5e050`  
		Last Modified: Wed, 13 Aug 2025 21:34:23 GMT  
		Size: 2.0 MB (2007332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fdd95540cec834ae6e6c6bf9ad1d03f83f75af3a4d5bc52a9b7018dd212823a`  
		Last Modified: Wed, 13 Aug 2025 21:34:24 GMT  
		Size: 22.2 KB (22196 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:11a993750bd36cfb7d37197d06ccbf217f829c9012146de0d45d0e3494add433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30314569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c2cfe621133fc4a453c7272eacac5ac0ae1cd214c7f7076d785ec3ed0fb6554`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:498399880872f14c562c46bd2a1ef4cfcf3c2a1453514ff0d0f6b7d89f8010dd`  
		Last Modified: Tue, 12 Aug 2025 22:02:01 GMT  
		Size: 27.9 MB (27941706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a99137a20a1adabf0ea411a3bed51f642b1fd51a7c56596ed760ece4727e8c3`  
		Last Modified: Wed, 13 Aug 2025 23:01:56 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7528817abdc345977b6df3988bcacfd622b20f1e6b64e6c01f3c3203275806`  
		Last Modified: Wed, 13 Aug 2025 23:01:57 GMT  
		Size: 144.0 KB (144046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5147466300d5970b08521247c1dcffd9c72644b33c0c4c7a7455293fdaa7514d`  
		Last Modified: Wed, 13 Aug 2025 23:01:58 GMT  
		Size: 2.2 MB (2227304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403dfb443663282b32ef64dddd4d9ece2badd91a91669659aad2213ef1db444c`  
		Last Modified: Wed, 13 Aug 2025 23:00:39 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ac9453a3752c151d9eb3d487d5be8ee9971ce482aa48cbcbffa05e594977ac`  
		Last Modified: Wed, 13 Aug 2025 23:01:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:99d7cc2296b1fdf18d0156098b6c8db466fa371221860e1628d6da1f33862b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe55e32abc4c444556bb77a6cd989bc4c29ae0720781b045162ad41710f332b0`

```dockerfile
```

-	Layers:
	-	`sha256:49bb7a93a18c7972be0483acacb6a99b49edc4bf097a764ed976c48c0516bc14`  
		Last Modified: Thu, 14 Aug 2025 00:34:25 GMT  
		Size: 2.0 MB (2010335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b1896ac27634d50430d62234a56bf5e22627fb59bbe9e2f974832c3f5823cfd`  
		Last Modified: Thu, 14 Aug 2025 00:34:26 GMT  
		Size: 22.3 KB (22343 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v7

```console
$ docker pull memcached@sha256:4b9bce762cb0cd433a31cf56c571b0a5bb7789813cbb111958bf806cba8b87af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28526851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a10eddf8fe36bdc9bc58ad2f45be5555dd9f6f746d916f9ce491ee5f8239bf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc714abeba0eb64ab96f4d3b22e0750d8fb5ca04c15135a1da25d7f28cb90c8`  
		Last Modified: Thu, 14 Aug 2025 03:26:02 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b548feee9753e7f47e9e09d371fbbc5da58c093655fbe6a70e9e8ce1792c6ddc`  
		Last Modified: Thu, 14 Aug 2025 03:26:02 GMT  
		Size: 135.3 KB (135298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9fd10cb429ca884c5738921b455ecc2d83781179e716d4003166bdc8c44e27`  
		Last Modified: Thu, 14 Aug 2025 03:26:01 GMT  
		Size: 2.2 MB (2182550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59893ea711e5a2631eada91282e598b013d3173b17a0edb0fdbe97d67d122e7`  
		Last Modified: Thu, 14 Aug 2025 03:26:02 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8512db29f6abd27987969691ca0de8c6cc141db19a00f2e80bd8996e6cb5de`  
		Last Modified: Thu, 14 Aug 2025 03:26:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:f4b425f37419b579837d2d7857c8ed429c6b2356824bf7c3f83036db9125cc20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f026c9ae0860a234d056b9a6607c5d4673b4e40c52e93c31e76e3cf463fa3c45`

```dockerfile
```

-	Layers:
	-	`sha256:58eba98bd420cdad2a71753e58bb1b1a587f0039d88944045180d74e4c08996c`  
		Last Modified: Thu, 14 Aug 2025 06:34:23 GMT  
		Size: 2.0 MB (2008792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab426c3e7d709a71c837bd5c98de92c219718788268a0700d3c8305f5117b7b8`  
		Last Modified: Thu, 14 Aug 2025 06:34:24 GMT  
		Size: 22.3 KB (22342 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:78a21084b1c4e79dc2fffab373fb465acb723f351bffdc0639a504a5bdc6a2d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32566079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717e9950cc2b302a7f75cdc9919226e0160142934f76014b1a905aa5e39c4046`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d84227403935277ab9817ff62ad9fca6d45f7c109953945d36caa72d73813d0`  
		Last Modified: Wed, 13 Aug 2025 23:02:57 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb0aae300c3cd52b99acd2ae25cb8bf507859ae7b182097672be779a7337fd4`  
		Last Modified: Wed, 13 Aug 2025 23:02:58 GMT  
		Size: 153.4 KB (153369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd2017b19819b1012be52dad0541d85c7797897955d5d0b747b8b86f08da76e`  
		Last Modified: Wed, 13 Aug 2025 23:03:00 GMT  
		Size: 2.3 MB (2275152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad146d7e60bd2063118973d72ff4507de475a826636f2b8fc3bdf36633379d07`  
		Last Modified: Wed, 13 Aug 2025 23:02:59 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fe42a1afd3681fa0efd222132b453c718236f571b4b56018cf362f2333cfb7`  
		Last Modified: Wed, 13 Aug 2025 23:02:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:f34a398dc1f988e0076ebc490e58021e7dc24976392ab10fb871628e11888166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98dee621777b57d248833b652d7622be9c6c901776820489ce629be6f59e5d5f`

```dockerfile
```

-	Layers:
	-	`sha256:4b5fb9727c43d6c906cc0c58b470a99299321ac1e3bcc6a9ea9ec90086d4260d`  
		Last Modified: Thu, 14 Aug 2025 00:34:33 GMT  
		Size: 2.0 MB (2007648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a88652c31f79e7599a31a3fe7d0341deeb4915c7ae0dab214e3c4768ec058300`  
		Last Modified: Thu, 14 Aug 2025 00:34:33 GMT  
		Size: 22.4 KB (22393 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; 386

```console
$ docker pull memcached@sha256:5b9ccecd7eb2ba800cc927d7dfaa5941d25387818d57d8583260ed7d5ea2ef8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33682664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c160d159b0b83b9824df1d8b4cbe201c4c67902d0171a4a03282d3e230939d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:346d0c953bdbc38917a27a6f30726e5b46419d98ecaf4d2d8f201bc3b7025e57`  
		Last Modified: Tue, 12 Aug 2025 20:45:00 GMT  
		Size: 31.3 MB (31289378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1f928fbfcc7da63ca647a381869549b7db17d2971110bc771c27aeed80b33c`  
		Last Modified: Wed, 13 Aug 2025 21:09:56 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49988f067cdbb2558e23451192304fe7f89c2cbe23fcf5463b9e0b80dfbd2a36`  
		Last Modified: Wed, 13 Aug 2025 21:09:56 GMT  
		Size: 147.4 KB (147419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19f3e01a2ee783f4cf292ba84f151492df7a0170128094f4d011075d629af43`  
		Last Modified: Wed, 13 Aug 2025 21:09:56 GMT  
		Size: 2.2 MB (2244354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2288d51449876e6f7fb89b6cac2eda51fef5f03deb3722ef32bf3a9bdc2f5e17`  
		Last Modified: Wed, 13 Aug 2025 21:09:56 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3668cc13fc1544b7319b7b3307e0d74b4e82d36ca065c5a3be7d080267054267`  
		Last Modified: Wed, 13 Aug 2025 21:09:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:df8cca141522937dd5415946521e71f57731ecc574e78d3175b26ce6260dcd46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2026627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff448533f7fe52a0dc6195d7b9320b996bd2623b7c1e7a5b02f7f5cee32b92a4`

```dockerfile
```

-	Layers:
	-	`sha256:80c0a6ea529144e269d6dc30e72d370cfbc53736314c92cca55d737de9562dd6`  
		Last Modified: Wed, 13 Aug 2025 21:34:31 GMT  
		Size: 2.0 MB (2004489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32faf37cac7f889e11009fc41358994c9714a5ebc9aed8843e1fb57a3de6d243`  
		Last Modified: Wed, 13 Aug 2025 21:34:32 GMT  
		Size: 22.1 KB (22138 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:dcc628faf353367b245beec24d23d1b3103986479dff33e10653c5ef2d8b54b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36182904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d113eca2d57658d5e20bd62171298229010cdbce2c33479664dcad6be5ec2acd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26c42ec1bf9e33e4a6a75b57802a57b9d166fccf4b2e5b13cef2b9742fc5025`  
		Last Modified: Thu, 14 Aug 2025 02:32:42 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a82df09860007e05001d706e92e1aa450bfd12fc72a24522ccca5edc6f43cd`  
		Last Modified: Thu, 14 Aug 2025 02:32:42 GMT  
		Size: 170.2 KB (170241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f425e49b56f20bc4209bec20b1ab8671bd728a94104369def1c947c90134052`  
		Last Modified: Thu, 14 Aug 2025 02:32:42 GMT  
		Size: 2.4 MB (2416933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b832c8b1a0256fd9b38e9fd823309571e179c77a2f44d5115f06ae282b7972f`  
		Last Modified: Thu, 14 Aug 2025 02:32:42 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da165b338847a53b7c8a0a0a08c089c86721f3997c5f507291c4737245ade82f`  
		Last Modified: Thu, 14 Aug 2025 02:32:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:d11fb93c72d4e4416799b886acc2230eefbe26e6381d65c674a1a47f310f22ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2154e1260dfec440f34afa1451b8e89c13a23e1eb451b2250766c9c88cf993a`

```dockerfile
```

-	Layers:
	-	`sha256:3c0cb7a63a69d321f183e466c5c0a934dd9a09173b6e174e2f17a9a24e241dee`  
		Last Modified: Thu, 14 Aug 2025 03:34:34 GMT  
		Size: 2.0 MB (2010933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e4dcd6c60091d8eaa78af8659654106ffc91270b3f5b4b6e166f41e295e361f`  
		Last Modified: Thu, 14 Aug 2025 03:34:35 GMT  
		Size: 22.3 KB (22269 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; s390x

```console
$ docker pull memcached@sha256:c7b8d8a8065d2a0ea3bdaaadd564986a39a88ad9d9ef599faf4f923888bb9126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32288745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6fca6b4af0e7ae24559fc296fb0ce831a94645f64b986956f57f9306df1ed22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024aba4218861d2cdfa6f7186fcca6f2f2041ce6c7210cd258e28d55a2c1fa16`  
		Last Modified: Thu, 14 Aug 2025 02:58:06 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2b32b5cc5f77750b103e7bdeb63810088dca53dae4f8b6eed4e17f219a5826`  
		Last Modified: Thu, 14 Aug 2025 02:58:05 GMT  
		Size: 140.4 KB (140388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a046ba92157d2c0b391049e3f702ebcac682b0c6ee6e651f44d940e5d9bd8cd7`  
		Last Modified: Thu, 14 Aug 2025 02:58:07 GMT  
		Size: 2.3 MB (2313787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd7d0eef9a2ce528ea647334f74bfda29496059b15274182ae0d16fb7e5f28d`  
		Last Modified: Thu, 14 Aug 2025 02:58:06 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c5230e4318cec0912586827ea533d6abfaed20ff08b3662b6cf6871a9abae1`  
		Last Modified: Thu, 14 Aug 2025 02:58:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:88badce3b30eeb4fdb00156647e4a3479b0c7cf8dddb286e0bd07105084f4e5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7704cd55751a22fc58eb4a349020abdd760508cd1b9344ccb0df28dc62d35f98`

```dockerfile
```

-	Layers:
	-	`sha256:91e3962d713f291258d33cdc619c48c657c3a72b3a6c808786e3b209389502b2`  
		Last Modified: Thu, 14 Aug 2025 03:34:39 GMT  
		Size: 2.0 MB (2008769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76baa03c0dea63878577ee4ab27db735c1db244cbefee8f9c7b5d5eb4d3887f1`  
		Last Modified: Thu, 14 Aug 2025 03:34:39 GMT  
		Size: 22.2 KB (22196 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine`

```console
$ docker pull memcached@sha256:b50070f2faf253d8aacd530742e8e71791a39222c75abcdbcc442dbb7a2f3f25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
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
$ docker pull memcached@sha256:033134f4dd9f45d4e22b6e98b040ea3fccf0dca740af3c949b44bebf458b04d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5904246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca259aa2216a248c482fc8a069d48b1e70b087529d2c3de97154bfa458dbb7a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fb46bc7dee2beda6f5f6f567aecd4d7d7698b9749ed917988a859b7dd96e30`  
		Last Modified: Tue, 29 Jul 2025 16:32:22 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48faf8c85515fb9d17e0752e77d8241f223d53b1adc90439c606d17daabd0ae`  
		Last Modified: Tue, 29 Jul 2025 16:32:24 GMT  
		Size: 104.7 KB (104725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d552a2d777fd444b41cb79438f9f1b441821162e78d73e96dc848a773cf43892`  
		Last Modified: Tue, 29 Jul 2025 16:32:24 GMT  
		Size: 2.0 MB (1998477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c70665f30f3e15975d429b494cb17b21c5d4630c1800cb0addc3fce3a11aa29`  
		Last Modified: Tue, 29 Jul 2025 16:32:20 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ff68520caaf588cec750ad7c403cf55d79eecfff4b7a4ac5eb3910c90c2817`  
		Last Modified: Tue, 29 Jul 2025 16:32:21 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7b27e0df383f45d6d523345a078898524a69cee4d6978cf64bf26532b8679dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 KB (116752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb88e7ee6d3e67b2e4f307c081504a685666917ddf50770fe8beb5abd60a3dc5`

```dockerfile
```

-	Layers:
	-	`sha256:2cf00a09ffccb2c00421311314137de90d0586c126b79dbe5315ce321c168b34`  
		Last Modified: Tue, 29 Jul 2025 18:35:07 GMT  
		Size: 96.2 KB (96180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55325ecc9b276e9c55badf949ed4f06840c34aa8baf0aa6f974e0b90dc5d4e0d`  
		Last Modified: Tue, 29 Jul 2025 18:35:07 GMT  
		Size: 20.6 KB (20572 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:78b59dd3af5a55e950f5106869e642af122a7dc470545f4ba533f6833d83b62c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5550795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb09d5ce1b7010f7a36d77494bc5358d666339628c183692906db6a961373847`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c710b5ddcc2882c5014d0c8cb93aec2bd8b6cc3c59fd42b40c87d94f89a7bc7f`  
		Last Modified: Wed, 23 Jul 2025 22:59:16 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c42040d822a4af7f05f9ccd4d18a7a5e4712b118b7f18d1a7969761029a9d2`  
		Last Modified: Wed, 23 Jul 2025 22:59:16 GMT  
		Size: 101.5 KB (101533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3095e18cd24048696efd57ac64d04dde381a3abde625964e02165c7364eb5633`  
		Last Modified: Tue, 29 Jul 2025 16:50:12 GMT  
		Size: 1.9 MB (1947003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0436ec50f04ed972ff0dd760f7e820f192236e5e720bddb6173f65159c7c36`  
		Last Modified: Tue, 29 Jul 2025 16:50:11 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671c24aae36bb04a32e05bd64e1371384f594889cdbbc41029c916447666d402`  
		Last Modified: Tue, 29 Jul 2025 16:50:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c2a050c6822d834285577c3a001fdfcf9949b7f5a483a4a76a49b549bea19641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54e8bda3e734528caeab4505f084ca7a3076d5ec2273287f66954b5e91af42f`

```dockerfile
```

-	Layers:
	-	`sha256:0d86924831d61ce8b792b25421e9ff0fa2eda9ab940eba5309d44d0eeada7e8e`  
		Last Modified: Tue, 29 Jul 2025 18:35:11 GMT  
		Size: 20.5 KB (20506 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:c9f5db2389b9b0b4a2cd199c4417a9f49a60c42d616e8421177e662d4830de07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9421ed030d4b6b6405714612b8858bda87bc53ac8b0c5ed65c582119527f2d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251060498ca8f0484e20714689b9caba533d09c1b74ed8f2a06780db515a28e2`  
		Last Modified: Thu, 24 Jul 2025 00:27:37 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2293bd2fb47d57e5869c197133067e17f9b1e51ea0f298af1e480e7fd33d681`  
		Last Modified: Thu, 24 Jul 2025 00:27:38 GMT  
		Size: 91.3 KB (91313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ae82f2bac2f7e6fe57f8cb7006fc227c972da1ae5749eba9f5f73e6f3248ec`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 1.9 MB (1905692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e60bf2b2164c620b69e40bdcb64d4104d02eab86c96ea6e170a3601b9ecfd82`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665fe4cd856f1a5c2193568e756c572656949b17c381fc8d43efaa823e18cfa7`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:376a71bc0fef7741e92fdae8b96c825c4622e980de01e724b1a3a0bec3d95f20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 KB (116963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22b574f6c6d021a917c0e99ff4800d8ac3c22fb94b94f88c404cc7609f562fb5`

```dockerfile
```

-	Layers:
	-	`sha256:58ebd4bc7ee5888c552e0fa618f93aefbdb1d15a56ecd3abef19a46ce2f93eee`  
		Last Modified: Tue, 29 Jul 2025 18:35:15 GMT  
		Size: 96.2 KB (96248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d432ed2053ed8249834dd5016fe3199bbc3f82dc7013027c3ead9efe2a007b98`  
		Last Modified: Tue, 29 Jul 2025 18:35:16 GMT  
		Size: 20.7 KB (20715 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b5e4ecc3e927ee30e5cfcfc8aa044960631c75eb8abed9d0fcee6232aa5fdf79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6241700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c880dc2c785861dc9010b813bb6f533f30518443a3bb7e7f477bc96af14582`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbfeb6ac9fd2045c5bea10a301ad554c1f703ffc2885c41520dd5e42eb4a59a`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47acaa5035f94aed634b9d7ecae02fb3838f19e38f8e752ecd6cfba97699b31`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 120.8 KB (120812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8160f3136c6863b52f0dec4f9918b91b8a509700b2071ec0aecd5a6231f00f2a`  
		Last Modified: Tue, 29 Jul 2025 16:41:09 GMT  
		Size: 2.0 MB (1988782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff22f0cad01950efb78a7a862b0becb8b2fd22d795b585f97dad66c091c3dd7`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed19cbfb574c7d8cab364e2ec072c0e03f694468ada41cd70bfcd35392df9e7`  
		Last Modified: Tue, 29 Jul 2025 16:41:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b4c81c7ababb91ecdda3b7d70514d16818602199d759eb2aadd74de732d52960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 KB (117055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80452fd4f79f6e7a0dab0beebf5c144f9df7c257255cdd3cb93ccbff77001fd6`

```dockerfile
```

-	Layers:
	-	`sha256:f11d2a322f6088804ee63ae1a77b9d5ddcdfdc0c65c22e7a70b7ee67cf4532ed`  
		Last Modified: Tue, 29 Jul 2025 18:35:20 GMT  
		Size: 96.3 KB (96284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e225dd6ea14146ddf445598f24189c065ec684fbeb92e7d053a0211a7d60efda`  
		Last Modified: Tue, 29 Jul 2025 18:35:21 GMT  
		Size: 20.8 KB (20771 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:c58767364161c180098aa6daf4620c8c55ad8713deb64ca620668e7bb829bb41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5683246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac911958149764a83bf951afae4135a482e9064dd0c7dbee61474116cf4bc68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1f621f1e5b25aa798d604ab87259f546a42e522b1311f962484669d45183fa`  
		Last Modified: Tue, 29 Jul 2025 16:32:40 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7cf471d76eab33abc760b1edf151f0e3d4d73732c3f002c74ef629f8ded5f9`  
		Last Modified: Tue, 29 Jul 2025 16:32:39 GMT  
		Size: 109.5 KB (109523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a287f0dc98767a99d5c18925da988244c99243b51f5870a4ed36648b93518402`  
		Last Modified: Tue, 29 Jul 2025 16:32:42 GMT  
		Size: 2.0 MB (1957368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101df272f2e8c1be378c334f0d3d2de9dcd2c58db6fe3580d4451396deef84de`  
		Last Modified: Tue, 29 Jul 2025 16:32:41 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f870cbd8529325263ac998fe634981f154a171a39da706e91a9ea2d91038d361`  
		Last Modified: Tue, 29 Jul 2025 16:32:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:837e0ff5feebc7262c78ddd6b4bece1b5b4c3c22b0eb71b71bf9c6c9d154b416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.7 KB (116651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf22108f9222361c74085ca0633d2876cf3187ccaeb4353499f02fc7a24cc51b`

```dockerfile
```

-	Layers:
	-	`sha256:5143c40f563e8ee15ea82be605c093d36fd7445bcd1cedc45d0754c52b6d3f9d`  
		Last Modified: Tue, 29 Jul 2025 18:35:24 GMT  
		Size: 96.1 KB (96135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fcabff32e4e745d2c95395b620e73b812d1c38929ba82167c1d76583a2f4150`  
		Last Modified: Tue, 29 Jul 2025 18:35:25 GMT  
		Size: 20.5 KB (20516 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:04386ede5dcbf35cabad144bcdc951cc64882f7b9727f2d09927fe0d5551dd19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5942089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8252590eee78d67456ac83fd8279259aaea4d2a555c8bc20b173663fcaa2883`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc22e0cec7e7fe8cff10539bca58363ad6749e2de4f878015c25b5f2b6ecadb9`  
		Last Modified: Tue, 29 Jul 2025 16:33:46 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992ebe18219bd78e59e7e56661aae22f700927f47bc7ad1dfe7717093b371c15`  
		Last Modified: Tue, 29 Jul 2025 16:33:49 GMT  
		Size: 124.3 KB (124315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953f5a37d23881d59809ea64dc6ebf1a152a1ff8929f51befb10577771755f5d`  
		Last Modified: Tue, 29 Jul 2025 16:33:49 GMT  
		Size: 2.1 MB (2089310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b62870a2d7b266495d83cfd72dcf702c91c5c60a7e29836bd9bdac776511a7`  
		Last Modified: Tue, 29 Jul 2025 16:33:47 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1cc8c0fe9a4ef7e2ef70e32ddbfbd2fd68985dd452630a8f390c5b41c654f8`  
		Last Modified: Tue, 29 Jul 2025 16:33:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:cf7e9735e4ef5d00dc25928653b808214f070708e9d879ef54afc4d77ce9db2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcceb455cfdb86bdb0c165af3bc54cbab794d56fef1dbae2b484d28027db791c`

```dockerfile
```

-	Layers:
	-	`sha256:a40704a0afb5cf1b90c0fbdf73c5218a4d8f0e93bb39014507b5fa5f8c7265dd`  
		Last Modified: Tue, 29 Jul 2025 18:35:29 GMT  
		Size: 94.3 KB (94287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da22397f364310e72420738395739c36e25b4e4813bbc5da197582a91bb55ac9`  
		Last Modified: Tue, 29 Jul 2025 18:35:29 GMT  
		Size: 20.6 KB (20648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:d55b98c34ba1c2f546461bd57477d46ab868f9de6b107ffb8f20e06dab1e10d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1034dde2661f43165e85db9a13ff0e10d237d14d4b1b7ee1d4570f19d7df4e69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bbdcecb4dec3cbaba0500f9425897948884cfd8db95ccdf9b824d448b24049`  
		Last Modified: Wed, 23 Jul 2025 23:54:15 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c18051d55886d147cafcee8f9e220087c0b60c0e11ec8898a4005352ee0f7e4`  
		Last Modified: Wed, 23 Jul 2025 23:50:14 GMT  
		Size: 107.9 KB (107902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953c2b44fe537b63907764cf78cbb294c6a1133eacb39c62d35ee5d4914779cb`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 1.9 MB (1932977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d69b2f63abf91684a15b9de7b5e617996762376da3fdda50c4e20c2f1e0f4da`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57c134601fc15e8f2cf183cfd9a3057731ad48b915988217f51df31b5d3cf38`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d50b42de80ef3381b05da20cef4ba6ab4491facb607528e075c034257fe9d327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27766c161110b7e46063a39ce6e176f87233fd6722a825ec338e1568892a77a3`

```dockerfile
```

-	Layers:
	-	`sha256:f933f968a4a14795196607a1337a19431e9f61db78bb49c5c2f89f64a17a1d89`  
		Last Modified: Tue, 29 Jul 2025 18:35:33 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffc41094fe9f57bca69da70bbb18eca52aaf6d27d0fb6d79eda79f9e011a157a`  
		Last Modified: Tue, 29 Jul 2025 18:35:33 GMT  
		Size: 20.6 KB (20647 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:cfd223eb11df3d2297224d458caf974f3f0aae4742ff917812f1b8c84c84e705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5797268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e23f18e891a12e72ef84139504baf8783a7db21d4976fc0b607f8e9bbf736f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00131fb0ca26b15f1ac64b82554fc342b19f8c1ef38312a75addb6686f7bc24`  
		Last Modified: Tue, 29 Jul 2025 16:41:40 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e54da6ab620e035fd78987688d45401e87278ec8a5c02cef8a57e4ea9fd286`  
		Last Modified: Tue, 29 Jul 2025 16:41:42 GMT  
		Size: 113.5 KB (113499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6160f9fac1fd86eda224e9ce4740ea46f7e23dc7edb6d1fe9d830001313e63a`  
		Last Modified: Tue, 29 Jul 2025 16:41:46 GMT  
		Size: 2.0 MB (2037446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d01cd71d33b01b420652f4ad9275f1475f4f0bf253dc0a1b48198df2010be5`  
		Last Modified: Tue, 29 Jul 2025 16:41:52 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831dd5e3c39dd2744dc8823190095f709c36020b55ccdaf85f62a146582c7d9d`  
		Last Modified: Tue, 29 Jul 2025 16:41:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:79f0de7e4dcc9afdbfa1fa22250cf3e544d6f3c33174246b427d2865c7e343d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71dad4d71741d8d354038cb6898389aebb54c956dfcd865d57f78dcc3b238bf8`

```dockerfile
```

-	Layers:
	-	`sha256:f942bbb9520308ae352a056c148fdce8f6b09672c257e0a769aa2504bacf1845`  
		Last Modified: Tue, 29 Jul 2025 18:35:37 GMT  
		Size: 94.2 KB (94229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c46680ef7cf08a43965ab9c7727cc70268ee89e366a1ce1806d0f7980b4ad812`  
		Last Modified: Tue, 29 Jul 2025 18:35:38 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine3.22`

```console
$ docker pull memcached@sha256:b50070f2faf253d8aacd530742e8e71791a39222c75abcdbcc442dbb7a2f3f25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
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

### `memcached:1.6-alpine3.22` - linux; amd64

```console
$ docker pull memcached@sha256:033134f4dd9f45d4e22b6e98b040ea3fccf0dca740af3c949b44bebf458b04d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5904246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca259aa2216a248c482fc8a069d48b1e70b087529d2c3de97154bfa458dbb7a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fb46bc7dee2beda6f5f6f567aecd4d7d7698b9749ed917988a859b7dd96e30`  
		Last Modified: Tue, 29 Jul 2025 16:32:22 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48faf8c85515fb9d17e0752e77d8241f223d53b1adc90439c606d17daabd0ae`  
		Last Modified: Tue, 29 Jul 2025 16:32:24 GMT  
		Size: 104.7 KB (104725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d552a2d777fd444b41cb79438f9f1b441821162e78d73e96dc848a773cf43892`  
		Last Modified: Tue, 29 Jul 2025 16:32:24 GMT  
		Size: 2.0 MB (1998477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c70665f30f3e15975d429b494cb17b21c5d4630c1800cb0addc3fce3a11aa29`  
		Last Modified: Tue, 29 Jul 2025 16:32:20 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ff68520caaf588cec750ad7c403cf55d79eecfff4b7a4ac5eb3910c90c2817`  
		Last Modified: Tue, 29 Jul 2025 16:32:21 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:7b27e0df383f45d6d523345a078898524a69cee4d6978cf64bf26532b8679dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 KB (116752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb88e7ee6d3e67b2e4f307c081504a685666917ddf50770fe8beb5abd60a3dc5`

```dockerfile
```

-	Layers:
	-	`sha256:2cf00a09ffccb2c00421311314137de90d0586c126b79dbe5315ce321c168b34`  
		Last Modified: Tue, 29 Jul 2025 18:35:07 GMT  
		Size: 96.2 KB (96180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55325ecc9b276e9c55badf949ed4f06840c34aa8baf0aa6f974e0b90dc5d4e0d`  
		Last Modified: Tue, 29 Jul 2025 18:35:07 GMT  
		Size: 20.6 KB (20572 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.22` - linux; arm variant v6

```console
$ docker pull memcached@sha256:78b59dd3af5a55e950f5106869e642af122a7dc470545f4ba533f6833d83b62c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5550795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb09d5ce1b7010f7a36d77494bc5358d666339628c183692906db6a961373847`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c710b5ddcc2882c5014d0c8cb93aec2bd8b6cc3c59fd42b40c87d94f89a7bc7f`  
		Last Modified: Wed, 23 Jul 2025 22:59:16 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c42040d822a4af7f05f9ccd4d18a7a5e4712b118b7f18d1a7969761029a9d2`  
		Last Modified: Wed, 23 Jul 2025 22:59:16 GMT  
		Size: 101.5 KB (101533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3095e18cd24048696efd57ac64d04dde381a3abde625964e02165c7364eb5633`  
		Last Modified: Tue, 29 Jul 2025 16:50:12 GMT  
		Size: 1.9 MB (1947003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0436ec50f04ed972ff0dd760f7e820f192236e5e720bddb6173f65159c7c36`  
		Last Modified: Tue, 29 Jul 2025 16:50:11 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671c24aae36bb04a32e05bd64e1371384f594889cdbbc41029c916447666d402`  
		Last Modified: Tue, 29 Jul 2025 16:50:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:c2a050c6822d834285577c3a001fdfcf9949b7f5a483a4a76a49b549bea19641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54e8bda3e734528caeab4505f084ca7a3076d5ec2273287f66954b5e91af42f`

```dockerfile
```

-	Layers:
	-	`sha256:0d86924831d61ce8b792b25421e9ff0fa2eda9ab940eba5309d44d0eeada7e8e`  
		Last Modified: Tue, 29 Jul 2025 18:35:11 GMT  
		Size: 20.5 KB (20506 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.22` - linux; arm variant v7

```console
$ docker pull memcached@sha256:c9f5db2389b9b0b4a2cd199c4417a9f49a60c42d616e8421177e662d4830de07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9421ed030d4b6b6405714612b8858bda87bc53ac8b0c5ed65c582119527f2d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251060498ca8f0484e20714689b9caba533d09c1b74ed8f2a06780db515a28e2`  
		Last Modified: Thu, 24 Jul 2025 00:27:37 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2293bd2fb47d57e5869c197133067e17f9b1e51ea0f298af1e480e7fd33d681`  
		Last Modified: Thu, 24 Jul 2025 00:27:38 GMT  
		Size: 91.3 KB (91313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ae82f2bac2f7e6fe57f8cb7006fc227c972da1ae5749eba9f5f73e6f3248ec`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 1.9 MB (1905692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e60bf2b2164c620b69e40bdcb64d4104d02eab86c96ea6e170a3601b9ecfd82`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665fe4cd856f1a5c2193568e756c572656949b17c381fc8d43efaa823e18cfa7`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:376a71bc0fef7741e92fdae8b96c825c4622e980de01e724b1a3a0bec3d95f20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 KB (116963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22b574f6c6d021a917c0e99ff4800d8ac3c22fb94b94f88c404cc7609f562fb5`

```dockerfile
```

-	Layers:
	-	`sha256:58ebd4bc7ee5888c552e0fa618f93aefbdb1d15a56ecd3abef19a46ce2f93eee`  
		Last Modified: Tue, 29 Jul 2025 18:35:15 GMT  
		Size: 96.2 KB (96248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d432ed2053ed8249834dd5016fe3199bbc3f82dc7013027c3ead9efe2a007b98`  
		Last Modified: Tue, 29 Jul 2025 18:35:16 GMT  
		Size: 20.7 KB (20715 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b5e4ecc3e927ee30e5cfcfc8aa044960631c75eb8abed9d0fcee6232aa5fdf79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6241700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c880dc2c785861dc9010b813bb6f533f30518443a3bb7e7f477bc96af14582`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbfeb6ac9fd2045c5bea10a301ad554c1f703ffc2885c41520dd5e42eb4a59a`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47acaa5035f94aed634b9d7ecae02fb3838f19e38f8e752ecd6cfba97699b31`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 120.8 KB (120812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8160f3136c6863b52f0dec4f9918b91b8a509700b2071ec0aecd5a6231f00f2a`  
		Last Modified: Tue, 29 Jul 2025 16:41:09 GMT  
		Size: 2.0 MB (1988782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff22f0cad01950efb78a7a862b0becb8b2fd22d795b585f97dad66c091c3dd7`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed19cbfb574c7d8cab364e2ec072c0e03f694468ada41cd70bfcd35392df9e7`  
		Last Modified: Tue, 29 Jul 2025 16:41:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:b4c81c7ababb91ecdda3b7d70514d16818602199d759eb2aadd74de732d52960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 KB (117055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80452fd4f79f6e7a0dab0beebf5c144f9df7c257255cdd3cb93ccbff77001fd6`

```dockerfile
```

-	Layers:
	-	`sha256:f11d2a322f6088804ee63ae1a77b9d5ddcdfdc0c65c22e7a70b7ee67cf4532ed`  
		Last Modified: Tue, 29 Jul 2025 18:35:20 GMT  
		Size: 96.3 KB (96284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e225dd6ea14146ddf445598f24189c065ec684fbeb92e7d053a0211a7d60efda`  
		Last Modified: Tue, 29 Jul 2025 18:35:21 GMT  
		Size: 20.8 KB (20771 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.22` - linux; 386

```console
$ docker pull memcached@sha256:c58767364161c180098aa6daf4620c8c55ad8713deb64ca620668e7bb829bb41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5683246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac911958149764a83bf951afae4135a482e9064dd0c7dbee61474116cf4bc68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1f621f1e5b25aa798d604ab87259f546a42e522b1311f962484669d45183fa`  
		Last Modified: Tue, 29 Jul 2025 16:32:40 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7cf471d76eab33abc760b1edf151f0e3d4d73732c3f002c74ef629f8ded5f9`  
		Last Modified: Tue, 29 Jul 2025 16:32:39 GMT  
		Size: 109.5 KB (109523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a287f0dc98767a99d5c18925da988244c99243b51f5870a4ed36648b93518402`  
		Last Modified: Tue, 29 Jul 2025 16:32:42 GMT  
		Size: 2.0 MB (1957368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101df272f2e8c1be378c334f0d3d2de9dcd2c58db6fe3580d4451396deef84de`  
		Last Modified: Tue, 29 Jul 2025 16:32:41 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f870cbd8529325263ac998fe634981f154a171a39da706e91a9ea2d91038d361`  
		Last Modified: Tue, 29 Jul 2025 16:32:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:837e0ff5feebc7262c78ddd6b4bece1b5b4c3c22b0eb71b71bf9c6c9d154b416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.7 KB (116651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf22108f9222361c74085ca0633d2876cf3187ccaeb4353499f02fc7a24cc51b`

```dockerfile
```

-	Layers:
	-	`sha256:5143c40f563e8ee15ea82be605c093d36fd7445bcd1cedc45d0754c52b6d3f9d`  
		Last Modified: Tue, 29 Jul 2025 18:35:24 GMT  
		Size: 96.1 KB (96135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fcabff32e4e745d2c95395b620e73b812d1c38929ba82167c1d76583a2f4150`  
		Last Modified: Tue, 29 Jul 2025 18:35:25 GMT  
		Size: 20.5 KB (20516 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.22` - linux; ppc64le

```console
$ docker pull memcached@sha256:04386ede5dcbf35cabad144bcdc951cc64882f7b9727f2d09927fe0d5551dd19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5942089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8252590eee78d67456ac83fd8279259aaea4d2a555c8bc20b173663fcaa2883`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc22e0cec7e7fe8cff10539bca58363ad6749e2de4f878015c25b5f2b6ecadb9`  
		Last Modified: Tue, 29 Jul 2025 16:33:46 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992ebe18219bd78e59e7e56661aae22f700927f47bc7ad1dfe7717093b371c15`  
		Last Modified: Tue, 29 Jul 2025 16:33:49 GMT  
		Size: 124.3 KB (124315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953f5a37d23881d59809ea64dc6ebf1a152a1ff8929f51befb10577771755f5d`  
		Last Modified: Tue, 29 Jul 2025 16:33:49 GMT  
		Size: 2.1 MB (2089310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b62870a2d7b266495d83cfd72dcf702c91c5c60a7e29836bd9bdac776511a7`  
		Last Modified: Tue, 29 Jul 2025 16:33:47 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1cc8c0fe9a4ef7e2ef70e32ddbfbd2fd68985dd452630a8f390c5b41c654f8`  
		Last Modified: Tue, 29 Jul 2025 16:33:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:cf7e9735e4ef5d00dc25928653b808214f070708e9d879ef54afc4d77ce9db2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcceb455cfdb86bdb0c165af3bc54cbab794d56fef1dbae2b484d28027db791c`

```dockerfile
```

-	Layers:
	-	`sha256:a40704a0afb5cf1b90c0fbdf73c5218a4d8f0e93bb39014507b5fa5f8c7265dd`  
		Last Modified: Tue, 29 Jul 2025 18:35:29 GMT  
		Size: 94.3 KB (94287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da22397f364310e72420738395739c36e25b4e4813bbc5da197582a91bb55ac9`  
		Last Modified: Tue, 29 Jul 2025 18:35:29 GMT  
		Size: 20.6 KB (20648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.22` - linux; riscv64

```console
$ docker pull memcached@sha256:d55b98c34ba1c2f546461bd57477d46ab868f9de6b107ffb8f20e06dab1e10d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1034dde2661f43165e85db9a13ff0e10d237d14d4b1b7ee1d4570f19d7df4e69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bbdcecb4dec3cbaba0500f9425897948884cfd8db95ccdf9b824d448b24049`  
		Last Modified: Wed, 23 Jul 2025 23:54:15 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c18051d55886d147cafcee8f9e220087c0b60c0e11ec8898a4005352ee0f7e4`  
		Last Modified: Wed, 23 Jul 2025 23:50:14 GMT  
		Size: 107.9 KB (107902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953c2b44fe537b63907764cf78cbb294c6a1133eacb39c62d35ee5d4914779cb`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 1.9 MB (1932977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d69b2f63abf91684a15b9de7b5e617996762376da3fdda50c4e20c2f1e0f4da`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57c134601fc15e8f2cf183cfd9a3057731ad48b915988217f51df31b5d3cf38`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:d50b42de80ef3381b05da20cef4ba6ab4491facb607528e075c034257fe9d327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27766c161110b7e46063a39ce6e176f87233fd6722a825ec338e1568892a77a3`

```dockerfile
```

-	Layers:
	-	`sha256:f933f968a4a14795196607a1337a19431e9f61db78bb49c5c2f89f64a17a1d89`  
		Last Modified: Tue, 29 Jul 2025 18:35:33 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffc41094fe9f57bca69da70bbb18eca52aaf6d27d0fb6d79eda79f9e011a157a`  
		Last Modified: Tue, 29 Jul 2025 18:35:33 GMT  
		Size: 20.6 KB (20647 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.22` - linux; s390x

```console
$ docker pull memcached@sha256:cfd223eb11df3d2297224d458caf974f3f0aae4742ff917812f1b8c84c84e705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5797268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e23f18e891a12e72ef84139504baf8783a7db21d4976fc0b607f8e9bbf736f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00131fb0ca26b15f1ac64b82554fc342b19f8c1ef38312a75addb6686f7bc24`  
		Last Modified: Tue, 29 Jul 2025 16:41:40 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e54da6ab620e035fd78987688d45401e87278ec8a5c02cef8a57e4ea9fd286`  
		Last Modified: Tue, 29 Jul 2025 16:41:42 GMT  
		Size: 113.5 KB (113499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6160f9fac1fd86eda224e9ce4740ea46f7e23dc7edb6d1fe9d830001313e63a`  
		Last Modified: Tue, 29 Jul 2025 16:41:46 GMT  
		Size: 2.0 MB (2037446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d01cd71d33b01b420652f4ad9275f1475f4f0bf253dc0a1b48198df2010be5`  
		Last Modified: Tue, 29 Jul 2025 16:41:52 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831dd5e3c39dd2744dc8823190095f709c36020b55ccdaf85f62a146582c7d9d`  
		Last Modified: Tue, 29 Jul 2025 16:41:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:79f0de7e4dcc9afdbfa1fa22250cf3e544d6f3c33174246b427d2865c7e343d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71dad4d71741d8d354038cb6898389aebb54c956dfcd865d57f78dcc3b238bf8`

```dockerfile
```

-	Layers:
	-	`sha256:f942bbb9520308ae352a056c148fdce8f6b09672c257e0a769aa2504bacf1845`  
		Last Modified: Tue, 29 Jul 2025 18:35:37 GMT  
		Size: 94.2 KB (94229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c46680ef7cf08a43965ab9c7727cc70268ee89e366a1ce1806d0f7980b4ad812`  
		Last Modified: Tue, 29 Jul 2025 18:35:38 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-trixie`

```console
$ docker pull memcached@sha256:c8b53d421310f274ece68507406126575bfc2af3ddc66b72709f81ede5fbe2a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:1.6-trixie` - linux; amd64

```console
$ docker pull memcached@sha256:489c2e770f5baac8e88e7b0fc7bd9ec7482c560232093860fa776480fd535059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32204915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09da43b5484edc83f2f153e8f750eae1edfc09a59f9c3c8a0d1543ad028f7702`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebfc0a813c97c15541bf6e00db67cec64e96bf712ccfedb445eff79095d78dd6`  
		Last Modified: Wed, 13 Aug 2025 21:21:18 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d44cb640c5a78307f95a5ba37e9b3ff77e080db5144ad044331bdd27e2ac3b8`  
		Last Modified: Wed, 13 Aug 2025 21:21:32 GMT  
		Size: 136.6 KB (136560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c2449a0115fae5ca7c26d3857bdae261f4168d8334ad67cb6c3461a0910fc6`  
		Last Modified: Wed, 13 Aug 2025 21:21:36 GMT  
		Size: 2.3 MB (2293557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9bbdd035dc48ae794ba5af4721f9afdab19142a19ba004aa4b42738ef8758d8`  
		Last Modified: Wed, 13 Aug 2025 21:21:42 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc99f3761e7cd9c6f00023c8aa0d889222b7b233949d24870d0f9b7ad10f58dd`  
		Last Modified: Wed, 13 Aug 2025 21:21:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:98607b9259666dec40f29b040ae0cac2276fac6541257d7f3a4d2fa8d30e3ae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2029528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ad42f4e39d2637475a5aaa10a446b94d8cb9b730bd194a0f995abf19ecba3e7`

```dockerfile
```

-	Layers:
	-	`sha256:249ac3e00cc732e2b029808c9c00d3520da2cdf38b1fc01081a592ea90a5e050`  
		Last Modified: Wed, 13 Aug 2025 21:34:23 GMT  
		Size: 2.0 MB (2007332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fdd95540cec834ae6e6c6bf9ad1d03f83f75af3a4d5bc52a9b7018dd212823a`  
		Last Modified: Wed, 13 Aug 2025 21:34:24 GMT  
		Size: 22.2 KB (22196 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:11a993750bd36cfb7d37197d06ccbf217f829c9012146de0d45d0e3494add433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30314569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c2cfe621133fc4a453c7272eacac5ac0ae1cd214c7f7076d785ec3ed0fb6554`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:498399880872f14c562c46bd2a1ef4cfcf3c2a1453514ff0d0f6b7d89f8010dd`  
		Last Modified: Tue, 12 Aug 2025 22:02:01 GMT  
		Size: 27.9 MB (27941706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a99137a20a1adabf0ea411a3bed51f642b1fd51a7c56596ed760ece4727e8c3`  
		Last Modified: Wed, 13 Aug 2025 23:01:56 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7528817abdc345977b6df3988bcacfd622b20f1e6b64e6c01f3c3203275806`  
		Last Modified: Wed, 13 Aug 2025 23:01:57 GMT  
		Size: 144.0 KB (144046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5147466300d5970b08521247c1dcffd9c72644b33c0c4c7a7455293fdaa7514d`  
		Last Modified: Wed, 13 Aug 2025 23:01:58 GMT  
		Size: 2.2 MB (2227304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403dfb443663282b32ef64dddd4d9ece2badd91a91669659aad2213ef1db444c`  
		Last Modified: Wed, 13 Aug 2025 23:00:39 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ac9453a3752c151d9eb3d487d5be8ee9971ce482aa48cbcbffa05e594977ac`  
		Last Modified: Wed, 13 Aug 2025 23:01:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:99d7cc2296b1fdf18d0156098b6c8db466fa371221860e1628d6da1f33862b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe55e32abc4c444556bb77a6cd989bc4c29ae0720781b045162ad41710f332b0`

```dockerfile
```

-	Layers:
	-	`sha256:49bb7a93a18c7972be0483acacb6a99b49edc4bf097a764ed976c48c0516bc14`  
		Last Modified: Thu, 14 Aug 2025 00:34:25 GMT  
		Size: 2.0 MB (2010335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b1896ac27634d50430d62234a56bf5e22627fb59bbe9e2f974832c3f5823cfd`  
		Last Modified: Thu, 14 Aug 2025 00:34:26 GMT  
		Size: 22.3 KB (22343 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:4b9bce762cb0cd433a31cf56c571b0a5bb7789813cbb111958bf806cba8b87af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28526851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a10eddf8fe36bdc9bc58ad2f45be5555dd9f6f746d916f9ce491ee5f8239bf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc714abeba0eb64ab96f4d3b22e0750d8fb5ca04c15135a1da25d7f28cb90c8`  
		Last Modified: Thu, 14 Aug 2025 03:26:02 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b548feee9753e7f47e9e09d371fbbc5da58c093655fbe6a70e9e8ce1792c6ddc`  
		Last Modified: Thu, 14 Aug 2025 03:26:02 GMT  
		Size: 135.3 KB (135298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9fd10cb429ca884c5738921b455ecc2d83781179e716d4003166bdc8c44e27`  
		Last Modified: Thu, 14 Aug 2025 03:26:01 GMT  
		Size: 2.2 MB (2182550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59893ea711e5a2631eada91282e598b013d3173b17a0edb0fdbe97d67d122e7`  
		Last Modified: Thu, 14 Aug 2025 03:26:02 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8512db29f6abd27987969691ca0de8c6cc141db19a00f2e80bd8996e6cb5de`  
		Last Modified: Thu, 14 Aug 2025 03:26:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:f4b425f37419b579837d2d7857c8ed429c6b2356824bf7c3f83036db9125cc20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f026c9ae0860a234d056b9a6607c5d4673b4e40c52e93c31e76e3cf463fa3c45`

```dockerfile
```

-	Layers:
	-	`sha256:58eba98bd420cdad2a71753e58bb1b1a587f0039d88944045180d74e4c08996c`  
		Last Modified: Thu, 14 Aug 2025 06:34:23 GMT  
		Size: 2.0 MB (2008792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab426c3e7d709a71c837bd5c98de92c219718788268a0700d3c8305f5117b7b8`  
		Last Modified: Thu, 14 Aug 2025 06:34:24 GMT  
		Size: 22.3 KB (22342 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:78a21084b1c4e79dc2fffab373fb465acb723f351bffdc0639a504a5bdc6a2d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32566079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717e9950cc2b302a7f75cdc9919226e0160142934f76014b1a905aa5e39c4046`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d84227403935277ab9817ff62ad9fca6d45f7c109953945d36caa72d73813d0`  
		Last Modified: Wed, 13 Aug 2025 23:02:57 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb0aae300c3cd52b99acd2ae25cb8bf507859ae7b182097672be779a7337fd4`  
		Last Modified: Wed, 13 Aug 2025 23:02:58 GMT  
		Size: 153.4 KB (153369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd2017b19819b1012be52dad0541d85c7797897955d5d0b747b8b86f08da76e`  
		Last Modified: Wed, 13 Aug 2025 23:03:00 GMT  
		Size: 2.3 MB (2275152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad146d7e60bd2063118973d72ff4507de475a826636f2b8fc3bdf36633379d07`  
		Last Modified: Wed, 13 Aug 2025 23:02:59 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fe42a1afd3681fa0efd222132b453c718236f571b4b56018cf362f2333cfb7`  
		Last Modified: Wed, 13 Aug 2025 23:02:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:f34a398dc1f988e0076ebc490e58021e7dc24976392ab10fb871628e11888166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98dee621777b57d248833b652d7622be9c6c901776820489ce629be6f59e5d5f`

```dockerfile
```

-	Layers:
	-	`sha256:4b5fb9727c43d6c906cc0c58b470a99299321ac1e3bcc6a9ea9ec90086d4260d`  
		Last Modified: Thu, 14 Aug 2025 00:34:33 GMT  
		Size: 2.0 MB (2007648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a88652c31f79e7599a31a3fe7d0341deeb4915c7ae0dab214e3c4768ec058300`  
		Last Modified: Thu, 14 Aug 2025 00:34:33 GMT  
		Size: 22.4 KB (22393 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; 386

```console
$ docker pull memcached@sha256:5b9ccecd7eb2ba800cc927d7dfaa5941d25387818d57d8583260ed7d5ea2ef8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33682664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c160d159b0b83b9824df1d8b4cbe201c4c67902d0171a4a03282d3e230939d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:346d0c953bdbc38917a27a6f30726e5b46419d98ecaf4d2d8f201bc3b7025e57`  
		Last Modified: Tue, 12 Aug 2025 20:45:00 GMT  
		Size: 31.3 MB (31289378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1f928fbfcc7da63ca647a381869549b7db17d2971110bc771c27aeed80b33c`  
		Last Modified: Wed, 13 Aug 2025 21:09:56 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49988f067cdbb2558e23451192304fe7f89c2cbe23fcf5463b9e0b80dfbd2a36`  
		Last Modified: Wed, 13 Aug 2025 21:09:56 GMT  
		Size: 147.4 KB (147419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19f3e01a2ee783f4cf292ba84f151492df7a0170128094f4d011075d629af43`  
		Last Modified: Wed, 13 Aug 2025 21:09:56 GMT  
		Size: 2.2 MB (2244354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2288d51449876e6f7fb89b6cac2eda51fef5f03deb3722ef32bf3a9bdc2f5e17`  
		Last Modified: Wed, 13 Aug 2025 21:09:56 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3668cc13fc1544b7319b7b3307e0d74b4e82d36ca065c5a3be7d080267054267`  
		Last Modified: Wed, 13 Aug 2025 21:09:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:df8cca141522937dd5415946521e71f57731ecc574e78d3175b26ce6260dcd46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2026627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff448533f7fe52a0dc6195d7b9320b996bd2623b7c1e7a5b02f7f5cee32b92a4`

```dockerfile
```

-	Layers:
	-	`sha256:80c0a6ea529144e269d6dc30e72d370cfbc53736314c92cca55d737de9562dd6`  
		Last Modified: Wed, 13 Aug 2025 21:34:31 GMT  
		Size: 2.0 MB (2004489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32faf37cac7f889e11009fc41358994c9714a5ebc9aed8843e1fb57a3de6d243`  
		Last Modified: Wed, 13 Aug 2025 21:34:32 GMT  
		Size: 22.1 KB (22138 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:dcc628faf353367b245beec24d23d1b3103986479dff33e10653c5ef2d8b54b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36182904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d113eca2d57658d5e20bd62171298229010cdbce2c33479664dcad6be5ec2acd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26c42ec1bf9e33e4a6a75b57802a57b9d166fccf4b2e5b13cef2b9742fc5025`  
		Last Modified: Thu, 14 Aug 2025 02:32:42 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a82df09860007e05001d706e92e1aa450bfd12fc72a24522ccca5edc6f43cd`  
		Last Modified: Thu, 14 Aug 2025 02:32:42 GMT  
		Size: 170.2 KB (170241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f425e49b56f20bc4209bec20b1ab8671bd728a94104369def1c947c90134052`  
		Last Modified: Thu, 14 Aug 2025 02:32:42 GMT  
		Size: 2.4 MB (2416933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b832c8b1a0256fd9b38e9fd823309571e179c77a2f44d5115f06ae282b7972f`  
		Last Modified: Thu, 14 Aug 2025 02:32:42 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da165b338847a53b7c8a0a0a08c089c86721f3997c5f507291c4737245ade82f`  
		Last Modified: Thu, 14 Aug 2025 02:32:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:d11fb93c72d4e4416799b886acc2230eefbe26e6381d65c674a1a47f310f22ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2154e1260dfec440f34afa1451b8e89c13a23e1eb451b2250766c9c88cf993a`

```dockerfile
```

-	Layers:
	-	`sha256:3c0cb7a63a69d321f183e466c5c0a934dd9a09173b6e174e2f17a9a24e241dee`  
		Last Modified: Thu, 14 Aug 2025 03:34:34 GMT  
		Size: 2.0 MB (2010933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e4dcd6c60091d8eaa78af8659654106ffc91270b3f5b4b6e166f41e295e361f`  
		Last Modified: Thu, 14 Aug 2025 03:34:35 GMT  
		Size: 22.3 KB (22269 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:c7b8d8a8065d2a0ea3bdaaadd564986a39a88ad9d9ef599faf4f923888bb9126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32288745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6fca6b4af0e7ae24559fc296fb0ce831a94645f64b986956f57f9306df1ed22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024aba4218861d2cdfa6f7186fcca6f2f2041ce6c7210cd258e28d55a2c1fa16`  
		Last Modified: Thu, 14 Aug 2025 02:58:06 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2b32b5cc5f77750b103e7bdeb63810088dca53dae4f8b6eed4e17f219a5826`  
		Last Modified: Thu, 14 Aug 2025 02:58:05 GMT  
		Size: 140.4 KB (140388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a046ba92157d2c0b391049e3f702ebcac682b0c6ee6e651f44d940e5d9bd8cd7`  
		Last Modified: Thu, 14 Aug 2025 02:58:07 GMT  
		Size: 2.3 MB (2313787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd7d0eef9a2ce528ea647334f74bfda29496059b15274182ae0d16fb7e5f28d`  
		Last Modified: Thu, 14 Aug 2025 02:58:06 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c5230e4318cec0912586827ea533d6abfaed20ff08b3662b6cf6871a9abae1`  
		Last Modified: Thu, 14 Aug 2025 02:58:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:88badce3b30eeb4fdb00156647e4a3479b0c7cf8dddb286e0bd07105084f4e5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7704cd55751a22fc58eb4a349020abdd760508cd1b9344ccb0df28dc62d35f98`

```dockerfile
```

-	Layers:
	-	`sha256:91e3962d713f291258d33cdc619c48c657c3a72b3a6c808786e3b209389502b2`  
		Last Modified: Thu, 14 Aug 2025 03:34:39 GMT  
		Size: 2.0 MB (2008769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76baa03c0dea63878577ee4ab27db735c1db244cbefee8f9c7b5d5eb4d3887f1`  
		Last Modified: Thu, 14 Aug 2025 03:34:39 GMT  
		Size: 22.2 KB (22196 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.39`

```console
$ docker pull memcached@sha256:c8b53d421310f274ece68507406126575bfc2af3ddc66b72709f81ede5fbe2a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:1.6.39` - linux; amd64

```console
$ docker pull memcached@sha256:489c2e770f5baac8e88e7b0fc7bd9ec7482c560232093860fa776480fd535059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32204915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09da43b5484edc83f2f153e8f750eae1edfc09a59f9c3c8a0d1543ad028f7702`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebfc0a813c97c15541bf6e00db67cec64e96bf712ccfedb445eff79095d78dd6`  
		Last Modified: Wed, 13 Aug 2025 21:21:18 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d44cb640c5a78307f95a5ba37e9b3ff77e080db5144ad044331bdd27e2ac3b8`  
		Last Modified: Wed, 13 Aug 2025 21:21:32 GMT  
		Size: 136.6 KB (136560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c2449a0115fae5ca7c26d3857bdae261f4168d8334ad67cb6c3461a0910fc6`  
		Last Modified: Wed, 13 Aug 2025 21:21:36 GMT  
		Size: 2.3 MB (2293557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9bbdd035dc48ae794ba5af4721f9afdab19142a19ba004aa4b42738ef8758d8`  
		Last Modified: Wed, 13 Aug 2025 21:21:42 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc99f3761e7cd9c6f00023c8aa0d889222b7b233949d24870d0f9b7ad10f58dd`  
		Last Modified: Wed, 13 Aug 2025 21:21:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39` - unknown; unknown

```console
$ docker pull memcached@sha256:98607b9259666dec40f29b040ae0cac2276fac6541257d7f3a4d2fa8d30e3ae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2029528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ad42f4e39d2637475a5aaa10a446b94d8cb9b730bd194a0f995abf19ecba3e7`

```dockerfile
```

-	Layers:
	-	`sha256:249ac3e00cc732e2b029808c9c00d3520da2cdf38b1fc01081a592ea90a5e050`  
		Last Modified: Wed, 13 Aug 2025 21:34:23 GMT  
		Size: 2.0 MB (2007332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fdd95540cec834ae6e6c6bf9ad1d03f83f75af3a4d5bc52a9b7018dd212823a`  
		Last Modified: Wed, 13 Aug 2025 21:34:24 GMT  
		Size: 22.2 KB (22196 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39` - linux; arm variant v5

```console
$ docker pull memcached@sha256:11a993750bd36cfb7d37197d06ccbf217f829c9012146de0d45d0e3494add433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30314569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c2cfe621133fc4a453c7272eacac5ac0ae1cd214c7f7076d785ec3ed0fb6554`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:498399880872f14c562c46bd2a1ef4cfcf3c2a1453514ff0d0f6b7d89f8010dd`  
		Last Modified: Tue, 12 Aug 2025 22:02:01 GMT  
		Size: 27.9 MB (27941706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a99137a20a1adabf0ea411a3bed51f642b1fd51a7c56596ed760ece4727e8c3`  
		Last Modified: Wed, 13 Aug 2025 23:01:56 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7528817abdc345977b6df3988bcacfd622b20f1e6b64e6c01f3c3203275806`  
		Last Modified: Wed, 13 Aug 2025 23:01:57 GMT  
		Size: 144.0 KB (144046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5147466300d5970b08521247c1dcffd9c72644b33c0c4c7a7455293fdaa7514d`  
		Last Modified: Wed, 13 Aug 2025 23:01:58 GMT  
		Size: 2.2 MB (2227304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403dfb443663282b32ef64dddd4d9ece2badd91a91669659aad2213ef1db444c`  
		Last Modified: Wed, 13 Aug 2025 23:00:39 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ac9453a3752c151d9eb3d487d5be8ee9971ce482aa48cbcbffa05e594977ac`  
		Last Modified: Wed, 13 Aug 2025 23:01:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39` - unknown; unknown

```console
$ docker pull memcached@sha256:99d7cc2296b1fdf18d0156098b6c8db466fa371221860e1628d6da1f33862b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe55e32abc4c444556bb77a6cd989bc4c29ae0720781b045162ad41710f332b0`

```dockerfile
```

-	Layers:
	-	`sha256:49bb7a93a18c7972be0483acacb6a99b49edc4bf097a764ed976c48c0516bc14`  
		Last Modified: Thu, 14 Aug 2025 00:34:25 GMT  
		Size: 2.0 MB (2010335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b1896ac27634d50430d62234a56bf5e22627fb59bbe9e2f974832c3f5823cfd`  
		Last Modified: Thu, 14 Aug 2025 00:34:26 GMT  
		Size: 22.3 KB (22343 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39` - linux; arm variant v7

```console
$ docker pull memcached@sha256:4b9bce762cb0cd433a31cf56c571b0a5bb7789813cbb111958bf806cba8b87af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28526851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a10eddf8fe36bdc9bc58ad2f45be5555dd9f6f746d916f9ce491ee5f8239bf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc714abeba0eb64ab96f4d3b22e0750d8fb5ca04c15135a1da25d7f28cb90c8`  
		Last Modified: Thu, 14 Aug 2025 03:26:02 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b548feee9753e7f47e9e09d371fbbc5da58c093655fbe6a70e9e8ce1792c6ddc`  
		Last Modified: Thu, 14 Aug 2025 03:26:02 GMT  
		Size: 135.3 KB (135298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9fd10cb429ca884c5738921b455ecc2d83781179e716d4003166bdc8c44e27`  
		Last Modified: Thu, 14 Aug 2025 03:26:01 GMT  
		Size: 2.2 MB (2182550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59893ea711e5a2631eada91282e598b013d3173b17a0edb0fdbe97d67d122e7`  
		Last Modified: Thu, 14 Aug 2025 03:26:02 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8512db29f6abd27987969691ca0de8c6cc141db19a00f2e80bd8996e6cb5de`  
		Last Modified: Thu, 14 Aug 2025 03:26:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39` - unknown; unknown

```console
$ docker pull memcached@sha256:f4b425f37419b579837d2d7857c8ed429c6b2356824bf7c3f83036db9125cc20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f026c9ae0860a234d056b9a6607c5d4673b4e40c52e93c31e76e3cf463fa3c45`

```dockerfile
```

-	Layers:
	-	`sha256:58eba98bd420cdad2a71753e58bb1b1a587f0039d88944045180d74e4c08996c`  
		Last Modified: Thu, 14 Aug 2025 06:34:23 GMT  
		Size: 2.0 MB (2008792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab426c3e7d709a71c837bd5c98de92c219718788268a0700d3c8305f5117b7b8`  
		Last Modified: Thu, 14 Aug 2025 06:34:24 GMT  
		Size: 22.3 KB (22342 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:78a21084b1c4e79dc2fffab373fb465acb723f351bffdc0639a504a5bdc6a2d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32566079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717e9950cc2b302a7f75cdc9919226e0160142934f76014b1a905aa5e39c4046`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d84227403935277ab9817ff62ad9fca6d45f7c109953945d36caa72d73813d0`  
		Last Modified: Wed, 13 Aug 2025 23:02:57 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb0aae300c3cd52b99acd2ae25cb8bf507859ae7b182097672be779a7337fd4`  
		Last Modified: Wed, 13 Aug 2025 23:02:58 GMT  
		Size: 153.4 KB (153369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd2017b19819b1012be52dad0541d85c7797897955d5d0b747b8b86f08da76e`  
		Last Modified: Wed, 13 Aug 2025 23:03:00 GMT  
		Size: 2.3 MB (2275152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad146d7e60bd2063118973d72ff4507de475a826636f2b8fc3bdf36633379d07`  
		Last Modified: Wed, 13 Aug 2025 23:02:59 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fe42a1afd3681fa0efd222132b453c718236f571b4b56018cf362f2333cfb7`  
		Last Modified: Wed, 13 Aug 2025 23:02:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39` - unknown; unknown

```console
$ docker pull memcached@sha256:f34a398dc1f988e0076ebc490e58021e7dc24976392ab10fb871628e11888166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98dee621777b57d248833b652d7622be9c6c901776820489ce629be6f59e5d5f`

```dockerfile
```

-	Layers:
	-	`sha256:4b5fb9727c43d6c906cc0c58b470a99299321ac1e3bcc6a9ea9ec90086d4260d`  
		Last Modified: Thu, 14 Aug 2025 00:34:33 GMT  
		Size: 2.0 MB (2007648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a88652c31f79e7599a31a3fe7d0341deeb4915c7ae0dab214e3c4768ec058300`  
		Last Modified: Thu, 14 Aug 2025 00:34:33 GMT  
		Size: 22.4 KB (22393 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39` - linux; 386

```console
$ docker pull memcached@sha256:5b9ccecd7eb2ba800cc927d7dfaa5941d25387818d57d8583260ed7d5ea2ef8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33682664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c160d159b0b83b9824df1d8b4cbe201c4c67902d0171a4a03282d3e230939d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:346d0c953bdbc38917a27a6f30726e5b46419d98ecaf4d2d8f201bc3b7025e57`  
		Last Modified: Tue, 12 Aug 2025 20:45:00 GMT  
		Size: 31.3 MB (31289378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1f928fbfcc7da63ca647a381869549b7db17d2971110bc771c27aeed80b33c`  
		Last Modified: Wed, 13 Aug 2025 21:09:56 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49988f067cdbb2558e23451192304fe7f89c2cbe23fcf5463b9e0b80dfbd2a36`  
		Last Modified: Wed, 13 Aug 2025 21:09:56 GMT  
		Size: 147.4 KB (147419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19f3e01a2ee783f4cf292ba84f151492df7a0170128094f4d011075d629af43`  
		Last Modified: Wed, 13 Aug 2025 21:09:56 GMT  
		Size: 2.2 MB (2244354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2288d51449876e6f7fb89b6cac2eda51fef5f03deb3722ef32bf3a9bdc2f5e17`  
		Last Modified: Wed, 13 Aug 2025 21:09:56 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3668cc13fc1544b7319b7b3307e0d74b4e82d36ca065c5a3be7d080267054267`  
		Last Modified: Wed, 13 Aug 2025 21:09:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39` - unknown; unknown

```console
$ docker pull memcached@sha256:df8cca141522937dd5415946521e71f57731ecc574e78d3175b26ce6260dcd46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2026627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff448533f7fe52a0dc6195d7b9320b996bd2623b7c1e7a5b02f7f5cee32b92a4`

```dockerfile
```

-	Layers:
	-	`sha256:80c0a6ea529144e269d6dc30e72d370cfbc53736314c92cca55d737de9562dd6`  
		Last Modified: Wed, 13 Aug 2025 21:34:31 GMT  
		Size: 2.0 MB (2004489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32faf37cac7f889e11009fc41358994c9714a5ebc9aed8843e1fb57a3de6d243`  
		Last Modified: Wed, 13 Aug 2025 21:34:32 GMT  
		Size: 22.1 KB (22138 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39` - linux; ppc64le

```console
$ docker pull memcached@sha256:dcc628faf353367b245beec24d23d1b3103986479dff33e10653c5ef2d8b54b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36182904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d113eca2d57658d5e20bd62171298229010cdbce2c33479664dcad6be5ec2acd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26c42ec1bf9e33e4a6a75b57802a57b9d166fccf4b2e5b13cef2b9742fc5025`  
		Last Modified: Thu, 14 Aug 2025 02:32:42 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a82df09860007e05001d706e92e1aa450bfd12fc72a24522ccca5edc6f43cd`  
		Last Modified: Thu, 14 Aug 2025 02:32:42 GMT  
		Size: 170.2 KB (170241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f425e49b56f20bc4209bec20b1ab8671bd728a94104369def1c947c90134052`  
		Last Modified: Thu, 14 Aug 2025 02:32:42 GMT  
		Size: 2.4 MB (2416933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b832c8b1a0256fd9b38e9fd823309571e179c77a2f44d5115f06ae282b7972f`  
		Last Modified: Thu, 14 Aug 2025 02:32:42 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da165b338847a53b7c8a0a0a08c089c86721f3997c5f507291c4737245ade82f`  
		Last Modified: Thu, 14 Aug 2025 02:32:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39` - unknown; unknown

```console
$ docker pull memcached@sha256:d11fb93c72d4e4416799b886acc2230eefbe26e6381d65c674a1a47f310f22ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2154e1260dfec440f34afa1451b8e89c13a23e1eb451b2250766c9c88cf993a`

```dockerfile
```

-	Layers:
	-	`sha256:3c0cb7a63a69d321f183e466c5c0a934dd9a09173b6e174e2f17a9a24e241dee`  
		Last Modified: Thu, 14 Aug 2025 03:34:34 GMT  
		Size: 2.0 MB (2010933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e4dcd6c60091d8eaa78af8659654106ffc91270b3f5b4b6e166f41e295e361f`  
		Last Modified: Thu, 14 Aug 2025 03:34:35 GMT  
		Size: 22.3 KB (22269 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39` - linux; s390x

```console
$ docker pull memcached@sha256:c7b8d8a8065d2a0ea3bdaaadd564986a39a88ad9d9ef599faf4f923888bb9126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32288745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6fca6b4af0e7ae24559fc296fb0ce831a94645f64b986956f57f9306df1ed22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024aba4218861d2cdfa6f7186fcca6f2f2041ce6c7210cd258e28d55a2c1fa16`  
		Last Modified: Thu, 14 Aug 2025 02:58:06 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2b32b5cc5f77750b103e7bdeb63810088dca53dae4f8b6eed4e17f219a5826`  
		Last Modified: Thu, 14 Aug 2025 02:58:05 GMT  
		Size: 140.4 KB (140388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a046ba92157d2c0b391049e3f702ebcac682b0c6ee6e651f44d940e5d9bd8cd7`  
		Last Modified: Thu, 14 Aug 2025 02:58:07 GMT  
		Size: 2.3 MB (2313787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd7d0eef9a2ce528ea647334f74bfda29496059b15274182ae0d16fb7e5f28d`  
		Last Modified: Thu, 14 Aug 2025 02:58:06 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c5230e4318cec0912586827ea533d6abfaed20ff08b3662b6cf6871a9abae1`  
		Last Modified: Thu, 14 Aug 2025 02:58:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39` - unknown; unknown

```console
$ docker pull memcached@sha256:88badce3b30eeb4fdb00156647e4a3479b0c7cf8dddb286e0bd07105084f4e5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7704cd55751a22fc58eb4a349020abdd760508cd1b9344ccb0df28dc62d35f98`

```dockerfile
```

-	Layers:
	-	`sha256:91e3962d713f291258d33cdc619c48c657c3a72b3a6c808786e3b209389502b2`  
		Last Modified: Thu, 14 Aug 2025 03:34:39 GMT  
		Size: 2.0 MB (2008769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76baa03c0dea63878577ee4ab27db735c1db244cbefee8f9c7b5d5eb4d3887f1`  
		Last Modified: Thu, 14 Aug 2025 03:34:39 GMT  
		Size: 22.2 KB (22196 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.39-alpine`

```console
$ docker pull memcached@sha256:b50070f2faf253d8aacd530742e8e71791a39222c75abcdbcc442dbb7a2f3f25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
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

### `memcached:1.6.39-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:033134f4dd9f45d4e22b6e98b040ea3fccf0dca740af3c949b44bebf458b04d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5904246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca259aa2216a248c482fc8a069d48b1e70b087529d2c3de97154bfa458dbb7a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fb46bc7dee2beda6f5f6f567aecd4d7d7698b9749ed917988a859b7dd96e30`  
		Last Modified: Tue, 29 Jul 2025 16:32:22 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48faf8c85515fb9d17e0752e77d8241f223d53b1adc90439c606d17daabd0ae`  
		Last Modified: Tue, 29 Jul 2025 16:32:24 GMT  
		Size: 104.7 KB (104725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d552a2d777fd444b41cb79438f9f1b441821162e78d73e96dc848a773cf43892`  
		Last Modified: Tue, 29 Jul 2025 16:32:24 GMT  
		Size: 2.0 MB (1998477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c70665f30f3e15975d429b494cb17b21c5d4630c1800cb0addc3fce3a11aa29`  
		Last Modified: Tue, 29 Jul 2025 16:32:20 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ff68520caaf588cec750ad7c403cf55d79eecfff4b7a4ac5eb3910c90c2817`  
		Last Modified: Tue, 29 Jul 2025 16:32:21 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7b27e0df383f45d6d523345a078898524a69cee4d6978cf64bf26532b8679dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 KB (116752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb88e7ee6d3e67b2e4f307c081504a685666917ddf50770fe8beb5abd60a3dc5`

```dockerfile
```

-	Layers:
	-	`sha256:2cf00a09ffccb2c00421311314137de90d0586c126b79dbe5315ce321c168b34`  
		Last Modified: Tue, 29 Jul 2025 18:35:07 GMT  
		Size: 96.2 KB (96180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55325ecc9b276e9c55badf949ed4f06840c34aa8baf0aa6f974e0b90dc5d4e0d`  
		Last Modified: Tue, 29 Jul 2025 18:35:07 GMT  
		Size: 20.6 KB (20572 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:78b59dd3af5a55e950f5106869e642af122a7dc470545f4ba533f6833d83b62c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5550795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb09d5ce1b7010f7a36d77494bc5358d666339628c183692906db6a961373847`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c710b5ddcc2882c5014d0c8cb93aec2bd8b6cc3c59fd42b40c87d94f89a7bc7f`  
		Last Modified: Wed, 23 Jul 2025 22:59:16 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c42040d822a4af7f05f9ccd4d18a7a5e4712b118b7f18d1a7969761029a9d2`  
		Last Modified: Wed, 23 Jul 2025 22:59:16 GMT  
		Size: 101.5 KB (101533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3095e18cd24048696efd57ac64d04dde381a3abde625964e02165c7364eb5633`  
		Last Modified: Tue, 29 Jul 2025 16:50:12 GMT  
		Size: 1.9 MB (1947003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0436ec50f04ed972ff0dd760f7e820f192236e5e720bddb6173f65159c7c36`  
		Last Modified: Tue, 29 Jul 2025 16:50:11 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671c24aae36bb04a32e05bd64e1371384f594889cdbbc41029c916447666d402`  
		Last Modified: Tue, 29 Jul 2025 16:50:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c2a050c6822d834285577c3a001fdfcf9949b7f5a483a4a76a49b549bea19641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54e8bda3e734528caeab4505f084ca7a3076d5ec2273287f66954b5e91af42f`

```dockerfile
```

-	Layers:
	-	`sha256:0d86924831d61ce8b792b25421e9ff0fa2eda9ab940eba5309d44d0eeada7e8e`  
		Last Modified: Tue, 29 Jul 2025 18:35:11 GMT  
		Size: 20.5 KB (20506 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:c9f5db2389b9b0b4a2cd199c4417a9f49a60c42d616e8421177e662d4830de07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9421ed030d4b6b6405714612b8858bda87bc53ac8b0c5ed65c582119527f2d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251060498ca8f0484e20714689b9caba533d09c1b74ed8f2a06780db515a28e2`  
		Last Modified: Thu, 24 Jul 2025 00:27:37 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2293bd2fb47d57e5869c197133067e17f9b1e51ea0f298af1e480e7fd33d681`  
		Last Modified: Thu, 24 Jul 2025 00:27:38 GMT  
		Size: 91.3 KB (91313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ae82f2bac2f7e6fe57f8cb7006fc227c972da1ae5749eba9f5f73e6f3248ec`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 1.9 MB (1905692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e60bf2b2164c620b69e40bdcb64d4104d02eab86c96ea6e170a3601b9ecfd82`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665fe4cd856f1a5c2193568e756c572656949b17c381fc8d43efaa823e18cfa7`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:376a71bc0fef7741e92fdae8b96c825c4622e980de01e724b1a3a0bec3d95f20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 KB (116963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22b574f6c6d021a917c0e99ff4800d8ac3c22fb94b94f88c404cc7609f562fb5`

```dockerfile
```

-	Layers:
	-	`sha256:58ebd4bc7ee5888c552e0fa618f93aefbdb1d15a56ecd3abef19a46ce2f93eee`  
		Last Modified: Tue, 29 Jul 2025 18:35:15 GMT  
		Size: 96.2 KB (96248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d432ed2053ed8249834dd5016fe3199bbc3f82dc7013027c3ead9efe2a007b98`  
		Last Modified: Tue, 29 Jul 2025 18:35:16 GMT  
		Size: 20.7 KB (20715 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b5e4ecc3e927ee30e5cfcfc8aa044960631c75eb8abed9d0fcee6232aa5fdf79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6241700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c880dc2c785861dc9010b813bb6f533f30518443a3bb7e7f477bc96af14582`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbfeb6ac9fd2045c5bea10a301ad554c1f703ffc2885c41520dd5e42eb4a59a`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47acaa5035f94aed634b9d7ecae02fb3838f19e38f8e752ecd6cfba97699b31`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 120.8 KB (120812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8160f3136c6863b52f0dec4f9918b91b8a509700b2071ec0aecd5a6231f00f2a`  
		Last Modified: Tue, 29 Jul 2025 16:41:09 GMT  
		Size: 2.0 MB (1988782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff22f0cad01950efb78a7a862b0becb8b2fd22d795b585f97dad66c091c3dd7`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed19cbfb574c7d8cab364e2ec072c0e03f694468ada41cd70bfcd35392df9e7`  
		Last Modified: Tue, 29 Jul 2025 16:41:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b4c81c7ababb91ecdda3b7d70514d16818602199d759eb2aadd74de732d52960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 KB (117055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80452fd4f79f6e7a0dab0beebf5c144f9df7c257255cdd3cb93ccbff77001fd6`

```dockerfile
```

-	Layers:
	-	`sha256:f11d2a322f6088804ee63ae1a77b9d5ddcdfdc0c65c22e7a70b7ee67cf4532ed`  
		Last Modified: Tue, 29 Jul 2025 18:35:20 GMT  
		Size: 96.3 KB (96284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e225dd6ea14146ddf445598f24189c065ec684fbeb92e7d053a0211a7d60efda`  
		Last Modified: Tue, 29 Jul 2025 18:35:21 GMT  
		Size: 20.8 KB (20771 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine` - linux; 386

```console
$ docker pull memcached@sha256:c58767364161c180098aa6daf4620c8c55ad8713deb64ca620668e7bb829bb41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5683246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac911958149764a83bf951afae4135a482e9064dd0c7dbee61474116cf4bc68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1f621f1e5b25aa798d604ab87259f546a42e522b1311f962484669d45183fa`  
		Last Modified: Tue, 29 Jul 2025 16:32:40 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7cf471d76eab33abc760b1edf151f0e3d4d73732c3f002c74ef629f8ded5f9`  
		Last Modified: Tue, 29 Jul 2025 16:32:39 GMT  
		Size: 109.5 KB (109523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a287f0dc98767a99d5c18925da988244c99243b51f5870a4ed36648b93518402`  
		Last Modified: Tue, 29 Jul 2025 16:32:42 GMT  
		Size: 2.0 MB (1957368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101df272f2e8c1be378c334f0d3d2de9dcd2c58db6fe3580d4451396deef84de`  
		Last Modified: Tue, 29 Jul 2025 16:32:41 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f870cbd8529325263ac998fe634981f154a171a39da706e91a9ea2d91038d361`  
		Last Modified: Tue, 29 Jul 2025 16:32:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:837e0ff5feebc7262c78ddd6b4bece1b5b4c3c22b0eb71b71bf9c6c9d154b416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.7 KB (116651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf22108f9222361c74085ca0633d2876cf3187ccaeb4353499f02fc7a24cc51b`

```dockerfile
```

-	Layers:
	-	`sha256:5143c40f563e8ee15ea82be605c093d36fd7445bcd1cedc45d0754c52b6d3f9d`  
		Last Modified: Tue, 29 Jul 2025 18:35:24 GMT  
		Size: 96.1 KB (96135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fcabff32e4e745d2c95395b620e73b812d1c38929ba82167c1d76583a2f4150`  
		Last Modified: Tue, 29 Jul 2025 18:35:25 GMT  
		Size: 20.5 KB (20516 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:04386ede5dcbf35cabad144bcdc951cc64882f7b9727f2d09927fe0d5551dd19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5942089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8252590eee78d67456ac83fd8279259aaea4d2a555c8bc20b173663fcaa2883`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc22e0cec7e7fe8cff10539bca58363ad6749e2de4f878015c25b5f2b6ecadb9`  
		Last Modified: Tue, 29 Jul 2025 16:33:46 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992ebe18219bd78e59e7e56661aae22f700927f47bc7ad1dfe7717093b371c15`  
		Last Modified: Tue, 29 Jul 2025 16:33:49 GMT  
		Size: 124.3 KB (124315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953f5a37d23881d59809ea64dc6ebf1a152a1ff8929f51befb10577771755f5d`  
		Last Modified: Tue, 29 Jul 2025 16:33:49 GMT  
		Size: 2.1 MB (2089310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b62870a2d7b266495d83cfd72dcf702c91c5c60a7e29836bd9bdac776511a7`  
		Last Modified: Tue, 29 Jul 2025 16:33:47 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1cc8c0fe9a4ef7e2ef70e32ddbfbd2fd68985dd452630a8f390c5b41c654f8`  
		Last Modified: Tue, 29 Jul 2025 16:33:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:cf7e9735e4ef5d00dc25928653b808214f070708e9d879ef54afc4d77ce9db2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcceb455cfdb86bdb0c165af3bc54cbab794d56fef1dbae2b484d28027db791c`

```dockerfile
```

-	Layers:
	-	`sha256:a40704a0afb5cf1b90c0fbdf73c5218a4d8f0e93bb39014507b5fa5f8c7265dd`  
		Last Modified: Tue, 29 Jul 2025 18:35:29 GMT  
		Size: 94.3 KB (94287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da22397f364310e72420738395739c36e25b4e4813bbc5da197582a91bb55ac9`  
		Last Modified: Tue, 29 Jul 2025 18:35:29 GMT  
		Size: 20.6 KB (20648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:d55b98c34ba1c2f546461bd57477d46ab868f9de6b107ffb8f20e06dab1e10d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1034dde2661f43165e85db9a13ff0e10d237d14d4b1b7ee1d4570f19d7df4e69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bbdcecb4dec3cbaba0500f9425897948884cfd8db95ccdf9b824d448b24049`  
		Last Modified: Wed, 23 Jul 2025 23:54:15 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c18051d55886d147cafcee8f9e220087c0b60c0e11ec8898a4005352ee0f7e4`  
		Last Modified: Wed, 23 Jul 2025 23:50:14 GMT  
		Size: 107.9 KB (107902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953c2b44fe537b63907764cf78cbb294c6a1133eacb39c62d35ee5d4914779cb`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 1.9 MB (1932977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d69b2f63abf91684a15b9de7b5e617996762376da3fdda50c4e20c2f1e0f4da`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57c134601fc15e8f2cf183cfd9a3057731ad48b915988217f51df31b5d3cf38`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d50b42de80ef3381b05da20cef4ba6ab4491facb607528e075c034257fe9d327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27766c161110b7e46063a39ce6e176f87233fd6722a825ec338e1568892a77a3`

```dockerfile
```

-	Layers:
	-	`sha256:f933f968a4a14795196607a1337a19431e9f61db78bb49c5c2f89f64a17a1d89`  
		Last Modified: Tue, 29 Jul 2025 18:35:33 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffc41094fe9f57bca69da70bbb18eca52aaf6d27d0fb6d79eda79f9e011a157a`  
		Last Modified: Tue, 29 Jul 2025 18:35:33 GMT  
		Size: 20.6 KB (20647 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:cfd223eb11df3d2297224d458caf974f3f0aae4742ff917812f1b8c84c84e705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5797268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e23f18e891a12e72ef84139504baf8783a7db21d4976fc0b607f8e9bbf736f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00131fb0ca26b15f1ac64b82554fc342b19f8c1ef38312a75addb6686f7bc24`  
		Last Modified: Tue, 29 Jul 2025 16:41:40 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e54da6ab620e035fd78987688d45401e87278ec8a5c02cef8a57e4ea9fd286`  
		Last Modified: Tue, 29 Jul 2025 16:41:42 GMT  
		Size: 113.5 KB (113499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6160f9fac1fd86eda224e9ce4740ea46f7e23dc7edb6d1fe9d830001313e63a`  
		Last Modified: Tue, 29 Jul 2025 16:41:46 GMT  
		Size: 2.0 MB (2037446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d01cd71d33b01b420652f4ad9275f1475f4f0bf253dc0a1b48198df2010be5`  
		Last Modified: Tue, 29 Jul 2025 16:41:52 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831dd5e3c39dd2744dc8823190095f709c36020b55ccdaf85f62a146582c7d9d`  
		Last Modified: Tue, 29 Jul 2025 16:41:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:79f0de7e4dcc9afdbfa1fa22250cf3e544d6f3c33174246b427d2865c7e343d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71dad4d71741d8d354038cb6898389aebb54c956dfcd865d57f78dcc3b238bf8`

```dockerfile
```

-	Layers:
	-	`sha256:f942bbb9520308ae352a056c148fdce8f6b09672c257e0a769aa2504bacf1845`  
		Last Modified: Tue, 29 Jul 2025 18:35:37 GMT  
		Size: 94.2 KB (94229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c46680ef7cf08a43965ab9c7727cc70268ee89e366a1ce1806d0f7980b4ad812`  
		Last Modified: Tue, 29 Jul 2025 18:35:38 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.39-alpine3.22`

```console
$ docker pull memcached@sha256:b50070f2faf253d8aacd530742e8e71791a39222c75abcdbcc442dbb7a2f3f25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
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

### `memcached:1.6.39-alpine3.22` - linux; amd64

```console
$ docker pull memcached@sha256:033134f4dd9f45d4e22b6e98b040ea3fccf0dca740af3c949b44bebf458b04d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5904246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca259aa2216a248c482fc8a069d48b1e70b087529d2c3de97154bfa458dbb7a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fb46bc7dee2beda6f5f6f567aecd4d7d7698b9749ed917988a859b7dd96e30`  
		Last Modified: Tue, 29 Jul 2025 16:32:22 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48faf8c85515fb9d17e0752e77d8241f223d53b1adc90439c606d17daabd0ae`  
		Last Modified: Tue, 29 Jul 2025 16:32:24 GMT  
		Size: 104.7 KB (104725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d552a2d777fd444b41cb79438f9f1b441821162e78d73e96dc848a773cf43892`  
		Last Modified: Tue, 29 Jul 2025 16:32:24 GMT  
		Size: 2.0 MB (1998477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c70665f30f3e15975d429b494cb17b21c5d4630c1800cb0addc3fce3a11aa29`  
		Last Modified: Tue, 29 Jul 2025 16:32:20 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ff68520caaf588cec750ad7c403cf55d79eecfff4b7a4ac5eb3910c90c2817`  
		Last Modified: Tue, 29 Jul 2025 16:32:21 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:7b27e0df383f45d6d523345a078898524a69cee4d6978cf64bf26532b8679dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 KB (116752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb88e7ee6d3e67b2e4f307c081504a685666917ddf50770fe8beb5abd60a3dc5`

```dockerfile
```

-	Layers:
	-	`sha256:2cf00a09ffccb2c00421311314137de90d0586c126b79dbe5315ce321c168b34`  
		Last Modified: Tue, 29 Jul 2025 18:35:07 GMT  
		Size: 96.2 KB (96180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55325ecc9b276e9c55badf949ed4f06840c34aa8baf0aa6f974e0b90dc5d4e0d`  
		Last Modified: Tue, 29 Jul 2025 18:35:07 GMT  
		Size: 20.6 KB (20572 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine3.22` - linux; arm variant v6

```console
$ docker pull memcached@sha256:78b59dd3af5a55e950f5106869e642af122a7dc470545f4ba533f6833d83b62c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5550795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb09d5ce1b7010f7a36d77494bc5358d666339628c183692906db6a961373847`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c710b5ddcc2882c5014d0c8cb93aec2bd8b6cc3c59fd42b40c87d94f89a7bc7f`  
		Last Modified: Wed, 23 Jul 2025 22:59:16 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c42040d822a4af7f05f9ccd4d18a7a5e4712b118b7f18d1a7969761029a9d2`  
		Last Modified: Wed, 23 Jul 2025 22:59:16 GMT  
		Size: 101.5 KB (101533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3095e18cd24048696efd57ac64d04dde381a3abde625964e02165c7364eb5633`  
		Last Modified: Tue, 29 Jul 2025 16:50:12 GMT  
		Size: 1.9 MB (1947003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0436ec50f04ed972ff0dd760f7e820f192236e5e720bddb6173f65159c7c36`  
		Last Modified: Tue, 29 Jul 2025 16:50:11 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671c24aae36bb04a32e05bd64e1371384f594889cdbbc41029c916447666d402`  
		Last Modified: Tue, 29 Jul 2025 16:50:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:c2a050c6822d834285577c3a001fdfcf9949b7f5a483a4a76a49b549bea19641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54e8bda3e734528caeab4505f084ca7a3076d5ec2273287f66954b5e91af42f`

```dockerfile
```

-	Layers:
	-	`sha256:0d86924831d61ce8b792b25421e9ff0fa2eda9ab940eba5309d44d0eeada7e8e`  
		Last Modified: Tue, 29 Jul 2025 18:35:11 GMT  
		Size: 20.5 KB (20506 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine3.22` - linux; arm variant v7

```console
$ docker pull memcached@sha256:c9f5db2389b9b0b4a2cd199c4417a9f49a60c42d616e8421177e662d4830de07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9421ed030d4b6b6405714612b8858bda87bc53ac8b0c5ed65c582119527f2d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251060498ca8f0484e20714689b9caba533d09c1b74ed8f2a06780db515a28e2`  
		Last Modified: Thu, 24 Jul 2025 00:27:37 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2293bd2fb47d57e5869c197133067e17f9b1e51ea0f298af1e480e7fd33d681`  
		Last Modified: Thu, 24 Jul 2025 00:27:38 GMT  
		Size: 91.3 KB (91313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ae82f2bac2f7e6fe57f8cb7006fc227c972da1ae5749eba9f5f73e6f3248ec`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 1.9 MB (1905692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e60bf2b2164c620b69e40bdcb64d4104d02eab86c96ea6e170a3601b9ecfd82`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665fe4cd856f1a5c2193568e756c572656949b17c381fc8d43efaa823e18cfa7`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:376a71bc0fef7741e92fdae8b96c825c4622e980de01e724b1a3a0bec3d95f20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 KB (116963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22b574f6c6d021a917c0e99ff4800d8ac3c22fb94b94f88c404cc7609f562fb5`

```dockerfile
```

-	Layers:
	-	`sha256:58ebd4bc7ee5888c552e0fa618f93aefbdb1d15a56ecd3abef19a46ce2f93eee`  
		Last Modified: Tue, 29 Jul 2025 18:35:15 GMT  
		Size: 96.2 KB (96248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d432ed2053ed8249834dd5016fe3199bbc3f82dc7013027c3ead9efe2a007b98`  
		Last Modified: Tue, 29 Jul 2025 18:35:16 GMT  
		Size: 20.7 KB (20715 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b5e4ecc3e927ee30e5cfcfc8aa044960631c75eb8abed9d0fcee6232aa5fdf79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6241700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c880dc2c785861dc9010b813bb6f533f30518443a3bb7e7f477bc96af14582`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbfeb6ac9fd2045c5bea10a301ad554c1f703ffc2885c41520dd5e42eb4a59a`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47acaa5035f94aed634b9d7ecae02fb3838f19e38f8e752ecd6cfba97699b31`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 120.8 KB (120812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8160f3136c6863b52f0dec4f9918b91b8a509700b2071ec0aecd5a6231f00f2a`  
		Last Modified: Tue, 29 Jul 2025 16:41:09 GMT  
		Size: 2.0 MB (1988782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff22f0cad01950efb78a7a862b0becb8b2fd22d795b585f97dad66c091c3dd7`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed19cbfb574c7d8cab364e2ec072c0e03f694468ada41cd70bfcd35392df9e7`  
		Last Modified: Tue, 29 Jul 2025 16:41:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:b4c81c7ababb91ecdda3b7d70514d16818602199d759eb2aadd74de732d52960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 KB (117055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80452fd4f79f6e7a0dab0beebf5c144f9df7c257255cdd3cb93ccbff77001fd6`

```dockerfile
```

-	Layers:
	-	`sha256:f11d2a322f6088804ee63ae1a77b9d5ddcdfdc0c65c22e7a70b7ee67cf4532ed`  
		Last Modified: Tue, 29 Jul 2025 18:35:20 GMT  
		Size: 96.3 KB (96284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e225dd6ea14146ddf445598f24189c065ec684fbeb92e7d053a0211a7d60efda`  
		Last Modified: Tue, 29 Jul 2025 18:35:21 GMT  
		Size: 20.8 KB (20771 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine3.22` - linux; 386

```console
$ docker pull memcached@sha256:c58767364161c180098aa6daf4620c8c55ad8713deb64ca620668e7bb829bb41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5683246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac911958149764a83bf951afae4135a482e9064dd0c7dbee61474116cf4bc68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1f621f1e5b25aa798d604ab87259f546a42e522b1311f962484669d45183fa`  
		Last Modified: Tue, 29 Jul 2025 16:32:40 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7cf471d76eab33abc760b1edf151f0e3d4d73732c3f002c74ef629f8ded5f9`  
		Last Modified: Tue, 29 Jul 2025 16:32:39 GMT  
		Size: 109.5 KB (109523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a287f0dc98767a99d5c18925da988244c99243b51f5870a4ed36648b93518402`  
		Last Modified: Tue, 29 Jul 2025 16:32:42 GMT  
		Size: 2.0 MB (1957368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101df272f2e8c1be378c334f0d3d2de9dcd2c58db6fe3580d4451396deef84de`  
		Last Modified: Tue, 29 Jul 2025 16:32:41 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f870cbd8529325263ac998fe634981f154a171a39da706e91a9ea2d91038d361`  
		Last Modified: Tue, 29 Jul 2025 16:32:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:837e0ff5feebc7262c78ddd6b4bece1b5b4c3c22b0eb71b71bf9c6c9d154b416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.7 KB (116651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf22108f9222361c74085ca0633d2876cf3187ccaeb4353499f02fc7a24cc51b`

```dockerfile
```

-	Layers:
	-	`sha256:5143c40f563e8ee15ea82be605c093d36fd7445bcd1cedc45d0754c52b6d3f9d`  
		Last Modified: Tue, 29 Jul 2025 18:35:24 GMT  
		Size: 96.1 KB (96135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fcabff32e4e745d2c95395b620e73b812d1c38929ba82167c1d76583a2f4150`  
		Last Modified: Tue, 29 Jul 2025 18:35:25 GMT  
		Size: 20.5 KB (20516 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine3.22` - linux; ppc64le

```console
$ docker pull memcached@sha256:04386ede5dcbf35cabad144bcdc951cc64882f7b9727f2d09927fe0d5551dd19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5942089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8252590eee78d67456ac83fd8279259aaea4d2a555c8bc20b173663fcaa2883`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc22e0cec7e7fe8cff10539bca58363ad6749e2de4f878015c25b5f2b6ecadb9`  
		Last Modified: Tue, 29 Jul 2025 16:33:46 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992ebe18219bd78e59e7e56661aae22f700927f47bc7ad1dfe7717093b371c15`  
		Last Modified: Tue, 29 Jul 2025 16:33:49 GMT  
		Size: 124.3 KB (124315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953f5a37d23881d59809ea64dc6ebf1a152a1ff8929f51befb10577771755f5d`  
		Last Modified: Tue, 29 Jul 2025 16:33:49 GMT  
		Size: 2.1 MB (2089310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b62870a2d7b266495d83cfd72dcf702c91c5c60a7e29836bd9bdac776511a7`  
		Last Modified: Tue, 29 Jul 2025 16:33:47 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1cc8c0fe9a4ef7e2ef70e32ddbfbd2fd68985dd452630a8f390c5b41c654f8`  
		Last Modified: Tue, 29 Jul 2025 16:33:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:cf7e9735e4ef5d00dc25928653b808214f070708e9d879ef54afc4d77ce9db2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcceb455cfdb86bdb0c165af3bc54cbab794d56fef1dbae2b484d28027db791c`

```dockerfile
```

-	Layers:
	-	`sha256:a40704a0afb5cf1b90c0fbdf73c5218a4d8f0e93bb39014507b5fa5f8c7265dd`  
		Last Modified: Tue, 29 Jul 2025 18:35:29 GMT  
		Size: 94.3 KB (94287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da22397f364310e72420738395739c36e25b4e4813bbc5da197582a91bb55ac9`  
		Last Modified: Tue, 29 Jul 2025 18:35:29 GMT  
		Size: 20.6 KB (20648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine3.22` - linux; riscv64

```console
$ docker pull memcached@sha256:d55b98c34ba1c2f546461bd57477d46ab868f9de6b107ffb8f20e06dab1e10d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1034dde2661f43165e85db9a13ff0e10d237d14d4b1b7ee1d4570f19d7df4e69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bbdcecb4dec3cbaba0500f9425897948884cfd8db95ccdf9b824d448b24049`  
		Last Modified: Wed, 23 Jul 2025 23:54:15 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c18051d55886d147cafcee8f9e220087c0b60c0e11ec8898a4005352ee0f7e4`  
		Last Modified: Wed, 23 Jul 2025 23:50:14 GMT  
		Size: 107.9 KB (107902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953c2b44fe537b63907764cf78cbb294c6a1133eacb39c62d35ee5d4914779cb`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 1.9 MB (1932977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d69b2f63abf91684a15b9de7b5e617996762376da3fdda50c4e20c2f1e0f4da`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57c134601fc15e8f2cf183cfd9a3057731ad48b915988217f51df31b5d3cf38`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:d50b42de80ef3381b05da20cef4ba6ab4491facb607528e075c034257fe9d327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27766c161110b7e46063a39ce6e176f87233fd6722a825ec338e1568892a77a3`

```dockerfile
```

-	Layers:
	-	`sha256:f933f968a4a14795196607a1337a19431e9f61db78bb49c5c2f89f64a17a1d89`  
		Last Modified: Tue, 29 Jul 2025 18:35:33 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffc41094fe9f57bca69da70bbb18eca52aaf6d27d0fb6d79eda79f9e011a157a`  
		Last Modified: Tue, 29 Jul 2025 18:35:33 GMT  
		Size: 20.6 KB (20647 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine3.22` - linux; s390x

```console
$ docker pull memcached@sha256:cfd223eb11df3d2297224d458caf974f3f0aae4742ff917812f1b8c84c84e705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5797268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e23f18e891a12e72ef84139504baf8783a7db21d4976fc0b607f8e9bbf736f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00131fb0ca26b15f1ac64b82554fc342b19f8c1ef38312a75addb6686f7bc24`  
		Last Modified: Tue, 29 Jul 2025 16:41:40 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e54da6ab620e035fd78987688d45401e87278ec8a5c02cef8a57e4ea9fd286`  
		Last Modified: Tue, 29 Jul 2025 16:41:42 GMT  
		Size: 113.5 KB (113499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6160f9fac1fd86eda224e9ce4740ea46f7e23dc7edb6d1fe9d830001313e63a`  
		Last Modified: Tue, 29 Jul 2025 16:41:46 GMT  
		Size: 2.0 MB (2037446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d01cd71d33b01b420652f4ad9275f1475f4f0bf253dc0a1b48198df2010be5`  
		Last Modified: Tue, 29 Jul 2025 16:41:52 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831dd5e3c39dd2744dc8823190095f709c36020b55ccdaf85f62a146582c7d9d`  
		Last Modified: Tue, 29 Jul 2025 16:41:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:79f0de7e4dcc9afdbfa1fa22250cf3e544d6f3c33174246b427d2865c7e343d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71dad4d71741d8d354038cb6898389aebb54c956dfcd865d57f78dcc3b238bf8`

```dockerfile
```

-	Layers:
	-	`sha256:f942bbb9520308ae352a056c148fdce8f6b09672c257e0a769aa2504bacf1845`  
		Last Modified: Tue, 29 Jul 2025 18:35:37 GMT  
		Size: 94.2 KB (94229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c46680ef7cf08a43965ab9c7727cc70268ee89e366a1ce1806d0f7980b4ad812`  
		Last Modified: Tue, 29 Jul 2025 18:35:38 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.39-trixie`

```console
$ docker pull memcached@sha256:c8b53d421310f274ece68507406126575bfc2af3ddc66b72709f81ede5fbe2a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:1.6.39-trixie` - linux; amd64

```console
$ docker pull memcached@sha256:489c2e770f5baac8e88e7b0fc7bd9ec7482c560232093860fa776480fd535059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32204915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09da43b5484edc83f2f153e8f750eae1edfc09a59f9c3c8a0d1543ad028f7702`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebfc0a813c97c15541bf6e00db67cec64e96bf712ccfedb445eff79095d78dd6`  
		Last Modified: Wed, 13 Aug 2025 21:21:18 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d44cb640c5a78307f95a5ba37e9b3ff77e080db5144ad044331bdd27e2ac3b8`  
		Last Modified: Wed, 13 Aug 2025 21:21:32 GMT  
		Size: 136.6 KB (136560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c2449a0115fae5ca7c26d3857bdae261f4168d8334ad67cb6c3461a0910fc6`  
		Last Modified: Wed, 13 Aug 2025 21:21:36 GMT  
		Size: 2.3 MB (2293557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9bbdd035dc48ae794ba5af4721f9afdab19142a19ba004aa4b42738ef8758d8`  
		Last Modified: Wed, 13 Aug 2025 21:21:42 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc99f3761e7cd9c6f00023c8aa0d889222b7b233949d24870d0f9b7ad10f58dd`  
		Last Modified: Wed, 13 Aug 2025 21:21:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:98607b9259666dec40f29b040ae0cac2276fac6541257d7f3a4d2fa8d30e3ae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2029528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ad42f4e39d2637475a5aaa10a446b94d8cb9b730bd194a0f995abf19ecba3e7`

```dockerfile
```

-	Layers:
	-	`sha256:249ac3e00cc732e2b029808c9c00d3520da2cdf38b1fc01081a592ea90a5e050`  
		Last Modified: Wed, 13 Aug 2025 21:34:23 GMT  
		Size: 2.0 MB (2007332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fdd95540cec834ae6e6c6bf9ad1d03f83f75af3a4d5bc52a9b7018dd212823a`  
		Last Modified: Wed, 13 Aug 2025 21:34:24 GMT  
		Size: 22.2 KB (22196 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:11a993750bd36cfb7d37197d06ccbf217f829c9012146de0d45d0e3494add433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30314569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c2cfe621133fc4a453c7272eacac5ac0ae1cd214c7f7076d785ec3ed0fb6554`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:498399880872f14c562c46bd2a1ef4cfcf3c2a1453514ff0d0f6b7d89f8010dd`  
		Last Modified: Tue, 12 Aug 2025 22:02:01 GMT  
		Size: 27.9 MB (27941706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a99137a20a1adabf0ea411a3bed51f642b1fd51a7c56596ed760ece4727e8c3`  
		Last Modified: Wed, 13 Aug 2025 23:01:56 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7528817abdc345977b6df3988bcacfd622b20f1e6b64e6c01f3c3203275806`  
		Last Modified: Wed, 13 Aug 2025 23:01:57 GMT  
		Size: 144.0 KB (144046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5147466300d5970b08521247c1dcffd9c72644b33c0c4c7a7455293fdaa7514d`  
		Last Modified: Wed, 13 Aug 2025 23:01:58 GMT  
		Size: 2.2 MB (2227304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403dfb443663282b32ef64dddd4d9ece2badd91a91669659aad2213ef1db444c`  
		Last Modified: Wed, 13 Aug 2025 23:00:39 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ac9453a3752c151d9eb3d487d5be8ee9971ce482aa48cbcbffa05e594977ac`  
		Last Modified: Wed, 13 Aug 2025 23:01:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:99d7cc2296b1fdf18d0156098b6c8db466fa371221860e1628d6da1f33862b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe55e32abc4c444556bb77a6cd989bc4c29ae0720781b045162ad41710f332b0`

```dockerfile
```

-	Layers:
	-	`sha256:49bb7a93a18c7972be0483acacb6a99b49edc4bf097a764ed976c48c0516bc14`  
		Last Modified: Thu, 14 Aug 2025 00:34:25 GMT  
		Size: 2.0 MB (2010335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b1896ac27634d50430d62234a56bf5e22627fb59bbe9e2f974832c3f5823cfd`  
		Last Modified: Thu, 14 Aug 2025 00:34:26 GMT  
		Size: 22.3 KB (22343 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:4b9bce762cb0cd433a31cf56c571b0a5bb7789813cbb111958bf806cba8b87af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28526851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a10eddf8fe36bdc9bc58ad2f45be5555dd9f6f746d916f9ce491ee5f8239bf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc714abeba0eb64ab96f4d3b22e0750d8fb5ca04c15135a1da25d7f28cb90c8`  
		Last Modified: Thu, 14 Aug 2025 03:26:02 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b548feee9753e7f47e9e09d371fbbc5da58c093655fbe6a70e9e8ce1792c6ddc`  
		Last Modified: Thu, 14 Aug 2025 03:26:02 GMT  
		Size: 135.3 KB (135298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9fd10cb429ca884c5738921b455ecc2d83781179e716d4003166bdc8c44e27`  
		Last Modified: Thu, 14 Aug 2025 03:26:01 GMT  
		Size: 2.2 MB (2182550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59893ea711e5a2631eada91282e598b013d3173b17a0edb0fdbe97d67d122e7`  
		Last Modified: Thu, 14 Aug 2025 03:26:02 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8512db29f6abd27987969691ca0de8c6cc141db19a00f2e80bd8996e6cb5de`  
		Last Modified: Thu, 14 Aug 2025 03:26:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:f4b425f37419b579837d2d7857c8ed429c6b2356824bf7c3f83036db9125cc20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f026c9ae0860a234d056b9a6607c5d4673b4e40c52e93c31e76e3cf463fa3c45`

```dockerfile
```

-	Layers:
	-	`sha256:58eba98bd420cdad2a71753e58bb1b1a587f0039d88944045180d74e4c08996c`  
		Last Modified: Thu, 14 Aug 2025 06:34:23 GMT  
		Size: 2.0 MB (2008792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab426c3e7d709a71c837bd5c98de92c219718788268a0700d3c8305f5117b7b8`  
		Last Modified: Thu, 14 Aug 2025 06:34:24 GMT  
		Size: 22.3 KB (22342 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:78a21084b1c4e79dc2fffab373fb465acb723f351bffdc0639a504a5bdc6a2d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32566079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717e9950cc2b302a7f75cdc9919226e0160142934f76014b1a905aa5e39c4046`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d84227403935277ab9817ff62ad9fca6d45f7c109953945d36caa72d73813d0`  
		Last Modified: Wed, 13 Aug 2025 23:02:57 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb0aae300c3cd52b99acd2ae25cb8bf507859ae7b182097672be779a7337fd4`  
		Last Modified: Wed, 13 Aug 2025 23:02:58 GMT  
		Size: 153.4 KB (153369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd2017b19819b1012be52dad0541d85c7797897955d5d0b747b8b86f08da76e`  
		Last Modified: Wed, 13 Aug 2025 23:03:00 GMT  
		Size: 2.3 MB (2275152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad146d7e60bd2063118973d72ff4507de475a826636f2b8fc3bdf36633379d07`  
		Last Modified: Wed, 13 Aug 2025 23:02:59 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fe42a1afd3681fa0efd222132b453c718236f571b4b56018cf362f2333cfb7`  
		Last Modified: Wed, 13 Aug 2025 23:02:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:f34a398dc1f988e0076ebc490e58021e7dc24976392ab10fb871628e11888166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98dee621777b57d248833b652d7622be9c6c901776820489ce629be6f59e5d5f`

```dockerfile
```

-	Layers:
	-	`sha256:4b5fb9727c43d6c906cc0c58b470a99299321ac1e3bcc6a9ea9ec90086d4260d`  
		Last Modified: Thu, 14 Aug 2025 00:34:33 GMT  
		Size: 2.0 MB (2007648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a88652c31f79e7599a31a3fe7d0341deeb4915c7ae0dab214e3c4768ec058300`  
		Last Modified: Thu, 14 Aug 2025 00:34:33 GMT  
		Size: 22.4 KB (22393 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-trixie` - linux; 386

```console
$ docker pull memcached@sha256:5b9ccecd7eb2ba800cc927d7dfaa5941d25387818d57d8583260ed7d5ea2ef8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33682664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c160d159b0b83b9824df1d8b4cbe201c4c67902d0171a4a03282d3e230939d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:346d0c953bdbc38917a27a6f30726e5b46419d98ecaf4d2d8f201bc3b7025e57`  
		Last Modified: Tue, 12 Aug 2025 20:45:00 GMT  
		Size: 31.3 MB (31289378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1f928fbfcc7da63ca647a381869549b7db17d2971110bc771c27aeed80b33c`  
		Last Modified: Wed, 13 Aug 2025 21:09:56 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49988f067cdbb2558e23451192304fe7f89c2cbe23fcf5463b9e0b80dfbd2a36`  
		Last Modified: Wed, 13 Aug 2025 21:09:56 GMT  
		Size: 147.4 KB (147419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19f3e01a2ee783f4cf292ba84f151492df7a0170128094f4d011075d629af43`  
		Last Modified: Wed, 13 Aug 2025 21:09:56 GMT  
		Size: 2.2 MB (2244354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2288d51449876e6f7fb89b6cac2eda51fef5f03deb3722ef32bf3a9bdc2f5e17`  
		Last Modified: Wed, 13 Aug 2025 21:09:56 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3668cc13fc1544b7319b7b3307e0d74b4e82d36ca065c5a3be7d080267054267`  
		Last Modified: Wed, 13 Aug 2025 21:09:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:df8cca141522937dd5415946521e71f57731ecc574e78d3175b26ce6260dcd46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2026627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff448533f7fe52a0dc6195d7b9320b996bd2623b7c1e7a5b02f7f5cee32b92a4`

```dockerfile
```

-	Layers:
	-	`sha256:80c0a6ea529144e269d6dc30e72d370cfbc53736314c92cca55d737de9562dd6`  
		Last Modified: Wed, 13 Aug 2025 21:34:31 GMT  
		Size: 2.0 MB (2004489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32faf37cac7f889e11009fc41358994c9714a5ebc9aed8843e1fb57a3de6d243`  
		Last Modified: Wed, 13 Aug 2025 21:34:32 GMT  
		Size: 22.1 KB (22138 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:dcc628faf353367b245beec24d23d1b3103986479dff33e10653c5ef2d8b54b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36182904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d113eca2d57658d5e20bd62171298229010cdbce2c33479664dcad6be5ec2acd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26c42ec1bf9e33e4a6a75b57802a57b9d166fccf4b2e5b13cef2b9742fc5025`  
		Last Modified: Thu, 14 Aug 2025 02:32:42 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a82df09860007e05001d706e92e1aa450bfd12fc72a24522ccca5edc6f43cd`  
		Last Modified: Thu, 14 Aug 2025 02:32:42 GMT  
		Size: 170.2 KB (170241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f425e49b56f20bc4209bec20b1ab8671bd728a94104369def1c947c90134052`  
		Last Modified: Thu, 14 Aug 2025 02:32:42 GMT  
		Size: 2.4 MB (2416933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b832c8b1a0256fd9b38e9fd823309571e179c77a2f44d5115f06ae282b7972f`  
		Last Modified: Thu, 14 Aug 2025 02:32:42 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da165b338847a53b7c8a0a0a08c089c86721f3997c5f507291c4737245ade82f`  
		Last Modified: Thu, 14 Aug 2025 02:32:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:d11fb93c72d4e4416799b886acc2230eefbe26e6381d65c674a1a47f310f22ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2154e1260dfec440f34afa1451b8e89c13a23e1eb451b2250766c9c88cf993a`

```dockerfile
```

-	Layers:
	-	`sha256:3c0cb7a63a69d321f183e466c5c0a934dd9a09173b6e174e2f17a9a24e241dee`  
		Last Modified: Thu, 14 Aug 2025 03:34:34 GMT  
		Size: 2.0 MB (2010933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e4dcd6c60091d8eaa78af8659654106ffc91270b3f5b4b6e166f41e295e361f`  
		Last Modified: Thu, 14 Aug 2025 03:34:35 GMT  
		Size: 22.3 KB (22269 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:c7b8d8a8065d2a0ea3bdaaadd564986a39a88ad9d9ef599faf4f923888bb9126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32288745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6fca6b4af0e7ae24559fc296fb0ce831a94645f64b986956f57f9306df1ed22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024aba4218861d2cdfa6f7186fcca6f2f2041ce6c7210cd258e28d55a2c1fa16`  
		Last Modified: Thu, 14 Aug 2025 02:58:06 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2b32b5cc5f77750b103e7bdeb63810088dca53dae4f8b6eed4e17f219a5826`  
		Last Modified: Thu, 14 Aug 2025 02:58:05 GMT  
		Size: 140.4 KB (140388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a046ba92157d2c0b391049e3f702ebcac682b0c6ee6e651f44d940e5d9bd8cd7`  
		Last Modified: Thu, 14 Aug 2025 02:58:07 GMT  
		Size: 2.3 MB (2313787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd7d0eef9a2ce528ea647334f74bfda29496059b15274182ae0d16fb7e5f28d`  
		Last Modified: Thu, 14 Aug 2025 02:58:06 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c5230e4318cec0912586827ea533d6abfaed20ff08b3662b6cf6871a9abae1`  
		Last Modified: Thu, 14 Aug 2025 02:58:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:88badce3b30eeb4fdb00156647e4a3479b0c7cf8dddb286e0bd07105084f4e5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7704cd55751a22fc58eb4a349020abdd760508cd1b9344ccb0df28dc62d35f98`

```dockerfile
```

-	Layers:
	-	`sha256:91e3962d713f291258d33cdc619c48c657c3a72b3a6c808786e3b209389502b2`  
		Last Modified: Thu, 14 Aug 2025 03:34:39 GMT  
		Size: 2.0 MB (2008769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76baa03c0dea63878577ee4ab27db735c1db244cbefee8f9c7b5d5eb4d3887f1`  
		Last Modified: Thu, 14 Aug 2025 03:34:39 GMT  
		Size: 22.2 KB (22196 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine`

```console
$ docker pull memcached@sha256:b50070f2faf253d8aacd530742e8e71791a39222c75abcdbcc442dbb7a2f3f25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
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
$ docker pull memcached@sha256:033134f4dd9f45d4e22b6e98b040ea3fccf0dca740af3c949b44bebf458b04d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5904246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca259aa2216a248c482fc8a069d48b1e70b087529d2c3de97154bfa458dbb7a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fb46bc7dee2beda6f5f6f567aecd4d7d7698b9749ed917988a859b7dd96e30`  
		Last Modified: Tue, 29 Jul 2025 16:32:22 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48faf8c85515fb9d17e0752e77d8241f223d53b1adc90439c606d17daabd0ae`  
		Last Modified: Tue, 29 Jul 2025 16:32:24 GMT  
		Size: 104.7 KB (104725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d552a2d777fd444b41cb79438f9f1b441821162e78d73e96dc848a773cf43892`  
		Last Modified: Tue, 29 Jul 2025 16:32:24 GMT  
		Size: 2.0 MB (1998477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c70665f30f3e15975d429b494cb17b21c5d4630c1800cb0addc3fce3a11aa29`  
		Last Modified: Tue, 29 Jul 2025 16:32:20 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ff68520caaf588cec750ad7c403cf55d79eecfff4b7a4ac5eb3910c90c2817`  
		Last Modified: Tue, 29 Jul 2025 16:32:21 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7b27e0df383f45d6d523345a078898524a69cee4d6978cf64bf26532b8679dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 KB (116752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb88e7ee6d3e67b2e4f307c081504a685666917ddf50770fe8beb5abd60a3dc5`

```dockerfile
```

-	Layers:
	-	`sha256:2cf00a09ffccb2c00421311314137de90d0586c126b79dbe5315ce321c168b34`  
		Last Modified: Tue, 29 Jul 2025 18:35:07 GMT  
		Size: 96.2 KB (96180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55325ecc9b276e9c55badf949ed4f06840c34aa8baf0aa6f974e0b90dc5d4e0d`  
		Last Modified: Tue, 29 Jul 2025 18:35:07 GMT  
		Size: 20.6 KB (20572 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:78b59dd3af5a55e950f5106869e642af122a7dc470545f4ba533f6833d83b62c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5550795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb09d5ce1b7010f7a36d77494bc5358d666339628c183692906db6a961373847`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c710b5ddcc2882c5014d0c8cb93aec2bd8b6cc3c59fd42b40c87d94f89a7bc7f`  
		Last Modified: Wed, 23 Jul 2025 22:59:16 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c42040d822a4af7f05f9ccd4d18a7a5e4712b118b7f18d1a7969761029a9d2`  
		Last Modified: Wed, 23 Jul 2025 22:59:16 GMT  
		Size: 101.5 KB (101533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3095e18cd24048696efd57ac64d04dde381a3abde625964e02165c7364eb5633`  
		Last Modified: Tue, 29 Jul 2025 16:50:12 GMT  
		Size: 1.9 MB (1947003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0436ec50f04ed972ff0dd760f7e820f192236e5e720bddb6173f65159c7c36`  
		Last Modified: Tue, 29 Jul 2025 16:50:11 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671c24aae36bb04a32e05bd64e1371384f594889cdbbc41029c916447666d402`  
		Last Modified: Tue, 29 Jul 2025 16:50:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c2a050c6822d834285577c3a001fdfcf9949b7f5a483a4a76a49b549bea19641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54e8bda3e734528caeab4505f084ca7a3076d5ec2273287f66954b5e91af42f`

```dockerfile
```

-	Layers:
	-	`sha256:0d86924831d61ce8b792b25421e9ff0fa2eda9ab940eba5309d44d0eeada7e8e`  
		Last Modified: Tue, 29 Jul 2025 18:35:11 GMT  
		Size: 20.5 KB (20506 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:c9f5db2389b9b0b4a2cd199c4417a9f49a60c42d616e8421177e662d4830de07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9421ed030d4b6b6405714612b8858bda87bc53ac8b0c5ed65c582119527f2d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251060498ca8f0484e20714689b9caba533d09c1b74ed8f2a06780db515a28e2`  
		Last Modified: Thu, 24 Jul 2025 00:27:37 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2293bd2fb47d57e5869c197133067e17f9b1e51ea0f298af1e480e7fd33d681`  
		Last Modified: Thu, 24 Jul 2025 00:27:38 GMT  
		Size: 91.3 KB (91313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ae82f2bac2f7e6fe57f8cb7006fc227c972da1ae5749eba9f5f73e6f3248ec`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 1.9 MB (1905692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e60bf2b2164c620b69e40bdcb64d4104d02eab86c96ea6e170a3601b9ecfd82`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665fe4cd856f1a5c2193568e756c572656949b17c381fc8d43efaa823e18cfa7`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:376a71bc0fef7741e92fdae8b96c825c4622e980de01e724b1a3a0bec3d95f20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 KB (116963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22b574f6c6d021a917c0e99ff4800d8ac3c22fb94b94f88c404cc7609f562fb5`

```dockerfile
```

-	Layers:
	-	`sha256:58ebd4bc7ee5888c552e0fa618f93aefbdb1d15a56ecd3abef19a46ce2f93eee`  
		Last Modified: Tue, 29 Jul 2025 18:35:15 GMT  
		Size: 96.2 KB (96248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d432ed2053ed8249834dd5016fe3199bbc3f82dc7013027c3ead9efe2a007b98`  
		Last Modified: Tue, 29 Jul 2025 18:35:16 GMT  
		Size: 20.7 KB (20715 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b5e4ecc3e927ee30e5cfcfc8aa044960631c75eb8abed9d0fcee6232aa5fdf79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6241700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c880dc2c785861dc9010b813bb6f533f30518443a3bb7e7f477bc96af14582`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbfeb6ac9fd2045c5bea10a301ad554c1f703ffc2885c41520dd5e42eb4a59a`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47acaa5035f94aed634b9d7ecae02fb3838f19e38f8e752ecd6cfba97699b31`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 120.8 KB (120812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8160f3136c6863b52f0dec4f9918b91b8a509700b2071ec0aecd5a6231f00f2a`  
		Last Modified: Tue, 29 Jul 2025 16:41:09 GMT  
		Size: 2.0 MB (1988782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff22f0cad01950efb78a7a862b0becb8b2fd22d795b585f97dad66c091c3dd7`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed19cbfb574c7d8cab364e2ec072c0e03f694468ada41cd70bfcd35392df9e7`  
		Last Modified: Tue, 29 Jul 2025 16:41:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b4c81c7ababb91ecdda3b7d70514d16818602199d759eb2aadd74de732d52960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 KB (117055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80452fd4f79f6e7a0dab0beebf5c144f9df7c257255cdd3cb93ccbff77001fd6`

```dockerfile
```

-	Layers:
	-	`sha256:f11d2a322f6088804ee63ae1a77b9d5ddcdfdc0c65c22e7a70b7ee67cf4532ed`  
		Last Modified: Tue, 29 Jul 2025 18:35:20 GMT  
		Size: 96.3 KB (96284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e225dd6ea14146ddf445598f24189c065ec684fbeb92e7d053a0211a7d60efda`  
		Last Modified: Tue, 29 Jul 2025 18:35:21 GMT  
		Size: 20.8 KB (20771 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:c58767364161c180098aa6daf4620c8c55ad8713deb64ca620668e7bb829bb41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5683246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac911958149764a83bf951afae4135a482e9064dd0c7dbee61474116cf4bc68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1f621f1e5b25aa798d604ab87259f546a42e522b1311f962484669d45183fa`  
		Last Modified: Tue, 29 Jul 2025 16:32:40 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7cf471d76eab33abc760b1edf151f0e3d4d73732c3f002c74ef629f8ded5f9`  
		Last Modified: Tue, 29 Jul 2025 16:32:39 GMT  
		Size: 109.5 KB (109523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a287f0dc98767a99d5c18925da988244c99243b51f5870a4ed36648b93518402`  
		Last Modified: Tue, 29 Jul 2025 16:32:42 GMT  
		Size: 2.0 MB (1957368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101df272f2e8c1be378c334f0d3d2de9dcd2c58db6fe3580d4451396deef84de`  
		Last Modified: Tue, 29 Jul 2025 16:32:41 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f870cbd8529325263ac998fe634981f154a171a39da706e91a9ea2d91038d361`  
		Last Modified: Tue, 29 Jul 2025 16:32:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:837e0ff5feebc7262c78ddd6b4bece1b5b4c3c22b0eb71b71bf9c6c9d154b416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.7 KB (116651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf22108f9222361c74085ca0633d2876cf3187ccaeb4353499f02fc7a24cc51b`

```dockerfile
```

-	Layers:
	-	`sha256:5143c40f563e8ee15ea82be605c093d36fd7445bcd1cedc45d0754c52b6d3f9d`  
		Last Modified: Tue, 29 Jul 2025 18:35:24 GMT  
		Size: 96.1 KB (96135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fcabff32e4e745d2c95395b620e73b812d1c38929ba82167c1d76583a2f4150`  
		Last Modified: Tue, 29 Jul 2025 18:35:25 GMT  
		Size: 20.5 KB (20516 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:04386ede5dcbf35cabad144bcdc951cc64882f7b9727f2d09927fe0d5551dd19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5942089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8252590eee78d67456ac83fd8279259aaea4d2a555c8bc20b173663fcaa2883`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc22e0cec7e7fe8cff10539bca58363ad6749e2de4f878015c25b5f2b6ecadb9`  
		Last Modified: Tue, 29 Jul 2025 16:33:46 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992ebe18219bd78e59e7e56661aae22f700927f47bc7ad1dfe7717093b371c15`  
		Last Modified: Tue, 29 Jul 2025 16:33:49 GMT  
		Size: 124.3 KB (124315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953f5a37d23881d59809ea64dc6ebf1a152a1ff8929f51befb10577771755f5d`  
		Last Modified: Tue, 29 Jul 2025 16:33:49 GMT  
		Size: 2.1 MB (2089310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b62870a2d7b266495d83cfd72dcf702c91c5c60a7e29836bd9bdac776511a7`  
		Last Modified: Tue, 29 Jul 2025 16:33:47 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1cc8c0fe9a4ef7e2ef70e32ddbfbd2fd68985dd452630a8f390c5b41c654f8`  
		Last Modified: Tue, 29 Jul 2025 16:33:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:cf7e9735e4ef5d00dc25928653b808214f070708e9d879ef54afc4d77ce9db2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcceb455cfdb86bdb0c165af3bc54cbab794d56fef1dbae2b484d28027db791c`

```dockerfile
```

-	Layers:
	-	`sha256:a40704a0afb5cf1b90c0fbdf73c5218a4d8f0e93bb39014507b5fa5f8c7265dd`  
		Last Modified: Tue, 29 Jul 2025 18:35:29 GMT  
		Size: 94.3 KB (94287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da22397f364310e72420738395739c36e25b4e4813bbc5da197582a91bb55ac9`  
		Last Modified: Tue, 29 Jul 2025 18:35:29 GMT  
		Size: 20.6 KB (20648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:d55b98c34ba1c2f546461bd57477d46ab868f9de6b107ffb8f20e06dab1e10d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1034dde2661f43165e85db9a13ff0e10d237d14d4b1b7ee1d4570f19d7df4e69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bbdcecb4dec3cbaba0500f9425897948884cfd8db95ccdf9b824d448b24049`  
		Last Modified: Wed, 23 Jul 2025 23:54:15 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c18051d55886d147cafcee8f9e220087c0b60c0e11ec8898a4005352ee0f7e4`  
		Last Modified: Wed, 23 Jul 2025 23:50:14 GMT  
		Size: 107.9 KB (107902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953c2b44fe537b63907764cf78cbb294c6a1133eacb39c62d35ee5d4914779cb`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 1.9 MB (1932977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d69b2f63abf91684a15b9de7b5e617996762376da3fdda50c4e20c2f1e0f4da`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57c134601fc15e8f2cf183cfd9a3057731ad48b915988217f51df31b5d3cf38`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d50b42de80ef3381b05da20cef4ba6ab4491facb607528e075c034257fe9d327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27766c161110b7e46063a39ce6e176f87233fd6722a825ec338e1568892a77a3`

```dockerfile
```

-	Layers:
	-	`sha256:f933f968a4a14795196607a1337a19431e9f61db78bb49c5c2f89f64a17a1d89`  
		Last Modified: Tue, 29 Jul 2025 18:35:33 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffc41094fe9f57bca69da70bbb18eca52aaf6d27d0fb6d79eda79f9e011a157a`  
		Last Modified: Tue, 29 Jul 2025 18:35:33 GMT  
		Size: 20.6 KB (20647 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; s390x

```console
$ docker pull memcached@sha256:cfd223eb11df3d2297224d458caf974f3f0aae4742ff917812f1b8c84c84e705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5797268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e23f18e891a12e72ef84139504baf8783a7db21d4976fc0b607f8e9bbf736f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00131fb0ca26b15f1ac64b82554fc342b19f8c1ef38312a75addb6686f7bc24`  
		Last Modified: Tue, 29 Jul 2025 16:41:40 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e54da6ab620e035fd78987688d45401e87278ec8a5c02cef8a57e4ea9fd286`  
		Last Modified: Tue, 29 Jul 2025 16:41:42 GMT  
		Size: 113.5 KB (113499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6160f9fac1fd86eda224e9ce4740ea46f7e23dc7edb6d1fe9d830001313e63a`  
		Last Modified: Tue, 29 Jul 2025 16:41:46 GMT  
		Size: 2.0 MB (2037446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d01cd71d33b01b420652f4ad9275f1475f4f0bf253dc0a1b48198df2010be5`  
		Last Modified: Tue, 29 Jul 2025 16:41:52 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831dd5e3c39dd2744dc8823190095f709c36020b55ccdaf85f62a146582c7d9d`  
		Last Modified: Tue, 29 Jul 2025 16:41:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:79f0de7e4dcc9afdbfa1fa22250cf3e544d6f3c33174246b427d2865c7e343d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71dad4d71741d8d354038cb6898389aebb54c956dfcd865d57f78dcc3b238bf8`

```dockerfile
```

-	Layers:
	-	`sha256:f942bbb9520308ae352a056c148fdce8f6b09672c257e0a769aa2504bacf1845`  
		Last Modified: Tue, 29 Jul 2025 18:35:37 GMT  
		Size: 94.2 KB (94229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c46680ef7cf08a43965ab9c7727cc70268ee89e366a1ce1806d0f7980b4ad812`  
		Last Modified: Tue, 29 Jul 2025 18:35:38 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine3.22`

```console
$ docker pull memcached@sha256:b50070f2faf253d8aacd530742e8e71791a39222c75abcdbcc442dbb7a2f3f25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
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

### `memcached:alpine3.22` - linux; amd64

```console
$ docker pull memcached@sha256:033134f4dd9f45d4e22b6e98b040ea3fccf0dca740af3c949b44bebf458b04d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5904246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca259aa2216a248c482fc8a069d48b1e70b087529d2c3de97154bfa458dbb7a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fb46bc7dee2beda6f5f6f567aecd4d7d7698b9749ed917988a859b7dd96e30`  
		Last Modified: Tue, 29 Jul 2025 16:32:22 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48faf8c85515fb9d17e0752e77d8241f223d53b1adc90439c606d17daabd0ae`  
		Last Modified: Tue, 29 Jul 2025 16:32:24 GMT  
		Size: 104.7 KB (104725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d552a2d777fd444b41cb79438f9f1b441821162e78d73e96dc848a773cf43892`  
		Last Modified: Tue, 29 Jul 2025 16:32:24 GMT  
		Size: 2.0 MB (1998477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c70665f30f3e15975d429b494cb17b21c5d4630c1800cb0addc3fce3a11aa29`  
		Last Modified: Tue, 29 Jul 2025 16:32:20 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ff68520caaf588cec750ad7c403cf55d79eecfff4b7a4ac5eb3910c90c2817`  
		Last Modified: Tue, 29 Jul 2025 16:32:21 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:7b27e0df383f45d6d523345a078898524a69cee4d6978cf64bf26532b8679dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 KB (116752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb88e7ee6d3e67b2e4f307c081504a685666917ddf50770fe8beb5abd60a3dc5`

```dockerfile
```

-	Layers:
	-	`sha256:2cf00a09ffccb2c00421311314137de90d0586c126b79dbe5315ce321c168b34`  
		Last Modified: Tue, 29 Jul 2025 18:35:07 GMT  
		Size: 96.2 KB (96180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55325ecc9b276e9c55badf949ed4f06840c34aa8baf0aa6f974e0b90dc5d4e0d`  
		Last Modified: Tue, 29 Jul 2025 18:35:07 GMT  
		Size: 20.6 KB (20572 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.22` - linux; arm variant v6

```console
$ docker pull memcached@sha256:78b59dd3af5a55e950f5106869e642af122a7dc470545f4ba533f6833d83b62c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5550795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb09d5ce1b7010f7a36d77494bc5358d666339628c183692906db6a961373847`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c710b5ddcc2882c5014d0c8cb93aec2bd8b6cc3c59fd42b40c87d94f89a7bc7f`  
		Last Modified: Wed, 23 Jul 2025 22:59:16 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c42040d822a4af7f05f9ccd4d18a7a5e4712b118b7f18d1a7969761029a9d2`  
		Last Modified: Wed, 23 Jul 2025 22:59:16 GMT  
		Size: 101.5 KB (101533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3095e18cd24048696efd57ac64d04dde381a3abde625964e02165c7364eb5633`  
		Last Modified: Tue, 29 Jul 2025 16:50:12 GMT  
		Size: 1.9 MB (1947003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0436ec50f04ed972ff0dd760f7e820f192236e5e720bddb6173f65159c7c36`  
		Last Modified: Tue, 29 Jul 2025 16:50:11 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671c24aae36bb04a32e05bd64e1371384f594889cdbbc41029c916447666d402`  
		Last Modified: Tue, 29 Jul 2025 16:50:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:c2a050c6822d834285577c3a001fdfcf9949b7f5a483a4a76a49b549bea19641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54e8bda3e734528caeab4505f084ca7a3076d5ec2273287f66954b5e91af42f`

```dockerfile
```

-	Layers:
	-	`sha256:0d86924831d61ce8b792b25421e9ff0fa2eda9ab940eba5309d44d0eeada7e8e`  
		Last Modified: Tue, 29 Jul 2025 18:35:11 GMT  
		Size: 20.5 KB (20506 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.22` - linux; arm variant v7

```console
$ docker pull memcached@sha256:c9f5db2389b9b0b4a2cd199c4417a9f49a60c42d616e8421177e662d4830de07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9421ed030d4b6b6405714612b8858bda87bc53ac8b0c5ed65c582119527f2d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251060498ca8f0484e20714689b9caba533d09c1b74ed8f2a06780db515a28e2`  
		Last Modified: Thu, 24 Jul 2025 00:27:37 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2293bd2fb47d57e5869c197133067e17f9b1e51ea0f298af1e480e7fd33d681`  
		Last Modified: Thu, 24 Jul 2025 00:27:38 GMT  
		Size: 91.3 KB (91313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ae82f2bac2f7e6fe57f8cb7006fc227c972da1ae5749eba9f5f73e6f3248ec`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 1.9 MB (1905692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e60bf2b2164c620b69e40bdcb64d4104d02eab86c96ea6e170a3601b9ecfd82`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665fe4cd856f1a5c2193568e756c572656949b17c381fc8d43efaa823e18cfa7`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:376a71bc0fef7741e92fdae8b96c825c4622e980de01e724b1a3a0bec3d95f20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 KB (116963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22b574f6c6d021a917c0e99ff4800d8ac3c22fb94b94f88c404cc7609f562fb5`

```dockerfile
```

-	Layers:
	-	`sha256:58ebd4bc7ee5888c552e0fa618f93aefbdb1d15a56ecd3abef19a46ce2f93eee`  
		Last Modified: Tue, 29 Jul 2025 18:35:15 GMT  
		Size: 96.2 KB (96248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d432ed2053ed8249834dd5016fe3199bbc3f82dc7013027c3ead9efe2a007b98`  
		Last Modified: Tue, 29 Jul 2025 18:35:16 GMT  
		Size: 20.7 KB (20715 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b5e4ecc3e927ee30e5cfcfc8aa044960631c75eb8abed9d0fcee6232aa5fdf79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6241700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c880dc2c785861dc9010b813bb6f533f30518443a3bb7e7f477bc96af14582`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbfeb6ac9fd2045c5bea10a301ad554c1f703ffc2885c41520dd5e42eb4a59a`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47acaa5035f94aed634b9d7ecae02fb3838f19e38f8e752ecd6cfba97699b31`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 120.8 KB (120812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8160f3136c6863b52f0dec4f9918b91b8a509700b2071ec0aecd5a6231f00f2a`  
		Last Modified: Tue, 29 Jul 2025 16:41:09 GMT  
		Size: 2.0 MB (1988782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff22f0cad01950efb78a7a862b0becb8b2fd22d795b585f97dad66c091c3dd7`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed19cbfb574c7d8cab364e2ec072c0e03f694468ada41cd70bfcd35392df9e7`  
		Last Modified: Tue, 29 Jul 2025 16:41:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:b4c81c7ababb91ecdda3b7d70514d16818602199d759eb2aadd74de732d52960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 KB (117055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80452fd4f79f6e7a0dab0beebf5c144f9df7c257255cdd3cb93ccbff77001fd6`

```dockerfile
```

-	Layers:
	-	`sha256:f11d2a322f6088804ee63ae1a77b9d5ddcdfdc0c65c22e7a70b7ee67cf4532ed`  
		Last Modified: Tue, 29 Jul 2025 18:35:20 GMT  
		Size: 96.3 KB (96284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e225dd6ea14146ddf445598f24189c065ec684fbeb92e7d053a0211a7d60efda`  
		Last Modified: Tue, 29 Jul 2025 18:35:21 GMT  
		Size: 20.8 KB (20771 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.22` - linux; 386

```console
$ docker pull memcached@sha256:c58767364161c180098aa6daf4620c8c55ad8713deb64ca620668e7bb829bb41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5683246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac911958149764a83bf951afae4135a482e9064dd0c7dbee61474116cf4bc68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1f621f1e5b25aa798d604ab87259f546a42e522b1311f962484669d45183fa`  
		Last Modified: Tue, 29 Jul 2025 16:32:40 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7cf471d76eab33abc760b1edf151f0e3d4d73732c3f002c74ef629f8ded5f9`  
		Last Modified: Tue, 29 Jul 2025 16:32:39 GMT  
		Size: 109.5 KB (109523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a287f0dc98767a99d5c18925da988244c99243b51f5870a4ed36648b93518402`  
		Last Modified: Tue, 29 Jul 2025 16:32:42 GMT  
		Size: 2.0 MB (1957368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101df272f2e8c1be378c334f0d3d2de9dcd2c58db6fe3580d4451396deef84de`  
		Last Modified: Tue, 29 Jul 2025 16:32:41 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f870cbd8529325263ac998fe634981f154a171a39da706e91a9ea2d91038d361`  
		Last Modified: Tue, 29 Jul 2025 16:32:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:837e0ff5feebc7262c78ddd6b4bece1b5b4c3c22b0eb71b71bf9c6c9d154b416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.7 KB (116651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf22108f9222361c74085ca0633d2876cf3187ccaeb4353499f02fc7a24cc51b`

```dockerfile
```

-	Layers:
	-	`sha256:5143c40f563e8ee15ea82be605c093d36fd7445bcd1cedc45d0754c52b6d3f9d`  
		Last Modified: Tue, 29 Jul 2025 18:35:24 GMT  
		Size: 96.1 KB (96135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fcabff32e4e745d2c95395b620e73b812d1c38929ba82167c1d76583a2f4150`  
		Last Modified: Tue, 29 Jul 2025 18:35:25 GMT  
		Size: 20.5 KB (20516 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.22` - linux; ppc64le

```console
$ docker pull memcached@sha256:04386ede5dcbf35cabad144bcdc951cc64882f7b9727f2d09927fe0d5551dd19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5942089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8252590eee78d67456ac83fd8279259aaea4d2a555c8bc20b173663fcaa2883`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc22e0cec7e7fe8cff10539bca58363ad6749e2de4f878015c25b5f2b6ecadb9`  
		Last Modified: Tue, 29 Jul 2025 16:33:46 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992ebe18219bd78e59e7e56661aae22f700927f47bc7ad1dfe7717093b371c15`  
		Last Modified: Tue, 29 Jul 2025 16:33:49 GMT  
		Size: 124.3 KB (124315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953f5a37d23881d59809ea64dc6ebf1a152a1ff8929f51befb10577771755f5d`  
		Last Modified: Tue, 29 Jul 2025 16:33:49 GMT  
		Size: 2.1 MB (2089310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b62870a2d7b266495d83cfd72dcf702c91c5c60a7e29836bd9bdac776511a7`  
		Last Modified: Tue, 29 Jul 2025 16:33:47 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1cc8c0fe9a4ef7e2ef70e32ddbfbd2fd68985dd452630a8f390c5b41c654f8`  
		Last Modified: Tue, 29 Jul 2025 16:33:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:cf7e9735e4ef5d00dc25928653b808214f070708e9d879ef54afc4d77ce9db2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcceb455cfdb86bdb0c165af3bc54cbab794d56fef1dbae2b484d28027db791c`

```dockerfile
```

-	Layers:
	-	`sha256:a40704a0afb5cf1b90c0fbdf73c5218a4d8f0e93bb39014507b5fa5f8c7265dd`  
		Last Modified: Tue, 29 Jul 2025 18:35:29 GMT  
		Size: 94.3 KB (94287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da22397f364310e72420738395739c36e25b4e4813bbc5da197582a91bb55ac9`  
		Last Modified: Tue, 29 Jul 2025 18:35:29 GMT  
		Size: 20.6 KB (20648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.22` - linux; riscv64

```console
$ docker pull memcached@sha256:d55b98c34ba1c2f546461bd57477d46ab868f9de6b107ffb8f20e06dab1e10d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1034dde2661f43165e85db9a13ff0e10d237d14d4b1b7ee1d4570f19d7df4e69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bbdcecb4dec3cbaba0500f9425897948884cfd8db95ccdf9b824d448b24049`  
		Last Modified: Wed, 23 Jul 2025 23:54:15 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c18051d55886d147cafcee8f9e220087c0b60c0e11ec8898a4005352ee0f7e4`  
		Last Modified: Wed, 23 Jul 2025 23:50:14 GMT  
		Size: 107.9 KB (107902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953c2b44fe537b63907764cf78cbb294c6a1133eacb39c62d35ee5d4914779cb`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 1.9 MB (1932977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d69b2f63abf91684a15b9de7b5e617996762376da3fdda50c4e20c2f1e0f4da`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57c134601fc15e8f2cf183cfd9a3057731ad48b915988217f51df31b5d3cf38`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:d50b42de80ef3381b05da20cef4ba6ab4491facb607528e075c034257fe9d327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27766c161110b7e46063a39ce6e176f87233fd6722a825ec338e1568892a77a3`

```dockerfile
```

-	Layers:
	-	`sha256:f933f968a4a14795196607a1337a19431e9f61db78bb49c5c2f89f64a17a1d89`  
		Last Modified: Tue, 29 Jul 2025 18:35:33 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffc41094fe9f57bca69da70bbb18eca52aaf6d27d0fb6d79eda79f9e011a157a`  
		Last Modified: Tue, 29 Jul 2025 18:35:33 GMT  
		Size: 20.6 KB (20647 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.22` - linux; s390x

```console
$ docker pull memcached@sha256:cfd223eb11df3d2297224d458caf974f3f0aae4742ff917812f1b8c84c84e705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5797268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e23f18e891a12e72ef84139504baf8783a7db21d4976fc0b607f8e9bbf736f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00131fb0ca26b15f1ac64b82554fc342b19f8c1ef38312a75addb6686f7bc24`  
		Last Modified: Tue, 29 Jul 2025 16:41:40 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e54da6ab620e035fd78987688d45401e87278ec8a5c02cef8a57e4ea9fd286`  
		Last Modified: Tue, 29 Jul 2025 16:41:42 GMT  
		Size: 113.5 KB (113499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6160f9fac1fd86eda224e9ce4740ea46f7e23dc7edb6d1fe9d830001313e63a`  
		Last Modified: Tue, 29 Jul 2025 16:41:46 GMT  
		Size: 2.0 MB (2037446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d01cd71d33b01b420652f4ad9275f1475f4f0bf253dc0a1b48198df2010be5`  
		Last Modified: Tue, 29 Jul 2025 16:41:52 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831dd5e3c39dd2744dc8823190095f709c36020b55ccdaf85f62a146582c7d9d`  
		Last Modified: Tue, 29 Jul 2025 16:41:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:79f0de7e4dcc9afdbfa1fa22250cf3e544d6f3c33174246b427d2865c7e343d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71dad4d71741d8d354038cb6898389aebb54c956dfcd865d57f78dcc3b238bf8`

```dockerfile
```

-	Layers:
	-	`sha256:f942bbb9520308ae352a056c148fdce8f6b09672c257e0a769aa2504bacf1845`  
		Last Modified: Tue, 29 Jul 2025 18:35:37 GMT  
		Size: 94.2 KB (94229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c46680ef7cf08a43965ab9c7727cc70268ee89e366a1ce1806d0f7980b4ad812`  
		Last Modified: Tue, 29 Jul 2025 18:35:38 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:latest`

```console
$ docker pull memcached@sha256:c8b53d421310f274ece68507406126575bfc2af3ddc66b72709f81ede5fbe2a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:latest` - linux; amd64

```console
$ docker pull memcached@sha256:489c2e770f5baac8e88e7b0fc7bd9ec7482c560232093860fa776480fd535059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32204915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09da43b5484edc83f2f153e8f750eae1edfc09a59f9c3c8a0d1543ad028f7702`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebfc0a813c97c15541bf6e00db67cec64e96bf712ccfedb445eff79095d78dd6`  
		Last Modified: Wed, 13 Aug 2025 21:21:18 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d44cb640c5a78307f95a5ba37e9b3ff77e080db5144ad044331bdd27e2ac3b8`  
		Last Modified: Wed, 13 Aug 2025 21:21:32 GMT  
		Size: 136.6 KB (136560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c2449a0115fae5ca7c26d3857bdae261f4168d8334ad67cb6c3461a0910fc6`  
		Last Modified: Wed, 13 Aug 2025 21:21:36 GMT  
		Size: 2.3 MB (2293557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9bbdd035dc48ae794ba5af4721f9afdab19142a19ba004aa4b42738ef8758d8`  
		Last Modified: Wed, 13 Aug 2025 21:21:42 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc99f3761e7cd9c6f00023c8aa0d889222b7b233949d24870d0f9b7ad10f58dd`  
		Last Modified: Wed, 13 Aug 2025 21:21:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:98607b9259666dec40f29b040ae0cac2276fac6541257d7f3a4d2fa8d30e3ae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2029528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ad42f4e39d2637475a5aaa10a446b94d8cb9b730bd194a0f995abf19ecba3e7`

```dockerfile
```

-	Layers:
	-	`sha256:249ac3e00cc732e2b029808c9c00d3520da2cdf38b1fc01081a592ea90a5e050`  
		Last Modified: Wed, 13 Aug 2025 21:34:23 GMT  
		Size: 2.0 MB (2007332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fdd95540cec834ae6e6c6bf9ad1d03f83f75af3a4d5bc52a9b7018dd212823a`  
		Last Modified: Wed, 13 Aug 2025 21:34:24 GMT  
		Size: 22.2 KB (22196 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:11a993750bd36cfb7d37197d06ccbf217f829c9012146de0d45d0e3494add433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30314569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c2cfe621133fc4a453c7272eacac5ac0ae1cd214c7f7076d785ec3ed0fb6554`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:498399880872f14c562c46bd2a1ef4cfcf3c2a1453514ff0d0f6b7d89f8010dd`  
		Last Modified: Tue, 12 Aug 2025 22:02:01 GMT  
		Size: 27.9 MB (27941706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a99137a20a1adabf0ea411a3bed51f642b1fd51a7c56596ed760ece4727e8c3`  
		Last Modified: Wed, 13 Aug 2025 23:01:56 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7528817abdc345977b6df3988bcacfd622b20f1e6b64e6c01f3c3203275806`  
		Last Modified: Wed, 13 Aug 2025 23:01:57 GMT  
		Size: 144.0 KB (144046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5147466300d5970b08521247c1dcffd9c72644b33c0c4c7a7455293fdaa7514d`  
		Last Modified: Wed, 13 Aug 2025 23:01:58 GMT  
		Size: 2.2 MB (2227304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403dfb443663282b32ef64dddd4d9ece2badd91a91669659aad2213ef1db444c`  
		Last Modified: Wed, 13 Aug 2025 23:00:39 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ac9453a3752c151d9eb3d487d5be8ee9971ce482aa48cbcbffa05e594977ac`  
		Last Modified: Wed, 13 Aug 2025 23:01:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:99d7cc2296b1fdf18d0156098b6c8db466fa371221860e1628d6da1f33862b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe55e32abc4c444556bb77a6cd989bc4c29ae0720781b045162ad41710f332b0`

```dockerfile
```

-	Layers:
	-	`sha256:49bb7a93a18c7972be0483acacb6a99b49edc4bf097a764ed976c48c0516bc14`  
		Last Modified: Thu, 14 Aug 2025 00:34:25 GMT  
		Size: 2.0 MB (2010335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b1896ac27634d50430d62234a56bf5e22627fb59bbe9e2f974832c3f5823cfd`  
		Last Modified: Thu, 14 Aug 2025 00:34:26 GMT  
		Size: 22.3 KB (22343 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v7

```console
$ docker pull memcached@sha256:4b9bce762cb0cd433a31cf56c571b0a5bb7789813cbb111958bf806cba8b87af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28526851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a10eddf8fe36bdc9bc58ad2f45be5555dd9f6f746d916f9ce491ee5f8239bf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc714abeba0eb64ab96f4d3b22e0750d8fb5ca04c15135a1da25d7f28cb90c8`  
		Last Modified: Thu, 14 Aug 2025 03:26:02 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b548feee9753e7f47e9e09d371fbbc5da58c093655fbe6a70e9e8ce1792c6ddc`  
		Last Modified: Thu, 14 Aug 2025 03:26:02 GMT  
		Size: 135.3 KB (135298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9fd10cb429ca884c5738921b455ecc2d83781179e716d4003166bdc8c44e27`  
		Last Modified: Thu, 14 Aug 2025 03:26:01 GMT  
		Size: 2.2 MB (2182550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59893ea711e5a2631eada91282e598b013d3173b17a0edb0fdbe97d67d122e7`  
		Last Modified: Thu, 14 Aug 2025 03:26:02 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8512db29f6abd27987969691ca0de8c6cc141db19a00f2e80bd8996e6cb5de`  
		Last Modified: Thu, 14 Aug 2025 03:26:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:f4b425f37419b579837d2d7857c8ed429c6b2356824bf7c3f83036db9125cc20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f026c9ae0860a234d056b9a6607c5d4673b4e40c52e93c31e76e3cf463fa3c45`

```dockerfile
```

-	Layers:
	-	`sha256:58eba98bd420cdad2a71753e58bb1b1a587f0039d88944045180d74e4c08996c`  
		Last Modified: Thu, 14 Aug 2025 06:34:23 GMT  
		Size: 2.0 MB (2008792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab426c3e7d709a71c837bd5c98de92c219718788268a0700d3c8305f5117b7b8`  
		Last Modified: Thu, 14 Aug 2025 06:34:24 GMT  
		Size: 22.3 KB (22342 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:78a21084b1c4e79dc2fffab373fb465acb723f351bffdc0639a504a5bdc6a2d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32566079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717e9950cc2b302a7f75cdc9919226e0160142934f76014b1a905aa5e39c4046`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d84227403935277ab9817ff62ad9fca6d45f7c109953945d36caa72d73813d0`  
		Last Modified: Wed, 13 Aug 2025 23:02:57 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb0aae300c3cd52b99acd2ae25cb8bf507859ae7b182097672be779a7337fd4`  
		Last Modified: Wed, 13 Aug 2025 23:02:58 GMT  
		Size: 153.4 KB (153369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd2017b19819b1012be52dad0541d85c7797897955d5d0b747b8b86f08da76e`  
		Last Modified: Wed, 13 Aug 2025 23:03:00 GMT  
		Size: 2.3 MB (2275152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad146d7e60bd2063118973d72ff4507de475a826636f2b8fc3bdf36633379d07`  
		Last Modified: Wed, 13 Aug 2025 23:02:59 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fe42a1afd3681fa0efd222132b453c718236f571b4b56018cf362f2333cfb7`  
		Last Modified: Wed, 13 Aug 2025 23:02:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:f34a398dc1f988e0076ebc490e58021e7dc24976392ab10fb871628e11888166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98dee621777b57d248833b652d7622be9c6c901776820489ce629be6f59e5d5f`

```dockerfile
```

-	Layers:
	-	`sha256:4b5fb9727c43d6c906cc0c58b470a99299321ac1e3bcc6a9ea9ec90086d4260d`  
		Last Modified: Thu, 14 Aug 2025 00:34:33 GMT  
		Size: 2.0 MB (2007648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a88652c31f79e7599a31a3fe7d0341deeb4915c7ae0dab214e3c4768ec058300`  
		Last Modified: Thu, 14 Aug 2025 00:34:33 GMT  
		Size: 22.4 KB (22393 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:5b9ccecd7eb2ba800cc927d7dfaa5941d25387818d57d8583260ed7d5ea2ef8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33682664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c160d159b0b83b9824df1d8b4cbe201c4c67902d0171a4a03282d3e230939d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:346d0c953bdbc38917a27a6f30726e5b46419d98ecaf4d2d8f201bc3b7025e57`  
		Last Modified: Tue, 12 Aug 2025 20:45:00 GMT  
		Size: 31.3 MB (31289378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1f928fbfcc7da63ca647a381869549b7db17d2971110bc771c27aeed80b33c`  
		Last Modified: Wed, 13 Aug 2025 21:09:56 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49988f067cdbb2558e23451192304fe7f89c2cbe23fcf5463b9e0b80dfbd2a36`  
		Last Modified: Wed, 13 Aug 2025 21:09:56 GMT  
		Size: 147.4 KB (147419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19f3e01a2ee783f4cf292ba84f151492df7a0170128094f4d011075d629af43`  
		Last Modified: Wed, 13 Aug 2025 21:09:56 GMT  
		Size: 2.2 MB (2244354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2288d51449876e6f7fb89b6cac2eda51fef5f03deb3722ef32bf3a9bdc2f5e17`  
		Last Modified: Wed, 13 Aug 2025 21:09:56 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3668cc13fc1544b7319b7b3307e0d74b4e82d36ca065c5a3be7d080267054267`  
		Last Modified: Wed, 13 Aug 2025 21:09:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:df8cca141522937dd5415946521e71f57731ecc574e78d3175b26ce6260dcd46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2026627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff448533f7fe52a0dc6195d7b9320b996bd2623b7c1e7a5b02f7f5cee32b92a4`

```dockerfile
```

-	Layers:
	-	`sha256:80c0a6ea529144e269d6dc30e72d370cfbc53736314c92cca55d737de9562dd6`  
		Last Modified: Wed, 13 Aug 2025 21:34:31 GMT  
		Size: 2.0 MB (2004489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32faf37cac7f889e11009fc41358994c9714a5ebc9aed8843e1fb57a3de6d243`  
		Last Modified: Wed, 13 Aug 2025 21:34:32 GMT  
		Size: 22.1 KB (22138 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:dcc628faf353367b245beec24d23d1b3103986479dff33e10653c5ef2d8b54b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36182904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d113eca2d57658d5e20bd62171298229010cdbce2c33479664dcad6be5ec2acd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26c42ec1bf9e33e4a6a75b57802a57b9d166fccf4b2e5b13cef2b9742fc5025`  
		Last Modified: Thu, 14 Aug 2025 02:32:42 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a82df09860007e05001d706e92e1aa450bfd12fc72a24522ccca5edc6f43cd`  
		Last Modified: Thu, 14 Aug 2025 02:32:42 GMT  
		Size: 170.2 KB (170241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f425e49b56f20bc4209bec20b1ab8671bd728a94104369def1c947c90134052`  
		Last Modified: Thu, 14 Aug 2025 02:32:42 GMT  
		Size: 2.4 MB (2416933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b832c8b1a0256fd9b38e9fd823309571e179c77a2f44d5115f06ae282b7972f`  
		Last Modified: Thu, 14 Aug 2025 02:32:42 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da165b338847a53b7c8a0a0a08c089c86721f3997c5f507291c4737245ade82f`  
		Last Modified: Thu, 14 Aug 2025 02:32:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:d11fb93c72d4e4416799b886acc2230eefbe26e6381d65c674a1a47f310f22ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2154e1260dfec440f34afa1451b8e89c13a23e1eb451b2250766c9c88cf993a`

```dockerfile
```

-	Layers:
	-	`sha256:3c0cb7a63a69d321f183e466c5c0a934dd9a09173b6e174e2f17a9a24e241dee`  
		Last Modified: Thu, 14 Aug 2025 03:34:34 GMT  
		Size: 2.0 MB (2010933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e4dcd6c60091d8eaa78af8659654106ffc91270b3f5b4b6e166f41e295e361f`  
		Last Modified: Thu, 14 Aug 2025 03:34:35 GMT  
		Size: 22.3 KB (22269 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:c7b8d8a8065d2a0ea3bdaaadd564986a39a88ad9d9ef599faf4f923888bb9126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32288745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6fca6b4af0e7ae24559fc296fb0ce831a94645f64b986956f57f9306df1ed22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024aba4218861d2cdfa6f7186fcca6f2f2041ce6c7210cd258e28d55a2c1fa16`  
		Last Modified: Thu, 14 Aug 2025 02:58:06 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2b32b5cc5f77750b103e7bdeb63810088dca53dae4f8b6eed4e17f219a5826`  
		Last Modified: Thu, 14 Aug 2025 02:58:05 GMT  
		Size: 140.4 KB (140388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a046ba92157d2c0b391049e3f702ebcac682b0c6ee6e651f44d940e5d9bd8cd7`  
		Last Modified: Thu, 14 Aug 2025 02:58:07 GMT  
		Size: 2.3 MB (2313787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd7d0eef9a2ce528ea647334f74bfda29496059b15274182ae0d16fb7e5f28d`  
		Last Modified: Thu, 14 Aug 2025 02:58:06 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c5230e4318cec0912586827ea533d6abfaed20ff08b3662b6cf6871a9abae1`  
		Last Modified: Thu, 14 Aug 2025 02:58:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:88badce3b30eeb4fdb00156647e4a3479b0c7cf8dddb286e0bd07105084f4e5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7704cd55751a22fc58eb4a349020abdd760508cd1b9344ccb0df28dc62d35f98`

```dockerfile
```

-	Layers:
	-	`sha256:91e3962d713f291258d33cdc619c48c657c3a72b3a6c808786e3b209389502b2`  
		Last Modified: Thu, 14 Aug 2025 03:34:39 GMT  
		Size: 2.0 MB (2008769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76baa03c0dea63878577ee4ab27db735c1db244cbefee8f9c7b5d5eb4d3887f1`  
		Last Modified: Thu, 14 Aug 2025 03:34:39 GMT  
		Size: 22.2 KB (22196 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:trixie`

```console
$ docker pull memcached@sha256:c8b53d421310f274ece68507406126575bfc2af3ddc66b72709f81ede5fbe2a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:trixie` - linux; amd64

```console
$ docker pull memcached@sha256:489c2e770f5baac8e88e7b0fc7bd9ec7482c560232093860fa776480fd535059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32204915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09da43b5484edc83f2f153e8f750eae1edfc09a59f9c3c8a0d1543ad028f7702`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebfc0a813c97c15541bf6e00db67cec64e96bf712ccfedb445eff79095d78dd6`  
		Last Modified: Wed, 13 Aug 2025 21:21:18 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d44cb640c5a78307f95a5ba37e9b3ff77e080db5144ad044331bdd27e2ac3b8`  
		Last Modified: Wed, 13 Aug 2025 21:21:32 GMT  
		Size: 136.6 KB (136560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c2449a0115fae5ca7c26d3857bdae261f4168d8334ad67cb6c3461a0910fc6`  
		Last Modified: Wed, 13 Aug 2025 21:21:36 GMT  
		Size: 2.3 MB (2293557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9bbdd035dc48ae794ba5af4721f9afdab19142a19ba004aa4b42738ef8758d8`  
		Last Modified: Wed, 13 Aug 2025 21:21:42 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc99f3761e7cd9c6f00023c8aa0d889222b7b233949d24870d0f9b7ad10f58dd`  
		Last Modified: Wed, 13 Aug 2025 21:21:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:98607b9259666dec40f29b040ae0cac2276fac6541257d7f3a4d2fa8d30e3ae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2029528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ad42f4e39d2637475a5aaa10a446b94d8cb9b730bd194a0f995abf19ecba3e7`

```dockerfile
```

-	Layers:
	-	`sha256:249ac3e00cc732e2b029808c9c00d3520da2cdf38b1fc01081a592ea90a5e050`  
		Last Modified: Wed, 13 Aug 2025 21:34:23 GMT  
		Size: 2.0 MB (2007332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fdd95540cec834ae6e6c6bf9ad1d03f83f75af3a4d5bc52a9b7018dd212823a`  
		Last Modified: Wed, 13 Aug 2025 21:34:24 GMT  
		Size: 22.2 KB (22196 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:11a993750bd36cfb7d37197d06ccbf217f829c9012146de0d45d0e3494add433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30314569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c2cfe621133fc4a453c7272eacac5ac0ae1cd214c7f7076d785ec3ed0fb6554`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:498399880872f14c562c46bd2a1ef4cfcf3c2a1453514ff0d0f6b7d89f8010dd`  
		Last Modified: Tue, 12 Aug 2025 22:02:01 GMT  
		Size: 27.9 MB (27941706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a99137a20a1adabf0ea411a3bed51f642b1fd51a7c56596ed760ece4727e8c3`  
		Last Modified: Wed, 13 Aug 2025 23:01:56 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7528817abdc345977b6df3988bcacfd622b20f1e6b64e6c01f3c3203275806`  
		Last Modified: Wed, 13 Aug 2025 23:01:57 GMT  
		Size: 144.0 KB (144046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5147466300d5970b08521247c1dcffd9c72644b33c0c4c7a7455293fdaa7514d`  
		Last Modified: Wed, 13 Aug 2025 23:01:58 GMT  
		Size: 2.2 MB (2227304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403dfb443663282b32ef64dddd4d9ece2badd91a91669659aad2213ef1db444c`  
		Last Modified: Wed, 13 Aug 2025 23:00:39 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ac9453a3752c151d9eb3d487d5be8ee9971ce482aa48cbcbffa05e594977ac`  
		Last Modified: Wed, 13 Aug 2025 23:01:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:99d7cc2296b1fdf18d0156098b6c8db466fa371221860e1628d6da1f33862b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe55e32abc4c444556bb77a6cd989bc4c29ae0720781b045162ad41710f332b0`

```dockerfile
```

-	Layers:
	-	`sha256:49bb7a93a18c7972be0483acacb6a99b49edc4bf097a764ed976c48c0516bc14`  
		Last Modified: Thu, 14 Aug 2025 00:34:25 GMT  
		Size: 2.0 MB (2010335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b1896ac27634d50430d62234a56bf5e22627fb59bbe9e2f974832c3f5823cfd`  
		Last Modified: Thu, 14 Aug 2025 00:34:26 GMT  
		Size: 22.3 KB (22343 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:4b9bce762cb0cd433a31cf56c571b0a5bb7789813cbb111958bf806cba8b87af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28526851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a10eddf8fe36bdc9bc58ad2f45be5555dd9f6f746d916f9ce491ee5f8239bf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc714abeba0eb64ab96f4d3b22e0750d8fb5ca04c15135a1da25d7f28cb90c8`  
		Last Modified: Thu, 14 Aug 2025 03:26:02 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b548feee9753e7f47e9e09d371fbbc5da58c093655fbe6a70e9e8ce1792c6ddc`  
		Last Modified: Thu, 14 Aug 2025 03:26:02 GMT  
		Size: 135.3 KB (135298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9fd10cb429ca884c5738921b455ecc2d83781179e716d4003166bdc8c44e27`  
		Last Modified: Thu, 14 Aug 2025 03:26:01 GMT  
		Size: 2.2 MB (2182550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59893ea711e5a2631eada91282e598b013d3173b17a0edb0fdbe97d67d122e7`  
		Last Modified: Thu, 14 Aug 2025 03:26:02 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8512db29f6abd27987969691ca0de8c6cc141db19a00f2e80bd8996e6cb5de`  
		Last Modified: Thu, 14 Aug 2025 03:26:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:f4b425f37419b579837d2d7857c8ed429c6b2356824bf7c3f83036db9125cc20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f026c9ae0860a234d056b9a6607c5d4673b4e40c52e93c31e76e3cf463fa3c45`

```dockerfile
```

-	Layers:
	-	`sha256:58eba98bd420cdad2a71753e58bb1b1a587f0039d88944045180d74e4c08996c`  
		Last Modified: Thu, 14 Aug 2025 06:34:23 GMT  
		Size: 2.0 MB (2008792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab426c3e7d709a71c837bd5c98de92c219718788268a0700d3c8305f5117b7b8`  
		Last Modified: Thu, 14 Aug 2025 06:34:24 GMT  
		Size: 22.3 KB (22342 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:78a21084b1c4e79dc2fffab373fb465acb723f351bffdc0639a504a5bdc6a2d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32566079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717e9950cc2b302a7f75cdc9919226e0160142934f76014b1a905aa5e39c4046`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d84227403935277ab9817ff62ad9fca6d45f7c109953945d36caa72d73813d0`  
		Last Modified: Wed, 13 Aug 2025 23:02:57 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb0aae300c3cd52b99acd2ae25cb8bf507859ae7b182097672be779a7337fd4`  
		Last Modified: Wed, 13 Aug 2025 23:02:58 GMT  
		Size: 153.4 KB (153369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd2017b19819b1012be52dad0541d85c7797897955d5d0b747b8b86f08da76e`  
		Last Modified: Wed, 13 Aug 2025 23:03:00 GMT  
		Size: 2.3 MB (2275152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad146d7e60bd2063118973d72ff4507de475a826636f2b8fc3bdf36633379d07`  
		Last Modified: Wed, 13 Aug 2025 23:02:59 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fe42a1afd3681fa0efd222132b453c718236f571b4b56018cf362f2333cfb7`  
		Last Modified: Wed, 13 Aug 2025 23:02:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:f34a398dc1f988e0076ebc490e58021e7dc24976392ab10fb871628e11888166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98dee621777b57d248833b652d7622be9c6c901776820489ce629be6f59e5d5f`

```dockerfile
```

-	Layers:
	-	`sha256:4b5fb9727c43d6c906cc0c58b470a99299321ac1e3bcc6a9ea9ec90086d4260d`  
		Last Modified: Thu, 14 Aug 2025 00:34:33 GMT  
		Size: 2.0 MB (2007648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a88652c31f79e7599a31a3fe7d0341deeb4915c7ae0dab214e3c4768ec058300`  
		Last Modified: Thu, 14 Aug 2025 00:34:33 GMT  
		Size: 22.4 KB (22393 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; 386

```console
$ docker pull memcached@sha256:5b9ccecd7eb2ba800cc927d7dfaa5941d25387818d57d8583260ed7d5ea2ef8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33682664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c160d159b0b83b9824df1d8b4cbe201c4c67902d0171a4a03282d3e230939d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:346d0c953bdbc38917a27a6f30726e5b46419d98ecaf4d2d8f201bc3b7025e57`  
		Last Modified: Tue, 12 Aug 2025 20:45:00 GMT  
		Size: 31.3 MB (31289378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1f928fbfcc7da63ca647a381869549b7db17d2971110bc771c27aeed80b33c`  
		Last Modified: Wed, 13 Aug 2025 21:09:56 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49988f067cdbb2558e23451192304fe7f89c2cbe23fcf5463b9e0b80dfbd2a36`  
		Last Modified: Wed, 13 Aug 2025 21:09:56 GMT  
		Size: 147.4 KB (147419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19f3e01a2ee783f4cf292ba84f151492df7a0170128094f4d011075d629af43`  
		Last Modified: Wed, 13 Aug 2025 21:09:56 GMT  
		Size: 2.2 MB (2244354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2288d51449876e6f7fb89b6cac2eda51fef5f03deb3722ef32bf3a9bdc2f5e17`  
		Last Modified: Wed, 13 Aug 2025 21:09:56 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3668cc13fc1544b7319b7b3307e0d74b4e82d36ca065c5a3be7d080267054267`  
		Last Modified: Wed, 13 Aug 2025 21:09:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:df8cca141522937dd5415946521e71f57731ecc574e78d3175b26ce6260dcd46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2026627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff448533f7fe52a0dc6195d7b9320b996bd2623b7c1e7a5b02f7f5cee32b92a4`

```dockerfile
```

-	Layers:
	-	`sha256:80c0a6ea529144e269d6dc30e72d370cfbc53736314c92cca55d737de9562dd6`  
		Last Modified: Wed, 13 Aug 2025 21:34:31 GMT  
		Size: 2.0 MB (2004489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32faf37cac7f889e11009fc41358994c9714a5ebc9aed8843e1fb57a3de6d243`  
		Last Modified: Wed, 13 Aug 2025 21:34:32 GMT  
		Size: 22.1 KB (22138 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:dcc628faf353367b245beec24d23d1b3103986479dff33e10653c5ef2d8b54b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36182904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d113eca2d57658d5e20bd62171298229010cdbce2c33479664dcad6be5ec2acd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26c42ec1bf9e33e4a6a75b57802a57b9d166fccf4b2e5b13cef2b9742fc5025`  
		Last Modified: Thu, 14 Aug 2025 02:32:42 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a82df09860007e05001d706e92e1aa450bfd12fc72a24522ccca5edc6f43cd`  
		Last Modified: Thu, 14 Aug 2025 02:32:42 GMT  
		Size: 170.2 KB (170241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f425e49b56f20bc4209bec20b1ab8671bd728a94104369def1c947c90134052`  
		Last Modified: Thu, 14 Aug 2025 02:32:42 GMT  
		Size: 2.4 MB (2416933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b832c8b1a0256fd9b38e9fd823309571e179c77a2f44d5115f06ae282b7972f`  
		Last Modified: Thu, 14 Aug 2025 02:32:42 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da165b338847a53b7c8a0a0a08c089c86721f3997c5f507291c4737245ade82f`  
		Last Modified: Thu, 14 Aug 2025 02:32:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:d11fb93c72d4e4416799b886acc2230eefbe26e6381d65c674a1a47f310f22ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2154e1260dfec440f34afa1451b8e89c13a23e1eb451b2250766c9c88cf993a`

```dockerfile
```

-	Layers:
	-	`sha256:3c0cb7a63a69d321f183e466c5c0a934dd9a09173b6e174e2f17a9a24e241dee`  
		Last Modified: Thu, 14 Aug 2025 03:34:34 GMT  
		Size: 2.0 MB (2010933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e4dcd6c60091d8eaa78af8659654106ffc91270b3f5b4b6e166f41e295e361f`  
		Last Modified: Thu, 14 Aug 2025 03:34:35 GMT  
		Size: 22.3 KB (22269 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; s390x

```console
$ docker pull memcached@sha256:c7b8d8a8065d2a0ea3bdaaadd564986a39a88ad9d9ef599faf4f923888bb9126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32288745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6fca6b4af0e7ae24559fc296fb0ce831a94645f64b986956f57f9306df1ed22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024aba4218861d2cdfa6f7186fcca6f2f2041ce6c7210cd258e28d55a2c1fa16`  
		Last Modified: Thu, 14 Aug 2025 02:58:06 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2b32b5cc5f77750b103e7bdeb63810088dca53dae4f8b6eed4e17f219a5826`  
		Last Modified: Thu, 14 Aug 2025 02:58:05 GMT  
		Size: 140.4 KB (140388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a046ba92157d2c0b391049e3f702ebcac682b0c6ee6e651f44d940e5d9bd8cd7`  
		Last Modified: Thu, 14 Aug 2025 02:58:07 GMT  
		Size: 2.3 MB (2313787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd7d0eef9a2ce528ea647334f74bfda29496059b15274182ae0d16fb7e5f28d`  
		Last Modified: Thu, 14 Aug 2025 02:58:06 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c5230e4318cec0912586827ea533d6abfaed20ff08b3662b6cf6871a9abae1`  
		Last Modified: Thu, 14 Aug 2025 02:58:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:88badce3b30eeb4fdb00156647e4a3479b0c7cf8dddb286e0bd07105084f4e5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7704cd55751a22fc58eb4a349020abdd760508cd1b9344ccb0df28dc62d35f98`

```dockerfile
```

-	Layers:
	-	`sha256:91e3962d713f291258d33cdc619c48c657c3a72b3a6c808786e3b209389502b2`  
		Last Modified: Thu, 14 Aug 2025 03:34:39 GMT  
		Size: 2.0 MB (2008769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76baa03c0dea63878577ee4ab27db735c1db244cbefee8f9c7b5d5eb4d3887f1`  
		Last Modified: Thu, 14 Aug 2025 03:34:39 GMT  
		Size: 22.2 KB (22196 bytes)  
		MIME: application/vnd.in-toto+json
