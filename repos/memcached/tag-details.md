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
-	[`memcached:1.6.25`](#memcached1625)
-	[`memcached:1.6.25-alpine`](#memcached1625-alpine)
-	[`memcached:1.6.25-alpine3.19`](#memcached1625-alpine319)
-	[`memcached:1.6.25-bookworm`](#memcached1625-bookworm)
-	[`memcached:alpine`](#memcachedalpine)
-	[`memcached:alpine3.19`](#memcachedalpine319)
-	[`memcached:bookworm`](#memcachedbookworm)
-	[`memcached:latest`](#memcachedlatest)

## `memcached:1`

```console
$ docker pull memcached@sha256:502113923d3c966943ae15105a43a8f09669f8e3d311b41ecf6d4844917c3eb2
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
$ docker pull memcached@sha256:f5d6b34b5e53f3c3efa1761e78a3ec1e48806b9cf323f275eb73f744ccecb592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38789552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5659585297ecca8269e4b42bf75ee0ba65573bc53f1ac844ce4442a41168219b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:01 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Tue, 12 Mar 2024 01:21:01 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f5b0c7d5ff100485df42c707b8f798c23491e3390670b6102ec309459c56e1`  
		Last Modified: Wed, 20 Mar 2024 21:53:21 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0347f087df5e5a5e55e4e61f495fb25766015d39f1a62d755e903df3f0a4b463`  
		Last Modified: Wed, 20 Mar 2024 21:53:22 GMT  
		Size: 2.5 MB (2488465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e3316b02adf5a1ede79c485a31043189f5e47f3f295394d2c0e8d4cde01c24`  
		Last Modified: Wed, 20 Mar 2024 21:53:21 GMT  
		Size: 7.2 MB (7175392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b72ea418779aaf6ffa3dcf321d061b13df238a88fcdd3f8d4a8e811f3f329f2`  
		Last Modified: Wed, 20 Mar 2024 21:53:21 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534937fe67d0636cc42a8284656ac23b9f0a138b3b912da0122025298ba0187e`  
		Last Modified: Wed, 20 Mar 2024 21:53:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:cdfdc5468a693b11d8b5e2c584c6b8167aca56f16bbef4a5c73f88e254f01849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3536051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c3d70d51d8c20eb5bffd2b9e173bf20449fb79a7c1f5dc4e067211a394bba7`

```dockerfile
```

-	Layers:
	-	`sha256:77f1295784ab211addd97298191a342ea0b5bc2ac83e5349eebc5752f9e00eda`  
		Last Modified: Wed, 20 Mar 2024 21:53:22 GMT  
		Size: 3.5 MB (3514934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:204bffe148afae4b974e13d601af8e712c6135452b18b6283a30fa1ffde6e69b`  
		Last Modified: Wed, 20 Mar 2024 21:53:21 GMT  
		Size: 21.1 KB (21117 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v5

```console
$ docker pull memcached@sha256:2c0a8fd6a587a5d73f6afbc1fe07536b8a21f37ff8533ce389195c3f0ccfd62b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34811756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0041b5946d66d8e8b27a51ff5f1bb8d593ed96c761133d93788591b5ab21d8e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:48:31 GMT
ADD file:b1bd2ec7dd2a8894ea7b5837afba4e15ba798f4809586f0ac1b8855bd0032651 in / 
# Tue, 12 Mar 2024 00:48:31 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:64806d9455193063a6bd4aebf47380e94fad8313f6ad1b5d831882c453f43261`  
		Last Modified: Tue, 12 Mar 2024 00:51:39 GMT  
		Size: 26.9 MB (26884021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e32a50f75b9d40c50ce7692a0631af44e30f327e696aa5b28831455123c0d1`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a78498071cf34c7c6bcb0da9274a1a38c73fbb294d613cfac9c0100e903977`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 2.1 MB (2089476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36068ff9365ced1cbed88c3e977f60059201881a2482f8cf3f5d95de3212f48`  
		Last Modified: Wed, 20 Mar 2024 21:52:39 GMT  
		Size: 5.8 MB (5836746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf53231953d794bde70e2b7b7119a814be7bcedab1a665a0c94985ad91a5934`  
		Last Modified: Wed, 20 Mar 2024 21:52:39 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f512760eb47d5604a6a012660a82a055b5433c332a9ed9dbeff2acdf4e8c831e`  
		Last Modified: Wed, 20 Mar 2024 21:52:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:f924932e4f06ee4421d9aa0c65781bc2d4e66b5b6921cd2701898c5f207cf5b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3506305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cc0ff8d1f5c499d166f30b882b9a756a9c801545de1080d663caeb2bb0f42db`

```dockerfile
```

-	Layers:
	-	`sha256:bfe76f7bb20909be4b9e643fa059225a1d9e992c6e123b3795bceaf5a7acc391`  
		Last Modified: Wed, 20 Mar 2024 21:52:39 GMT  
		Size: 3.5 MB (3485214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59b8882010ed55ddacd7b4a1329987ff2af9a2367d809d764e8e333d83cc9f4a`  
		Last Modified: Wed, 20 Mar 2024 21:52:38 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ccd988c5b8b64dd797254c5db351be97958404a16137214c5569c0ffd0081e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37688087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27728f0ab685b3a67c0f34a20d27afd4f5f137af0204c15e024a08ccb9689493`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac48a97998740def0fa8b1b7e818bbec003d87e56636ed14d66e8ea9c1b49c18`  
		Last Modified: Wed, 20 Mar 2024 22:05:32 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e6aa77c2974c982d56d398f0e7fde37261a6e629e0ae13bd38cbcfbc94d0f2`  
		Last Modified: Wed, 20 Mar 2024 22:05:33 GMT  
		Size: 2.3 MB (2346182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e87543748bdbe302f363c5c5ba30d5d2f7bddba6e8aa1b1492dbf60f97823f`  
		Last Modified: Wed, 20 Mar 2024 22:05:33 GMT  
		Size: 6.2 MB (6183961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fcc56c57aa721ad68c916103760548406b2f2ae78798ee219c5c037804554d3`  
		Last Modified: Wed, 20 Mar 2024 22:05:32 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad54eed22cbb0e5b0a76ceabcf728ab53a51c2d584ed743ca55c3f83749c7fb`  
		Last Modified: Wed, 20 Mar 2024 22:05:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:e311165ff6d518330323d445e95dd591ded261f129a6dfd3b9bba58349db9b26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3507065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3d95ab8f1447c9653180938a8afc4364a3d150c55a19bcc457e994da2deb96`

```dockerfile
```

-	Layers:
	-	`sha256:088471520c083942039c4a09387bdbef3ef68263c757673503b19844809bb1a8`  
		Last Modified: Wed, 20 Mar 2024 22:05:34 GMT  
		Size: 3.5 MB (3486097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daa3f98d4564330b08871a65867b9574becccd48cf8f34418e8e4e5007494a52`  
		Last Modified: Wed, 20 Mar 2024 22:05:32 GMT  
		Size: 21.0 KB (20968 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:f81e3f7f720aaf1482cc81d8bb3f063a146e5ed1fef7ffe54e62f36346a71b3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39272880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18bb6bb8ab561077858738067ab803ed63757a2c5f53e276936c40e1a4527aae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:57:59 GMT
ADD file:88f04d79dc9f1691544c636ff52d6744a2ff68d504793ea8034b797d0bfc6fd3 in / 
# Tue, 12 Mar 2024 00:58:00 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:576af7ffb10b3f3b8d5523e6b91da8667eb39393cdfd50fb26dfc178e504ba70`  
		Last Modified: Tue, 12 Mar 2024 01:02:43 GMT  
		Size: 30.1 MB (30141873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ca1e74787d7f5345fa4e48b3752fab05e59b0cc9269325db87012c10c20201`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c850abea3f675f18aec4a116fba49dae8f46e99f06997b55a6a2eed0636db316`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 2.5 MB (2492637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14fde32a1b90b6896eaf4e91a78b8f32edf62e2bde66ca3bdbf842d607182b63`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 6.6 MB (6636851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1abdc4ae20d60ffc06b6d337d69a65d0501dc932a9a31039f97854efd852c00c`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e56d15c7c18240ea35e93bd1fadf02ad9d12cf1d4168fc6347adda471053737`  
		Last Modified: Wed, 20 Mar 2024 21:53:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:1a82d1205f3b793796a0ce63454ba7a0e8439159d0cddbbdaa20a03103fa3b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3529875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb96cb648ee7c46e17e8193e254b792e2d16ab1dcd2944281ce40379f0ee1ed`

```dockerfile
```

-	Layers:
	-	`sha256:d0b36f1ef0868bd6a59e83aefd9d82a113291e6d8405938446ea789c06aaae64`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 3.5 MB (3508813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56aa96415543efa9a697197eaf5addc87d9d2eeed66dd1fa3b0821a739c733a7`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 21.1 KB (21062 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; mips64le

```console
$ docker pull memcached@sha256:19524094dd845883d46d265bc2c0e83abda00c944e71c65beeb688e1328aee22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37565245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1983e467da37a29b6a5ccc7f7dc4da935cad3d72f262f972d952995365d45623`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 01:06:19 GMT
ADD file:c03c59e261bb08f39e6a97df2fd4b82f1e11b49a62d1859a8f8efac680b80a88 in / 
# Tue, 12 Mar 2024 01:06:23 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aad79459a0f767fcded51c9547150a1cfd96638972389ab8621b5f3eb4a9c280`  
		Last Modified: Tue, 12 Mar 2024 01:17:09 GMT  
		Size: 29.1 MB (29119205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f9ce6b6ef9151bae2476ece2788ab3fcb6d9abf46076b3ab61890a8c5d25e3`  
		Last Modified: Wed, 20 Mar 2024 21:59:53 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4e0a67df5eca0e49eef014debfeb0680de1b95463963c1256e155e92c967a0`  
		Last Modified: Wed, 20 Mar 2024 21:59:54 GMT  
		Size: 1.9 MB (1937678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db0c438efebe0bbb19f79fa801c9c2c52655b590ac16a7196adc5d05702258e`  
		Last Modified: Wed, 20 Mar 2024 21:59:55 GMT  
		Size: 6.5 MB (6506842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97107982137a0d6d10cd7c2f2e613455871a16b69d19c544d26f5c9df4ef2d0`  
		Last Modified: Wed, 20 Mar 2024 21:59:54 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d2108a68b8f51c577db7aa9b41e3bc0507fa18834dc4e235303677021f369f`  
		Last Modified: Wed, 20 Mar 2024 21:59:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:dde4628406ffa6f2e54cdce761e8d050d342a45b4663463a5827ae0420ad7072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.0 KB (21003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ec8712d9cafb05213294e7c991f103858f9ccc5443c2a33560e9fefc5964e32`

```dockerfile
```

-	Layers:
	-	`sha256:ac6b20491333ea6e06cb55be035327040ed503fedd32e789ed3e8082ecaedf94`  
		Last Modified: Wed, 20 Mar 2024 21:59:54 GMT  
		Size: 21.0 KB (21003 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:4c3db32aa1a397cf2a03078efa95429139072b980ab1cfe1d38a3fc03e16b21b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (43006041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ea28ef1fe375457227b59ed4cffadfe2eb8c198795094bf26e6233bd556c8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:9273ef56d086dbc93b46b7e8ae424eb04096fb00c693dd6cda1f48346290d4d5 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c28cd0e276dcdeb4d44f5cc5bb958610750ff902a081b668e3863c2f38eef054`  
		Last Modified: Tue, 12 Mar 2024 00:38:06 GMT  
		Size: 33.1 MB (33119023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62aa36b84dc23bc5eecf52bd0d09534dcc186ab27089192c7aed8210f610e32`  
		Last Modified: Wed, 13 Mar 2024 02:14:26 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec1785cd98038ba62eb16a4aacec38cdbb91c26f98360aafb2ed1017cda3df8`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 2.7 MB (2698364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5105d8a1d382e8083f62216ad1a3ac3ed9e0dab0a2cd5110eb1afa516b084b`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 7.2 MB (7187142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356eaa328e166dd1628acf5a67acf74c032ae2b79667868199736be62871fcc9`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936d8dbc2ebbedc4ae8dc525f7a6ed2c953784d75251955a347e5cb1eab83a22`  
		Last Modified: Wed, 13 Mar 2024 02:14:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:7ba7fc566a7ca1cc4ee19a4562d3c8ff3cbd5c66504843364b286c16a51c673a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3521676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e456fccef08393cbfaa927989c957a984aca49d5b68aff7e43a60bebf063443e`

```dockerfile
```

-	Layers:
	-	`sha256:40dd29e81bcfdcdc7a12cb2843f9bc037c7633d5502e7d49aeab7f1a38b351d1`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 3.5 MB (3500658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1acb5997eff88a90491a6c619d8236c97c1febf8bf3b8fce15b91660a29910df`  
		Last Modified: Wed, 13 Mar 2024 02:14:26 GMT  
		Size: 21.0 KB (21018 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:6ba3af09c6f41f8a8aeb75f0b92546ff342929150d6da315f2c1152c2ac8b89c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35721763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3b0f99b55b9844b9cf7f544669c714d836ca78200a54ea085af430fa58934e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:54:02 GMT
ADD file:80ab985d4871ca6a72156bedfe1038e6b1a89591fc2fd86c4ef778d293223aff in / 
# Tue, 12 Mar 2024 00:54:03 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9cada496cd2b8a88571bf23d513e7fce34888d13321fcf23c6613bffe4c37297`  
		Last Modified: Tue, 12 Mar 2024 01:21:14 GMT  
		Size: 27.5 MB (27488684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c430faffa085700d40355ac1aea08d429376e112bef3b9c00780b1ede56859c2`  
		Last Modified: Wed, 20 Mar 2024 22:17:08 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf1db148a80e9f25b06fe946c697ba8fa83bc46c13515904d4ceceaeb2a4eeb`  
		Last Modified: Wed, 20 Mar 2024 22:17:12 GMT  
		Size: 2.2 MB (2152657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf95ab69cc340a00b9e21b620561903f3f26a245d421506febe9e3c376310098`  
		Last Modified: Wed, 20 Mar 2024 22:17:09 GMT  
		Size: 6.1 MB (6078907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5304ac9e894c6780910c4bd4889d1cc407cb62e54cc4940d8bc7fa74efbb9699`  
		Last Modified: Wed, 20 Mar 2024 22:17:09 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:722d63b783293116e31d9ac81edb640d7218dbb304e2efdc0c1d48aed76e12d2`  
		Last Modified: Wed, 20 Mar 2024 22:17:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:6b3778c79df56c62c44f402a80b924fdb3a5c869694053bff124b8f232640d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bcc8294911dfe44976e400bf92d4e2bee63c8bd56170c94ca2b3c3b05c59135`

```dockerfile
```

-	Layers:
	-	`sha256:e43c6eaae62edc62c95fce6ffd315f1d7c3c249e703a751b4f13b92dba078b59`  
		Last Modified: Wed, 20 Mar 2024 22:17:09 GMT  
		Size: 3.5 MB (3503203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a25398f94b500655282b6629c187cb91a22c84327a970fdcecacda3d14b74649`  
		Last Modified: Wed, 20 Mar 2024 22:17:08 GMT  
		Size: 21.1 KB (21075 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:58dfadef5a410ef30822e05229187fddce1a8da7c1937038b091fb8cb7826ac1
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
$ docker pull memcached@sha256:f6b5f19ba2996847e54c3f8ac723bfcee01dcbf26a743b771eebd949adcd3214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbcb4ff24a50bf9bfef0d77f5f341124655431b10d81d888846724c5482b817e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52bc7dd0547fab52a919b23ad8ed09de96e085903366fa3e77e95ad2fe89f1e`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba631f297238f62439f901dd841f1562f5e460c41dbdc74a6a8e5e6999a18cf`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 104.2 KB (104208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ff2edca2876fc5c62dce1c2b8acbf97b83c796b95f85065e90770a00b21cc5`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 952.1 KB (952140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da3504e92ee2c623b4d2facb6ab6f4a1bc4f1fdcea560b6e9f700f66fd285b2`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71408ec44fa46990bd8afeb115db16e6bf557a3ab9d5e2525082db1f56fbc1ab`  
		Last Modified: Wed, 20 Mar 2024 21:53:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9a6af97b4f188d601386a7ae666c795c7b8ced4a5a80bc0b486f58a12925509b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d835d5590b950bb321312a339b2d238165437c07297b88b798cf96444114337`

```dockerfile
```

-	Layers:
	-	`sha256:3ab2902d9d1e907cc57cd60627dd6c14dc918adc7f486aa089a23cf66f2590f7`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1e7a2c87072e6d2f3f1c8bb3223221aa5aa79c74f7068735808f053d22d34f6`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 19.5 KB (19468 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:89080028f9e15816ca1bad47470cbb7f97f41c7a4d0127a8b78a39e3eaf3f26f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4425175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38f424677a1fe9988b83477de372d7e42da856eab7e901ecffc2712f49dafe6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
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
	-	`sha256:35d4a8618a7d4f81bed85e38e956c13ad0f4dbe365a1d3e4839d8c84a65a7a2e`  
		Last Modified: Wed, 20 Mar 2024 22:08:20 GMT  
		Size: 954.9 KB (954913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8e229d9ad87b49355b05973eae3eec037dabe9d4f26ae02436d266d09eb384`  
		Last Modified: Wed, 20 Mar 2024 22:08:19 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e5d64381b1947651e9afa510f0f1b109147ea08caf9fcdd31872232fa5da2f`  
		Last Modified: Wed, 20 Mar 2024 22:08:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c71eeeaa3b1e21d77b74c472adfe61bcdb9f3ea73b628eac681931a06d6b2f66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f535672624f50a772f4ee3e725c007c633eb779ee9b37c92dc962f4c991c87c`

```dockerfile
```

-	Layers:
	-	`sha256:ef9589529b64b76286139cc56c9358c9e2b0583070c534151222f1761776eee8`  
		Last Modified: Wed, 20 Mar 2024 22:08:19 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b6a01c1332859fd1b1618cc06466869f7737c345d4d193f6728cbf8f25c4c8c`  
		Last Modified: Wed, 20 Mar 2024 22:08:19 GMT  
		Size: 19.3 KB (19320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:7a09990d28075b0ae82ca0fbb381a9682d782f55fcf7927794c1f56d3f5f5592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4300861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc1012fc4f4bdb1275a61cd5fae08ce070ed5dfb60886d0b72e9434ceb746f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7fcdd9df8a6fc84db8522d3ed5fa60931ec83e5741b97bf6b6484e58efd689`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114d973bd16245ab06782260b9892f2d397fb5a001bc2e9e75d7aae40f50f0e7`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 109.3 KB (109323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d971f09b89e4ba53f0f0b60389db42eb23aecc41de6341fbaa80d85968e87b`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 945.8 KB (945803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce30c9db432ce705b03569af9ac255d12c994029ddd23ac85803f8001718016`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f35a47fb81dc09ebc6d8faab40aaa406320d7901e751097edfdb6c70fd5b50`  
		Last Modified: Wed, 20 Mar 2024 21:53:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d83e592adef091fda12c0a2c1d3940a307ebd22dfff5ef4abacf9d9350d7e64d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9372b7c2bc43fdaf94c2fb5b07e31b6dbd0c58d87c5a23a58590088e0e731222`

```dockerfile
```

-	Layers:
	-	`sha256:c1fcdf84d7c55edc2be4a9ca13b91e6fb4a0bb46b7782ccf23066d0e625113d9`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:729594b664d4e18c05f402b9c0e9d9665ebafe54d9fc4b434cfb3d02cbd14fb4`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 19.4 KB (19413 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:542b6c07395477ef8cb25d0ea2ff0d596b1ab7f849518c04e8ca9bb8f990a1da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4468736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9760785d8debed5a647d14058f436d167f4af55a64b0f203426e99da48cb8a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
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
	-	`sha256:d5aa23581942b7bdabf4f033e906fb350a53e488d497193d8d284750885a4cd6`  
		Last Modified: Sat, 16 Mar 2024 10:30:19 GMT  
		Size: 985.3 KB (985333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00d6241d3b173192fb86c75a90e166eda74b11c2dadd7519e8bfd5e5f8d20b5`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2008720f740687d6af827d98e0a17ac17c40265a0733232b3f65891cefd55ba4`  
		Last Modified: Sat, 16 Mar 2024 10:30:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:baf2f10adc34c6657b730c8bcf1d40afa9cbc5277bc79c1e4a35799ba08c4504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f61ca4d4044f9e7f21d7149dd863ef113c78738e2c3e84b2994e68fe5b7adda`

```dockerfile
```

-	Layers:
	-	`sha256:054cdb368dd44a8e73fdf9e940711c8c646cb1d917752910cfd489178cd1bd40`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e0b9862dbe39bc1e2f1598d956acc8877a83d8516baa2fe29261ecd8d5c16ed`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 19.4 KB (19370 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:2bbbf6c60ae563e7fbf0b0d7fff645531ed4706dd6c6b783c35d4ecef1fd70d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4327559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a414e168eff8283c9d16f99e5c31558dec31c6b15ee761de45a40bb6839ee1cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
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
	-	`sha256:61064e5fd6e0cc6334b6eefff4fe163950d84c1de3c42ec9fdf85d92005f3ae9`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 970.1 KB (970135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f1d5965cdbebebdce4669474799f51b9ef3d6f42b376fa617a1b945d4d4325`  
		Last Modified: Sun, 17 Mar 2024 22:11:55 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23608093e2a154f293a6e3287a11ad798936c0146ae7f1943b035db32efa778b`  
		Last Modified: Sun, 17 Mar 2024 22:11:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2dd2215c8ae081cddcbefef029e030b94e041ecd1f2e409d9f704ffdb720d99a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e50e27f5c06d319f5b8cc2b2ba76311d2d120269d1d9d22aa58ae531733001`

```dockerfile
```

-	Layers:
	-	`sha256:91ebf1e0392ad0faffa17054e66a85a7fb1aa0004495345cf4ed19fd5cfa0a6b`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f135346500525ff3a63124190a6511a8a7af0659061127048c4c9f62c219d119`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 19.3 KB (19301 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine3.19`

```console
$ docker pull memcached@sha256:58dfadef5a410ef30822e05229187fddce1a8da7c1937038b091fb8cb7826ac1
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
$ docker pull memcached@sha256:f6b5f19ba2996847e54c3f8ac723bfcee01dcbf26a743b771eebd949adcd3214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbcb4ff24a50bf9bfef0d77f5f341124655431b10d81d888846724c5482b817e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52bc7dd0547fab52a919b23ad8ed09de96e085903366fa3e77e95ad2fe89f1e`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba631f297238f62439f901dd841f1562f5e460c41dbdc74a6a8e5e6999a18cf`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 104.2 KB (104208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ff2edca2876fc5c62dce1c2b8acbf97b83c796b95f85065e90770a00b21cc5`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 952.1 KB (952140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da3504e92ee2c623b4d2facb6ab6f4a1bc4f1fdcea560b6e9f700f66fd285b2`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71408ec44fa46990bd8afeb115db16e6bf557a3ab9d5e2525082db1f56fbc1ab`  
		Last Modified: Wed, 20 Mar 2024 21:53:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:9a6af97b4f188d601386a7ae666c795c7b8ced4a5a80bc0b486f58a12925509b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d835d5590b950bb321312a339b2d238165437c07297b88b798cf96444114337`

```dockerfile
```

-	Layers:
	-	`sha256:3ab2902d9d1e907cc57cd60627dd6c14dc918adc7f486aa089a23cf66f2590f7`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1e7a2c87072e6d2f3f1c8bb3223221aa5aa79c74f7068735808f053d22d34f6`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 19.5 KB (19468 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:89080028f9e15816ca1bad47470cbb7f97f41c7a4d0127a8b78a39e3eaf3f26f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4425175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38f424677a1fe9988b83477de372d7e42da856eab7e901ecffc2712f49dafe6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
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
	-	`sha256:35d4a8618a7d4f81bed85e38e956c13ad0f4dbe365a1d3e4839d8c84a65a7a2e`  
		Last Modified: Wed, 20 Mar 2024 22:08:20 GMT  
		Size: 954.9 KB (954913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8e229d9ad87b49355b05973eae3eec037dabe9d4f26ae02436d266d09eb384`  
		Last Modified: Wed, 20 Mar 2024 22:08:19 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e5d64381b1947651e9afa510f0f1b109147ea08caf9fcdd31872232fa5da2f`  
		Last Modified: Wed, 20 Mar 2024 22:08:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:c71eeeaa3b1e21d77b74c472adfe61bcdb9f3ea73b628eac681931a06d6b2f66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f535672624f50a772f4ee3e725c007c633eb779ee9b37c92dc962f4c991c87c`

```dockerfile
```

-	Layers:
	-	`sha256:ef9589529b64b76286139cc56c9358c9e2b0583070c534151222f1761776eee8`  
		Last Modified: Wed, 20 Mar 2024 22:08:19 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b6a01c1332859fd1b1618cc06466869f7737c345d4d193f6728cbf8f25c4c8c`  
		Last Modified: Wed, 20 Mar 2024 22:08:19 GMT  
		Size: 19.3 KB (19320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.19` - linux; 386

```console
$ docker pull memcached@sha256:7a09990d28075b0ae82ca0fbb381a9682d782f55fcf7927794c1f56d3f5f5592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4300861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc1012fc4f4bdb1275a61cd5fae08ce070ed5dfb60886d0b72e9434ceb746f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7fcdd9df8a6fc84db8522d3ed5fa60931ec83e5741b97bf6b6484e58efd689`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114d973bd16245ab06782260b9892f2d397fb5a001bc2e9e75d7aae40f50f0e7`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 109.3 KB (109323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d971f09b89e4ba53f0f0b60389db42eb23aecc41de6341fbaa80d85968e87b`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 945.8 KB (945803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce30c9db432ce705b03569af9ac255d12c994029ddd23ac85803f8001718016`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f35a47fb81dc09ebc6d8faab40aaa406320d7901e751097edfdb6c70fd5b50`  
		Last Modified: Wed, 20 Mar 2024 21:53:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:d83e592adef091fda12c0a2c1d3940a307ebd22dfff5ef4abacf9d9350d7e64d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9372b7c2bc43fdaf94c2fb5b07e31b6dbd0c58d87c5a23a58590088e0e731222`

```dockerfile
```

-	Layers:
	-	`sha256:c1fcdf84d7c55edc2be4a9ca13b91e6fb4a0bb46b7782ccf23066d0e625113d9`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:729594b664d4e18c05f402b9c0e9d9665ebafe54d9fc4b434cfb3d02cbd14fb4`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 19.4 KB (19413 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.19` - linux; ppc64le

```console
$ docker pull memcached@sha256:542b6c07395477ef8cb25d0ea2ff0d596b1ab7f849518c04e8ca9bb8f990a1da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4468736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9760785d8debed5a647d14058f436d167f4af55a64b0f203426e99da48cb8a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
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
	-	`sha256:d5aa23581942b7bdabf4f033e906fb350a53e488d497193d8d284750885a4cd6`  
		Last Modified: Sat, 16 Mar 2024 10:30:19 GMT  
		Size: 985.3 KB (985333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00d6241d3b173192fb86c75a90e166eda74b11c2dadd7519e8bfd5e5f8d20b5`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2008720f740687d6af827d98e0a17ac17c40265a0733232b3f65891cefd55ba4`  
		Last Modified: Sat, 16 Mar 2024 10:30:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:baf2f10adc34c6657b730c8bcf1d40afa9cbc5277bc79c1e4a35799ba08c4504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f61ca4d4044f9e7f21d7149dd863ef113c78738e2c3e84b2994e68fe5b7adda`

```dockerfile
```

-	Layers:
	-	`sha256:054cdb368dd44a8e73fdf9e940711c8c646cb1d917752910cfd489178cd1bd40`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e0b9862dbe39bc1e2f1598d956acc8877a83d8516baa2fe29261ecd8d5c16ed`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 19.4 KB (19370 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.19` - linux; s390x

```console
$ docker pull memcached@sha256:2bbbf6c60ae563e7fbf0b0d7fff645531ed4706dd6c6b783c35d4ecef1fd70d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4327559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a414e168eff8283c9d16f99e5c31558dec31c6b15ee761de45a40bb6839ee1cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
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
	-	`sha256:61064e5fd6e0cc6334b6eefff4fe163950d84c1de3c42ec9fdf85d92005f3ae9`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 970.1 KB (970135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f1d5965cdbebebdce4669474799f51b9ef3d6f42b376fa617a1b945d4d4325`  
		Last Modified: Sun, 17 Mar 2024 22:11:55 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23608093e2a154f293a6e3287a11ad798936c0146ae7f1943b035db32efa778b`  
		Last Modified: Sun, 17 Mar 2024 22:11:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:2dd2215c8ae081cddcbefef029e030b94e041ecd1f2e409d9f704ffdb720d99a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e50e27f5c06d319f5b8cc2b2ba76311d2d120269d1d9d22aa58ae531733001`

```dockerfile
```

-	Layers:
	-	`sha256:91ebf1e0392ad0faffa17054e66a85a7fb1aa0004495345cf4ed19fd5cfa0a6b`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f135346500525ff3a63124190a6511a8a7af0659061127048c4c9f62c219d119`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 19.3 KB (19301 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-bookworm`

```console
$ docker pull memcached@sha256:502113923d3c966943ae15105a43a8f09669f8e3d311b41ecf6d4844917c3eb2
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
$ docker pull memcached@sha256:f5d6b34b5e53f3c3efa1761e78a3ec1e48806b9cf323f275eb73f744ccecb592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38789552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5659585297ecca8269e4b42bf75ee0ba65573bc53f1ac844ce4442a41168219b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:01 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Tue, 12 Mar 2024 01:21:01 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f5b0c7d5ff100485df42c707b8f798c23491e3390670b6102ec309459c56e1`  
		Last Modified: Wed, 20 Mar 2024 21:53:21 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0347f087df5e5a5e55e4e61f495fb25766015d39f1a62d755e903df3f0a4b463`  
		Last Modified: Wed, 20 Mar 2024 21:53:22 GMT  
		Size: 2.5 MB (2488465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e3316b02adf5a1ede79c485a31043189f5e47f3f295394d2c0e8d4cde01c24`  
		Last Modified: Wed, 20 Mar 2024 21:53:21 GMT  
		Size: 7.2 MB (7175392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b72ea418779aaf6ffa3dcf321d061b13df238a88fcdd3f8d4a8e811f3f329f2`  
		Last Modified: Wed, 20 Mar 2024 21:53:21 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534937fe67d0636cc42a8284656ac23b9f0a138b3b912da0122025298ba0187e`  
		Last Modified: Wed, 20 Mar 2024 21:53:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:cdfdc5468a693b11d8b5e2c584c6b8167aca56f16bbef4a5c73f88e254f01849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3536051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c3d70d51d8c20eb5bffd2b9e173bf20449fb79a7c1f5dc4e067211a394bba7`

```dockerfile
```

-	Layers:
	-	`sha256:77f1295784ab211addd97298191a342ea0b5bc2ac83e5349eebc5752f9e00eda`  
		Last Modified: Wed, 20 Mar 2024 21:53:22 GMT  
		Size: 3.5 MB (3514934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:204bffe148afae4b974e13d601af8e712c6135452b18b6283a30fa1ffde6e69b`  
		Last Modified: Wed, 20 Mar 2024 21:53:21 GMT  
		Size: 21.1 KB (21117 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:2c0a8fd6a587a5d73f6afbc1fe07536b8a21f37ff8533ce389195c3f0ccfd62b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34811756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0041b5946d66d8e8b27a51ff5f1bb8d593ed96c761133d93788591b5ab21d8e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:48:31 GMT
ADD file:b1bd2ec7dd2a8894ea7b5837afba4e15ba798f4809586f0ac1b8855bd0032651 in / 
# Tue, 12 Mar 2024 00:48:31 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:64806d9455193063a6bd4aebf47380e94fad8313f6ad1b5d831882c453f43261`  
		Last Modified: Tue, 12 Mar 2024 00:51:39 GMT  
		Size: 26.9 MB (26884021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e32a50f75b9d40c50ce7692a0631af44e30f327e696aa5b28831455123c0d1`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a78498071cf34c7c6bcb0da9274a1a38c73fbb294d613cfac9c0100e903977`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 2.1 MB (2089476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36068ff9365ced1cbed88c3e977f60059201881a2482f8cf3f5d95de3212f48`  
		Last Modified: Wed, 20 Mar 2024 21:52:39 GMT  
		Size: 5.8 MB (5836746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf53231953d794bde70e2b7b7119a814be7bcedab1a665a0c94985ad91a5934`  
		Last Modified: Wed, 20 Mar 2024 21:52:39 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f512760eb47d5604a6a012660a82a055b5433c332a9ed9dbeff2acdf4e8c831e`  
		Last Modified: Wed, 20 Mar 2024 21:52:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f924932e4f06ee4421d9aa0c65781bc2d4e66b5b6921cd2701898c5f207cf5b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3506305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cc0ff8d1f5c499d166f30b882b9a756a9c801545de1080d663caeb2bb0f42db`

```dockerfile
```

-	Layers:
	-	`sha256:bfe76f7bb20909be4b9e643fa059225a1d9e992c6e123b3795bceaf5a7acc391`  
		Last Modified: Wed, 20 Mar 2024 21:52:39 GMT  
		Size: 3.5 MB (3485214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59b8882010ed55ddacd7b4a1329987ff2af9a2367d809d764e8e333d83cc9f4a`  
		Last Modified: Wed, 20 Mar 2024 21:52:38 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ccd988c5b8b64dd797254c5db351be97958404a16137214c5569c0ffd0081e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37688087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27728f0ab685b3a67c0f34a20d27afd4f5f137af0204c15e024a08ccb9689493`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac48a97998740def0fa8b1b7e818bbec003d87e56636ed14d66e8ea9c1b49c18`  
		Last Modified: Wed, 20 Mar 2024 22:05:32 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e6aa77c2974c982d56d398f0e7fde37261a6e629e0ae13bd38cbcfbc94d0f2`  
		Last Modified: Wed, 20 Mar 2024 22:05:33 GMT  
		Size: 2.3 MB (2346182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e87543748bdbe302f363c5c5ba30d5d2f7bddba6e8aa1b1492dbf60f97823f`  
		Last Modified: Wed, 20 Mar 2024 22:05:33 GMT  
		Size: 6.2 MB (6183961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fcc56c57aa721ad68c916103760548406b2f2ae78798ee219c5c037804554d3`  
		Last Modified: Wed, 20 Mar 2024 22:05:32 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad54eed22cbb0e5b0a76ceabcf728ab53a51c2d584ed743ca55c3f83749c7fb`  
		Last Modified: Wed, 20 Mar 2024 22:05:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:e311165ff6d518330323d445e95dd591ded261f129a6dfd3b9bba58349db9b26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3507065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3d95ab8f1447c9653180938a8afc4364a3d150c55a19bcc457e994da2deb96`

```dockerfile
```

-	Layers:
	-	`sha256:088471520c083942039c4a09387bdbef3ef68263c757673503b19844809bb1a8`  
		Last Modified: Wed, 20 Mar 2024 22:05:34 GMT  
		Size: 3.5 MB (3486097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daa3f98d4564330b08871a65867b9574becccd48cf8f34418e8e4e5007494a52`  
		Last Modified: Wed, 20 Mar 2024 22:05:32 GMT  
		Size: 21.0 KB (20968 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:f81e3f7f720aaf1482cc81d8bb3f063a146e5ed1fef7ffe54e62f36346a71b3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39272880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18bb6bb8ab561077858738067ab803ed63757a2c5f53e276936c40e1a4527aae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:57:59 GMT
ADD file:88f04d79dc9f1691544c636ff52d6744a2ff68d504793ea8034b797d0bfc6fd3 in / 
# Tue, 12 Mar 2024 00:58:00 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:576af7ffb10b3f3b8d5523e6b91da8667eb39393cdfd50fb26dfc178e504ba70`  
		Last Modified: Tue, 12 Mar 2024 01:02:43 GMT  
		Size: 30.1 MB (30141873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ca1e74787d7f5345fa4e48b3752fab05e59b0cc9269325db87012c10c20201`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c850abea3f675f18aec4a116fba49dae8f46e99f06997b55a6a2eed0636db316`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 2.5 MB (2492637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14fde32a1b90b6896eaf4e91a78b8f32edf62e2bde66ca3bdbf842d607182b63`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 6.6 MB (6636851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1abdc4ae20d60ffc06b6d337d69a65d0501dc932a9a31039f97854efd852c00c`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e56d15c7c18240ea35e93bd1fadf02ad9d12cf1d4168fc6347adda471053737`  
		Last Modified: Wed, 20 Mar 2024 21:53:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:1a82d1205f3b793796a0ce63454ba7a0e8439159d0cddbbdaa20a03103fa3b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3529875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb96cb648ee7c46e17e8193e254b792e2d16ab1dcd2944281ce40379f0ee1ed`

```dockerfile
```

-	Layers:
	-	`sha256:d0b36f1ef0868bd6a59e83aefd9d82a113291e6d8405938446ea789c06aaae64`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 3.5 MB (3508813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56aa96415543efa9a697197eaf5addc87d9d2eeed66dd1fa3b0821a739c733a7`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 21.1 KB (21062 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:19524094dd845883d46d265bc2c0e83abda00c944e71c65beeb688e1328aee22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37565245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1983e467da37a29b6a5ccc7f7dc4da935cad3d72f262f972d952995365d45623`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 01:06:19 GMT
ADD file:c03c59e261bb08f39e6a97df2fd4b82f1e11b49a62d1859a8f8efac680b80a88 in / 
# Tue, 12 Mar 2024 01:06:23 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aad79459a0f767fcded51c9547150a1cfd96638972389ab8621b5f3eb4a9c280`  
		Last Modified: Tue, 12 Mar 2024 01:17:09 GMT  
		Size: 29.1 MB (29119205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f9ce6b6ef9151bae2476ece2788ab3fcb6d9abf46076b3ab61890a8c5d25e3`  
		Last Modified: Wed, 20 Mar 2024 21:59:53 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4e0a67df5eca0e49eef014debfeb0680de1b95463963c1256e155e92c967a0`  
		Last Modified: Wed, 20 Mar 2024 21:59:54 GMT  
		Size: 1.9 MB (1937678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db0c438efebe0bbb19f79fa801c9c2c52655b590ac16a7196adc5d05702258e`  
		Last Modified: Wed, 20 Mar 2024 21:59:55 GMT  
		Size: 6.5 MB (6506842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97107982137a0d6d10cd7c2f2e613455871a16b69d19c544d26f5c9df4ef2d0`  
		Last Modified: Wed, 20 Mar 2024 21:59:54 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d2108a68b8f51c577db7aa9b41e3bc0507fa18834dc4e235303677021f369f`  
		Last Modified: Wed, 20 Mar 2024 21:59:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:dde4628406ffa6f2e54cdce761e8d050d342a45b4663463a5827ae0420ad7072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.0 KB (21003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ec8712d9cafb05213294e7c991f103858f9ccc5443c2a33560e9fefc5964e32`

```dockerfile
```

-	Layers:
	-	`sha256:ac6b20491333ea6e06cb55be035327040ed503fedd32e789ed3e8082ecaedf94`  
		Last Modified: Wed, 20 Mar 2024 21:59:54 GMT  
		Size: 21.0 KB (21003 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:4c3db32aa1a397cf2a03078efa95429139072b980ab1cfe1d38a3fc03e16b21b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (43006041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ea28ef1fe375457227b59ed4cffadfe2eb8c198795094bf26e6233bd556c8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:9273ef56d086dbc93b46b7e8ae424eb04096fb00c693dd6cda1f48346290d4d5 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c28cd0e276dcdeb4d44f5cc5bb958610750ff902a081b668e3863c2f38eef054`  
		Last Modified: Tue, 12 Mar 2024 00:38:06 GMT  
		Size: 33.1 MB (33119023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62aa36b84dc23bc5eecf52bd0d09534dcc186ab27089192c7aed8210f610e32`  
		Last Modified: Wed, 13 Mar 2024 02:14:26 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec1785cd98038ba62eb16a4aacec38cdbb91c26f98360aafb2ed1017cda3df8`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 2.7 MB (2698364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5105d8a1d382e8083f62216ad1a3ac3ed9e0dab0a2cd5110eb1afa516b084b`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 7.2 MB (7187142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356eaa328e166dd1628acf5a67acf74c032ae2b79667868199736be62871fcc9`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936d8dbc2ebbedc4ae8dc525f7a6ed2c953784d75251955a347e5cb1eab83a22`  
		Last Modified: Wed, 13 Mar 2024 02:14:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:7ba7fc566a7ca1cc4ee19a4562d3c8ff3cbd5c66504843364b286c16a51c673a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3521676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e456fccef08393cbfaa927989c957a984aca49d5b68aff7e43a60bebf063443e`

```dockerfile
```

-	Layers:
	-	`sha256:40dd29e81bcfdcdc7a12cb2843f9bc037c7633d5502e7d49aeab7f1a38b351d1`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 3.5 MB (3500658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1acb5997eff88a90491a6c619d8236c97c1febf8bf3b8fce15b91660a29910df`  
		Last Modified: Wed, 13 Mar 2024 02:14:26 GMT  
		Size: 21.0 KB (21018 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:6ba3af09c6f41f8a8aeb75f0b92546ff342929150d6da315f2c1152c2ac8b89c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35721763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3b0f99b55b9844b9cf7f544669c714d836ca78200a54ea085af430fa58934e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:54:02 GMT
ADD file:80ab985d4871ca6a72156bedfe1038e6b1a89591fc2fd86c4ef778d293223aff in / 
# Tue, 12 Mar 2024 00:54:03 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9cada496cd2b8a88571bf23d513e7fce34888d13321fcf23c6613bffe4c37297`  
		Last Modified: Tue, 12 Mar 2024 01:21:14 GMT  
		Size: 27.5 MB (27488684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c430faffa085700d40355ac1aea08d429376e112bef3b9c00780b1ede56859c2`  
		Last Modified: Wed, 20 Mar 2024 22:17:08 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf1db148a80e9f25b06fe946c697ba8fa83bc46c13515904d4ceceaeb2a4eeb`  
		Last Modified: Wed, 20 Mar 2024 22:17:12 GMT  
		Size: 2.2 MB (2152657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf95ab69cc340a00b9e21b620561903f3f26a245d421506febe9e3c376310098`  
		Last Modified: Wed, 20 Mar 2024 22:17:09 GMT  
		Size: 6.1 MB (6078907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5304ac9e894c6780910c4bd4889d1cc407cb62e54cc4940d8bc7fa74efbb9699`  
		Last Modified: Wed, 20 Mar 2024 22:17:09 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:722d63b783293116e31d9ac81edb640d7218dbb304e2efdc0c1d48aed76e12d2`  
		Last Modified: Wed, 20 Mar 2024 22:17:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:6b3778c79df56c62c44f402a80b924fdb3a5c869694053bff124b8f232640d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bcc8294911dfe44976e400bf92d4e2bee63c8bd56170c94ca2b3c3b05c59135`

```dockerfile
```

-	Layers:
	-	`sha256:e43c6eaae62edc62c95fce6ffd315f1d7c3c249e703a751b4f13b92dba078b59`  
		Last Modified: Wed, 20 Mar 2024 22:17:09 GMT  
		Size: 3.5 MB (3503203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a25398f94b500655282b6629c187cb91a22c84327a970fdcecacda3d14b74649`  
		Last Modified: Wed, 20 Mar 2024 22:17:08 GMT  
		Size: 21.1 KB (21075 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6`

```console
$ docker pull memcached@sha256:502113923d3c966943ae15105a43a8f09669f8e3d311b41ecf6d4844917c3eb2
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
$ docker pull memcached@sha256:f5d6b34b5e53f3c3efa1761e78a3ec1e48806b9cf323f275eb73f744ccecb592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38789552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5659585297ecca8269e4b42bf75ee0ba65573bc53f1ac844ce4442a41168219b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:01 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Tue, 12 Mar 2024 01:21:01 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f5b0c7d5ff100485df42c707b8f798c23491e3390670b6102ec309459c56e1`  
		Last Modified: Wed, 20 Mar 2024 21:53:21 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0347f087df5e5a5e55e4e61f495fb25766015d39f1a62d755e903df3f0a4b463`  
		Last Modified: Wed, 20 Mar 2024 21:53:22 GMT  
		Size: 2.5 MB (2488465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e3316b02adf5a1ede79c485a31043189f5e47f3f295394d2c0e8d4cde01c24`  
		Last Modified: Wed, 20 Mar 2024 21:53:21 GMT  
		Size: 7.2 MB (7175392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b72ea418779aaf6ffa3dcf321d061b13df238a88fcdd3f8d4a8e811f3f329f2`  
		Last Modified: Wed, 20 Mar 2024 21:53:21 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534937fe67d0636cc42a8284656ac23b9f0a138b3b912da0122025298ba0187e`  
		Last Modified: Wed, 20 Mar 2024 21:53:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:cdfdc5468a693b11d8b5e2c584c6b8167aca56f16bbef4a5c73f88e254f01849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3536051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c3d70d51d8c20eb5bffd2b9e173bf20449fb79a7c1f5dc4e067211a394bba7`

```dockerfile
```

-	Layers:
	-	`sha256:77f1295784ab211addd97298191a342ea0b5bc2ac83e5349eebc5752f9e00eda`  
		Last Modified: Wed, 20 Mar 2024 21:53:22 GMT  
		Size: 3.5 MB (3514934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:204bffe148afae4b974e13d601af8e712c6135452b18b6283a30fa1ffde6e69b`  
		Last Modified: Wed, 20 Mar 2024 21:53:21 GMT  
		Size: 21.1 KB (21117 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:2c0a8fd6a587a5d73f6afbc1fe07536b8a21f37ff8533ce389195c3f0ccfd62b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34811756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0041b5946d66d8e8b27a51ff5f1bb8d593ed96c761133d93788591b5ab21d8e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:48:31 GMT
ADD file:b1bd2ec7dd2a8894ea7b5837afba4e15ba798f4809586f0ac1b8855bd0032651 in / 
# Tue, 12 Mar 2024 00:48:31 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:64806d9455193063a6bd4aebf47380e94fad8313f6ad1b5d831882c453f43261`  
		Last Modified: Tue, 12 Mar 2024 00:51:39 GMT  
		Size: 26.9 MB (26884021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e32a50f75b9d40c50ce7692a0631af44e30f327e696aa5b28831455123c0d1`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a78498071cf34c7c6bcb0da9274a1a38c73fbb294d613cfac9c0100e903977`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 2.1 MB (2089476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36068ff9365ced1cbed88c3e977f60059201881a2482f8cf3f5d95de3212f48`  
		Last Modified: Wed, 20 Mar 2024 21:52:39 GMT  
		Size: 5.8 MB (5836746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf53231953d794bde70e2b7b7119a814be7bcedab1a665a0c94985ad91a5934`  
		Last Modified: Wed, 20 Mar 2024 21:52:39 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f512760eb47d5604a6a012660a82a055b5433c332a9ed9dbeff2acdf4e8c831e`  
		Last Modified: Wed, 20 Mar 2024 21:52:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:f924932e4f06ee4421d9aa0c65781bc2d4e66b5b6921cd2701898c5f207cf5b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3506305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cc0ff8d1f5c499d166f30b882b9a756a9c801545de1080d663caeb2bb0f42db`

```dockerfile
```

-	Layers:
	-	`sha256:bfe76f7bb20909be4b9e643fa059225a1d9e992c6e123b3795bceaf5a7acc391`  
		Last Modified: Wed, 20 Mar 2024 21:52:39 GMT  
		Size: 3.5 MB (3485214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59b8882010ed55ddacd7b4a1329987ff2af9a2367d809d764e8e333d83cc9f4a`  
		Last Modified: Wed, 20 Mar 2024 21:52:38 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ccd988c5b8b64dd797254c5db351be97958404a16137214c5569c0ffd0081e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37688087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27728f0ab685b3a67c0f34a20d27afd4f5f137af0204c15e024a08ccb9689493`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac48a97998740def0fa8b1b7e818bbec003d87e56636ed14d66e8ea9c1b49c18`  
		Last Modified: Wed, 20 Mar 2024 22:05:32 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e6aa77c2974c982d56d398f0e7fde37261a6e629e0ae13bd38cbcfbc94d0f2`  
		Last Modified: Wed, 20 Mar 2024 22:05:33 GMT  
		Size: 2.3 MB (2346182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e87543748bdbe302f363c5c5ba30d5d2f7bddba6e8aa1b1492dbf60f97823f`  
		Last Modified: Wed, 20 Mar 2024 22:05:33 GMT  
		Size: 6.2 MB (6183961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fcc56c57aa721ad68c916103760548406b2f2ae78798ee219c5c037804554d3`  
		Last Modified: Wed, 20 Mar 2024 22:05:32 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad54eed22cbb0e5b0a76ceabcf728ab53a51c2d584ed743ca55c3f83749c7fb`  
		Last Modified: Wed, 20 Mar 2024 22:05:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:e311165ff6d518330323d445e95dd591ded261f129a6dfd3b9bba58349db9b26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3507065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3d95ab8f1447c9653180938a8afc4364a3d150c55a19bcc457e994da2deb96`

```dockerfile
```

-	Layers:
	-	`sha256:088471520c083942039c4a09387bdbef3ef68263c757673503b19844809bb1a8`  
		Last Modified: Wed, 20 Mar 2024 22:05:34 GMT  
		Size: 3.5 MB (3486097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daa3f98d4564330b08871a65867b9574becccd48cf8f34418e8e4e5007494a52`  
		Last Modified: Wed, 20 Mar 2024 22:05:32 GMT  
		Size: 21.0 KB (20968 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; 386

```console
$ docker pull memcached@sha256:f81e3f7f720aaf1482cc81d8bb3f063a146e5ed1fef7ffe54e62f36346a71b3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39272880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18bb6bb8ab561077858738067ab803ed63757a2c5f53e276936c40e1a4527aae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:57:59 GMT
ADD file:88f04d79dc9f1691544c636ff52d6744a2ff68d504793ea8034b797d0bfc6fd3 in / 
# Tue, 12 Mar 2024 00:58:00 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:576af7ffb10b3f3b8d5523e6b91da8667eb39393cdfd50fb26dfc178e504ba70`  
		Last Modified: Tue, 12 Mar 2024 01:02:43 GMT  
		Size: 30.1 MB (30141873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ca1e74787d7f5345fa4e48b3752fab05e59b0cc9269325db87012c10c20201`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c850abea3f675f18aec4a116fba49dae8f46e99f06997b55a6a2eed0636db316`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 2.5 MB (2492637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14fde32a1b90b6896eaf4e91a78b8f32edf62e2bde66ca3bdbf842d607182b63`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 6.6 MB (6636851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1abdc4ae20d60ffc06b6d337d69a65d0501dc932a9a31039f97854efd852c00c`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e56d15c7c18240ea35e93bd1fadf02ad9d12cf1d4168fc6347adda471053737`  
		Last Modified: Wed, 20 Mar 2024 21:53:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:1a82d1205f3b793796a0ce63454ba7a0e8439159d0cddbbdaa20a03103fa3b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3529875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb96cb648ee7c46e17e8193e254b792e2d16ab1dcd2944281ce40379f0ee1ed`

```dockerfile
```

-	Layers:
	-	`sha256:d0b36f1ef0868bd6a59e83aefd9d82a113291e6d8405938446ea789c06aaae64`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 3.5 MB (3508813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56aa96415543efa9a697197eaf5addc87d9d2eeed66dd1fa3b0821a739c733a7`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 21.1 KB (21062 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; mips64le

```console
$ docker pull memcached@sha256:19524094dd845883d46d265bc2c0e83abda00c944e71c65beeb688e1328aee22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37565245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1983e467da37a29b6a5ccc7f7dc4da935cad3d72f262f972d952995365d45623`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 01:06:19 GMT
ADD file:c03c59e261bb08f39e6a97df2fd4b82f1e11b49a62d1859a8f8efac680b80a88 in / 
# Tue, 12 Mar 2024 01:06:23 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aad79459a0f767fcded51c9547150a1cfd96638972389ab8621b5f3eb4a9c280`  
		Last Modified: Tue, 12 Mar 2024 01:17:09 GMT  
		Size: 29.1 MB (29119205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f9ce6b6ef9151bae2476ece2788ab3fcb6d9abf46076b3ab61890a8c5d25e3`  
		Last Modified: Wed, 20 Mar 2024 21:59:53 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4e0a67df5eca0e49eef014debfeb0680de1b95463963c1256e155e92c967a0`  
		Last Modified: Wed, 20 Mar 2024 21:59:54 GMT  
		Size: 1.9 MB (1937678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db0c438efebe0bbb19f79fa801c9c2c52655b590ac16a7196adc5d05702258e`  
		Last Modified: Wed, 20 Mar 2024 21:59:55 GMT  
		Size: 6.5 MB (6506842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97107982137a0d6d10cd7c2f2e613455871a16b69d19c544d26f5c9df4ef2d0`  
		Last Modified: Wed, 20 Mar 2024 21:59:54 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d2108a68b8f51c577db7aa9b41e3bc0507fa18834dc4e235303677021f369f`  
		Last Modified: Wed, 20 Mar 2024 21:59:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:dde4628406ffa6f2e54cdce761e8d050d342a45b4663463a5827ae0420ad7072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.0 KB (21003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ec8712d9cafb05213294e7c991f103858f9ccc5443c2a33560e9fefc5964e32`

```dockerfile
```

-	Layers:
	-	`sha256:ac6b20491333ea6e06cb55be035327040ed503fedd32e789ed3e8082ecaedf94`  
		Last Modified: Wed, 20 Mar 2024 21:59:54 GMT  
		Size: 21.0 KB (21003 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:4c3db32aa1a397cf2a03078efa95429139072b980ab1cfe1d38a3fc03e16b21b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (43006041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ea28ef1fe375457227b59ed4cffadfe2eb8c198795094bf26e6233bd556c8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:9273ef56d086dbc93b46b7e8ae424eb04096fb00c693dd6cda1f48346290d4d5 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c28cd0e276dcdeb4d44f5cc5bb958610750ff902a081b668e3863c2f38eef054`  
		Last Modified: Tue, 12 Mar 2024 00:38:06 GMT  
		Size: 33.1 MB (33119023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62aa36b84dc23bc5eecf52bd0d09534dcc186ab27089192c7aed8210f610e32`  
		Last Modified: Wed, 13 Mar 2024 02:14:26 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec1785cd98038ba62eb16a4aacec38cdbb91c26f98360aafb2ed1017cda3df8`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 2.7 MB (2698364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5105d8a1d382e8083f62216ad1a3ac3ed9e0dab0a2cd5110eb1afa516b084b`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 7.2 MB (7187142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356eaa328e166dd1628acf5a67acf74c032ae2b79667868199736be62871fcc9`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936d8dbc2ebbedc4ae8dc525f7a6ed2c953784d75251955a347e5cb1eab83a22`  
		Last Modified: Wed, 13 Mar 2024 02:14:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:7ba7fc566a7ca1cc4ee19a4562d3c8ff3cbd5c66504843364b286c16a51c673a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3521676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e456fccef08393cbfaa927989c957a984aca49d5b68aff7e43a60bebf063443e`

```dockerfile
```

-	Layers:
	-	`sha256:40dd29e81bcfdcdc7a12cb2843f9bc037c7633d5502e7d49aeab7f1a38b351d1`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 3.5 MB (3500658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1acb5997eff88a90491a6c619d8236c97c1febf8bf3b8fce15b91660a29910df`  
		Last Modified: Wed, 13 Mar 2024 02:14:26 GMT  
		Size: 21.0 KB (21018 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; s390x

```console
$ docker pull memcached@sha256:6ba3af09c6f41f8a8aeb75f0b92546ff342929150d6da315f2c1152c2ac8b89c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35721763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3b0f99b55b9844b9cf7f544669c714d836ca78200a54ea085af430fa58934e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:54:02 GMT
ADD file:80ab985d4871ca6a72156bedfe1038e6b1a89591fc2fd86c4ef778d293223aff in / 
# Tue, 12 Mar 2024 00:54:03 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9cada496cd2b8a88571bf23d513e7fce34888d13321fcf23c6613bffe4c37297`  
		Last Modified: Tue, 12 Mar 2024 01:21:14 GMT  
		Size: 27.5 MB (27488684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c430faffa085700d40355ac1aea08d429376e112bef3b9c00780b1ede56859c2`  
		Last Modified: Wed, 20 Mar 2024 22:17:08 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf1db148a80e9f25b06fe946c697ba8fa83bc46c13515904d4ceceaeb2a4eeb`  
		Last Modified: Wed, 20 Mar 2024 22:17:12 GMT  
		Size: 2.2 MB (2152657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf95ab69cc340a00b9e21b620561903f3f26a245d421506febe9e3c376310098`  
		Last Modified: Wed, 20 Mar 2024 22:17:09 GMT  
		Size: 6.1 MB (6078907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5304ac9e894c6780910c4bd4889d1cc407cb62e54cc4940d8bc7fa74efbb9699`  
		Last Modified: Wed, 20 Mar 2024 22:17:09 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:722d63b783293116e31d9ac81edb640d7218dbb304e2efdc0c1d48aed76e12d2`  
		Last Modified: Wed, 20 Mar 2024 22:17:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:6b3778c79df56c62c44f402a80b924fdb3a5c869694053bff124b8f232640d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bcc8294911dfe44976e400bf92d4e2bee63c8bd56170c94ca2b3c3b05c59135`

```dockerfile
```

-	Layers:
	-	`sha256:e43c6eaae62edc62c95fce6ffd315f1d7c3c249e703a751b4f13b92dba078b59`  
		Last Modified: Wed, 20 Mar 2024 22:17:09 GMT  
		Size: 3.5 MB (3503203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a25398f94b500655282b6629c187cb91a22c84327a970fdcecacda3d14b74649`  
		Last Modified: Wed, 20 Mar 2024 22:17:08 GMT  
		Size: 21.1 KB (21075 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine`

```console
$ docker pull memcached@sha256:58dfadef5a410ef30822e05229187fddce1a8da7c1937038b091fb8cb7826ac1
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
$ docker pull memcached@sha256:f6b5f19ba2996847e54c3f8ac723bfcee01dcbf26a743b771eebd949adcd3214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbcb4ff24a50bf9bfef0d77f5f341124655431b10d81d888846724c5482b817e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52bc7dd0547fab52a919b23ad8ed09de96e085903366fa3e77e95ad2fe89f1e`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba631f297238f62439f901dd841f1562f5e460c41dbdc74a6a8e5e6999a18cf`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 104.2 KB (104208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ff2edca2876fc5c62dce1c2b8acbf97b83c796b95f85065e90770a00b21cc5`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 952.1 KB (952140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da3504e92ee2c623b4d2facb6ab6f4a1bc4f1fdcea560b6e9f700f66fd285b2`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71408ec44fa46990bd8afeb115db16e6bf557a3ab9d5e2525082db1f56fbc1ab`  
		Last Modified: Wed, 20 Mar 2024 21:53:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9a6af97b4f188d601386a7ae666c795c7b8ced4a5a80bc0b486f58a12925509b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d835d5590b950bb321312a339b2d238165437c07297b88b798cf96444114337`

```dockerfile
```

-	Layers:
	-	`sha256:3ab2902d9d1e907cc57cd60627dd6c14dc918adc7f486aa089a23cf66f2590f7`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1e7a2c87072e6d2f3f1c8bb3223221aa5aa79c74f7068735808f053d22d34f6`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 19.5 KB (19468 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:89080028f9e15816ca1bad47470cbb7f97f41c7a4d0127a8b78a39e3eaf3f26f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4425175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38f424677a1fe9988b83477de372d7e42da856eab7e901ecffc2712f49dafe6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
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
	-	`sha256:35d4a8618a7d4f81bed85e38e956c13ad0f4dbe365a1d3e4839d8c84a65a7a2e`  
		Last Modified: Wed, 20 Mar 2024 22:08:20 GMT  
		Size: 954.9 KB (954913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8e229d9ad87b49355b05973eae3eec037dabe9d4f26ae02436d266d09eb384`  
		Last Modified: Wed, 20 Mar 2024 22:08:19 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e5d64381b1947651e9afa510f0f1b109147ea08caf9fcdd31872232fa5da2f`  
		Last Modified: Wed, 20 Mar 2024 22:08:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c71eeeaa3b1e21d77b74c472adfe61bcdb9f3ea73b628eac681931a06d6b2f66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f535672624f50a772f4ee3e725c007c633eb779ee9b37c92dc962f4c991c87c`

```dockerfile
```

-	Layers:
	-	`sha256:ef9589529b64b76286139cc56c9358c9e2b0583070c534151222f1761776eee8`  
		Last Modified: Wed, 20 Mar 2024 22:08:19 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b6a01c1332859fd1b1618cc06466869f7737c345d4d193f6728cbf8f25c4c8c`  
		Last Modified: Wed, 20 Mar 2024 22:08:19 GMT  
		Size: 19.3 KB (19320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:7a09990d28075b0ae82ca0fbb381a9682d782f55fcf7927794c1f56d3f5f5592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4300861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc1012fc4f4bdb1275a61cd5fae08ce070ed5dfb60886d0b72e9434ceb746f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7fcdd9df8a6fc84db8522d3ed5fa60931ec83e5741b97bf6b6484e58efd689`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114d973bd16245ab06782260b9892f2d397fb5a001bc2e9e75d7aae40f50f0e7`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 109.3 KB (109323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d971f09b89e4ba53f0f0b60389db42eb23aecc41de6341fbaa80d85968e87b`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 945.8 KB (945803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce30c9db432ce705b03569af9ac255d12c994029ddd23ac85803f8001718016`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f35a47fb81dc09ebc6d8faab40aaa406320d7901e751097edfdb6c70fd5b50`  
		Last Modified: Wed, 20 Mar 2024 21:53:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d83e592adef091fda12c0a2c1d3940a307ebd22dfff5ef4abacf9d9350d7e64d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9372b7c2bc43fdaf94c2fb5b07e31b6dbd0c58d87c5a23a58590088e0e731222`

```dockerfile
```

-	Layers:
	-	`sha256:c1fcdf84d7c55edc2be4a9ca13b91e6fb4a0bb46b7782ccf23066d0e625113d9`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:729594b664d4e18c05f402b9c0e9d9665ebafe54d9fc4b434cfb3d02cbd14fb4`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 19.4 KB (19413 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:542b6c07395477ef8cb25d0ea2ff0d596b1ab7f849518c04e8ca9bb8f990a1da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4468736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9760785d8debed5a647d14058f436d167f4af55a64b0f203426e99da48cb8a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
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
	-	`sha256:d5aa23581942b7bdabf4f033e906fb350a53e488d497193d8d284750885a4cd6`  
		Last Modified: Sat, 16 Mar 2024 10:30:19 GMT  
		Size: 985.3 KB (985333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00d6241d3b173192fb86c75a90e166eda74b11c2dadd7519e8bfd5e5f8d20b5`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2008720f740687d6af827d98e0a17ac17c40265a0733232b3f65891cefd55ba4`  
		Last Modified: Sat, 16 Mar 2024 10:30:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:baf2f10adc34c6657b730c8bcf1d40afa9cbc5277bc79c1e4a35799ba08c4504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f61ca4d4044f9e7f21d7149dd863ef113c78738e2c3e84b2994e68fe5b7adda`

```dockerfile
```

-	Layers:
	-	`sha256:054cdb368dd44a8e73fdf9e940711c8c646cb1d917752910cfd489178cd1bd40`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e0b9862dbe39bc1e2f1598d956acc8877a83d8516baa2fe29261ecd8d5c16ed`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 19.4 KB (19370 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:2bbbf6c60ae563e7fbf0b0d7fff645531ed4706dd6c6b783c35d4ecef1fd70d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4327559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a414e168eff8283c9d16f99e5c31558dec31c6b15ee761de45a40bb6839ee1cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
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
	-	`sha256:61064e5fd6e0cc6334b6eefff4fe163950d84c1de3c42ec9fdf85d92005f3ae9`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 970.1 KB (970135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f1d5965cdbebebdce4669474799f51b9ef3d6f42b376fa617a1b945d4d4325`  
		Last Modified: Sun, 17 Mar 2024 22:11:55 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23608093e2a154f293a6e3287a11ad798936c0146ae7f1943b035db32efa778b`  
		Last Modified: Sun, 17 Mar 2024 22:11:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2dd2215c8ae081cddcbefef029e030b94e041ecd1f2e409d9f704ffdb720d99a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e50e27f5c06d319f5b8cc2b2ba76311d2d120269d1d9d22aa58ae531733001`

```dockerfile
```

-	Layers:
	-	`sha256:91ebf1e0392ad0faffa17054e66a85a7fb1aa0004495345cf4ed19fd5cfa0a6b`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f135346500525ff3a63124190a6511a8a7af0659061127048c4c9f62c219d119`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 19.3 KB (19301 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine3.19`

```console
$ docker pull memcached@sha256:58dfadef5a410ef30822e05229187fddce1a8da7c1937038b091fb8cb7826ac1
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
$ docker pull memcached@sha256:f6b5f19ba2996847e54c3f8ac723bfcee01dcbf26a743b771eebd949adcd3214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbcb4ff24a50bf9bfef0d77f5f341124655431b10d81d888846724c5482b817e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52bc7dd0547fab52a919b23ad8ed09de96e085903366fa3e77e95ad2fe89f1e`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba631f297238f62439f901dd841f1562f5e460c41dbdc74a6a8e5e6999a18cf`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 104.2 KB (104208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ff2edca2876fc5c62dce1c2b8acbf97b83c796b95f85065e90770a00b21cc5`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 952.1 KB (952140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da3504e92ee2c623b4d2facb6ab6f4a1bc4f1fdcea560b6e9f700f66fd285b2`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71408ec44fa46990bd8afeb115db16e6bf557a3ab9d5e2525082db1f56fbc1ab`  
		Last Modified: Wed, 20 Mar 2024 21:53:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:9a6af97b4f188d601386a7ae666c795c7b8ced4a5a80bc0b486f58a12925509b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d835d5590b950bb321312a339b2d238165437c07297b88b798cf96444114337`

```dockerfile
```

-	Layers:
	-	`sha256:3ab2902d9d1e907cc57cd60627dd6c14dc918adc7f486aa089a23cf66f2590f7`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1e7a2c87072e6d2f3f1c8bb3223221aa5aa79c74f7068735808f053d22d34f6`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 19.5 KB (19468 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:89080028f9e15816ca1bad47470cbb7f97f41c7a4d0127a8b78a39e3eaf3f26f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4425175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38f424677a1fe9988b83477de372d7e42da856eab7e901ecffc2712f49dafe6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
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
	-	`sha256:35d4a8618a7d4f81bed85e38e956c13ad0f4dbe365a1d3e4839d8c84a65a7a2e`  
		Last Modified: Wed, 20 Mar 2024 22:08:20 GMT  
		Size: 954.9 KB (954913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8e229d9ad87b49355b05973eae3eec037dabe9d4f26ae02436d266d09eb384`  
		Last Modified: Wed, 20 Mar 2024 22:08:19 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e5d64381b1947651e9afa510f0f1b109147ea08caf9fcdd31872232fa5da2f`  
		Last Modified: Wed, 20 Mar 2024 22:08:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:c71eeeaa3b1e21d77b74c472adfe61bcdb9f3ea73b628eac681931a06d6b2f66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f535672624f50a772f4ee3e725c007c633eb779ee9b37c92dc962f4c991c87c`

```dockerfile
```

-	Layers:
	-	`sha256:ef9589529b64b76286139cc56c9358c9e2b0583070c534151222f1761776eee8`  
		Last Modified: Wed, 20 Mar 2024 22:08:19 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b6a01c1332859fd1b1618cc06466869f7737c345d4d193f6728cbf8f25c4c8c`  
		Last Modified: Wed, 20 Mar 2024 22:08:19 GMT  
		Size: 19.3 KB (19320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.19` - linux; 386

```console
$ docker pull memcached@sha256:7a09990d28075b0ae82ca0fbb381a9682d782f55fcf7927794c1f56d3f5f5592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4300861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc1012fc4f4bdb1275a61cd5fae08ce070ed5dfb60886d0b72e9434ceb746f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7fcdd9df8a6fc84db8522d3ed5fa60931ec83e5741b97bf6b6484e58efd689`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114d973bd16245ab06782260b9892f2d397fb5a001bc2e9e75d7aae40f50f0e7`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 109.3 KB (109323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d971f09b89e4ba53f0f0b60389db42eb23aecc41de6341fbaa80d85968e87b`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 945.8 KB (945803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce30c9db432ce705b03569af9ac255d12c994029ddd23ac85803f8001718016`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f35a47fb81dc09ebc6d8faab40aaa406320d7901e751097edfdb6c70fd5b50`  
		Last Modified: Wed, 20 Mar 2024 21:53:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:d83e592adef091fda12c0a2c1d3940a307ebd22dfff5ef4abacf9d9350d7e64d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9372b7c2bc43fdaf94c2fb5b07e31b6dbd0c58d87c5a23a58590088e0e731222`

```dockerfile
```

-	Layers:
	-	`sha256:c1fcdf84d7c55edc2be4a9ca13b91e6fb4a0bb46b7782ccf23066d0e625113d9`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:729594b664d4e18c05f402b9c0e9d9665ebafe54d9fc4b434cfb3d02cbd14fb4`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 19.4 KB (19413 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.19` - linux; ppc64le

```console
$ docker pull memcached@sha256:542b6c07395477ef8cb25d0ea2ff0d596b1ab7f849518c04e8ca9bb8f990a1da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4468736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9760785d8debed5a647d14058f436d167f4af55a64b0f203426e99da48cb8a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
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
	-	`sha256:d5aa23581942b7bdabf4f033e906fb350a53e488d497193d8d284750885a4cd6`  
		Last Modified: Sat, 16 Mar 2024 10:30:19 GMT  
		Size: 985.3 KB (985333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00d6241d3b173192fb86c75a90e166eda74b11c2dadd7519e8bfd5e5f8d20b5`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2008720f740687d6af827d98e0a17ac17c40265a0733232b3f65891cefd55ba4`  
		Last Modified: Sat, 16 Mar 2024 10:30:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:baf2f10adc34c6657b730c8bcf1d40afa9cbc5277bc79c1e4a35799ba08c4504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f61ca4d4044f9e7f21d7149dd863ef113c78738e2c3e84b2994e68fe5b7adda`

```dockerfile
```

-	Layers:
	-	`sha256:054cdb368dd44a8e73fdf9e940711c8c646cb1d917752910cfd489178cd1bd40`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e0b9862dbe39bc1e2f1598d956acc8877a83d8516baa2fe29261ecd8d5c16ed`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 19.4 KB (19370 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.19` - linux; s390x

```console
$ docker pull memcached@sha256:2bbbf6c60ae563e7fbf0b0d7fff645531ed4706dd6c6b783c35d4ecef1fd70d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4327559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a414e168eff8283c9d16f99e5c31558dec31c6b15ee761de45a40bb6839ee1cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
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
	-	`sha256:61064e5fd6e0cc6334b6eefff4fe163950d84c1de3c42ec9fdf85d92005f3ae9`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 970.1 KB (970135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f1d5965cdbebebdce4669474799f51b9ef3d6f42b376fa617a1b945d4d4325`  
		Last Modified: Sun, 17 Mar 2024 22:11:55 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23608093e2a154f293a6e3287a11ad798936c0146ae7f1943b035db32efa778b`  
		Last Modified: Sun, 17 Mar 2024 22:11:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:2dd2215c8ae081cddcbefef029e030b94e041ecd1f2e409d9f704ffdb720d99a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e50e27f5c06d319f5b8cc2b2ba76311d2d120269d1d9d22aa58ae531733001`

```dockerfile
```

-	Layers:
	-	`sha256:91ebf1e0392ad0faffa17054e66a85a7fb1aa0004495345cf4ed19fd5cfa0a6b`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f135346500525ff3a63124190a6511a8a7af0659061127048c4c9f62c219d119`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 19.3 KB (19301 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-bookworm`

```console
$ docker pull memcached@sha256:502113923d3c966943ae15105a43a8f09669f8e3d311b41ecf6d4844917c3eb2
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
$ docker pull memcached@sha256:f5d6b34b5e53f3c3efa1761e78a3ec1e48806b9cf323f275eb73f744ccecb592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38789552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5659585297ecca8269e4b42bf75ee0ba65573bc53f1ac844ce4442a41168219b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:01 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Tue, 12 Mar 2024 01:21:01 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f5b0c7d5ff100485df42c707b8f798c23491e3390670b6102ec309459c56e1`  
		Last Modified: Wed, 20 Mar 2024 21:53:21 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0347f087df5e5a5e55e4e61f495fb25766015d39f1a62d755e903df3f0a4b463`  
		Last Modified: Wed, 20 Mar 2024 21:53:22 GMT  
		Size: 2.5 MB (2488465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e3316b02adf5a1ede79c485a31043189f5e47f3f295394d2c0e8d4cde01c24`  
		Last Modified: Wed, 20 Mar 2024 21:53:21 GMT  
		Size: 7.2 MB (7175392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b72ea418779aaf6ffa3dcf321d061b13df238a88fcdd3f8d4a8e811f3f329f2`  
		Last Modified: Wed, 20 Mar 2024 21:53:21 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534937fe67d0636cc42a8284656ac23b9f0a138b3b912da0122025298ba0187e`  
		Last Modified: Wed, 20 Mar 2024 21:53:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:cdfdc5468a693b11d8b5e2c584c6b8167aca56f16bbef4a5c73f88e254f01849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3536051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c3d70d51d8c20eb5bffd2b9e173bf20449fb79a7c1f5dc4e067211a394bba7`

```dockerfile
```

-	Layers:
	-	`sha256:77f1295784ab211addd97298191a342ea0b5bc2ac83e5349eebc5752f9e00eda`  
		Last Modified: Wed, 20 Mar 2024 21:53:22 GMT  
		Size: 3.5 MB (3514934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:204bffe148afae4b974e13d601af8e712c6135452b18b6283a30fa1ffde6e69b`  
		Last Modified: Wed, 20 Mar 2024 21:53:21 GMT  
		Size: 21.1 KB (21117 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:2c0a8fd6a587a5d73f6afbc1fe07536b8a21f37ff8533ce389195c3f0ccfd62b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34811756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0041b5946d66d8e8b27a51ff5f1bb8d593ed96c761133d93788591b5ab21d8e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:48:31 GMT
ADD file:b1bd2ec7dd2a8894ea7b5837afba4e15ba798f4809586f0ac1b8855bd0032651 in / 
# Tue, 12 Mar 2024 00:48:31 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:64806d9455193063a6bd4aebf47380e94fad8313f6ad1b5d831882c453f43261`  
		Last Modified: Tue, 12 Mar 2024 00:51:39 GMT  
		Size: 26.9 MB (26884021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e32a50f75b9d40c50ce7692a0631af44e30f327e696aa5b28831455123c0d1`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a78498071cf34c7c6bcb0da9274a1a38c73fbb294d613cfac9c0100e903977`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 2.1 MB (2089476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36068ff9365ced1cbed88c3e977f60059201881a2482f8cf3f5d95de3212f48`  
		Last Modified: Wed, 20 Mar 2024 21:52:39 GMT  
		Size: 5.8 MB (5836746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf53231953d794bde70e2b7b7119a814be7bcedab1a665a0c94985ad91a5934`  
		Last Modified: Wed, 20 Mar 2024 21:52:39 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f512760eb47d5604a6a012660a82a055b5433c332a9ed9dbeff2acdf4e8c831e`  
		Last Modified: Wed, 20 Mar 2024 21:52:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f924932e4f06ee4421d9aa0c65781bc2d4e66b5b6921cd2701898c5f207cf5b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3506305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cc0ff8d1f5c499d166f30b882b9a756a9c801545de1080d663caeb2bb0f42db`

```dockerfile
```

-	Layers:
	-	`sha256:bfe76f7bb20909be4b9e643fa059225a1d9e992c6e123b3795bceaf5a7acc391`  
		Last Modified: Wed, 20 Mar 2024 21:52:39 GMT  
		Size: 3.5 MB (3485214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59b8882010ed55ddacd7b4a1329987ff2af9a2367d809d764e8e333d83cc9f4a`  
		Last Modified: Wed, 20 Mar 2024 21:52:38 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ccd988c5b8b64dd797254c5db351be97958404a16137214c5569c0ffd0081e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37688087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27728f0ab685b3a67c0f34a20d27afd4f5f137af0204c15e024a08ccb9689493`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac48a97998740def0fa8b1b7e818bbec003d87e56636ed14d66e8ea9c1b49c18`  
		Last Modified: Wed, 20 Mar 2024 22:05:32 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e6aa77c2974c982d56d398f0e7fde37261a6e629e0ae13bd38cbcfbc94d0f2`  
		Last Modified: Wed, 20 Mar 2024 22:05:33 GMT  
		Size: 2.3 MB (2346182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e87543748bdbe302f363c5c5ba30d5d2f7bddba6e8aa1b1492dbf60f97823f`  
		Last Modified: Wed, 20 Mar 2024 22:05:33 GMT  
		Size: 6.2 MB (6183961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fcc56c57aa721ad68c916103760548406b2f2ae78798ee219c5c037804554d3`  
		Last Modified: Wed, 20 Mar 2024 22:05:32 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad54eed22cbb0e5b0a76ceabcf728ab53a51c2d584ed743ca55c3f83749c7fb`  
		Last Modified: Wed, 20 Mar 2024 22:05:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:e311165ff6d518330323d445e95dd591ded261f129a6dfd3b9bba58349db9b26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3507065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3d95ab8f1447c9653180938a8afc4364a3d150c55a19bcc457e994da2deb96`

```dockerfile
```

-	Layers:
	-	`sha256:088471520c083942039c4a09387bdbef3ef68263c757673503b19844809bb1a8`  
		Last Modified: Wed, 20 Mar 2024 22:05:34 GMT  
		Size: 3.5 MB (3486097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daa3f98d4564330b08871a65867b9574becccd48cf8f34418e8e4e5007494a52`  
		Last Modified: Wed, 20 Mar 2024 22:05:32 GMT  
		Size: 21.0 KB (20968 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:f81e3f7f720aaf1482cc81d8bb3f063a146e5ed1fef7ffe54e62f36346a71b3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39272880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18bb6bb8ab561077858738067ab803ed63757a2c5f53e276936c40e1a4527aae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:57:59 GMT
ADD file:88f04d79dc9f1691544c636ff52d6744a2ff68d504793ea8034b797d0bfc6fd3 in / 
# Tue, 12 Mar 2024 00:58:00 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:576af7ffb10b3f3b8d5523e6b91da8667eb39393cdfd50fb26dfc178e504ba70`  
		Last Modified: Tue, 12 Mar 2024 01:02:43 GMT  
		Size: 30.1 MB (30141873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ca1e74787d7f5345fa4e48b3752fab05e59b0cc9269325db87012c10c20201`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c850abea3f675f18aec4a116fba49dae8f46e99f06997b55a6a2eed0636db316`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 2.5 MB (2492637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14fde32a1b90b6896eaf4e91a78b8f32edf62e2bde66ca3bdbf842d607182b63`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 6.6 MB (6636851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1abdc4ae20d60ffc06b6d337d69a65d0501dc932a9a31039f97854efd852c00c`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e56d15c7c18240ea35e93bd1fadf02ad9d12cf1d4168fc6347adda471053737`  
		Last Modified: Wed, 20 Mar 2024 21:53:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:1a82d1205f3b793796a0ce63454ba7a0e8439159d0cddbbdaa20a03103fa3b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3529875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb96cb648ee7c46e17e8193e254b792e2d16ab1dcd2944281ce40379f0ee1ed`

```dockerfile
```

-	Layers:
	-	`sha256:d0b36f1ef0868bd6a59e83aefd9d82a113291e6d8405938446ea789c06aaae64`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 3.5 MB (3508813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56aa96415543efa9a697197eaf5addc87d9d2eeed66dd1fa3b0821a739c733a7`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 21.1 KB (21062 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:19524094dd845883d46d265bc2c0e83abda00c944e71c65beeb688e1328aee22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37565245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1983e467da37a29b6a5ccc7f7dc4da935cad3d72f262f972d952995365d45623`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 01:06:19 GMT
ADD file:c03c59e261bb08f39e6a97df2fd4b82f1e11b49a62d1859a8f8efac680b80a88 in / 
# Tue, 12 Mar 2024 01:06:23 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aad79459a0f767fcded51c9547150a1cfd96638972389ab8621b5f3eb4a9c280`  
		Last Modified: Tue, 12 Mar 2024 01:17:09 GMT  
		Size: 29.1 MB (29119205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f9ce6b6ef9151bae2476ece2788ab3fcb6d9abf46076b3ab61890a8c5d25e3`  
		Last Modified: Wed, 20 Mar 2024 21:59:53 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4e0a67df5eca0e49eef014debfeb0680de1b95463963c1256e155e92c967a0`  
		Last Modified: Wed, 20 Mar 2024 21:59:54 GMT  
		Size: 1.9 MB (1937678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db0c438efebe0bbb19f79fa801c9c2c52655b590ac16a7196adc5d05702258e`  
		Last Modified: Wed, 20 Mar 2024 21:59:55 GMT  
		Size: 6.5 MB (6506842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97107982137a0d6d10cd7c2f2e613455871a16b69d19c544d26f5c9df4ef2d0`  
		Last Modified: Wed, 20 Mar 2024 21:59:54 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d2108a68b8f51c577db7aa9b41e3bc0507fa18834dc4e235303677021f369f`  
		Last Modified: Wed, 20 Mar 2024 21:59:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:dde4628406ffa6f2e54cdce761e8d050d342a45b4663463a5827ae0420ad7072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.0 KB (21003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ec8712d9cafb05213294e7c991f103858f9ccc5443c2a33560e9fefc5964e32`

```dockerfile
```

-	Layers:
	-	`sha256:ac6b20491333ea6e06cb55be035327040ed503fedd32e789ed3e8082ecaedf94`  
		Last Modified: Wed, 20 Mar 2024 21:59:54 GMT  
		Size: 21.0 KB (21003 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:4c3db32aa1a397cf2a03078efa95429139072b980ab1cfe1d38a3fc03e16b21b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (43006041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ea28ef1fe375457227b59ed4cffadfe2eb8c198795094bf26e6233bd556c8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:9273ef56d086dbc93b46b7e8ae424eb04096fb00c693dd6cda1f48346290d4d5 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c28cd0e276dcdeb4d44f5cc5bb958610750ff902a081b668e3863c2f38eef054`  
		Last Modified: Tue, 12 Mar 2024 00:38:06 GMT  
		Size: 33.1 MB (33119023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62aa36b84dc23bc5eecf52bd0d09534dcc186ab27089192c7aed8210f610e32`  
		Last Modified: Wed, 13 Mar 2024 02:14:26 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec1785cd98038ba62eb16a4aacec38cdbb91c26f98360aafb2ed1017cda3df8`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 2.7 MB (2698364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5105d8a1d382e8083f62216ad1a3ac3ed9e0dab0a2cd5110eb1afa516b084b`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 7.2 MB (7187142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356eaa328e166dd1628acf5a67acf74c032ae2b79667868199736be62871fcc9`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936d8dbc2ebbedc4ae8dc525f7a6ed2c953784d75251955a347e5cb1eab83a22`  
		Last Modified: Wed, 13 Mar 2024 02:14:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:7ba7fc566a7ca1cc4ee19a4562d3c8ff3cbd5c66504843364b286c16a51c673a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3521676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e456fccef08393cbfaa927989c957a984aca49d5b68aff7e43a60bebf063443e`

```dockerfile
```

-	Layers:
	-	`sha256:40dd29e81bcfdcdc7a12cb2843f9bc037c7633d5502e7d49aeab7f1a38b351d1`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 3.5 MB (3500658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1acb5997eff88a90491a6c619d8236c97c1febf8bf3b8fce15b91660a29910df`  
		Last Modified: Wed, 13 Mar 2024 02:14:26 GMT  
		Size: 21.0 KB (21018 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:6ba3af09c6f41f8a8aeb75f0b92546ff342929150d6da315f2c1152c2ac8b89c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35721763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3b0f99b55b9844b9cf7f544669c714d836ca78200a54ea085af430fa58934e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:54:02 GMT
ADD file:80ab985d4871ca6a72156bedfe1038e6b1a89591fc2fd86c4ef778d293223aff in / 
# Tue, 12 Mar 2024 00:54:03 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9cada496cd2b8a88571bf23d513e7fce34888d13321fcf23c6613bffe4c37297`  
		Last Modified: Tue, 12 Mar 2024 01:21:14 GMT  
		Size: 27.5 MB (27488684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c430faffa085700d40355ac1aea08d429376e112bef3b9c00780b1ede56859c2`  
		Last Modified: Wed, 20 Mar 2024 22:17:08 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf1db148a80e9f25b06fe946c697ba8fa83bc46c13515904d4ceceaeb2a4eeb`  
		Last Modified: Wed, 20 Mar 2024 22:17:12 GMT  
		Size: 2.2 MB (2152657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf95ab69cc340a00b9e21b620561903f3f26a245d421506febe9e3c376310098`  
		Last Modified: Wed, 20 Mar 2024 22:17:09 GMT  
		Size: 6.1 MB (6078907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5304ac9e894c6780910c4bd4889d1cc407cb62e54cc4940d8bc7fa74efbb9699`  
		Last Modified: Wed, 20 Mar 2024 22:17:09 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:722d63b783293116e31d9ac81edb640d7218dbb304e2efdc0c1d48aed76e12d2`  
		Last Modified: Wed, 20 Mar 2024 22:17:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:6b3778c79df56c62c44f402a80b924fdb3a5c869694053bff124b8f232640d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bcc8294911dfe44976e400bf92d4e2bee63c8bd56170c94ca2b3c3b05c59135`

```dockerfile
```

-	Layers:
	-	`sha256:e43c6eaae62edc62c95fce6ffd315f1d7c3c249e703a751b4f13b92dba078b59`  
		Last Modified: Wed, 20 Mar 2024 22:17:09 GMT  
		Size: 3.5 MB (3503203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a25398f94b500655282b6629c187cb91a22c84327a970fdcecacda3d14b74649`  
		Last Modified: Wed, 20 Mar 2024 22:17:08 GMT  
		Size: 21.1 KB (21075 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.25`

```console
$ docker pull memcached@sha256:b2c9c9eee25dcc267638dd7142e10a1065f81aa8413f93a1ae915880a1e54645
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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
	-	linux; s390x
	-	unknown; unknown

### `memcached:1.6.25` - linux; amd64

```console
$ docker pull memcached@sha256:f5d6b34b5e53f3c3efa1761e78a3ec1e48806b9cf323f275eb73f744ccecb592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38789552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5659585297ecca8269e4b42bf75ee0ba65573bc53f1ac844ce4442a41168219b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:01 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Tue, 12 Mar 2024 01:21:01 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f5b0c7d5ff100485df42c707b8f798c23491e3390670b6102ec309459c56e1`  
		Last Modified: Wed, 20 Mar 2024 21:53:21 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0347f087df5e5a5e55e4e61f495fb25766015d39f1a62d755e903df3f0a4b463`  
		Last Modified: Wed, 20 Mar 2024 21:53:22 GMT  
		Size: 2.5 MB (2488465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e3316b02adf5a1ede79c485a31043189f5e47f3f295394d2c0e8d4cde01c24`  
		Last Modified: Wed, 20 Mar 2024 21:53:21 GMT  
		Size: 7.2 MB (7175392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b72ea418779aaf6ffa3dcf321d061b13df238a88fcdd3f8d4a8e811f3f329f2`  
		Last Modified: Wed, 20 Mar 2024 21:53:21 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534937fe67d0636cc42a8284656ac23b9f0a138b3b912da0122025298ba0187e`  
		Last Modified: Wed, 20 Mar 2024 21:53:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.25` - unknown; unknown

```console
$ docker pull memcached@sha256:cdfdc5468a693b11d8b5e2c584c6b8167aca56f16bbef4a5c73f88e254f01849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3536051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c3d70d51d8c20eb5bffd2b9e173bf20449fb79a7c1f5dc4e067211a394bba7`

```dockerfile
```

-	Layers:
	-	`sha256:77f1295784ab211addd97298191a342ea0b5bc2ac83e5349eebc5752f9e00eda`  
		Last Modified: Wed, 20 Mar 2024 21:53:22 GMT  
		Size: 3.5 MB (3514934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:204bffe148afae4b974e13d601af8e712c6135452b18b6283a30fa1ffde6e69b`  
		Last Modified: Wed, 20 Mar 2024 21:53:21 GMT  
		Size: 21.1 KB (21117 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.25` - linux; arm variant v5

```console
$ docker pull memcached@sha256:2c0a8fd6a587a5d73f6afbc1fe07536b8a21f37ff8533ce389195c3f0ccfd62b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34811756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0041b5946d66d8e8b27a51ff5f1bb8d593ed96c761133d93788591b5ab21d8e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:48:31 GMT
ADD file:b1bd2ec7dd2a8894ea7b5837afba4e15ba798f4809586f0ac1b8855bd0032651 in / 
# Tue, 12 Mar 2024 00:48:31 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:64806d9455193063a6bd4aebf47380e94fad8313f6ad1b5d831882c453f43261`  
		Last Modified: Tue, 12 Mar 2024 00:51:39 GMT  
		Size: 26.9 MB (26884021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e32a50f75b9d40c50ce7692a0631af44e30f327e696aa5b28831455123c0d1`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a78498071cf34c7c6bcb0da9274a1a38c73fbb294d613cfac9c0100e903977`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 2.1 MB (2089476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36068ff9365ced1cbed88c3e977f60059201881a2482f8cf3f5d95de3212f48`  
		Last Modified: Wed, 20 Mar 2024 21:52:39 GMT  
		Size: 5.8 MB (5836746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf53231953d794bde70e2b7b7119a814be7bcedab1a665a0c94985ad91a5934`  
		Last Modified: Wed, 20 Mar 2024 21:52:39 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f512760eb47d5604a6a012660a82a055b5433c332a9ed9dbeff2acdf4e8c831e`  
		Last Modified: Wed, 20 Mar 2024 21:52:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.25` - unknown; unknown

```console
$ docker pull memcached@sha256:f924932e4f06ee4421d9aa0c65781bc2d4e66b5b6921cd2701898c5f207cf5b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3506305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cc0ff8d1f5c499d166f30b882b9a756a9c801545de1080d663caeb2bb0f42db`

```dockerfile
```

-	Layers:
	-	`sha256:bfe76f7bb20909be4b9e643fa059225a1d9e992c6e123b3795bceaf5a7acc391`  
		Last Modified: Wed, 20 Mar 2024 21:52:39 GMT  
		Size: 3.5 MB (3485214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59b8882010ed55ddacd7b4a1329987ff2af9a2367d809d764e8e333d83cc9f4a`  
		Last Modified: Wed, 20 Mar 2024 21:52:38 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.25` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ccd988c5b8b64dd797254c5db351be97958404a16137214c5569c0ffd0081e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37688087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27728f0ab685b3a67c0f34a20d27afd4f5f137af0204c15e024a08ccb9689493`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac48a97998740def0fa8b1b7e818bbec003d87e56636ed14d66e8ea9c1b49c18`  
		Last Modified: Wed, 20 Mar 2024 22:05:32 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e6aa77c2974c982d56d398f0e7fde37261a6e629e0ae13bd38cbcfbc94d0f2`  
		Last Modified: Wed, 20 Mar 2024 22:05:33 GMT  
		Size: 2.3 MB (2346182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e87543748bdbe302f363c5c5ba30d5d2f7bddba6e8aa1b1492dbf60f97823f`  
		Last Modified: Wed, 20 Mar 2024 22:05:33 GMT  
		Size: 6.2 MB (6183961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fcc56c57aa721ad68c916103760548406b2f2ae78798ee219c5c037804554d3`  
		Last Modified: Wed, 20 Mar 2024 22:05:32 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad54eed22cbb0e5b0a76ceabcf728ab53a51c2d584ed743ca55c3f83749c7fb`  
		Last Modified: Wed, 20 Mar 2024 22:05:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.25` - unknown; unknown

```console
$ docker pull memcached@sha256:e311165ff6d518330323d445e95dd591ded261f129a6dfd3b9bba58349db9b26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3507065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3d95ab8f1447c9653180938a8afc4364a3d150c55a19bcc457e994da2deb96`

```dockerfile
```

-	Layers:
	-	`sha256:088471520c083942039c4a09387bdbef3ef68263c757673503b19844809bb1a8`  
		Last Modified: Wed, 20 Mar 2024 22:05:34 GMT  
		Size: 3.5 MB (3486097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daa3f98d4564330b08871a65867b9574becccd48cf8f34418e8e4e5007494a52`  
		Last Modified: Wed, 20 Mar 2024 22:05:32 GMT  
		Size: 21.0 KB (20968 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.25` - linux; 386

```console
$ docker pull memcached@sha256:f81e3f7f720aaf1482cc81d8bb3f063a146e5ed1fef7ffe54e62f36346a71b3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39272880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18bb6bb8ab561077858738067ab803ed63757a2c5f53e276936c40e1a4527aae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:57:59 GMT
ADD file:88f04d79dc9f1691544c636ff52d6744a2ff68d504793ea8034b797d0bfc6fd3 in / 
# Tue, 12 Mar 2024 00:58:00 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:576af7ffb10b3f3b8d5523e6b91da8667eb39393cdfd50fb26dfc178e504ba70`  
		Last Modified: Tue, 12 Mar 2024 01:02:43 GMT  
		Size: 30.1 MB (30141873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ca1e74787d7f5345fa4e48b3752fab05e59b0cc9269325db87012c10c20201`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c850abea3f675f18aec4a116fba49dae8f46e99f06997b55a6a2eed0636db316`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 2.5 MB (2492637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14fde32a1b90b6896eaf4e91a78b8f32edf62e2bde66ca3bdbf842d607182b63`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 6.6 MB (6636851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1abdc4ae20d60ffc06b6d337d69a65d0501dc932a9a31039f97854efd852c00c`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e56d15c7c18240ea35e93bd1fadf02ad9d12cf1d4168fc6347adda471053737`  
		Last Modified: Wed, 20 Mar 2024 21:53:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.25` - unknown; unknown

```console
$ docker pull memcached@sha256:1a82d1205f3b793796a0ce63454ba7a0e8439159d0cddbbdaa20a03103fa3b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3529875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb96cb648ee7c46e17e8193e254b792e2d16ab1dcd2944281ce40379f0ee1ed`

```dockerfile
```

-	Layers:
	-	`sha256:d0b36f1ef0868bd6a59e83aefd9d82a113291e6d8405938446ea789c06aaae64`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 3.5 MB (3508813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56aa96415543efa9a697197eaf5addc87d9d2eeed66dd1fa3b0821a739c733a7`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 21.1 KB (21062 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.25` - linux; mips64le

```console
$ docker pull memcached@sha256:19524094dd845883d46d265bc2c0e83abda00c944e71c65beeb688e1328aee22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37565245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1983e467da37a29b6a5ccc7f7dc4da935cad3d72f262f972d952995365d45623`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 01:06:19 GMT
ADD file:c03c59e261bb08f39e6a97df2fd4b82f1e11b49a62d1859a8f8efac680b80a88 in / 
# Tue, 12 Mar 2024 01:06:23 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aad79459a0f767fcded51c9547150a1cfd96638972389ab8621b5f3eb4a9c280`  
		Last Modified: Tue, 12 Mar 2024 01:17:09 GMT  
		Size: 29.1 MB (29119205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f9ce6b6ef9151bae2476ece2788ab3fcb6d9abf46076b3ab61890a8c5d25e3`  
		Last Modified: Wed, 20 Mar 2024 21:59:53 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4e0a67df5eca0e49eef014debfeb0680de1b95463963c1256e155e92c967a0`  
		Last Modified: Wed, 20 Mar 2024 21:59:54 GMT  
		Size: 1.9 MB (1937678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db0c438efebe0bbb19f79fa801c9c2c52655b590ac16a7196adc5d05702258e`  
		Last Modified: Wed, 20 Mar 2024 21:59:55 GMT  
		Size: 6.5 MB (6506842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97107982137a0d6d10cd7c2f2e613455871a16b69d19c544d26f5c9df4ef2d0`  
		Last Modified: Wed, 20 Mar 2024 21:59:54 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d2108a68b8f51c577db7aa9b41e3bc0507fa18834dc4e235303677021f369f`  
		Last Modified: Wed, 20 Mar 2024 21:59:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.25` - unknown; unknown

```console
$ docker pull memcached@sha256:dde4628406ffa6f2e54cdce761e8d050d342a45b4663463a5827ae0420ad7072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.0 KB (21003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ec8712d9cafb05213294e7c991f103858f9ccc5443c2a33560e9fefc5964e32`

```dockerfile
```

-	Layers:
	-	`sha256:ac6b20491333ea6e06cb55be035327040ed503fedd32e789ed3e8082ecaedf94`  
		Last Modified: Wed, 20 Mar 2024 21:59:54 GMT  
		Size: 21.0 KB (21003 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.25` - linux; s390x

```console
$ docker pull memcached@sha256:6ba3af09c6f41f8a8aeb75f0b92546ff342929150d6da315f2c1152c2ac8b89c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35721763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3b0f99b55b9844b9cf7f544669c714d836ca78200a54ea085af430fa58934e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:54:02 GMT
ADD file:80ab985d4871ca6a72156bedfe1038e6b1a89591fc2fd86c4ef778d293223aff in / 
# Tue, 12 Mar 2024 00:54:03 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9cada496cd2b8a88571bf23d513e7fce34888d13321fcf23c6613bffe4c37297`  
		Last Modified: Tue, 12 Mar 2024 01:21:14 GMT  
		Size: 27.5 MB (27488684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c430faffa085700d40355ac1aea08d429376e112bef3b9c00780b1ede56859c2`  
		Last Modified: Wed, 20 Mar 2024 22:17:08 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf1db148a80e9f25b06fe946c697ba8fa83bc46c13515904d4ceceaeb2a4eeb`  
		Last Modified: Wed, 20 Mar 2024 22:17:12 GMT  
		Size: 2.2 MB (2152657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf95ab69cc340a00b9e21b620561903f3f26a245d421506febe9e3c376310098`  
		Last Modified: Wed, 20 Mar 2024 22:17:09 GMT  
		Size: 6.1 MB (6078907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5304ac9e894c6780910c4bd4889d1cc407cb62e54cc4940d8bc7fa74efbb9699`  
		Last Modified: Wed, 20 Mar 2024 22:17:09 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:722d63b783293116e31d9ac81edb640d7218dbb304e2efdc0c1d48aed76e12d2`  
		Last Modified: Wed, 20 Mar 2024 22:17:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.25` - unknown; unknown

```console
$ docker pull memcached@sha256:6b3778c79df56c62c44f402a80b924fdb3a5c869694053bff124b8f232640d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bcc8294911dfe44976e400bf92d4e2bee63c8bd56170c94ca2b3c3b05c59135`

```dockerfile
```

-	Layers:
	-	`sha256:e43c6eaae62edc62c95fce6ffd315f1d7c3c249e703a751b4f13b92dba078b59`  
		Last Modified: Wed, 20 Mar 2024 22:17:09 GMT  
		Size: 3.5 MB (3503203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a25398f94b500655282b6629c187cb91a22c84327a970fdcecacda3d14b74649`  
		Last Modified: Wed, 20 Mar 2024 22:17:08 GMT  
		Size: 21.1 KB (21075 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.25-alpine`

```console
$ docker pull memcached@sha256:c0d2b9fc0e85570729d32bc0674774c40ef9e7641a8d0e9c3d4efddb15c3a9e3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `memcached:1.6.25-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:f6b5f19ba2996847e54c3f8ac723bfcee01dcbf26a743b771eebd949adcd3214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbcb4ff24a50bf9bfef0d77f5f341124655431b10d81d888846724c5482b817e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52bc7dd0547fab52a919b23ad8ed09de96e085903366fa3e77e95ad2fe89f1e`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba631f297238f62439f901dd841f1562f5e460c41dbdc74a6a8e5e6999a18cf`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 104.2 KB (104208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ff2edca2876fc5c62dce1c2b8acbf97b83c796b95f85065e90770a00b21cc5`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 952.1 KB (952140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da3504e92ee2c623b4d2facb6ab6f4a1bc4f1fdcea560b6e9f700f66fd285b2`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71408ec44fa46990bd8afeb115db16e6bf557a3ab9d5e2525082db1f56fbc1ab`  
		Last Modified: Wed, 20 Mar 2024 21:53:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.25-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9a6af97b4f188d601386a7ae666c795c7b8ced4a5a80bc0b486f58a12925509b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d835d5590b950bb321312a339b2d238165437c07297b88b798cf96444114337`

```dockerfile
```

-	Layers:
	-	`sha256:3ab2902d9d1e907cc57cd60627dd6c14dc918adc7f486aa089a23cf66f2590f7`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1e7a2c87072e6d2f3f1c8bb3223221aa5aa79c74f7068735808f053d22d34f6`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 19.5 KB (19468 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.25-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:89080028f9e15816ca1bad47470cbb7f97f41c7a4d0127a8b78a39e3eaf3f26f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4425175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38f424677a1fe9988b83477de372d7e42da856eab7e901ecffc2712f49dafe6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
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
	-	`sha256:35d4a8618a7d4f81bed85e38e956c13ad0f4dbe365a1d3e4839d8c84a65a7a2e`  
		Last Modified: Wed, 20 Mar 2024 22:08:20 GMT  
		Size: 954.9 KB (954913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8e229d9ad87b49355b05973eae3eec037dabe9d4f26ae02436d266d09eb384`  
		Last Modified: Wed, 20 Mar 2024 22:08:19 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e5d64381b1947651e9afa510f0f1b109147ea08caf9fcdd31872232fa5da2f`  
		Last Modified: Wed, 20 Mar 2024 22:08:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.25-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c71eeeaa3b1e21d77b74c472adfe61bcdb9f3ea73b628eac681931a06d6b2f66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f535672624f50a772f4ee3e725c007c633eb779ee9b37c92dc962f4c991c87c`

```dockerfile
```

-	Layers:
	-	`sha256:ef9589529b64b76286139cc56c9358c9e2b0583070c534151222f1761776eee8`  
		Last Modified: Wed, 20 Mar 2024 22:08:19 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b6a01c1332859fd1b1618cc06466869f7737c345d4d193f6728cbf8f25c4c8c`  
		Last Modified: Wed, 20 Mar 2024 22:08:19 GMT  
		Size: 19.3 KB (19320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.25-alpine` - linux; 386

```console
$ docker pull memcached@sha256:7a09990d28075b0ae82ca0fbb381a9682d782f55fcf7927794c1f56d3f5f5592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4300861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc1012fc4f4bdb1275a61cd5fae08ce070ed5dfb60886d0b72e9434ceb746f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7fcdd9df8a6fc84db8522d3ed5fa60931ec83e5741b97bf6b6484e58efd689`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114d973bd16245ab06782260b9892f2d397fb5a001bc2e9e75d7aae40f50f0e7`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 109.3 KB (109323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d971f09b89e4ba53f0f0b60389db42eb23aecc41de6341fbaa80d85968e87b`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 945.8 KB (945803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce30c9db432ce705b03569af9ac255d12c994029ddd23ac85803f8001718016`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f35a47fb81dc09ebc6d8faab40aaa406320d7901e751097edfdb6c70fd5b50`  
		Last Modified: Wed, 20 Mar 2024 21:53:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.25-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d83e592adef091fda12c0a2c1d3940a307ebd22dfff5ef4abacf9d9350d7e64d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9372b7c2bc43fdaf94c2fb5b07e31b6dbd0c58d87c5a23a58590088e0e731222`

```dockerfile
```

-	Layers:
	-	`sha256:c1fcdf84d7c55edc2be4a9ca13b91e6fb4a0bb46b7782ccf23066d0e625113d9`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:729594b664d4e18c05f402b9c0e9d9665ebafe54d9fc4b434cfb3d02cbd14fb4`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 19.4 KB (19413 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.25-alpine3.19`

```console
$ docker pull memcached@sha256:c0d2b9fc0e85570729d32bc0674774c40ef9e7641a8d0e9c3d4efddb15c3a9e3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `memcached:1.6.25-alpine3.19` - linux; amd64

```console
$ docker pull memcached@sha256:f6b5f19ba2996847e54c3f8ac723bfcee01dcbf26a743b771eebd949adcd3214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbcb4ff24a50bf9bfef0d77f5f341124655431b10d81d888846724c5482b817e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52bc7dd0547fab52a919b23ad8ed09de96e085903366fa3e77e95ad2fe89f1e`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba631f297238f62439f901dd841f1562f5e460c41dbdc74a6a8e5e6999a18cf`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 104.2 KB (104208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ff2edca2876fc5c62dce1c2b8acbf97b83c796b95f85065e90770a00b21cc5`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 952.1 KB (952140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da3504e92ee2c623b4d2facb6ab6f4a1bc4f1fdcea560b6e9f700f66fd285b2`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71408ec44fa46990bd8afeb115db16e6bf557a3ab9d5e2525082db1f56fbc1ab`  
		Last Modified: Wed, 20 Mar 2024 21:53:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.25-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:9a6af97b4f188d601386a7ae666c795c7b8ced4a5a80bc0b486f58a12925509b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d835d5590b950bb321312a339b2d238165437c07297b88b798cf96444114337`

```dockerfile
```

-	Layers:
	-	`sha256:3ab2902d9d1e907cc57cd60627dd6c14dc918adc7f486aa089a23cf66f2590f7`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1e7a2c87072e6d2f3f1c8bb3223221aa5aa79c74f7068735808f053d22d34f6`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 19.5 KB (19468 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.25-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:89080028f9e15816ca1bad47470cbb7f97f41c7a4d0127a8b78a39e3eaf3f26f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4425175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38f424677a1fe9988b83477de372d7e42da856eab7e901ecffc2712f49dafe6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
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
	-	`sha256:35d4a8618a7d4f81bed85e38e956c13ad0f4dbe365a1d3e4839d8c84a65a7a2e`  
		Last Modified: Wed, 20 Mar 2024 22:08:20 GMT  
		Size: 954.9 KB (954913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8e229d9ad87b49355b05973eae3eec037dabe9d4f26ae02436d266d09eb384`  
		Last Modified: Wed, 20 Mar 2024 22:08:19 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e5d64381b1947651e9afa510f0f1b109147ea08caf9fcdd31872232fa5da2f`  
		Last Modified: Wed, 20 Mar 2024 22:08:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.25-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:c71eeeaa3b1e21d77b74c472adfe61bcdb9f3ea73b628eac681931a06d6b2f66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f535672624f50a772f4ee3e725c007c633eb779ee9b37c92dc962f4c991c87c`

```dockerfile
```

-	Layers:
	-	`sha256:ef9589529b64b76286139cc56c9358c9e2b0583070c534151222f1761776eee8`  
		Last Modified: Wed, 20 Mar 2024 22:08:19 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b6a01c1332859fd1b1618cc06466869f7737c345d4d193f6728cbf8f25c4c8c`  
		Last Modified: Wed, 20 Mar 2024 22:08:19 GMT  
		Size: 19.3 KB (19320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.25-alpine3.19` - linux; 386

```console
$ docker pull memcached@sha256:7a09990d28075b0ae82ca0fbb381a9682d782f55fcf7927794c1f56d3f5f5592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4300861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc1012fc4f4bdb1275a61cd5fae08ce070ed5dfb60886d0b72e9434ceb746f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7fcdd9df8a6fc84db8522d3ed5fa60931ec83e5741b97bf6b6484e58efd689`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114d973bd16245ab06782260b9892f2d397fb5a001bc2e9e75d7aae40f50f0e7`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 109.3 KB (109323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d971f09b89e4ba53f0f0b60389db42eb23aecc41de6341fbaa80d85968e87b`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 945.8 KB (945803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce30c9db432ce705b03569af9ac255d12c994029ddd23ac85803f8001718016`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f35a47fb81dc09ebc6d8faab40aaa406320d7901e751097edfdb6c70fd5b50`  
		Last Modified: Wed, 20 Mar 2024 21:53:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.25-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:d83e592adef091fda12c0a2c1d3940a307ebd22dfff5ef4abacf9d9350d7e64d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9372b7c2bc43fdaf94c2fb5b07e31b6dbd0c58d87c5a23a58590088e0e731222`

```dockerfile
```

-	Layers:
	-	`sha256:c1fcdf84d7c55edc2be4a9ca13b91e6fb4a0bb46b7782ccf23066d0e625113d9`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:729594b664d4e18c05f402b9c0e9d9665ebafe54d9fc4b434cfb3d02cbd14fb4`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 19.4 KB (19413 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.25-bookworm`

```console
$ docker pull memcached@sha256:b2c9c9eee25dcc267638dd7142e10a1065f81aa8413f93a1ae915880a1e54645
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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
	-	linux; s390x
	-	unknown; unknown

### `memcached:1.6.25-bookworm` - linux; amd64

```console
$ docker pull memcached@sha256:f5d6b34b5e53f3c3efa1761e78a3ec1e48806b9cf323f275eb73f744ccecb592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38789552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5659585297ecca8269e4b42bf75ee0ba65573bc53f1ac844ce4442a41168219b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:01 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Tue, 12 Mar 2024 01:21:01 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f5b0c7d5ff100485df42c707b8f798c23491e3390670b6102ec309459c56e1`  
		Last Modified: Wed, 20 Mar 2024 21:53:21 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0347f087df5e5a5e55e4e61f495fb25766015d39f1a62d755e903df3f0a4b463`  
		Last Modified: Wed, 20 Mar 2024 21:53:22 GMT  
		Size: 2.5 MB (2488465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e3316b02adf5a1ede79c485a31043189f5e47f3f295394d2c0e8d4cde01c24`  
		Last Modified: Wed, 20 Mar 2024 21:53:21 GMT  
		Size: 7.2 MB (7175392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b72ea418779aaf6ffa3dcf321d061b13df238a88fcdd3f8d4a8e811f3f329f2`  
		Last Modified: Wed, 20 Mar 2024 21:53:21 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534937fe67d0636cc42a8284656ac23b9f0a138b3b912da0122025298ba0187e`  
		Last Modified: Wed, 20 Mar 2024 21:53:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.25-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:cdfdc5468a693b11d8b5e2c584c6b8167aca56f16bbef4a5c73f88e254f01849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3536051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c3d70d51d8c20eb5bffd2b9e173bf20449fb79a7c1f5dc4e067211a394bba7`

```dockerfile
```

-	Layers:
	-	`sha256:77f1295784ab211addd97298191a342ea0b5bc2ac83e5349eebc5752f9e00eda`  
		Last Modified: Wed, 20 Mar 2024 21:53:22 GMT  
		Size: 3.5 MB (3514934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:204bffe148afae4b974e13d601af8e712c6135452b18b6283a30fa1ffde6e69b`  
		Last Modified: Wed, 20 Mar 2024 21:53:21 GMT  
		Size: 21.1 KB (21117 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.25-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:2c0a8fd6a587a5d73f6afbc1fe07536b8a21f37ff8533ce389195c3f0ccfd62b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34811756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0041b5946d66d8e8b27a51ff5f1bb8d593ed96c761133d93788591b5ab21d8e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:48:31 GMT
ADD file:b1bd2ec7dd2a8894ea7b5837afba4e15ba798f4809586f0ac1b8855bd0032651 in / 
# Tue, 12 Mar 2024 00:48:31 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:64806d9455193063a6bd4aebf47380e94fad8313f6ad1b5d831882c453f43261`  
		Last Modified: Tue, 12 Mar 2024 00:51:39 GMT  
		Size: 26.9 MB (26884021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e32a50f75b9d40c50ce7692a0631af44e30f327e696aa5b28831455123c0d1`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a78498071cf34c7c6bcb0da9274a1a38c73fbb294d613cfac9c0100e903977`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 2.1 MB (2089476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36068ff9365ced1cbed88c3e977f60059201881a2482f8cf3f5d95de3212f48`  
		Last Modified: Wed, 20 Mar 2024 21:52:39 GMT  
		Size: 5.8 MB (5836746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf53231953d794bde70e2b7b7119a814be7bcedab1a665a0c94985ad91a5934`  
		Last Modified: Wed, 20 Mar 2024 21:52:39 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f512760eb47d5604a6a012660a82a055b5433c332a9ed9dbeff2acdf4e8c831e`  
		Last Modified: Wed, 20 Mar 2024 21:52:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.25-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f924932e4f06ee4421d9aa0c65781bc2d4e66b5b6921cd2701898c5f207cf5b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3506305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cc0ff8d1f5c499d166f30b882b9a756a9c801545de1080d663caeb2bb0f42db`

```dockerfile
```

-	Layers:
	-	`sha256:bfe76f7bb20909be4b9e643fa059225a1d9e992c6e123b3795bceaf5a7acc391`  
		Last Modified: Wed, 20 Mar 2024 21:52:39 GMT  
		Size: 3.5 MB (3485214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59b8882010ed55ddacd7b4a1329987ff2af9a2367d809d764e8e333d83cc9f4a`  
		Last Modified: Wed, 20 Mar 2024 21:52:38 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.25-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ccd988c5b8b64dd797254c5db351be97958404a16137214c5569c0ffd0081e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37688087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27728f0ab685b3a67c0f34a20d27afd4f5f137af0204c15e024a08ccb9689493`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac48a97998740def0fa8b1b7e818bbec003d87e56636ed14d66e8ea9c1b49c18`  
		Last Modified: Wed, 20 Mar 2024 22:05:32 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e6aa77c2974c982d56d398f0e7fde37261a6e629e0ae13bd38cbcfbc94d0f2`  
		Last Modified: Wed, 20 Mar 2024 22:05:33 GMT  
		Size: 2.3 MB (2346182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e87543748bdbe302f363c5c5ba30d5d2f7bddba6e8aa1b1492dbf60f97823f`  
		Last Modified: Wed, 20 Mar 2024 22:05:33 GMT  
		Size: 6.2 MB (6183961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fcc56c57aa721ad68c916103760548406b2f2ae78798ee219c5c037804554d3`  
		Last Modified: Wed, 20 Mar 2024 22:05:32 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad54eed22cbb0e5b0a76ceabcf728ab53a51c2d584ed743ca55c3f83749c7fb`  
		Last Modified: Wed, 20 Mar 2024 22:05:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.25-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:e311165ff6d518330323d445e95dd591ded261f129a6dfd3b9bba58349db9b26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3507065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3d95ab8f1447c9653180938a8afc4364a3d150c55a19bcc457e994da2deb96`

```dockerfile
```

-	Layers:
	-	`sha256:088471520c083942039c4a09387bdbef3ef68263c757673503b19844809bb1a8`  
		Last Modified: Wed, 20 Mar 2024 22:05:34 GMT  
		Size: 3.5 MB (3486097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daa3f98d4564330b08871a65867b9574becccd48cf8f34418e8e4e5007494a52`  
		Last Modified: Wed, 20 Mar 2024 22:05:32 GMT  
		Size: 21.0 KB (20968 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.25-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:f81e3f7f720aaf1482cc81d8bb3f063a146e5ed1fef7ffe54e62f36346a71b3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39272880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18bb6bb8ab561077858738067ab803ed63757a2c5f53e276936c40e1a4527aae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:57:59 GMT
ADD file:88f04d79dc9f1691544c636ff52d6744a2ff68d504793ea8034b797d0bfc6fd3 in / 
# Tue, 12 Mar 2024 00:58:00 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:576af7ffb10b3f3b8d5523e6b91da8667eb39393cdfd50fb26dfc178e504ba70`  
		Last Modified: Tue, 12 Mar 2024 01:02:43 GMT  
		Size: 30.1 MB (30141873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ca1e74787d7f5345fa4e48b3752fab05e59b0cc9269325db87012c10c20201`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c850abea3f675f18aec4a116fba49dae8f46e99f06997b55a6a2eed0636db316`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 2.5 MB (2492637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14fde32a1b90b6896eaf4e91a78b8f32edf62e2bde66ca3bdbf842d607182b63`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 6.6 MB (6636851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1abdc4ae20d60ffc06b6d337d69a65d0501dc932a9a31039f97854efd852c00c`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e56d15c7c18240ea35e93bd1fadf02ad9d12cf1d4168fc6347adda471053737`  
		Last Modified: Wed, 20 Mar 2024 21:53:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.25-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:1a82d1205f3b793796a0ce63454ba7a0e8439159d0cddbbdaa20a03103fa3b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3529875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb96cb648ee7c46e17e8193e254b792e2d16ab1dcd2944281ce40379f0ee1ed`

```dockerfile
```

-	Layers:
	-	`sha256:d0b36f1ef0868bd6a59e83aefd9d82a113291e6d8405938446ea789c06aaae64`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 3.5 MB (3508813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56aa96415543efa9a697197eaf5addc87d9d2eeed66dd1fa3b0821a739c733a7`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 21.1 KB (21062 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.25-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:19524094dd845883d46d265bc2c0e83abda00c944e71c65beeb688e1328aee22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37565245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1983e467da37a29b6a5ccc7f7dc4da935cad3d72f262f972d952995365d45623`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 01:06:19 GMT
ADD file:c03c59e261bb08f39e6a97df2fd4b82f1e11b49a62d1859a8f8efac680b80a88 in / 
# Tue, 12 Mar 2024 01:06:23 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aad79459a0f767fcded51c9547150a1cfd96638972389ab8621b5f3eb4a9c280`  
		Last Modified: Tue, 12 Mar 2024 01:17:09 GMT  
		Size: 29.1 MB (29119205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f9ce6b6ef9151bae2476ece2788ab3fcb6d9abf46076b3ab61890a8c5d25e3`  
		Last Modified: Wed, 20 Mar 2024 21:59:53 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4e0a67df5eca0e49eef014debfeb0680de1b95463963c1256e155e92c967a0`  
		Last Modified: Wed, 20 Mar 2024 21:59:54 GMT  
		Size: 1.9 MB (1937678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db0c438efebe0bbb19f79fa801c9c2c52655b590ac16a7196adc5d05702258e`  
		Last Modified: Wed, 20 Mar 2024 21:59:55 GMT  
		Size: 6.5 MB (6506842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97107982137a0d6d10cd7c2f2e613455871a16b69d19c544d26f5c9df4ef2d0`  
		Last Modified: Wed, 20 Mar 2024 21:59:54 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d2108a68b8f51c577db7aa9b41e3bc0507fa18834dc4e235303677021f369f`  
		Last Modified: Wed, 20 Mar 2024 21:59:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.25-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:dde4628406ffa6f2e54cdce761e8d050d342a45b4663463a5827ae0420ad7072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.0 KB (21003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ec8712d9cafb05213294e7c991f103858f9ccc5443c2a33560e9fefc5964e32`

```dockerfile
```

-	Layers:
	-	`sha256:ac6b20491333ea6e06cb55be035327040ed503fedd32e789ed3e8082ecaedf94`  
		Last Modified: Wed, 20 Mar 2024 21:59:54 GMT  
		Size: 21.0 KB (21003 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.25-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:6ba3af09c6f41f8a8aeb75f0b92546ff342929150d6da315f2c1152c2ac8b89c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35721763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3b0f99b55b9844b9cf7f544669c714d836ca78200a54ea085af430fa58934e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:54:02 GMT
ADD file:80ab985d4871ca6a72156bedfe1038e6b1a89591fc2fd86c4ef778d293223aff in / 
# Tue, 12 Mar 2024 00:54:03 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9cada496cd2b8a88571bf23d513e7fce34888d13321fcf23c6613bffe4c37297`  
		Last Modified: Tue, 12 Mar 2024 01:21:14 GMT  
		Size: 27.5 MB (27488684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c430faffa085700d40355ac1aea08d429376e112bef3b9c00780b1ede56859c2`  
		Last Modified: Wed, 20 Mar 2024 22:17:08 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf1db148a80e9f25b06fe946c697ba8fa83bc46c13515904d4ceceaeb2a4eeb`  
		Last Modified: Wed, 20 Mar 2024 22:17:12 GMT  
		Size: 2.2 MB (2152657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf95ab69cc340a00b9e21b620561903f3f26a245d421506febe9e3c376310098`  
		Last Modified: Wed, 20 Mar 2024 22:17:09 GMT  
		Size: 6.1 MB (6078907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5304ac9e894c6780910c4bd4889d1cc407cb62e54cc4940d8bc7fa74efbb9699`  
		Last Modified: Wed, 20 Mar 2024 22:17:09 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:722d63b783293116e31d9ac81edb640d7218dbb304e2efdc0c1d48aed76e12d2`  
		Last Modified: Wed, 20 Mar 2024 22:17:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.25-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:6b3778c79df56c62c44f402a80b924fdb3a5c869694053bff124b8f232640d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bcc8294911dfe44976e400bf92d4e2bee63c8bd56170c94ca2b3c3b05c59135`

```dockerfile
```

-	Layers:
	-	`sha256:e43c6eaae62edc62c95fce6ffd315f1d7c3c249e703a751b4f13b92dba078b59`  
		Last Modified: Wed, 20 Mar 2024 22:17:09 GMT  
		Size: 3.5 MB (3503203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a25398f94b500655282b6629c187cb91a22c84327a970fdcecacda3d14b74649`  
		Last Modified: Wed, 20 Mar 2024 22:17:08 GMT  
		Size: 21.1 KB (21075 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine`

```console
$ docker pull memcached@sha256:58dfadef5a410ef30822e05229187fddce1a8da7c1937038b091fb8cb7826ac1
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
$ docker pull memcached@sha256:f6b5f19ba2996847e54c3f8ac723bfcee01dcbf26a743b771eebd949adcd3214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbcb4ff24a50bf9bfef0d77f5f341124655431b10d81d888846724c5482b817e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52bc7dd0547fab52a919b23ad8ed09de96e085903366fa3e77e95ad2fe89f1e`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba631f297238f62439f901dd841f1562f5e460c41dbdc74a6a8e5e6999a18cf`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 104.2 KB (104208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ff2edca2876fc5c62dce1c2b8acbf97b83c796b95f85065e90770a00b21cc5`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 952.1 KB (952140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da3504e92ee2c623b4d2facb6ab6f4a1bc4f1fdcea560b6e9f700f66fd285b2`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71408ec44fa46990bd8afeb115db16e6bf557a3ab9d5e2525082db1f56fbc1ab`  
		Last Modified: Wed, 20 Mar 2024 21:53:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9a6af97b4f188d601386a7ae666c795c7b8ced4a5a80bc0b486f58a12925509b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d835d5590b950bb321312a339b2d238165437c07297b88b798cf96444114337`

```dockerfile
```

-	Layers:
	-	`sha256:3ab2902d9d1e907cc57cd60627dd6c14dc918adc7f486aa089a23cf66f2590f7`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1e7a2c87072e6d2f3f1c8bb3223221aa5aa79c74f7068735808f053d22d34f6`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 19.5 KB (19468 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:89080028f9e15816ca1bad47470cbb7f97f41c7a4d0127a8b78a39e3eaf3f26f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4425175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38f424677a1fe9988b83477de372d7e42da856eab7e901ecffc2712f49dafe6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
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
	-	`sha256:35d4a8618a7d4f81bed85e38e956c13ad0f4dbe365a1d3e4839d8c84a65a7a2e`  
		Last Modified: Wed, 20 Mar 2024 22:08:20 GMT  
		Size: 954.9 KB (954913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8e229d9ad87b49355b05973eae3eec037dabe9d4f26ae02436d266d09eb384`  
		Last Modified: Wed, 20 Mar 2024 22:08:19 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e5d64381b1947651e9afa510f0f1b109147ea08caf9fcdd31872232fa5da2f`  
		Last Modified: Wed, 20 Mar 2024 22:08:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c71eeeaa3b1e21d77b74c472adfe61bcdb9f3ea73b628eac681931a06d6b2f66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f535672624f50a772f4ee3e725c007c633eb779ee9b37c92dc962f4c991c87c`

```dockerfile
```

-	Layers:
	-	`sha256:ef9589529b64b76286139cc56c9358c9e2b0583070c534151222f1761776eee8`  
		Last Modified: Wed, 20 Mar 2024 22:08:19 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b6a01c1332859fd1b1618cc06466869f7737c345d4d193f6728cbf8f25c4c8c`  
		Last Modified: Wed, 20 Mar 2024 22:08:19 GMT  
		Size: 19.3 KB (19320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:7a09990d28075b0ae82ca0fbb381a9682d782f55fcf7927794c1f56d3f5f5592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4300861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc1012fc4f4bdb1275a61cd5fae08ce070ed5dfb60886d0b72e9434ceb746f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7fcdd9df8a6fc84db8522d3ed5fa60931ec83e5741b97bf6b6484e58efd689`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114d973bd16245ab06782260b9892f2d397fb5a001bc2e9e75d7aae40f50f0e7`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 109.3 KB (109323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d971f09b89e4ba53f0f0b60389db42eb23aecc41de6341fbaa80d85968e87b`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 945.8 KB (945803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce30c9db432ce705b03569af9ac255d12c994029ddd23ac85803f8001718016`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f35a47fb81dc09ebc6d8faab40aaa406320d7901e751097edfdb6c70fd5b50`  
		Last Modified: Wed, 20 Mar 2024 21:53:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d83e592adef091fda12c0a2c1d3940a307ebd22dfff5ef4abacf9d9350d7e64d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9372b7c2bc43fdaf94c2fb5b07e31b6dbd0c58d87c5a23a58590088e0e731222`

```dockerfile
```

-	Layers:
	-	`sha256:c1fcdf84d7c55edc2be4a9ca13b91e6fb4a0bb46b7782ccf23066d0e625113d9`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:729594b664d4e18c05f402b9c0e9d9665ebafe54d9fc4b434cfb3d02cbd14fb4`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 19.4 KB (19413 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:542b6c07395477ef8cb25d0ea2ff0d596b1ab7f849518c04e8ca9bb8f990a1da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4468736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9760785d8debed5a647d14058f436d167f4af55a64b0f203426e99da48cb8a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
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
	-	`sha256:d5aa23581942b7bdabf4f033e906fb350a53e488d497193d8d284750885a4cd6`  
		Last Modified: Sat, 16 Mar 2024 10:30:19 GMT  
		Size: 985.3 KB (985333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00d6241d3b173192fb86c75a90e166eda74b11c2dadd7519e8bfd5e5f8d20b5`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2008720f740687d6af827d98e0a17ac17c40265a0733232b3f65891cefd55ba4`  
		Last Modified: Sat, 16 Mar 2024 10:30:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:baf2f10adc34c6657b730c8bcf1d40afa9cbc5277bc79c1e4a35799ba08c4504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f61ca4d4044f9e7f21d7149dd863ef113c78738e2c3e84b2994e68fe5b7adda`

```dockerfile
```

-	Layers:
	-	`sha256:054cdb368dd44a8e73fdf9e940711c8c646cb1d917752910cfd489178cd1bd40`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e0b9862dbe39bc1e2f1598d956acc8877a83d8516baa2fe29261ecd8d5c16ed`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 19.4 KB (19370 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; s390x

```console
$ docker pull memcached@sha256:2bbbf6c60ae563e7fbf0b0d7fff645531ed4706dd6c6b783c35d4ecef1fd70d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4327559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a414e168eff8283c9d16f99e5c31558dec31c6b15ee761de45a40bb6839ee1cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
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
	-	`sha256:61064e5fd6e0cc6334b6eefff4fe163950d84c1de3c42ec9fdf85d92005f3ae9`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 970.1 KB (970135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f1d5965cdbebebdce4669474799f51b9ef3d6f42b376fa617a1b945d4d4325`  
		Last Modified: Sun, 17 Mar 2024 22:11:55 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23608093e2a154f293a6e3287a11ad798936c0146ae7f1943b035db32efa778b`  
		Last Modified: Sun, 17 Mar 2024 22:11:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2dd2215c8ae081cddcbefef029e030b94e041ecd1f2e409d9f704ffdb720d99a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e50e27f5c06d319f5b8cc2b2ba76311d2d120269d1d9d22aa58ae531733001`

```dockerfile
```

-	Layers:
	-	`sha256:91ebf1e0392ad0faffa17054e66a85a7fb1aa0004495345cf4ed19fd5cfa0a6b`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f135346500525ff3a63124190a6511a8a7af0659061127048c4c9f62c219d119`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 19.3 KB (19301 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine3.19`

```console
$ docker pull memcached@sha256:58dfadef5a410ef30822e05229187fddce1a8da7c1937038b091fb8cb7826ac1
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
$ docker pull memcached@sha256:f6b5f19ba2996847e54c3f8ac723bfcee01dcbf26a743b771eebd949adcd3214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbcb4ff24a50bf9bfef0d77f5f341124655431b10d81d888846724c5482b817e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52bc7dd0547fab52a919b23ad8ed09de96e085903366fa3e77e95ad2fe89f1e`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba631f297238f62439f901dd841f1562f5e460c41dbdc74a6a8e5e6999a18cf`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 104.2 KB (104208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ff2edca2876fc5c62dce1c2b8acbf97b83c796b95f85065e90770a00b21cc5`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 952.1 KB (952140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da3504e92ee2c623b4d2facb6ab6f4a1bc4f1fdcea560b6e9f700f66fd285b2`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71408ec44fa46990bd8afeb115db16e6bf557a3ab9d5e2525082db1f56fbc1ab`  
		Last Modified: Wed, 20 Mar 2024 21:53:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:9a6af97b4f188d601386a7ae666c795c7b8ced4a5a80bc0b486f58a12925509b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d835d5590b950bb321312a339b2d238165437c07297b88b798cf96444114337`

```dockerfile
```

-	Layers:
	-	`sha256:3ab2902d9d1e907cc57cd60627dd6c14dc918adc7f486aa089a23cf66f2590f7`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1e7a2c87072e6d2f3f1c8bb3223221aa5aa79c74f7068735808f053d22d34f6`  
		Last Modified: Wed, 20 Mar 2024 21:53:05 GMT  
		Size: 19.5 KB (19468 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:89080028f9e15816ca1bad47470cbb7f97f41c7a4d0127a8b78a39e3eaf3f26f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4425175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38f424677a1fe9988b83477de372d7e42da856eab7e901ecffc2712f49dafe6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
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
	-	`sha256:35d4a8618a7d4f81bed85e38e956c13ad0f4dbe365a1d3e4839d8c84a65a7a2e`  
		Last Modified: Wed, 20 Mar 2024 22:08:20 GMT  
		Size: 954.9 KB (954913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8e229d9ad87b49355b05973eae3eec037dabe9d4f26ae02436d266d09eb384`  
		Last Modified: Wed, 20 Mar 2024 22:08:19 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e5d64381b1947651e9afa510f0f1b109147ea08caf9fcdd31872232fa5da2f`  
		Last Modified: Wed, 20 Mar 2024 22:08:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:c71eeeaa3b1e21d77b74c472adfe61bcdb9f3ea73b628eac681931a06d6b2f66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f535672624f50a772f4ee3e725c007c633eb779ee9b37c92dc962f4c991c87c`

```dockerfile
```

-	Layers:
	-	`sha256:ef9589529b64b76286139cc56c9358c9e2b0583070c534151222f1761776eee8`  
		Last Modified: Wed, 20 Mar 2024 22:08:19 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b6a01c1332859fd1b1618cc06466869f7737c345d4d193f6728cbf8f25c4c8c`  
		Last Modified: Wed, 20 Mar 2024 22:08:19 GMT  
		Size: 19.3 KB (19320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.19` - linux; 386

```console
$ docker pull memcached@sha256:7a09990d28075b0ae82ca0fbb381a9682d782f55fcf7927794c1f56d3f5f5592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4300861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc1012fc4f4bdb1275a61cd5fae08ce070ed5dfb60886d0b72e9434ceb746f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7fcdd9df8a6fc84db8522d3ed5fa60931ec83e5741b97bf6b6484e58efd689`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114d973bd16245ab06782260b9892f2d397fb5a001bc2e9e75d7aae40f50f0e7`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 109.3 KB (109323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d971f09b89e4ba53f0f0b60389db42eb23aecc41de6341fbaa80d85968e87b`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 945.8 KB (945803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce30c9db432ce705b03569af9ac255d12c994029ddd23ac85803f8001718016`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f35a47fb81dc09ebc6d8faab40aaa406320d7901e751097edfdb6c70fd5b50`  
		Last Modified: Wed, 20 Mar 2024 21:53:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:d83e592adef091fda12c0a2c1d3940a307ebd22dfff5ef4abacf9d9350d7e64d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9372b7c2bc43fdaf94c2fb5b07e31b6dbd0c58d87c5a23a58590088e0e731222`

```dockerfile
```

-	Layers:
	-	`sha256:c1fcdf84d7c55edc2be4a9ca13b91e6fb4a0bb46b7782ccf23066d0e625113d9`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:729594b664d4e18c05f402b9c0e9d9665ebafe54d9fc4b434cfb3d02cbd14fb4`  
		Last Modified: Wed, 20 Mar 2024 21:53:15 GMT  
		Size: 19.4 KB (19413 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.19` - linux; ppc64le

```console
$ docker pull memcached@sha256:542b6c07395477ef8cb25d0ea2ff0d596b1ab7f849518c04e8ca9bb8f990a1da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4468736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9760785d8debed5a647d14058f436d167f4af55a64b0f203426e99da48cb8a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
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
	-	`sha256:d5aa23581942b7bdabf4f033e906fb350a53e488d497193d8d284750885a4cd6`  
		Last Modified: Sat, 16 Mar 2024 10:30:19 GMT  
		Size: 985.3 KB (985333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00d6241d3b173192fb86c75a90e166eda74b11c2dadd7519e8bfd5e5f8d20b5`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2008720f740687d6af827d98e0a17ac17c40265a0733232b3f65891cefd55ba4`  
		Last Modified: Sat, 16 Mar 2024 10:30:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:baf2f10adc34c6657b730c8bcf1d40afa9cbc5277bc79c1e4a35799ba08c4504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f61ca4d4044f9e7f21d7149dd863ef113c78738e2c3e84b2994e68fe5b7adda`

```dockerfile
```

-	Layers:
	-	`sha256:054cdb368dd44a8e73fdf9e940711c8c646cb1d917752910cfd489178cd1bd40`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e0b9862dbe39bc1e2f1598d956acc8877a83d8516baa2fe29261ecd8d5c16ed`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 19.4 KB (19370 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.19` - linux; s390x

```console
$ docker pull memcached@sha256:2bbbf6c60ae563e7fbf0b0d7fff645531ed4706dd6c6b783c35d4ecef1fd70d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4327559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a414e168eff8283c9d16f99e5c31558dec31c6b15ee761de45a40bb6839ee1cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
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
	-	`sha256:61064e5fd6e0cc6334b6eefff4fe163950d84c1de3c42ec9fdf85d92005f3ae9`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 970.1 KB (970135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f1d5965cdbebebdce4669474799f51b9ef3d6f42b376fa617a1b945d4d4325`  
		Last Modified: Sun, 17 Mar 2024 22:11:55 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23608093e2a154f293a6e3287a11ad798936c0146ae7f1943b035db32efa778b`  
		Last Modified: Sun, 17 Mar 2024 22:11:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:2dd2215c8ae081cddcbefef029e030b94e041ecd1f2e409d9f704ffdb720d99a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e50e27f5c06d319f5b8cc2b2ba76311d2d120269d1d9d22aa58ae531733001`

```dockerfile
```

-	Layers:
	-	`sha256:91ebf1e0392ad0faffa17054e66a85a7fb1aa0004495345cf4ed19fd5cfa0a6b`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f135346500525ff3a63124190a6511a8a7af0659061127048c4c9f62c219d119`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 19.3 KB (19301 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:bookworm`

```console
$ docker pull memcached@sha256:502113923d3c966943ae15105a43a8f09669f8e3d311b41ecf6d4844917c3eb2
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
$ docker pull memcached@sha256:f5d6b34b5e53f3c3efa1761e78a3ec1e48806b9cf323f275eb73f744ccecb592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38789552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5659585297ecca8269e4b42bf75ee0ba65573bc53f1ac844ce4442a41168219b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:01 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Tue, 12 Mar 2024 01:21:01 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f5b0c7d5ff100485df42c707b8f798c23491e3390670b6102ec309459c56e1`  
		Last Modified: Wed, 20 Mar 2024 21:53:21 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0347f087df5e5a5e55e4e61f495fb25766015d39f1a62d755e903df3f0a4b463`  
		Last Modified: Wed, 20 Mar 2024 21:53:22 GMT  
		Size: 2.5 MB (2488465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e3316b02adf5a1ede79c485a31043189f5e47f3f295394d2c0e8d4cde01c24`  
		Last Modified: Wed, 20 Mar 2024 21:53:21 GMT  
		Size: 7.2 MB (7175392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b72ea418779aaf6ffa3dcf321d061b13df238a88fcdd3f8d4a8e811f3f329f2`  
		Last Modified: Wed, 20 Mar 2024 21:53:21 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534937fe67d0636cc42a8284656ac23b9f0a138b3b912da0122025298ba0187e`  
		Last Modified: Wed, 20 Mar 2024 21:53:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:cdfdc5468a693b11d8b5e2c584c6b8167aca56f16bbef4a5c73f88e254f01849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3536051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c3d70d51d8c20eb5bffd2b9e173bf20449fb79a7c1f5dc4e067211a394bba7`

```dockerfile
```

-	Layers:
	-	`sha256:77f1295784ab211addd97298191a342ea0b5bc2ac83e5349eebc5752f9e00eda`  
		Last Modified: Wed, 20 Mar 2024 21:53:22 GMT  
		Size: 3.5 MB (3514934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:204bffe148afae4b974e13d601af8e712c6135452b18b6283a30fa1ffde6e69b`  
		Last Modified: Wed, 20 Mar 2024 21:53:21 GMT  
		Size: 21.1 KB (21117 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:2c0a8fd6a587a5d73f6afbc1fe07536b8a21f37ff8533ce389195c3f0ccfd62b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34811756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0041b5946d66d8e8b27a51ff5f1bb8d593ed96c761133d93788591b5ab21d8e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:48:31 GMT
ADD file:b1bd2ec7dd2a8894ea7b5837afba4e15ba798f4809586f0ac1b8855bd0032651 in / 
# Tue, 12 Mar 2024 00:48:31 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:64806d9455193063a6bd4aebf47380e94fad8313f6ad1b5d831882c453f43261`  
		Last Modified: Tue, 12 Mar 2024 00:51:39 GMT  
		Size: 26.9 MB (26884021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e32a50f75b9d40c50ce7692a0631af44e30f327e696aa5b28831455123c0d1`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a78498071cf34c7c6bcb0da9274a1a38c73fbb294d613cfac9c0100e903977`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 2.1 MB (2089476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36068ff9365ced1cbed88c3e977f60059201881a2482f8cf3f5d95de3212f48`  
		Last Modified: Wed, 20 Mar 2024 21:52:39 GMT  
		Size: 5.8 MB (5836746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf53231953d794bde70e2b7b7119a814be7bcedab1a665a0c94985ad91a5934`  
		Last Modified: Wed, 20 Mar 2024 21:52:39 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f512760eb47d5604a6a012660a82a055b5433c332a9ed9dbeff2acdf4e8c831e`  
		Last Modified: Wed, 20 Mar 2024 21:52:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f924932e4f06ee4421d9aa0c65781bc2d4e66b5b6921cd2701898c5f207cf5b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3506305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cc0ff8d1f5c499d166f30b882b9a756a9c801545de1080d663caeb2bb0f42db`

```dockerfile
```

-	Layers:
	-	`sha256:bfe76f7bb20909be4b9e643fa059225a1d9e992c6e123b3795bceaf5a7acc391`  
		Last Modified: Wed, 20 Mar 2024 21:52:39 GMT  
		Size: 3.5 MB (3485214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59b8882010ed55ddacd7b4a1329987ff2af9a2367d809d764e8e333d83cc9f4a`  
		Last Modified: Wed, 20 Mar 2024 21:52:38 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ccd988c5b8b64dd797254c5db351be97958404a16137214c5569c0ffd0081e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37688087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27728f0ab685b3a67c0f34a20d27afd4f5f137af0204c15e024a08ccb9689493`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac48a97998740def0fa8b1b7e818bbec003d87e56636ed14d66e8ea9c1b49c18`  
		Last Modified: Wed, 20 Mar 2024 22:05:32 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e6aa77c2974c982d56d398f0e7fde37261a6e629e0ae13bd38cbcfbc94d0f2`  
		Last Modified: Wed, 20 Mar 2024 22:05:33 GMT  
		Size: 2.3 MB (2346182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e87543748bdbe302f363c5c5ba30d5d2f7bddba6e8aa1b1492dbf60f97823f`  
		Last Modified: Wed, 20 Mar 2024 22:05:33 GMT  
		Size: 6.2 MB (6183961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fcc56c57aa721ad68c916103760548406b2f2ae78798ee219c5c037804554d3`  
		Last Modified: Wed, 20 Mar 2024 22:05:32 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad54eed22cbb0e5b0a76ceabcf728ab53a51c2d584ed743ca55c3f83749c7fb`  
		Last Modified: Wed, 20 Mar 2024 22:05:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:e311165ff6d518330323d445e95dd591ded261f129a6dfd3b9bba58349db9b26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3507065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3d95ab8f1447c9653180938a8afc4364a3d150c55a19bcc457e994da2deb96`

```dockerfile
```

-	Layers:
	-	`sha256:088471520c083942039c4a09387bdbef3ef68263c757673503b19844809bb1a8`  
		Last Modified: Wed, 20 Mar 2024 22:05:34 GMT  
		Size: 3.5 MB (3486097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daa3f98d4564330b08871a65867b9574becccd48cf8f34418e8e4e5007494a52`  
		Last Modified: Wed, 20 Mar 2024 22:05:32 GMT  
		Size: 21.0 KB (20968 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; 386

```console
$ docker pull memcached@sha256:f81e3f7f720aaf1482cc81d8bb3f063a146e5ed1fef7ffe54e62f36346a71b3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39272880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18bb6bb8ab561077858738067ab803ed63757a2c5f53e276936c40e1a4527aae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:57:59 GMT
ADD file:88f04d79dc9f1691544c636ff52d6744a2ff68d504793ea8034b797d0bfc6fd3 in / 
# Tue, 12 Mar 2024 00:58:00 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:576af7ffb10b3f3b8d5523e6b91da8667eb39393cdfd50fb26dfc178e504ba70`  
		Last Modified: Tue, 12 Mar 2024 01:02:43 GMT  
		Size: 30.1 MB (30141873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ca1e74787d7f5345fa4e48b3752fab05e59b0cc9269325db87012c10c20201`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c850abea3f675f18aec4a116fba49dae8f46e99f06997b55a6a2eed0636db316`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 2.5 MB (2492637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14fde32a1b90b6896eaf4e91a78b8f32edf62e2bde66ca3bdbf842d607182b63`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 6.6 MB (6636851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1abdc4ae20d60ffc06b6d337d69a65d0501dc932a9a31039f97854efd852c00c`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e56d15c7c18240ea35e93bd1fadf02ad9d12cf1d4168fc6347adda471053737`  
		Last Modified: Wed, 20 Mar 2024 21:53:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:1a82d1205f3b793796a0ce63454ba7a0e8439159d0cddbbdaa20a03103fa3b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3529875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb96cb648ee7c46e17e8193e254b792e2d16ab1dcd2944281ce40379f0ee1ed`

```dockerfile
```

-	Layers:
	-	`sha256:d0b36f1ef0868bd6a59e83aefd9d82a113291e6d8405938446ea789c06aaae64`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 3.5 MB (3508813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56aa96415543efa9a697197eaf5addc87d9d2eeed66dd1fa3b0821a739c733a7`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 21.1 KB (21062 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:19524094dd845883d46d265bc2c0e83abda00c944e71c65beeb688e1328aee22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37565245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1983e467da37a29b6a5ccc7f7dc4da935cad3d72f262f972d952995365d45623`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 01:06:19 GMT
ADD file:c03c59e261bb08f39e6a97df2fd4b82f1e11b49a62d1859a8f8efac680b80a88 in / 
# Tue, 12 Mar 2024 01:06:23 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aad79459a0f767fcded51c9547150a1cfd96638972389ab8621b5f3eb4a9c280`  
		Last Modified: Tue, 12 Mar 2024 01:17:09 GMT  
		Size: 29.1 MB (29119205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f9ce6b6ef9151bae2476ece2788ab3fcb6d9abf46076b3ab61890a8c5d25e3`  
		Last Modified: Wed, 20 Mar 2024 21:59:53 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4e0a67df5eca0e49eef014debfeb0680de1b95463963c1256e155e92c967a0`  
		Last Modified: Wed, 20 Mar 2024 21:59:54 GMT  
		Size: 1.9 MB (1937678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db0c438efebe0bbb19f79fa801c9c2c52655b590ac16a7196adc5d05702258e`  
		Last Modified: Wed, 20 Mar 2024 21:59:55 GMT  
		Size: 6.5 MB (6506842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97107982137a0d6d10cd7c2f2e613455871a16b69d19c544d26f5c9df4ef2d0`  
		Last Modified: Wed, 20 Mar 2024 21:59:54 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d2108a68b8f51c577db7aa9b41e3bc0507fa18834dc4e235303677021f369f`  
		Last Modified: Wed, 20 Mar 2024 21:59:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:dde4628406ffa6f2e54cdce761e8d050d342a45b4663463a5827ae0420ad7072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.0 KB (21003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ec8712d9cafb05213294e7c991f103858f9ccc5443c2a33560e9fefc5964e32`

```dockerfile
```

-	Layers:
	-	`sha256:ac6b20491333ea6e06cb55be035327040ed503fedd32e789ed3e8082ecaedf94`  
		Last Modified: Wed, 20 Mar 2024 21:59:54 GMT  
		Size: 21.0 KB (21003 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:4c3db32aa1a397cf2a03078efa95429139072b980ab1cfe1d38a3fc03e16b21b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (43006041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ea28ef1fe375457227b59ed4cffadfe2eb8c198795094bf26e6233bd556c8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:9273ef56d086dbc93b46b7e8ae424eb04096fb00c693dd6cda1f48346290d4d5 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c28cd0e276dcdeb4d44f5cc5bb958610750ff902a081b668e3863c2f38eef054`  
		Last Modified: Tue, 12 Mar 2024 00:38:06 GMT  
		Size: 33.1 MB (33119023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62aa36b84dc23bc5eecf52bd0d09534dcc186ab27089192c7aed8210f610e32`  
		Last Modified: Wed, 13 Mar 2024 02:14:26 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec1785cd98038ba62eb16a4aacec38cdbb91c26f98360aafb2ed1017cda3df8`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 2.7 MB (2698364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5105d8a1d382e8083f62216ad1a3ac3ed9e0dab0a2cd5110eb1afa516b084b`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 7.2 MB (7187142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356eaa328e166dd1628acf5a67acf74c032ae2b79667868199736be62871fcc9`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936d8dbc2ebbedc4ae8dc525f7a6ed2c953784d75251955a347e5cb1eab83a22`  
		Last Modified: Wed, 13 Mar 2024 02:14:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:7ba7fc566a7ca1cc4ee19a4562d3c8ff3cbd5c66504843364b286c16a51c673a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3521676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e456fccef08393cbfaa927989c957a984aca49d5b68aff7e43a60bebf063443e`

```dockerfile
```

-	Layers:
	-	`sha256:40dd29e81bcfdcdc7a12cb2843f9bc037c7633d5502e7d49aeab7f1a38b351d1`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 3.5 MB (3500658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1acb5997eff88a90491a6c619d8236c97c1febf8bf3b8fce15b91660a29910df`  
		Last Modified: Wed, 13 Mar 2024 02:14:26 GMT  
		Size: 21.0 KB (21018 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:6ba3af09c6f41f8a8aeb75f0b92546ff342929150d6da315f2c1152c2ac8b89c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35721763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3b0f99b55b9844b9cf7f544669c714d836ca78200a54ea085af430fa58934e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:54:02 GMT
ADD file:80ab985d4871ca6a72156bedfe1038e6b1a89591fc2fd86c4ef778d293223aff in / 
# Tue, 12 Mar 2024 00:54:03 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9cada496cd2b8a88571bf23d513e7fce34888d13321fcf23c6613bffe4c37297`  
		Last Modified: Tue, 12 Mar 2024 01:21:14 GMT  
		Size: 27.5 MB (27488684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c430faffa085700d40355ac1aea08d429376e112bef3b9c00780b1ede56859c2`  
		Last Modified: Wed, 20 Mar 2024 22:17:08 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf1db148a80e9f25b06fe946c697ba8fa83bc46c13515904d4ceceaeb2a4eeb`  
		Last Modified: Wed, 20 Mar 2024 22:17:12 GMT  
		Size: 2.2 MB (2152657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf95ab69cc340a00b9e21b620561903f3f26a245d421506febe9e3c376310098`  
		Last Modified: Wed, 20 Mar 2024 22:17:09 GMT  
		Size: 6.1 MB (6078907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5304ac9e894c6780910c4bd4889d1cc407cb62e54cc4940d8bc7fa74efbb9699`  
		Last Modified: Wed, 20 Mar 2024 22:17:09 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:722d63b783293116e31d9ac81edb640d7218dbb304e2efdc0c1d48aed76e12d2`  
		Last Modified: Wed, 20 Mar 2024 22:17:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:6b3778c79df56c62c44f402a80b924fdb3a5c869694053bff124b8f232640d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bcc8294911dfe44976e400bf92d4e2bee63c8bd56170c94ca2b3c3b05c59135`

```dockerfile
```

-	Layers:
	-	`sha256:e43c6eaae62edc62c95fce6ffd315f1d7c3c249e703a751b4f13b92dba078b59`  
		Last Modified: Wed, 20 Mar 2024 22:17:09 GMT  
		Size: 3.5 MB (3503203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a25398f94b500655282b6629c187cb91a22c84327a970fdcecacda3d14b74649`  
		Last Modified: Wed, 20 Mar 2024 22:17:08 GMT  
		Size: 21.1 KB (21075 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:latest`

```console
$ docker pull memcached@sha256:502113923d3c966943ae15105a43a8f09669f8e3d311b41ecf6d4844917c3eb2
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
$ docker pull memcached@sha256:f5d6b34b5e53f3c3efa1761e78a3ec1e48806b9cf323f275eb73f744ccecb592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38789552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5659585297ecca8269e4b42bf75ee0ba65573bc53f1ac844ce4442a41168219b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:01 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Tue, 12 Mar 2024 01:21:01 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f5b0c7d5ff100485df42c707b8f798c23491e3390670b6102ec309459c56e1`  
		Last Modified: Wed, 20 Mar 2024 21:53:21 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0347f087df5e5a5e55e4e61f495fb25766015d39f1a62d755e903df3f0a4b463`  
		Last Modified: Wed, 20 Mar 2024 21:53:22 GMT  
		Size: 2.5 MB (2488465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e3316b02adf5a1ede79c485a31043189f5e47f3f295394d2c0e8d4cde01c24`  
		Last Modified: Wed, 20 Mar 2024 21:53:21 GMT  
		Size: 7.2 MB (7175392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b72ea418779aaf6ffa3dcf321d061b13df238a88fcdd3f8d4a8e811f3f329f2`  
		Last Modified: Wed, 20 Mar 2024 21:53:21 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534937fe67d0636cc42a8284656ac23b9f0a138b3b912da0122025298ba0187e`  
		Last Modified: Wed, 20 Mar 2024 21:53:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:cdfdc5468a693b11d8b5e2c584c6b8167aca56f16bbef4a5c73f88e254f01849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3536051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c3d70d51d8c20eb5bffd2b9e173bf20449fb79a7c1f5dc4e067211a394bba7`

```dockerfile
```

-	Layers:
	-	`sha256:77f1295784ab211addd97298191a342ea0b5bc2ac83e5349eebc5752f9e00eda`  
		Last Modified: Wed, 20 Mar 2024 21:53:22 GMT  
		Size: 3.5 MB (3514934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:204bffe148afae4b974e13d601af8e712c6135452b18b6283a30fa1ffde6e69b`  
		Last Modified: Wed, 20 Mar 2024 21:53:21 GMT  
		Size: 21.1 KB (21117 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:2c0a8fd6a587a5d73f6afbc1fe07536b8a21f37ff8533ce389195c3f0ccfd62b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34811756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0041b5946d66d8e8b27a51ff5f1bb8d593ed96c761133d93788591b5ab21d8e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:48:31 GMT
ADD file:b1bd2ec7dd2a8894ea7b5837afba4e15ba798f4809586f0ac1b8855bd0032651 in / 
# Tue, 12 Mar 2024 00:48:31 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:64806d9455193063a6bd4aebf47380e94fad8313f6ad1b5d831882c453f43261`  
		Last Modified: Tue, 12 Mar 2024 00:51:39 GMT  
		Size: 26.9 MB (26884021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e32a50f75b9d40c50ce7692a0631af44e30f327e696aa5b28831455123c0d1`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a78498071cf34c7c6bcb0da9274a1a38c73fbb294d613cfac9c0100e903977`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 2.1 MB (2089476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36068ff9365ced1cbed88c3e977f60059201881a2482f8cf3f5d95de3212f48`  
		Last Modified: Wed, 20 Mar 2024 21:52:39 GMT  
		Size: 5.8 MB (5836746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf53231953d794bde70e2b7b7119a814be7bcedab1a665a0c94985ad91a5934`  
		Last Modified: Wed, 20 Mar 2024 21:52:39 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f512760eb47d5604a6a012660a82a055b5433c332a9ed9dbeff2acdf4e8c831e`  
		Last Modified: Wed, 20 Mar 2024 21:52:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:f924932e4f06ee4421d9aa0c65781bc2d4e66b5b6921cd2701898c5f207cf5b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3506305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cc0ff8d1f5c499d166f30b882b9a756a9c801545de1080d663caeb2bb0f42db`

```dockerfile
```

-	Layers:
	-	`sha256:bfe76f7bb20909be4b9e643fa059225a1d9e992c6e123b3795bceaf5a7acc391`  
		Last Modified: Wed, 20 Mar 2024 21:52:39 GMT  
		Size: 3.5 MB (3485214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59b8882010ed55ddacd7b4a1329987ff2af9a2367d809d764e8e333d83cc9f4a`  
		Last Modified: Wed, 20 Mar 2024 21:52:38 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ccd988c5b8b64dd797254c5db351be97958404a16137214c5569c0ffd0081e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37688087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27728f0ab685b3a67c0f34a20d27afd4f5f137af0204c15e024a08ccb9689493`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac48a97998740def0fa8b1b7e818bbec003d87e56636ed14d66e8ea9c1b49c18`  
		Last Modified: Wed, 20 Mar 2024 22:05:32 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e6aa77c2974c982d56d398f0e7fde37261a6e629e0ae13bd38cbcfbc94d0f2`  
		Last Modified: Wed, 20 Mar 2024 22:05:33 GMT  
		Size: 2.3 MB (2346182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e87543748bdbe302f363c5c5ba30d5d2f7bddba6e8aa1b1492dbf60f97823f`  
		Last Modified: Wed, 20 Mar 2024 22:05:33 GMT  
		Size: 6.2 MB (6183961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fcc56c57aa721ad68c916103760548406b2f2ae78798ee219c5c037804554d3`  
		Last Modified: Wed, 20 Mar 2024 22:05:32 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad54eed22cbb0e5b0a76ceabcf728ab53a51c2d584ed743ca55c3f83749c7fb`  
		Last Modified: Wed, 20 Mar 2024 22:05:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:e311165ff6d518330323d445e95dd591ded261f129a6dfd3b9bba58349db9b26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3507065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3d95ab8f1447c9653180938a8afc4364a3d150c55a19bcc457e994da2deb96`

```dockerfile
```

-	Layers:
	-	`sha256:088471520c083942039c4a09387bdbef3ef68263c757673503b19844809bb1a8`  
		Last Modified: Wed, 20 Mar 2024 22:05:34 GMT  
		Size: 3.5 MB (3486097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daa3f98d4564330b08871a65867b9574becccd48cf8f34418e8e4e5007494a52`  
		Last Modified: Wed, 20 Mar 2024 22:05:32 GMT  
		Size: 21.0 KB (20968 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:f81e3f7f720aaf1482cc81d8bb3f063a146e5ed1fef7ffe54e62f36346a71b3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39272880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18bb6bb8ab561077858738067ab803ed63757a2c5f53e276936c40e1a4527aae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:57:59 GMT
ADD file:88f04d79dc9f1691544c636ff52d6744a2ff68d504793ea8034b797d0bfc6fd3 in / 
# Tue, 12 Mar 2024 00:58:00 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:576af7ffb10b3f3b8d5523e6b91da8667eb39393cdfd50fb26dfc178e504ba70`  
		Last Modified: Tue, 12 Mar 2024 01:02:43 GMT  
		Size: 30.1 MB (30141873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ca1e74787d7f5345fa4e48b3752fab05e59b0cc9269325db87012c10c20201`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c850abea3f675f18aec4a116fba49dae8f46e99f06997b55a6a2eed0636db316`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 2.5 MB (2492637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14fde32a1b90b6896eaf4e91a78b8f32edf62e2bde66ca3bdbf842d607182b63`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 6.6 MB (6636851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1abdc4ae20d60ffc06b6d337d69a65d0501dc932a9a31039f97854efd852c00c`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e56d15c7c18240ea35e93bd1fadf02ad9d12cf1d4168fc6347adda471053737`  
		Last Modified: Wed, 20 Mar 2024 21:53:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:1a82d1205f3b793796a0ce63454ba7a0e8439159d0cddbbdaa20a03103fa3b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3529875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb96cb648ee7c46e17e8193e254b792e2d16ab1dcd2944281ce40379f0ee1ed`

```dockerfile
```

-	Layers:
	-	`sha256:d0b36f1ef0868bd6a59e83aefd9d82a113291e6d8405938446ea789c06aaae64`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 3.5 MB (3508813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56aa96415543efa9a697197eaf5addc87d9d2eeed66dd1fa3b0821a739c733a7`  
		Last Modified: Wed, 20 Mar 2024 21:53:34 GMT  
		Size: 21.1 KB (21062 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; mips64le

```console
$ docker pull memcached@sha256:19524094dd845883d46d265bc2c0e83abda00c944e71c65beeb688e1328aee22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37565245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1983e467da37a29b6a5ccc7f7dc4da935cad3d72f262f972d952995365d45623`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 01:06:19 GMT
ADD file:c03c59e261bb08f39e6a97df2fd4b82f1e11b49a62d1859a8f8efac680b80a88 in / 
# Tue, 12 Mar 2024 01:06:23 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aad79459a0f767fcded51c9547150a1cfd96638972389ab8621b5f3eb4a9c280`  
		Last Modified: Tue, 12 Mar 2024 01:17:09 GMT  
		Size: 29.1 MB (29119205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f9ce6b6ef9151bae2476ece2788ab3fcb6d9abf46076b3ab61890a8c5d25e3`  
		Last Modified: Wed, 20 Mar 2024 21:59:53 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4e0a67df5eca0e49eef014debfeb0680de1b95463963c1256e155e92c967a0`  
		Last Modified: Wed, 20 Mar 2024 21:59:54 GMT  
		Size: 1.9 MB (1937678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db0c438efebe0bbb19f79fa801c9c2c52655b590ac16a7196adc5d05702258e`  
		Last Modified: Wed, 20 Mar 2024 21:59:55 GMT  
		Size: 6.5 MB (6506842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97107982137a0d6d10cd7c2f2e613455871a16b69d19c544d26f5c9df4ef2d0`  
		Last Modified: Wed, 20 Mar 2024 21:59:54 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d2108a68b8f51c577db7aa9b41e3bc0507fa18834dc4e235303677021f369f`  
		Last Modified: Wed, 20 Mar 2024 21:59:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:dde4628406ffa6f2e54cdce761e8d050d342a45b4663463a5827ae0420ad7072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.0 KB (21003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ec8712d9cafb05213294e7c991f103858f9ccc5443c2a33560e9fefc5964e32`

```dockerfile
```

-	Layers:
	-	`sha256:ac6b20491333ea6e06cb55be035327040ed503fedd32e789ed3e8082ecaedf94`  
		Last Modified: Wed, 20 Mar 2024 21:59:54 GMT  
		Size: 21.0 KB (21003 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:4c3db32aa1a397cf2a03078efa95429139072b980ab1cfe1d38a3fc03e16b21b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (43006041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ea28ef1fe375457227b59ed4cffadfe2eb8c198795094bf26e6233bd556c8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:9273ef56d086dbc93b46b7e8ae424eb04096fb00c693dd6cda1f48346290d4d5 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c28cd0e276dcdeb4d44f5cc5bb958610750ff902a081b668e3863c2f38eef054`  
		Last Modified: Tue, 12 Mar 2024 00:38:06 GMT  
		Size: 33.1 MB (33119023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62aa36b84dc23bc5eecf52bd0d09534dcc186ab27089192c7aed8210f610e32`  
		Last Modified: Wed, 13 Mar 2024 02:14:26 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec1785cd98038ba62eb16a4aacec38cdbb91c26f98360aafb2ed1017cda3df8`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 2.7 MB (2698364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5105d8a1d382e8083f62216ad1a3ac3ed9e0dab0a2cd5110eb1afa516b084b`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 7.2 MB (7187142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356eaa328e166dd1628acf5a67acf74c032ae2b79667868199736be62871fcc9`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936d8dbc2ebbedc4ae8dc525f7a6ed2c953784d75251955a347e5cb1eab83a22`  
		Last Modified: Wed, 13 Mar 2024 02:14:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:7ba7fc566a7ca1cc4ee19a4562d3c8ff3cbd5c66504843364b286c16a51c673a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3521676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e456fccef08393cbfaa927989c957a984aca49d5b68aff7e43a60bebf063443e`

```dockerfile
```

-	Layers:
	-	`sha256:40dd29e81bcfdcdc7a12cb2843f9bc037c7633d5502e7d49aeab7f1a38b351d1`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 3.5 MB (3500658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1acb5997eff88a90491a6c619d8236c97c1febf8bf3b8fce15b91660a29910df`  
		Last Modified: Wed, 13 Mar 2024 02:14:26 GMT  
		Size: 21.0 KB (21018 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:6ba3af09c6f41f8a8aeb75f0b92546ff342929150d6da315f2c1152c2ac8b89c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35721763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3b0f99b55b9844b9cf7f544669c714d836ca78200a54ea085af430fa58934e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:54:02 GMT
ADD file:80ab985d4871ca6a72156bedfe1038e6b1a89591fc2fd86c4ef778d293223aff in / 
# Tue, 12 Mar 2024 00:54:03 GMT
CMD ["bash"]
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_VERSION=1.6.25
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.25.tar.gz
# Wed, 20 Mar 2024 00:54:13 GMT
ENV MEMCACHED_SHA1=8825b31936100c90439d2447182ca2d49ecca9a0
# Wed, 20 Mar 2024 00:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 20 Mar 2024 00:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 00:54:13 GMT
USER memcache
# Wed, 20 Mar 2024 00:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 20 Mar 2024 00:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9cada496cd2b8a88571bf23d513e7fce34888d13321fcf23c6613bffe4c37297`  
		Last Modified: Tue, 12 Mar 2024 01:21:14 GMT  
		Size: 27.5 MB (27488684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c430faffa085700d40355ac1aea08d429376e112bef3b9c00780b1ede56859c2`  
		Last Modified: Wed, 20 Mar 2024 22:17:08 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf1db148a80e9f25b06fe946c697ba8fa83bc46c13515904d4ceceaeb2a4eeb`  
		Last Modified: Wed, 20 Mar 2024 22:17:12 GMT  
		Size: 2.2 MB (2152657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf95ab69cc340a00b9e21b620561903f3f26a245d421506febe9e3c376310098`  
		Last Modified: Wed, 20 Mar 2024 22:17:09 GMT  
		Size: 6.1 MB (6078907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5304ac9e894c6780910c4bd4889d1cc407cb62e54cc4940d8bc7fa74efbb9699`  
		Last Modified: Wed, 20 Mar 2024 22:17:09 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:722d63b783293116e31d9ac81edb640d7218dbb304e2efdc0c1d48aed76e12d2`  
		Last Modified: Wed, 20 Mar 2024 22:17:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:6b3778c79df56c62c44f402a80b924fdb3a5c869694053bff124b8f232640d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bcc8294911dfe44976e400bf92d4e2bee63c8bd56170c94ca2b3c3b05c59135`

```dockerfile
```

-	Layers:
	-	`sha256:e43c6eaae62edc62c95fce6ffd315f1d7c3c249e703a751b4f13b92dba078b59`  
		Last Modified: Wed, 20 Mar 2024 22:17:09 GMT  
		Size: 3.5 MB (3503203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a25398f94b500655282b6629c187cb91a22c84327a970fdcecacda3d14b74649`  
		Last Modified: Wed, 20 Mar 2024 22:17:08 GMT  
		Size: 21.1 KB (21075 bytes)  
		MIME: application/vnd.in-toto+json
