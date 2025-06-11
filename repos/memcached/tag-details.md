<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `memcached`

-	[`memcached:1`](#memcached1)
-	[`memcached:1-alpine`](#memcached1-alpine)
-	[`memcached:1-alpine3.22`](#memcached1-alpine322)
-	[`memcached:1-bookworm`](#memcached1-bookworm)
-	[`memcached:1.6`](#memcached16)
-	[`memcached:1.6-alpine`](#memcached16-alpine)
-	[`memcached:1.6-alpine3.22`](#memcached16-alpine322)
-	[`memcached:1.6-bookworm`](#memcached16-bookworm)
-	[`memcached:1.6.38`](#memcached1638)
-	[`memcached:1.6.38-alpine`](#memcached1638-alpine)
-	[`memcached:1.6.38-alpine3.22`](#memcached1638-alpine322)
-	[`memcached:1.6.38-bookworm`](#memcached1638-bookworm)
-	[`memcached:alpine`](#memcachedalpine)
-	[`memcached:alpine3.22`](#memcachedalpine322)
-	[`memcached:bookworm`](#memcachedbookworm)
-	[`memcached:latest`](#memcachedlatest)

## `memcached:1`

```console
$ docker pull memcached@sha256:89b2dfa7e55e5fd1986e22210cdf89f0a5e5d6c913101e2bcfdfb4d1d73de7ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:1` - linux; amd64

```console
$ docker pull memcached@sha256:c2b5b37862a0d15d6622bea58a1e3a7a34610456324dc81a6de4e3369d06a5f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33026651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:809ba6b39db15dffb27e2affc4fc5bc5eee2c32ee9b06e08f2f604ee63e41a78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35255ebbfb2408b64a9d53c3d868456872a9b4d89ff4e80f2a8d20c4332dd69`  
		Last Modified: Tue, 10 Jun 2025 23:32:18 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be9410e6aeed64e084cb2812f5d70658e1a9ffe79b5972cea39097c9b949e4e`  
		Last Modified: Tue, 10 Jun 2025 23:32:19 GMT  
		Size: 2.5 MB (2492199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d86227fbbb72b09a47e8016b198dc2062598d3e4c4b358cfa655a2a2c044ef`  
		Last Modified: Tue, 10 Jun 2025 23:32:20 GMT  
		Size: 2.3 MB (2302808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad105488469355bcd85bf5c9c6b74cf9729838da44ad0c6f500f252c6860e8c`  
		Last Modified: Tue, 10 Jun 2025 23:32:20 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90864ece76220d4e897cf79c19145c02ce9d1c1326bb831401963b27ec0ca566`  
		Last Modified: Tue, 10 Jun 2025 23:32:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:5b481897e28479249d51b4c0720b45485fe1952dcb27924f267fcd30d68de833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2425304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6773503e415cd198fe6533c8042593b7aabb0d583e0baf500eed5c4c78452531`

```dockerfile
```

-	Layers:
	-	`sha256:4c6461ec41fb74fe203eb1b6c30c50eddc7f6c11871bfa03eab07db6a4b17c6f`  
		Last Modified: Wed, 11 Jun 2025 00:34:27 GMT  
		Size: 2.4 MB (2399984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e35a57a543fde6b5a8a3e185100a7e9b5ac2a947dea0b7589b5531fab06c67c`  
		Last Modified: Wed, 11 Jun 2025 00:34:28 GMT  
		Size: 25.3 KB (25320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v5

```console
$ docker pull memcached@sha256:ca1e51720502c0722aae38efd0a64db105570638d65d6a70ab4572658aff584a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.1 MB (30093253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86fc08738ceff7b24bd461ffd9a41799a048727c6673c1a3c4cb5a01f6b82608`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:750907abe8bb5d66304ed40261e1579b6575871f6848cfbd720888c20afd3b67`  
		Last Modified: Tue, 10 Jun 2025 22:47:31 GMT  
		Size: 25.8 MB (25762396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9660206a4f42b745fdc386aced2845f4fa99b6de361892e4df07c2daf0f24c`  
		Last Modified: Wed, 11 Jun 2025 00:04:16 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877a28dd495fb8632729edaf5b9318ec22ce2a5e402b746782fb7084fd01032c`  
		Last Modified: Wed, 11 Jun 2025 00:04:19 GMT  
		Size: 2.1 MB (2097026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06cb49b999b102d1dc8725fedf17028635be0bcc810a049a03c6e96128a9e4e6`  
		Last Modified: Wed, 11 Jun 2025 00:04:30 GMT  
		Size: 2.2 MB (2232317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee68dfb7714895c5d09887e2708b1296a8855e4ac7ff3d0a158bf029e81e157`  
		Last Modified: Wed, 11 Jun 2025 00:04:39 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff86e8516fa08ad0aa15dfb3afebb40da609006594dcf941ed7900b39cec11aa`  
		Last Modified: Wed, 11 Jun 2025 00:04:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:68162c3dae075d4cb8b6a636c634479c8402119be9f3b6f995913ba4d47162e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2429297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10be7e4ce251f42cb456f15eae67ae97fc6e3040fc50fe0990c4503b35a8829b`

```dockerfile
```

-	Layers:
	-	`sha256:5874edec5896e806374ff905b6f10f3724d44a31a61bf0d830a5ecac4cfbb548`  
		Last Modified: Wed, 11 Jun 2025 03:34:34 GMT  
		Size: 2.4 MB (2403830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54b0ebcaf098420587b0d84ab425ad9abdfc444c86c6ba478b50be7b335cd3c6`  
		Last Modified: Wed, 11 Jun 2025 03:34:34 GMT  
		Size: 25.5 KB (25467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v7

```console
$ docker pull memcached@sha256:d208683140025f905b085b97b35b3a533015b73809d3740e5e3d968c202ec9e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28070929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b74912d1ce300e7a774e690f1c07510c2228991f23ee542e33cc1028e45d90bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6615a784a0e15fd2ed6d79980e68d9cfe87df589b9af6f4c71656286b040acc`  
		Last Modified: Tue, 10 Jun 2025 23:43:55 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66fc152354c58f6024d7e37104e92e718be7b1e70f9745e96e63006f79730f5`  
		Last Modified: Tue, 10 Jun 2025 23:43:56 GMT  
		Size: 1.9 MB (1946292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3712992b59c9c2fa191ca82275b5fb441fcc21940ef625721d0221723f70d9e`  
		Last Modified: Tue, 10 Jun 2025 23:43:56 GMT  
		Size: 2.2 MB (2184378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ba9e36b6e72e151a91cc69343438b9341451e4196d29b259766ab25ece2755`  
		Last Modified: Tue, 10 Jun 2025 23:43:56 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f566ffc3a278d8a018e52b43be1df458ee6632e59b56f75a94a0d058a6cfe73`  
		Last Modified: Tue, 10 Jun 2025 23:43:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:2bbfd653e524ef9316e75f9681ac6876a3e40a63ac124b1e00216760e2855ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2427734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e73cc4fc38d626337d836752990c011dfc545348cb8fd74aa3ae7a39e08c5bc`

```dockerfile
```

-	Layers:
	-	`sha256:8eec2d1ef62751b78959b1e676c070de5b6da4490f0797715b6038816e6ecbe7`  
		Last Modified: Wed, 11 Jun 2025 00:34:36 GMT  
		Size: 2.4 MB (2402267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7bd74b81adae550be8823fda7677f05554265436005a14b9a3f3775ec776a45`  
		Last Modified: Wed, 11 Jun 2025 00:34:37 GMT  
		Size: 25.5 KB (25467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:8a7286d77ae74f81f50dffd6f6e763edd304ed10f5a56e2fe3bdbc38578586a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32723815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05a57428c8257697aa07726f04832bba5278021c4028ea564ada3e7c63bf181`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c5447936c48fe52b15de86391eaf4d170445111319a12dd6f05a85d115b1a4`  
		Last Modified: Wed, 11 Jun 2025 00:32:55 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfca24a3c9155df906544ba98f8bb2bc9f66d9704ed8edf0e731bfe4672420d2`  
		Last Modified: Wed, 11 Jun 2025 00:32:58 GMT  
		Size: 2.4 MB (2355841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eab66920dbc0773d0617dced9ec788e2dc243fc3c3abb0855646922df94744d`  
		Last Modified: Wed, 11 Jun 2025 00:33:04 GMT  
		Size: 2.3 MB (2288782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99014141349bea93d0cf26fd4326ec422f06a635c0ba43644c022fc9960456b8`  
		Last Modified: Wed, 11 Jun 2025 00:33:09 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c855df1fbe1070effdf016a21c2055af95b6325b3e22aa0f32e24d1896dd7a1a`  
		Last Modified: Wed, 11 Jun 2025 00:33:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:45dd4c7b93d5dc7ac1a41023089465fc7feeb3a6878b831308593b595c4453ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2425816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d377887b57b57637deedd7fc6db230aceaeb6f127b9d419649daf5eb921dcfe3`

```dockerfile
```

-	Layers:
	-	`sha256:104fd15db5961a346a71d8c3471d234720c45848fed57ef5c979b5904c13679d`  
		Last Modified: Wed, 11 Jun 2025 03:34:41 GMT  
		Size: 2.4 MB (2400299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b12674469f62c07ff246f7a86cd72871b797a081f0f1a29ebf34768864970340`  
		Last Modified: Wed, 11 Jun 2025 03:34:42 GMT  
		Size: 25.5 KB (25517 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:2fd3408e4989cc9e56a6d3add7ce53181decaf9d7cc19e14b49670b45944e40e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33967948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a326ebe4a452ab75793d01324bf45cdf00e7f2aa83d4793e9993f6317370b81`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c3d46fed134488b3ee18c12cb308c8d5520b8c647122c392f9fb76e3e1e2fc61`  
		Last Modified: Tue, 10 Jun 2025 22:47:25 GMT  
		Size: 29.2 MB (29212433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6e1ece79d563054c9ed24818e5adb5d97e5a1bd3a898d27b10ad0ed0d944fe`  
		Last Modified: Tue, 10 Jun 2025 23:32:02 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d82ab526e835ea99bac51cedfd44fda08d1096806527e0e4776d1747931bfb`  
		Last Modified: Tue, 10 Jun 2025 23:32:03 GMT  
		Size: 2.5 MB (2502688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c26ac869e988fa955c3c084363eb741d506a2034cdd3e12a5c98ff74e4c65c5`  
		Last Modified: Tue, 10 Jun 2025 23:32:03 GMT  
		Size: 2.3 MB (2251313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87ab77943d07e12971b970348f051de5367dd6a2bb147741b63f12eca74d55f`  
		Last Modified: Tue, 10 Jun 2025 23:32:03 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5505b2cac6d2a77393345699695a05426271e871ba824bf0e22789a5cdf44f8e`  
		Last Modified: Tue, 10 Jun 2025 23:32:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:f5178b4eff39883c5450012b44b95dc2e13a26e5c3efe2221f9a929a01b99a6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2422389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db0fa4b9612a2b4b5f20852ca646c7fa318ae7057ec68f20599d1281453c0ac5`

```dockerfile
```

-	Layers:
	-	`sha256:27ef430fcb7445f00c5cbbac9416a8082301986670c56b7112c8ee8d2bc7ea63`  
		Last Modified: Wed, 11 Jun 2025 00:34:45 GMT  
		Size: 2.4 MB (2397127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c71e82389c2ff610732d9cc27ec31e1061a1fe683a7594c559d2f0ad1b307bf`  
		Last Modified: Wed, 11 Jun 2025 00:34:46 GMT  
		Size: 25.3 KB (25262 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; mips64le

```console
$ docker pull memcached@sha256:4dcc31fdaa97e6430560dfb497e4dde22b2ef368e6c66a3b271a5343bfd86e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32779330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6bba452dff6149dc16dfc6eda06981c4240993be55b9b6f998d30e26935e676`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ac3f61581c7f5755d8598b3a0857c417db0251b17c0e4e4f43a5fc0e24023524`  
		Last Modified: Tue, 10 Jun 2025 22:48:26 GMT  
		Size: 28.5 MB (28516717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b713f027201c7d06c5013a8693a2fb17e64d3d8113328cd83f01c565ddd25a31`  
		Last Modified: Wed, 11 Jun 2025 00:38:45 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699452fffd3fdc6e04d5c6c072d85da568d4477714b34612b15505bebad40576`  
		Last Modified: Wed, 11 Jun 2025 00:38:49 GMT  
		Size: 1.9 MB (1944083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4909573bcae2300d9ad92749c2279eaab07c75210c195cc36bcc323a289711c`  
		Last Modified: Wed, 11 Jun 2025 00:38:54 GMT  
		Size: 2.3 MB (2317017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42800230fbc3a3fdd8ebd615178ea6d750f32c99d916c8d4c1fce650c9724740`  
		Last Modified: Wed, 11 Jun 2025 00:39:03 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc602c2ec2581679f4ba36524612bf709f9828eae2e8e2382a5b72cfe43ddde`  
		Last Modified: Wed, 11 Jun 2025 00:39:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:c8b58a5685ab59a7e412a46fadca1a86a8065cb821c20aa84496f3da2932a6bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d142d271ffff6f14e07b46862b9d5c35a3f62a5ae21f22698dbf2729e22393e5`

```dockerfile
```

-	Layers:
	-	`sha256:0c2d883e7eeaa126767df6696d4d4d21074e1b88388aca7a8d9936e34d972390`  
		Last Modified: Wed, 11 Jun 2025 03:34:48 GMT  
		Size: 25.2 KB (25216 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:ec8926cb7edeb9e447cfa09a6496daf6ddf6214c670db96c915bfbfcdd867a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37203472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f834c7368564e22deca1fec762744af6a328960d29a0757f965efb0922ef2ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c9cd5d5c131a8141631d87d9507a82e0549a2144689442301c07d2da80f39d19`  
		Last Modified: Tue, 10 Jun 2025 23:58:45 GMT  
		Size: 32.1 MB (32072795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783cc02b7ca742bdfa931c46ca74a297d6743f7632079af1d38a86f0ef33e67e`  
		Last Modified: Tue, 10 Jun 2025 23:50:23 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dcb0a6965f82b33b339604c7bfc7e13fddac325187039be9416554f6deaa468`  
		Last Modified: Tue, 10 Jun 2025 23:50:24 GMT  
		Size: 2.7 MB (2710185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460f1a7eb5adf7c13e3a2c6e82959f31bd877cd781b02a5997ba29d421ea0845`  
		Last Modified: Tue, 10 Jun 2025 23:50:24 GMT  
		Size: 2.4 MB (2418981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5dbb0f6f2b188832219b7b4c16a43d53399710d576b050d6939a213e05dd83`  
		Last Modified: Tue, 10 Jun 2025 23:50:24 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ce0fe2674fef821731c0bf8d4218891392e919b579863b73b27c02281d67bb`  
		Last Modified: Tue, 10 Jun 2025 23:50:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:295a95b2a5fbcaba4f0430c8b8fc00ec4ebe4a3ab75480f5ed7890dd086efdc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2429850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd03034a2e56497ce0625f4e0bfba90e28c4d23be1250fe5547dfab3f61abd66`

```dockerfile
```

-	Layers:
	-	`sha256:5e551af8256cd1f6d5d31b7a99d5338c2e0f7c59dd109277d12a1d01c1f8e4dc`  
		Last Modified: Wed, 11 Jun 2025 03:34:53 GMT  
		Size: 2.4 MB (2404456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eac12139332bd876a1e77dd40aa823e07245885fb8a0d33164fd342e6a3198b9`  
		Last Modified: Wed, 11 Jun 2025 03:34:54 GMT  
		Size: 25.4 KB (25394 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:04933adc68fd0a9324a7d5796e1d3cde2a0012644f2ea93c60f0b9ef4f676e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31309863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d59a9f1fa8b8ed5157a51f715aac503833e36e3aa6da498fd68e1647c8366e7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d890a6beb4a310ea4195e7ebd130e37a17b64820c995a543bb5619b2eab1e6`  
		Last Modified: Wed, 11 Jun 2025 09:15:09 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119a4250ae0069dea78d2943d561ab4ad7db7018ddd34dcdf8ceecada8494508`  
		Last Modified: Wed, 11 Jun 2025 09:15:10 GMT  
		Size: 2.2 MB (2156963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eea4eabc325c68a766c64d84b958281150eee02f4ada0091377c9af7b07a793`  
		Last Modified: Wed, 11 Jun 2025 09:15:10 GMT  
		Size: 2.3 MB (2263533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ddbca61153701e80e50122cb3d22cd45a49b4bf191114e8b132b588b077673`  
		Last Modified: Wed, 11 Jun 2025 09:15:10 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42132a3abe6b3ca5bc8e4e623ffa00fe86641a0a42454bba499fa70136dea21`  
		Last Modified: Wed, 11 Jun 2025 09:15:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:2f715ae3a26ddc650f595ca31d33c4a4c14311b1347a6e8d20aca949b131063d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2422126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a4df8b3c359f6d964f37642182e6de7a4cd8cc28676c409e313aa88eaf5b698`

```dockerfile
```

-	Layers:
	-	`sha256:994b93c94dedc6bf0bf79fcfb6b5332c77a3fea69cd945274a1b5eead27d80e0`  
		Last Modified: Wed, 11 Jun 2025 12:34:39 GMT  
		Size: 2.4 MB (2396806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bd4c128777cf5eda46cb5a3ab851f4294546c4b8267f89d17b1adfc4ad5e9bd`  
		Last Modified: Wed, 11 Jun 2025 12:34:40 GMT  
		Size: 25.3 KB (25320 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:08b6a6cba188fab22215b24a3d5c1ccc18343bc337268f663f20cd86dbdfffeb
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
$ docker pull memcached@sha256:606d01f5580448504043b6ca9994e651efd5cd79822d58639d3f7cb17850fe19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5901265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be94f0135609b0bf7b7f5787294b235034eed9e87be4689825605790d50cff24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef12469432374e0b8bca5dba738c021a8d10c2fc0374275956b8104d92b4053`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b606d4a25237e4f6fe0e5c302a9e8567588be271b95f83da33a31499dac8b0`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 104.7 KB (104728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05dc60670fe6d174274d0896db26274c8ef0e2f77afc45eb51b7cdefceddab51`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 2.0 MB (1998336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa1296a9dd4dfcfb8fcefddbc83edb103f22840e4a193ee7a1e207b232e7338e`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea55364413c47b3f8818b61b2de7d3e3a28b8592bbe25c146ef8a1edf4a17363`  
		Last Modified: Tue, 03 Jun 2025 13:30:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:552c1686ee77c9b7fba7c898a29803c51578a0e80715122dccafcb355025c0de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 KB (119969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb77b32517cfa4aa8e784ef0102259db59c51c349a263d3c87b50ed983fc3ef`

```dockerfile
```

-	Layers:
	-	`sha256:ce2831bada0ca80b430da313ea1ccf45204f6ca84dec4484adbc614b9494be4f`  
		Last Modified: Tue, 03 Jun 2025 14:45:05 GMT  
		Size: 96.2 KB (96180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2114cfbb746c8f95ef4f406bb87b6458f0b23a4844fe5a9774c62c1e9255d42c`  
		Last Modified: Tue, 03 Jun 2025 14:45:05 GMT  
		Size: 23.8 KB (23789 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:41a88acc0a34fb3e7bf86b58cd20dce95d6a609303362364ed6f7f7bd3079880
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6247593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7dfc69a347c50839ad628b964963b8149866c24446202e5789804bc8067e23c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf218c5787338a7792daeaefbb181cf59684549881841831603999e10d5187e`  
		Last Modified: Tue, 03 Jun 2025 13:30:42 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661f41de55d4df851603ae02c2cdc6e73b2ab9a9ecf45eac9b82f105cb482ee1`  
		Last Modified: Tue, 03 Jun 2025 13:32:27 GMT  
		Size: 120.8 KB (120818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e622a5461288686c20e7803ad3d17a45f79a7b140e90b6bbcb6bc8f462c57010`  
		Last Modified: Tue, 03 Jun 2025 13:34:11 GMT  
		Size: 2.0 MB (1989486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd408342d331a0cceff7d0f0d80a5ec8f14ea99c95791d36a29518931ebefb8e`  
		Last Modified: Tue, 03 Jun 2025 13:30:50 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9520bec02cd5779ce2136e2d96c570b84f26641fe4e391f33fb8228c77f4aeac`  
		Last Modified: Tue, 03 Jun 2025 13:30:57 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:e3d2683766797f6a8fe83ea61b5a2979ef33a4d78ea3e0aa9047e37cd2a3fd7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 KB (120271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7447a1da56e995b60bc91c0a003ba4d9d9a6c78fc3a8f9220e19353f0eebc3fc`

```dockerfile
```

-	Layers:
	-	`sha256:ca6f6e30cd21da5e6e9e17e53ca50b541ab1099c4a87acc15081d16797f581c2`  
		Last Modified: Tue, 03 Jun 2025 14:45:05 GMT  
		Size: 96.3 KB (96284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e835bdadfb4d4407a7c5d19b63c33e1f15ec1d83efbabf27ae3e33553a599c2a`  
		Last Modified: Tue, 03 Jun 2025 14:45:05 GMT  
		Size: 24.0 KB (23987 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:39a104f3004fd4a9e820173573ffcc2b15ec2948ca68e6b3d8cfe0e3ecdd12b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5686724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34077a3f17da3a414af6d200ebb8d57c0e73bd8d1d460d1e2ed17e8cc61341c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4498fffb412d9bcc1b73bd7bfa0d2754cf5230f83c22efba4479b1854b502291`  
		Last Modified: Tue, 03 Jun 2025 14:45:06 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7c585852f370434b2f4b564d7ec7ea58c5b06e528ac6b8dffd1212dd6f521e`  
		Last Modified: Tue, 03 Jun 2025 14:45:06 GMT  
		Size: 109.5 KB (109520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc95d14dcefd82bdeb2d89e3ba0fad63fd7fc93194f678a93bc1d9217b9c2ff`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 2.0 MB (1959822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f21560067e099265312c0975371d273829c2923dee88b90d7e24537a458d696`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f53957473f72614ae6b6abc50bff4d20acd3a704edb23755b4e2a5bb6f71a7aa`  
		Last Modified: Tue, 03 Jun 2025 14:45:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:3d21a067c964615eb13e5e591df9d66ea730e3a04be65f71321ad10f1c367d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.9 KB (119867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:897704751afe9189615b739f6bf4308d242df30afe8b42aff038d7828ab081db`

```dockerfile
```

-	Layers:
	-	`sha256:6e6181041c0daeaf47a8f8475f930b1ea73d5cf55a7b5a7b3efba14627e6e8c4`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 96.1 KB (96135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:768c02304a965eacaab05dd9b82b91c453a28d3fbc77b34221ab010ccc28cbcb`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 23.7 KB (23732 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:0bf6f7efe5d3e4b11cec8d17f924ae42d7622e1b0bbcdb56d4757bb3d22ab4b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5947182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf2f7366cf8143a64896b9b751eadad7798b3eec347162fca324567acec20082`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6dc89a1ff7a965251a27c2d9dcb719f464507b964ba3286d6a6034d9f89769`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d75cf13bd9119987f7710d75fd446cd9d065487b3e83297be8c9c4b3120e7e`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 124.3 KB (124312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9461b52977c4cd8b006ffee034043d389554e4c3b267b0901829e7a7a353b8`  
		Last Modified: Tue, 03 Jun 2025 14:45:08 GMT  
		Size: 2.1 MB (2091330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c2dc09d491c7a103b9bd75fa5267b316526d77163130840938eadadb72e6b1`  
		Last Modified: Tue, 03 Jun 2025 14:45:08 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bece68e2cfcb576a9778e7da37d6e2a58ac091bd908caf52a90c4baf09d4d079`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:efd926e1e98c4bedf0db6b24ec177d116548e0652d6b66db54cb2a3e81d21899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 KB (118151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57233506303dd47952c792831142da6a3fe9c4e6c5ea7678ff91b329c08e589`

```dockerfile
```

-	Layers:
	-	`sha256:ed1b26ef88ce71431cfd88a99e6d2d4d13494e7bf5056e489b0b1eb2133d81ab`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 94.3 KB (94287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eaf4c09f8a1fb9991161e85051ae93568c08ab9b2a1142b1bbf99a182e7c0f0`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 23.9 KB (23864 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:aed10964c6cc121d6201aaa8301e269cb88396f19e514ab4529073da9d0c2218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f0390597339801ec08bfd34d10d8bf91dc8e03f2e864f9643758e7ade704d40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db926e6f83170fbe6f646943cb34741a092b9ce5226a6d1bd6b9214d4515055f`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1884ffba96f71fb43c1fef7f0405221b4c8070f55b8667e8b75cc04d268f5cbc`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 107.9 KB (107905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9dea200205fca0caa1f83f40ea69123226bf113407054775efd4a508ae03c65`  
		Last Modified: Tue, 03 Jun 2025 14:45:10 GMT  
		Size: 1.9 MB (1932426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0f27bac94157c911304329980a3ac043834b3407e7ebf8f6a152d114f5949c`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec883045be124559e6a84f03b352a143404848596a99aacded6fe91e3150c5eb`  
		Last Modified: Tue, 03 Jun 2025 14:45:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:aa82a1a35cac8440e684fe5059460736ac54ad11d07080afd5fe8fc546806556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.1 KB (118146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc357c735ee41efba1c1c97057f37ee17ce47e28b9887307cbd229d6895da03`

```dockerfile
```

-	Layers:
	-	`sha256:194792c5d362608149275ef412c050bbec126c27232fd4210029e547cac00ae7`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddb88c4acf94b34eadf22eea85377681f766029d1748d93ace4a6a7e7b23538a`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 23.9 KB (23863 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:656e879b0120ed1dc41f4eea945ffd837cbd61df8792d9622df23bb94621dcba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5800523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6248ca4cb8546aea87cb93f6af7f23e99e572b78a8454a9af00758038970fb5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb224b0e357fdb3b8b28a5e9a31cd54bf59197e6b87eff81737fee0cbf2326d1`  
		Last Modified: Tue, 03 Jun 2025 14:45:11 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ffb790e1ad6ec57e858ea0d68a71a20c8d4f1e44cb7d1089e651677c61ff004`  
		Last Modified: Tue, 03 Jun 2025 14:45:11 GMT  
		Size: 113.5 KB (113497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ed9fcfc8c703bdee212b6c00a17c6ea94d9ae8e768825af3a9999a2cc0aa5f`  
		Last Modified: Tue, 03 Jun 2025 14:45:11 GMT  
		Size: 2.0 MB (2038146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d331df3ee94402980d3422bee4dcbd4613703a284b9ccc1fe1f6fdec3f4d869`  
		Last Modified: Tue, 03 Jun 2025 14:45:11 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93af5977e9aba9bde51aba44398ec5690948753fa15a6c35e41208a543d6c2e`  
		Last Modified: Tue, 03 Jun 2025 14:45:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:3dd443c4d6c4cbce2a2b09a2b2869282e7d1478a57e9967b3b38705268315e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.0 KB (118019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538a73a14cc21737f67c2f643b673960e4d7c106988e28fa3bb45734ed83532d`

```dockerfile
```

-	Layers:
	-	`sha256:726d5699c7a6f8c2cc2e05311aefbfc8a4a5369d49388faaf922cdf278a20b7c`  
		Last Modified: Tue, 03 Jun 2025 14:45:12 GMT  
		Size: 94.2 KB (94229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:382c68890507f3d9fe2510636665755df015b0354866ac714c3e70a3201ca87e`  
		Last Modified: Tue, 03 Jun 2025 14:45:11 GMT  
		Size: 23.8 KB (23790 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine3.22`

```console
$ docker pull memcached@sha256:08b6a6cba188fab22215b24a3d5c1ccc18343bc337268f663f20cd86dbdfffeb
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

### `memcached:1-alpine3.22` - linux; amd64

```console
$ docker pull memcached@sha256:606d01f5580448504043b6ca9994e651efd5cd79822d58639d3f7cb17850fe19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5901265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be94f0135609b0bf7b7f5787294b235034eed9e87be4689825605790d50cff24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef12469432374e0b8bca5dba738c021a8d10c2fc0374275956b8104d92b4053`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b606d4a25237e4f6fe0e5c302a9e8567588be271b95f83da33a31499dac8b0`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 104.7 KB (104728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05dc60670fe6d174274d0896db26274c8ef0e2f77afc45eb51b7cdefceddab51`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 2.0 MB (1998336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa1296a9dd4dfcfb8fcefddbc83edb103f22840e4a193ee7a1e207b232e7338e`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea55364413c47b3f8818b61b2de7d3e3a28b8592bbe25c146ef8a1edf4a17363`  
		Last Modified: Tue, 03 Jun 2025 13:30:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:552c1686ee77c9b7fba7c898a29803c51578a0e80715122dccafcb355025c0de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 KB (119969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb77b32517cfa4aa8e784ef0102259db59c51c349a263d3c87b50ed983fc3ef`

```dockerfile
```

-	Layers:
	-	`sha256:ce2831bada0ca80b430da313ea1ccf45204f6ca84dec4484adbc614b9494be4f`  
		Last Modified: Tue, 03 Jun 2025 14:45:05 GMT  
		Size: 96.2 KB (96180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2114cfbb746c8f95ef4f406bb87b6458f0b23a4844fe5a9774c62c1e9255d42c`  
		Last Modified: Tue, 03 Jun 2025 14:45:05 GMT  
		Size: 23.8 KB (23789 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:41a88acc0a34fb3e7bf86b58cd20dce95d6a609303362364ed6f7f7bd3079880
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6247593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7dfc69a347c50839ad628b964963b8149866c24446202e5789804bc8067e23c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf218c5787338a7792daeaefbb181cf59684549881841831603999e10d5187e`  
		Last Modified: Tue, 03 Jun 2025 13:30:42 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661f41de55d4df851603ae02c2cdc6e73b2ab9a9ecf45eac9b82f105cb482ee1`  
		Last Modified: Tue, 03 Jun 2025 13:32:27 GMT  
		Size: 120.8 KB (120818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e622a5461288686c20e7803ad3d17a45f79a7b140e90b6bbcb6bc8f462c57010`  
		Last Modified: Tue, 03 Jun 2025 13:34:11 GMT  
		Size: 2.0 MB (1989486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd408342d331a0cceff7d0f0d80a5ec8f14ea99c95791d36a29518931ebefb8e`  
		Last Modified: Tue, 03 Jun 2025 13:30:50 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9520bec02cd5779ce2136e2d96c570b84f26641fe4e391f33fb8228c77f4aeac`  
		Last Modified: Tue, 03 Jun 2025 13:30:57 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:e3d2683766797f6a8fe83ea61b5a2979ef33a4d78ea3e0aa9047e37cd2a3fd7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 KB (120271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7447a1da56e995b60bc91c0a003ba4d9d9a6c78fc3a8f9220e19353f0eebc3fc`

```dockerfile
```

-	Layers:
	-	`sha256:ca6f6e30cd21da5e6e9e17e53ca50b541ab1099c4a87acc15081d16797f581c2`  
		Last Modified: Tue, 03 Jun 2025 14:45:05 GMT  
		Size: 96.3 KB (96284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e835bdadfb4d4407a7c5d19b63c33e1f15ec1d83efbabf27ae3e33553a599c2a`  
		Last Modified: Tue, 03 Jun 2025 14:45:05 GMT  
		Size: 24.0 KB (23987 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.22` - linux; 386

```console
$ docker pull memcached@sha256:39a104f3004fd4a9e820173573ffcc2b15ec2948ca68e6b3d8cfe0e3ecdd12b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5686724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34077a3f17da3a414af6d200ebb8d57c0e73bd8d1d460d1e2ed17e8cc61341c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4498fffb412d9bcc1b73bd7bfa0d2754cf5230f83c22efba4479b1854b502291`  
		Last Modified: Tue, 03 Jun 2025 14:45:06 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7c585852f370434b2f4b564d7ec7ea58c5b06e528ac6b8dffd1212dd6f521e`  
		Last Modified: Tue, 03 Jun 2025 14:45:06 GMT  
		Size: 109.5 KB (109520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc95d14dcefd82bdeb2d89e3ba0fad63fd7fc93194f678a93bc1d9217b9c2ff`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 2.0 MB (1959822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f21560067e099265312c0975371d273829c2923dee88b90d7e24537a458d696`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f53957473f72614ae6b6abc50bff4d20acd3a704edb23755b4e2a5bb6f71a7aa`  
		Last Modified: Tue, 03 Jun 2025 14:45:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:3d21a067c964615eb13e5e591df9d66ea730e3a04be65f71321ad10f1c367d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.9 KB (119867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:897704751afe9189615b739f6bf4308d242df30afe8b42aff038d7828ab081db`

```dockerfile
```

-	Layers:
	-	`sha256:6e6181041c0daeaf47a8f8475f930b1ea73d5cf55a7b5a7b3efba14627e6e8c4`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 96.1 KB (96135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:768c02304a965eacaab05dd9b82b91c453a28d3fbc77b34221ab010ccc28cbcb`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 23.7 KB (23732 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.22` - linux; ppc64le

```console
$ docker pull memcached@sha256:0bf6f7efe5d3e4b11cec8d17f924ae42d7622e1b0bbcdb56d4757bb3d22ab4b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5947182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf2f7366cf8143a64896b9b751eadad7798b3eec347162fca324567acec20082`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6dc89a1ff7a965251a27c2d9dcb719f464507b964ba3286d6a6034d9f89769`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d75cf13bd9119987f7710d75fd446cd9d065487b3e83297be8c9c4b3120e7e`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 124.3 KB (124312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9461b52977c4cd8b006ffee034043d389554e4c3b267b0901829e7a7a353b8`  
		Last Modified: Tue, 03 Jun 2025 14:45:08 GMT  
		Size: 2.1 MB (2091330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c2dc09d491c7a103b9bd75fa5267b316526d77163130840938eadadb72e6b1`  
		Last Modified: Tue, 03 Jun 2025 14:45:08 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bece68e2cfcb576a9778e7da37d6e2a58ac091bd908caf52a90c4baf09d4d079`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:efd926e1e98c4bedf0db6b24ec177d116548e0652d6b66db54cb2a3e81d21899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 KB (118151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57233506303dd47952c792831142da6a3fe9c4e6c5ea7678ff91b329c08e589`

```dockerfile
```

-	Layers:
	-	`sha256:ed1b26ef88ce71431cfd88a99e6d2d4d13494e7bf5056e489b0b1eb2133d81ab`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 94.3 KB (94287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eaf4c09f8a1fb9991161e85051ae93568c08ab9b2a1142b1bbf99a182e7c0f0`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 23.9 KB (23864 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.22` - linux; riscv64

```console
$ docker pull memcached@sha256:aed10964c6cc121d6201aaa8301e269cb88396f19e514ab4529073da9d0c2218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f0390597339801ec08bfd34d10d8bf91dc8e03f2e864f9643758e7ade704d40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db926e6f83170fbe6f646943cb34741a092b9ce5226a6d1bd6b9214d4515055f`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1884ffba96f71fb43c1fef7f0405221b4c8070f55b8667e8b75cc04d268f5cbc`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 107.9 KB (107905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9dea200205fca0caa1f83f40ea69123226bf113407054775efd4a508ae03c65`  
		Last Modified: Tue, 03 Jun 2025 14:45:10 GMT  
		Size: 1.9 MB (1932426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0f27bac94157c911304329980a3ac043834b3407e7ebf8f6a152d114f5949c`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec883045be124559e6a84f03b352a143404848596a99aacded6fe91e3150c5eb`  
		Last Modified: Tue, 03 Jun 2025 14:45:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:aa82a1a35cac8440e684fe5059460736ac54ad11d07080afd5fe8fc546806556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.1 KB (118146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc357c735ee41efba1c1c97057f37ee17ce47e28b9887307cbd229d6895da03`

```dockerfile
```

-	Layers:
	-	`sha256:194792c5d362608149275ef412c050bbec126c27232fd4210029e547cac00ae7`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddb88c4acf94b34eadf22eea85377681f766029d1748d93ace4a6a7e7b23538a`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 23.9 KB (23863 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.22` - linux; s390x

```console
$ docker pull memcached@sha256:656e879b0120ed1dc41f4eea945ffd837cbd61df8792d9622df23bb94621dcba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5800523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6248ca4cb8546aea87cb93f6af7f23e99e572b78a8454a9af00758038970fb5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb224b0e357fdb3b8b28a5e9a31cd54bf59197e6b87eff81737fee0cbf2326d1`  
		Last Modified: Tue, 03 Jun 2025 14:45:11 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ffb790e1ad6ec57e858ea0d68a71a20c8d4f1e44cb7d1089e651677c61ff004`  
		Last Modified: Tue, 03 Jun 2025 14:45:11 GMT  
		Size: 113.5 KB (113497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ed9fcfc8c703bdee212b6c00a17c6ea94d9ae8e768825af3a9999a2cc0aa5f`  
		Last Modified: Tue, 03 Jun 2025 14:45:11 GMT  
		Size: 2.0 MB (2038146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d331df3ee94402980d3422bee4dcbd4613703a284b9ccc1fe1f6fdec3f4d869`  
		Last Modified: Tue, 03 Jun 2025 14:45:11 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93af5977e9aba9bde51aba44398ec5690948753fa15a6c35e41208a543d6c2e`  
		Last Modified: Tue, 03 Jun 2025 14:45:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:3dd443c4d6c4cbce2a2b09a2b2869282e7d1478a57e9967b3b38705268315e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.0 KB (118019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538a73a14cc21737f67c2f643b673960e4d7c106988e28fa3bb45734ed83532d`

```dockerfile
```

-	Layers:
	-	`sha256:726d5699c7a6f8c2cc2e05311aefbfc8a4a5369d49388faaf922cdf278a20b7c`  
		Last Modified: Tue, 03 Jun 2025 14:45:12 GMT  
		Size: 94.2 KB (94229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:382c68890507f3d9fe2510636665755df015b0354866ac714c3e70a3201ca87e`  
		Last Modified: Tue, 03 Jun 2025 14:45:11 GMT  
		Size: 23.8 KB (23790 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-bookworm`

```console
$ docker pull memcached@sha256:89b2dfa7e55e5fd1986e22210cdf89f0a5e5d6c913101e2bcfdfb4d1d73de7ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:1-bookworm` - linux; amd64

```console
$ docker pull memcached@sha256:c2b5b37862a0d15d6622bea58a1e3a7a34610456324dc81a6de4e3369d06a5f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33026651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:809ba6b39db15dffb27e2affc4fc5bc5eee2c32ee9b06e08f2f604ee63e41a78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35255ebbfb2408b64a9d53c3d868456872a9b4d89ff4e80f2a8d20c4332dd69`  
		Last Modified: Tue, 10 Jun 2025 23:32:18 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be9410e6aeed64e084cb2812f5d70658e1a9ffe79b5972cea39097c9b949e4e`  
		Last Modified: Tue, 10 Jun 2025 23:32:19 GMT  
		Size: 2.5 MB (2492199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d86227fbbb72b09a47e8016b198dc2062598d3e4c4b358cfa655a2a2c044ef`  
		Last Modified: Tue, 10 Jun 2025 23:32:20 GMT  
		Size: 2.3 MB (2302808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad105488469355bcd85bf5c9c6b74cf9729838da44ad0c6f500f252c6860e8c`  
		Last Modified: Tue, 10 Jun 2025 23:32:20 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90864ece76220d4e897cf79c19145c02ce9d1c1326bb831401963b27ec0ca566`  
		Last Modified: Tue, 10 Jun 2025 23:32:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:5b481897e28479249d51b4c0720b45485fe1952dcb27924f267fcd30d68de833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2425304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6773503e415cd198fe6533c8042593b7aabb0d583e0baf500eed5c4c78452531`

```dockerfile
```

-	Layers:
	-	`sha256:4c6461ec41fb74fe203eb1b6c30c50eddc7f6c11871bfa03eab07db6a4b17c6f`  
		Last Modified: Wed, 11 Jun 2025 00:34:27 GMT  
		Size: 2.4 MB (2399984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e35a57a543fde6b5a8a3e185100a7e9b5ac2a947dea0b7589b5531fab06c67c`  
		Last Modified: Wed, 11 Jun 2025 00:34:28 GMT  
		Size: 25.3 KB (25320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:ca1e51720502c0722aae38efd0a64db105570638d65d6a70ab4572658aff584a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.1 MB (30093253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86fc08738ceff7b24bd461ffd9a41799a048727c6673c1a3c4cb5a01f6b82608`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:750907abe8bb5d66304ed40261e1579b6575871f6848cfbd720888c20afd3b67`  
		Last Modified: Tue, 10 Jun 2025 22:47:31 GMT  
		Size: 25.8 MB (25762396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9660206a4f42b745fdc386aced2845f4fa99b6de361892e4df07c2daf0f24c`  
		Last Modified: Wed, 11 Jun 2025 00:04:16 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877a28dd495fb8632729edaf5b9318ec22ce2a5e402b746782fb7084fd01032c`  
		Last Modified: Wed, 11 Jun 2025 00:04:19 GMT  
		Size: 2.1 MB (2097026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06cb49b999b102d1dc8725fedf17028635be0bcc810a049a03c6e96128a9e4e6`  
		Last Modified: Wed, 11 Jun 2025 00:04:30 GMT  
		Size: 2.2 MB (2232317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee68dfb7714895c5d09887e2708b1296a8855e4ac7ff3d0a158bf029e81e157`  
		Last Modified: Wed, 11 Jun 2025 00:04:39 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff86e8516fa08ad0aa15dfb3afebb40da609006594dcf941ed7900b39cec11aa`  
		Last Modified: Wed, 11 Jun 2025 00:04:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:68162c3dae075d4cb8b6a636c634479c8402119be9f3b6f995913ba4d47162e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2429297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10be7e4ce251f42cb456f15eae67ae97fc6e3040fc50fe0990c4503b35a8829b`

```dockerfile
```

-	Layers:
	-	`sha256:5874edec5896e806374ff905b6f10f3724d44a31a61bf0d830a5ecac4cfbb548`  
		Last Modified: Wed, 11 Jun 2025 03:34:34 GMT  
		Size: 2.4 MB (2403830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54b0ebcaf098420587b0d84ab425ad9abdfc444c86c6ba478b50be7b335cd3c6`  
		Last Modified: Wed, 11 Jun 2025 03:34:34 GMT  
		Size: 25.5 KB (25467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm variant v7

```console
$ docker pull memcached@sha256:d208683140025f905b085b97b35b3a533015b73809d3740e5e3d968c202ec9e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28070929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b74912d1ce300e7a774e690f1c07510c2228991f23ee542e33cc1028e45d90bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6615a784a0e15fd2ed6d79980e68d9cfe87df589b9af6f4c71656286b040acc`  
		Last Modified: Tue, 10 Jun 2025 23:43:55 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66fc152354c58f6024d7e37104e92e718be7b1e70f9745e96e63006f79730f5`  
		Last Modified: Tue, 10 Jun 2025 23:43:56 GMT  
		Size: 1.9 MB (1946292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3712992b59c9c2fa191ca82275b5fb441fcc21940ef625721d0221723f70d9e`  
		Last Modified: Tue, 10 Jun 2025 23:43:56 GMT  
		Size: 2.2 MB (2184378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ba9e36b6e72e151a91cc69343438b9341451e4196d29b259766ab25ece2755`  
		Last Modified: Tue, 10 Jun 2025 23:43:56 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f566ffc3a278d8a018e52b43be1df458ee6632e59b56f75a94a0d058a6cfe73`  
		Last Modified: Tue, 10 Jun 2025 23:43:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:2bbfd653e524ef9316e75f9681ac6876a3e40a63ac124b1e00216760e2855ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2427734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e73cc4fc38d626337d836752990c011dfc545348cb8fd74aa3ae7a39e08c5bc`

```dockerfile
```

-	Layers:
	-	`sha256:8eec2d1ef62751b78959b1e676c070de5b6da4490f0797715b6038816e6ecbe7`  
		Last Modified: Wed, 11 Jun 2025 00:34:36 GMT  
		Size: 2.4 MB (2402267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7bd74b81adae550be8823fda7677f05554265436005a14b9a3f3775ec776a45`  
		Last Modified: Wed, 11 Jun 2025 00:34:37 GMT  
		Size: 25.5 KB (25467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:8a7286d77ae74f81f50dffd6f6e763edd304ed10f5a56e2fe3bdbc38578586a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32723815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05a57428c8257697aa07726f04832bba5278021c4028ea564ada3e7c63bf181`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c5447936c48fe52b15de86391eaf4d170445111319a12dd6f05a85d115b1a4`  
		Last Modified: Wed, 11 Jun 2025 00:32:55 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfca24a3c9155df906544ba98f8bb2bc9f66d9704ed8edf0e731bfe4672420d2`  
		Last Modified: Wed, 11 Jun 2025 00:32:58 GMT  
		Size: 2.4 MB (2355841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eab66920dbc0773d0617dced9ec788e2dc243fc3c3abb0855646922df94744d`  
		Last Modified: Wed, 11 Jun 2025 00:33:04 GMT  
		Size: 2.3 MB (2288782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99014141349bea93d0cf26fd4326ec422f06a635c0ba43644c022fc9960456b8`  
		Last Modified: Wed, 11 Jun 2025 00:33:09 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c855df1fbe1070effdf016a21c2055af95b6325b3e22aa0f32e24d1896dd7a1a`  
		Last Modified: Wed, 11 Jun 2025 00:33:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:45dd4c7b93d5dc7ac1a41023089465fc7feeb3a6878b831308593b595c4453ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2425816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d377887b57b57637deedd7fc6db230aceaeb6f127b9d419649daf5eb921dcfe3`

```dockerfile
```

-	Layers:
	-	`sha256:104fd15db5961a346a71d8c3471d234720c45848fed57ef5c979b5904c13679d`  
		Last Modified: Wed, 11 Jun 2025 03:34:41 GMT  
		Size: 2.4 MB (2400299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b12674469f62c07ff246f7a86cd72871b797a081f0f1a29ebf34768864970340`  
		Last Modified: Wed, 11 Jun 2025 03:34:42 GMT  
		Size: 25.5 KB (25517 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:2fd3408e4989cc9e56a6d3add7ce53181decaf9d7cc19e14b49670b45944e40e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33967948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a326ebe4a452ab75793d01324bf45cdf00e7f2aa83d4793e9993f6317370b81`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c3d46fed134488b3ee18c12cb308c8d5520b8c647122c392f9fb76e3e1e2fc61`  
		Last Modified: Tue, 10 Jun 2025 22:47:25 GMT  
		Size: 29.2 MB (29212433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6e1ece79d563054c9ed24818e5adb5d97e5a1bd3a898d27b10ad0ed0d944fe`  
		Last Modified: Tue, 10 Jun 2025 23:32:02 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d82ab526e835ea99bac51cedfd44fda08d1096806527e0e4776d1747931bfb`  
		Last Modified: Tue, 10 Jun 2025 23:32:03 GMT  
		Size: 2.5 MB (2502688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c26ac869e988fa955c3c084363eb741d506a2034cdd3e12a5c98ff74e4c65c5`  
		Last Modified: Tue, 10 Jun 2025 23:32:03 GMT  
		Size: 2.3 MB (2251313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87ab77943d07e12971b970348f051de5367dd6a2bb147741b63f12eca74d55f`  
		Last Modified: Tue, 10 Jun 2025 23:32:03 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5505b2cac6d2a77393345699695a05426271e871ba824bf0e22789a5cdf44f8e`  
		Last Modified: Tue, 10 Jun 2025 23:32:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f5178b4eff39883c5450012b44b95dc2e13a26e5c3efe2221f9a929a01b99a6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2422389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db0fa4b9612a2b4b5f20852ca646c7fa318ae7057ec68f20599d1281453c0ac5`

```dockerfile
```

-	Layers:
	-	`sha256:27ef430fcb7445f00c5cbbac9416a8082301986670c56b7112c8ee8d2bc7ea63`  
		Last Modified: Wed, 11 Jun 2025 00:34:45 GMT  
		Size: 2.4 MB (2397127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c71e82389c2ff610732d9cc27ec31e1061a1fe683a7594c559d2f0ad1b307bf`  
		Last Modified: Wed, 11 Jun 2025 00:34:46 GMT  
		Size: 25.3 KB (25262 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:4dcc31fdaa97e6430560dfb497e4dde22b2ef368e6c66a3b271a5343bfd86e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32779330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6bba452dff6149dc16dfc6eda06981c4240993be55b9b6f998d30e26935e676`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ac3f61581c7f5755d8598b3a0857c417db0251b17c0e4e4f43a5fc0e24023524`  
		Last Modified: Tue, 10 Jun 2025 22:48:26 GMT  
		Size: 28.5 MB (28516717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b713f027201c7d06c5013a8693a2fb17e64d3d8113328cd83f01c565ddd25a31`  
		Last Modified: Wed, 11 Jun 2025 00:38:45 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699452fffd3fdc6e04d5c6c072d85da568d4477714b34612b15505bebad40576`  
		Last Modified: Wed, 11 Jun 2025 00:38:49 GMT  
		Size: 1.9 MB (1944083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4909573bcae2300d9ad92749c2279eaab07c75210c195cc36bcc323a289711c`  
		Last Modified: Wed, 11 Jun 2025 00:38:54 GMT  
		Size: 2.3 MB (2317017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42800230fbc3a3fdd8ebd615178ea6d750f32c99d916c8d4c1fce650c9724740`  
		Last Modified: Wed, 11 Jun 2025 00:39:03 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc602c2ec2581679f4ba36524612bf709f9828eae2e8e2382a5b72cfe43ddde`  
		Last Modified: Wed, 11 Jun 2025 00:39:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:c8b58a5685ab59a7e412a46fadca1a86a8065cb821c20aa84496f3da2932a6bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d142d271ffff6f14e07b46862b9d5c35a3f62a5ae21f22698dbf2729e22393e5`

```dockerfile
```

-	Layers:
	-	`sha256:0c2d883e7eeaa126767df6696d4d4d21074e1b88388aca7a8d9936e34d972390`  
		Last Modified: Wed, 11 Jun 2025 03:34:48 GMT  
		Size: 25.2 KB (25216 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:ec8926cb7edeb9e447cfa09a6496daf6ddf6214c670db96c915bfbfcdd867a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37203472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f834c7368564e22deca1fec762744af6a328960d29a0757f965efb0922ef2ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c9cd5d5c131a8141631d87d9507a82e0549a2144689442301c07d2da80f39d19`  
		Last Modified: Tue, 10 Jun 2025 23:58:45 GMT  
		Size: 32.1 MB (32072795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783cc02b7ca742bdfa931c46ca74a297d6743f7632079af1d38a86f0ef33e67e`  
		Last Modified: Tue, 10 Jun 2025 23:50:23 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dcb0a6965f82b33b339604c7bfc7e13fddac325187039be9416554f6deaa468`  
		Last Modified: Tue, 10 Jun 2025 23:50:24 GMT  
		Size: 2.7 MB (2710185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460f1a7eb5adf7c13e3a2c6e82959f31bd877cd781b02a5997ba29d421ea0845`  
		Last Modified: Tue, 10 Jun 2025 23:50:24 GMT  
		Size: 2.4 MB (2418981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5dbb0f6f2b188832219b7b4c16a43d53399710d576b050d6939a213e05dd83`  
		Last Modified: Tue, 10 Jun 2025 23:50:24 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ce0fe2674fef821731c0bf8d4218891392e919b579863b73b27c02281d67bb`  
		Last Modified: Tue, 10 Jun 2025 23:50:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:295a95b2a5fbcaba4f0430c8b8fc00ec4ebe4a3ab75480f5ed7890dd086efdc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2429850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd03034a2e56497ce0625f4e0bfba90e28c4d23be1250fe5547dfab3f61abd66`

```dockerfile
```

-	Layers:
	-	`sha256:5e551af8256cd1f6d5d31b7a99d5338c2e0f7c59dd109277d12a1d01c1f8e4dc`  
		Last Modified: Wed, 11 Jun 2025 03:34:53 GMT  
		Size: 2.4 MB (2404456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eac12139332bd876a1e77dd40aa823e07245885fb8a0d33164fd342e6a3198b9`  
		Last Modified: Wed, 11 Jun 2025 03:34:54 GMT  
		Size: 25.4 KB (25394 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:04933adc68fd0a9324a7d5796e1d3cde2a0012644f2ea93c60f0b9ef4f676e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31309863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d59a9f1fa8b8ed5157a51f715aac503833e36e3aa6da498fd68e1647c8366e7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d890a6beb4a310ea4195e7ebd130e37a17b64820c995a543bb5619b2eab1e6`  
		Last Modified: Wed, 11 Jun 2025 09:15:09 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119a4250ae0069dea78d2943d561ab4ad7db7018ddd34dcdf8ceecada8494508`  
		Last Modified: Wed, 11 Jun 2025 09:15:10 GMT  
		Size: 2.2 MB (2156963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eea4eabc325c68a766c64d84b958281150eee02f4ada0091377c9af7b07a793`  
		Last Modified: Wed, 11 Jun 2025 09:15:10 GMT  
		Size: 2.3 MB (2263533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ddbca61153701e80e50122cb3d22cd45a49b4bf191114e8b132b588b077673`  
		Last Modified: Wed, 11 Jun 2025 09:15:10 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42132a3abe6b3ca5bc8e4e623ffa00fe86641a0a42454bba499fa70136dea21`  
		Last Modified: Wed, 11 Jun 2025 09:15:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:2f715ae3a26ddc650f595ca31d33c4a4c14311b1347a6e8d20aca949b131063d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2422126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a4df8b3c359f6d964f37642182e6de7a4cd8cc28676c409e313aa88eaf5b698`

```dockerfile
```

-	Layers:
	-	`sha256:994b93c94dedc6bf0bf79fcfb6b5332c77a3fea69cd945274a1b5eead27d80e0`  
		Last Modified: Wed, 11 Jun 2025 12:34:39 GMT  
		Size: 2.4 MB (2396806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bd4c128777cf5eda46cb5a3ab851f4294546c4b8267f89d17b1adfc4ad5e9bd`  
		Last Modified: Wed, 11 Jun 2025 12:34:40 GMT  
		Size: 25.3 KB (25320 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6`

```console
$ docker pull memcached@sha256:89b2dfa7e55e5fd1986e22210cdf89f0a5e5d6c913101e2bcfdfb4d1d73de7ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:1.6` - linux; amd64

```console
$ docker pull memcached@sha256:c2b5b37862a0d15d6622bea58a1e3a7a34610456324dc81a6de4e3369d06a5f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33026651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:809ba6b39db15dffb27e2affc4fc5bc5eee2c32ee9b06e08f2f604ee63e41a78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35255ebbfb2408b64a9d53c3d868456872a9b4d89ff4e80f2a8d20c4332dd69`  
		Last Modified: Tue, 10 Jun 2025 23:32:18 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be9410e6aeed64e084cb2812f5d70658e1a9ffe79b5972cea39097c9b949e4e`  
		Last Modified: Tue, 10 Jun 2025 23:32:19 GMT  
		Size: 2.5 MB (2492199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d86227fbbb72b09a47e8016b198dc2062598d3e4c4b358cfa655a2a2c044ef`  
		Last Modified: Tue, 10 Jun 2025 23:32:20 GMT  
		Size: 2.3 MB (2302808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad105488469355bcd85bf5c9c6b74cf9729838da44ad0c6f500f252c6860e8c`  
		Last Modified: Tue, 10 Jun 2025 23:32:20 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90864ece76220d4e897cf79c19145c02ce9d1c1326bb831401963b27ec0ca566`  
		Last Modified: Tue, 10 Jun 2025 23:32:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:5b481897e28479249d51b4c0720b45485fe1952dcb27924f267fcd30d68de833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2425304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6773503e415cd198fe6533c8042593b7aabb0d583e0baf500eed5c4c78452531`

```dockerfile
```

-	Layers:
	-	`sha256:4c6461ec41fb74fe203eb1b6c30c50eddc7f6c11871bfa03eab07db6a4b17c6f`  
		Last Modified: Wed, 11 Jun 2025 00:34:27 GMT  
		Size: 2.4 MB (2399984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e35a57a543fde6b5a8a3e185100a7e9b5ac2a947dea0b7589b5531fab06c67c`  
		Last Modified: Wed, 11 Jun 2025 00:34:28 GMT  
		Size: 25.3 KB (25320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:ca1e51720502c0722aae38efd0a64db105570638d65d6a70ab4572658aff584a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.1 MB (30093253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86fc08738ceff7b24bd461ffd9a41799a048727c6673c1a3c4cb5a01f6b82608`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:750907abe8bb5d66304ed40261e1579b6575871f6848cfbd720888c20afd3b67`  
		Last Modified: Tue, 10 Jun 2025 22:47:31 GMT  
		Size: 25.8 MB (25762396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9660206a4f42b745fdc386aced2845f4fa99b6de361892e4df07c2daf0f24c`  
		Last Modified: Wed, 11 Jun 2025 00:04:16 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877a28dd495fb8632729edaf5b9318ec22ce2a5e402b746782fb7084fd01032c`  
		Last Modified: Wed, 11 Jun 2025 00:04:19 GMT  
		Size: 2.1 MB (2097026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06cb49b999b102d1dc8725fedf17028635be0bcc810a049a03c6e96128a9e4e6`  
		Last Modified: Wed, 11 Jun 2025 00:04:30 GMT  
		Size: 2.2 MB (2232317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee68dfb7714895c5d09887e2708b1296a8855e4ac7ff3d0a158bf029e81e157`  
		Last Modified: Wed, 11 Jun 2025 00:04:39 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff86e8516fa08ad0aa15dfb3afebb40da609006594dcf941ed7900b39cec11aa`  
		Last Modified: Wed, 11 Jun 2025 00:04:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:68162c3dae075d4cb8b6a636c634479c8402119be9f3b6f995913ba4d47162e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2429297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10be7e4ce251f42cb456f15eae67ae97fc6e3040fc50fe0990c4503b35a8829b`

```dockerfile
```

-	Layers:
	-	`sha256:5874edec5896e806374ff905b6f10f3724d44a31a61bf0d830a5ecac4cfbb548`  
		Last Modified: Wed, 11 Jun 2025 03:34:34 GMT  
		Size: 2.4 MB (2403830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54b0ebcaf098420587b0d84ab425ad9abdfc444c86c6ba478b50be7b335cd3c6`  
		Last Modified: Wed, 11 Jun 2025 03:34:34 GMT  
		Size: 25.5 KB (25467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v7

```console
$ docker pull memcached@sha256:d208683140025f905b085b97b35b3a533015b73809d3740e5e3d968c202ec9e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28070929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b74912d1ce300e7a774e690f1c07510c2228991f23ee542e33cc1028e45d90bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6615a784a0e15fd2ed6d79980e68d9cfe87df589b9af6f4c71656286b040acc`  
		Last Modified: Tue, 10 Jun 2025 23:43:55 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66fc152354c58f6024d7e37104e92e718be7b1e70f9745e96e63006f79730f5`  
		Last Modified: Tue, 10 Jun 2025 23:43:56 GMT  
		Size: 1.9 MB (1946292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3712992b59c9c2fa191ca82275b5fb441fcc21940ef625721d0221723f70d9e`  
		Last Modified: Tue, 10 Jun 2025 23:43:56 GMT  
		Size: 2.2 MB (2184378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ba9e36b6e72e151a91cc69343438b9341451e4196d29b259766ab25ece2755`  
		Last Modified: Tue, 10 Jun 2025 23:43:56 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f566ffc3a278d8a018e52b43be1df458ee6632e59b56f75a94a0d058a6cfe73`  
		Last Modified: Tue, 10 Jun 2025 23:43:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:2bbfd653e524ef9316e75f9681ac6876a3e40a63ac124b1e00216760e2855ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2427734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e73cc4fc38d626337d836752990c011dfc545348cb8fd74aa3ae7a39e08c5bc`

```dockerfile
```

-	Layers:
	-	`sha256:8eec2d1ef62751b78959b1e676c070de5b6da4490f0797715b6038816e6ecbe7`  
		Last Modified: Wed, 11 Jun 2025 00:34:36 GMT  
		Size: 2.4 MB (2402267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7bd74b81adae550be8823fda7677f05554265436005a14b9a3f3775ec776a45`  
		Last Modified: Wed, 11 Jun 2025 00:34:37 GMT  
		Size: 25.5 KB (25467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:8a7286d77ae74f81f50dffd6f6e763edd304ed10f5a56e2fe3bdbc38578586a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32723815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05a57428c8257697aa07726f04832bba5278021c4028ea564ada3e7c63bf181`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c5447936c48fe52b15de86391eaf4d170445111319a12dd6f05a85d115b1a4`  
		Last Modified: Wed, 11 Jun 2025 00:32:55 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfca24a3c9155df906544ba98f8bb2bc9f66d9704ed8edf0e731bfe4672420d2`  
		Last Modified: Wed, 11 Jun 2025 00:32:58 GMT  
		Size: 2.4 MB (2355841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eab66920dbc0773d0617dced9ec788e2dc243fc3c3abb0855646922df94744d`  
		Last Modified: Wed, 11 Jun 2025 00:33:04 GMT  
		Size: 2.3 MB (2288782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99014141349bea93d0cf26fd4326ec422f06a635c0ba43644c022fc9960456b8`  
		Last Modified: Wed, 11 Jun 2025 00:33:09 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c855df1fbe1070effdf016a21c2055af95b6325b3e22aa0f32e24d1896dd7a1a`  
		Last Modified: Wed, 11 Jun 2025 00:33:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:45dd4c7b93d5dc7ac1a41023089465fc7feeb3a6878b831308593b595c4453ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2425816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d377887b57b57637deedd7fc6db230aceaeb6f127b9d419649daf5eb921dcfe3`

```dockerfile
```

-	Layers:
	-	`sha256:104fd15db5961a346a71d8c3471d234720c45848fed57ef5c979b5904c13679d`  
		Last Modified: Wed, 11 Jun 2025 03:34:41 GMT  
		Size: 2.4 MB (2400299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b12674469f62c07ff246f7a86cd72871b797a081f0f1a29ebf34768864970340`  
		Last Modified: Wed, 11 Jun 2025 03:34:42 GMT  
		Size: 25.5 KB (25517 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; 386

```console
$ docker pull memcached@sha256:2fd3408e4989cc9e56a6d3add7ce53181decaf9d7cc19e14b49670b45944e40e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33967948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a326ebe4a452ab75793d01324bf45cdf00e7f2aa83d4793e9993f6317370b81`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c3d46fed134488b3ee18c12cb308c8d5520b8c647122c392f9fb76e3e1e2fc61`  
		Last Modified: Tue, 10 Jun 2025 22:47:25 GMT  
		Size: 29.2 MB (29212433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6e1ece79d563054c9ed24818e5adb5d97e5a1bd3a898d27b10ad0ed0d944fe`  
		Last Modified: Tue, 10 Jun 2025 23:32:02 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d82ab526e835ea99bac51cedfd44fda08d1096806527e0e4776d1747931bfb`  
		Last Modified: Tue, 10 Jun 2025 23:32:03 GMT  
		Size: 2.5 MB (2502688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c26ac869e988fa955c3c084363eb741d506a2034cdd3e12a5c98ff74e4c65c5`  
		Last Modified: Tue, 10 Jun 2025 23:32:03 GMT  
		Size: 2.3 MB (2251313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87ab77943d07e12971b970348f051de5367dd6a2bb147741b63f12eca74d55f`  
		Last Modified: Tue, 10 Jun 2025 23:32:03 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5505b2cac6d2a77393345699695a05426271e871ba824bf0e22789a5cdf44f8e`  
		Last Modified: Tue, 10 Jun 2025 23:32:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:f5178b4eff39883c5450012b44b95dc2e13a26e5c3efe2221f9a929a01b99a6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2422389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db0fa4b9612a2b4b5f20852ca646c7fa318ae7057ec68f20599d1281453c0ac5`

```dockerfile
```

-	Layers:
	-	`sha256:27ef430fcb7445f00c5cbbac9416a8082301986670c56b7112c8ee8d2bc7ea63`  
		Last Modified: Wed, 11 Jun 2025 00:34:45 GMT  
		Size: 2.4 MB (2397127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c71e82389c2ff610732d9cc27ec31e1061a1fe683a7594c559d2f0ad1b307bf`  
		Last Modified: Wed, 11 Jun 2025 00:34:46 GMT  
		Size: 25.3 KB (25262 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; mips64le

```console
$ docker pull memcached@sha256:4dcc31fdaa97e6430560dfb497e4dde22b2ef368e6c66a3b271a5343bfd86e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32779330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6bba452dff6149dc16dfc6eda06981c4240993be55b9b6f998d30e26935e676`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ac3f61581c7f5755d8598b3a0857c417db0251b17c0e4e4f43a5fc0e24023524`  
		Last Modified: Tue, 10 Jun 2025 22:48:26 GMT  
		Size: 28.5 MB (28516717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b713f027201c7d06c5013a8693a2fb17e64d3d8113328cd83f01c565ddd25a31`  
		Last Modified: Wed, 11 Jun 2025 00:38:45 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699452fffd3fdc6e04d5c6c072d85da568d4477714b34612b15505bebad40576`  
		Last Modified: Wed, 11 Jun 2025 00:38:49 GMT  
		Size: 1.9 MB (1944083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4909573bcae2300d9ad92749c2279eaab07c75210c195cc36bcc323a289711c`  
		Last Modified: Wed, 11 Jun 2025 00:38:54 GMT  
		Size: 2.3 MB (2317017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42800230fbc3a3fdd8ebd615178ea6d750f32c99d916c8d4c1fce650c9724740`  
		Last Modified: Wed, 11 Jun 2025 00:39:03 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc602c2ec2581679f4ba36524612bf709f9828eae2e8e2382a5b72cfe43ddde`  
		Last Modified: Wed, 11 Jun 2025 00:39:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:c8b58a5685ab59a7e412a46fadca1a86a8065cb821c20aa84496f3da2932a6bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d142d271ffff6f14e07b46862b9d5c35a3f62a5ae21f22698dbf2729e22393e5`

```dockerfile
```

-	Layers:
	-	`sha256:0c2d883e7eeaa126767df6696d4d4d21074e1b88388aca7a8d9936e34d972390`  
		Last Modified: Wed, 11 Jun 2025 03:34:48 GMT  
		Size: 25.2 KB (25216 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:ec8926cb7edeb9e447cfa09a6496daf6ddf6214c670db96c915bfbfcdd867a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37203472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f834c7368564e22deca1fec762744af6a328960d29a0757f965efb0922ef2ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c9cd5d5c131a8141631d87d9507a82e0549a2144689442301c07d2da80f39d19`  
		Last Modified: Tue, 10 Jun 2025 23:58:45 GMT  
		Size: 32.1 MB (32072795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783cc02b7ca742bdfa931c46ca74a297d6743f7632079af1d38a86f0ef33e67e`  
		Last Modified: Tue, 10 Jun 2025 23:50:23 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dcb0a6965f82b33b339604c7bfc7e13fddac325187039be9416554f6deaa468`  
		Last Modified: Tue, 10 Jun 2025 23:50:24 GMT  
		Size: 2.7 MB (2710185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460f1a7eb5adf7c13e3a2c6e82959f31bd877cd781b02a5997ba29d421ea0845`  
		Last Modified: Tue, 10 Jun 2025 23:50:24 GMT  
		Size: 2.4 MB (2418981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5dbb0f6f2b188832219b7b4c16a43d53399710d576b050d6939a213e05dd83`  
		Last Modified: Tue, 10 Jun 2025 23:50:24 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ce0fe2674fef821731c0bf8d4218891392e919b579863b73b27c02281d67bb`  
		Last Modified: Tue, 10 Jun 2025 23:50:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:295a95b2a5fbcaba4f0430c8b8fc00ec4ebe4a3ab75480f5ed7890dd086efdc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2429850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd03034a2e56497ce0625f4e0bfba90e28c4d23be1250fe5547dfab3f61abd66`

```dockerfile
```

-	Layers:
	-	`sha256:5e551af8256cd1f6d5d31b7a99d5338c2e0f7c59dd109277d12a1d01c1f8e4dc`  
		Last Modified: Wed, 11 Jun 2025 03:34:53 GMT  
		Size: 2.4 MB (2404456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eac12139332bd876a1e77dd40aa823e07245885fb8a0d33164fd342e6a3198b9`  
		Last Modified: Wed, 11 Jun 2025 03:34:54 GMT  
		Size: 25.4 KB (25394 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; s390x

```console
$ docker pull memcached@sha256:04933adc68fd0a9324a7d5796e1d3cde2a0012644f2ea93c60f0b9ef4f676e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31309863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d59a9f1fa8b8ed5157a51f715aac503833e36e3aa6da498fd68e1647c8366e7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d890a6beb4a310ea4195e7ebd130e37a17b64820c995a543bb5619b2eab1e6`  
		Last Modified: Wed, 11 Jun 2025 09:15:09 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119a4250ae0069dea78d2943d561ab4ad7db7018ddd34dcdf8ceecada8494508`  
		Last Modified: Wed, 11 Jun 2025 09:15:10 GMT  
		Size: 2.2 MB (2156963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eea4eabc325c68a766c64d84b958281150eee02f4ada0091377c9af7b07a793`  
		Last Modified: Wed, 11 Jun 2025 09:15:10 GMT  
		Size: 2.3 MB (2263533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ddbca61153701e80e50122cb3d22cd45a49b4bf191114e8b132b588b077673`  
		Last Modified: Wed, 11 Jun 2025 09:15:10 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42132a3abe6b3ca5bc8e4e623ffa00fe86641a0a42454bba499fa70136dea21`  
		Last Modified: Wed, 11 Jun 2025 09:15:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:2f715ae3a26ddc650f595ca31d33c4a4c14311b1347a6e8d20aca949b131063d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2422126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a4df8b3c359f6d964f37642182e6de7a4cd8cc28676c409e313aa88eaf5b698`

```dockerfile
```

-	Layers:
	-	`sha256:994b93c94dedc6bf0bf79fcfb6b5332c77a3fea69cd945274a1b5eead27d80e0`  
		Last Modified: Wed, 11 Jun 2025 12:34:39 GMT  
		Size: 2.4 MB (2396806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bd4c128777cf5eda46cb5a3ab851f4294546c4b8267f89d17b1adfc4ad5e9bd`  
		Last Modified: Wed, 11 Jun 2025 12:34:40 GMT  
		Size: 25.3 KB (25320 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine`

```console
$ docker pull memcached@sha256:08b6a6cba188fab22215b24a3d5c1ccc18343bc337268f663f20cd86dbdfffeb
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
$ docker pull memcached@sha256:606d01f5580448504043b6ca9994e651efd5cd79822d58639d3f7cb17850fe19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5901265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be94f0135609b0bf7b7f5787294b235034eed9e87be4689825605790d50cff24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef12469432374e0b8bca5dba738c021a8d10c2fc0374275956b8104d92b4053`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b606d4a25237e4f6fe0e5c302a9e8567588be271b95f83da33a31499dac8b0`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 104.7 KB (104728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05dc60670fe6d174274d0896db26274c8ef0e2f77afc45eb51b7cdefceddab51`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 2.0 MB (1998336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa1296a9dd4dfcfb8fcefddbc83edb103f22840e4a193ee7a1e207b232e7338e`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea55364413c47b3f8818b61b2de7d3e3a28b8592bbe25c146ef8a1edf4a17363`  
		Last Modified: Tue, 03 Jun 2025 13:30:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:552c1686ee77c9b7fba7c898a29803c51578a0e80715122dccafcb355025c0de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 KB (119969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb77b32517cfa4aa8e784ef0102259db59c51c349a263d3c87b50ed983fc3ef`

```dockerfile
```

-	Layers:
	-	`sha256:ce2831bada0ca80b430da313ea1ccf45204f6ca84dec4484adbc614b9494be4f`  
		Last Modified: Tue, 03 Jun 2025 14:45:05 GMT  
		Size: 96.2 KB (96180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2114cfbb746c8f95ef4f406bb87b6458f0b23a4844fe5a9774c62c1e9255d42c`  
		Last Modified: Tue, 03 Jun 2025 14:45:05 GMT  
		Size: 23.8 KB (23789 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:41a88acc0a34fb3e7bf86b58cd20dce95d6a609303362364ed6f7f7bd3079880
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6247593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7dfc69a347c50839ad628b964963b8149866c24446202e5789804bc8067e23c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf218c5787338a7792daeaefbb181cf59684549881841831603999e10d5187e`  
		Last Modified: Tue, 03 Jun 2025 13:30:42 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661f41de55d4df851603ae02c2cdc6e73b2ab9a9ecf45eac9b82f105cb482ee1`  
		Last Modified: Tue, 03 Jun 2025 13:32:27 GMT  
		Size: 120.8 KB (120818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e622a5461288686c20e7803ad3d17a45f79a7b140e90b6bbcb6bc8f462c57010`  
		Last Modified: Tue, 03 Jun 2025 13:34:11 GMT  
		Size: 2.0 MB (1989486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd408342d331a0cceff7d0f0d80a5ec8f14ea99c95791d36a29518931ebefb8e`  
		Last Modified: Tue, 03 Jun 2025 13:30:50 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9520bec02cd5779ce2136e2d96c570b84f26641fe4e391f33fb8228c77f4aeac`  
		Last Modified: Tue, 03 Jun 2025 13:30:57 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:e3d2683766797f6a8fe83ea61b5a2979ef33a4d78ea3e0aa9047e37cd2a3fd7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 KB (120271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7447a1da56e995b60bc91c0a003ba4d9d9a6c78fc3a8f9220e19353f0eebc3fc`

```dockerfile
```

-	Layers:
	-	`sha256:ca6f6e30cd21da5e6e9e17e53ca50b541ab1099c4a87acc15081d16797f581c2`  
		Last Modified: Tue, 03 Jun 2025 14:45:05 GMT  
		Size: 96.3 KB (96284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e835bdadfb4d4407a7c5d19b63c33e1f15ec1d83efbabf27ae3e33553a599c2a`  
		Last Modified: Tue, 03 Jun 2025 14:45:05 GMT  
		Size: 24.0 KB (23987 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:39a104f3004fd4a9e820173573ffcc2b15ec2948ca68e6b3d8cfe0e3ecdd12b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5686724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34077a3f17da3a414af6d200ebb8d57c0e73bd8d1d460d1e2ed17e8cc61341c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4498fffb412d9bcc1b73bd7bfa0d2754cf5230f83c22efba4479b1854b502291`  
		Last Modified: Tue, 03 Jun 2025 14:45:06 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7c585852f370434b2f4b564d7ec7ea58c5b06e528ac6b8dffd1212dd6f521e`  
		Last Modified: Tue, 03 Jun 2025 14:45:06 GMT  
		Size: 109.5 KB (109520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc95d14dcefd82bdeb2d89e3ba0fad63fd7fc93194f678a93bc1d9217b9c2ff`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 2.0 MB (1959822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f21560067e099265312c0975371d273829c2923dee88b90d7e24537a458d696`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f53957473f72614ae6b6abc50bff4d20acd3a704edb23755b4e2a5bb6f71a7aa`  
		Last Modified: Tue, 03 Jun 2025 14:45:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:3d21a067c964615eb13e5e591df9d66ea730e3a04be65f71321ad10f1c367d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.9 KB (119867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:897704751afe9189615b739f6bf4308d242df30afe8b42aff038d7828ab081db`

```dockerfile
```

-	Layers:
	-	`sha256:6e6181041c0daeaf47a8f8475f930b1ea73d5cf55a7b5a7b3efba14627e6e8c4`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 96.1 KB (96135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:768c02304a965eacaab05dd9b82b91c453a28d3fbc77b34221ab010ccc28cbcb`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 23.7 KB (23732 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:0bf6f7efe5d3e4b11cec8d17f924ae42d7622e1b0bbcdb56d4757bb3d22ab4b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5947182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf2f7366cf8143a64896b9b751eadad7798b3eec347162fca324567acec20082`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6dc89a1ff7a965251a27c2d9dcb719f464507b964ba3286d6a6034d9f89769`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d75cf13bd9119987f7710d75fd446cd9d065487b3e83297be8c9c4b3120e7e`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 124.3 KB (124312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9461b52977c4cd8b006ffee034043d389554e4c3b267b0901829e7a7a353b8`  
		Last Modified: Tue, 03 Jun 2025 14:45:08 GMT  
		Size: 2.1 MB (2091330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c2dc09d491c7a103b9bd75fa5267b316526d77163130840938eadadb72e6b1`  
		Last Modified: Tue, 03 Jun 2025 14:45:08 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bece68e2cfcb576a9778e7da37d6e2a58ac091bd908caf52a90c4baf09d4d079`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:efd926e1e98c4bedf0db6b24ec177d116548e0652d6b66db54cb2a3e81d21899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 KB (118151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57233506303dd47952c792831142da6a3fe9c4e6c5ea7678ff91b329c08e589`

```dockerfile
```

-	Layers:
	-	`sha256:ed1b26ef88ce71431cfd88a99e6d2d4d13494e7bf5056e489b0b1eb2133d81ab`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 94.3 KB (94287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eaf4c09f8a1fb9991161e85051ae93568c08ab9b2a1142b1bbf99a182e7c0f0`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 23.9 KB (23864 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:aed10964c6cc121d6201aaa8301e269cb88396f19e514ab4529073da9d0c2218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f0390597339801ec08bfd34d10d8bf91dc8e03f2e864f9643758e7ade704d40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db926e6f83170fbe6f646943cb34741a092b9ce5226a6d1bd6b9214d4515055f`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1884ffba96f71fb43c1fef7f0405221b4c8070f55b8667e8b75cc04d268f5cbc`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 107.9 KB (107905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9dea200205fca0caa1f83f40ea69123226bf113407054775efd4a508ae03c65`  
		Last Modified: Tue, 03 Jun 2025 14:45:10 GMT  
		Size: 1.9 MB (1932426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0f27bac94157c911304329980a3ac043834b3407e7ebf8f6a152d114f5949c`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec883045be124559e6a84f03b352a143404848596a99aacded6fe91e3150c5eb`  
		Last Modified: Tue, 03 Jun 2025 14:45:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:aa82a1a35cac8440e684fe5059460736ac54ad11d07080afd5fe8fc546806556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.1 KB (118146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc357c735ee41efba1c1c97057f37ee17ce47e28b9887307cbd229d6895da03`

```dockerfile
```

-	Layers:
	-	`sha256:194792c5d362608149275ef412c050bbec126c27232fd4210029e547cac00ae7`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddb88c4acf94b34eadf22eea85377681f766029d1748d93ace4a6a7e7b23538a`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 23.9 KB (23863 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:656e879b0120ed1dc41f4eea945ffd837cbd61df8792d9622df23bb94621dcba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5800523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6248ca4cb8546aea87cb93f6af7f23e99e572b78a8454a9af00758038970fb5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb224b0e357fdb3b8b28a5e9a31cd54bf59197e6b87eff81737fee0cbf2326d1`  
		Last Modified: Tue, 03 Jun 2025 14:45:11 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ffb790e1ad6ec57e858ea0d68a71a20c8d4f1e44cb7d1089e651677c61ff004`  
		Last Modified: Tue, 03 Jun 2025 14:45:11 GMT  
		Size: 113.5 KB (113497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ed9fcfc8c703bdee212b6c00a17c6ea94d9ae8e768825af3a9999a2cc0aa5f`  
		Last Modified: Tue, 03 Jun 2025 14:45:11 GMT  
		Size: 2.0 MB (2038146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d331df3ee94402980d3422bee4dcbd4613703a284b9ccc1fe1f6fdec3f4d869`  
		Last Modified: Tue, 03 Jun 2025 14:45:11 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93af5977e9aba9bde51aba44398ec5690948753fa15a6c35e41208a543d6c2e`  
		Last Modified: Tue, 03 Jun 2025 14:45:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:3dd443c4d6c4cbce2a2b09a2b2869282e7d1478a57e9967b3b38705268315e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.0 KB (118019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538a73a14cc21737f67c2f643b673960e4d7c106988e28fa3bb45734ed83532d`

```dockerfile
```

-	Layers:
	-	`sha256:726d5699c7a6f8c2cc2e05311aefbfc8a4a5369d49388faaf922cdf278a20b7c`  
		Last Modified: Tue, 03 Jun 2025 14:45:12 GMT  
		Size: 94.2 KB (94229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:382c68890507f3d9fe2510636665755df015b0354866ac714c3e70a3201ca87e`  
		Last Modified: Tue, 03 Jun 2025 14:45:11 GMT  
		Size: 23.8 KB (23790 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine3.22`

```console
$ docker pull memcached@sha256:08b6a6cba188fab22215b24a3d5c1ccc18343bc337268f663f20cd86dbdfffeb
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

### `memcached:1.6-alpine3.22` - linux; amd64

```console
$ docker pull memcached@sha256:606d01f5580448504043b6ca9994e651efd5cd79822d58639d3f7cb17850fe19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5901265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be94f0135609b0bf7b7f5787294b235034eed9e87be4689825605790d50cff24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef12469432374e0b8bca5dba738c021a8d10c2fc0374275956b8104d92b4053`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b606d4a25237e4f6fe0e5c302a9e8567588be271b95f83da33a31499dac8b0`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 104.7 KB (104728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05dc60670fe6d174274d0896db26274c8ef0e2f77afc45eb51b7cdefceddab51`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 2.0 MB (1998336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa1296a9dd4dfcfb8fcefddbc83edb103f22840e4a193ee7a1e207b232e7338e`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea55364413c47b3f8818b61b2de7d3e3a28b8592bbe25c146ef8a1edf4a17363`  
		Last Modified: Tue, 03 Jun 2025 13:30:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:552c1686ee77c9b7fba7c898a29803c51578a0e80715122dccafcb355025c0de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 KB (119969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb77b32517cfa4aa8e784ef0102259db59c51c349a263d3c87b50ed983fc3ef`

```dockerfile
```

-	Layers:
	-	`sha256:ce2831bada0ca80b430da313ea1ccf45204f6ca84dec4484adbc614b9494be4f`  
		Last Modified: Tue, 03 Jun 2025 14:45:05 GMT  
		Size: 96.2 KB (96180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2114cfbb746c8f95ef4f406bb87b6458f0b23a4844fe5a9774c62c1e9255d42c`  
		Last Modified: Tue, 03 Jun 2025 14:45:05 GMT  
		Size: 23.8 KB (23789 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:41a88acc0a34fb3e7bf86b58cd20dce95d6a609303362364ed6f7f7bd3079880
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6247593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7dfc69a347c50839ad628b964963b8149866c24446202e5789804bc8067e23c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf218c5787338a7792daeaefbb181cf59684549881841831603999e10d5187e`  
		Last Modified: Tue, 03 Jun 2025 13:30:42 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661f41de55d4df851603ae02c2cdc6e73b2ab9a9ecf45eac9b82f105cb482ee1`  
		Last Modified: Tue, 03 Jun 2025 13:32:27 GMT  
		Size: 120.8 KB (120818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e622a5461288686c20e7803ad3d17a45f79a7b140e90b6bbcb6bc8f462c57010`  
		Last Modified: Tue, 03 Jun 2025 13:34:11 GMT  
		Size: 2.0 MB (1989486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd408342d331a0cceff7d0f0d80a5ec8f14ea99c95791d36a29518931ebefb8e`  
		Last Modified: Tue, 03 Jun 2025 13:30:50 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9520bec02cd5779ce2136e2d96c570b84f26641fe4e391f33fb8228c77f4aeac`  
		Last Modified: Tue, 03 Jun 2025 13:30:57 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:e3d2683766797f6a8fe83ea61b5a2979ef33a4d78ea3e0aa9047e37cd2a3fd7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 KB (120271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7447a1da56e995b60bc91c0a003ba4d9d9a6c78fc3a8f9220e19353f0eebc3fc`

```dockerfile
```

-	Layers:
	-	`sha256:ca6f6e30cd21da5e6e9e17e53ca50b541ab1099c4a87acc15081d16797f581c2`  
		Last Modified: Tue, 03 Jun 2025 14:45:05 GMT  
		Size: 96.3 KB (96284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e835bdadfb4d4407a7c5d19b63c33e1f15ec1d83efbabf27ae3e33553a599c2a`  
		Last Modified: Tue, 03 Jun 2025 14:45:05 GMT  
		Size: 24.0 KB (23987 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.22` - linux; 386

```console
$ docker pull memcached@sha256:39a104f3004fd4a9e820173573ffcc2b15ec2948ca68e6b3d8cfe0e3ecdd12b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5686724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34077a3f17da3a414af6d200ebb8d57c0e73bd8d1d460d1e2ed17e8cc61341c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4498fffb412d9bcc1b73bd7bfa0d2754cf5230f83c22efba4479b1854b502291`  
		Last Modified: Tue, 03 Jun 2025 14:45:06 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7c585852f370434b2f4b564d7ec7ea58c5b06e528ac6b8dffd1212dd6f521e`  
		Last Modified: Tue, 03 Jun 2025 14:45:06 GMT  
		Size: 109.5 KB (109520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc95d14dcefd82bdeb2d89e3ba0fad63fd7fc93194f678a93bc1d9217b9c2ff`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 2.0 MB (1959822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f21560067e099265312c0975371d273829c2923dee88b90d7e24537a458d696`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f53957473f72614ae6b6abc50bff4d20acd3a704edb23755b4e2a5bb6f71a7aa`  
		Last Modified: Tue, 03 Jun 2025 14:45:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:3d21a067c964615eb13e5e591df9d66ea730e3a04be65f71321ad10f1c367d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.9 KB (119867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:897704751afe9189615b739f6bf4308d242df30afe8b42aff038d7828ab081db`

```dockerfile
```

-	Layers:
	-	`sha256:6e6181041c0daeaf47a8f8475f930b1ea73d5cf55a7b5a7b3efba14627e6e8c4`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 96.1 KB (96135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:768c02304a965eacaab05dd9b82b91c453a28d3fbc77b34221ab010ccc28cbcb`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 23.7 KB (23732 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.22` - linux; ppc64le

```console
$ docker pull memcached@sha256:0bf6f7efe5d3e4b11cec8d17f924ae42d7622e1b0bbcdb56d4757bb3d22ab4b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5947182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf2f7366cf8143a64896b9b751eadad7798b3eec347162fca324567acec20082`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6dc89a1ff7a965251a27c2d9dcb719f464507b964ba3286d6a6034d9f89769`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d75cf13bd9119987f7710d75fd446cd9d065487b3e83297be8c9c4b3120e7e`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 124.3 KB (124312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9461b52977c4cd8b006ffee034043d389554e4c3b267b0901829e7a7a353b8`  
		Last Modified: Tue, 03 Jun 2025 14:45:08 GMT  
		Size: 2.1 MB (2091330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c2dc09d491c7a103b9bd75fa5267b316526d77163130840938eadadb72e6b1`  
		Last Modified: Tue, 03 Jun 2025 14:45:08 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bece68e2cfcb576a9778e7da37d6e2a58ac091bd908caf52a90c4baf09d4d079`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:efd926e1e98c4bedf0db6b24ec177d116548e0652d6b66db54cb2a3e81d21899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 KB (118151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57233506303dd47952c792831142da6a3fe9c4e6c5ea7678ff91b329c08e589`

```dockerfile
```

-	Layers:
	-	`sha256:ed1b26ef88ce71431cfd88a99e6d2d4d13494e7bf5056e489b0b1eb2133d81ab`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 94.3 KB (94287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eaf4c09f8a1fb9991161e85051ae93568c08ab9b2a1142b1bbf99a182e7c0f0`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 23.9 KB (23864 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.22` - linux; riscv64

```console
$ docker pull memcached@sha256:aed10964c6cc121d6201aaa8301e269cb88396f19e514ab4529073da9d0c2218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f0390597339801ec08bfd34d10d8bf91dc8e03f2e864f9643758e7ade704d40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db926e6f83170fbe6f646943cb34741a092b9ce5226a6d1bd6b9214d4515055f`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1884ffba96f71fb43c1fef7f0405221b4c8070f55b8667e8b75cc04d268f5cbc`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 107.9 KB (107905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9dea200205fca0caa1f83f40ea69123226bf113407054775efd4a508ae03c65`  
		Last Modified: Tue, 03 Jun 2025 14:45:10 GMT  
		Size: 1.9 MB (1932426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0f27bac94157c911304329980a3ac043834b3407e7ebf8f6a152d114f5949c`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec883045be124559e6a84f03b352a143404848596a99aacded6fe91e3150c5eb`  
		Last Modified: Tue, 03 Jun 2025 14:45:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:aa82a1a35cac8440e684fe5059460736ac54ad11d07080afd5fe8fc546806556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.1 KB (118146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc357c735ee41efba1c1c97057f37ee17ce47e28b9887307cbd229d6895da03`

```dockerfile
```

-	Layers:
	-	`sha256:194792c5d362608149275ef412c050bbec126c27232fd4210029e547cac00ae7`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddb88c4acf94b34eadf22eea85377681f766029d1748d93ace4a6a7e7b23538a`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 23.9 KB (23863 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.22` - linux; s390x

```console
$ docker pull memcached@sha256:656e879b0120ed1dc41f4eea945ffd837cbd61df8792d9622df23bb94621dcba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5800523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6248ca4cb8546aea87cb93f6af7f23e99e572b78a8454a9af00758038970fb5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb224b0e357fdb3b8b28a5e9a31cd54bf59197e6b87eff81737fee0cbf2326d1`  
		Last Modified: Tue, 03 Jun 2025 14:45:11 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ffb790e1ad6ec57e858ea0d68a71a20c8d4f1e44cb7d1089e651677c61ff004`  
		Last Modified: Tue, 03 Jun 2025 14:45:11 GMT  
		Size: 113.5 KB (113497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ed9fcfc8c703bdee212b6c00a17c6ea94d9ae8e768825af3a9999a2cc0aa5f`  
		Last Modified: Tue, 03 Jun 2025 14:45:11 GMT  
		Size: 2.0 MB (2038146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d331df3ee94402980d3422bee4dcbd4613703a284b9ccc1fe1f6fdec3f4d869`  
		Last Modified: Tue, 03 Jun 2025 14:45:11 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93af5977e9aba9bde51aba44398ec5690948753fa15a6c35e41208a543d6c2e`  
		Last Modified: Tue, 03 Jun 2025 14:45:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:3dd443c4d6c4cbce2a2b09a2b2869282e7d1478a57e9967b3b38705268315e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.0 KB (118019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538a73a14cc21737f67c2f643b673960e4d7c106988e28fa3bb45734ed83532d`

```dockerfile
```

-	Layers:
	-	`sha256:726d5699c7a6f8c2cc2e05311aefbfc8a4a5369d49388faaf922cdf278a20b7c`  
		Last Modified: Tue, 03 Jun 2025 14:45:12 GMT  
		Size: 94.2 KB (94229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:382c68890507f3d9fe2510636665755df015b0354866ac714c3e70a3201ca87e`  
		Last Modified: Tue, 03 Jun 2025 14:45:11 GMT  
		Size: 23.8 KB (23790 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-bookworm`

```console
$ docker pull memcached@sha256:89b2dfa7e55e5fd1986e22210cdf89f0a5e5d6c913101e2bcfdfb4d1d73de7ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:1.6-bookworm` - linux; amd64

```console
$ docker pull memcached@sha256:c2b5b37862a0d15d6622bea58a1e3a7a34610456324dc81a6de4e3369d06a5f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33026651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:809ba6b39db15dffb27e2affc4fc5bc5eee2c32ee9b06e08f2f604ee63e41a78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35255ebbfb2408b64a9d53c3d868456872a9b4d89ff4e80f2a8d20c4332dd69`  
		Last Modified: Tue, 10 Jun 2025 23:32:18 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be9410e6aeed64e084cb2812f5d70658e1a9ffe79b5972cea39097c9b949e4e`  
		Last Modified: Tue, 10 Jun 2025 23:32:19 GMT  
		Size: 2.5 MB (2492199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d86227fbbb72b09a47e8016b198dc2062598d3e4c4b358cfa655a2a2c044ef`  
		Last Modified: Tue, 10 Jun 2025 23:32:20 GMT  
		Size: 2.3 MB (2302808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad105488469355bcd85bf5c9c6b74cf9729838da44ad0c6f500f252c6860e8c`  
		Last Modified: Tue, 10 Jun 2025 23:32:20 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90864ece76220d4e897cf79c19145c02ce9d1c1326bb831401963b27ec0ca566`  
		Last Modified: Tue, 10 Jun 2025 23:32:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:5b481897e28479249d51b4c0720b45485fe1952dcb27924f267fcd30d68de833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2425304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6773503e415cd198fe6533c8042593b7aabb0d583e0baf500eed5c4c78452531`

```dockerfile
```

-	Layers:
	-	`sha256:4c6461ec41fb74fe203eb1b6c30c50eddc7f6c11871bfa03eab07db6a4b17c6f`  
		Last Modified: Wed, 11 Jun 2025 00:34:27 GMT  
		Size: 2.4 MB (2399984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e35a57a543fde6b5a8a3e185100a7e9b5ac2a947dea0b7589b5531fab06c67c`  
		Last Modified: Wed, 11 Jun 2025 00:34:28 GMT  
		Size: 25.3 KB (25320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:ca1e51720502c0722aae38efd0a64db105570638d65d6a70ab4572658aff584a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.1 MB (30093253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86fc08738ceff7b24bd461ffd9a41799a048727c6673c1a3c4cb5a01f6b82608`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:750907abe8bb5d66304ed40261e1579b6575871f6848cfbd720888c20afd3b67`  
		Last Modified: Tue, 10 Jun 2025 22:47:31 GMT  
		Size: 25.8 MB (25762396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9660206a4f42b745fdc386aced2845f4fa99b6de361892e4df07c2daf0f24c`  
		Last Modified: Wed, 11 Jun 2025 00:04:16 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877a28dd495fb8632729edaf5b9318ec22ce2a5e402b746782fb7084fd01032c`  
		Last Modified: Wed, 11 Jun 2025 00:04:19 GMT  
		Size: 2.1 MB (2097026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06cb49b999b102d1dc8725fedf17028635be0bcc810a049a03c6e96128a9e4e6`  
		Last Modified: Wed, 11 Jun 2025 00:04:30 GMT  
		Size: 2.2 MB (2232317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee68dfb7714895c5d09887e2708b1296a8855e4ac7ff3d0a158bf029e81e157`  
		Last Modified: Wed, 11 Jun 2025 00:04:39 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff86e8516fa08ad0aa15dfb3afebb40da609006594dcf941ed7900b39cec11aa`  
		Last Modified: Wed, 11 Jun 2025 00:04:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:68162c3dae075d4cb8b6a636c634479c8402119be9f3b6f995913ba4d47162e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2429297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10be7e4ce251f42cb456f15eae67ae97fc6e3040fc50fe0990c4503b35a8829b`

```dockerfile
```

-	Layers:
	-	`sha256:5874edec5896e806374ff905b6f10f3724d44a31a61bf0d830a5ecac4cfbb548`  
		Last Modified: Wed, 11 Jun 2025 03:34:34 GMT  
		Size: 2.4 MB (2403830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54b0ebcaf098420587b0d84ab425ad9abdfc444c86c6ba478b50be7b335cd3c6`  
		Last Modified: Wed, 11 Jun 2025 03:34:34 GMT  
		Size: 25.5 KB (25467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm variant v7

```console
$ docker pull memcached@sha256:d208683140025f905b085b97b35b3a533015b73809d3740e5e3d968c202ec9e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28070929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b74912d1ce300e7a774e690f1c07510c2228991f23ee542e33cc1028e45d90bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6615a784a0e15fd2ed6d79980e68d9cfe87df589b9af6f4c71656286b040acc`  
		Last Modified: Tue, 10 Jun 2025 23:43:55 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66fc152354c58f6024d7e37104e92e718be7b1e70f9745e96e63006f79730f5`  
		Last Modified: Tue, 10 Jun 2025 23:43:56 GMT  
		Size: 1.9 MB (1946292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3712992b59c9c2fa191ca82275b5fb441fcc21940ef625721d0221723f70d9e`  
		Last Modified: Tue, 10 Jun 2025 23:43:56 GMT  
		Size: 2.2 MB (2184378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ba9e36b6e72e151a91cc69343438b9341451e4196d29b259766ab25ece2755`  
		Last Modified: Tue, 10 Jun 2025 23:43:56 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f566ffc3a278d8a018e52b43be1df458ee6632e59b56f75a94a0d058a6cfe73`  
		Last Modified: Tue, 10 Jun 2025 23:43:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:2bbfd653e524ef9316e75f9681ac6876a3e40a63ac124b1e00216760e2855ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2427734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e73cc4fc38d626337d836752990c011dfc545348cb8fd74aa3ae7a39e08c5bc`

```dockerfile
```

-	Layers:
	-	`sha256:8eec2d1ef62751b78959b1e676c070de5b6da4490f0797715b6038816e6ecbe7`  
		Last Modified: Wed, 11 Jun 2025 00:34:36 GMT  
		Size: 2.4 MB (2402267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7bd74b81adae550be8823fda7677f05554265436005a14b9a3f3775ec776a45`  
		Last Modified: Wed, 11 Jun 2025 00:34:37 GMT  
		Size: 25.5 KB (25467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:8a7286d77ae74f81f50dffd6f6e763edd304ed10f5a56e2fe3bdbc38578586a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32723815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05a57428c8257697aa07726f04832bba5278021c4028ea564ada3e7c63bf181`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c5447936c48fe52b15de86391eaf4d170445111319a12dd6f05a85d115b1a4`  
		Last Modified: Wed, 11 Jun 2025 00:32:55 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfca24a3c9155df906544ba98f8bb2bc9f66d9704ed8edf0e731bfe4672420d2`  
		Last Modified: Wed, 11 Jun 2025 00:32:58 GMT  
		Size: 2.4 MB (2355841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eab66920dbc0773d0617dced9ec788e2dc243fc3c3abb0855646922df94744d`  
		Last Modified: Wed, 11 Jun 2025 00:33:04 GMT  
		Size: 2.3 MB (2288782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99014141349bea93d0cf26fd4326ec422f06a635c0ba43644c022fc9960456b8`  
		Last Modified: Wed, 11 Jun 2025 00:33:09 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c855df1fbe1070effdf016a21c2055af95b6325b3e22aa0f32e24d1896dd7a1a`  
		Last Modified: Wed, 11 Jun 2025 00:33:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:45dd4c7b93d5dc7ac1a41023089465fc7feeb3a6878b831308593b595c4453ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2425816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d377887b57b57637deedd7fc6db230aceaeb6f127b9d419649daf5eb921dcfe3`

```dockerfile
```

-	Layers:
	-	`sha256:104fd15db5961a346a71d8c3471d234720c45848fed57ef5c979b5904c13679d`  
		Last Modified: Wed, 11 Jun 2025 03:34:41 GMT  
		Size: 2.4 MB (2400299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b12674469f62c07ff246f7a86cd72871b797a081f0f1a29ebf34768864970340`  
		Last Modified: Wed, 11 Jun 2025 03:34:42 GMT  
		Size: 25.5 KB (25517 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:2fd3408e4989cc9e56a6d3add7ce53181decaf9d7cc19e14b49670b45944e40e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33967948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a326ebe4a452ab75793d01324bf45cdf00e7f2aa83d4793e9993f6317370b81`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c3d46fed134488b3ee18c12cb308c8d5520b8c647122c392f9fb76e3e1e2fc61`  
		Last Modified: Tue, 10 Jun 2025 22:47:25 GMT  
		Size: 29.2 MB (29212433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6e1ece79d563054c9ed24818e5adb5d97e5a1bd3a898d27b10ad0ed0d944fe`  
		Last Modified: Tue, 10 Jun 2025 23:32:02 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d82ab526e835ea99bac51cedfd44fda08d1096806527e0e4776d1747931bfb`  
		Last Modified: Tue, 10 Jun 2025 23:32:03 GMT  
		Size: 2.5 MB (2502688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c26ac869e988fa955c3c084363eb741d506a2034cdd3e12a5c98ff74e4c65c5`  
		Last Modified: Tue, 10 Jun 2025 23:32:03 GMT  
		Size: 2.3 MB (2251313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87ab77943d07e12971b970348f051de5367dd6a2bb147741b63f12eca74d55f`  
		Last Modified: Tue, 10 Jun 2025 23:32:03 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5505b2cac6d2a77393345699695a05426271e871ba824bf0e22789a5cdf44f8e`  
		Last Modified: Tue, 10 Jun 2025 23:32:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f5178b4eff39883c5450012b44b95dc2e13a26e5c3efe2221f9a929a01b99a6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2422389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db0fa4b9612a2b4b5f20852ca646c7fa318ae7057ec68f20599d1281453c0ac5`

```dockerfile
```

-	Layers:
	-	`sha256:27ef430fcb7445f00c5cbbac9416a8082301986670c56b7112c8ee8d2bc7ea63`  
		Last Modified: Wed, 11 Jun 2025 00:34:45 GMT  
		Size: 2.4 MB (2397127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c71e82389c2ff610732d9cc27ec31e1061a1fe683a7594c559d2f0ad1b307bf`  
		Last Modified: Wed, 11 Jun 2025 00:34:46 GMT  
		Size: 25.3 KB (25262 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:4dcc31fdaa97e6430560dfb497e4dde22b2ef368e6c66a3b271a5343bfd86e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32779330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6bba452dff6149dc16dfc6eda06981c4240993be55b9b6f998d30e26935e676`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ac3f61581c7f5755d8598b3a0857c417db0251b17c0e4e4f43a5fc0e24023524`  
		Last Modified: Tue, 10 Jun 2025 22:48:26 GMT  
		Size: 28.5 MB (28516717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b713f027201c7d06c5013a8693a2fb17e64d3d8113328cd83f01c565ddd25a31`  
		Last Modified: Wed, 11 Jun 2025 00:38:45 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699452fffd3fdc6e04d5c6c072d85da568d4477714b34612b15505bebad40576`  
		Last Modified: Wed, 11 Jun 2025 00:38:49 GMT  
		Size: 1.9 MB (1944083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4909573bcae2300d9ad92749c2279eaab07c75210c195cc36bcc323a289711c`  
		Last Modified: Wed, 11 Jun 2025 00:38:54 GMT  
		Size: 2.3 MB (2317017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42800230fbc3a3fdd8ebd615178ea6d750f32c99d916c8d4c1fce650c9724740`  
		Last Modified: Wed, 11 Jun 2025 00:39:03 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc602c2ec2581679f4ba36524612bf709f9828eae2e8e2382a5b72cfe43ddde`  
		Last Modified: Wed, 11 Jun 2025 00:39:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:c8b58a5685ab59a7e412a46fadca1a86a8065cb821c20aa84496f3da2932a6bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d142d271ffff6f14e07b46862b9d5c35a3f62a5ae21f22698dbf2729e22393e5`

```dockerfile
```

-	Layers:
	-	`sha256:0c2d883e7eeaa126767df6696d4d4d21074e1b88388aca7a8d9936e34d972390`  
		Last Modified: Wed, 11 Jun 2025 03:34:48 GMT  
		Size: 25.2 KB (25216 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:ec8926cb7edeb9e447cfa09a6496daf6ddf6214c670db96c915bfbfcdd867a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37203472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f834c7368564e22deca1fec762744af6a328960d29a0757f965efb0922ef2ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c9cd5d5c131a8141631d87d9507a82e0549a2144689442301c07d2da80f39d19`  
		Last Modified: Tue, 10 Jun 2025 23:58:45 GMT  
		Size: 32.1 MB (32072795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783cc02b7ca742bdfa931c46ca74a297d6743f7632079af1d38a86f0ef33e67e`  
		Last Modified: Tue, 10 Jun 2025 23:50:23 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dcb0a6965f82b33b339604c7bfc7e13fddac325187039be9416554f6deaa468`  
		Last Modified: Tue, 10 Jun 2025 23:50:24 GMT  
		Size: 2.7 MB (2710185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460f1a7eb5adf7c13e3a2c6e82959f31bd877cd781b02a5997ba29d421ea0845`  
		Last Modified: Tue, 10 Jun 2025 23:50:24 GMT  
		Size: 2.4 MB (2418981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5dbb0f6f2b188832219b7b4c16a43d53399710d576b050d6939a213e05dd83`  
		Last Modified: Tue, 10 Jun 2025 23:50:24 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ce0fe2674fef821731c0bf8d4218891392e919b579863b73b27c02281d67bb`  
		Last Modified: Tue, 10 Jun 2025 23:50:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:295a95b2a5fbcaba4f0430c8b8fc00ec4ebe4a3ab75480f5ed7890dd086efdc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2429850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd03034a2e56497ce0625f4e0bfba90e28c4d23be1250fe5547dfab3f61abd66`

```dockerfile
```

-	Layers:
	-	`sha256:5e551af8256cd1f6d5d31b7a99d5338c2e0f7c59dd109277d12a1d01c1f8e4dc`  
		Last Modified: Wed, 11 Jun 2025 03:34:53 GMT  
		Size: 2.4 MB (2404456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eac12139332bd876a1e77dd40aa823e07245885fb8a0d33164fd342e6a3198b9`  
		Last Modified: Wed, 11 Jun 2025 03:34:54 GMT  
		Size: 25.4 KB (25394 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:04933adc68fd0a9324a7d5796e1d3cde2a0012644f2ea93c60f0b9ef4f676e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31309863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d59a9f1fa8b8ed5157a51f715aac503833e36e3aa6da498fd68e1647c8366e7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d890a6beb4a310ea4195e7ebd130e37a17b64820c995a543bb5619b2eab1e6`  
		Last Modified: Wed, 11 Jun 2025 09:15:09 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119a4250ae0069dea78d2943d561ab4ad7db7018ddd34dcdf8ceecada8494508`  
		Last Modified: Wed, 11 Jun 2025 09:15:10 GMT  
		Size: 2.2 MB (2156963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eea4eabc325c68a766c64d84b958281150eee02f4ada0091377c9af7b07a793`  
		Last Modified: Wed, 11 Jun 2025 09:15:10 GMT  
		Size: 2.3 MB (2263533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ddbca61153701e80e50122cb3d22cd45a49b4bf191114e8b132b588b077673`  
		Last Modified: Wed, 11 Jun 2025 09:15:10 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42132a3abe6b3ca5bc8e4e623ffa00fe86641a0a42454bba499fa70136dea21`  
		Last Modified: Wed, 11 Jun 2025 09:15:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:2f715ae3a26ddc650f595ca31d33c4a4c14311b1347a6e8d20aca949b131063d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2422126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a4df8b3c359f6d964f37642182e6de7a4cd8cc28676c409e313aa88eaf5b698`

```dockerfile
```

-	Layers:
	-	`sha256:994b93c94dedc6bf0bf79fcfb6b5332c77a3fea69cd945274a1b5eead27d80e0`  
		Last Modified: Wed, 11 Jun 2025 12:34:39 GMT  
		Size: 2.4 MB (2396806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bd4c128777cf5eda46cb5a3ab851f4294546c4b8267f89d17b1adfc4ad5e9bd`  
		Last Modified: Wed, 11 Jun 2025 12:34:40 GMT  
		Size: 25.3 KB (25320 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.38`

```console
$ docker pull memcached@sha256:89b2dfa7e55e5fd1986e22210cdf89f0a5e5d6c913101e2bcfdfb4d1d73de7ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:1.6.38` - linux; amd64

```console
$ docker pull memcached@sha256:c2b5b37862a0d15d6622bea58a1e3a7a34610456324dc81a6de4e3369d06a5f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33026651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:809ba6b39db15dffb27e2affc4fc5bc5eee2c32ee9b06e08f2f604ee63e41a78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35255ebbfb2408b64a9d53c3d868456872a9b4d89ff4e80f2a8d20c4332dd69`  
		Last Modified: Tue, 10 Jun 2025 23:32:18 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be9410e6aeed64e084cb2812f5d70658e1a9ffe79b5972cea39097c9b949e4e`  
		Last Modified: Tue, 10 Jun 2025 23:32:19 GMT  
		Size: 2.5 MB (2492199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d86227fbbb72b09a47e8016b198dc2062598d3e4c4b358cfa655a2a2c044ef`  
		Last Modified: Tue, 10 Jun 2025 23:32:20 GMT  
		Size: 2.3 MB (2302808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad105488469355bcd85bf5c9c6b74cf9729838da44ad0c6f500f252c6860e8c`  
		Last Modified: Tue, 10 Jun 2025 23:32:20 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90864ece76220d4e897cf79c19145c02ce9d1c1326bb831401963b27ec0ca566`  
		Last Modified: Tue, 10 Jun 2025 23:32:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38` - unknown; unknown

```console
$ docker pull memcached@sha256:5b481897e28479249d51b4c0720b45485fe1952dcb27924f267fcd30d68de833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2425304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6773503e415cd198fe6533c8042593b7aabb0d583e0baf500eed5c4c78452531`

```dockerfile
```

-	Layers:
	-	`sha256:4c6461ec41fb74fe203eb1b6c30c50eddc7f6c11871bfa03eab07db6a4b17c6f`  
		Last Modified: Wed, 11 Jun 2025 00:34:27 GMT  
		Size: 2.4 MB (2399984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e35a57a543fde6b5a8a3e185100a7e9b5ac2a947dea0b7589b5531fab06c67c`  
		Last Modified: Wed, 11 Jun 2025 00:34:28 GMT  
		Size: 25.3 KB (25320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38` - linux; arm variant v5

```console
$ docker pull memcached@sha256:ca1e51720502c0722aae38efd0a64db105570638d65d6a70ab4572658aff584a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.1 MB (30093253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86fc08738ceff7b24bd461ffd9a41799a048727c6673c1a3c4cb5a01f6b82608`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:750907abe8bb5d66304ed40261e1579b6575871f6848cfbd720888c20afd3b67`  
		Last Modified: Tue, 10 Jun 2025 22:47:31 GMT  
		Size: 25.8 MB (25762396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9660206a4f42b745fdc386aced2845f4fa99b6de361892e4df07c2daf0f24c`  
		Last Modified: Wed, 11 Jun 2025 00:04:16 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877a28dd495fb8632729edaf5b9318ec22ce2a5e402b746782fb7084fd01032c`  
		Last Modified: Wed, 11 Jun 2025 00:04:19 GMT  
		Size: 2.1 MB (2097026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06cb49b999b102d1dc8725fedf17028635be0bcc810a049a03c6e96128a9e4e6`  
		Last Modified: Wed, 11 Jun 2025 00:04:30 GMT  
		Size: 2.2 MB (2232317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee68dfb7714895c5d09887e2708b1296a8855e4ac7ff3d0a158bf029e81e157`  
		Last Modified: Wed, 11 Jun 2025 00:04:39 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff86e8516fa08ad0aa15dfb3afebb40da609006594dcf941ed7900b39cec11aa`  
		Last Modified: Wed, 11 Jun 2025 00:04:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38` - unknown; unknown

```console
$ docker pull memcached@sha256:68162c3dae075d4cb8b6a636c634479c8402119be9f3b6f995913ba4d47162e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2429297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10be7e4ce251f42cb456f15eae67ae97fc6e3040fc50fe0990c4503b35a8829b`

```dockerfile
```

-	Layers:
	-	`sha256:5874edec5896e806374ff905b6f10f3724d44a31a61bf0d830a5ecac4cfbb548`  
		Last Modified: Wed, 11 Jun 2025 03:34:34 GMT  
		Size: 2.4 MB (2403830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54b0ebcaf098420587b0d84ab425ad9abdfc444c86c6ba478b50be7b335cd3c6`  
		Last Modified: Wed, 11 Jun 2025 03:34:34 GMT  
		Size: 25.5 KB (25467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38` - linux; arm variant v7

```console
$ docker pull memcached@sha256:d208683140025f905b085b97b35b3a533015b73809d3740e5e3d968c202ec9e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28070929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b74912d1ce300e7a774e690f1c07510c2228991f23ee542e33cc1028e45d90bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6615a784a0e15fd2ed6d79980e68d9cfe87df589b9af6f4c71656286b040acc`  
		Last Modified: Tue, 10 Jun 2025 23:43:55 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66fc152354c58f6024d7e37104e92e718be7b1e70f9745e96e63006f79730f5`  
		Last Modified: Tue, 10 Jun 2025 23:43:56 GMT  
		Size: 1.9 MB (1946292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3712992b59c9c2fa191ca82275b5fb441fcc21940ef625721d0221723f70d9e`  
		Last Modified: Tue, 10 Jun 2025 23:43:56 GMT  
		Size: 2.2 MB (2184378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ba9e36b6e72e151a91cc69343438b9341451e4196d29b259766ab25ece2755`  
		Last Modified: Tue, 10 Jun 2025 23:43:56 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f566ffc3a278d8a018e52b43be1df458ee6632e59b56f75a94a0d058a6cfe73`  
		Last Modified: Tue, 10 Jun 2025 23:43:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38` - unknown; unknown

```console
$ docker pull memcached@sha256:2bbfd653e524ef9316e75f9681ac6876a3e40a63ac124b1e00216760e2855ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2427734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e73cc4fc38d626337d836752990c011dfc545348cb8fd74aa3ae7a39e08c5bc`

```dockerfile
```

-	Layers:
	-	`sha256:8eec2d1ef62751b78959b1e676c070de5b6da4490f0797715b6038816e6ecbe7`  
		Last Modified: Wed, 11 Jun 2025 00:34:36 GMT  
		Size: 2.4 MB (2402267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7bd74b81adae550be8823fda7677f05554265436005a14b9a3f3775ec776a45`  
		Last Modified: Wed, 11 Jun 2025 00:34:37 GMT  
		Size: 25.5 KB (25467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:8a7286d77ae74f81f50dffd6f6e763edd304ed10f5a56e2fe3bdbc38578586a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32723815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05a57428c8257697aa07726f04832bba5278021c4028ea564ada3e7c63bf181`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c5447936c48fe52b15de86391eaf4d170445111319a12dd6f05a85d115b1a4`  
		Last Modified: Wed, 11 Jun 2025 00:32:55 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfca24a3c9155df906544ba98f8bb2bc9f66d9704ed8edf0e731bfe4672420d2`  
		Last Modified: Wed, 11 Jun 2025 00:32:58 GMT  
		Size: 2.4 MB (2355841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eab66920dbc0773d0617dced9ec788e2dc243fc3c3abb0855646922df94744d`  
		Last Modified: Wed, 11 Jun 2025 00:33:04 GMT  
		Size: 2.3 MB (2288782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99014141349bea93d0cf26fd4326ec422f06a635c0ba43644c022fc9960456b8`  
		Last Modified: Wed, 11 Jun 2025 00:33:09 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c855df1fbe1070effdf016a21c2055af95b6325b3e22aa0f32e24d1896dd7a1a`  
		Last Modified: Wed, 11 Jun 2025 00:33:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38` - unknown; unknown

```console
$ docker pull memcached@sha256:45dd4c7b93d5dc7ac1a41023089465fc7feeb3a6878b831308593b595c4453ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2425816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d377887b57b57637deedd7fc6db230aceaeb6f127b9d419649daf5eb921dcfe3`

```dockerfile
```

-	Layers:
	-	`sha256:104fd15db5961a346a71d8c3471d234720c45848fed57ef5c979b5904c13679d`  
		Last Modified: Wed, 11 Jun 2025 03:34:41 GMT  
		Size: 2.4 MB (2400299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b12674469f62c07ff246f7a86cd72871b797a081f0f1a29ebf34768864970340`  
		Last Modified: Wed, 11 Jun 2025 03:34:42 GMT  
		Size: 25.5 KB (25517 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38` - linux; 386

```console
$ docker pull memcached@sha256:2fd3408e4989cc9e56a6d3add7ce53181decaf9d7cc19e14b49670b45944e40e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33967948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a326ebe4a452ab75793d01324bf45cdf00e7f2aa83d4793e9993f6317370b81`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c3d46fed134488b3ee18c12cb308c8d5520b8c647122c392f9fb76e3e1e2fc61`  
		Last Modified: Tue, 10 Jun 2025 22:47:25 GMT  
		Size: 29.2 MB (29212433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6e1ece79d563054c9ed24818e5adb5d97e5a1bd3a898d27b10ad0ed0d944fe`  
		Last Modified: Tue, 10 Jun 2025 23:32:02 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d82ab526e835ea99bac51cedfd44fda08d1096806527e0e4776d1747931bfb`  
		Last Modified: Tue, 10 Jun 2025 23:32:03 GMT  
		Size: 2.5 MB (2502688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c26ac869e988fa955c3c084363eb741d506a2034cdd3e12a5c98ff74e4c65c5`  
		Last Modified: Tue, 10 Jun 2025 23:32:03 GMT  
		Size: 2.3 MB (2251313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87ab77943d07e12971b970348f051de5367dd6a2bb147741b63f12eca74d55f`  
		Last Modified: Tue, 10 Jun 2025 23:32:03 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5505b2cac6d2a77393345699695a05426271e871ba824bf0e22789a5cdf44f8e`  
		Last Modified: Tue, 10 Jun 2025 23:32:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38` - unknown; unknown

```console
$ docker pull memcached@sha256:f5178b4eff39883c5450012b44b95dc2e13a26e5c3efe2221f9a929a01b99a6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2422389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db0fa4b9612a2b4b5f20852ca646c7fa318ae7057ec68f20599d1281453c0ac5`

```dockerfile
```

-	Layers:
	-	`sha256:27ef430fcb7445f00c5cbbac9416a8082301986670c56b7112c8ee8d2bc7ea63`  
		Last Modified: Wed, 11 Jun 2025 00:34:45 GMT  
		Size: 2.4 MB (2397127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c71e82389c2ff610732d9cc27ec31e1061a1fe683a7594c559d2f0ad1b307bf`  
		Last Modified: Wed, 11 Jun 2025 00:34:46 GMT  
		Size: 25.3 KB (25262 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38` - linux; mips64le

```console
$ docker pull memcached@sha256:4dcc31fdaa97e6430560dfb497e4dde22b2ef368e6c66a3b271a5343bfd86e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32779330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6bba452dff6149dc16dfc6eda06981c4240993be55b9b6f998d30e26935e676`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ac3f61581c7f5755d8598b3a0857c417db0251b17c0e4e4f43a5fc0e24023524`  
		Last Modified: Tue, 10 Jun 2025 22:48:26 GMT  
		Size: 28.5 MB (28516717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b713f027201c7d06c5013a8693a2fb17e64d3d8113328cd83f01c565ddd25a31`  
		Last Modified: Wed, 11 Jun 2025 00:38:45 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699452fffd3fdc6e04d5c6c072d85da568d4477714b34612b15505bebad40576`  
		Last Modified: Wed, 11 Jun 2025 00:38:49 GMT  
		Size: 1.9 MB (1944083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4909573bcae2300d9ad92749c2279eaab07c75210c195cc36bcc323a289711c`  
		Last Modified: Wed, 11 Jun 2025 00:38:54 GMT  
		Size: 2.3 MB (2317017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42800230fbc3a3fdd8ebd615178ea6d750f32c99d916c8d4c1fce650c9724740`  
		Last Modified: Wed, 11 Jun 2025 00:39:03 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc602c2ec2581679f4ba36524612bf709f9828eae2e8e2382a5b72cfe43ddde`  
		Last Modified: Wed, 11 Jun 2025 00:39:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38` - unknown; unknown

```console
$ docker pull memcached@sha256:c8b58a5685ab59a7e412a46fadca1a86a8065cb821c20aa84496f3da2932a6bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d142d271ffff6f14e07b46862b9d5c35a3f62a5ae21f22698dbf2729e22393e5`

```dockerfile
```

-	Layers:
	-	`sha256:0c2d883e7eeaa126767df6696d4d4d21074e1b88388aca7a8d9936e34d972390`  
		Last Modified: Wed, 11 Jun 2025 03:34:48 GMT  
		Size: 25.2 KB (25216 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38` - linux; ppc64le

```console
$ docker pull memcached@sha256:ec8926cb7edeb9e447cfa09a6496daf6ddf6214c670db96c915bfbfcdd867a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37203472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f834c7368564e22deca1fec762744af6a328960d29a0757f965efb0922ef2ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c9cd5d5c131a8141631d87d9507a82e0549a2144689442301c07d2da80f39d19`  
		Last Modified: Tue, 10 Jun 2025 23:58:45 GMT  
		Size: 32.1 MB (32072795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783cc02b7ca742bdfa931c46ca74a297d6743f7632079af1d38a86f0ef33e67e`  
		Last Modified: Tue, 10 Jun 2025 23:50:23 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dcb0a6965f82b33b339604c7bfc7e13fddac325187039be9416554f6deaa468`  
		Last Modified: Tue, 10 Jun 2025 23:50:24 GMT  
		Size: 2.7 MB (2710185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460f1a7eb5adf7c13e3a2c6e82959f31bd877cd781b02a5997ba29d421ea0845`  
		Last Modified: Tue, 10 Jun 2025 23:50:24 GMT  
		Size: 2.4 MB (2418981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5dbb0f6f2b188832219b7b4c16a43d53399710d576b050d6939a213e05dd83`  
		Last Modified: Tue, 10 Jun 2025 23:50:24 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ce0fe2674fef821731c0bf8d4218891392e919b579863b73b27c02281d67bb`  
		Last Modified: Tue, 10 Jun 2025 23:50:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38` - unknown; unknown

```console
$ docker pull memcached@sha256:295a95b2a5fbcaba4f0430c8b8fc00ec4ebe4a3ab75480f5ed7890dd086efdc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2429850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd03034a2e56497ce0625f4e0bfba90e28c4d23be1250fe5547dfab3f61abd66`

```dockerfile
```

-	Layers:
	-	`sha256:5e551af8256cd1f6d5d31b7a99d5338c2e0f7c59dd109277d12a1d01c1f8e4dc`  
		Last Modified: Wed, 11 Jun 2025 03:34:53 GMT  
		Size: 2.4 MB (2404456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eac12139332bd876a1e77dd40aa823e07245885fb8a0d33164fd342e6a3198b9`  
		Last Modified: Wed, 11 Jun 2025 03:34:54 GMT  
		Size: 25.4 KB (25394 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38` - linux; s390x

```console
$ docker pull memcached@sha256:04933adc68fd0a9324a7d5796e1d3cde2a0012644f2ea93c60f0b9ef4f676e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31309863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d59a9f1fa8b8ed5157a51f715aac503833e36e3aa6da498fd68e1647c8366e7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d890a6beb4a310ea4195e7ebd130e37a17b64820c995a543bb5619b2eab1e6`  
		Last Modified: Wed, 11 Jun 2025 09:15:09 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119a4250ae0069dea78d2943d561ab4ad7db7018ddd34dcdf8ceecada8494508`  
		Last Modified: Wed, 11 Jun 2025 09:15:10 GMT  
		Size: 2.2 MB (2156963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eea4eabc325c68a766c64d84b958281150eee02f4ada0091377c9af7b07a793`  
		Last Modified: Wed, 11 Jun 2025 09:15:10 GMT  
		Size: 2.3 MB (2263533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ddbca61153701e80e50122cb3d22cd45a49b4bf191114e8b132b588b077673`  
		Last Modified: Wed, 11 Jun 2025 09:15:10 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42132a3abe6b3ca5bc8e4e623ffa00fe86641a0a42454bba499fa70136dea21`  
		Last Modified: Wed, 11 Jun 2025 09:15:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38` - unknown; unknown

```console
$ docker pull memcached@sha256:2f715ae3a26ddc650f595ca31d33c4a4c14311b1347a6e8d20aca949b131063d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2422126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a4df8b3c359f6d964f37642182e6de7a4cd8cc28676c409e313aa88eaf5b698`

```dockerfile
```

-	Layers:
	-	`sha256:994b93c94dedc6bf0bf79fcfb6b5332c77a3fea69cd945274a1b5eead27d80e0`  
		Last Modified: Wed, 11 Jun 2025 12:34:39 GMT  
		Size: 2.4 MB (2396806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bd4c128777cf5eda46cb5a3ab851f4294546c4b8267f89d17b1adfc4ad5e9bd`  
		Last Modified: Wed, 11 Jun 2025 12:34:40 GMT  
		Size: 25.3 KB (25320 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.38-alpine`

```console
$ docker pull memcached@sha256:08b6a6cba188fab22215b24a3d5c1ccc18343bc337268f663f20cd86dbdfffeb
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

### `memcached:1.6.38-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:606d01f5580448504043b6ca9994e651efd5cd79822d58639d3f7cb17850fe19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5901265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be94f0135609b0bf7b7f5787294b235034eed9e87be4689825605790d50cff24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef12469432374e0b8bca5dba738c021a8d10c2fc0374275956b8104d92b4053`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b606d4a25237e4f6fe0e5c302a9e8567588be271b95f83da33a31499dac8b0`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 104.7 KB (104728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05dc60670fe6d174274d0896db26274c8ef0e2f77afc45eb51b7cdefceddab51`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 2.0 MB (1998336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa1296a9dd4dfcfb8fcefddbc83edb103f22840e4a193ee7a1e207b232e7338e`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea55364413c47b3f8818b61b2de7d3e3a28b8592bbe25c146ef8a1edf4a17363`  
		Last Modified: Tue, 03 Jun 2025 13:30:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:552c1686ee77c9b7fba7c898a29803c51578a0e80715122dccafcb355025c0de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 KB (119969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb77b32517cfa4aa8e784ef0102259db59c51c349a263d3c87b50ed983fc3ef`

```dockerfile
```

-	Layers:
	-	`sha256:ce2831bada0ca80b430da313ea1ccf45204f6ca84dec4484adbc614b9494be4f`  
		Last Modified: Tue, 03 Jun 2025 14:45:05 GMT  
		Size: 96.2 KB (96180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2114cfbb746c8f95ef4f406bb87b6458f0b23a4844fe5a9774c62c1e9255d42c`  
		Last Modified: Tue, 03 Jun 2025 14:45:05 GMT  
		Size: 23.8 KB (23789 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:41a88acc0a34fb3e7bf86b58cd20dce95d6a609303362364ed6f7f7bd3079880
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6247593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7dfc69a347c50839ad628b964963b8149866c24446202e5789804bc8067e23c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf218c5787338a7792daeaefbb181cf59684549881841831603999e10d5187e`  
		Last Modified: Tue, 03 Jun 2025 13:30:42 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661f41de55d4df851603ae02c2cdc6e73b2ab9a9ecf45eac9b82f105cb482ee1`  
		Last Modified: Tue, 03 Jun 2025 13:32:27 GMT  
		Size: 120.8 KB (120818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e622a5461288686c20e7803ad3d17a45f79a7b140e90b6bbcb6bc8f462c57010`  
		Last Modified: Tue, 03 Jun 2025 13:34:11 GMT  
		Size: 2.0 MB (1989486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd408342d331a0cceff7d0f0d80a5ec8f14ea99c95791d36a29518931ebefb8e`  
		Last Modified: Tue, 03 Jun 2025 13:30:50 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9520bec02cd5779ce2136e2d96c570b84f26641fe4e391f33fb8228c77f4aeac`  
		Last Modified: Tue, 03 Jun 2025 13:30:57 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:e3d2683766797f6a8fe83ea61b5a2979ef33a4d78ea3e0aa9047e37cd2a3fd7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 KB (120271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7447a1da56e995b60bc91c0a003ba4d9d9a6c78fc3a8f9220e19353f0eebc3fc`

```dockerfile
```

-	Layers:
	-	`sha256:ca6f6e30cd21da5e6e9e17e53ca50b541ab1099c4a87acc15081d16797f581c2`  
		Last Modified: Tue, 03 Jun 2025 14:45:05 GMT  
		Size: 96.3 KB (96284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e835bdadfb4d4407a7c5d19b63c33e1f15ec1d83efbabf27ae3e33553a599c2a`  
		Last Modified: Tue, 03 Jun 2025 14:45:05 GMT  
		Size: 24.0 KB (23987 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-alpine` - linux; 386

```console
$ docker pull memcached@sha256:39a104f3004fd4a9e820173573ffcc2b15ec2948ca68e6b3d8cfe0e3ecdd12b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5686724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34077a3f17da3a414af6d200ebb8d57c0e73bd8d1d460d1e2ed17e8cc61341c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4498fffb412d9bcc1b73bd7bfa0d2754cf5230f83c22efba4479b1854b502291`  
		Last Modified: Tue, 03 Jun 2025 14:45:06 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7c585852f370434b2f4b564d7ec7ea58c5b06e528ac6b8dffd1212dd6f521e`  
		Last Modified: Tue, 03 Jun 2025 14:45:06 GMT  
		Size: 109.5 KB (109520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc95d14dcefd82bdeb2d89e3ba0fad63fd7fc93194f678a93bc1d9217b9c2ff`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 2.0 MB (1959822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f21560067e099265312c0975371d273829c2923dee88b90d7e24537a458d696`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f53957473f72614ae6b6abc50bff4d20acd3a704edb23755b4e2a5bb6f71a7aa`  
		Last Modified: Tue, 03 Jun 2025 14:45:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:3d21a067c964615eb13e5e591df9d66ea730e3a04be65f71321ad10f1c367d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.9 KB (119867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:897704751afe9189615b739f6bf4308d242df30afe8b42aff038d7828ab081db`

```dockerfile
```

-	Layers:
	-	`sha256:6e6181041c0daeaf47a8f8475f930b1ea73d5cf55a7b5a7b3efba14627e6e8c4`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 96.1 KB (96135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:768c02304a965eacaab05dd9b82b91c453a28d3fbc77b34221ab010ccc28cbcb`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 23.7 KB (23732 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:0bf6f7efe5d3e4b11cec8d17f924ae42d7622e1b0bbcdb56d4757bb3d22ab4b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5947182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf2f7366cf8143a64896b9b751eadad7798b3eec347162fca324567acec20082`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6dc89a1ff7a965251a27c2d9dcb719f464507b964ba3286d6a6034d9f89769`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d75cf13bd9119987f7710d75fd446cd9d065487b3e83297be8c9c4b3120e7e`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 124.3 KB (124312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9461b52977c4cd8b006ffee034043d389554e4c3b267b0901829e7a7a353b8`  
		Last Modified: Tue, 03 Jun 2025 14:45:08 GMT  
		Size: 2.1 MB (2091330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c2dc09d491c7a103b9bd75fa5267b316526d77163130840938eadadb72e6b1`  
		Last Modified: Tue, 03 Jun 2025 14:45:08 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bece68e2cfcb576a9778e7da37d6e2a58ac091bd908caf52a90c4baf09d4d079`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:efd926e1e98c4bedf0db6b24ec177d116548e0652d6b66db54cb2a3e81d21899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 KB (118151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57233506303dd47952c792831142da6a3fe9c4e6c5ea7678ff91b329c08e589`

```dockerfile
```

-	Layers:
	-	`sha256:ed1b26ef88ce71431cfd88a99e6d2d4d13494e7bf5056e489b0b1eb2133d81ab`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 94.3 KB (94287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eaf4c09f8a1fb9991161e85051ae93568c08ab9b2a1142b1bbf99a182e7c0f0`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 23.9 KB (23864 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:aed10964c6cc121d6201aaa8301e269cb88396f19e514ab4529073da9d0c2218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f0390597339801ec08bfd34d10d8bf91dc8e03f2e864f9643758e7ade704d40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db926e6f83170fbe6f646943cb34741a092b9ce5226a6d1bd6b9214d4515055f`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1884ffba96f71fb43c1fef7f0405221b4c8070f55b8667e8b75cc04d268f5cbc`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 107.9 KB (107905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9dea200205fca0caa1f83f40ea69123226bf113407054775efd4a508ae03c65`  
		Last Modified: Tue, 03 Jun 2025 14:45:10 GMT  
		Size: 1.9 MB (1932426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0f27bac94157c911304329980a3ac043834b3407e7ebf8f6a152d114f5949c`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec883045be124559e6a84f03b352a143404848596a99aacded6fe91e3150c5eb`  
		Last Modified: Tue, 03 Jun 2025 14:45:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:aa82a1a35cac8440e684fe5059460736ac54ad11d07080afd5fe8fc546806556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.1 KB (118146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc357c735ee41efba1c1c97057f37ee17ce47e28b9887307cbd229d6895da03`

```dockerfile
```

-	Layers:
	-	`sha256:194792c5d362608149275ef412c050bbec126c27232fd4210029e547cac00ae7`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddb88c4acf94b34eadf22eea85377681f766029d1748d93ace4a6a7e7b23538a`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 23.9 KB (23863 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:656e879b0120ed1dc41f4eea945ffd837cbd61df8792d9622df23bb94621dcba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5800523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6248ca4cb8546aea87cb93f6af7f23e99e572b78a8454a9af00758038970fb5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb224b0e357fdb3b8b28a5e9a31cd54bf59197e6b87eff81737fee0cbf2326d1`  
		Last Modified: Tue, 03 Jun 2025 14:45:11 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ffb790e1ad6ec57e858ea0d68a71a20c8d4f1e44cb7d1089e651677c61ff004`  
		Last Modified: Tue, 03 Jun 2025 14:45:11 GMT  
		Size: 113.5 KB (113497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ed9fcfc8c703bdee212b6c00a17c6ea94d9ae8e768825af3a9999a2cc0aa5f`  
		Last Modified: Tue, 03 Jun 2025 14:45:11 GMT  
		Size: 2.0 MB (2038146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d331df3ee94402980d3422bee4dcbd4613703a284b9ccc1fe1f6fdec3f4d869`  
		Last Modified: Tue, 03 Jun 2025 14:45:11 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93af5977e9aba9bde51aba44398ec5690948753fa15a6c35e41208a543d6c2e`  
		Last Modified: Tue, 03 Jun 2025 14:45:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:3dd443c4d6c4cbce2a2b09a2b2869282e7d1478a57e9967b3b38705268315e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.0 KB (118019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538a73a14cc21737f67c2f643b673960e4d7c106988e28fa3bb45734ed83532d`

```dockerfile
```

-	Layers:
	-	`sha256:726d5699c7a6f8c2cc2e05311aefbfc8a4a5369d49388faaf922cdf278a20b7c`  
		Last Modified: Tue, 03 Jun 2025 14:45:12 GMT  
		Size: 94.2 KB (94229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:382c68890507f3d9fe2510636665755df015b0354866ac714c3e70a3201ca87e`  
		Last Modified: Tue, 03 Jun 2025 14:45:11 GMT  
		Size: 23.8 KB (23790 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.38-alpine3.22`

```console
$ docker pull memcached@sha256:08b6a6cba188fab22215b24a3d5c1ccc18343bc337268f663f20cd86dbdfffeb
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

### `memcached:1.6.38-alpine3.22` - linux; amd64

```console
$ docker pull memcached@sha256:606d01f5580448504043b6ca9994e651efd5cd79822d58639d3f7cb17850fe19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5901265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be94f0135609b0bf7b7f5787294b235034eed9e87be4689825605790d50cff24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef12469432374e0b8bca5dba738c021a8d10c2fc0374275956b8104d92b4053`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b606d4a25237e4f6fe0e5c302a9e8567588be271b95f83da33a31499dac8b0`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 104.7 KB (104728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05dc60670fe6d174274d0896db26274c8ef0e2f77afc45eb51b7cdefceddab51`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 2.0 MB (1998336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa1296a9dd4dfcfb8fcefddbc83edb103f22840e4a193ee7a1e207b232e7338e`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea55364413c47b3f8818b61b2de7d3e3a28b8592bbe25c146ef8a1edf4a17363`  
		Last Modified: Tue, 03 Jun 2025 13:30:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:552c1686ee77c9b7fba7c898a29803c51578a0e80715122dccafcb355025c0de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 KB (119969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb77b32517cfa4aa8e784ef0102259db59c51c349a263d3c87b50ed983fc3ef`

```dockerfile
```

-	Layers:
	-	`sha256:ce2831bada0ca80b430da313ea1ccf45204f6ca84dec4484adbc614b9494be4f`  
		Last Modified: Tue, 03 Jun 2025 14:45:05 GMT  
		Size: 96.2 KB (96180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2114cfbb746c8f95ef4f406bb87b6458f0b23a4844fe5a9774c62c1e9255d42c`  
		Last Modified: Tue, 03 Jun 2025 14:45:05 GMT  
		Size: 23.8 KB (23789 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:41a88acc0a34fb3e7bf86b58cd20dce95d6a609303362364ed6f7f7bd3079880
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6247593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7dfc69a347c50839ad628b964963b8149866c24446202e5789804bc8067e23c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf218c5787338a7792daeaefbb181cf59684549881841831603999e10d5187e`  
		Last Modified: Tue, 03 Jun 2025 13:30:42 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661f41de55d4df851603ae02c2cdc6e73b2ab9a9ecf45eac9b82f105cb482ee1`  
		Last Modified: Tue, 03 Jun 2025 13:32:27 GMT  
		Size: 120.8 KB (120818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e622a5461288686c20e7803ad3d17a45f79a7b140e90b6bbcb6bc8f462c57010`  
		Last Modified: Tue, 03 Jun 2025 13:34:11 GMT  
		Size: 2.0 MB (1989486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd408342d331a0cceff7d0f0d80a5ec8f14ea99c95791d36a29518931ebefb8e`  
		Last Modified: Tue, 03 Jun 2025 13:30:50 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9520bec02cd5779ce2136e2d96c570b84f26641fe4e391f33fb8228c77f4aeac`  
		Last Modified: Tue, 03 Jun 2025 13:30:57 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:e3d2683766797f6a8fe83ea61b5a2979ef33a4d78ea3e0aa9047e37cd2a3fd7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 KB (120271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7447a1da56e995b60bc91c0a003ba4d9d9a6c78fc3a8f9220e19353f0eebc3fc`

```dockerfile
```

-	Layers:
	-	`sha256:ca6f6e30cd21da5e6e9e17e53ca50b541ab1099c4a87acc15081d16797f581c2`  
		Last Modified: Tue, 03 Jun 2025 14:45:05 GMT  
		Size: 96.3 KB (96284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e835bdadfb4d4407a7c5d19b63c33e1f15ec1d83efbabf27ae3e33553a599c2a`  
		Last Modified: Tue, 03 Jun 2025 14:45:05 GMT  
		Size: 24.0 KB (23987 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-alpine3.22` - linux; 386

```console
$ docker pull memcached@sha256:39a104f3004fd4a9e820173573ffcc2b15ec2948ca68e6b3d8cfe0e3ecdd12b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5686724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34077a3f17da3a414af6d200ebb8d57c0e73bd8d1d460d1e2ed17e8cc61341c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4498fffb412d9bcc1b73bd7bfa0d2754cf5230f83c22efba4479b1854b502291`  
		Last Modified: Tue, 03 Jun 2025 14:45:06 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7c585852f370434b2f4b564d7ec7ea58c5b06e528ac6b8dffd1212dd6f521e`  
		Last Modified: Tue, 03 Jun 2025 14:45:06 GMT  
		Size: 109.5 KB (109520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc95d14dcefd82bdeb2d89e3ba0fad63fd7fc93194f678a93bc1d9217b9c2ff`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 2.0 MB (1959822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f21560067e099265312c0975371d273829c2923dee88b90d7e24537a458d696`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f53957473f72614ae6b6abc50bff4d20acd3a704edb23755b4e2a5bb6f71a7aa`  
		Last Modified: Tue, 03 Jun 2025 14:45:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:3d21a067c964615eb13e5e591df9d66ea730e3a04be65f71321ad10f1c367d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.9 KB (119867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:897704751afe9189615b739f6bf4308d242df30afe8b42aff038d7828ab081db`

```dockerfile
```

-	Layers:
	-	`sha256:6e6181041c0daeaf47a8f8475f930b1ea73d5cf55a7b5a7b3efba14627e6e8c4`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 96.1 KB (96135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:768c02304a965eacaab05dd9b82b91c453a28d3fbc77b34221ab010ccc28cbcb`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 23.7 KB (23732 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-alpine3.22` - linux; ppc64le

```console
$ docker pull memcached@sha256:0bf6f7efe5d3e4b11cec8d17f924ae42d7622e1b0bbcdb56d4757bb3d22ab4b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5947182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf2f7366cf8143a64896b9b751eadad7798b3eec347162fca324567acec20082`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6dc89a1ff7a965251a27c2d9dcb719f464507b964ba3286d6a6034d9f89769`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d75cf13bd9119987f7710d75fd446cd9d065487b3e83297be8c9c4b3120e7e`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 124.3 KB (124312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9461b52977c4cd8b006ffee034043d389554e4c3b267b0901829e7a7a353b8`  
		Last Modified: Tue, 03 Jun 2025 14:45:08 GMT  
		Size: 2.1 MB (2091330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c2dc09d491c7a103b9bd75fa5267b316526d77163130840938eadadb72e6b1`  
		Last Modified: Tue, 03 Jun 2025 14:45:08 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bece68e2cfcb576a9778e7da37d6e2a58ac091bd908caf52a90c4baf09d4d079`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:efd926e1e98c4bedf0db6b24ec177d116548e0652d6b66db54cb2a3e81d21899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 KB (118151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57233506303dd47952c792831142da6a3fe9c4e6c5ea7678ff91b329c08e589`

```dockerfile
```

-	Layers:
	-	`sha256:ed1b26ef88ce71431cfd88a99e6d2d4d13494e7bf5056e489b0b1eb2133d81ab`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 94.3 KB (94287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eaf4c09f8a1fb9991161e85051ae93568c08ab9b2a1142b1bbf99a182e7c0f0`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 23.9 KB (23864 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-alpine3.22` - linux; riscv64

```console
$ docker pull memcached@sha256:aed10964c6cc121d6201aaa8301e269cb88396f19e514ab4529073da9d0c2218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f0390597339801ec08bfd34d10d8bf91dc8e03f2e864f9643758e7ade704d40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db926e6f83170fbe6f646943cb34741a092b9ce5226a6d1bd6b9214d4515055f`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1884ffba96f71fb43c1fef7f0405221b4c8070f55b8667e8b75cc04d268f5cbc`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 107.9 KB (107905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9dea200205fca0caa1f83f40ea69123226bf113407054775efd4a508ae03c65`  
		Last Modified: Tue, 03 Jun 2025 14:45:10 GMT  
		Size: 1.9 MB (1932426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0f27bac94157c911304329980a3ac043834b3407e7ebf8f6a152d114f5949c`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec883045be124559e6a84f03b352a143404848596a99aacded6fe91e3150c5eb`  
		Last Modified: Tue, 03 Jun 2025 14:45:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:aa82a1a35cac8440e684fe5059460736ac54ad11d07080afd5fe8fc546806556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.1 KB (118146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc357c735ee41efba1c1c97057f37ee17ce47e28b9887307cbd229d6895da03`

```dockerfile
```

-	Layers:
	-	`sha256:194792c5d362608149275ef412c050bbec126c27232fd4210029e547cac00ae7`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddb88c4acf94b34eadf22eea85377681f766029d1748d93ace4a6a7e7b23538a`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 23.9 KB (23863 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-alpine3.22` - linux; s390x

```console
$ docker pull memcached@sha256:656e879b0120ed1dc41f4eea945ffd837cbd61df8792d9622df23bb94621dcba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5800523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6248ca4cb8546aea87cb93f6af7f23e99e572b78a8454a9af00758038970fb5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb224b0e357fdb3b8b28a5e9a31cd54bf59197e6b87eff81737fee0cbf2326d1`  
		Last Modified: Tue, 03 Jun 2025 14:45:11 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ffb790e1ad6ec57e858ea0d68a71a20c8d4f1e44cb7d1089e651677c61ff004`  
		Last Modified: Tue, 03 Jun 2025 14:45:11 GMT  
		Size: 113.5 KB (113497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ed9fcfc8c703bdee212b6c00a17c6ea94d9ae8e768825af3a9999a2cc0aa5f`  
		Last Modified: Tue, 03 Jun 2025 14:45:11 GMT  
		Size: 2.0 MB (2038146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d331df3ee94402980d3422bee4dcbd4613703a284b9ccc1fe1f6fdec3f4d869`  
		Last Modified: Tue, 03 Jun 2025 14:45:11 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93af5977e9aba9bde51aba44398ec5690948753fa15a6c35e41208a543d6c2e`  
		Last Modified: Tue, 03 Jun 2025 14:45:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:3dd443c4d6c4cbce2a2b09a2b2869282e7d1478a57e9967b3b38705268315e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.0 KB (118019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538a73a14cc21737f67c2f643b673960e4d7c106988e28fa3bb45734ed83532d`

```dockerfile
```

-	Layers:
	-	`sha256:726d5699c7a6f8c2cc2e05311aefbfc8a4a5369d49388faaf922cdf278a20b7c`  
		Last Modified: Tue, 03 Jun 2025 14:45:12 GMT  
		Size: 94.2 KB (94229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:382c68890507f3d9fe2510636665755df015b0354866ac714c3e70a3201ca87e`  
		Last Modified: Tue, 03 Jun 2025 14:45:11 GMT  
		Size: 23.8 KB (23790 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.38-bookworm`

```console
$ docker pull memcached@sha256:89b2dfa7e55e5fd1986e22210cdf89f0a5e5d6c913101e2bcfdfb4d1d73de7ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:1.6.38-bookworm` - linux; amd64

```console
$ docker pull memcached@sha256:c2b5b37862a0d15d6622bea58a1e3a7a34610456324dc81a6de4e3369d06a5f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33026651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:809ba6b39db15dffb27e2affc4fc5bc5eee2c32ee9b06e08f2f604ee63e41a78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35255ebbfb2408b64a9d53c3d868456872a9b4d89ff4e80f2a8d20c4332dd69`  
		Last Modified: Tue, 10 Jun 2025 23:32:18 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be9410e6aeed64e084cb2812f5d70658e1a9ffe79b5972cea39097c9b949e4e`  
		Last Modified: Tue, 10 Jun 2025 23:32:19 GMT  
		Size: 2.5 MB (2492199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d86227fbbb72b09a47e8016b198dc2062598d3e4c4b358cfa655a2a2c044ef`  
		Last Modified: Tue, 10 Jun 2025 23:32:20 GMT  
		Size: 2.3 MB (2302808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad105488469355bcd85bf5c9c6b74cf9729838da44ad0c6f500f252c6860e8c`  
		Last Modified: Tue, 10 Jun 2025 23:32:20 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90864ece76220d4e897cf79c19145c02ce9d1c1326bb831401963b27ec0ca566`  
		Last Modified: Tue, 10 Jun 2025 23:32:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:5b481897e28479249d51b4c0720b45485fe1952dcb27924f267fcd30d68de833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2425304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6773503e415cd198fe6533c8042593b7aabb0d583e0baf500eed5c4c78452531`

```dockerfile
```

-	Layers:
	-	`sha256:4c6461ec41fb74fe203eb1b6c30c50eddc7f6c11871bfa03eab07db6a4b17c6f`  
		Last Modified: Wed, 11 Jun 2025 00:34:27 GMT  
		Size: 2.4 MB (2399984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e35a57a543fde6b5a8a3e185100a7e9b5ac2a947dea0b7589b5531fab06c67c`  
		Last Modified: Wed, 11 Jun 2025 00:34:28 GMT  
		Size: 25.3 KB (25320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:ca1e51720502c0722aae38efd0a64db105570638d65d6a70ab4572658aff584a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.1 MB (30093253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86fc08738ceff7b24bd461ffd9a41799a048727c6673c1a3c4cb5a01f6b82608`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:750907abe8bb5d66304ed40261e1579b6575871f6848cfbd720888c20afd3b67`  
		Last Modified: Tue, 10 Jun 2025 22:47:31 GMT  
		Size: 25.8 MB (25762396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9660206a4f42b745fdc386aced2845f4fa99b6de361892e4df07c2daf0f24c`  
		Last Modified: Wed, 11 Jun 2025 00:04:16 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877a28dd495fb8632729edaf5b9318ec22ce2a5e402b746782fb7084fd01032c`  
		Last Modified: Wed, 11 Jun 2025 00:04:19 GMT  
		Size: 2.1 MB (2097026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06cb49b999b102d1dc8725fedf17028635be0bcc810a049a03c6e96128a9e4e6`  
		Last Modified: Wed, 11 Jun 2025 00:04:30 GMT  
		Size: 2.2 MB (2232317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee68dfb7714895c5d09887e2708b1296a8855e4ac7ff3d0a158bf029e81e157`  
		Last Modified: Wed, 11 Jun 2025 00:04:39 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff86e8516fa08ad0aa15dfb3afebb40da609006594dcf941ed7900b39cec11aa`  
		Last Modified: Wed, 11 Jun 2025 00:04:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:68162c3dae075d4cb8b6a636c634479c8402119be9f3b6f995913ba4d47162e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2429297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10be7e4ce251f42cb456f15eae67ae97fc6e3040fc50fe0990c4503b35a8829b`

```dockerfile
```

-	Layers:
	-	`sha256:5874edec5896e806374ff905b6f10f3724d44a31a61bf0d830a5ecac4cfbb548`  
		Last Modified: Wed, 11 Jun 2025 03:34:34 GMT  
		Size: 2.4 MB (2403830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54b0ebcaf098420587b0d84ab425ad9abdfc444c86c6ba478b50be7b335cd3c6`  
		Last Modified: Wed, 11 Jun 2025 03:34:34 GMT  
		Size: 25.5 KB (25467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-bookworm` - linux; arm variant v7

```console
$ docker pull memcached@sha256:d208683140025f905b085b97b35b3a533015b73809d3740e5e3d968c202ec9e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28070929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b74912d1ce300e7a774e690f1c07510c2228991f23ee542e33cc1028e45d90bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6615a784a0e15fd2ed6d79980e68d9cfe87df589b9af6f4c71656286b040acc`  
		Last Modified: Tue, 10 Jun 2025 23:43:55 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66fc152354c58f6024d7e37104e92e718be7b1e70f9745e96e63006f79730f5`  
		Last Modified: Tue, 10 Jun 2025 23:43:56 GMT  
		Size: 1.9 MB (1946292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3712992b59c9c2fa191ca82275b5fb441fcc21940ef625721d0221723f70d9e`  
		Last Modified: Tue, 10 Jun 2025 23:43:56 GMT  
		Size: 2.2 MB (2184378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ba9e36b6e72e151a91cc69343438b9341451e4196d29b259766ab25ece2755`  
		Last Modified: Tue, 10 Jun 2025 23:43:56 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f566ffc3a278d8a018e52b43be1df458ee6632e59b56f75a94a0d058a6cfe73`  
		Last Modified: Tue, 10 Jun 2025 23:43:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:2bbfd653e524ef9316e75f9681ac6876a3e40a63ac124b1e00216760e2855ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2427734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e73cc4fc38d626337d836752990c011dfc545348cb8fd74aa3ae7a39e08c5bc`

```dockerfile
```

-	Layers:
	-	`sha256:8eec2d1ef62751b78959b1e676c070de5b6da4490f0797715b6038816e6ecbe7`  
		Last Modified: Wed, 11 Jun 2025 00:34:36 GMT  
		Size: 2.4 MB (2402267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7bd74b81adae550be8823fda7677f05554265436005a14b9a3f3775ec776a45`  
		Last Modified: Wed, 11 Jun 2025 00:34:37 GMT  
		Size: 25.5 KB (25467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:8a7286d77ae74f81f50dffd6f6e763edd304ed10f5a56e2fe3bdbc38578586a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32723815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05a57428c8257697aa07726f04832bba5278021c4028ea564ada3e7c63bf181`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c5447936c48fe52b15de86391eaf4d170445111319a12dd6f05a85d115b1a4`  
		Last Modified: Wed, 11 Jun 2025 00:32:55 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfca24a3c9155df906544ba98f8bb2bc9f66d9704ed8edf0e731bfe4672420d2`  
		Last Modified: Wed, 11 Jun 2025 00:32:58 GMT  
		Size: 2.4 MB (2355841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eab66920dbc0773d0617dced9ec788e2dc243fc3c3abb0855646922df94744d`  
		Last Modified: Wed, 11 Jun 2025 00:33:04 GMT  
		Size: 2.3 MB (2288782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99014141349bea93d0cf26fd4326ec422f06a635c0ba43644c022fc9960456b8`  
		Last Modified: Wed, 11 Jun 2025 00:33:09 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c855df1fbe1070effdf016a21c2055af95b6325b3e22aa0f32e24d1896dd7a1a`  
		Last Modified: Wed, 11 Jun 2025 00:33:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:45dd4c7b93d5dc7ac1a41023089465fc7feeb3a6878b831308593b595c4453ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2425816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d377887b57b57637deedd7fc6db230aceaeb6f127b9d419649daf5eb921dcfe3`

```dockerfile
```

-	Layers:
	-	`sha256:104fd15db5961a346a71d8c3471d234720c45848fed57ef5c979b5904c13679d`  
		Last Modified: Wed, 11 Jun 2025 03:34:41 GMT  
		Size: 2.4 MB (2400299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b12674469f62c07ff246f7a86cd72871b797a081f0f1a29ebf34768864970340`  
		Last Modified: Wed, 11 Jun 2025 03:34:42 GMT  
		Size: 25.5 KB (25517 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:2fd3408e4989cc9e56a6d3add7ce53181decaf9d7cc19e14b49670b45944e40e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33967948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a326ebe4a452ab75793d01324bf45cdf00e7f2aa83d4793e9993f6317370b81`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c3d46fed134488b3ee18c12cb308c8d5520b8c647122c392f9fb76e3e1e2fc61`  
		Last Modified: Tue, 10 Jun 2025 22:47:25 GMT  
		Size: 29.2 MB (29212433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6e1ece79d563054c9ed24818e5adb5d97e5a1bd3a898d27b10ad0ed0d944fe`  
		Last Modified: Tue, 10 Jun 2025 23:32:02 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d82ab526e835ea99bac51cedfd44fda08d1096806527e0e4776d1747931bfb`  
		Last Modified: Tue, 10 Jun 2025 23:32:03 GMT  
		Size: 2.5 MB (2502688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c26ac869e988fa955c3c084363eb741d506a2034cdd3e12a5c98ff74e4c65c5`  
		Last Modified: Tue, 10 Jun 2025 23:32:03 GMT  
		Size: 2.3 MB (2251313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87ab77943d07e12971b970348f051de5367dd6a2bb147741b63f12eca74d55f`  
		Last Modified: Tue, 10 Jun 2025 23:32:03 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5505b2cac6d2a77393345699695a05426271e871ba824bf0e22789a5cdf44f8e`  
		Last Modified: Tue, 10 Jun 2025 23:32:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f5178b4eff39883c5450012b44b95dc2e13a26e5c3efe2221f9a929a01b99a6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2422389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db0fa4b9612a2b4b5f20852ca646c7fa318ae7057ec68f20599d1281453c0ac5`

```dockerfile
```

-	Layers:
	-	`sha256:27ef430fcb7445f00c5cbbac9416a8082301986670c56b7112c8ee8d2bc7ea63`  
		Last Modified: Wed, 11 Jun 2025 00:34:45 GMT  
		Size: 2.4 MB (2397127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c71e82389c2ff610732d9cc27ec31e1061a1fe683a7594c559d2f0ad1b307bf`  
		Last Modified: Wed, 11 Jun 2025 00:34:46 GMT  
		Size: 25.3 KB (25262 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:4dcc31fdaa97e6430560dfb497e4dde22b2ef368e6c66a3b271a5343bfd86e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32779330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6bba452dff6149dc16dfc6eda06981c4240993be55b9b6f998d30e26935e676`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ac3f61581c7f5755d8598b3a0857c417db0251b17c0e4e4f43a5fc0e24023524`  
		Last Modified: Tue, 10 Jun 2025 22:48:26 GMT  
		Size: 28.5 MB (28516717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b713f027201c7d06c5013a8693a2fb17e64d3d8113328cd83f01c565ddd25a31`  
		Last Modified: Wed, 11 Jun 2025 00:38:45 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699452fffd3fdc6e04d5c6c072d85da568d4477714b34612b15505bebad40576`  
		Last Modified: Wed, 11 Jun 2025 00:38:49 GMT  
		Size: 1.9 MB (1944083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4909573bcae2300d9ad92749c2279eaab07c75210c195cc36bcc323a289711c`  
		Last Modified: Wed, 11 Jun 2025 00:38:54 GMT  
		Size: 2.3 MB (2317017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42800230fbc3a3fdd8ebd615178ea6d750f32c99d916c8d4c1fce650c9724740`  
		Last Modified: Wed, 11 Jun 2025 00:39:03 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc602c2ec2581679f4ba36524612bf709f9828eae2e8e2382a5b72cfe43ddde`  
		Last Modified: Wed, 11 Jun 2025 00:39:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:c8b58a5685ab59a7e412a46fadca1a86a8065cb821c20aa84496f3da2932a6bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d142d271ffff6f14e07b46862b9d5c35a3f62a5ae21f22698dbf2729e22393e5`

```dockerfile
```

-	Layers:
	-	`sha256:0c2d883e7eeaa126767df6696d4d4d21074e1b88388aca7a8d9936e34d972390`  
		Last Modified: Wed, 11 Jun 2025 03:34:48 GMT  
		Size: 25.2 KB (25216 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:ec8926cb7edeb9e447cfa09a6496daf6ddf6214c670db96c915bfbfcdd867a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37203472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f834c7368564e22deca1fec762744af6a328960d29a0757f965efb0922ef2ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c9cd5d5c131a8141631d87d9507a82e0549a2144689442301c07d2da80f39d19`  
		Last Modified: Tue, 10 Jun 2025 23:58:45 GMT  
		Size: 32.1 MB (32072795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783cc02b7ca742bdfa931c46ca74a297d6743f7632079af1d38a86f0ef33e67e`  
		Last Modified: Tue, 10 Jun 2025 23:50:23 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dcb0a6965f82b33b339604c7bfc7e13fddac325187039be9416554f6deaa468`  
		Last Modified: Tue, 10 Jun 2025 23:50:24 GMT  
		Size: 2.7 MB (2710185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460f1a7eb5adf7c13e3a2c6e82959f31bd877cd781b02a5997ba29d421ea0845`  
		Last Modified: Tue, 10 Jun 2025 23:50:24 GMT  
		Size: 2.4 MB (2418981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5dbb0f6f2b188832219b7b4c16a43d53399710d576b050d6939a213e05dd83`  
		Last Modified: Tue, 10 Jun 2025 23:50:24 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ce0fe2674fef821731c0bf8d4218891392e919b579863b73b27c02281d67bb`  
		Last Modified: Tue, 10 Jun 2025 23:50:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:295a95b2a5fbcaba4f0430c8b8fc00ec4ebe4a3ab75480f5ed7890dd086efdc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2429850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd03034a2e56497ce0625f4e0bfba90e28c4d23be1250fe5547dfab3f61abd66`

```dockerfile
```

-	Layers:
	-	`sha256:5e551af8256cd1f6d5d31b7a99d5338c2e0f7c59dd109277d12a1d01c1f8e4dc`  
		Last Modified: Wed, 11 Jun 2025 03:34:53 GMT  
		Size: 2.4 MB (2404456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eac12139332bd876a1e77dd40aa823e07245885fb8a0d33164fd342e6a3198b9`  
		Last Modified: Wed, 11 Jun 2025 03:34:54 GMT  
		Size: 25.4 KB (25394 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:04933adc68fd0a9324a7d5796e1d3cde2a0012644f2ea93c60f0b9ef4f676e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31309863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d59a9f1fa8b8ed5157a51f715aac503833e36e3aa6da498fd68e1647c8366e7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d890a6beb4a310ea4195e7ebd130e37a17b64820c995a543bb5619b2eab1e6`  
		Last Modified: Wed, 11 Jun 2025 09:15:09 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119a4250ae0069dea78d2943d561ab4ad7db7018ddd34dcdf8ceecada8494508`  
		Last Modified: Wed, 11 Jun 2025 09:15:10 GMT  
		Size: 2.2 MB (2156963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eea4eabc325c68a766c64d84b958281150eee02f4ada0091377c9af7b07a793`  
		Last Modified: Wed, 11 Jun 2025 09:15:10 GMT  
		Size: 2.3 MB (2263533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ddbca61153701e80e50122cb3d22cd45a49b4bf191114e8b132b588b077673`  
		Last Modified: Wed, 11 Jun 2025 09:15:10 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42132a3abe6b3ca5bc8e4e623ffa00fe86641a0a42454bba499fa70136dea21`  
		Last Modified: Wed, 11 Jun 2025 09:15:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:2f715ae3a26ddc650f595ca31d33c4a4c14311b1347a6e8d20aca949b131063d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2422126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a4df8b3c359f6d964f37642182e6de7a4cd8cc28676c409e313aa88eaf5b698`

```dockerfile
```

-	Layers:
	-	`sha256:994b93c94dedc6bf0bf79fcfb6b5332c77a3fea69cd945274a1b5eead27d80e0`  
		Last Modified: Wed, 11 Jun 2025 12:34:39 GMT  
		Size: 2.4 MB (2396806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bd4c128777cf5eda46cb5a3ab851f4294546c4b8267f89d17b1adfc4ad5e9bd`  
		Last Modified: Wed, 11 Jun 2025 12:34:40 GMT  
		Size: 25.3 KB (25320 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine`

```console
$ docker pull memcached@sha256:08b6a6cba188fab22215b24a3d5c1ccc18343bc337268f663f20cd86dbdfffeb
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
$ docker pull memcached@sha256:606d01f5580448504043b6ca9994e651efd5cd79822d58639d3f7cb17850fe19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5901265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be94f0135609b0bf7b7f5787294b235034eed9e87be4689825605790d50cff24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef12469432374e0b8bca5dba738c021a8d10c2fc0374275956b8104d92b4053`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b606d4a25237e4f6fe0e5c302a9e8567588be271b95f83da33a31499dac8b0`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 104.7 KB (104728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05dc60670fe6d174274d0896db26274c8ef0e2f77afc45eb51b7cdefceddab51`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 2.0 MB (1998336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa1296a9dd4dfcfb8fcefddbc83edb103f22840e4a193ee7a1e207b232e7338e`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea55364413c47b3f8818b61b2de7d3e3a28b8592bbe25c146ef8a1edf4a17363`  
		Last Modified: Tue, 03 Jun 2025 13:30:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:552c1686ee77c9b7fba7c898a29803c51578a0e80715122dccafcb355025c0de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 KB (119969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb77b32517cfa4aa8e784ef0102259db59c51c349a263d3c87b50ed983fc3ef`

```dockerfile
```

-	Layers:
	-	`sha256:ce2831bada0ca80b430da313ea1ccf45204f6ca84dec4484adbc614b9494be4f`  
		Last Modified: Tue, 03 Jun 2025 14:45:05 GMT  
		Size: 96.2 KB (96180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2114cfbb746c8f95ef4f406bb87b6458f0b23a4844fe5a9774c62c1e9255d42c`  
		Last Modified: Tue, 03 Jun 2025 14:45:05 GMT  
		Size: 23.8 KB (23789 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:41a88acc0a34fb3e7bf86b58cd20dce95d6a609303362364ed6f7f7bd3079880
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6247593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7dfc69a347c50839ad628b964963b8149866c24446202e5789804bc8067e23c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf218c5787338a7792daeaefbb181cf59684549881841831603999e10d5187e`  
		Last Modified: Tue, 03 Jun 2025 13:30:42 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661f41de55d4df851603ae02c2cdc6e73b2ab9a9ecf45eac9b82f105cb482ee1`  
		Last Modified: Tue, 03 Jun 2025 13:32:27 GMT  
		Size: 120.8 KB (120818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e622a5461288686c20e7803ad3d17a45f79a7b140e90b6bbcb6bc8f462c57010`  
		Last Modified: Tue, 03 Jun 2025 13:34:11 GMT  
		Size: 2.0 MB (1989486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd408342d331a0cceff7d0f0d80a5ec8f14ea99c95791d36a29518931ebefb8e`  
		Last Modified: Tue, 03 Jun 2025 13:30:50 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9520bec02cd5779ce2136e2d96c570b84f26641fe4e391f33fb8228c77f4aeac`  
		Last Modified: Tue, 03 Jun 2025 13:30:57 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:e3d2683766797f6a8fe83ea61b5a2979ef33a4d78ea3e0aa9047e37cd2a3fd7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 KB (120271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7447a1da56e995b60bc91c0a003ba4d9d9a6c78fc3a8f9220e19353f0eebc3fc`

```dockerfile
```

-	Layers:
	-	`sha256:ca6f6e30cd21da5e6e9e17e53ca50b541ab1099c4a87acc15081d16797f581c2`  
		Last Modified: Tue, 03 Jun 2025 14:45:05 GMT  
		Size: 96.3 KB (96284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e835bdadfb4d4407a7c5d19b63c33e1f15ec1d83efbabf27ae3e33553a599c2a`  
		Last Modified: Tue, 03 Jun 2025 14:45:05 GMT  
		Size: 24.0 KB (23987 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:39a104f3004fd4a9e820173573ffcc2b15ec2948ca68e6b3d8cfe0e3ecdd12b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5686724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34077a3f17da3a414af6d200ebb8d57c0e73bd8d1d460d1e2ed17e8cc61341c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4498fffb412d9bcc1b73bd7bfa0d2754cf5230f83c22efba4479b1854b502291`  
		Last Modified: Tue, 03 Jun 2025 14:45:06 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7c585852f370434b2f4b564d7ec7ea58c5b06e528ac6b8dffd1212dd6f521e`  
		Last Modified: Tue, 03 Jun 2025 14:45:06 GMT  
		Size: 109.5 KB (109520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc95d14dcefd82bdeb2d89e3ba0fad63fd7fc93194f678a93bc1d9217b9c2ff`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 2.0 MB (1959822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f21560067e099265312c0975371d273829c2923dee88b90d7e24537a458d696`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f53957473f72614ae6b6abc50bff4d20acd3a704edb23755b4e2a5bb6f71a7aa`  
		Last Modified: Tue, 03 Jun 2025 14:45:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:3d21a067c964615eb13e5e591df9d66ea730e3a04be65f71321ad10f1c367d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.9 KB (119867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:897704751afe9189615b739f6bf4308d242df30afe8b42aff038d7828ab081db`

```dockerfile
```

-	Layers:
	-	`sha256:6e6181041c0daeaf47a8f8475f930b1ea73d5cf55a7b5a7b3efba14627e6e8c4`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 96.1 KB (96135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:768c02304a965eacaab05dd9b82b91c453a28d3fbc77b34221ab010ccc28cbcb`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 23.7 KB (23732 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:0bf6f7efe5d3e4b11cec8d17f924ae42d7622e1b0bbcdb56d4757bb3d22ab4b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5947182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf2f7366cf8143a64896b9b751eadad7798b3eec347162fca324567acec20082`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6dc89a1ff7a965251a27c2d9dcb719f464507b964ba3286d6a6034d9f89769`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d75cf13bd9119987f7710d75fd446cd9d065487b3e83297be8c9c4b3120e7e`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 124.3 KB (124312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9461b52977c4cd8b006ffee034043d389554e4c3b267b0901829e7a7a353b8`  
		Last Modified: Tue, 03 Jun 2025 14:45:08 GMT  
		Size: 2.1 MB (2091330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c2dc09d491c7a103b9bd75fa5267b316526d77163130840938eadadb72e6b1`  
		Last Modified: Tue, 03 Jun 2025 14:45:08 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bece68e2cfcb576a9778e7da37d6e2a58ac091bd908caf52a90c4baf09d4d079`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:efd926e1e98c4bedf0db6b24ec177d116548e0652d6b66db54cb2a3e81d21899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 KB (118151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57233506303dd47952c792831142da6a3fe9c4e6c5ea7678ff91b329c08e589`

```dockerfile
```

-	Layers:
	-	`sha256:ed1b26ef88ce71431cfd88a99e6d2d4d13494e7bf5056e489b0b1eb2133d81ab`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 94.3 KB (94287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eaf4c09f8a1fb9991161e85051ae93568c08ab9b2a1142b1bbf99a182e7c0f0`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 23.9 KB (23864 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:aed10964c6cc121d6201aaa8301e269cb88396f19e514ab4529073da9d0c2218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f0390597339801ec08bfd34d10d8bf91dc8e03f2e864f9643758e7ade704d40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db926e6f83170fbe6f646943cb34741a092b9ce5226a6d1bd6b9214d4515055f`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1884ffba96f71fb43c1fef7f0405221b4c8070f55b8667e8b75cc04d268f5cbc`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 107.9 KB (107905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9dea200205fca0caa1f83f40ea69123226bf113407054775efd4a508ae03c65`  
		Last Modified: Tue, 03 Jun 2025 14:45:10 GMT  
		Size: 1.9 MB (1932426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0f27bac94157c911304329980a3ac043834b3407e7ebf8f6a152d114f5949c`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec883045be124559e6a84f03b352a143404848596a99aacded6fe91e3150c5eb`  
		Last Modified: Tue, 03 Jun 2025 14:45:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:aa82a1a35cac8440e684fe5059460736ac54ad11d07080afd5fe8fc546806556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.1 KB (118146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc357c735ee41efba1c1c97057f37ee17ce47e28b9887307cbd229d6895da03`

```dockerfile
```

-	Layers:
	-	`sha256:194792c5d362608149275ef412c050bbec126c27232fd4210029e547cac00ae7`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddb88c4acf94b34eadf22eea85377681f766029d1748d93ace4a6a7e7b23538a`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 23.9 KB (23863 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; s390x

```console
$ docker pull memcached@sha256:656e879b0120ed1dc41f4eea945ffd837cbd61df8792d9622df23bb94621dcba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5800523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6248ca4cb8546aea87cb93f6af7f23e99e572b78a8454a9af00758038970fb5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb224b0e357fdb3b8b28a5e9a31cd54bf59197e6b87eff81737fee0cbf2326d1`  
		Last Modified: Tue, 03 Jun 2025 14:45:11 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ffb790e1ad6ec57e858ea0d68a71a20c8d4f1e44cb7d1089e651677c61ff004`  
		Last Modified: Tue, 03 Jun 2025 14:45:11 GMT  
		Size: 113.5 KB (113497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ed9fcfc8c703bdee212b6c00a17c6ea94d9ae8e768825af3a9999a2cc0aa5f`  
		Last Modified: Tue, 03 Jun 2025 14:45:11 GMT  
		Size: 2.0 MB (2038146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d331df3ee94402980d3422bee4dcbd4613703a284b9ccc1fe1f6fdec3f4d869`  
		Last Modified: Tue, 03 Jun 2025 14:45:11 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93af5977e9aba9bde51aba44398ec5690948753fa15a6c35e41208a543d6c2e`  
		Last Modified: Tue, 03 Jun 2025 14:45:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:3dd443c4d6c4cbce2a2b09a2b2869282e7d1478a57e9967b3b38705268315e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.0 KB (118019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538a73a14cc21737f67c2f643b673960e4d7c106988e28fa3bb45734ed83532d`

```dockerfile
```

-	Layers:
	-	`sha256:726d5699c7a6f8c2cc2e05311aefbfc8a4a5369d49388faaf922cdf278a20b7c`  
		Last Modified: Tue, 03 Jun 2025 14:45:12 GMT  
		Size: 94.2 KB (94229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:382c68890507f3d9fe2510636665755df015b0354866ac714c3e70a3201ca87e`  
		Last Modified: Tue, 03 Jun 2025 14:45:11 GMT  
		Size: 23.8 KB (23790 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine3.22`

```console
$ docker pull memcached@sha256:08b6a6cba188fab22215b24a3d5c1ccc18343bc337268f663f20cd86dbdfffeb
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

### `memcached:alpine3.22` - linux; amd64

```console
$ docker pull memcached@sha256:606d01f5580448504043b6ca9994e651efd5cd79822d58639d3f7cb17850fe19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5901265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be94f0135609b0bf7b7f5787294b235034eed9e87be4689825605790d50cff24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef12469432374e0b8bca5dba738c021a8d10c2fc0374275956b8104d92b4053`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b606d4a25237e4f6fe0e5c302a9e8567588be271b95f83da33a31499dac8b0`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 104.7 KB (104728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05dc60670fe6d174274d0896db26274c8ef0e2f77afc45eb51b7cdefceddab51`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 2.0 MB (1998336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa1296a9dd4dfcfb8fcefddbc83edb103f22840e4a193ee7a1e207b232e7338e`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea55364413c47b3f8818b61b2de7d3e3a28b8592bbe25c146ef8a1edf4a17363`  
		Last Modified: Tue, 03 Jun 2025 13:30:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:552c1686ee77c9b7fba7c898a29803c51578a0e80715122dccafcb355025c0de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 KB (119969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb77b32517cfa4aa8e784ef0102259db59c51c349a263d3c87b50ed983fc3ef`

```dockerfile
```

-	Layers:
	-	`sha256:ce2831bada0ca80b430da313ea1ccf45204f6ca84dec4484adbc614b9494be4f`  
		Last Modified: Tue, 03 Jun 2025 14:45:05 GMT  
		Size: 96.2 KB (96180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2114cfbb746c8f95ef4f406bb87b6458f0b23a4844fe5a9774c62c1e9255d42c`  
		Last Modified: Tue, 03 Jun 2025 14:45:05 GMT  
		Size: 23.8 KB (23789 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:41a88acc0a34fb3e7bf86b58cd20dce95d6a609303362364ed6f7f7bd3079880
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6247593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7dfc69a347c50839ad628b964963b8149866c24446202e5789804bc8067e23c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf218c5787338a7792daeaefbb181cf59684549881841831603999e10d5187e`  
		Last Modified: Tue, 03 Jun 2025 13:30:42 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661f41de55d4df851603ae02c2cdc6e73b2ab9a9ecf45eac9b82f105cb482ee1`  
		Last Modified: Tue, 03 Jun 2025 13:32:27 GMT  
		Size: 120.8 KB (120818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e622a5461288686c20e7803ad3d17a45f79a7b140e90b6bbcb6bc8f462c57010`  
		Last Modified: Tue, 03 Jun 2025 13:34:11 GMT  
		Size: 2.0 MB (1989486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd408342d331a0cceff7d0f0d80a5ec8f14ea99c95791d36a29518931ebefb8e`  
		Last Modified: Tue, 03 Jun 2025 13:30:50 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9520bec02cd5779ce2136e2d96c570b84f26641fe4e391f33fb8228c77f4aeac`  
		Last Modified: Tue, 03 Jun 2025 13:30:57 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:e3d2683766797f6a8fe83ea61b5a2979ef33a4d78ea3e0aa9047e37cd2a3fd7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 KB (120271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7447a1da56e995b60bc91c0a003ba4d9d9a6c78fc3a8f9220e19353f0eebc3fc`

```dockerfile
```

-	Layers:
	-	`sha256:ca6f6e30cd21da5e6e9e17e53ca50b541ab1099c4a87acc15081d16797f581c2`  
		Last Modified: Tue, 03 Jun 2025 14:45:05 GMT  
		Size: 96.3 KB (96284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e835bdadfb4d4407a7c5d19b63c33e1f15ec1d83efbabf27ae3e33553a599c2a`  
		Last Modified: Tue, 03 Jun 2025 14:45:05 GMT  
		Size: 24.0 KB (23987 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.22` - linux; 386

```console
$ docker pull memcached@sha256:39a104f3004fd4a9e820173573ffcc2b15ec2948ca68e6b3d8cfe0e3ecdd12b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5686724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34077a3f17da3a414af6d200ebb8d57c0e73bd8d1d460d1e2ed17e8cc61341c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4498fffb412d9bcc1b73bd7bfa0d2754cf5230f83c22efba4479b1854b502291`  
		Last Modified: Tue, 03 Jun 2025 14:45:06 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7c585852f370434b2f4b564d7ec7ea58c5b06e528ac6b8dffd1212dd6f521e`  
		Last Modified: Tue, 03 Jun 2025 14:45:06 GMT  
		Size: 109.5 KB (109520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc95d14dcefd82bdeb2d89e3ba0fad63fd7fc93194f678a93bc1d9217b9c2ff`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 2.0 MB (1959822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f21560067e099265312c0975371d273829c2923dee88b90d7e24537a458d696`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f53957473f72614ae6b6abc50bff4d20acd3a704edb23755b4e2a5bb6f71a7aa`  
		Last Modified: Tue, 03 Jun 2025 14:45:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:3d21a067c964615eb13e5e591df9d66ea730e3a04be65f71321ad10f1c367d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.9 KB (119867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:897704751afe9189615b739f6bf4308d242df30afe8b42aff038d7828ab081db`

```dockerfile
```

-	Layers:
	-	`sha256:6e6181041c0daeaf47a8f8475f930b1ea73d5cf55a7b5a7b3efba14627e6e8c4`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 96.1 KB (96135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:768c02304a965eacaab05dd9b82b91c453a28d3fbc77b34221ab010ccc28cbcb`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 23.7 KB (23732 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.22` - linux; ppc64le

```console
$ docker pull memcached@sha256:0bf6f7efe5d3e4b11cec8d17f924ae42d7622e1b0bbcdb56d4757bb3d22ab4b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5947182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf2f7366cf8143a64896b9b751eadad7798b3eec347162fca324567acec20082`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6dc89a1ff7a965251a27c2d9dcb719f464507b964ba3286d6a6034d9f89769`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d75cf13bd9119987f7710d75fd446cd9d065487b3e83297be8c9c4b3120e7e`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 124.3 KB (124312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9461b52977c4cd8b006ffee034043d389554e4c3b267b0901829e7a7a353b8`  
		Last Modified: Tue, 03 Jun 2025 14:45:08 GMT  
		Size: 2.1 MB (2091330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c2dc09d491c7a103b9bd75fa5267b316526d77163130840938eadadb72e6b1`  
		Last Modified: Tue, 03 Jun 2025 14:45:08 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bece68e2cfcb576a9778e7da37d6e2a58ac091bd908caf52a90c4baf09d4d079`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:efd926e1e98c4bedf0db6b24ec177d116548e0652d6b66db54cb2a3e81d21899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 KB (118151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57233506303dd47952c792831142da6a3fe9c4e6c5ea7678ff91b329c08e589`

```dockerfile
```

-	Layers:
	-	`sha256:ed1b26ef88ce71431cfd88a99e6d2d4d13494e7bf5056e489b0b1eb2133d81ab`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 94.3 KB (94287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eaf4c09f8a1fb9991161e85051ae93568c08ab9b2a1142b1bbf99a182e7c0f0`  
		Last Modified: Tue, 03 Jun 2025 14:45:07 GMT  
		Size: 23.9 KB (23864 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.22` - linux; riscv64

```console
$ docker pull memcached@sha256:aed10964c6cc121d6201aaa8301e269cb88396f19e514ab4529073da9d0c2218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f0390597339801ec08bfd34d10d8bf91dc8e03f2e864f9643758e7ade704d40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db926e6f83170fbe6f646943cb34741a092b9ce5226a6d1bd6b9214d4515055f`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1884ffba96f71fb43c1fef7f0405221b4c8070f55b8667e8b75cc04d268f5cbc`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 107.9 KB (107905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9dea200205fca0caa1f83f40ea69123226bf113407054775efd4a508ae03c65`  
		Last Modified: Tue, 03 Jun 2025 14:45:10 GMT  
		Size: 1.9 MB (1932426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0f27bac94157c911304329980a3ac043834b3407e7ebf8f6a152d114f5949c`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec883045be124559e6a84f03b352a143404848596a99aacded6fe91e3150c5eb`  
		Last Modified: Tue, 03 Jun 2025 14:45:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:aa82a1a35cac8440e684fe5059460736ac54ad11d07080afd5fe8fc546806556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.1 KB (118146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc357c735ee41efba1c1c97057f37ee17ce47e28b9887307cbd229d6895da03`

```dockerfile
```

-	Layers:
	-	`sha256:194792c5d362608149275ef412c050bbec126c27232fd4210029e547cac00ae7`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddb88c4acf94b34eadf22eea85377681f766029d1748d93ace4a6a7e7b23538a`  
		Last Modified: Tue, 03 Jun 2025 14:45:09 GMT  
		Size: 23.9 KB (23863 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.22` - linux; s390x

```console
$ docker pull memcached@sha256:656e879b0120ed1dc41f4eea945ffd837cbd61df8792d9622df23bb94621dcba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5800523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6248ca4cb8546aea87cb93f6af7f23e99e572b78a8454a9af00758038970fb5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_VERSION=1.6.38
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Fri, 30 May 2025 18:54:14 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Fri, 30 May 2025 18:54:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 30 May 2025 18:54:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:54:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 30 May 2025 18:54:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:54:14 GMT
USER memcache
# Fri, 30 May 2025 18:54:14 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 30 May 2025 18:54:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb224b0e357fdb3b8b28a5e9a31cd54bf59197e6b87eff81737fee0cbf2326d1`  
		Last Modified: Tue, 03 Jun 2025 14:45:11 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ffb790e1ad6ec57e858ea0d68a71a20c8d4f1e44cb7d1089e651677c61ff004`  
		Last Modified: Tue, 03 Jun 2025 14:45:11 GMT  
		Size: 113.5 KB (113497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ed9fcfc8c703bdee212b6c00a17c6ea94d9ae8e768825af3a9999a2cc0aa5f`  
		Last Modified: Tue, 03 Jun 2025 14:45:11 GMT  
		Size: 2.0 MB (2038146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d331df3ee94402980d3422bee4dcbd4613703a284b9ccc1fe1f6fdec3f4d869`  
		Last Modified: Tue, 03 Jun 2025 14:45:11 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93af5977e9aba9bde51aba44398ec5690948753fa15a6c35e41208a543d6c2e`  
		Last Modified: Tue, 03 Jun 2025 14:45:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:3dd443c4d6c4cbce2a2b09a2b2869282e7d1478a57e9967b3b38705268315e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.0 KB (118019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538a73a14cc21737f67c2f643b673960e4d7c106988e28fa3bb45734ed83532d`

```dockerfile
```

-	Layers:
	-	`sha256:726d5699c7a6f8c2cc2e05311aefbfc8a4a5369d49388faaf922cdf278a20b7c`  
		Last Modified: Tue, 03 Jun 2025 14:45:12 GMT  
		Size: 94.2 KB (94229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:382c68890507f3d9fe2510636665755df015b0354866ac714c3e70a3201ca87e`  
		Last Modified: Tue, 03 Jun 2025 14:45:11 GMT  
		Size: 23.8 KB (23790 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:bookworm`

```console
$ docker pull memcached@sha256:89b2dfa7e55e5fd1986e22210cdf89f0a5e5d6c913101e2bcfdfb4d1d73de7ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:bookworm` - linux; amd64

```console
$ docker pull memcached@sha256:c2b5b37862a0d15d6622bea58a1e3a7a34610456324dc81a6de4e3369d06a5f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33026651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:809ba6b39db15dffb27e2affc4fc5bc5eee2c32ee9b06e08f2f604ee63e41a78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35255ebbfb2408b64a9d53c3d868456872a9b4d89ff4e80f2a8d20c4332dd69`  
		Last Modified: Tue, 10 Jun 2025 23:32:18 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be9410e6aeed64e084cb2812f5d70658e1a9ffe79b5972cea39097c9b949e4e`  
		Last Modified: Tue, 10 Jun 2025 23:32:19 GMT  
		Size: 2.5 MB (2492199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d86227fbbb72b09a47e8016b198dc2062598d3e4c4b358cfa655a2a2c044ef`  
		Last Modified: Tue, 10 Jun 2025 23:32:20 GMT  
		Size: 2.3 MB (2302808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad105488469355bcd85bf5c9c6b74cf9729838da44ad0c6f500f252c6860e8c`  
		Last Modified: Tue, 10 Jun 2025 23:32:20 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90864ece76220d4e897cf79c19145c02ce9d1c1326bb831401963b27ec0ca566`  
		Last Modified: Tue, 10 Jun 2025 23:32:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:5b481897e28479249d51b4c0720b45485fe1952dcb27924f267fcd30d68de833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2425304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6773503e415cd198fe6533c8042593b7aabb0d583e0baf500eed5c4c78452531`

```dockerfile
```

-	Layers:
	-	`sha256:4c6461ec41fb74fe203eb1b6c30c50eddc7f6c11871bfa03eab07db6a4b17c6f`  
		Last Modified: Wed, 11 Jun 2025 00:34:27 GMT  
		Size: 2.4 MB (2399984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e35a57a543fde6b5a8a3e185100a7e9b5ac2a947dea0b7589b5531fab06c67c`  
		Last Modified: Wed, 11 Jun 2025 00:34:28 GMT  
		Size: 25.3 KB (25320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:ca1e51720502c0722aae38efd0a64db105570638d65d6a70ab4572658aff584a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.1 MB (30093253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86fc08738ceff7b24bd461ffd9a41799a048727c6673c1a3c4cb5a01f6b82608`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:750907abe8bb5d66304ed40261e1579b6575871f6848cfbd720888c20afd3b67`  
		Last Modified: Tue, 10 Jun 2025 22:47:31 GMT  
		Size: 25.8 MB (25762396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9660206a4f42b745fdc386aced2845f4fa99b6de361892e4df07c2daf0f24c`  
		Last Modified: Wed, 11 Jun 2025 00:04:16 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877a28dd495fb8632729edaf5b9318ec22ce2a5e402b746782fb7084fd01032c`  
		Last Modified: Wed, 11 Jun 2025 00:04:19 GMT  
		Size: 2.1 MB (2097026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06cb49b999b102d1dc8725fedf17028635be0bcc810a049a03c6e96128a9e4e6`  
		Last Modified: Wed, 11 Jun 2025 00:04:30 GMT  
		Size: 2.2 MB (2232317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee68dfb7714895c5d09887e2708b1296a8855e4ac7ff3d0a158bf029e81e157`  
		Last Modified: Wed, 11 Jun 2025 00:04:39 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff86e8516fa08ad0aa15dfb3afebb40da609006594dcf941ed7900b39cec11aa`  
		Last Modified: Wed, 11 Jun 2025 00:04:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:68162c3dae075d4cb8b6a636c634479c8402119be9f3b6f995913ba4d47162e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2429297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10be7e4ce251f42cb456f15eae67ae97fc6e3040fc50fe0990c4503b35a8829b`

```dockerfile
```

-	Layers:
	-	`sha256:5874edec5896e806374ff905b6f10f3724d44a31a61bf0d830a5ecac4cfbb548`  
		Last Modified: Wed, 11 Jun 2025 03:34:34 GMT  
		Size: 2.4 MB (2403830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54b0ebcaf098420587b0d84ab425ad9abdfc444c86c6ba478b50be7b335cd3c6`  
		Last Modified: Wed, 11 Jun 2025 03:34:34 GMT  
		Size: 25.5 KB (25467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm variant v7

```console
$ docker pull memcached@sha256:d208683140025f905b085b97b35b3a533015b73809d3740e5e3d968c202ec9e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28070929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b74912d1ce300e7a774e690f1c07510c2228991f23ee542e33cc1028e45d90bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6615a784a0e15fd2ed6d79980e68d9cfe87df589b9af6f4c71656286b040acc`  
		Last Modified: Tue, 10 Jun 2025 23:43:55 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66fc152354c58f6024d7e37104e92e718be7b1e70f9745e96e63006f79730f5`  
		Last Modified: Tue, 10 Jun 2025 23:43:56 GMT  
		Size: 1.9 MB (1946292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3712992b59c9c2fa191ca82275b5fb441fcc21940ef625721d0221723f70d9e`  
		Last Modified: Tue, 10 Jun 2025 23:43:56 GMT  
		Size: 2.2 MB (2184378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ba9e36b6e72e151a91cc69343438b9341451e4196d29b259766ab25ece2755`  
		Last Modified: Tue, 10 Jun 2025 23:43:56 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f566ffc3a278d8a018e52b43be1df458ee6632e59b56f75a94a0d058a6cfe73`  
		Last Modified: Tue, 10 Jun 2025 23:43:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:2bbfd653e524ef9316e75f9681ac6876a3e40a63ac124b1e00216760e2855ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2427734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e73cc4fc38d626337d836752990c011dfc545348cb8fd74aa3ae7a39e08c5bc`

```dockerfile
```

-	Layers:
	-	`sha256:8eec2d1ef62751b78959b1e676c070de5b6da4490f0797715b6038816e6ecbe7`  
		Last Modified: Wed, 11 Jun 2025 00:34:36 GMT  
		Size: 2.4 MB (2402267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7bd74b81adae550be8823fda7677f05554265436005a14b9a3f3775ec776a45`  
		Last Modified: Wed, 11 Jun 2025 00:34:37 GMT  
		Size: 25.5 KB (25467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:8a7286d77ae74f81f50dffd6f6e763edd304ed10f5a56e2fe3bdbc38578586a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32723815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05a57428c8257697aa07726f04832bba5278021c4028ea564ada3e7c63bf181`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c5447936c48fe52b15de86391eaf4d170445111319a12dd6f05a85d115b1a4`  
		Last Modified: Wed, 11 Jun 2025 00:32:55 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfca24a3c9155df906544ba98f8bb2bc9f66d9704ed8edf0e731bfe4672420d2`  
		Last Modified: Wed, 11 Jun 2025 00:32:58 GMT  
		Size: 2.4 MB (2355841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eab66920dbc0773d0617dced9ec788e2dc243fc3c3abb0855646922df94744d`  
		Last Modified: Wed, 11 Jun 2025 00:33:04 GMT  
		Size: 2.3 MB (2288782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99014141349bea93d0cf26fd4326ec422f06a635c0ba43644c022fc9960456b8`  
		Last Modified: Wed, 11 Jun 2025 00:33:09 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c855df1fbe1070effdf016a21c2055af95b6325b3e22aa0f32e24d1896dd7a1a`  
		Last Modified: Wed, 11 Jun 2025 00:33:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:45dd4c7b93d5dc7ac1a41023089465fc7feeb3a6878b831308593b595c4453ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2425816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d377887b57b57637deedd7fc6db230aceaeb6f127b9d419649daf5eb921dcfe3`

```dockerfile
```

-	Layers:
	-	`sha256:104fd15db5961a346a71d8c3471d234720c45848fed57ef5c979b5904c13679d`  
		Last Modified: Wed, 11 Jun 2025 03:34:41 GMT  
		Size: 2.4 MB (2400299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b12674469f62c07ff246f7a86cd72871b797a081f0f1a29ebf34768864970340`  
		Last Modified: Wed, 11 Jun 2025 03:34:42 GMT  
		Size: 25.5 KB (25517 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; 386

```console
$ docker pull memcached@sha256:2fd3408e4989cc9e56a6d3add7ce53181decaf9d7cc19e14b49670b45944e40e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33967948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a326ebe4a452ab75793d01324bf45cdf00e7f2aa83d4793e9993f6317370b81`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c3d46fed134488b3ee18c12cb308c8d5520b8c647122c392f9fb76e3e1e2fc61`  
		Last Modified: Tue, 10 Jun 2025 22:47:25 GMT  
		Size: 29.2 MB (29212433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6e1ece79d563054c9ed24818e5adb5d97e5a1bd3a898d27b10ad0ed0d944fe`  
		Last Modified: Tue, 10 Jun 2025 23:32:02 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d82ab526e835ea99bac51cedfd44fda08d1096806527e0e4776d1747931bfb`  
		Last Modified: Tue, 10 Jun 2025 23:32:03 GMT  
		Size: 2.5 MB (2502688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c26ac869e988fa955c3c084363eb741d506a2034cdd3e12a5c98ff74e4c65c5`  
		Last Modified: Tue, 10 Jun 2025 23:32:03 GMT  
		Size: 2.3 MB (2251313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87ab77943d07e12971b970348f051de5367dd6a2bb147741b63f12eca74d55f`  
		Last Modified: Tue, 10 Jun 2025 23:32:03 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5505b2cac6d2a77393345699695a05426271e871ba824bf0e22789a5cdf44f8e`  
		Last Modified: Tue, 10 Jun 2025 23:32:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f5178b4eff39883c5450012b44b95dc2e13a26e5c3efe2221f9a929a01b99a6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2422389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db0fa4b9612a2b4b5f20852ca646c7fa318ae7057ec68f20599d1281453c0ac5`

```dockerfile
```

-	Layers:
	-	`sha256:27ef430fcb7445f00c5cbbac9416a8082301986670c56b7112c8ee8d2bc7ea63`  
		Last Modified: Wed, 11 Jun 2025 00:34:45 GMT  
		Size: 2.4 MB (2397127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c71e82389c2ff610732d9cc27ec31e1061a1fe683a7594c559d2f0ad1b307bf`  
		Last Modified: Wed, 11 Jun 2025 00:34:46 GMT  
		Size: 25.3 KB (25262 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:4dcc31fdaa97e6430560dfb497e4dde22b2ef368e6c66a3b271a5343bfd86e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32779330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6bba452dff6149dc16dfc6eda06981c4240993be55b9b6f998d30e26935e676`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ac3f61581c7f5755d8598b3a0857c417db0251b17c0e4e4f43a5fc0e24023524`  
		Last Modified: Tue, 10 Jun 2025 22:48:26 GMT  
		Size: 28.5 MB (28516717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b713f027201c7d06c5013a8693a2fb17e64d3d8113328cd83f01c565ddd25a31`  
		Last Modified: Wed, 11 Jun 2025 00:38:45 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699452fffd3fdc6e04d5c6c072d85da568d4477714b34612b15505bebad40576`  
		Last Modified: Wed, 11 Jun 2025 00:38:49 GMT  
		Size: 1.9 MB (1944083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4909573bcae2300d9ad92749c2279eaab07c75210c195cc36bcc323a289711c`  
		Last Modified: Wed, 11 Jun 2025 00:38:54 GMT  
		Size: 2.3 MB (2317017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42800230fbc3a3fdd8ebd615178ea6d750f32c99d916c8d4c1fce650c9724740`  
		Last Modified: Wed, 11 Jun 2025 00:39:03 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc602c2ec2581679f4ba36524612bf709f9828eae2e8e2382a5b72cfe43ddde`  
		Last Modified: Wed, 11 Jun 2025 00:39:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:c8b58a5685ab59a7e412a46fadca1a86a8065cb821c20aa84496f3da2932a6bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d142d271ffff6f14e07b46862b9d5c35a3f62a5ae21f22698dbf2729e22393e5`

```dockerfile
```

-	Layers:
	-	`sha256:0c2d883e7eeaa126767df6696d4d4d21074e1b88388aca7a8d9936e34d972390`  
		Last Modified: Wed, 11 Jun 2025 03:34:48 GMT  
		Size: 25.2 KB (25216 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:ec8926cb7edeb9e447cfa09a6496daf6ddf6214c670db96c915bfbfcdd867a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37203472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f834c7368564e22deca1fec762744af6a328960d29a0757f965efb0922ef2ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c9cd5d5c131a8141631d87d9507a82e0549a2144689442301c07d2da80f39d19`  
		Last Modified: Tue, 10 Jun 2025 23:58:45 GMT  
		Size: 32.1 MB (32072795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783cc02b7ca742bdfa931c46ca74a297d6743f7632079af1d38a86f0ef33e67e`  
		Last Modified: Tue, 10 Jun 2025 23:50:23 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dcb0a6965f82b33b339604c7bfc7e13fddac325187039be9416554f6deaa468`  
		Last Modified: Tue, 10 Jun 2025 23:50:24 GMT  
		Size: 2.7 MB (2710185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460f1a7eb5adf7c13e3a2c6e82959f31bd877cd781b02a5997ba29d421ea0845`  
		Last Modified: Tue, 10 Jun 2025 23:50:24 GMT  
		Size: 2.4 MB (2418981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5dbb0f6f2b188832219b7b4c16a43d53399710d576b050d6939a213e05dd83`  
		Last Modified: Tue, 10 Jun 2025 23:50:24 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ce0fe2674fef821731c0bf8d4218891392e919b579863b73b27c02281d67bb`  
		Last Modified: Tue, 10 Jun 2025 23:50:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:295a95b2a5fbcaba4f0430c8b8fc00ec4ebe4a3ab75480f5ed7890dd086efdc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2429850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd03034a2e56497ce0625f4e0bfba90e28c4d23be1250fe5547dfab3f61abd66`

```dockerfile
```

-	Layers:
	-	`sha256:5e551af8256cd1f6d5d31b7a99d5338c2e0f7c59dd109277d12a1d01c1f8e4dc`  
		Last Modified: Wed, 11 Jun 2025 03:34:53 GMT  
		Size: 2.4 MB (2404456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eac12139332bd876a1e77dd40aa823e07245885fb8a0d33164fd342e6a3198b9`  
		Last Modified: Wed, 11 Jun 2025 03:34:54 GMT  
		Size: 25.4 KB (25394 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:04933adc68fd0a9324a7d5796e1d3cde2a0012644f2ea93c60f0b9ef4f676e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31309863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d59a9f1fa8b8ed5157a51f715aac503833e36e3aa6da498fd68e1647c8366e7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d890a6beb4a310ea4195e7ebd130e37a17b64820c995a543bb5619b2eab1e6`  
		Last Modified: Wed, 11 Jun 2025 09:15:09 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119a4250ae0069dea78d2943d561ab4ad7db7018ddd34dcdf8ceecada8494508`  
		Last Modified: Wed, 11 Jun 2025 09:15:10 GMT  
		Size: 2.2 MB (2156963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eea4eabc325c68a766c64d84b958281150eee02f4ada0091377c9af7b07a793`  
		Last Modified: Wed, 11 Jun 2025 09:15:10 GMT  
		Size: 2.3 MB (2263533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ddbca61153701e80e50122cb3d22cd45a49b4bf191114e8b132b588b077673`  
		Last Modified: Wed, 11 Jun 2025 09:15:10 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42132a3abe6b3ca5bc8e4e623ffa00fe86641a0a42454bba499fa70136dea21`  
		Last Modified: Wed, 11 Jun 2025 09:15:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:2f715ae3a26ddc650f595ca31d33c4a4c14311b1347a6e8d20aca949b131063d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2422126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a4df8b3c359f6d964f37642182e6de7a4cd8cc28676c409e313aa88eaf5b698`

```dockerfile
```

-	Layers:
	-	`sha256:994b93c94dedc6bf0bf79fcfb6b5332c77a3fea69cd945274a1b5eead27d80e0`  
		Last Modified: Wed, 11 Jun 2025 12:34:39 GMT  
		Size: 2.4 MB (2396806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bd4c128777cf5eda46cb5a3ab851f4294546c4b8267f89d17b1adfc4ad5e9bd`  
		Last Modified: Wed, 11 Jun 2025 12:34:40 GMT  
		Size: 25.3 KB (25320 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:latest`

```console
$ docker pull memcached@sha256:89b2dfa7e55e5fd1986e22210cdf89f0a5e5d6c913101e2bcfdfb4d1d73de7ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:latest` - linux; amd64

```console
$ docker pull memcached@sha256:c2b5b37862a0d15d6622bea58a1e3a7a34610456324dc81a6de4e3369d06a5f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33026651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:809ba6b39db15dffb27e2affc4fc5bc5eee2c32ee9b06e08f2f604ee63e41a78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35255ebbfb2408b64a9d53c3d868456872a9b4d89ff4e80f2a8d20c4332dd69`  
		Last Modified: Tue, 10 Jun 2025 23:32:18 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be9410e6aeed64e084cb2812f5d70658e1a9ffe79b5972cea39097c9b949e4e`  
		Last Modified: Tue, 10 Jun 2025 23:32:19 GMT  
		Size: 2.5 MB (2492199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d86227fbbb72b09a47e8016b198dc2062598d3e4c4b358cfa655a2a2c044ef`  
		Last Modified: Tue, 10 Jun 2025 23:32:20 GMT  
		Size: 2.3 MB (2302808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad105488469355bcd85bf5c9c6b74cf9729838da44ad0c6f500f252c6860e8c`  
		Last Modified: Tue, 10 Jun 2025 23:32:20 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90864ece76220d4e897cf79c19145c02ce9d1c1326bb831401963b27ec0ca566`  
		Last Modified: Tue, 10 Jun 2025 23:32:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:5b481897e28479249d51b4c0720b45485fe1952dcb27924f267fcd30d68de833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2425304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6773503e415cd198fe6533c8042593b7aabb0d583e0baf500eed5c4c78452531`

```dockerfile
```

-	Layers:
	-	`sha256:4c6461ec41fb74fe203eb1b6c30c50eddc7f6c11871bfa03eab07db6a4b17c6f`  
		Last Modified: Wed, 11 Jun 2025 00:34:27 GMT  
		Size: 2.4 MB (2399984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e35a57a543fde6b5a8a3e185100a7e9b5ac2a947dea0b7589b5531fab06c67c`  
		Last Modified: Wed, 11 Jun 2025 00:34:28 GMT  
		Size: 25.3 KB (25320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:ca1e51720502c0722aae38efd0a64db105570638d65d6a70ab4572658aff584a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.1 MB (30093253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86fc08738ceff7b24bd461ffd9a41799a048727c6673c1a3c4cb5a01f6b82608`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:750907abe8bb5d66304ed40261e1579b6575871f6848cfbd720888c20afd3b67`  
		Last Modified: Tue, 10 Jun 2025 22:47:31 GMT  
		Size: 25.8 MB (25762396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9660206a4f42b745fdc386aced2845f4fa99b6de361892e4df07c2daf0f24c`  
		Last Modified: Wed, 11 Jun 2025 00:04:16 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877a28dd495fb8632729edaf5b9318ec22ce2a5e402b746782fb7084fd01032c`  
		Last Modified: Wed, 11 Jun 2025 00:04:19 GMT  
		Size: 2.1 MB (2097026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06cb49b999b102d1dc8725fedf17028635be0bcc810a049a03c6e96128a9e4e6`  
		Last Modified: Wed, 11 Jun 2025 00:04:30 GMT  
		Size: 2.2 MB (2232317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee68dfb7714895c5d09887e2708b1296a8855e4ac7ff3d0a158bf029e81e157`  
		Last Modified: Wed, 11 Jun 2025 00:04:39 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff86e8516fa08ad0aa15dfb3afebb40da609006594dcf941ed7900b39cec11aa`  
		Last Modified: Wed, 11 Jun 2025 00:04:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:68162c3dae075d4cb8b6a636c634479c8402119be9f3b6f995913ba4d47162e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2429297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10be7e4ce251f42cb456f15eae67ae97fc6e3040fc50fe0990c4503b35a8829b`

```dockerfile
```

-	Layers:
	-	`sha256:5874edec5896e806374ff905b6f10f3724d44a31a61bf0d830a5ecac4cfbb548`  
		Last Modified: Wed, 11 Jun 2025 03:34:34 GMT  
		Size: 2.4 MB (2403830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54b0ebcaf098420587b0d84ab425ad9abdfc444c86c6ba478b50be7b335cd3c6`  
		Last Modified: Wed, 11 Jun 2025 03:34:34 GMT  
		Size: 25.5 KB (25467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v7

```console
$ docker pull memcached@sha256:d208683140025f905b085b97b35b3a533015b73809d3740e5e3d968c202ec9e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28070929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b74912d1ce300e7a774e690f1c07510c2228991f23ee542e33cc1028e45d90bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6615a784a0e15fd2ed6d79980e68d9cfe87df589b9af6f4c71656286b040acc`  
		Last Modified: Tue, 10 Jun 2025 23:43:55 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66fc152354c58f6024d7e37104e92e718be7b1e70f9745e96e63006f79730f5`  
		Last Modified: Tue, 10 Jun 2025 23:43:56 GMT  
		Size: 1.9 MB (1946292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3712992b59c9c2fa191ca82275b5fb441fcc21940ef625721d0221723f70d9e`  
		Last Modified: Tue, 10 Jun 2025 23:43:56 GMT  
		Size: 2.2 MB (2184378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ba9e36b6e72e151a91cc69343438b9341451e4196d29b259766ab25ece2755`  
		Last Modified: Tue, 10 Jun 2025 23:43:56 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f566ffc3a278d8a018e52b43be1df458ee6632e59b56f75a94a0d058a6cfe73`  
		Last Modified: Tue, 10 Jun 2025 23:43:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:2bbfd653e524ef9316e75f9681ac6876a3e40a63ac124b1e00216760e2855ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2427734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e73cc4fc38d626337d836752990c011dfc545348cb8fd74aa3ae7a39e08c5bc`

```dockerfile
```

-	Layers:
	-	`sha256:8eec2d1ef62751b78959b1e676c070de5b6da4490f0797715b6038816e6ecbe7`  
		Last Modified: Wed, 11 Jun 2025 00:34:36 GMT  
		Size: 2.4 MB (2402267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7bd74b81adae550be8823fda7677f05554265436005a14b9a3f3775ec776a45`  
		Last Modified: Wed, 11 Jun 2025 00:34:37 GMT  
		Size: 25.5 KB (25467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:8a7286d77ae74f81f50dffd6f6e763edd304ed10f5a56e2fe3bdbc38578586a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32723815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05a57428c8257697aa07726f04832bba5278021c4028ea564ada3e7c63bf181`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c5447936c48fe52b15de86391eaf4d170445111319a12dd6f05a85d115b1a4`  
		Last Modified: Wed, 11 Jun 2025 00:32:55 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfca24a3c9155df906544ba98f8bb2bc9f66d9704ed8edf0e731bfe4672420d2`  
		Last Modified: Wed, 11 Jun 2025 00:32:58 GMT  
		Size: 2.4 MB (2355841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eab66920dbc0773d0617dced9ec788e2dc243fc3c3abb0855646922df94744d`  
		Last Modified: Wed, 11 Jun 2025 00:33:04 GMT  
		Size: 2.3 MB (2288782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99014141349bea93d0cf26fd4326ec422f06a635c0ba43644c022fc9960456b8`  
		Last Modified: Wed, 11 Jun 2025 00:33:09 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c855df1fbe1070effdf016a21c2055af95b6325b3e22aa0f32e24d1896dd7a1a`  
		Last Modified: Wed, 11 Jun 2025 00:33:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:45dd4c7b93d5dc7ac1a41023089465fc7feeb3a6878b831308593b595c4453ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2425816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d377887b57b57637deedd7fc6db230aceaeb6f127b9d419649daf5eb921dcfe3`

```dockerfile
```

-	Layers:
	-	`sha256:104fd15db5961a346a71d8c3471d234720c45848fed57ef5c979b5904c13679d`  
		Last Modified: Wed, 11 Jun 2025 03:34:41 GMT  
		Size: 2.4 MB (2400299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b12674469f62c07ff246f7a86cd72871b797a081f0f1a29ebf34768864970340`  
		Last Modified: Wed, 11 Jun 2025 03:34:42 GMT  
		Size: 25.5 KB (25517 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:2fd3408e4989cc9e56a6d3add7ce53181decaf9d7cc19e14b49670b45944e40e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33967948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a326ebe4a452ab75793d01324bf45cdf00e7f2aa83d4793e9993f6317370b81`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c3d46fed134488b3ee18c12cb308c8d5520b8c647122c392f9fb76e3e1e2fc61`  
		Last Modified: Tue, 10 Jun 2025 22:47:25 GMT  
		Size: 29.2 MB (29212433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6e1ece79d563054c9ed24818e5adb5d97e5a1bd3a898d27b10ad0ed0d944fe`  
		Last Modified: Tue, 10 Jun 2025 23:32:02 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d82ab526e835ea99bac51cedfd44fda08d1096806527e0e4776d1747931bfb`  
		Last Modified: Tue, 10 Jun 2025 23:32:03 GMT  
		Size: 2.5 MB (2502688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c26ac869e988fa955c3c084363eb741d506a2034cdd3e12a5c98ff74e4c65c5`  
		Last Modified: Tue, 10 Jun 2025 23:32:03 GMT  
		Size: 2.3 MB (2251313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87ab77943d07e12971b970348f051de5367dd6a2bb147741b63f12eca74d55f`  
		Last Modified: Tue, 10 Jun 2025 23:32:03 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5505b2cac6d2a77393345699695a05426271e871ba824bf0e22789a5cdf44f8e`  
		Last Modified: Tue, 10 Jun 2025 23:32:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:f5178b4eff39883c5450012b44b95dc2e13a26e5c3efe2221f9a929a01b99a6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2422389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db0fa4b9612a2b4b5f20852ca646c7fa318ae7057ec68f20599d1281453c0ac5`

```dockerfile
```

-	Layers:
	-	`sha256:27ef430fcb7445f00c5cbbac9416a8082301986670c56b7112c8ee8d2bc7ea63`  
		Last Modified: Wed, 11 Jun 2025 00:34:45 GMT  
		Size: 2.4 MB (2397127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c71e82389c2ff610732d9cc27ec31e1061a1fe683a7594c559d2f0ad1b307bf`  
		Last Modified: Wed, 11 Jun 2025 00:34:46 GMT  
		Size: 25.3 KB (25262 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; mips64le

```console
$ docker pull memcached@sha256:4dcc31fdaa97e6430560dfb497e4dde22b2ef368e6c66a3b271a5343bfd86e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32779330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6bba452dff6149dc16dfc6eda06981c4240993be55b9b6f998d30e26935e676`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ac3f61581c7f5755d8598b3a0857c417db0251b17c0e4e4f43a5fc0e24023524`  
		Last Modified: Tue, 10 Jun 2025 22:48:26 GMT  
		Size: 28.5 MB (28516717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b713f027201c7d06c5013a8693a2fb17e64d3d8113328cd83f01c565ddd25a31`  
		Last Modified: Wed, 11 Jun 2025 00:38:45 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699452fffd3fdc6e04d5c6c072d85da568d4477714b34612b15505bebad40576`  
		Last Modified: Wed, 11 Jun 2025 00:38:49 GMT  
		Size: 1.9 MB (1944083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4909573bcae2300d9ad92749c2279eaab07c75210c195cc36bcc323a289711c`  
		Last Modified: Wed, 11 Jun 2025 00:38:54 GMT  
		Size: 2.3 MB (2317017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42800230fbc3a3fdd8ebd615178ea6d750f32c99d916c8d4c1fce650c9724740`  
		Last Modified: Wed, 11 Jun 2025 00:39:03 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc602c2ec2581679f4ba36524612bf709f9828eae2e8e2382a5b72cfe43ddde`  
		Last Modified: Wed, 11 Jun 2025 00:39:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:c8b58a5685ab59a7e412a46fadca1a86a8065cb821c20aa84496f3da2932a6bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d142d271ffff6f14e07b46862b9d5c35a3f62a5ae21f22698dbf2729e22393e5`

```dockerfile
```

-	Layers:
	-	`sha256:0c2d883e7eeaa126767df6696d4d4d21074e1b88388aca7a8d9936e34d972390`  
		Last Modified: Wed, 11 Jun 2025 03:34:48 GMT  
		Size: 25.2 KB (25216 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:ec8926cb7edeb9e447cfa09a6496daf6ddf6214c670db96c915bfbfcdd867a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37203472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f834c7368564e22deca1fec762744af6a328960d29a0757f965efb0922ef2ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c9cd5d5c131a8141631d87d9507a82e0549a2144689442301c07d2da80f39d19`  
		Last Modified: Tue, 10 Jun 2025 23:58:45 GMT  
		Size: 32.1 MB (32072795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783cc02b7ca742bdfa931c46ca74a297d6743f7632079af1d38a86f0ef33e67e`  
		Last Modified: Tue, 10 Jun 2025 23:50:23 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dcb0a6965f82b33b339604c7bfc7e13fddac325187039be9416554f6deaa468`  
		Last Modified: Tue, 10 Jun 2025 23:50:24 GMT  
		Size: 2.7 MB (2710185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460f1a7eb5adf7c13e3a2c6e82959f31bd877cd781b02a5997ba29d421ea0845`  
		Last Modified: Tue, 10 Jun 2025 23:50:24 GMT  
		Size: 2.4 MB (2418981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5dbb0f6f2b188832219b7b4c16a43d53399710d576b050d6939a213e05dd83`  
		Last Modified: Tue, 10 Jun 2025 23:50:24 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ce0fe2674fef821731c0bf8d4218891392e919b579863b73b27c02281d67bb`  
		Last Modified: Tue, 10 Jun 2025 23:50:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:295a95b2a5fbcaba4f0430c8b8fc00ec4ebe4a3ab75480f5ed7890dd086efdc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2429850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd03034a2e56497ce0625f4e0bfba90e28c4d23be1250fe5547dfab3f61abd66`

```dockerfile
```

-	Layers:
	-	`sha256:5e551af8256cd1f6d5d31b7a99d5338c2e0f7c59dd109277d12a1d01c1f8e4dc`  
		Last Modified: Wed, 11 Jun 2025 03:34:53 GMT  
		Size: 2.4 MB (2404456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eac12139332bd876a1e77dd40aa823e07245885fb8a0d33164fd342e6a3198b9`  
		Last Modified: Wed, 11 Jun 2025 03:34:54 GMT  
		Size: 25.4 KB (25394 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:04933adc68fd0a9324a7d5796e1d3cde2a0012644f2ea93c60f0b9ef4f676e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31309863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d59a9f1fa8b8ed5157a51f715aac503833e36e3aa6da498fd68e1647c8366e7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d890a6beb4a310ea4195e7ebd130e37a17b64820c995a543bb5619b2eab1e6`  
		Last Modified: Wed, 11 Jun 2025 09:15:09 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119a4250ae0069dea78d2943d561ab4ad7db7018ddd34dcdf8ceecada8494508`  
		Last Modified: Wed, 11 Jun 2025 09:15:10 GMT  
		Size: 2.2 MB (2156963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eea4eabc325c68a766c64d84b958281150eee02f4ada0091377c9af7b07a793`  
		Last Modified: Wed, 11 Jun 2025 09:15:10 GMT  
		Size: 2.3 MB (2263533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ddbca61153701e80e50122cb3d22cd45a49b4bf191114e8b132b588b077673`  
		Last Modified: Wed, 11 Jun 2025 09:15:10 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42132a3abe6b3ca5bc8e4e623ffa00fe86641a0a42454bba499fa70136dea21`  
		Last Modified: Wed, 11 Jun 2025 09:15:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:2f715ae3a26ddc650f595ca31d33c4a4c14311b1347a6e8d20aca949b131063d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2422126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a4df8b3c359f6d964f37642182e6de7a4cd8cc28676c409e313aa88eaf5b698`

```dockerfile
```

-	Layers:
	-	`sha256:994b93c94dedc6bf0bf79fcfb6b5332c77a3fea69cd945274a1b5eead27d80e0`  
		Last Modified: Wed, 11 Jun 2025 12:34:39 GMT  
		Size: 2.4 MB (2396806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bd4c128777cf5eda46cb5a3ab851f4294546c4b8267f89d17b1adfc4ad5e9bd`  
		Last Modified: Wed, 11 Jun 2025 12:34:40 GMT  
		Size: 25.3 KB (25320 bytes)  
		MIME: application/vnd.in-toto+json
