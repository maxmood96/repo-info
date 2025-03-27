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
$ docker pull memcached@sha256:56725c927f12a53093b0dd8a58ddd8df3d020b46567cb14a8e0201279b97a79e
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
$ docker pull memcached@sha256:c1130e43766e72579b0bb3de4a483b13617fc482b7a3f660833032ddd3df46ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33000858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d4e3512a87fc3884351cf771b57d83866a516c78d3313b209064b6257c17b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14ee0758901af029fd1a78a75a39cef72470aa2c4538747549decb8769c9036`  
		Last Modified: Thu, 27 Mar 2025 20:53:08 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a603c9ce7da5d29d874ef3f48909ac8d815642ee1161fb1088c5c79590059ded`  
		Last Modified: Thu, 27 Mar 2025 20:53:09 GMT  
		Size: 2.5 MB (2491772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6080c85c433088b18ef903a680b49c4c60d2cdf59b8653368bec12dbef863d54`  
		Last Modified: Thu, 27 Mar 2025 20:53:08 GMT  
		Size: 2.3 MB (2302705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b725e8c43056a4da24ef0710ac4716517b27c4ffd092842d38289d6efbb7ab25`  
		Last Modified: Thu, 27 Mar 2025 20:53:08 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfffb76f39255069f9125012bc7bc79eeaeb3f9c248ef8f35de284adafd60312`  
		Last Modified: Thu, 27 Mar 2025 20:53:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:e6c4e9ea0da3ea8f19a3d9280c07e1908364c8c40779cbb2d4f65feaee440615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2312005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4242aa375d1ecdacb2c396dac8135d5aa9caf7db2374a6216f2ad87e3cf05d`

```dockerfile
```

-	Layers:
	-	`sha256:5049b68d7e40887d89a570516aa826f3c1401d51538fa705eefa45144e8da58e`  
		Last Modified: Thu, 27 Mar 2025 20:53:08 GMT  
		Size: 2.3 MB (2289333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7273a520dbd5019d2de56854018a19f4479f6eceba42c52a77dfb5716bfd57c3`  
		Last Modified: Thu, 27 Mar 2025 20:53:08 GMT  
		Size: 22.7 KB (22672 bytes)  
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
$ docker pull memcached@sha256:c014ab323b1b4bcbb3166beafd41410dbddfbb1a0a6f19deb69e802762874555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32689553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f119d1180b3eca14d9a554f5a3a4e962d438c72c8e71c607ef6688353aa74e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
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
	-	`sha256:c583561c73b24d79d3cb55803558b6f1e508bb37288ee1635b47bdf9a51a38da`  
		Last Modified: Thu, 27 Mar 2025 20:54:02 GMT  
		Size: 2.3 MB (2288694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e039a4f24583d1fa81e89c1a686785aff6e7a269cafcb224a2b61b3d05c6f0ea`  
		Last Modified: Thu, 27 Mar 2025 20:54:01 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aad33c6fcc162e8b1413e31976faafcba7edc16db7e020bc51a9b57c5ecf490`  
		Last Modified: Thu, 27 Mar 2025 20:54:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:73ecf1ebde9749379f2fba28e4e4ba518b5d4943a699ee9745cb9e89f423cb4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2312518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6766598d442fb4e939fe0f028c923ef5ed6b6766633eb2f01669a27a672232`

```dockerfile
```

-	Layers:
	-	`sha256:e93a26c0b4c7baf66130df39a4ea1e3fe6f1767bc12f5ef6698589251a6b6d58`  
		Last Modified: Thu, 27 Mar 2025 20:54:02 GMT  
		Size: 2.3 MB (2289648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5f2e6a18098b4d97813a7772aa4e2bf79a1f45eedbe86caf481cb1840fa9586`  
		Last Modified: Thu, 27 Mar 2025 20:54:01 GMT  
		Size: 22.9 KB (22870 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:a5ea0c0aa510a293159050b633c507887a11ebcdc5abb316a7154fcd83ff32c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33943021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfaa7026b44f46e71ba9c44a1481824fdcf9b54f5047b75c26c8710944a5475c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bd5b700a5532cf1e91c064d6ed472b6c511c3d9e9b08a7f31f608192b9afad`  
		Last Modified: Thu, 27 Mar 2025 20:53:34 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c7d8b538dbde73a9a5e3e42f1a04a0fd79356f7f702038a5b159b503cfc1e5`  
		Last Modified: Thu, 27 Mar 2025 20:53:35 GMT  
		Size: 2.5 MB (2500728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7542439206b95728641ceb4b680180a73442cabd6b41fe578628f18b945a9e2a`  
		Last Modified: Thu, 27 Mar 2025 20:53:35 GMT  
		Size: 2.3 MB (2251248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a46d28f72d87befc244136b60a9c42a9b18e552434f284c5687e64805032464`  
		Last Modified: Thu, 27 Mar 2025 20:53:34 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42201d898a9285374141b63bacd52743d268d2f3d800b22b5ee94e5e553fbf8`  
		Last Modified: Thu, 27 Mar 2025 20:53:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:3972e3e9979c0f37a3396a5d86757d1c64ff1661a01486faa24077f6cc9ea8a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2309047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa4d34e6df623288ed6ec9f921a2605e855bfe7736d69fc81466b9e9b903ae7`

```dockerfile
```

-	Layers:
	-	`sha256:9ea1e6ba191d57b2933c4d03388f6a23b8d2b5e5a7fe476d51afcdbf00f53f5c`  
		Last Modified: Thu, 27 Mar 2025 20:53:35 GMT  
		Size: 2.3 MB (2286432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd31371d2f6db2ac800c33bd000734380c9ac8a14aca23e7c2d17ef259810eba`  
		Last Modified: Thu, 27 Mar 2025 20:53:34 GMT  
		Size: 22.6 KB (22615 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; mips64le

```console
$ docker pull memcached@sha256:0058a46283d5026f6e6d46d9f8bf0bc5007eefa0fb50ba124a8d9c5c8718c92a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32751201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3b77978b5a8fc2eac21e1b870c55c85b4c6184d63d4ebf29b6e8f154e6af6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1742169600'
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
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
	-	`sha256:40897f2d64cafc6fcb222667c78c37539448596456ecffd3f8ce7cb9b5cabb28`  
		Last Modified: Thu, 27 Mar 2025 20:57:34 GMT  
		Size: 2.3 MB (2317020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82dc27b022eac657403b67589f084f87ad57c6f2891889c6d34ebb4474ee310`  
		Last Modified: Thu, 27 Mar 2025 20:57:34 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e60fc6582e411940064800863c4b87c02105118e0ab5e9648ba1dc12ad8f61`  
		Last Modified: Thu, 27 Mar 2025 20:57:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:f4049ead4762d06719ad4fdd2ae2b4f0046a130d2891e2ade50695d33f6d10f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 KB (22569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ba92a7b7f909a167a9bf4e5b91ff175e39f2e162a4f1e6ccf92f49c51b6006`

```dockerfile
```

-	Layers:
	-	`sha256:a8aaf8662d9c73787c7977bf75670f2471e3dd62e02f2103193777209066ad7e`  
		Last Modified: Thu, 27 Mar 2025 20:57:33 GMT  
		Size: 22.6 KB (22569 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:7a7bb97c6c61dd3b4c61f8065dab499bbdfe7cfbe4cb956effa9edcb2e66af3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37176878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc98e5d5a70cd46d1686601994b63dc20ca2175f52c40dba598b762926e2a37c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
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
	-	`sha256:253d36c80692194d710c838a9dcf641b5f4e5b708caf7a0167a65231d784da21`  
		Last Modified: Thu, 27 Mar 2025 20:52:14 GMT  
		Size: 2.4 MB (2418931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815dd2a928bdc05f75187e8f6ea5d86523616fee3840ca9163dbf320a5a6ccc7`  
		Last Modified: Thu, 27 Mar 2025 20:52:13 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121efc6039ff41bfa98a9b47bcf4885d5e03c9456814d0361df3e771d123d137`  
		Last Modified: Thu, 27 Mar 2025 20:52:13 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:d58f5f6a5ac867f60ce3aadad1e9917e3c03c7abb83b35be66d9f4cdcd7be38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2316452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8bcaaed8fc07c31e2e028ca1bc38f788ad0afe190b58e4ba7e054fcb4f4340`

```dockerfile
```

-	Layers:
	-	`sha256:27246f4bfd4ab676df1caa36848b296c12c320d9fc5d0b12540a193755ca7353`  
		Last Modified: Thu, 27 Mar 2025 20:52:14 GMT  
		Size: 2.3 MB (2293705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd9de6d66fe54e520712184227e13e9b50f4e82e578f5812610dd60205ae9f61`  
		Last Modified: Thu, 27 Mar 2025 20:52:13 GMT  
		Size: 22.7 KB (22747 bytes)  
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
$ docker pull memcached@sha256:7da5f599a2a094daee0cdc0654ce5188389ee6c7d4b34ded97d4b8177ec3ee89
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
$ docker pull memcached@sha256:06c629488bcbeeb5ce4b3701748928d93d1b32778a0e729fdc3a5374eaba4571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5746566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56bdd3e4a7232079ba7497e7a5fdc7995c9742cc777c57d4cc6b78f91ec073c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1341251c0a26b782fc5ad7d13973a828fa117452636a63d4ae201b1667af32`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66a1cc00f297101211a7a048e61e1072370d39ecac768421aadccc8eeb63886`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 104.7 KB (104693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e764e8e2bff857e5ff55376c244229b37704bf0d8907bba88555f37e409981d2`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 2.0 MB (1998269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278163aab69155dd6749e516fd5aa7ac1c8804dbd96615b6c6c5d084adbeaed6`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35d8ffb74c551d7cdd9c1a838d885466c863663bc11ba5866e2cdcc14da5b13`  
		Last Modified: Thu, 27 Mar 2025 20:53:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7c8fdb5dcff76dd27e53ba9cb1682214360b3787e9758840a7f8e0e9e7f3cc15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66b46bea0468821817967032976045f8680b204a6277a76ab860a1b6f9125db2`

```dockerfile
```

-	Layers:
	-	`sha256:6f3203e9b8cd79a8f7763cd6e69146dad76bc1c77e3d2302caba89a423037bf9`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 93.6 KB (93633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac63a4f8a3074e4d23c3c8a1a59305cec2e5d28d1b025df6d1540b8f73174ff8`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 21.2 KB (21159 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:684f5401f5f644171126d516de1ebdcb1608433972008bb421508aa7c3abb1b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6104612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb60fe52ab38f8d170995e48747f784b5d30f72cc8cc5ecde8a2a3f789435bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
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
	-	`sha256:abb28ae90c9bffea35355aef624a2e35ecaedd538b0bbc177e52734d7ab3dcd2`  
		Last Modified: Thu, 27 Mar 2025 20:57:10 GMT  
		Size: 2.0 MB (1989460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9471b9190bd21604219c213d28e742bdd010051f6ea84ecd6723e7eb9e0bf7`  
		Last Modified: Thu, 27 Mar 2025 20:57:09 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189f409c92e6a19050d616acb8da97bddfff5c598fc3903ceb7141c91235d6fa`  
		Last Modified: Thu, 27 Mar 2025 20:57:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:707fc3a048ec6345dc3f8828ff0cb13627f8437236439a243de930cd586e9138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d75d4d1d6177f5310b1a617d8a643092097f96d6253e7c98c69bc61d853505`

```dockerfile
```

-	Layers:
	-	`sha256:1d113af0ec580fd3c52e1675b66ffd5453996b0f564448dcf9f231c02192c184`  
		Last Modified: Thu, 27 Mar 2025 20:57:09 GMT  
		Size: 93.7 KB (93737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48139650f70b212083be85e732df16032edcc486b3af2dfbac099741fef6bb2`  
		Last Modified: Thu, 27 Mar 2025 20:57:09 GMT  
		Size: 21.4 KB (21356 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:b40fc687669e8c2d9dbac25e1f627e5c27ce30d1636b0ae32ea8b0d3d2c56ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5534238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8c8e64a825b2c7e4c88e1ca4d0a45305c37b4b3308e819dab16a852e47d2719`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e2f92344d79ef7f1ba0a143585705ed78f249d82bceb677069e5373b3edea9`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae03b6003c1510a2c1bc31c06714cf492ff9ae437f9cbe1d835bc1b3afa95a4`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 109.5 KB (109484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f729c997aa8639d7314cd6b15d0d678628e45bdf485953f69cb89966d078795`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 2.0 MB (1959776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e488a63a3c8d2aa14b4ef7c3c0e563ff99ba11a36b602ce7c81a499f598efcd`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363743b6d219afcbcc9cd8037d51201784e1b3c1605e5c5b6c85d42fa3315788`  
		Last Modified: Thu, 27 Mar 2025 20:53:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:27084cf0d56fdead95f5789352b216da11bb2798a6fcffd9f41125c2ecdf95ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 KB (114689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df8ec4074a13a2d084b6c2da617b85afac8f4a5bc80ec144bc81dd04e752e45`

```dockerfile
```

-	Layers:
	-	`sha256:0d2eb1fe2f7200332e0f72a04f10ec6a9355c72a25b95ff6dbc26dc84c428ede`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 93.6 KB (93588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40259002d91f5318e16c29fd221af80ba97f7a89b92d761a067cc1ed95270a5e`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 21.1 KB (21101 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:e983630451e7d57a7ced6bd4a893c9903a2b50ae487efa4f0b8f5b298f6cfa34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5791362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c9ba664c418a4c21c59a935f8b35644fe1d17ea0fd99f693645818d7097b6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
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
	-	`sha256:427e1b046fb9f579d4b7879a999d743f20bd21eb9f7ec3aa8e98c5dff5fa7ce2`  
		Last Modified: Thu, 27 Mar 2025 20:55:24 GMT  
		Size: 2.1 MB (2091383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661f0560043b5762cdfe652be7c75103b960f325ddf9c7d39079e1ef5da44730`  
		Last Modified: Thu, 27 Mar 2025 20:55:23 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976e19956b9f2e61552a8a71907b18fc974d41b5ee50b5f0b422469c6811e306`  
		Last Modified: Thu, 27 Mar 2025 20:55:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9fb4e7ab3a251a8a5ebaa9bea164dbe4d2fda72570c279440c9d95f5f26bcb67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 KB (112972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a413dea3279278472afb6eadef6effca79012a2f955eaf5fa39a5d410c111373`

```dockerfile
```

-	Layers:
	-	`sha256:c222b8b6f12483b61f4c3e3738172861210af0947bb823a874b4bdbfc72770aa`  
		Last Modified: Thu, 27 Mar 2025 20:55:23 GMT  
		Size: 91.7 KB (91740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc826d89b23d4bd8b0c27863fbedc9e2474d48194575f8e5f4eaa3ec7db78ecf`  
		Last Modified: Thu, 27 Mar 2025 20:55:23 GMT  
		Size: 21.2 KB (21232 bytes)  
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
$ docker pull memcached@sha256:709ca82c737ee52acc94da9623ba812e9117074d754b5aa2060faae09e9cae75
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
$ docker pull memcached@sha256:06c629488bcbeeb5ce4b3701748928d93d1b32778a0e729fdc3a5374eaba4571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5746566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56bdd3e4a7232079ba7497e7a5fdc7995c9742cc777c57d4cc6b78f91ec073c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1341251c0a26b782fc5ad7d13973a828fa117452636a63d4ae201b1667af32`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66a1cc00f297101211a7a048e61e1072370d39ecac768421aadccc8eeb63886`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 104.7 KB (104693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e764e8e2bff857e5ff55376c244229b37704bf0d8907bba88555f37e409981d2`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 2.0 MB (1998269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278163aab69155dd6749e516fd5aa7ac1c8804dbd96615b6c6c5d084adbeaed6`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35d8ffb74c551d7cdd9c1a838d885466c863663bc11ba5866e2cdcc14da5b13`  
		Last Modified: Thu, 27 Mar 2025 20:53:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:7c8fdb5dcff76dd27e53ba9cb1682214360b3787e9758840a7f8e0e9e7f3cc15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66b46bea0468821817967032976045f8680b204a6277a76ab860a1b6f9125db2`

```dockerfile
```

-	Layers:
	-	`sha256:6f3203e9b8cd79a8f7763cd6e69146dad76bc1c77e3d2302caba89a423037bf9`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 93.6 KB (93633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac63a4f8a3074e4d23c3c8a1a59305cec2e5d28d1b025df6d1540b8f73174ff8`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 21.2 KB (21159 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:684f5401f5f644171126d516de1ebdcb1608433972008bb421508aa7c3abb1b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6104612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb60fe52ab38f8d170995e48747f784b5d30f72cc8cc5ecde8a2a3f789435bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
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
	-	`sha256:abb28ae90c9bffea35355aef624a2e35ecaedd538b0bbc177e52734d7ab3dcd2`  
		Last Modified: Thu, 27 Mar 2025 20:57:10 GMT  
		Size: 2.0 MB (1989460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9471b9190bd21604219c213d28e742bdd010051f6ea84ecd6723e7eb9e0bf7`  
		Last Modified: Thu, 27 Mar 2025 20:57:09 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189f409c92e6a19050d616acb8da97bddfff5c598fc3903ceb7141c91235d6fa`  
		Last Modified: Thu, 27 Mar 2025 20:57:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:707fc3a048ec6345dc3f8828ff0cb13627f8437236439a243de930cd586e9138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d75d4d1d6177f5310b1a617d8a643092097f96d6253e7c98c69bc61d853505`

```dockerfile
```

-	Layers:
	-	`sha256:1d113af0ec580fd3c52e1675b66ffd5453996b0f564448dcf9f231c02192c184`  
		Last Modified: Thu, 27 Mar 2025 20:57:09 GMT  
		Size: 93.7 KB (93737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48139650f70b212083be85e732df16032edcc486b3af2dfbac099741fef6bb2`  
		Last Modified: Thu, 27 Mar 2025 20:57:09 GMT  
		Size: 21.4 KB (21356 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; 386

```console
$ docker pull memcached@sha256:b40fc687669e8c2d9dbac25e1f627e5c27ce30d1636b0ae32ea8b0d3d2c56ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5534238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8c8e64a825b2c7e4c88e1ca4d0a45305c37b4b3308e819dab16a852e47d2719`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e2f92344d79ef7f1ba0a143585705ed78f249d82bceb677069e5373b3edea9`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae03b6003c1510a2c1bc31c06714cf492ff9ae437f9cbe1d835bc1b3afa95a4`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 109.5 KB (109484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f729c997aa8639d7314cd6b15d0d678628e45bdf485953f69cb89966d078795`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 2.0 MB (1959776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e488a63a3c8d2aa14b4ef7c3c0e563ff99ba11a36b602ce7c81a499f598efcd`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363743b6d219afcbcc9cd8037d51201784e1b3c1605e5c5b6c85d42fa3315788`  
		Last Modified: Thu, 27 Mar 2025 20:53:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:27084cf0d56fdead95f5789352b216da11bb2798a6fcffd9f41125c2ecdf95ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 KB (114689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df8ec4074a13a2d084b6c2da617b85afac8f4a5bc80ec144bc81dd04e752e45`

```dockerfile
```

-	Layers:
	-	`sha256:0d2eb1fe2f7200332e0f72a04f10ec6a9355c72a25b95ff6dbc26dc84c428ede`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 93.6 KB (93588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40259002d91f5318e16c29fd221af80ba97f7a89b92d761a067cc1ed95270a5e`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 21.1 KB (21101 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; ppc64le

```console
$ docker pull memcached@sha256:e983630451e7d57a7ced6bd4a893c9903a2b50ae487efa4f0b8f5b298f6cfa34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5791362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c9ba664c418a4c21c59a935f8b35644fe1d17ea0fd99f693645818d7097b6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
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
	-	`sha256:427e1b046fb9f579d4b7879a999d743f20bd21eb9f7ec3aa8e98c5dff5fa7ce2`  
		Last Modified: Thu, 27 Mar 2025 20:55:24 GMT  
		Size: 2.1 MB (2091383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661f0560043b5762cdfe652be7c75103b960f325ddf9c7d39079e1ef5da44730`  
		Last Modified: Thu, 27 Mar 2025 20:55:23 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976e19956b9f2e61552a8a71907b18fc974d41b5ee50b5f0b422469c6811e306`  
		Last Modified: Thu, 27 Mar 2025 20:55:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:9fb4e7ab3a251a8a5ebaa9bea164dbe4d2fda72570c279440c9d95f5f26bcb67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 KB (112972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a413dea3279278472afb6eadef6effca79012a2f955eaf5fa39a5d410c111373`

```dockerfile
```

-	Layers:
	-	`sha256:c222b8b6f12483b61f4c3e3738172861210af0947bb823a874b4bdbfc72770aa`  
		Last Modified: Thu, 27 Mar 2025 20:55:23 GMT  
		Size: 91.7 KB (91740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc826d89b23d4bd8b0c27863fbedc9e2474d48194575f8e5f4eaa3ec7db78ecf`  
		Last Modified: Thu, 27 Mar 2025 20:55:23 GMT  
		Size: 21.2 KB (21232 bytes)  
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
$ docker pull memcached@sha256:56725c927f12a53093b0dd8a58ddd8df3d020b46567cb14a8e0201279b97a79e
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
$ docker pull memcached@sha256:c1130e43766e72579b0bb3de4a483b13617fc482b7a3f660833032ddd3df46ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33000858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d4e3512a87fc3884351cf771b57d83866a516c78d3313b209064b6257c17b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14ee0758901af029fd1a78a75a39cef72470aa2c4538747549decb8769c9036`  
		Last Modified: Thu, 27 Mar 2025 20:53:08 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a603c9ce7da5d29d874ef3f48909ac8d815642ee1161fb1088c5c79590059ded`  
		Last Modified: Thu, 27 Mar 2025 20:53:09 GMT  
		Size: 2.5 MB (2491772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6080c85c433088b18ef903a680b49c4c60d2cdf59b8653368bec12dbef863d54`  
		Last Modified: Thu, 27 Mar 2025 20:53:08 GMT  
		Size: 2.3 MB (2302705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b725e8c43056a4da24ef0710ac4716517b27c4ffd092842d38289d6efbb7ab25`  
		Last Modified: Thu, 27 Mar 2025 20:53:08 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfffb76f39255069f9125012bc7bc79eeaeb3f9c248ef8f35de284adafd60312`  
		Last Modified: Thu, 27 Mar 2025 20:53:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:e6c4e9ea0da3ea8f19a3d9280c07e1908364c8c40779cbb2d4f65feaee440615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2312005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4242aa375d1ecdacb2c396dac8135d5aa9caf7db2374a6216f2ad87e3cf05d`

```dockerfile
```

-	Layers:
	-	`sha256:5049b68d7e40887d89a570516aa826f3c1401d51538fa705eefa45144e8da58e`  
		Last Modified: Thu, 27 Mar 2025 20:53:08 GMT  
		Size: 2.3 MB (2289333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7273a520dbd5019d2de56854018a19f4479f6eceba42c52a77dfb5716bfd57c3`  
		Last Modified: Thu, 27 Mar 2025 20:53:08 GMT  
		Size: 22.7 KB (22672 bytes)  
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
$ docker pull memcached@sha256:c014ab323b1b4bcbb3166beafd41410dbddfbb1a0a6f19deb69e802762874555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32689553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f119d1180b3eca14d9a554f5a3a4e962d438c72c8e71c607ef6688353aa74e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
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
	-	`sha256:c583561c73b24d79d3cb55803558b6f1e508bb37288ee1635b47bdf9a51a38da`  
		Last Modified: Thu, 27 Mar 2025 20:54:02 GMT  
		Size: 2.3 MB (2288694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e039a4f24583d1fa81e89c1a686785aff6e7a269cafcb224a2b61b3d05c6f0ea`  
		Last Modified: Thu, 27 Mar 2025 20:54:01 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aad33c6fcc162e8b1413e31976faafcba7edc16db7e020bc51a9b57c5ecf490`  
		Last Modified: Thu, 27 Mar 2025 20:54:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:73ecf1ebde9749379f2fba28e4e4ba518b5d4943a699ee9745cb9e89f423cb4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2312518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6766598d442fb4e939fe0f028c923ef5ed6b6766633eb2f01669a27a672232`

```dockerfile
```

-	Layers:
	-	`sha256:e93a26c0b4c7baf66130df39a4ea1e3fe6f1767bc12f5ef6698589251a6b6d58`  
		Last Modified: Thu, 27 Mar 2025 20:54:02 GMT  
		Size: 2.3 MB (2289648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5f2e6a18098b4d97813a7772aa4e2bf79a1f45eedbe86caf481cb1840fa9586`  
		Last Modified: Thu, 27 Mar 2025 20:54:01 GMT  
		Size: 22.9 KB (22870 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:a5ea0c0aa510a293159050b633c507887a11ebcdc5abb316a7154fcd83ff32c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33943021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfaa7026b44f46e71ba9c44a1481824fdcf9b54f5047b75c26c8710944a5475c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bd5b700a5532cf1e91c064d6ed472b6c511c3d9e9b08a7f31f608192b9afad`  
		Last Modified: Thu, 27 Mar 2025 20:53:34 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c7d8b538dbde73a9a5e3e42f1a04a0fd79356f7f702038a5b159b503cfc1e5`  
		Last Modified: Thu, 27 Mar 2025 20:53:35 GMT  
		Size: 2.5 MB (2500728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7542439206b95728641ceb4b680180a73442cabd6b41fe578628f18b945a9e2a`  
		Last Modified: Thu, 27 Mar 2025 20:53:35 GMT  
		Size: 2.3 MB (2251248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a46d28f72d87befc244136b60a9c42a9b18e552434f284c5687e64805032464`  
		Last Modified: Thu, 27 Mar 2025 20:53:34 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42201d898a9285374141b63bacd52743d268d2f3d800b22b5ee94e5e553fbf8`  
		Last Modified: Thu, 27 Mar 2025 20:53:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:3972e3e9979c0f37a3396a5d86757d1c64ff1661a01486faa24077f6cc9ea8a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2309047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa4d34e6df623288ed6ec9f921a2605e855bfe7736d69fc81466b9e9b903ae7`

```dockerfile
```

-	Layers:
	-	`sha256:9ea1e6ba191d57b2933c4d03388f6a23b8d2b5e5a7fe476d51afcdbf00f53f5c`  
		Last Modified: Thu, 27 Mar 2025 20:53:35 GMT  
		Size: 2.3 MB (2286432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd31371d2f6db2ac800c33bd000734380c9ac8a14aca23e7c2d17ef259810eba`  
		Last Modified: Thu, 27 Mar 2025 20:53:34 GMT  
		Size: 22.6 KB (22615 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:0058a46283d5026f6e6d46d9f8bf0bc5007eefa0fb50ba124a8d9c5c8718c92a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32751201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3b77978b5a8fc2eac21e1b870c55c85b4c6184d63d4ebf29b6e8f154e6af6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1742169600'
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
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
	-	`sha256:40897f2d64cafc6fcb222667c78c37539448596456ecffd3f8ce7cb9b5cabb28`  
		Last Modified: Thu, 27 Mar 2025 20:57:34 GMT  
		Size: 2.3 MB (2317020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82dc27b022eac657403b67589f084f87ad57c6f2891889c6d34ebb4474ee310`  
		Last Modified: Thu, 27 Mar 2025 20:57:34 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e60fc6582e411940064800863c4b87c02105118e0ab5e9648ba1dc12ad8f61`  
		Last Modified: Thu, 27 Mar 2025 20:57:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f4049ead4762d06719ad4fdd2ae2b4f0046a130d2891e2ade50695d33f6d10f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 KB (22569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ba92a7b7f909a167a9bf4e5b91ff175e39f2e162a4f1e6ccf92f49c51b6006`

```dockerfile
```

-	Layers:
	-	`sha256:a8aaf8662d9c73787c7977bf75670f2471e3dd62e02f2103193777209066ad7e`  
		Last Modified: Thu, 27 Mar 2025 20:57:33 GMT  
		Size: 22.6 KB (22569 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:7a7bb97c6c61dd3b4c61f8065dab499bbdfe7cfbe4cb956effa9edcb2e66af3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37176878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc98e5d5a70cd46d1686601994b63dc20ca2175f52c40dba598b762926e2a37c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
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
	-	`sha256:253d36c80692194d710c838a9dcf641b5f4e5b708caf7a0167a65231d784da21`  
		Last Modified: Thu, 27 Mar 2025 20:52:14 GMT  
		Size: 2.4 MB (2418931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815dd2a928bdc05f75187e8f6ea5d86523616fee3840ca9163dbf320a5a6ccc7`  
		Last Modified: Thu, 27 Mar 2025 20:52:13 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121efc6039ff41bfa98a9b47bcf4885d5e03c9456814d0361df3e771d123d137`  
		Last Modified: Thu, 27 Mar 2025 20:52:13 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:d58f5f6a5ac867f60ce3aadad1e9917e3c03c7abb83b35be66d9f4cdcd7be38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2316452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8bcaaed8fc07c31e2e028ca1bc38f788ad0afe190b58e4ba7e054fcb4f4340`

```dockerfile
```

-	Layers:
	-	`sha256:27246f4bfd4ab676df1caa36848b296c12c320d9fc5d0b12540a193755ca7353`  
		Last Modified: Thu, 27 Mar 2025 20:52:14 GMT  
		Size: 2.3 MB (2293705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd9de6d66fe54e520712184227e13e9b50f4e82e578f5812610dd60205ae9f61`  
		Last Modified: Thu, 27 Mar 2025 20:52:13 GMT  
		Size: 22.7 KB (22747 bytes)  
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
$ docker pull memcached@sha256:56725c927f12a53093b0dd8a58ddd8df3d020b46567cb14a8e0201279b97a79e
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
$ docker pull memcached@sha256:c1130e43766e72579b0bb3de4a483b13617fc482b7a3f660833032ddd3df46ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33000858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d4e3512a87fc3884351cf771b57d83866a516c78d3313b209064b6257c17b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14ee0758901af029fd1a78a75a39cef72470aa2c4538747549decb8769c9036`  
		Last Modified: Thu, 27 Mar 2025 20:53:08 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a603c9ce7da5d29d874ef3f48909ac8d815642ee1161fb1088c5c79590059ded`  
		Last Modified: Thu, 27 Mar 2025 20:53:09 GMT  
		Size: 2.5 MB (2491772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6080c85c433088b18ef903a680b49c4c60d2cdf59b8653368bec12dbef863d54`  
		Last Modified: Thu, 27 Mar 2025 20:53:08 GMT  
		Size: 2.3 MB (2302705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b725e8c43056a4da24ef0710ac4716517b27c4ffd092842d38289d6efbb7ab25`  
		Last Modified: Thu, 27 Mar 2025 20:53:08 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfffb76f39255069f9125012bc7bc79eeaeb3f9c248ef8f35de284adafd60312`  
		Last Modified: Thu, 27 Mar 2025 20:53:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:e6c4e9ea0da3ea8f19a3d9280c07e1908364c8c40779cbb2d4f65feaee440615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2312005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4242aa375d1ecdacb2c396dac8135d5aa9caf7db2374a6216f2ad87e3cf05d`

```dockerfile
```

-	Layers:
	-	`sha256:5049b68d7e40887d89a570516aa826f3c1401d51538fa705eefa45144e8da58e`  
		Last Modified: Thu, 27 Mar 2025 20:53:08 GMT  
		Size: 2.3 MB (2289333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7273a520dbd5019d2de56854018a19f4479f6eceba42c52a77dfb5716bfd57c3`  
		Last Modified: Thu, 27 Mar 2025 20:53:08 GMT  
		Size: 22.7 KB (22672 bytes)  
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
$ docker pull memcached@sha256:c014ab323b1b4bcbb3166beafd41410dbddfbb1a0a6f19deb69e802762874555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32689553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f119d1180b3eca14d9a554f5a3a4e962d438c72c8e71c607ef6688353aa74e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
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
	-	`sha256:c583561c73b24d79d3cb55803558b6f1e508bb37288ee1635b47bdf9a51a38da`  
		Last Modified: Thu, 27 Mar 2025 20:54:02 GMT  
		Size: 2.3 MB (2288694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e039a4f24583d1fa81e89c1a686785aff6e7a269cafcb224a2b61b3d05c6f0ea`  
		Last Modified: Thu, 27 Mar 2025 20:54:01 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aad33c6fcc162e8b1413e31976faafcba7edc16db7e020bc51a9b57c5ecf490`  
		Last Modified: Thu, 27 Mar 2025 20:54:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:73ecf1ebde9749379f2fba28e4e4ba518b5d4943a699ee9745cb9e89f423cb4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2312518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6766598d442fb4e939fe0f028c923ef5ed6b6766633eb2f01669a27a672232`

```dockerfile
```

-	Layers:
	-	`sha256:e93a26c0b4c7baf66130df39a4ea1e3fe6f1767bc12f5ef6698589251a6b6d58`  
		Last Modified: Thu, 27 Mar 2025 20:54:02 GMT  
		Size: 2.3 MB (2289648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5f2e6a18098b4d97813a7772aa4e2bf79a1f45eedbe86caf481cb1840fa9586`  
		Last Modified: Thu, 27 Mar 2025 20:54:01 GMT  
		Size: 22.9 KB (22870 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; 386

```console
$ docker pull memcached@sha256:a5ea0c0aa510a293159050b633c507887a11ebcdc5abb316a7154fcd83ff32c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33943021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfaa7026b44f46e71ba9c44a1481824fdcf9b54f5047b75c26c8710944a5475c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bd5b700a5532cf1e91c064d6ed472b6c511c3d9e9b08a7f31f608192b9afad`  
		Last Modified: Thu, 27 Mar 2025 20:53:34 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c7d8b538dbde73a9a5e3e42f1a04a0fd79356f7f702038a5b159b503cfc1e5`  
		Last Modified: Thu, 27 Mar 2025 20:53:35 GMT  
		Size: 2.5 MB (2500728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7542439206b95728641ceb4b680180a73442cabd6b41fe578628f18b945a9e2a`  
		Last Modified: Thu, 27 Mar 2025 20:53:35 GMT  
		Size: 2.3 MB (2251248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a46d28f72d87befc244136b60a9c42a9b18e552434f284c5687e64805032464`  
		Last Modified: Thu, 27 Mar 2025 20:53:34 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42201d898a9285374141b63bacd52743d268d2f3d800b22b5ee94e5e553fbf8`  
		Last Modified: Thu, 27 Mar 2025 20:53:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:3972e3e9979c0f37a3396a5d86757d1c64ff1661a01486faa24077f6cc9ea8a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2309047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa4d34e6df623288ed6ec9f921a2605e855bfe7736d69fc81466b9e9b903ae7`

```dockerfile
```

-	Layers:
	-	`sha256:9ea1e6ba191d57b2933c4d03388f6a23b8d2b5e5a7fe476d51afcdbf00f53f5c`  
		Last Modified: Thu, 27 Mar 2025 20:53:35 GMT  
		Size: 2.3 MB (2286432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd31371d2f6db2ac800c33bd000734380c9ac8a14aca23e7c2d17ef259810eba`  
		Last Modified: Thu, 27 Mar 2025 20:53:34 GMT  
		Size: 22.6 KB (22615 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; mips64le

```console
$ docker pull memcached@sha256:0058a46283d5026f6e6d46d9f8bf0bc5007eefa0fb50ba124a8d9c5c8718c92a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32751201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3b77978b5a8fc2eac21e1b870c55c85b4c6184d63d4ebf29b6e8f154e6af6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1742169600'
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
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
	-	`sha256:40897f2d64cafc6fcb222667c78c37539448596456ecffd3f8ce7cb9b5cabb28`  
		Last Modified: Thu, 27 Mar 2025 20:57:34 GMT  
		Size: 2.3 MB (2317020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82dc27b022eac657403b67589f084f87ad57c6f2891889c6d34ebb4474ee310`  
		Last Modified: Thu, 27 Mar 2025 20:57:34 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e60fc6582e411940064800863c4b87c02105118e0ab5e9648ba1dc12ad8f61`  
		Last Modified: Thu, 27 Mar 2025 20:57:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:f4049ead4762d06719ad4fdd2ae2b4f0046a130d2891e2ade50695d33f6d10f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 KB (22569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ba92a7b7f909a167a9bf4e5b91ff175e39f2e162a4f1e6ccf92f49c51b6006`

```dockerfile
```

-	Layers:
	-	`sha256:a8aaf8662d9c73787c7977bf75670f2471e3dd62e02f2103193777209066ad7e`  
		Last Modified: Thu, 27 Mar 2025 20:57:33 GMT  
		Size: 22.6 KB (22569 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:7a7bb97c6c61dd3b4c61f8065dab499bbdfe7cfbe4cb956effa9edcb2e66af3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37176878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc98e5d5a70cd46d1686601994b63dc20ca2175f52c40dba598b762926e2a37c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
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
	-	`sha256:253d36c80692194d710c838a9dcf641b5f4e5b708caf7a0167a65231d784da21`  
		Last Modified: Thu, 27 Mar 2025 20:52:14 GMT  
		Size: 2.4 MB (2418931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815dd2a928bdc05f75187e8f6ea5d86523616fee3840ca9163dbf320a5a6ccc7`  
		Last Modified: Thu, 27 Mar 2025 20:52:13 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121efc6039ff41bfa98a9b47bcf4885d5e03c9456814d0361df3e771d123d137`  
		Last Modified: Thu, 27 Mar 2025 20:52:13 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:d58f5f6a5ac867f60ce3aadad1e9917e3c03c7abb83b35be66d9f4cdcd7be38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2316452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8bcaaed8fc07c31e2e028ca1bc38f788ad0afe190b58e4ba7e054fcb4f4340`

```dockerfile
```

-	Layers:
	-	`sha256:27246f4bfd4ab676df1caa36848b296c12c320d9fc5d0b12540a193755ca7353`  
		Last Modified: Thu, 27 Mar 2025 20:52:14 GMT  
		Size: 2.3 MB (2293705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd9de6d66fe54e520712184227e13e9b50f4e82e578f5812610dd60205ae9f61`  
		Last Modified: Thu, 27 Mar 2025 20:52:13 GMT  
		Size: 22.7 KB (22747 bytes)  
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
$ docker pull memcached@sha256:7da5f599a2a094daee0cdc0654ce5188389ee6c7d4b34ded97d4b8177ec3ee89
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
$ docker pull memcached@sha256:06c629488bcbeeb5ce4b3701748928d93d1b32778a0e729fdc3a5374eaba4571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5746566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56bdd3e4a7232079ba7497e7a5fdc7995c9742cc777c57d4cc6b78f91ec073c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1341251c0a26b782fc5ad7d13973a828fa117452636a63d4ae201b1667af32`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66a1cc00f297101211a7a048e61e1072370d39ecac768421aadccc8eeb63886`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 104.7 KB (104693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e764e8e2bff857e5ff55376c244229b37704bf0d8907bba88555f37e409981d2`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 2.0 MB (1998269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278163aab69155dd6749e516fd5aa7ac1c8804dbd96615b6c6c5d084adbeaed6`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35d8ffb74c551d7cdd9c1a838d885466c863663bc11ba5866e2cdcc14da5b13`  
		Last Modified: Thu, 27 Mar 2025 20:53:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7c8fdb5dcff76dd27e53ba9cb1682214360b3787e9758840a7f8e0e9e7f3cc15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66b46bea0468821817967032976045f8680b204a6277a76ab860a1b6f9125db2`

```dockerfile
```

-	Layers:
	-	`sha256:6f3203e9b8cd79a8f7763cd6e69146dad76bc1c77e3d2302caba89a423037bf9`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 93.6 KB (93633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac63a4f8a3074e4d23c3c8a1a59305cec2e5d28d1b025df6d1540b8f73174ff8`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 21.2 KB (21159 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:684f5401f5f644171126d516de1ebdcb1608433972008bb421508aa7c3abb1b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6104612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb60fe52ab38f8d170995e48747f784b5d30f72cc8cc5ecde8a2a3f789435bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
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
	-	`sha256:abb28ae90c9bffea35355aef624a2e35ecaedd538b0bbc177e52734d7ab3dcd2`  
		Last Modified: Thu, 27 Mar 2025 20:57:10 GMT  
		Size: 2.0 MB (1989460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9471b9190bd21604219c213d28e742bdd010051f6ea84ecd6723e7eb9e0bf7`  
		Last Modified: Thu, 27 Mar 2025 20:57:09 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189f409c92e6a19050d616acb8da97bddfff5c598fc3903ceb7141c91235d6fa`  
		Last Modified: Thu, 27 Mar 2025 20:57:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:707fc3a048ec6345dc3f8828ff0cb13627f8437236439a243de930cd586e9138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d75d4d1d6177f5310b1a617d8a643092097f96d6253e7c98c69bc61d853505`

```dockerfile
```

-	Layers:
	-	`sha256:1d113af0ec580fd3c52e1675b66ffd5453996b0f564448dcf9f231c02192c184`  
		Last Modified: Thu, 27 Mar 2025 20:57:09 GMT  
		Size: 93.7 KB (93737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48139650f70b212083be85e732df16032edcc486b3af2dfbac099741fef6bb2`  
		Last Modified: Thu, 27 Mar 2025 20:57:09 GMT  
		Size: 21.4 KB (21356 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:b40fc687669e8c2d9dbac25e1f627e5c27ce30d1636b0ae32ea8b0d3d2c56ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5534238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8c8e64a825b2c7e4c88e1ca4d0a45305c37b4b3308e819dab16a852e47d2719`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e2f92344d79ef7f1ba0a143585705ed78f249d82bceb677069e5373b3edea9`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae03b6003c1510a2c1bc31c06714cf492ff9ae437f9cbe1d835bc1b3afa95a4`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 109.5 KB (109484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f729c997aa8639d7314cd6b15d0d678628e45bdf485953f69cb89966d078795`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 2.0 MB (1959776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e488a63a3c8d2aa14b4ef7c3c0e563ff99ba11a36b602ce7c81a499f598efcd`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363743b6d219afcbcc9cd8037d51201784e1b3c1605e5c5b6c85d42fa3315788`  
		Last Modified: Thu, 27 Mar 2025 20:53:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:27084cf0d56fdead95f5789352b216da11bb2798a6fcffd9f41125c2ecdf95ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 KB (114689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df8ec4074a13a2d084b6c2da617b85afac8f4a5bc80ec144bc81dd04e752e45`

```dockerfile
```

-	Layers:
	-	`sha256:0d2eb1fe2f7200332e0f72a04f10ec6a9355c72a25b95ff6dbc26dc84c428ede`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 93.6 KB (93588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40259002d91f5318e16c29fd221af80ba97f7a89b92d761a067cc1ed95270a5e`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 21.1 KB (21101 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:e983630451e7d57a7ced6bd4a893c9903a2b50ae487efa4f0b8f5b298f6cfa34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5791362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c9ba664c418a4c21c59a935f8b35644fe1d17ea0fd99f693645818d7097b6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
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
	-	`sha256:427e1b046fb9f579d4b7879a999d743f20bd21eb9f7ec3aa8e98c5dff5fa7ce2`  
		Last Modified: Thu, 27 Mar 2025 20:55:24 GMT  
		Size: 2.1 MB (2091383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661f0560043b5762cdfe652be7c75103b960f325ddf9c7d39079e1ef5da44730`  
		Last Modified: Thu, 27 Mar 2025 20:55:23 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976e19956b9f2e61552a8a71907b18fc974d41b5ee50b5f0b422469c6811e306`  
		Last Modified: Thu, 27 Mar 2025 20:55:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9fb4e7ab3a251a8a5ebaa9bea164dbe4d2fda72570c279440c9d95f5f26bcb67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 KB (112972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a413dea3279278472afb6eadef6effca79012a2f955eaf5fa39a5d410c111373`

```dockerfile
```

-	Layers:
	-	`sha256:c222b8b6f12483b61f4c3e3738172861210af0947bb823a874b4bdbfc72770aa`  
		Last Modified: Thu, 27 Mar 2025 20:55:23 GMT  
		Size: 91.7 KB (91740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc826d89b23d4bd8b0c27863fbedc9e2474d48194575f8e5f4eaa3ec7db78ecf`  
		Last Modified: Thu, 27 Mar 2025 20:55:23 GMT  
		Size: 21.2 KB (21232 bytes)  
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
$ docker pull memcached@sha256:709ca82c737ee52acc94da9623ba812e9117074d754b5aa2060faae09e9cae75
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
$ docker pull memcached@sha256:06c629488bcbeeb5ce4b3701748928d93d1b32778a0e729fdc3a5374eaba4571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5746566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56bdd3e4a7232079ba7497e7a5fdc7995c9742cc777c57d4cc6b78f91ec073c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1341251c0a26b782fc5ad7d13973a828fa117452636a63d4ae201b1667af32`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66a1cc00f297101211a7a048e61e1072370d39ecac768421aadccc8eeb63886`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 104.7 KB (104693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e764e8e2bff857e5ff55376c244229b37704bf0d8907bba88555f37e409981d2`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 2.0 MB (1998269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278163aab69155dd6749e516fd5aa7ac1c8804dbd96615b6c6c5d084adbeaed6`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35d8ffb74c551d7cdd9c1a838d885466c863663bc11ba5866e2cdcc14da5b13`  
		Last Modified: Thu, 27 Mar 2025 20:53:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:7c8fdb5dcff76dd27e53ba9cb1682214360b3787e9758840a7f8e0e9e7f3cc15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66b46bea0468821817967032976045f8680b204a6277a76ab860a1b6f9125db2`

```dockerfile
```

-	Layers:
	-	`sha256:6f3203e9b8cd79a8f7763cd6e69146dad76bc1c77e3d2302caba89a423037bf9`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 93.6 KB (93633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac63a4f8a3074e4d23c3c8a1a59305cec2e5d28d1b025df6d1540b8f73174ff8`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 21.2 KB (21159 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:684f5401f5f644171126d516de1ebdcb1608433972008bb421508aa7c3abb1b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6104612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb60fe52ab38f8d170995e48747f784b5d30f72cc8cc5ecde8a2a3f789435bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
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
	-	`sha256:abb28ae90c9bffea35355aef624a2e35ecaedd538b0bbc177e52734d7ab3dcd2`  
		Last Modified: Thu, 27 Mar 2025 20:57:10 GMT  
		Size: 2.0 MB (1989460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9471b9190bd21604219c213d28e742bdd010051f6ea84ecd6723e7eb9e0bf7`  
		Last Modified: Thu, 27 Mar 2025 20:57:09 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189f409c92e6a19050d616acb8da97bddfff5c598fc3903ceb7141c91235d6fa`  
		Last Modified: Thu, 27 Mar 2025 20:57:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:707fc3a048ec6345dc3f8828ff0cb13627f8437236439a243de930cd586e9138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d75d4d1d6177f5310b1a617d8a643092097f96d6253e7c98c69bc61d853505`

```dockerfile
```

-	Layers:
	-	`sha256:1d113af0ec580fd3c52e1675b66ffd5453996b0f564448dcf9f231c02192c184`  
		Last Modified: Thu, 27 Mar 2025 20:57:09 GMT  
		Size: 93.7 KB (93737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48139650f70b212083be85e732df16032edcc486b3af2dfbac099741fef6bb2`  
		Last Modified: Thu, 27 Mar 2025 20:57:09 GMT  
		Size: 21.4 KB (21356 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.21` - linux; 386

```console
$ docker pull memcached@sha256:b40fc687669e8c2d9dbac25e1f627e5c27ce30d1636b0ae32ea8b0d3d2c56ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5534238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8c8e64a825b2c7e4c88e1ca4d0a45305c37b4b3308e819dab16a852e47d2719`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e2f92344d79ef7f1ba0a143585705ed78f249d82bceb677069e5373b3edea9`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae03b6003c1510a2c1bc31c06714cf492ff9ae437f9cbe1d835bc1b3afa95a4`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 109.5 KB (109484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f729c997aa8639d7314cd6b15d0d678628e45bdf485953f69cb89966d078795`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 2.0 MB (1959776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e488a63a3c8d2aa14b4ef7c3c0e563ff99ba11a36b602ce7c81a499f598efcd`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363743b6d219afcbcc9cd8037d51201784e1b3c1605e5c5b6c85d42fa3315788`  
		Last Modified: Thu, 27 Mar 2025 20:53:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:27084cf0d56fdead95f5789352b216da11bb2798a6fcffd9f41125c2ecdf95ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 KB (114689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df8ec4074a13a2d084b6c2da617b85afac8f4a5bc80ec144bc81dd04e752e45`

```dockerfile
```

-	Layers:
	-	`sha256:0d2eb1fe2f7200332e0f72a04f10ec6a9355c72a25b95ff6dbc26dc84c428ede`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 93.6 KB (93588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40259002d91f5318e16c29fd221af80ba97f7a89b92d761a067cc1ed95270a5e`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 21.1 KB (21101 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.21` - linux; ppc64le

```console
$ docker pull memcached@sha256:e983630451e7d57a7ced6bd4a893c9903a2b50ae487efa4f0b8f5b298f6cfa34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5791362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c9ba664c418a4c21c59a935f8b35644fe1d17ea0fd99f693645818d7097b6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
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
	-	`sha256:427e1b046fb9f579d4b7879a999d743f20bd21eb9f7ec3aa8e98c5dff5fa7ce2`  
		Last Modified: Thu, 27 Mar 2025 20:55:24 GMT  
		Size: 2.1 MB (2091383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661f0560043b5762cdfe652be7c75103b960f325ddf9c7d39079e1ef5da44730`  
		Last Modified: Thu, 27 Mar 2025 20:55:23 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976e19956b9f2e61552a8a71907b18fc974d41b5ee50b5f0b422469c6811e306`  
		Last Modified: Thu, 27 Mar 2025 20:55:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:9fb4e7ab3a251a8a5ebaa9bea164dbe4d2fda72570c279440c9d95f5f26bcb67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 KB (112972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a413dea3279278472afb6eadef6effca79012a2f955eaf5fa39a5d410c111373`

```dockerfile
```

-	Layers:
	-	`sha256:c222b8b6f12483b61f4c3e3738172861210af0947bb823a874b4bdbfc72770aa`  
		Last Modified: Thu, 27 Mar 2025 20:55:23 GMT  
		Size: 91.7 KB (91740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc826d89b23d4bd8b0c27863fbedc9e2474d48194575f8e5f4eaa3ec7db78ecf`  
		Last Modified: Thu, 27 Mar 2025 20:55:23 GMT  
		Size: 21.2 KB (21232 bytes)  
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
$ docker pull memcached@sha256:56725c927f12a53093b0dd8a58ddd8df3d020b46567cb14a8e0201279b97a79e
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
$ docker pull memcached@sha256:c1130e43766e72579b0bb3de4a483b13617fc482b7a3f660833032ddd3df46ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33000858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d4e3512a87fc3884351cf771b57d83866a516c78d3313b209064b6257c17b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14ee0758901af029fd1a78a75a39cef72470aa2c4538747549decb8769c9036`  
		Last Modified: Thu, 27 Mar 2025 20:53:08 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a603c9ce7da5d29d874ef3f48909ac8d815642ee1161fb1088c5c79590059ded`  
		Last Modified: Thu, 27 Mar 2025 20:53:09 GMT  
		Size: 2.5 MB (2491772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6080c85c433088b18ef903a680b49c4c60d2cdf59b8653368bec12dbef863d54`  
		Last Modified: Thu, 27 Mar 2025 20:53:08 GMT  
		Size: 2.3 MB (2302705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b725e8c43056a4da24ef0710ac4716517b27c4ffd092842d38289d6efbb7ab25`  
		Last Modified: Thu, 27 Mar 2025 20:53:08 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfffb76f39255069f9125012bc7bc79eeaeb3f9c248ef8f35de284adafd60312`  
		Last Modified: Thu, 27 Mar 2025 20:53:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:e6c4e9ea0da3ea8f19a3d9280c07e1908364c8c40779cbb2d4f65feaee440615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2312005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4242aa375d1ecdacb2c396dac8135d5aa9caf7db2374a6216f2ad87e3cf05d`

```dockerfile
```

-	Layers:
	-	`sha256:5049b68d7e40887d89a570516aa826f3c1401d51538fa705eefa45144e8da58e`  
		Last Modified: Thu, 27 Mar 2025 20:53:08 GMT  
		Size: 2.3 MB (2289333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7273a520dbd5019d2de56854018a19f4479f6eceba42c52a77dfb5716bfd57c3`  
		Last Modified: Thu, 27 Mar 2025 20:53:08 GMT  
		Size: 22.7 KB (22672 bytes)  
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
$ docker pull memcached@sha256:c014ab323b1b4bcbb3166beafd41410dbddfbb1a0a6f19deb69e802762874555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32689553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f119d1180b3eca14d9a554f5a3a4e962d438c72c8e71c607ef6688353aa74e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
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
	-	`sha256:c583561c73b24d79d3cb55803558b6f1e508bb37288ee1635b47bdf9a51a38da`  
		Last Modified: Thu, 27 Mar 2025 20:54:02 GMT  
		Size: 2.3 MB (2288694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e039a4f24583d1fa81e89c1a686785aff6e7a269cafcb224a2b61b3d05c6f0ea`  
		Last Modified: Thu, 27 Mar 2025 20:54:01 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aad33c6fcc162e8b1413e31976faafcba7edc16db7e020bc51a9b57c5ecf490`  
		Last Modified: Thu, 27 Mar 2025 20:54:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:73ecf1ebde9749379f2fba28e4e4ba518b5d4943a699ee9745cb9e89f423cb4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2312518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6766598d442fb4e939fe0f028c923ef5ed6b6766633eb2f01669a27a672232`

```dockerfile
```

-	Layers:
	-	`sha256:e93a26c0b4c7baf66130df39a4ea1e3fe6f1767bc12f5ef6698589251a6b6d58`  
		Last Modified: Thu, 27 Mar 2025 20:54:02 GMT  
		Size: 2.3 MB (2289648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5f2e6a18098b4d97813a7772aa4e2bf79a1f45eedbe86caf481cb1840fa9586`  
		Last Modified: Thu, 27 Mar 2025 20:54:01 GMT  
		Size: 22.9 KB (22870 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:a5ea0c0aa510a293159050b633c507887a11ebcdc5abb316a7154fcd83ff32c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33943021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfaa7026b44f46e71ba9c44a1481824fdcf9b54f5047b75c26c8710944a5475c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bd5b700a5532cf1e91c064d6ed472b6c511c3d9e9b08a7f31f608192b9afad`  
		Last Modified: Thu, 27 Mar 2025 20:53:34 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c7d8b538dbde73a9a5e3e42f1a04a0fd79356f7f702038a5b159b503cfc1e5`  
		Last Modified: Thu, 27 Mar 2025 20:53:35 GMT  
		Size: 2.5 MB (2500728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7542439206b95728641ceb4b680180a73442cabd6b41fe578628f18b945a9e2a`  
		Last Modified: Thu, 27 Mar 2025 20:53:35 GMT  
		Size: 2.3 MB (2251248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a46d28f72d87befc244136b60a9c42a9b18e552434f284c5687e64805032464`  
		Last Modified: Thu, 27 Mar 2025 20:53:34 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42201d898a9285374141b63bacd52743d268d2f3d800b22b5ee94e5e553fbf8`  
		Last Modified: Thu, 27 Mar 2025 20:53:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:3972e3e9979c0f37a3396a5d86757d1c64ff1661a01486faa24077f6cc9ea8a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2309047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa4d34e6df623288ed6ec9f921a2605e855bfe7736d69fc81466b9e9b903ae7`

```dockerfile
```

-	Layers:
	-	`sha256:9ea1e6ba191d57b2933c4d03388f6a23b8d2b5e5a7fe476d51afcdbf00f53f5c`  
		Last Modified: Thu, 27 Mar 2025 20:53:35 GMT  
		Size: 2.3 MB (2286432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd31371d2f6db2ac800c33bd000734380c9ac8a14aca23e7c2d17ef259810eba`  
		Last Modified: Thu, 27 Mar 2025 20:53:34 GMT  
		Size: 22.6 KB (22615 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:0058a46283d5026f6e6d46d9f8bf0bc5007eefa0fb50ba124a8d9c5c8718c92a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32751201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3b77978b5a8fc2eac21e1b870c55c85b4c6184d63d4ebf29b6e8f154e6af6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1742169600'
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
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
	-	`sha256:40897f2d64cafc6fcb222667c78c37539448596456ecffd3f8ce7cb9b5cabb28`  
		Last Modified: Thu, 27 Mar 2025 20:57:34 GMT  
		Size: 2.3 MB (2317020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82dc27b022eac657403b67589f084f87ad57c6f2891889c6d34ebb4474ee310`  
		Last Modified: Thu, 27 Mar 2025 20:57:34 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e60fc6582e411940064800863c4b87c02105118e0ab5e9648ba1dc12ad8f61`  
		Last Modified: Thu, 27 Mar 2025 20:57:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f4049ead4762d06719ad4fdd2ae2b4f0046a130d2891e2ade50695d33f6d10f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 KB (22569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ba92a7b7f909a167a9bf4e5b91ff175e39f2e162a4f1e6ccf92f49c51b6006`

```dockerfile
```

-	Layers:
	-	`sha256:a8aaf8662d9c73787c7977bf75670f2471e3dd62e02f2103193777209066ad7e`  
		Last Modified: Thu, 27 Mar 2025 20:57:33 GMT  
		Size: 22.6 KB (22569 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:7a7bb97c6c61dd3b4c61f8065dab499bbdfe7cfbe4cb956effa9edcb2e66af3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37176878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc98e5d5a70cd46d1686601994b63dc20ca2175f52c40dba598b762926e2a37c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
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
	-	`sha256:253d36c80692194d710c838a9dcf641b5f4e5b708caf7a0167a65231d784da21`  
		Last Modified: Thu, 27 Mar 2025 20:52:14 GMT  
		Size: 2.4 MB (2418931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815dd2a928bdc05f75187e8f6ea5d86523616fee3840ca9163dbf320a5a6ccc7`  
		Last Modified: Thu, 27 Mar 2025 20:52:13 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121efc6039ff41bfa98a9b47bcf4885d5e03c9456814d0361df3e771d123d137`  
		Last Modified: Thu, 27 Mar 2025 20:52:13 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:d58f5f6a5ac867f60ce3aadad1e9917e3c03c7abb83b35be66d9f4cdcd7be38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2316452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8bcaaed8fc07c31e2e028ca1bc38f788ad0afe190b58e4ba7e054fcb4f4340`

```dockerfile
```

-	Layers:
	-	`sha256:27246f4bfd4ab676df1caa36848b296c12c320d9fc5d0b12540a193755ca7353`  
		Last Modified: Thu, 27 Mar 2025 20:52:14 GMT  
		Size: 2.3 MB (2293705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd9de6d66fe54e520712184227e13e9b50f4e82e578f5812610dd60205ae9f61`  
		Last Modified: Thu, 27 Mar 2025 20:52:13 GMT  
		Size: 22.7 KB (22747 bytes)  
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
$ docker pull memcached@sha256:56725c927f12a53093b0dd8a58ddd8df3d020b46567cb14a8e0201279b97a79e
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
$ docker pull memcached@sha256:c1130e43766e72579b0bb3de4a483b13617fc482b7a3f660833032ddd3df46ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33000858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d4e3512a87fc3884351cf771b57d83866a516c78d3313b209064b6257c17b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14ee0758901af029fd1a78a75a39cef72470aa2c4538747549decb8769c9036`  
		Last Modified: Thu, 27 Mar 2025 20:53:08 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a603c9ce7da5d29d874ef3f48909ac8d815642ee1161fb1088c5c79590059ded`  
		Last Modified: Thu, 27 Mar 2025 20:53:09 GMT  
		Size: 2.5 MB (2491772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6080c85c433088b18ef903a680b49c4c60d2cdf59b8653368bec12dbef863d54`  
		Last Modified: Thu, 27 Mar 2025 20:53:08 GMT  
		Size: 2.3 MB (2302705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b725e8c43056a4da24ef0710ac4716517b27c4ffd092842d38289d6efbb7ab25`  
		Last Modified: Thu, 27 Mar 2025 20:53:08 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfffb76f39255069f9125012bc7bc79eeaeb3f9c248ef8f35de284adafd60312`  
		Last Modified: Thu, 27 Mar 2025 20:53:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38` - unknown; unknown

```console
$ docker pull memcached@sha256:e6c4e9ea0da3ea8f19a3d9280c07e1908364c8c40779cbb2d4f65feaee440615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2312005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4242aa375d1ecdacb2c396dac8135d5aa9caf7db2374a6216f2ad87e3cf05d`

```dockerfile
```

-	Layers:
	-	`sha256:5049b68d7e40887d89a570516aa826f3c1401d51538fa705eefa45144e8da58e`  
		Last Modified: Thu, 27 Mar 2025 20:53:08 GMT  
		Size: 2.3 MB (2289333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7273a520dbd5019d2de56854018a19f4479f6eceba42c52a77dfb5716bfd57c3`  
		Last Modified: Thu, 27 Mar 2025 20:53:08 GMT  
		Size: 22.7 KB (22672 bytes)  
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
$ docker pull memcached@sha256:c014ab323b1b4bcbb3166beafd41410dbddfbb1a0a6f19deb69e802762874555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32689553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f119d1180b3eca14d9a554f5a3a4e962d438c72c8e71c607ef6688353aa74e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
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
	-	`sha256:c583561c73b24d79d3cb55803558b6f1e508bb37288ee1635b47bdf9a51a38da`  
		Last Modified: Thu, 27 Mar 2025 20:54:02 GMT  
		Size: 2.3 MB (2288694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e039a4f24583d1fa81e89c1a686785aff6e7a269cafcb224a2b61b3d05c6f0ea`  
		Last Modified: Thu, 27 Mar 2025 20:54:01 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aad33c6fcc162e8b1413e31976faafcba7edc16db7e020bc51a9b57c5ecf490`  
		Last Modified: Thu, 27 Mar 2025 20:54:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38` - unknown; unknown

```console
$ docker pull memcached@sha256:73ecf1ebde9749379f2fba28e4e4ba518b5d4943a699ee9745cb9e89f423cb4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2312518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6766598d442fb4e939fe0f028c923ef5ed6b6766633eb2f01669a27a672232`

```dockerfile
```

-	Layers:
	-	`sha256:e93a26c0b4c7baf66130df39a4ea1e3fe6f1767bc12f5ef6698589251a6b6d58`  
		Last Modified: Thu, 27 Mar 2025 20:54:02 GMT  
		Size: 2.3 MB (2289648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5f2e6a18098b4d97813a7772aa4e2bf79a1f45eedbe86caf481cb1840fa9586`  
		Last Modified: Thu, 27 Mar 2025 20:54:01 GMT  
		Size: 22.9 KB (22870 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38` - linux; 386

```console
$ docker pull memcached@sha256:a5ea0c0aa510a293159050b633c507887a11ebcdc5abb316a7154fcd83ff32c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33943021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfaa7026b44f46e71ba9c44a1481824fdcf9b54f5047b75c26c8710944a5475c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bd5b700a5532cf1e91c064d6ed472b6c511c3d9e9b08a7f31f608192b9afad`  
		Last Modified: Thu, 27 Mar 2025 20:53:34 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c7d8b538dbde73a9a5e3e42f1a04a0fd79356f7f702038a5b159b503cfc1e5`  
		Last Modified: Thu, 27 Mar 2025 20:53:35 GMT  
		Size: 2.5 MB (2500728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7542439206b95728641ceb4b680180a73442cabd6b41fe578628f18b945a9e2a`  
		Last Modified: Thu, 27 Mar 2025 20:53:35 GMT  
		Size: 2.3 MB (2251248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a46d28f72d87befc244136b60a9c42a9b18e552434f284c5687e64805032464`  
		Last Modified: Thu, 27 Mar 2025 20:53:34 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42201d898a9285374141b63bacd52743d268d2f3d800b22b5ee94e5e553fbf8`  
		Last Modified: Thu, 27 Mar 2025 20:53:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38` - unknown; unknown

```console
$ docker pull memcached@sha256:3972e3e9979c0f37a3396a5d86757d1c64ff1661a01486faa24077f6cc9ea8a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2309047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa4d34e6df623288ed6ec9f921a2605e855bfe7736d69fc81466b9e9b903ae7`

```dockerfile
```

-	Layers:
	-	`sha256:9ea1e6ba191d57b2933c4d03388f6a23b8d2b5e5a7fe476d51afcdbf00f53f5c`  
		Last Modified: Thu, 27 Mar 2025 20:53:35 GMT  
		Size: 2.3 MB (2286432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd31371d2f6db2ac800c33bd000734380c9ac8a14aca23e7c2d17ef259810eba`  
		Last Modified: Thu, 27 Mar 2025 20:53:34 GMT  
		Size: 22.6 KB (22615 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38` - linux; mips64le

```console
$ docker pull memcached@sha256:0058a46283d5026f6e6d46d9f8bf0bc5007eefa0fb50ba124a8d9c5c8718c92a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32751201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3b77978b5a8fc2eac21e1b870c55c85b4c6184d63d4ebf29b6e8f154e6af6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1742169600'
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
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
	-	`sha256:40897f2d64cafc6fcb222667c78c37539448596456ecffd3f8ce7cb9b5cabb28`  
		Last Modified: Thu, 27 Mar 2025 20:57:34 GMT  
		Size: 2.3 MB (2317020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82dc27b022eac657403b67589f084f87ad57c6f2891889c6d34ebb4474ee310`  
		Last Modified: Thu, 27 Mar 2025 20:57:34 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e60fc6582e411940064800863c4b87c02105118e0ab5e9648ba1dc12ad8f61`  
		Last Modified: Thu, 27 Mar 2025 20:57:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38` - unknown; unknown

```console
$ docker pull memcached@sha256:f4049ead4762d06719ad4fdd2ae2b4f0046a130d2891e2ade50695d33f6d10f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 KB (22569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ba92a7b7f909a167a9bf4e5b91ff175e39f2e162a4f1e6ccf92f49c51b6006`

```dockerfile
```

-	Layers:
	-	`sha256:a8aaf8662d9c73787c7977bf75670f2471e3dd62e02f2103193777209066ad7e`  
		Last Modified: Thu, 27 Mar 2025 20:57:33 GMT  
		Size: 22.6 KB (22569 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38` - linux; ppc64le

```console
$ docker pull memcached@sha256:7a7bb97c6c61dd3b4c61f8065dab499bbdfe7cfbe4cb956effa9edcb2e66af3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37176878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc98e5d5a70cd46d1686601994b63dc20ca2175f52c40dba598b762926e2a37c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
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
	-	`sha256:253d36c80692194d710c838a9dcf641b5f4e5b708caf7a0167a65231d784da21`  
		Last Modified: Thu, 27 Mar 2025 20:52:14 GMT  
		Size: 2.4 MB (2418931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815dd2a928bdc05f75187e8f6ea5d86523616fee3840ca9163dbf320a5a6ccc7`  
		Last Modified: Thu, 27 Mar 2025 20:52:13 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121efc6039ff41bfa98a9b47bcf4885d5e03c9456814d0361df3e771d123d137`  
		Last Modified: Thu, 27 Mar 2025 20:52:13 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38` - unknown; unknown

```console
$ docker pull memcached@sha256:d58f5f6a5ac867f60ce3aadad1e9917e3c03c7abb83b35be66d9f4cdcd7be38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2316452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8bcaaed8fc07c31e2e028ca1bc38f788ad0afe190b58e4ba7e054fcb4f4340`

```dockerfile
```

-	Layers:
	-	`sha256:27246f4bfd4ab676df1caa36848b296c12c320d9fc5d0b12540a193755ca7353`  
		Last Modified: Thu, 27 Mar 2025 20:52:14 GMT  
		Size: 2.3 MB (2293705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd9de6d66fe54e520712184227e13e9b50f4e82e578f5812610dd60205ae9f61`  
		Last Modified: Thu, 27 Mar 2025 20:52:13 GMT  
		Size: 22.7 KB (22747 bytes)  
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
$ docker pull memcached@sha256:709ca82c737ee52acc94da9623ba812e9117074d754b5aa2060faae09e9cae75
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
$ docker pull memcached@sha256:06c629488bcbeeb5ce4b3701748928d93d1b32778a0e729fdc3a5374eaba4571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5746566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56bdd3e4a7232079ba7497e7a5fdc7995c9742cc777c57d4cc6b78f91ec073c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1341251c0a26b782fc5ad7d13973a828fa117452636a63d4ae201b1667af32`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66a1cc00f297101211a7a048e61e1072370d39ecac768421aadccc8eeb63886`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 104.7 KB (104693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e764e8e2bff857e5ff55376c244229b37704bf0d8907bba88555f37e409981d2`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 2.0 MB (1998269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278163aab69155dd6749e516fd5aa7ac1c8804dbd96615b6c6c5d084adbeaed6`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35d8ffb74c551d7cdd9c1a838d885466c863663bc11ba5866e2cdcc14da5b13`  
		Last Modified: Thu, 27 Mar 2025 20:53:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7c8fdb5dcff76dd27e53ba9cb1682214360b3787e9758840a7f8e0e9e7f3cc15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66b46bea0468821817967032976045f8680b204a6277a76ab860a1b6f9125db2`

```dockerfile
```

-	Layers:
	-	`sha256:6f3203e9b8cd79a8f7763cd6e69146dad76bc1c77e3d2302caba89a423037bf9`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 93.6 KB (93633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac63a4f8a3074e4d23c3c8a1a59305cec2e5d28d1b025df6d1540b8f73174ff8`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 21.2 KB (21159 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:684f5401f5f644171126d516de1ebdcb1608433972008bb421508aa7c3abb1b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6104612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb60fe52ab38f8d170995e48747f784b5d30f72cc8cc5ecde8a2a3f789435bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
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
	-	`sha256:abb28ae90c9bffea35355aef624a2e35ecaedd538b0bbc177e52734d7ab3dcd2`  
		Last Modified: Thu, 27 Mar 2025 20:57:10 GMT  
		Size: 2.0 MB (1989460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9471b9190bd21604219c213d28e742bdd010051f6ea84ecd6723e7eb9e0bf7`  
		Last Modified: Thu, 27 Mar 2025 20:57:09 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189f409c92e6a19050d616acb8da97bddfff5c598fc3903ceb7141c91235d6fa`  
		Last Modified: Thu, 27 Mar 2025 20:57:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:707fc3a048ec6345dc3f8828ff0cb13627f8437236439a243de930cd586e9138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d75d4d1d6177f5310b1a617d8a643092097f96d6253e7c98c69bc61d853505`

```dockerfile
```

-	Layers:
	-	`sha256:1d113af0ec580fd3c52e1675b66ffd5453996b0f564448dcf9f231c02192c184`  
		Last Modified: Thu, 27 Mar 2025 20:57:09 GMT  
		Size: 93.7 KB (93737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48139650f70b212083be85e732df16032edcc486b3af2dfbac099741fef6bb2`  
		Last Modified: Thu, 27 Mar 2025 20:57:09 GMT  
		Size: 21.4 KB (21356 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-alpine` - linux; 386

```console
$ docker pull memcached@sha256:b40fc687669e8c2d9dbac25e1f627e5c27ce30d1636b0ae32ea8b0d3d2c56ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5534238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8c8e64a825b2c7e4c88e1ca4d0a45305c37b4b3308e819dab16a852e47d2719`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e2f92344d79ef7f1ba0a143585705ed78f249d82bceb677069e5373b3edea9`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae03b6003c1510a2c1bc31c06714cf492ff9ae437f9cbe1d835bc1b3afa95a4`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 109.5 KB (109484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f729c997aa8639d7314cd6b15d0d678628e45bdf485953f69cb89966d078795`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 2.0 MB (1959776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e488a63a3c8d2aa14b4ef7c3c0e563ff99ba11a36b602ce7c81a499f598efcd`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363743b6d219afcbcc9cd8037d51201784e1b3c1605e5c5b6c85d42fa3315788`  
		Last Modified: Thu, 27 Mar 2025 20:53:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:27084cf0d56fdead95f5789352b216da11bb2798a6fcffd9f41125c2ecdf95ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 KB (114689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df8ec4074a13a2d084b6c2da617b85afac8f4a5bc80ec144bc81dd04e752e45`

```dockerfile
```

-	Layers:
	-	`sha256:0d2eb1fe2f7200332e0f72a04f10ec6a9355c72a25b95ff6dbc26dc84c428ede`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 93.6 KB (93588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40259002d91f5318e16c29fd221af80ba97f7a89b92d761a067cc1ed95270a5e`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 21.1 KB (21101 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:e983630451e7d57a7ced6bd4a893c9903a2b50ae487efa4f0b8f5b298f6cfa34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5791362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c9ba664c418a4c21c59a935f8b35644fe1d17ea0fd99f693645818d7097b6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
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
	-	`sha256:427e1b046fb9f579d4b7879a999d743f20bd21eb9f7ec3aa8e98c5dff5fa7ce2`  
		Last Modified: Thu, 27 Mar 2025 20:55:24 GMT  
		Size: 2.1 MB (2091383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661f0560043b5762cdfe652be7c75103b960f325ddf9c7d39079e1ef5da44730`  
		Last Modified: Thu, 27 Mar 2025 20:55:23 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976e19956b9f2e61552a8a71907b18fc974d41b5ee50b5f0b422469c6811e306`  
		Last Modified: Thu, 27 Mar 2025 20:55:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9fb4e7ab3a251a8a5ebaa9bea164dbe4d2fda72570c279440c9d95f5f26bcb67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 KB (112972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a413dea3279278472afb6eadef6effca79012a2f955eaf5fa39a5d410c111373`

```dockerfile
```

-	Layers:
	-	`sha256:c222b8b6f12483b61f4c3e3738172861210af0947bb823a874b4bdbfc72770aa`  
		Last Modified: Thu, 27 Mar 2025 20:55:23 GMT  
		Size: 91.7 KB (91740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc826d89b23d4bd8b0c27863fbedc9e2474d48194575f8e5f4eaa3ec7db78ecf`  
		Last Modified: Thu, 27 Mar 2025 20:55:23 GMT  
		Size: 21.2 KB (21232 bytes)  
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
$ docker pull memcached@sha256:709ca82c737ee52acc94da9623ba812e9117074d754b5aa2060faae09e9cae75
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
$ docker pull memcached@sha256:06c629488bcbeeb5ce4b3701748928d93d1b32778a0e729fdc3a5374eaba4571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5746566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56bdd3e4a7232079ba7497e7a5fdc7995c9742cc777c57d4cc6b78f91ec073c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1341251c0a26b782fc5ad7d13973a828fa117452636a63d4ae201b1667af32`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66a1cc00f297101211a7a048e61e1072370d39ecac768421aadccc8eeb63886`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 104.7 KB (104693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e764e8e2bff857e5ff55376c244229b37704bf0d8907bba88555f37e409981d2`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 2.0 MB (1998269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278163aab69155dd6749e516fd5aa7ac1c8804dbd96615b6c6c5d084adbeaed6`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35d8ffb74c551d7cdd9c1a838d885466c863663bc11ba5866e2cdcc14da5b13`  
		Last Modified: Thu, 27 Mar 2025 20:53:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:7c8fdb5dcff76dd27e53ba9cb1682214360b3787e9758840a7f8e0e9e7f3cc15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66b46bea0468821817967032976045f8680b204a6277a76ab860a1b6f9125db2`

```dockerfile
```

-	Layers:
	-	`sha256:6f3203e9b8cd79a8f7763cd6e69146dad76bc1c77e3d2302caba89a423037bf9`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 93.6 KB (93633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac63a4f8a3074e4d23c3c8a1a59305cec2e5d28d1b025df6d1540b8f73174ff8`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 21.2 KB (21159 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:684f5401f5f644171126d516de1ebdcb1608433972008bb421508aa7c3abb1b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6104612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb60fe52ab38f8d170995e48747f784b5d30f72cc8cc5ecde8a2a3f789435bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
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
	-	`sha256:abb28ae90c9bffea35355aef624a2e35ecaedd538b0bbc177e52734d7ab3dcd2`  
		Last Modified: Thu, 27 Mar 2025 20:57:10 GMT  
		Size: 2.0 MB (1989460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9471b9190bd21604219c213d28e742bdd010051f6ea84ecd6723e7eb9e0bf7`  
		Last Modified: Thu, 27 Mar 2025 20:57:09 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189f409c92e6a19050d616acb8da97bddfff5c598fc3903ceb7141c91235d6fa`  
		Last Modified: Thu, 27 Mar 2025 20:57:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:707fc3a048ec6345dc3f8828ff0cb13627f8437236439a243de930cd586e9138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d75d4d1d6177f5310b1a617d8a643092097f96d6253e7c98c69bc61d853505`

```dockerfile
```

-	Layers:
	-	`sha256:1d113af0ec580fd3c52e1675b66ffd5453996b0f564448dcf9f231c02192c184`  
		Last Modified: Thu, 27 Mar 2025 20:57:09 GMT  
		Size: 93.7 KB (93737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48139650f70b212083be85e732df16032edcc486b3af2dfbac099741fef6bb2`  
		Last Modified: Thu, 27 Mar 2025 20:57:09 GMT  
		Size: 21.4 KB (21356 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-alpine3.21` - linux; 386

```console
$ docker pull memcached@sha256:b40fc687669e8c2d9dbac25e1f627e5c27ce30d1636b0ae32ea8b0d3d2c56ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5534238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8c8e64a825b2c7e4c88e1ca4d0a45305c37b4b3308e819dab16a852e47d2719`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e2f92344d79ef7f1ba0a143585705ed78f249d82bceb677069e5373b3edea9`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae03b6003c1510a2c1bc31c06714cf492ff9ae437f9cbe1d835bc1b3afa95a4`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 109.5 KB (109484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f729c997aa8639d7314cd6b15d0d678628e45bdf485953f69cb89966d078795`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 2.0 MB (1959776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e488a63a3c8d2aa14b4ef7c3c0e563ff99ba11a36b602ce7c81a499f598efcd`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363743b6d219afcbcc9cd8037d51201784e1b3c1605e5c5b6c85d42fa3315788`  
		Last Modified: Thu, 27 Mar 2025 20:53:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:27084cf0d56fdead95f5789352b216da11bb2798a6fcffd9f41125c2ecdf95ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 KB (114689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df8ec4074a13a2d084b6c2da617b85afac8f4a5bc80ec144bc81dd04e752e45`

```dockerfile
```

-	Layers:
	-	`sha256:0d2eb1fe2f7200332e0f72a04f10ec6a9355c72a25b95ff6dbc26dc84c428ede`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 93.6 KB (93588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40259002d91f5318e16c29fd221af80ba97f7a89b92d761a067cc1ed95270a5e`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 21.1 KB (21101 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-alpine3.21` - linux; ppc64le

```console
$ docker pull memcached@sha256:e983630451e7d57a7ced6bd4a893c9903a2b50ae487efa4f0b8f5b298f6cfa34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5791362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c9ba664c418a4c21c59a935f8b35644fe1d17ea0fd99f693645818d7097b6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
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
	-	`sha256:427e1b046fb9f579d4b7879a999d743f20bd21eb9f7ec3aa8e98c5dff5fa7ce2`  
		Last Modified: Thu, 27 Mar 2025 20:55:24 GMT  
		Size: 2.1 MB (2091383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661f0560043b5762cdfe652be7c75103b960f325ddf9c7d39079e1ef5da44730`  
		Last Modified: Thu, 27 Mar 2025 20:55:23 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976e19956b9f2e61552a8a71907b18fc974d41b5ee50b5f0b422469c6811e306`  
		Last Modified: Thu, 27 Mar 2025 20:55:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:9fb4e7ab3a251a8a5ebaa9bea164dbe4d2fda72570c279440c9d95f5f26bcb67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 KB (112972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a413dea3279278472afb6eadef6effca79012a2f955eaf5fa39a5d410c111373`

```dockerfile
```

-	Layers:
	-	`sha256:c222b8b6f12483b61f4c3e3738172861210af0947bb823a874b4bdbfc72770aa`  
		Last Modified: Thu, 27 Mar 2025 20:55:23 GMT  
		Size: 91.7 KB (91740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc826d89b23d4bd8b0c27863fbedc9e2474d48194575f8e5f4eaa3ec7db78ecf`  
		Last Modified: Thu, 27 Mar 2025 20:55:23 GMT  
		Size: 21.2 KB (21232 bytes)  
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
$ docker pull memcached@sha256:56725c927f12a53093b0dd8a58ddd8df3d020b46567cb14a8e0201279b97a79e
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
$ docker pull memcached@sha256:c1130e43766e72579b0bb3de4a483b13617fc482b7a3f660833032ddd3df46ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33000858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d4e3512a87fc3884351cf771b57d83866a516c78d3313b209064b6257c17b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14ee0758901af029fd1a78a75a39cef72470aa2c4538747549decb8769c9036`  
		Last Modified: Thu, 27 Mar 2025 20:53:08 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a603c9ce7da5d29d874ef3f48909ac8d815642ee1161fb1088c5c79590059ded`  
		Last Modified: Thu, 27 Mar 2025 20:53:09 GMT  
		Size: 2.5 MB (2491772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6080c85c433088b18ef903a680b49c4c60d2cdf59b8653368bec12dbef863d54`  
		Last Modified: Thu, 27 Mar 2025 20:53:08 GMT  
		Size: 2.3 MB (2302705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b725e8c43056a4da24ef0710ac4716517b27c4ffd092842d38289d6efbb7ab25`  
		Last Modified: Thu, 27 Mar 2025 20:53:08 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfffb76f39255069f9125012bc7bc79eeaeb3f9c248ef8f35de284adafd60312`  
		Last Modified: Thu, 27 Mar 2025 20:53:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:e6c4e9ea0da3ea8f19a3d9280c07e1908364c8c40779cbb2d4f65feaee440615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2312005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4242aa375d1ecdacb2c396dac8135d5aa9caf7db2374a6216f2ad87e3cf05d`

```dockerfile
```

-	Layers:
	-	`sha256:5049b68d7e40887d89a570516aa826f3c1401d51538fa705eefa45144e8da58e`  
		Last Modified: Thu, 27 Mar 2025 20:53:08 GMT  
		Size: 2.3 MB (2289333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7273a520dbd5019d2de56854018a19f4479f6eceba42c52a77dfb5716bfd57c3`  
		Last Modified: Thu, 27 Mar 2025 20:53:08 GMT  
		Size: 22.7 KB (22672 bytes)  
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
$ docker pull memcached@sha256:c014ab323b1b4bcbb3166beafd41410dbddfbb1a0a6f19deb69e802762874555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32689553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f119d1180b3eca14d9a554f5a3a4e962d438c72c8e71c607ef6688353aa74e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
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
	-	`sha256:c583561c73b24d79d3cb55803558b6f1e508bb37288ee1635b47bdf9a51a38da`  
		Last Modified: Thu, 27 Mar 2025 20:54:02 GMT  
		Size: 2.3 MB (2288694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e039a4f24583d1fa81e89c1a686785aff6e7a269cafcb224a2b61b3d05c6f0ea`  
		Last Modified: Thu, 27 Mar 2025 20:54:01 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aad33c6fcc162e8b1413e31976faafcba7edc16db7e020bc51a9b57c5ecf490`  
		Last Modified: Thu, 27 Mar 2025 20:54:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:73ecf1ebde9749379f2fba28e4e4ba518b5d4943a699ee9745cb9e89f423cb4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2312518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6766598d442fb4e939fe0f028c923ef5ed6b6766633eb2f01669a27a672232`

```dockerfile
```

-	Layers:
	-	`sha256:e93a26c0b4c7baf66130df39a4ea1e3fe6f1767bc12f5ef6698589251a6b6d58`  
		Last Modified: Thu, 27 Mar 2025 20:54:02 GMT  
		Size: 2.3 MB (2289648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5f2e6a18098b4d97813a7772aa4e2bf79a1f45eedbe86caf481cb1840fa9586`  
		Last Modified: Thu, 27 Mar 2025 20:54:01 GMT  
		Size: 22.9 KB (22870 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:a5ea0c0aa510a293159050b633c507887a11ebcdc5abb316a7154fcd83ff32c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33943021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfaa7026b44f46e71ba9c44a1481824fdcf9b54f5047b75c26c8710944a5475c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bd5b700a5532cf1e91c064d6ed472b6c511c3d9e9b08a7f31f608192b9afad`  
		Last Modified: Thu, 27 Mar 2025 20:53:34 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c7d8b538dbde73a9a5e3e42f1a04a0fd79356f7f702038a5b159b503cfc1e5`  
		Last Modified: Thu, 27 Mar 2025 20:53:35 GMT  
		Size: 2.5 MB (2500728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7542439206b95728641ceb4b680180a73442cabd6b41fe578628f18b945a9e2a`  
		Last Modified: Thu, 27 Mar 2025 20:53:35 GMT  
		Size: 2.3 MB (2251248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a46d28f72d87befc244136b60a9c42a9b18e552434f284c5687e64805032464`  
		Last Modified: Thu, 27 Mar 2025 20:53:34 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42201d898a9285374141b63bacd52743d268d2f3d800b22b5ee94e5e553fbf8`  
		Last Modified: Thu, 27 Mar 2025 20:53:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:3972e3e9979c0f37a3396a5d86757d1c64ff1661a01486faa24077f6cc9ea8a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2309047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa4d34e6df623288ed6ec9f921a2605e855bfe7736d69fc81466b9e9b903ae7`

```dockerfile
```

-	Layers:
	-	`sha256:9ea1e6ba191d57b2933c4d03388f6a23b8d2b5e5a7fe476d51afcdbf00f53f5c`  
		Last Modified: Thu, 27 Mar 2025 20:53:35 GMT  
		Size: 2.3 MB (2286432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd31371d2f6db2ac800c33bd000734380c9ac8a14aca23e7c2d17ef259810eba`  
		Last Modified: Thu, 27 Mar 2025 20:53:34 GMT  
		Size: 22.6 KB (22615 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:0058a46283d5026f6e6d46d9f8bf0bc5007eefa0fb50ba124a8d9c5c8718c92a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32751201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3b77978b5a8fc2eac21e1b870c55c85b4c6184d63d4ebf29b6e8f154e6af6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1742169600'
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
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
	-	`sha256:40897f2d64cafc6fcb222667c78c37539448596456ecffd3f8ce7cb9b5cabb28`  
		Last Modified: Thu, 27 Mar 2025 20:57:34 GMT  
		Size: 2.3 MB (2317020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82dc27b022eac657403b67589f084f87ad57c6f2891889c6d34ebb4474ee310`  
		Last Modified: Thu, 27 Mar 2025 20:57:34 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e60fc6582e411940064800863c4b87c02105118e0ab5e9648ba1dc12ad8f61`  
		Last Modified: Thu, 27 Mar 2025 20:57:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f4049ead4762d06719ad4fdd2ae2b4f0046a130d2891e2ade50695d33f6d10f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 KB (22569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ba92a7b7f909a167a9bf4e5b91ff175e39f2e162a4f1e6ccf92f49c51b6006`

```dockerfile
```

-	Layers:
	-	`sha256:a8aaf8662d9c73787c7977bf75670f2471e3dd62e02f2103193777209066ad7e`  
		Last Modified: Thu, 27 Mar 2025 20:57:33 GMT  
		Size: 22.6 KB (22569 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:7a7bb97c6c61dd3b4c61f8065dab499bbdfe7cfbe4cb956effa9edcb2e66af3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37176878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc98e5d5a70cd46d1686601994b63dc20ca2175f52c40dba598b762926e2a37c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
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
	-	`sha256:253d36c80692194d710c838a9dcf641b5f4e5b708caf7a0167a65231d784da21`  
		Last Modified: Thu, 27 Mar 2025 20:52:14 GMT  
		Size: 2.4 MB (2418931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815dd2a928bdc05f75187e8f6ea5d86523616fee3840ca9163dbf320a5a6ccc7`  
		Last Modified: Thu, 27 Mar 2025 20:52:13 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121efc6039ff41bfa98a9b47bcf4885d5e03c9456814d0361df3e771d123d137`  
		Last Modified: Thu, 27 Mar 2025 20:52:13 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:d58f5f6a5ac867f60ce3aadad1e9917e3c03c7abb83b35be66d9f4cdcd7be38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2316452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8bcaaed8fc07c31e2e028ca1bc38f788ad0afe190b58e4ba7e054fcb4f4340`

```dockerfile
```

-	Layers:
	-	`sha256:27246f4bfd4ab676df1caa36848b296c12c320d9fc5d0b12540a193755ca7353`  
		Last Modified: Thu, 27 Mar 2025 20:52:14 GMT  
		Size: 2.3 MB (2293705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd9de6d66fe54e520712184227e13e9b50f4e82e578f5812610dd60205ae9f61`  
		Last Modified: Thu, 27 Mar 2025 20:52:13 GMT  
		Size: 22.7 KB (22747 bytes)  
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
$ docker pull memcached@sha256:7da5f599a2a094daee0cdc0654ce5188389ee6c7d4b34ded97d4b8177ec3ee89
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
$ docker pull memcached@sha256:06c629488bcbeeb5ce4b3701748928d93d1b32778a0e729fdc3a5374eaba4571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5746566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56bdd3e4a7232079ba7497e7a5fdc7995c9742cc777c57d4cc6b78f91ec073c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1341251c0a26b782fc5ad7d13973a828fa117452636a63d4ae201b1667af32`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66a1cc00f297101211a7a048e61e1072370d39ecac768421aadccc8eeb63886`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 104.7 KB (104693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e764e8e2bff857e5ff55376c244229b37704bf0d8907bba88555f37e409981d2`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 2.0 MB (1998269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278163aab69155dd6749e516fd5aa7ac1c8804dbd96615b6c6c5d084adbeaed6`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35d8ffb74c551d7cdd9c1a838d885466c863663bc11ba5866e2cdcc14da5b13`  
		Last Modified: Thu, 27 Mar 2025 20:53:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7c8fdb5dcff76dd27e53ba9cb1682214360b3787e9758840a7f8e0e9e7f3cc15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66b46bea0468821817967032976045f8680b204a6277a76ab860a1b6f9125db2`

```dockerfile
```

-	Layers:
	-	`sha256:6f3203e9b8cd79a8f7763cd6e69146dad76bc1c77e3d2302caba89a423037bf9`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 93.6 KB (93633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac63a4f8a3074e4d23c3c8a1a59305cec2e5d28d1b025df6d1540b8f73174ff8`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 21.2 KB (21159 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:684f5401f5f644171126d516de1ebdcb1608433972008bb421508aa7c3abb1b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6104612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb60fe52ab38f8d170995e48747f784b5d30f72cc8cc5ecde8a2a3f789435bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
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
	-	`sha256:abb28ae90c9bffea35355aef624a2e35ecaedd538b0bbc177e52734d7ab3dcd2`  
		Last Modified: Thu, 27 Mar 2025 20:57:10 GMT  
		Size: 2.0 MB (1989460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9471b9190bd21604219c213d28e742bdd010051f6ea84ecd6723e7eb9e0bf7`  
		Last Modified: Thu, 27 Mar 2025 20:57:09 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189f409c92e6a19050d616acb8da97bddfff5c598fc3903ceb7141c91235d6fa`  
		Last Modified: Thu, 27 Mar 2025 20:57:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:707fc3a048ec6345dc3f8828ff0cb13627f8437236439a243de930cd586e9138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d75d4d1d6177f5310b1a617d8a643092097f96d6253e7c98c69bc61d853505`

```dockerfile
```

-	Layers:
	-	`sha256:1d113af0ec580fd3c52e1675b66ffd5453996b0f564448dcf9f231c02192c184`  
		Last Modified: Thu, 27 Mar 2025 20:57:09 GMT  
		Size: 93.7 KB (93737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48139650f70b212083be85e732df16032edcc486b3af2dfbac099741fef6bb2`  
		Last Modified: Thu, 27 Mar 2025 20:57:09 GMT  
		Size: 21.4 KB (21356 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:b40fc687669e8c2d9dbac25e1f627e5c27ce30d1636b0ae32ea8b0d3d2c56ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5534238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8c8e64a825b2c7e4c88e1ca4d0a45305c37b4b3308e819dab16a852e47d2719`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e2f92344d79ef7f1ba0a143585705ed78f249d82bceb677069e5373b3edea9`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae03b6003c1510a2c1bc31c06714cf492ff9ae437f9cbe1d835bc1b3afa95a4`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 109.5 KB (109484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f729c997aa8639d7314cd6b15d0d678628e45bdf485953f69cb89966d078795`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 2.0 MB (1959776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e488a63a3c8d2aa14b4ef7c3c0e563ff99ba11a36b602ce7c81a499f598efcd`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363743b6d219afcbcc9cd8037d51201784e1b3c1605e5c5b6c85d42fa3315788`  
		Last Modified: Thu, 27 Mar 2025 20:53:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:27084cf0d56fdead95f5789352b216da11bb2798a6fcffd9f41125c2ecdf95ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 KB (114689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df8ec4074a13a2d084b6c2da617b85afac8f4a5bc80ec144bc81dd04e752e45`

```dockerfile
```

-	Layers:
	-	`sha256:0d2eb1fe2f7200332e0f72a04f10ec6a9355c72a25b95ff6dbc26dc84c428ede`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 93.6 KB (93588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40259002d91f5318e16c29fd221af80ba97f7a89b92d761a067cc1ed95270a5e`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 21.1 KB (21101 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:e983630451e7d57a7ced6bd4a893c9903a2b50ae487efa4f0b8f5b298f6cfa34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5791362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c9ba664c418a4c21c59a935f8b35644fe1d17ea0fd99f693645818d7097b6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
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
	-	`sha256:427e1b046fb9f579d4b7879a999d743f20bd21eb9f7ec3aa8e98c5dff5fa7ce2`  
		Last Modified: Thu, 27 Mar 2025 20:55:24 GMT  
		Size: 2.1 MB (2091383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661f0560043b5762cdfe652be7c75103b960f325ddf9c7d39079e1ef5da44730`  
		Last Modified: Thu, 27 Mar 2025 20:55:23 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976e19956b9f2e61552a8a71907b18fc974d41b5ee50b5f0b422469c6811e306`  
		Last Modified: Thu, 27 Mar 2025 20:55:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9fb4e7ab3a251a8a5ebaa9bea164dbe4d2fda72570c279440c9d95f5f26bcb67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 KB (112972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a413dea3279278472afb6eadef6effca79012a2f955eaf5fa39a5d410c111373`

```dockerfile
```

-	Layers:
	-	`sha256:c222b8b6f12483b61f4c3e3738172861210af0947bb823a874b4bdbfc72770aa`  
		Last Modified: Thu, 27 Mar 2025 20:55:23 GMT  
		Size: 91.7 KB (91740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc826d89b23d4bd8b0c27863fbedc9e2474d48194575f8e5f4eaa3ec7db78ecf`  
		Last Modified: Thu, 27 Mar 2025 20:55:23 GMT  
		Size: 21.2 KB (21232 bytes)  
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
$ docker pull memcached@sha256:709ca82c737ee52acc94da9623ba812e9117074d754b5aa2060faae09e9cae75
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
$ docker pull memcached@sha256:06c629488bcbeeb5ce4b3701748928d93d1b32778a0e729fdc3a5374eaba4571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5746566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56bdd3e4a7232079ba7497e7a5fdc7995c9742cc777c57d4cc6b78f91ec073c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1341251c0a26b782fc5ad7d13973a828fa117452636a63d4ae201b1667af32`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66a1cc00f297101211a7a048e61e1072370d39ecac768421aadccc8eeb63886`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 104.7 KB (104693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e764e8e2bff857e5ff55376c244229b37704bf0d8907bba88555f37e409981d2`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 2.0 MB (1998269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278163aab69155dd6749e516fd5aa7ac1c8804dbd96615b6c6c5d084adbeaed6`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35d8ffb74c551d7cdd9c1a838d885466c863663bc11ba5866e2cdcc14da5b13`  
		Last Modified: Thu, 27 Mar 2025 20:53:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:7c8fdb5dcff76dd27e53ba9cb1682214360b3787e9758840a7f8e0e9e7f3cc15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66b46bea0468821817967032976045f8680b204a6277a76ab860a1b6f9125db2`

```dockerfile
```

-	Layers:
	-	`sha256:6f3203e9b8cd79a8f7763cd6e69146dad76bc1c77e3d2302caba89a423037bf9`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 93.6 KB (93633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac63a4f8a3074e4d23c3c8a1a59305cec2e5d28d1b025df6d1540b8f73174ff8`  
		Last Modified: Thu, 27 Mar 2025 20:53:04 GMT  
		Size: 21.2 KB (21159 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:684f5401f5f644171126d516de1ebdcb1608433972008bb421508aa7c3abb1b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6104612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb60fe52ab38f8d170995e48747f784b5d30f72cc8cc5ecde8a2a3f789435bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
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
	-	`sha256:abb28ae90c9bffea35355aef624a2e35ecaedd538b0bbc177e52734d7ab3dcd2`  
		Last Modified: Thu, 27 Mar 2025 20:57:10 GMT  
		Size: 2.0 MB (1989460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9471b9190bd21604219c213d28e742bdd010051f6ea84ecd6723e7eb9e0bf7`  
		Last Modified: Thu, 27 Mar 2025 20:57:09 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189f409c92e6a19050d616acb8da97bddfff5c598fc3903ceb7141c91235d6fa`  
		Last Modified: Thu, 27 Mar 2025 20:57:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:707fc3a048ec6345dc3f8828ff0cb13627f8437236439a243de930cd586e9138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d75d4d1d6177f5310b1a617d8a643092097f96d6253e7c98c69bc61d853505`

```dockerfile
```

-	Layers:
	-	`sha256:1d113af0ec580fd3c52e1675b66ffd5453996b0f564448dcf9f231c02192c184`  
		Last Modified: Thu, 27 Mar 2025 20:57:09 GMT  
		Size: 93.7 KB (93737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48139650f70b212083be85e732df16032edcc486b3af2dfbac099741fef6bb2`  
		Last Modified: Thu, 27 Mar 2025 20:57:09 GMT  
		Size: 21.4 KB (21356 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.21` - linux; 386

```console
$ docker pull memcached@sha256:b40fc687669e8c2d9dbac25e1f627e5c27ce30d1636b0ae32ea8b0d3d2c56ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5534238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8c8e64a825b2c7e4c88e1ca4d0a45305c37b4b3308e819dab16a852e47d2719`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e2f92344d79ef7f1ba0a143585705ed78f249d82bceb677069e5373b3edea9`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae03b6003c1510a2c1bc31c06714cf492ff9ae437f9cbe1d835bc1b3afa95a4`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 109.5 KB (109484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f729c997aa8639d7314cd6b15d0d678628e45bdf485953f69cb89966d078795`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 2.0 MB (1959776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e488a63a3c8d2aa14b4ef7c3c0e563ff99ba11a36b602ce7c81a499f598efcd`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363743b6d219afcbcc9cd8037d51201784e1b3c1605e5c5b6c85d42fa3315788`  
		Last Modified: Thu, 27 Mar 2025 20:53:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:27084cf0d56fdead95f5789352b216da11bb2798a6fcffd9f41125c2ecdf95ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 KB (114689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df8ec4074a13a2d084b6c2da617b85afac8f4a5bc80ec144bc81dd04e752e45`

```dockerfile
```

-	Layers:
	-	`sha256:0d2eb1fe2f7200332e0f72a04f10ec6a9355c72a25b95ff6dbc26dc84c428ede`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 93.6 KB (93588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40259002d91f5318e16c29fd221af80ba97f7a89b92d761a067cc1ed95270a5e`  
		Last Modified: Thu, 27 Mar 2025 20:53:36 GMT  
		Size: 21.1 KB (21101 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.21` - linux; ppc64le

```console
$ docker pull memcached@sha256:e983630451e7d57a7ced6bd4a893c9903a2b50ae487efa4f0b8f5b298f6cfa34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5791362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c9ba664c418a4c21c59a935f8b35644fe1d17ea0fd99f693645818d7097b6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
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
	-	`sha256:427e1b046fb9f579d4b7879a999d743f20bd21eb9f7ec3aa8e98c5dff5fa7ce2`  
		Last Modified: Thu, 27 Mar 2025 20:55:24 GMT  
		Size: 2.1 MB (2091383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661f0560043b5762cdfe652be7c75103b960f325ddf9c7d39079e1ef5da44730`  
		Last Modified: Thu, 27 Mar 2025 20:55:23 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976e19956b9f2e61552a8a71907b18fc974d41b5ee50b5f0b422469c6811e306`  
		Last Modified: Thu, 27 Mar 2025 20:55:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:9fb4e7ab3a251a8a5ebaa9bea164dbe4d2fda72570c279440c9d95f5f26bcb67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 KB (112972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a413dea3279278472afb6eadef6effca79012a2f955eaf5fa39a5d410c111373`

```dockerfile
```

-	Layers:
	-	`sha256:c222b8b6f12483b61f4c3e3738172861210af0947bb823a874b4bdbfc72770aa`  
		Last Modified: Thu, 27 Mar 2025 20:55:23 GMT  
		Size: 91.7 KB (91740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc826d89b23d4bd8b0c27863fbedc9e2474d48194575f8e5f4eaa3ec7db78ecf`  
		Last Modified: Thu, 27 Mar 2025 20:55:23 GMT  
		Size: 21.2 KB (21232 bytes)  
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
$ docker pull memcached@sha256:56725c927f12a53093b0dd8a58ddd8df3d020b46567cb14a8e0201279b97a79e
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
$ docker pull memcached@sha256:c1130e43766e72579b0bb3de4a483b13617fc482b7a3f660833032ddd3df46ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33000858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d4e3512a87fc3884351cf771b57d83866a516c78d3313b209064b6257c17b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14ee0758901af029fd1a78a75a39cef72470aa2c4538747549decb8769c9036`  
		Last Modified: Thu, 27 Mar 2025 20:53:08 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a603c9ce7da5d29d874ef3f48909ac8d815642ee1161fb1088c5c79590059ded`  
		Last Modified: Thu, 27 Mar 2025 20:53:09 GMT  
		Size: 2.5 MB (2491772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6080c85c433088b18ef903a680b49c4c60d2cdf59b8653368bec12dbef863d54`  
		Last Modified: Thu, 27 Mar 2025 20:53:08 GMT  
		Size: 2.3 MB (2302705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b725e8c43056a4da24ef0710ac4716517b27c4ffd092842d38289d6efbb7ab25`  
		Last Modified: Thu, 27 Mar 2025 20:53:08 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfffb76f39255069f9125012bc7bc79eeaeb3f9c248ef8f35de284adafd60312`  
		Last Modified: Thu, 27 Mar 2025 20:53:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:e6c4e9ea0da3ea8f19a3d9280c07e1908364c8c40779cbb2d4f65feaee440615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2312005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4242aa375d1ecdacb2c396dac8135d5aa9caf7db2374a6216f2ad87e3cf05d`

```dockerfile
```

-	Layers:
	-	`sha256:5049b68d7e40887d89a570516aa826f3c1401d51538fa705eefa45144e8da58e`  
		Last Modified: Thu, 27 Mar 2025 20:53:08 GMT  
		Size: 2.3 MB (2289333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7273a520dbd5019d2de56854018a19f4479f6eceba42c52a77dfb5716bfd57c3`  
		Last Modified: Thu, 27 Mar 2025 20:53:08 GMT  
		Size: 22.7 KB (22672 bytes)  
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
$ docker pull memcached@sha256:c014ab323b1b4bcbb3166beafd41410dbddfbb1a0a6f19deb69e802762874555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32689553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f119d1180b3eca14d9a554f5a3a4e962d438c72c8e71c607ef6688353aa74e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
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
	-	`sha256:c583561c73b24d79d3cb55803558b6f1e508bb37288ee1635b47bdf9a51a38da`  
		Last Modified: Thu, 27 Mar 2025 20:54:02 GMT  
		Size: 2.3 MB (2288694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e039a4f24583d1fa81e89c1a686785aff6e7a269cafcb224a2b61b3d05c6f0ea`  
		Last Modified: Thu, 27 Mar 2025 20:54:01 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aad33c6fcc162e8b1413e31976faafcba7edc16db7e020bc51a9b57c5ecf490`  
		Last Modified: Thu, 27 Mar 2025 20:54:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:73ecf1ebde9749379f2fba28e4e4ba518b5d4943a699ee9745cb9e89f423cb4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2312518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6766598d442fb4e939fe0f028c923ef5ed6b6766633eb2f01669a27a672232`

```dockerfile
```

-	Layers:
	-	`sha256:e93a26c0b4c7baf66130df39a4ea1e3fe6f1767bc12f5ef6698589251a6b6d58`  
		Last Modified: Thu, 27 Mar 2025 20:54:02 GMT  
		Size: 2.3 MB (2289648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5f2e6a18098b4d97813a7772aa4e2bf79a1f45eedbe86caf481cb1840fa9586`  
		Last Modified: Thu, 27 Mar 2025 20:54:01 GMT  
		Size: 22.9 KB (22870 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; 386

```console
$ docker pull memcached@sha256:a5ea0c0aa510a293159050b633c507887a11ebcdc5abb316a7154fcd83ff32c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33943021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfaa7026b44f46e71ba9c44a1481824fdcf9b54f5047b75c26c8710944a5475c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bd5b700a5532cf1e91c064d6ed472b6c511c3d9e9b08a7f31f608192b9afad`  
		Last Modified: Thu, 27 Mar 2025 20:53:34 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c7d8b538dbde73a9a5e3e42f1a04a0fd79356f7f702038a5b159b503cfc1e5`  
		Last Modified: Thu, 27 Mar 2025 20:53:35 GMT  
		Size: 2.5 MB (2500728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7542439206b95728641ceb4b680180a73442cabd6b41fe578628f18b945a9e2a`  
		Last Modified: Thu, 27 Mar 2025 20:53:35 GMT  
		Size: 2.3 MB (2251248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a46d28f72d87befc244136b60a9c42a9b18e552434f284c5687e64805032464`  
		Last Modified: Thu, 27 Mar 2025 20:53:34 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42201d898a9285374141b63bacd52743d268d2f3d800b22b5ee94e5e553fbf8`  
		Last Modified: Thu, 27 Mar 2025 20:53:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:3972e3e9979c0f37a3396a5d86757d1c64ff1661a01486faa24077f6cc9ea8a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2309047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa4d34e6df623288ed6ec9f921a2605e855bfe7736d69fc81466b9e9b903ae7`

```dockerfile
```

-	Layers:
	-	`sha256:9ea1e6ba191d57b2933c4d03388f6a23b8d2b5e5a7fe476d51afcdbf00f53f5c`  
		Last Modified: Thu, 27 Mar 2025 20:53:35 GMT  
		Size: 2.3 MB (2286432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd31371d2f6db2ac800c33bd000734380c9ac8a14aca23e7c2d17ef259810eba`  
		Last Modified: Thu, 27 Mar 2025 20:53:34 GMT  
		Size: 22.6 KB (22615 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:0058a46283d5026f6e6d46d9f8bf0bc5007eefa0fb50ba124a8d9c5c8718c92a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32751201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3b77978b5a8fc2eac21e1b870c55c85b4c6184d63d4ebf29b6e8f154e6af6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1742169600'
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
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
	-	`sha256:40897f2d64cafc6fcb222667c78c37539448596456ecffd3f8ce7cb9b5cabb28`  
		Last Modified: Thu, 27 Mar 2025 20:57:34 GMT  
		Size: 2.3 MB (2317020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82dc27b022eac657403b67589f084f87ad57c6f2891889c6d34ebb4474ee310`  
		Last Modified: Thu, 27 Mar 2025 20:57:34 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e60fc6582e411940064800863c4b87c02105118e0ab5e9648ba1dc12ad8f61`  
		Last Modified: Thu, 27 Mar 2025 20:57:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f4049ead4762d06719ad4fdd2ae2b4f0046a130d2891e2ade50695d33f6d10f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 KB (22569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ba92a7b7f909a167a9bf4e5b91ff175e39f2e162a4f1e6ccf92f49c51b6006`

```dockerfile
```

-	Layers:
	-	`sha256:a8aaf8662d9c73787c7977bf75670f2471e3dd62e02f2103193777209066ad7e`  
		Last Modified: Thu, 27 Mar 2025 20:57:33 GMT  
		Size: 22.6 KB (22569 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:7a7bb97c6c61dd3b4c61f8065dab499bbdfe7cfbe4cb956effa9edcb2e66af3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37176878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc98e5d5a70cd46d1686601994b63dc20ca2175f52c40dba598b762926e2a37c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
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
	-	`sha256:253d36c80692194d710c838a9dcf641b5f4e5b708caf7a0167a65231d784da21`  
		Last Modified: Thu, 27 Mar 2025 20:52:14 GMT  
		Size: 2.4 MB (2418931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815dd2a928bdc05f75187e8f6ea5d86523616fee3840ca9163dbf320a5a6ccc7`  
		Last Modified: Thu, 27 Mar 2025 20:52:13 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121efc6039ff41bfa98a9b47bcf4885d5e03c9456814d0361df3e771d123d137`  
		Last Modified: Thu, 27 Mar 2025 20:52:13 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:d58f5f6a5ac867f60ce3aadad1e9917e3c03c7abb83b35be66d9f4cdcd7be38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2316452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8bcaaed8fc07c31e2e028ca1bc38f788ad0afe190b58e4ba7e054fcb4f4340`

```dockerfile
```

-	Layers:
	-	`sha256:27246f4bfd4ab676df1caa36848b296c12c320d9fc5d0b12540a193755ca7353`  
		Last Modified: Thu, 27 Mar 2025 20:52:14 GMT  
		Size: 2.3 MB (2293705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd9de6d66fe54e520712184227e13e9b50f4e82e578f5812610dd60205ae9f61`  
		Last Modified: Thu, 27 Mar 2025 20:52:13 GMT  
		Size: 22.7 KB (22747 bytes)  
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
$ docker pull memcached@sha256:56725c927f12a53093b0dd8a58ddd8df3d020b46567cb14a8e0201279b97a79e
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
$ docker pull memcached@sha256:c1130e43766e72579b0bb3de4a483b13617fc482b7a3f660833032ddd3df46ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33000858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d4e3512a87fc3884351cf771b57d83866a516c78d3313b209064b6257c17b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14ee0758901af029fd1a78a75a39cef72470aa2c4538747549decb8769c9036`  
		Last Modified: Thu, 27 Mar 2025 20:53:08 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a603c9ce7da5d29d874ef3f48909ac8d815642ee1161fb1088c5c79590059ded`  
		Last Modified: Thu, 27 Mar 2025 20:53:09 GMT  
		Size: 2.5 MB (2491772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6080c85c433088b18ef903a680b49c4c60d2cdf59b8653368bec12dbef863d54`  
		Last Modified: Thu, 27 Mar 2025 20:53:08 GMT  
		Size: 2.3 MB (2302705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b725e8c43056a4da24ef0710ac4716517b27c4ffd092842d38289d6efbb7ab25`  
		Last Modified: Thu, 27 Mar 2025 20:53:08 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfffb76f39255069f9125012bc7bc79eeaeb3f9c248ef8f35de284adafd60312`  
		Last Modified: Thu, 27 Mar 2025 20:53:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:e6c4e9ea0da3ea8f19a3d9280c07e1908364c8c40779cbb2d4f65feaee440615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2312005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4242aa375d1ecdacb2c396dac8135d5aa9caf7db2374a6216f2ad87e3cf05d`

```dockerfile
```

-	Layers:
	-	`sha256:5049b68d7e40887d89a570516aa826f3c1401d51538fa705eefa45144e8da58e`  
		Last Modified: Thu, 27 Mar 2025 20:53:08 GMT  
		Size: 2.3 MB (2289333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7273a520dbd5019d2de56854018a19f4479f6eceba42c52a77dfb5716bfd57c3`  
		Last Modified: Thu, 27 Mar 2025 20:53:08 GMT  
		Size: 22.7 KB (22672 bytes)  
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
$ docker pull memcached@sha256:c014ab323b1b4bcbb3166beafd41410dbddfbb1a0a6f19deb69e802762874555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32689553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f119d1180b3eca14d9a554f5a3a4e962d438c72c8e71c607ef6688353aa74e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
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
	-	`sha256:c583561c73b24d79d3cb55803558b6f1e508bb37288ee1635b47bdf9a51a38da`  
		Last Modified: Thu, 27 Mar 2025 20:54:02 GMT  
		Size: 2.3 MB (2288694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e039a4f24583d1fa81e89c1a686785aff6e7a269cafcb224a2b61b3d05c6f0ea`  
		Last Modified: Thu, 27 Mar 2025 20:54:01 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aad33c6fcc162e8b1413e31976faafcba7edc16db7e020bc51a9b57c5ecf490`  
		Last Modified: Thu, 27 Mar 2025 20:54:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:73ecf1ebde9749379f2fba28e4e4ba518b5d4943a699ee9745cb9e89f423cb4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2312518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6766598d442fb4e939fe0f028c923ef5ed6b6766633eb2f01669a27a672232`

```dockerfile
```

-	Layers:
	-	`sha256:e93a26c0b4c7baf66130df39a4ea1e3fe6f1767bc12f5ef6698589251a6b6d58`  
		Last Modified: Thu, 27 Mar 2025 20:54:02 GMT  
		Size: 2.3 MB (2289648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5f2e6a18098b4d97813a7772aa4e2bf79a1f45eedbe86caf481cb1840fa9586`  
		Last Modified: Thu, 27 Mar 2025 20:54:01 GMT  
		Size: 22.9 KB (22870 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:a5ea0c0aa510a293159050b633c507887a11ebcdc5abb316a7154fcd83ff32c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33943021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfaa7026b44f46e71ba9c44a1481824fdcf9b54f5047b75c26c8710944a5475c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bd5b700a5532cf1e91c064d6ed472b6c511c3d9e9b08a7f31f608192b9afad`  
		Last Modified: Thu, 27 Mar 2025 20:53:34 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c7d8b538dbde73a9a5e3e42f1a04a0fd79356f7f702038a5b159b503cfc1e5`  
		Last Modified: Thu, 27 Mar 2025 20:53:35 GMT  
		Size: 2.5 MB (2500728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7542439206b95728641ceb4b680180a73442cabd6b41fe578628f18b945a9e2a`  
		Last Modified: Thu, 27 Mar 2025 20:53:35 GMT  
		Size: 2.3 MB (2251248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a46d28f72d87befc244136b60a9c42a9b18e552434f284c5687e64805032464`  
		Last Modified: Thu, 27 Mar 2025 20:53:34 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42201d898a9285374141b63bacd52743d268d2f3d800b22b5ee94e5e553fbf8`  
		Last Modified: Thu, 27 Mar 2025 20:53:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:3972e3e9979c0f37a3396a5d86757d1c64ff1661a01486faa24077f6cc9ea8a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2309047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa4d34e6df623288ed6ec9f921a2605e855bfe7736d69fc81466b9e9b903ae7`

```dockerfile
```

-	Layers:
	-	`sha256:9ea1e6ba191d57b2933c4d03388f6a23b8d2b5e5a7fe476d51afcdbf00f53f5c`  
		Last Modified: Thu, 27 Mar 2025 20:53:35 GMT  
		Size: 2.3 MB (2286432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd31371d2f6db2ac800c33bd000734380c9ac8a14aca23e7c2d17ef259810eba`  
		Last Modified: Thu, 27 Mar 2025 20:53:34 GMT  
		Size: 22.6 KB (22615 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; mips64le

```console
$ docker pull memcached@sha256:0058a46283d5026f6e6d46d9f8bf0bc5007eefa0fb50ba124a8d9c5c8718c92a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32751201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3b77978b5a8fc2eac21e1b870c55c85b4c6184d63d4ebf29b6e8f154e6af6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1742169600'
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
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
	-	`sha256:40897f2d64cafc6fcb222667c78c37539448596456ecffd3f8ce7cb9b5cabb28`  
		Last Modified: Thu, 27 Mar 2025 20:57:34 GMT  
		Size: 2.3 MB (2317020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82dc27b022eac657403b67589f084f87ad57c6f2891889c6d34ebb4474ee310`  
		Last Modified: Thu, 27 Mar 2025 20:57:34 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e60fc6582e411940064800863c4b87c02105118e0ab5e9648ba1dc12ad8f61`  
		Last Modified: Thu, 27 Mar 2025 20:57:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:f4049ead4762d06719ad4fdd2ae2b4f0046a130d2891e2ade50695d33f6d10f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 KB (22569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ba92a7b7f909a167a9bf4e5b91ff175e39f2e162a4f1e6ccf92f49c51b6006`

```dockerfile
```

-	Layers:
	-	`sha256:a8aaf8662d9c73787c7977bf75670f2471e3dd62e02f2103193777209066ad7e`  
		Last Modified: Thu, 27 Mar 2025 20:57:33 GMT  
		Size: 22.6 KB (22569 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:7a7bb97c6c61dd3b4c61f8065dab499bbdfe7cfbe4cb956effa9edcb2e66af3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37176878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc98e5d5a70cd46d1686601994b63dc20ca2175f52c40dba598b762926e2a37c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
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
	-	`sha256:253d36c80692194d710c838a9dcf641b5f4e5b708caf7a0167a65231d784da21`  
		Last Modified: Thu, 27 Mar 2025 20:52:14 GMT  
		Size: 2.4 MB (2418931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815dd2a928bdc05f75187e8f6ea5d86523616fee3840ca9163dbf320a5a6ccc7`  
		Last Modified: Thu, 27 Mar 2025 20:52:13 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121efc6039ff41bfa98a9b47bcf4885d5e03c9456814d0361df3e771d123d137`  
		Last Modified: Thu, 27 Mar 2025 20:52:13 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:d58f5f6a5ac867f60ce3aadad1e9917e3c03c7abb83b35be66d9f4cdcd7be38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2316452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8bcaaed8fc07c31e2e028ca1bc38f788ad0afe190b58e4ba7e054fcb4f4340`

```dockerfile
```

-	Layers:
	-	`sha256:27246f4bfd4ab676df1caa36848b296c12c320d9fc5d0b12540a193755ca7353`  
		Last Modified: Thu, 27 Mar 2025 20:52:14 GMT  
		Size: 2.3 MB (2293705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd9de6d66fe54e520712184227e13e9b50f4e82e578f5812610dd60205ae9f61`  
		Last Modified: Thu, 27 Mar 2025 20:52:13 GMT  
		Size: 22.7 KB (22747 bytes)  
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
