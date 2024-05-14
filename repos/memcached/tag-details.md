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
-	[`memcached:1.6.27`](#memcached1627)
-	[`memcached:1.6.27-alpine`](#memcached1627-alpine)
-	[`memcached:1.6.27-alpine3.19`](#memcached1627-alpine319)
-	[`memcached:1.6.27-bookworm`](#memcached1627-bookworm)
-	[`memcached:alpine`](#memcachedalpine)
-	[`memcached:alpine3.19`](#memcachedalpine319)
-	[`memcached:bookworm`](#memcachedbookworm)
-	[`memcached:latest`](#memcachedlatest)

## `memcached:1`

```console
$ docker pull memcached@sha256:2585b867c96c722e5f4b9d3986a64b3ad67b956f55e31fdf4469f1e5dc157bdc
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
$ docker pull memcached@sha256:29dde2f0a4b996fa7684041ce78bb31e7c2b1a9c8aa6abe467364e8215c57035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38691245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec8c94e66592eab160b4534afad21e21800362694048e80f2c8e82b20c060a78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105cdbf392f0d274b354ff593187bc8b5c883e9087567f7ae4974eea189e7847`  
		Last Modified: Mon, 06 May 2024 23:08:23 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ef4162d3aae0771395e4e1b7ce0c5431fc5fbf987c9c410b7e5b959e302a40`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 2.5 MB (2488488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be957db0d2fe09ea0c4fe874c335ee65f4a0a268476fbc1e646c611ca6b0b1f8`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 7.1 MB (7050761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028dbe498f2fd4131b262e14a863a793bb71221f0cc5b9488822c6a1bb1b0c8c`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7239ceaa87f6c0fc3415c2d6d064020f0b8d2427a548364ecbde0f044094cfdb`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:dce70377f5e30a5563e4d8507edfff7f8947a7575b6ebfe7283407d9fcce4458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c9ef74fba5a31fccf3f549b4fd48b6c4db07bef69a0e574ecb6e9c5bc37448a`

```dockerfile
```

-	Layers:
	-	`sha256:67f37454203d55985eef3fd618246f415a13be9dd32f789dc93d5ee36efcd7e2`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 2.3 MB (2261261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1481c59e0b769395485e713e760e5b60c337edf6600a053a98eaacdcb4a121eb`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 21.1 KB (21146 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v5

```console
$ docker pull memcached@sha256:d04280085fd0255be4cf80a6c19c28266f51615eddfe506d718c588dd762a01c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.9 MB (34885683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac68380af8a0798b278fdebe3bfeaf85e0f6d53f505d959ae42ae2eb4de89c15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:53:11 GMT
ADD file:0140ab9be4171f94aae33901f189ffd8822ce6da4a052798883fd66d03b79be9 in / 
# Wed, 24 Apr 2024 03:53:12 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2c9444d4d8a989f4536a8afd8b41a3461ede5b15d490d87c3369b051095d7ae3`  
		Last Modified: Wed, 24 Apr 2024 03:56:28 GMT  
		Size: 26.9 MB (26910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad3b02f635c19a5c749474c01db78c0d1bd9f6465178c236ac42079364c167e`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c82b33e3a41551599953fed1e04a047e0a017d6de973951e88a2319d4eb3b5`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 2.1 MB (2089520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f05e3ac287ed1762995abf279872754c6f943b51b3f1a25e8a2a4b17c08657`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 5.9 MB (5884617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764bff9a4b0a489e9c8c1102b502bf6142559e169252ba08d486d8f0a5b60c90`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e968f84d0f8d617f917f72762217ea784201f4dbd8d958e7c679479a25500e22`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:6bfcd444a59b433ecbc80cb2f9ce87fc6ec5ebc6e20d69b79ab258a8df83d8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1b6d39e43bcacaafbba90473dd410c5e07008c7b5e8f6c5e0053a1cd81e4d2`

```dockerfile
```

-	Layers:
	-	`sha256:d15574302d09f987aff6a1dd074dfa1a5bcf39d50d2488e2bf25204432517fce`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 2.3 MB (2264549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcb55f3be2aa40dd40b859884d496c08b3c104f6782ea068c88df7430c224b5b`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 21.1 KB (21119 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:dcb3196cd0eaf5593a642df75f5c68b0962b89335e489c41d2bd2f50106b2990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.5 MB (38539477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:453e18c2977a4810fadaaeefd26b1cc5b3ddf8aea9a337463475b66a7eb5cf3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea3b2534cc10b3982041c25f3e3e46bc54885fb85a56a850e5d87825605d959`  
		Last Modified: Mon, 06 May 2024 23:40:33 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8c0c56b8ceb323ad11adf63e3d67d815207d779b691a1e144ecbbc509a56c6`  
		Last Modified: Mon, 06 May 2024 23:40:34 GMT  
		Size: 2.3 MB (2346198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b93f0391bd3380825799bef11d6a6236d36dd2a538fddf37ffe5eb89f606aa`  
		Last Modified: Mon, 06 May 2024 23:40:34 GMT  
		Size: 7.0 MB (7011826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5b9d9447753339dd1b2be478d2d2153513530b8476657fe41a93507ac389b2`  
		Last Modified: Mon, 06 May 2024 23:40:33 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd2e6309ee48b90c1469e3408f664e9277e5a348c13026648488c2ac26abc3e`  
		Last Modified: Mon, 06 May 2024 23:40:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:12c2959e59ca59159b3810394cf53899988571d57d4df9c4f0c63950fda39f80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c238d1722683e731e558126fa120d76c1f59a8c0e1fc8cdf25fadb97937810b6`

```dockerfile
```

-	Layers:
	-	`sha256:a23cc33f240eaa7b71c6e81fd3a50f2ba3a4c5c20de8d43766527e3f3cc40832`  
		Last Modified: Mon, 06 May 2024 23:40:34 GMT  
		Size: 2.3 MB (2261490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bc0c2167dc9c0dce55a2cb122d4d7721644ccca44d35b0906c74bac6eb00bfc`  
		Last Modified: Mon, 06 May 2024 23:40:33 GMT  
		Size: 21.0 KB (20997 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:3f542cc336b40813213949d5eb8e2da1a57005f88566c0d51c3b8624cc911916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33914242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a44cb325942314e83e433868ace554ffea1c0ef303993f238620f928b36bbcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa82d06bb0cba58ed3fae5da8ee9c6248a027c9d105f1c1e2094d1973ab2f78`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf14cdbfbd6ea1d7231b4119cb6c85336718c7ccee9bc57573aadcc210f05e2`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 2.5 MB (2492686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bed32b6d0ec7a40384a2ba4d5fa14871afba5fd572025e99ebc3c30541ee6bf`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 1.3 MB (1257406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07ba6ac3de2271f181cd17c67b57573da49f54d516ad3c852a2610d138c85b3`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a700f395f10bfe9002c02677754b0a58c0ee8ca0f1fc73477ef1b86dc734103b`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:8932028ec9d6cdd607a57df36f524623a045c35db7110aa26040859db5599b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303c5c842506ac0858dd708f266252ee2b586ba9dd6f506ef93e95c9d4d06402`

```dockerfile
```

-	Layers:
	-	`sha256:e55268858bc5b4c5b04534306d270b5c41b3d3dccd563cae845878933e3d7a1c`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 2.3 MB (2258359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4afdfadae6d39596deea4cc7598059a6d7cdd84a4bf4036bfd609cacb9347c22`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; mips64le

```console
$ docker pull memcached@sha256:54a6cf440988b85512b266a181d2e83efe8a6a16530029f48b2fd002efb2e251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38171114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac4ac5a7759abeb1658c052e8e13a0cdc6e05c7af62e12528e0d65428805b7b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:14:18 GMT
ADD file:a3e63beab80160854bfc2d48f69e7c70a9542cdfaf3c5b50f1d6248a998b75ae in / 
# Wed, 24 Apr 2024 03:14:22 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af25825be002e7bdd52bf28c2fbef5bae0ba9fcef8118e5591a874e7a70b2a62`  
		Last Modified: Wed, 24 Apr 2024 03:25:20 GMT  
		Size: 29.1 MB (29144174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70b69867f90cc0cd6ccf8b72f07ee05c80179a59283d6ce971d9191eaf11afe`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361f75ee595f0c436f725a5dd64b1009cb0da358d19361f68345abf27c392f03`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 1.9 MB (1937740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1d3e5a5aad136d9ada8e95bd8e9f609baf923df5c9a48a8021e50206e4e93d`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 7.1 MB (7087680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913b327051e93299424d31038856dead21e1781ab1e47927437d8d135ea97338`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a025835eff1c0dfdae38dce98ddefd33f8609362934acbc3106f445279e8b050`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:062ba12de9ac3ea604948fc8045fa1f18254e15045b75fd40ba397ca49ddac94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f78c9e4c785d57060d12fdc33b3579dde0c50533361c63c38632718921c39d`

```dockerfile
```

-	Layers:
	-	`sha256:0f87aa3b54f1e190b0d04cc9d1960d4d745a6c99015f572091bc1c532c971e12`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:00e8c12c53be74f05f1d407b5e6d79dc9f3c03eaf6bcc42d7fde84b55135c65b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43803388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c5835d941db2f784baf56126916def72cb031f8bf87f0eb9c85d38ab2a99006`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:13 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Wed, 24 Apr 2024 03:21:15 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7fcd02d677f7b314809120f00d6b081965b5807827188e6ebf3081436f54c9`  
		Last Modified: Mon, 06 May 2024 23:36:28 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7857db5dc94e4b30fbaed58c503c6aa7cf416363b6ebd7bfe4eb21d81bd3d54e`  
		Last Modified: Mon, 06 May 2024 23:36:29 GMT  
		Size: 2.7 MB (2698389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4129214713c04309f826d05e9dead290efde58d33f38bf8cc51796ce3d02392`  
		Last Modified: Mon, 06 May 2024 23:36:29 GMT  
		Size: 8.0 MB (7962280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009ed91ac73d01b73721c2c68710b06d4067d836af63780f5260d075df4cfa57`  
		Last Modified: Mon, 06 May 2024 23:36:29 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db194260f1714761a294b97e37fb2d51544c26f4447b3ff81009b1a9a07cd992`  
		Last Modified: Mon, 06 May 2024 23:36:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:577d80832f1718d990d4526e62c1abfd9b09fe17643600c30a82b75a5a0ad018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842a6e10e139ec873043472602e0301d3b0e0d09e7123af5c4739b4da4d20616`

```dockerfile
```

-	Layers:
	-	`sha256:0f8c1c8dfeeac8f6c9be4a58fec56319cd72fb7e52b664e29d21a1f603698b5f`  
		Last Modified: Mon, 06 May 2024 23:36:29 GMT  
		Size: 2.3 MB (2265632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c9b981b4bff189bd3a4d6c0d3c9a51794ea3d75674dc37ed4a0c88494b1d553`  
		Last Modified: Mon, 06 May 2024 23:36:29 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:f1eded0e1e184f274872c917b0898ea33d458ce85cf84dcfdd7fd612ccf43f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35763592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13d7f11723a6c3c0292b7fc87542450d38bec719b123b35792a28d4f0ee5cc3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:43:18 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Wed, 24 Apr 2024 03:43:21 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
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
	-	`sha256:31591ca6b7d175a856e1a87b1fcdba950a0189086a123e820f1638b43fd955e6`  
		Last Modified: Mon, 06 May 2024 23:39:10 GMT  
		Size: 6.1 MB (6097067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf96459eefa11b754c53ffaa240db16c5e7ca96d1187924dadb4717e9001079`  
		Last Modified: Mon, 06 May 2024 23:39:10 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c2b7746d8228729836f11aa3c212bc49ad4769651a8d03525966c158e0e828`  
		Last Modified: Mon, 06 May 2024 23:39:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:38c86b4cfae8572747cee6ca551e6e8e82e52321c96c1c8d178e87febf12857b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09d6f045f1e26176704badc902459105cc38b94d2b84961f936773844e9df075`

```dockerfile
```

-	Layers:
	-	`sha256:bb75dfb1e8a87ed594faee6dfd29fe3744905435891a990c608d532312e5c908`  
		Last Modified: Mon, 06 May 2024 23:39:10 GMT  
		Size: 2.3 MB (2261082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b711f312fd8f0ae434954fd2d919960b4b8522210024b2611eb5af0b5de5414`  
		Last Modified: Mon, 06 May 2024 23:39:10 GMT  
		Size: 21.0 KB (20979 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:4ee2d6582442b4920f0c9de6565947a81e18abc48089804df10251eedf388d66
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
$ docker pull memcached@sha256:cf854f636d506c0834dc1159ad5b472fea96028e88702014088384915a7c08dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6535198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21047320ccba2e62e0ee66c1ffa169149658e039ee012547c37ed6aa0130ad2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59605d18a5ec7e6531bd08f0238da758082d075c4fdd6a4ec8c00fd6f792425b`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8691b75405b7042ea4a853223cc80432131a0e21745f3baf9b21b00073207ace`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 104.2 KB (104211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8925d4d8379f9d71921da012b62d23d71f826e429777c701a1b0d4d56d0399ac`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 3.0 MB (3020613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86013193f6f292637e997c2518f84ab28fec9d7a494cda4090d07457058f10de`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cfe77bbca77075d0b682e8546bca4d6d045cfbff0be0336d51b7bbe1116983`  
		Last Modified: Mon, 06 May 2024 23:08:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d4a846cbc9f47d5db83dbb38f019064556e6af28dad33264b1f851bebbb2858b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ab3ae8df84416fe4351914e6bb061214bfad4b0cb01537aef674b02c008994`

```dockerfile
```

-	Layers:
	-	`sha256:59634fa6bbcc5be09a70b3894761425c9ea7b231a189445bce9ae40b97f09675`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2fd487a2e71a464ab83cce092819d041b742e29af0ecb901bcb36ac21fc7c2c`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 19.5 KB (19475 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:8a6f18eb424270a1dca99143a613014d570cb7376c9cb7d212b72d74c569b12a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6381171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ddcb41c8f4d78c4720e1ad02b3c978ef7af38607d717e52219f0c53ab6fb64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859f5f148ebb49ed2dfc712d036c8e1162fd5c08307e622f420c9e722f459c15`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a85abddca9696d1381e2dbbf52914e6119f22bd22e71c1ffc49aa385ca2d79`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 120.9 KB (120900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f80774db5f2d9cd2ec4f0bf8e7256768ab2ff5b90e1a822c70e5fb0a8d0a42`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 2.9 MB (2910908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fff6ea9e3e8e56264cef5ba1ceaacc5db1aa37fb687bf4cb684629a462a4e04`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e6b3e687f63ee869e2595d746eecfc9a9a64e49c7972eea118f9af26f3a02f`  
		Last Modified: Mon, 06 May 2024 23:43:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7677dd609f55b7dac25e997d7fc4942f1b433f1084ca54e71a01175c8608fedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce1cbd3428e47f29034986dc018cfef4ed121b030aef195db0d03c8a65cc79d`

```dockerfile
```

-	Layers:
	-	`sha256:c80e817fe71d2bd7ff1d9709ab1ac3d7ac30315b7cfd1b528ca1c316fecabc2f`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b568b0dd9cb0ef2428bd10a39e9ee3afe06fe97f6911abc8c1ae5e642b27094`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 19.3 KB (19326 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:1557e39ed6b5f943d53c54797d59f4ea27755c53c9e7004cbfb633c08757abd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6194136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48e3a30b8d39f2e6434ff10c1130366a5bfeac640bc8ecb88f89e6e996cdc4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c853f4fd5c9ee2e18e52b4399ccc43726449928a43d040161f83d3f67f596dd`  
		Last Modified: Mon, 06 May 2024 23:08:35 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca2d91782956c7a9591fd3f9edb724367e6a2770f04a809c6088a8ea623ea7f`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 109.3 KB (109328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5c07db0e07d757431d4458ea14990c3cc0b06aa9577b0e29f8db33fc51921b`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 2.8 MB (2839076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21633262023f9a6ae09f480b39a8a9a7109a0201b779ccdba90e721204cb20ae`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893c3463887c0e33218f5af72fe7534fe9bebd41fd26e976944bbd03c13a9d22`  
		Last Modified: Mon, 06 May 2024 23:08:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:4184448ad3b3ff9a34654847c26c9ad677ce54b07e8a96eedb429e8c509fe5e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04225924b78526836b6ef1d8f4bd3d25e994e9f858bedc4d73fbf5308500d074`

```dockerfile
```

-	Layers:
	-	`sha256:562178e7885ee7492a868cc754c309fe7cf0a52b74299dc570dc9959ecfc0c10`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d1f3d52b695ee750a517e356c17e9f3b6a3778f607f791f558ae9e31397df3f`  
		Last Modified: Mon, 06 May 2024 23:08:35 GMT  
		Size: 19.4 KB (19420 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:4b1fdeda480d0b679c2b9fa5a09c508dabaf7bf0bf1600d0078fcae81e004dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6407037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf112675855fb5780056fbde79f0822c329da1cfb19ca47270289ec2ac966e77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25735f744a453fbf0af2d088f79a0fa6de45cc2699601389d42141b2de2f21d3`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a61320e5e6694b8436a4074ba6280369b9b29e2474231252683fa11606b8e6`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 123.4 KB (123401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e809f0a1acfe802b3158bb0d4d370427885e8c5ba2ce6b98549da9bbac597e`  
		Last Modified: Mon, 06 May 2024 23:39:16 GMT  
		Size: 2.9 MB (2923638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99dc3c24ef4a44c763efcf66a6e3e44d31d723683dd339c343770bd43523007`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0b13828c450ce09acf99d42e4d9e625dbc1991b6f87a5727ff595e3e62a06c`  
		Last Modified: Mon, 06 May 2024 23:39:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d1dc50ec127cc25ab5b90bbe3fccaf4c5cda1379629dcd1760fa93b6cab32718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7934a2d41084621a7a7ff3aafbea88a9edfb76ded1149d611483fb61826d661`

```dockerfile
```

-	Layers:
	-	`sha256:dedf3264102cee8df6c9d7e964dedede98ab6b3865d8df8f76e88eeb42290632`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b25fbb2f936e2b3483885e59398fdcffdf62a984c55d6171eb02b6a8b6ef44d7`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 19.4 KB (19376 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:16979dbfdc08cb52efcfffcdfdff35be32426e49b90065b36155882be545d88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6151853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cca463729a03d73b6abb17295ed77bc6a13a336b4bc01a3b1c03a176f34fa06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
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
	-	`sha256:37d6a06c9130de338c39b57baed51f1e62b01cf60bb33a109ac31927ab8c775f`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 2.8 MB (2794432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db042a56f7b2a4ea616aa34e4b563284ea5d38557c0ff85c04706fc945bc905`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e7dbc7d250abc9822b7e752e47c8b83dd404648d74f9331600b392ac836970`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b885694442ff65cade16142bde9307eda742f797b4c4e48b95e2ecd62c262746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023ebbf730f939171a6dd74509e836130fe404e073174c8b1be5b28fd09e514e`

```dockerfile
```

-	Layers:
	-	`sha256:b18acb410267cb31ce209d09681474ba43f18c2f4af00288845c4061bd220974`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48c7d2c81f6bbcf60c7bbca78ec3114f620154531205c592fe14d252cb9daf08`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 19.3 KB (19309 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine3.19`

```console
$ docker pull memcached@sha256:4ee2d6582442b4920f0c9de6565947a81e18abc48089804df10251eedf388d66
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
$ docker pull memcached@sha256:cf854f636d506c0834dc1159ad5b472fea96028e88702014088384915a7c08dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6535198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21047320ccba2e62e0ee66c1ffa169149658e039ee012547c37ed6aa0130ad2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59605d18a5ec7e6531bd08f0238da758082d075c4fdd6a4ec8c00fd6f792425b`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8691b75405b7042ea4a853223cc80432131a0e21745f3baf9b21b00073207ace`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 104.2 KB (104211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8925d4d8379f9d71921da012b62d23d71f826e429777c701a1b0d4d56d0399ac`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 3.0 MB (3020613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86013193f6f292637e997c2518f84ab28fec9d7a494cda4090d07457058f10de`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cfe77bbca77075d0b682e8546bca4d6d045cfbff0be0336d51b7bbe1116983`  
		Last Modified: Mon, 06 May 2024 23:08:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:d4a846cbc9f47d5db83dbb38f019064556e6af28dad33264b1f851bebbb2858b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ab3ae8df84416fe4351914e6bb061214bfad4b0cb01537aef674b02c008994`

```dockerfile
```

-	Layers:
	-	`sha256:59634fa6bbcc5be09a70b3894761425c9ea7b231a189445bce9ae40b97f09675`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2fd487a2e71a464ab83cce092819d041b742e29af0ecb901bcb36ac21fc7c2c`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 19.5 KB (19475 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:8a6f18eb424270a1dca99143a613014d570cb7376c9cb7d212b72d74c569b12a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6381171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ddcb41c8f4d78c4720e1ad02b3c978ef7af38607d717e52219f0c53ab6fb64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859f5f148ebb49ed2dfc712d036c8e1162fd5c08307e622f420c9e722f459c15`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a85abddca9696d1381e2dbbf52914e6119f22bd22e71c1ffc49aa385ca2d79`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 120.9 KB (120900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f80774db5f2d9cd2ec4f0bf8e7256768ab2ff5b90e1a822c70e5fb0a8d0a42`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 2.9 MB (2910908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fff6ea9e3e8e56264cef5ba1ceaacc5db1aa37fb687bf4cb684629a462a4e04`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e6b3e687f63ee869e2595d746eecfc9a9a64e49c7972eea118f9af26f3a02f`  
		Last Modified: Mon, 06 May 2024 23:43:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:7677dd609f55b7dac25e997d7fc4942f1b433f1084ca54e71a01175c8608fedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce1cbd3428e47f29034986dc018cfef4ed121b030aef195db0d03c8a65cc79d`

```dockerfile
```

-	Layers:
	-	`sha256:c80e817fe71d2bd7ff1d9709ab1ac3d7ac30315b7cfd1b528ca1c316fecabc2f`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b568b0dd9cb0ef2428bd10a39e9ee3afe06fe97f6911abc8c1ae5e642b27094`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 19.3 KB (19326 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.19` - linux; 386

```console
$ docker pull memcached@sha256:1557e39ed6b5f943d53c54797d59f4ea27755c53c9e7004cbfb633c08757abd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6194136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48e3a30b8d39f2e6434ff10c1130366a5bfeac640bc8ecb88f89e6e996cdc4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c853f4fd5c9ee2e18e52b4399ccc43726449928a43d040161f83d3f67f596dd`  
		Last Modified: Mon, 06 May 2024 23:08:35 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca2d91782956c7a9591fd3f9edb724367e6a2770f04a809c6088a8ea623ea7f`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 109.3 KB (109328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5c07db0e07d757431d4458ea14990c3cc0b06aa9577b0e29f8db33fc51921b`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 2.8 MB (2839076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21633262023f9a6ae09f480b39a8a9a7109a0201b779ccdba90e721204cb20ae`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893c3463887c0e33218f5af72fe7534fe9bebd41fd26e976944bbd03c13a9d22`  
		Last Modified: Mon, 06 May 2024 23:08:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:4184448ad3b3ff9a34654847c26c9ad677ce54b07e8a96eedb429e8c509fe5e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04225924b78526836b6ef1d8f4bd3d25e994e9f858bedc4d73fbf5308500d074`

```dockerfile
```

-	Layers:
	-	`sha256:562178e7885ee7492a868cc754c309fe7cf0a52b74299dc570dc9959ecfc0c10`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d1f3d52b695ee750a517e356c17e9f3b6a3778f607f791f558ae9e31397df3f`  
		Last Modified: Mon, 06 May 2024 23:08:35 GMT  
		Size: 19.4 KB (19420 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.19` - linux; ppc64le

```console
$ docker pull memcached@sha256:4b1fdeda480d0b679c2b9fa5a09c508dabaf7bf0bf1600d0078fcae81e004dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6407037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf112675855fb5780056fbde79f0822c329da1cfb19ca47270289ec2ac966e77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25735f744a453fbf0af2d088f79a0fa6de45cc2699601389d42141b2de2f21d3`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a61320e5e6694b8436a4074ba6280369b9b29e2474231252683fa11606b8e6`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 123.4 KB (123401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e809f0a1acfe802b3158bb0d4d370427885e8c5ba2ce6b98549da9bbac597e`  
		Last Modified: Mon, 06 May 2024 23:39:16 GMT  
		Size: 2.9 MB (2923638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99dc3c24ef4a44c763efcf66a6e3e44d31d723683dd339c343770bd43523007`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0b13828c450ce09acf99d42e4d9e625dbc1991b6f87a5727ff595e3e62a06c`  
		Last Modified: Mon, 06 May 2024 23:39:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:d1dc50ec127cc25ab5b90bbe3fccaf4c5cda1379629dcd1760fa93b6cab32718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7934a2d41084621a7a7ff3aafbea88a9edfb76ded1149d611483fb61826d661`

```dockerfile
```

-	Layers:
	-	`sha256:dedf3264102cee8df6c9d7e964dedede98ab6b3865d8df8f76e88eeb42290632`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b25fbb2f936e2b3483885e59398fdcffdf62a984c55d6171eb02b6a8b6ef44d7`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 19.4 KB (19376 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.19` - linux; s390x

```console
$ docker pull memcached@sha256:16979dbfdc08cb52efcfffcdfdff35be32426e49b90065b36155882be545d88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6151853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cca463729a03d73b6abb17295ed77bc6a13a336b4bc01a3b1c03a176f34fa06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
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
	-	`sha256:37d6a06c9130de338c39b57baed51f1e62b01cf60bb33a109ac31927ab8c775f`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 2.8 MB (2794432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db042a56f7b2a4ea616aa34e4b563284ea5d38557c0ff85c04706fc945bc905`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e7dbc7d250abc9822b7e752e47c8b83dd404648d74f9331600b392ac836970`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:b885694442ff65cade16142bde9307eda742f797b4c4e48b95e2ecd62c262746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023ebbf730f939171a6dd74509e836130fe404e073174c8b1be5b28fd09e514e`

```dockerfile
```

-	Layers:
	-	`sha256:b18acb410267cb31ce209d09681474ba43f18c2f4af00288845c4061bd220974`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48c7d2c81f6bbcf60c7bbca78ec3114f620154531205c592fe14d252cb9daf08`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 19.3 KB (19309 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-bookworm`

```console
$ docker pull memcached@sha256:2585b867c96c722e5f4b9d3986a64b3ad67b956f55e31fdf4469f1e5dc157bdc
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
$ docker pull memcached@sha256:29dde2f0a4b996fa7684041ce78bb31e7c2b1a9c8aa6abe467364e8215c57035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38691245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec8c94e66592eab160b4534afad21e21800362694048e80f2c8e82b20c060a78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105cdbf392f0d274b354ff593187bc8b5c883e9087567f7ae4974eea189e7847`  
		Last Modified: Mon, 06 May 2024 23:08:23 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ef4162d3aae0771395e4e1b7ce0c5431fc5fbf987c9c410b7e5b959e302a40`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 2.5 MB (2488488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be957db0d2fe09ea0c4fe874c335ee65f4a0a268476fbc1e646c611ca6b0b1f8`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 7.1 MB (7050761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028dbe498f2fd4131b262e14a863a793bb71221f0cc5b9488822c6a1bb1b0c8c`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7239ceaa87f6c0fc3415c2d6d064020f0b8d2427a548364ecbde0f044094cfdb`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:dce70377f5e30a5563e4d8507edfff7f8947a7575b6ebfe7283407d9fcce4458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c9ef74fba5a31fccf3f549b4fd48b6c4db07bef69a0e574ecb6e9c5bc37448a`

```dockerfile
```

-	Layers:
	-	`sha256:67f37454203d55985eef3fd618246f415a13be9dd32f789dc93d5ee36efcd7e2`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 2.3 MB (2261261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1481c59e0b769395485e713e760e5b60c337edf6600a053a98eaacdcb4a121eb`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 21.1 KB (21146 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:d04280085fd0255be4cf80a6c19c28266f51615eddfe506d718c588dd762a01c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.9 MB (34885683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac68380af8a0798b278fdebe3bfeaf85e0f6d53f505d959ae42ae2eb4de89c15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:53:11 GMT
ADD file:0140ab9be4171f94aae33901f189ffd8822ce6da4a052798883fd66d03b79be9 in / 
# Wed, 24 Apr 2024 03:53:12 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2c9444d4d8a989f4536a8afd8b41a3461ede5b15d490d87c3369b051095d7ae3`  
		Last Modified: Wed, 24 Apr 2024 03:56:28 GMT  
		Size: 26.9 MB (26910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad3b02f635c19a5c749474c01db78c0d1bd9f6465178c236ac42079364c167e`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c82b33e3a41551599953fed1e04a047e0a017d6de973951e88a2319d4eb3b5`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 2.1 MB (2089520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f05e3ac287ed1762995abf279872754c6f943b51b3f1a25e8a2a4b17c08657`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 5.9 MB (5884617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764bff9a4b0a489e9c8c1102b502bf6142559e169252ba08d486d8f0a5b60c90`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e968f84d0f8d617f917f72762217ea784201f4dbd8d958e7c679479a25500e22`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:6bfcd444a59b433ecbc80cb2f9ce87fc6ec5ebc6e20d69b79ab258a8df83d8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1b6d39e43bcacaafbba90473dd410c5e07008c7b5e8f6c5e0053a1cd81e4d2`

```dockerfile
```

-	Layers:
	-	`sha256:d15574302d09f987aff6a1dd074dfa1a5bcf39d50d2488e2bf25204432517fce`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 2.3 MB (2264549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcb55f3be2aa40dd40b859884d496c08b3c104f6782ea068c88df7430c224b5b`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 21.1 KB (21119 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:dcb3196cd0eaf5593a642df75f5c68b0962b89335e489c41d2bd2f50106b2990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.5 MB (38539477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:453e18c2977a4810fadaaeefd26b1cc5b3ddf8aea9a337463475b66a7eb5cf3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea3b2534cc10b3982041c25f3e3e46bc54885fb85a56a850e5d87825605d959`  
		Last Modified: Mon, 06 May 2024 23:40:33 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8c0c56b8ceb323ad11adf63e3d67d815207d779b691a1e144ecbbc509a56c6`  
		Last Modified: Mon, 06 May 2024 23:40:34 GMT  
		Size: 2.3 MB (2346198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b93f0391bd3380825799bef11d6a6236d36dd2a538fddf37ffe5eb89f606aa`  
		Last Modified: Mon, 06 May 2024 23:40:34 GMT  
		Size: 7.0 MB (7011826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5b9d9447753339dd1b2be478d2d2153513530b8476657fe41a93507ac389b2`  
		Last Modified: Mon, 06 May 2024 23:40:33 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd2e6309ee48b90c1469e3408f664e9277e5a348c13026648488c2ac26abc3e`  
		Last Modified: Mon, 06 May 2024 23:40:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:12c2959e59ca59159b3810394cf53899988571d57d4df9c4f0c63950fda39f80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c238d1722683e731e558126fa120d76c1f59a8c0e1fc8cdf25fadb97937810b6`

```dockerfile
```

-	Layers:
	-	`sha256:a23cc33f240eaa7b71c6e81fd3a50f2ba3a4c5c20de8d43766527e3f3cc40832`  
		Last Modified: Mon, 06 May 2024 23:40:34 GMT  
		Size: 2.3 MB (2261490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bc0c2167dc9c0dce55a2cb122d4d7721644ccca44d35b0906c74bac6eb00bfc`  
		Last Modified: Mon, 06 May 2024 23:40:33 GMT  
		Size: 21.0 KB (20997 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:3f542cc336b40813213949d5eb8e2da1a57005f88566c0d51c3b8624cc911916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33914242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a44cb325942314e83e433868ace554ffea1c0ef303993f238620f928b36bbcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa82d06bb0cba58ed3fae5da8ee9c6248a027c9d105f1c1e2094d1973ab2f78`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf14cdbfbd6ea1d7231b4119cb6c85336718c7ccee9bc57573aadcc210f05e2`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 2.5 MB (2492686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bed32b6d0ec7a40384a2ba4d5fa14871afba5fd572025e99ebc3c30541ee6bf`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 1.3 MB (1257406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07ba6ac3de2271f181cd17c67b57573da49f54d516ad3c852a2610d138c85b3`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a700f395f10bfe9002c02677754b0a58c0ee8ca0f1fc73477ef1b86dc734103b`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:8932028ec9d6cdd607a57df36f524623a045c35db7110aa26040859db5599b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303c5c842506ac0858dd708f266252ee2b586ba9dd6f506ef93e95c9d4d06402`

```dockerfile
```

-	Layers:
	-	`sha256:e55268858bc5b4c5b04534306d270b5c41b3d3dccd563cae845878933e3d7a1c`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 2.3 MB (2258359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4afdfadae6d39596deea4cc7598059a6d7cdd84a4bf4036bfd609cacb9347c22`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:54a6cf440988b85512b266a181d2e83efe8a6a16530029f48b2fd002efb2e251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38171114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac4ac5a7759abeb1658c052e8e13a0cdc6e05c7af62e12528e0d65428805b7b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:14:18 GMT
ADD file:a3e63beab80160854bfc2d48f69e7c70a9542cdfaf3c5b50f1d6248a998b75ae in / 
# Wed, 24 Apr 2024 03:14:22 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af25825be002e7bdd52bf28c2fbef5bae0ba9fcef8118e5591a874e7a70b2a62`  
		Last Modified: Wed, 24 Apr 2024 03:25:20 GMT  
		Size: 29.1 MB (29144174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70b69867f90cc0cd6ccf8b72f07ee05c80179a59283d6ce971d9191eaf11afe`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361f75ee595f0c436f725a5dd64b1009cb0da358d19361f68345abf27c392f03`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 1.9 MB (1937740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1d3e5a5aad136d9ada8e95bd8e9f609baf923df5c9a48a8021e50206e4e93d`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 7.1 MB (7087680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913b327051e93299424d31038856dead21e1781ab1e47927437d8d135ea97338`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a025835eff1c0dfdae38dce98ddefd33f8609362934acbc3106f445279e8b050`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:062ba12de9ac3ea604948fc8045fa1f18254e15045b75fd40ba397ca49ddac94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f78c9e4c785d57060d12fdc33b3579dde0c50533361c63c38632718921c39d`

```dockerfile
```

-	Layers:
	-	`sha256:0f87aa3b54f1e190b0d04cc9d1960d4d745a6c99015f572091bc1c532c971e12`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:00e8c12c53be74f05f1d407b5e6d79dc9f3c03eaf6bcc42d7fde84b55135c65b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43803388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c5835d941db2f784baf56126916def72cb031f8bf87f0eb9c85d38ab2a99006`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:13 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Wed, 24 Apr 2024 03:21:15 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7fcd02d677f7b314809120f00d6b081965b5807827188e6ebf3081436f54c9`  
		Last Modified: Mon, 06 May 2024 23:36:28 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7857db5dc94e4b30fbaed58c503c6aa7cf416363b6ebd7bfe4eb21d81bd3d54e`  
		Last Modified: Mon, 06 May 2024 23:36:29 GMT  
		Size: 2.7 MB (2698389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4129214713c04309f826d05e9dead290efde58d33f38bf8cc51796ce3d02392`  
		Last Modified: Mon, 06 May 2024 23:36:29 GMT  
		Size: 8.0 MB (7962280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009ed91ac73d01b73721c2c68710b06d4067d836af63780f5260d075df4cfa57`  
		Last Modified: Mon, 06 May 2024 23:36:29 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db194260f1714761a294b97e37fb2d51544c26f4447b3ff81009b1a9a07cd992`  
		Last Modified: Mon, 06 May 2024 23:36:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:577d80832f1718d990d4526e62c1abfd9b09fe17643600c30a82b75a5a0ad018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842a6e10e139ec873043472602e0301d3b0e0d09e7123af5c4739b4da4d20616`

```dockerfile
```

-	Layers:
	-	`sha256:0f8c1c8dfeeac8f6c9be4a58fec56319cd72fb7e52b664e29d21a1f603698b5f`  
		Last Modified: Mon, 06 May 2024 23:36:29 GMT  
		Size: 2.3 MB (2265632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c9b981b4bff189bd3a4d6c0d3c9a51794ea3d75674dc37ed4a0c88494b1d553`  
		Last Modified: Mon, 06 May 2024 23:36:29 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:f1eded0e1e184f274872c917b0898ea33d458ce85cf84dcfdd7fd612ccf43f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35763592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13d7f11723a6c3c0292b7fc87542450d38bec719b123b35792a28d4f0ee5cc3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:43:18 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Wed, 24 Apr 2024 03:43:21 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
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
	-	`sha256:31591ca6b7d175a856e1a87b1fcdba950a0189086a123e820f1638b43fd955e6`  
		Last Modified: Mon, 06 May 2024 23:39:10 GMT  
		Size: 6.1 MB (6097067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf96459eefa11b754c53ffaa240db16c5e7ca96d1187924dadb4717e9001079`  
		Last Modified: Mon, 06 May 2024 23:39:10 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c2b7746d8228729836f11aa3c212bc49ad4769651a8d03525966c158e0e828`  
		Last Modified: Mon, 06 May 2024 23:39:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:38c86b4cfae8572747cee6ca551e6e8e82e52321c96c1c8d178e87febf12857b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09d6f045f1e26176704badc902459105cc38b94d2b84961f936773844e9df075`

```dockerfile
```

-	Layers:
	-	`sha256:bb75dfb1e8a87ed594faee6dfd29fe3744905435891a990c608d532312e5c908`  
		Last Modified: Mon, 06 May 2024 23:39:10 GMT  
		Size: 2.3 MB (2261082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b711f312fd8f0ae434954fd2d919960b4b8522210024b2611eb5af0b5de5414`  
		Last Modified: Mon, 06 May 2024 23:39:10 GMT  
		Size: 21.0 KB (20979 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6`

```console
$ docker pull memcached@sha256:2585b867c96c722e5f4b9d3986a64b3ad67b956f55e31fdf4469f1e5dc157bdc
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
$ docker pull memcached@sha256:29dde2f0a4b996fa7684041ce78bb31e7c2b1a9c8aa6abe467364e8215c57035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38691245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec8c94e66592eab160b4534afad21e21800362694048e80f2c8e82b20c060a78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105cdbf392f0d274b354ff593187bc8b5c883e9087567f7ae4974eea189e7847`  
		Last Modified: Mon, 06 May 2024 23:08:23 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ef4162d3aae0771395e4e1b7ce0c5431fc5fbf987c9c410b7e5b959e302a40`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 2.5 MB (2488488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be957db0d2fe09ea0c4fe874c335ee65f4a0a268476fbc1e646c611ca6b0b1f8`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 7.1 MB (7050761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028dbe498f2fd4131b262e14a863a793bb71221f0cc5b9488822c6a1bb1b0c8c`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7239ceaa87f6c0fc3415c2d6d064020f0b8d2427a548364ecbde0f044094cfdb`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:dce70377f5e30a5563e4d8507edfff7f8947a7575b6ebfe7283407d9fcce4458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c9ef74fba5a31fccf3f549b4fd48b6c4db07bef69a0e574ecb6e9c5bc37448a`

```dockerfile
```

-	Layers:
	-	`sha256:67f37454203d55985eef3fd618246f415a13be9dd32f789dc93d5ee36efcd7e2`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 2.3 MB (2261261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1481c59e0b769395485e713e760e5b60c337edf6600a053a98eaacdcb4a121eb`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 21.1 KB (21146 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:d04280085fd0255be4cf80a6c19c28266f51615eddfe506d718c588dd762a01c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.9 MB (34885683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac68380af8a0798b278fdebe3bfeaf85e0f6d53f505d959ae42ae2eb4de89c15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:53:11 GMT
ADD file:0140ab9be4171f94aae33901f189ffd8822ce6da4a052798883fd66d03b79be9 in / 
# Wed, 24 Apr 2024 03:53:12 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2c9444d4d8a989f4536a8afd8b41a3461ede5b15d490d87c3369b051095d7ae3`  
		Last Modified: Wed, 24 Apr 2024 03:56:28 GMT  
		Size: 26.9 MB (26910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad3b02f635c19a5c749474c01db78c0d1bd9f6465178c236ac42079364c167e`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c82b33e3a41551599953fed1e04a047e0a017d6de973951e88a2319d4eb3b5`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 2.1 MB (2089520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f05e3ac287ed1762995abf279872754c6f943b51b3f1a25e8a2a4b17c08657`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 5.9 MB (5884617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764bff9a4b0a489e9c8c1102b502bf6142559e169252ba08d486d8f0a5b60c90`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e968f84d0f8d617f917f72762217ea784201f4dbd8d958e7c679479a25500e22`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:6bfcd444a59b433ecbc80cb2f9ce87fc6ec5ebc6e20d69b79ab258a8df83d8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1b6d39e43bcacaafbba90473dd410c5e07008c7b5e8f6c5e0053a1cd81e4d2`

```dockerfile
```

-	Layers:
	-	`sha256:d15574302d09f987aff6a1dd074dfa1a5bcf39d50d2488e2bf25204432517fce`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 2.3 MB (2264549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcb55f3be2aa40dd40b859884d496c08b3c104f6782ea068c88df7430c224b5b`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 21.1 KB (21119 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:dcb3196cd0eaf5593a642df75f5c68b0962b89335e489c41d2bd2f50106b2990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.5 MB (38539477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:453e18c2977a4810fadaaeefd26b1cc5b3ddf8aea9a337463475b66a7eb5cf3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea3b2534cc10b3982041c25f3e3e46bc54885fb85a56a850e5d87825605d959`  
		Last Modified: Mon, 06 May 2024 23:40:33 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8c0c56b8ceb323ad11adf63e3d67d815207d779b691a1e144ecbbc509a56c6`  
		Last Modified: Mon, 06 May 2024 23:40:34 GMT  
		Size: 2.3 MB (2346198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b93f0391bd3380825799bef11d6a6236d36dd2a538fddf37ffe5eb89f606aa`  
		Last Modified: Mon, 06 May 2024 23:40:34 GMT  
		Size: 7.0 MB (7011826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5b9d9447753339dd1b2be478d2d2153513530b8476657fe41a93507ac389b2`  
		Last Modified: Mon, 06 May 2024 23:40:33 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd2e6309ee48b90c1469e3408f664e9277e5a348c13026648488c2ac26abc3e`  
		Last Modified: Mon, 06 May 2024 23:40:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:12c2959e59ca59159b3810394cf53899988571d57d4df9c4f0c63950fda39f80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c238d1722683e731e558126fa120d76c1f59a8c0e1fc8cdf25fadb97937810b6`

```dockerfile
```

-	Layers:
	-	`sha256:a23cc33f240eaa7b71c6e81fd3a50f2ba3a4c5c20de8d43766527e3f3cc40832`  
		Last Modified: Mon, 06 May 2024 23:40:34 GMT  
		Size: 2.3 MB (2261490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bc0c2167dc9c0dce55a2cb122d4d7721644ccca44d35b0906c74bac6eb00bfc`  
		Last Modified: Mon, 06 May 2024 23:40:33 GMT  
		Size: 21.0 KB (20997 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; 386

```console
$ docker pull memcached@sha256:3f542cc336b40813213949d5eb8e2da1a57005f88566c0d51c3b8624cc911916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33914242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a44cb325942314e83e433868ace554ffea1c0ef303993f238620f928b36bbcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa82d06bb0cba58ed3fae5da8ee9c6248a027c9d105f1c1e2094d1973ab2f78`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf14cdbfbd6ea1d7231b4119cb6c85336718c7ccee9bc57573aadcc210f05e2`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 2.5 MB (2492686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bed32b6d0ec7a40384a2ba4d5fa14871afba5fd572025e99ebc3c30541ee6bf`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 1.3 MB (1257406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07ba6ac3de2271f181cd17c67b57573da49f54d516ad3c852a2610d138c85b3`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a700f395f10bfe9002c02677754b0a58c0ee8ca0f1fc73477ef1b86dc734103b`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:8932028ec9d6cdd607a57df36f524623a045c35db7110aa26040859db5599b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303c5c842506ac0858dd708f266252ee2b586ba9dd6f506ef93e95c9d4d06402`

```dockerfile
```

-	Layers:
	-	`sha256:e55268858bc5b4c5b04534306d270b5c41b3d3dccd563cae845878933e3d7a1c`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 2.3 MB (2258359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4afdfadae6d39596deea4cc7598059a6d7cdd84a4bf4036bfd609cacb9347c22`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; mips64le

```console
$ docker pull memcached@sha256:54a6cf440988b85512b266a181d2e83efe8a6a16530029f48b2fd002efb2e251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38171114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac4ac5a7759abeb1658c052e8e13a0cdc6e05c7af62e12528e0d65428805b7b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:14:18 GMT
ADD file:a3e63beab80160854bfc2d48f69e7c70a9542cdfaf3c5b50f1d6248a998b75ae in / 
# Wed, 24 Apr 2024 03:14:22 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af25825be002e7bdd52bf28c2fbef5bae0ba9fcef8118e5591a874e7a70b2a62`  
		Last Modified: Wed, 24 Apr 2024 03:25:20 GMT  
		Size: 29.1 MB (29144174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70b69867f90cc0cd6ccf8b72f07ee05c80179a59283d6ce971d9191eaf11afe`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361f75ee595f0c436f725a5dd64b1009cb0da358d19361f68345abf27c392f03`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 1.9 MB (1937740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1d3e5a5aad136d9ada8e95bd8e9f609baf923df5c9a48a8021e50206e4e93d`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 7.1 MB (7087680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913b327051e93299424d31038856dead21e1781ab1e47927437d8d135ea97338`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a025835eff1c0dfdae38dce98ddefd33f8609362934acbc3106f445279e8b050`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:062ba12de9ac3ea604948fc8045fa1f18254e15045b75fd40ba397ca49ddac94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f78c9e4c785d57060d12fdc33b3579dde0c50533361c63c38632718921c39d`

```dockerfile
```

-	Layers:
	-	`sha256:0f87aa3b54f1e190b0d04cc9d1960d4d745a6c99015f572091bc1c532c971e12`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:00e8c12c53be74f05f1d407b5e6d79dc9f3c03eaf6bcc42d7fde84b55135c65b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43803388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c5835d941db2f784baf56126916def72cb031f8bf87f0eb9c85d38ab2a99006`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:13 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Wed, 24 Apr 2024 03:21:15 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7fcd02d677f7b314809120f00d6b081965b5807827188e6ebf3081436f54c9`  
		Last Modified: Mon, 06 May 2024 23:36:28 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7857db5dc94e4b30fbaed58c503c6aa7cf416363b6ebd7bfe4eb21d81bd3d54e`  
		Last Modified: Mon, 06 May 2024 23:36:29 GMT  
		Size: 2.7 MB (2698389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4129214713c04309f826d05e9dead290efde58d33f38bf8cc51796ce3d02392`  
		Last Modified: Mon, 06 May 2024 23:36:29 GMT  
		Size: 8.0 MB (7962280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009ed91ac73d01b73721c2c68710b06d4067d836af63780f5260d075df4cfa57`  
		Last Modified: Mon, 06 May 2024 23:36:29 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db194260f1714761a294b97e37fb2d51544c26f4447b3ff81009b1a9a07cd992`  
		Last Modified: Mon, 06 May 2024 23:36:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:577d80832f1718d990d4526e62c1abfd9b09fe17643600c30a82b75a5a0ad018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842a6e10e139ec873043472602e0301d3b0e0d09e7123af5c4739b4da4d20616`

```dockerfile
```

-	Layers:
	-	`sha256:0f8c1c8dfeeac8f6c9be4a58fec56319cd72fb7e52b664e29d21a1f603698b5f`  
		Last Modified: Mon, 06 May 2024 23:36:29 GMT  
		Size: 2.3 MB (2265632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c9b981b4bff189bd3a4d6c0d3c9a51794ea3d75674dc37ed4a0c88494b1d553`  
		Last Modified: Mon, 06 May 2024 23:36:29 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; s390x

```console
$ docker pull memcached@sha256:f1eded0e1e184f274872c917b0898ea33d458ce85cf84dcfdd7fd612ccf43f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35763592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13d7f11723a6c3c0292b7fc87542450d38bec719b123b35792a28d4f0ee5cc3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:43:18 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Wed, 24 Apr 2024 03:43:21 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
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
	-	`sha256:31591ca6b7d175a856e1a87b1fcdba950a0189086a123e820f1638b43fd955e6`  
		Last Modified: Mon, 06 May 2024 23:39:10 GMT  
		Size: 6.1 MB (6097067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf96459eefa11b754c53ffaa240db16c5e7ca96d1187924dadb4717e9001079`  
		Last Modified: Mon, 06 May 2024 23:39:10 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c2b7746d8228729836f11aa3c212bc49ad4769651a8d03525966c158e0e828`  
		Last Modified: Mon, 06 May 2024 23:39:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:38c86b4cfae8572747cee6ca551e6e8e82e52321c96c1c8d178e87febf12857b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09d6f045f1e26176704badc902459105cc38b94d2b84961f936773844e9df075`

```dockerfile
```

-	Layers:
	-	`sha256:bb75dfb1e8a87ed594faee6dfd29fe3744905435891a990c608d532312e5c908`  
		Last Modified: Mon, 06 May 2024 23:39:10 GMT  
		Size: 2.3 MB (2261082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b711f312fd8f0ae434954fd2d919960b4b8522210024b2611eb5af0b5de5414`  
		Last Modified: Mon, 06 May 2024 23:39:10 GMT  
		Size: 21.0 KB (20979 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine`

```console
$ docker pull memcached@sha256:4ee2d6582442b4920f0c9de6565947a81e18abc48089804df10251eedf388d66
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
$ docker pull memcached@sha256:cf854f636d506c0834dc1159ad5b472fea96028e88702014088384915a7c08dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6535198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21047320ccba2e62e0ee66c1ffa169149658e039ee012547c37ed6aa0130ad2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59605d18a5ec7e6531bd08f0238da758082d075c4fdd6a4ec8c00fd6f792425b`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8691b75405b7042ea4a853223cc80432131a0e21745f3baf9b21b00073207ace`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 104.2 KB (104211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8925d4d8379f9d71921da012b62d23d71f826e429777c701a1b0d4d56d0399ac`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 3.0 MB (3020613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86013193f6f292637e997c2518f84ab28fec9d7a494cda4090d07457058f10de`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cfe77bbca77075d0b682e8546bca4d6d045cfbff0be0336d51b7bbe1116983`  
		Last Modified: Mon, 06 May 2024 23:08:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d4a846cbc9f47d5db83dbb38f019064556e6af28dad33264b1f851bebbb2858b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ab3ae8df84416fe4351914e6bb061214bfad4b0cb01537aef674b02c008994`

```dockerfile
```

-	Layers:
	-	`sha256:59634fa6bbcc5be09a70b3894761425c9ea7b231a189445bce9ae40b97f09675`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2fd487a2e71a464ab83cce092819d041b742e29af0ecb901bcb36ac21fc7c2c`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 19.5 KB (19475 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:8a6f18eb424270a1dca99143a613014d570cb7376c9cb7d212b72d74c569b12a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6381171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ddcb41c8f4d78c4720e1ad02b3c978ef7af38607d717e52219f0c53ab6fb64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859f5f148ebb49ed2dfc712d036c8e1162fd5c08307e622f420c9e722f459c15`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a85abddca9696d1381e2dbbf52914e6119f22bd22e71c1ffc49aa385ca2d79`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 120.9 KB (120900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f80774db5f2d9cd2ec4f0bf8e7256768ab2ff5b90e1a822c70e5fb0a8d0a42`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 2.9 MB (2910908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fff6ea9e3e8e56264cef5ba1ceaacc5db1aa37fb687bf4cb684629a462a4e04`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e6b3e687f63ee869e2595d746eecfc9a9a64e49c7972eea118f9af26f3a02f`  
		Last Modified: Mon, 06 May 2024 23:43:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7677dd609f55b7dac25e997d7fc4942f1b433f1084ca54e71a01175c8608fedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce1cbd3428e47f29034986dc018cfef4ed121b030aef195db0d03c8a65cc79d`

```dockerfile
```

-	Layers:
	-	`sha256:c80e817fe71d2bd7ff1d9709ab1ac3d7ac30315b7cfd1b528ca1c316fecabc2f`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b568b0dd9cb0ef2428bd10a39e9ee3afe06fe97f6911abc8c1ae5e642b27094`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 19.3 KB (19326 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:1557e39ed6b5f943d53c54797d59f4ea27755c53c9e7004cbfb633c08757abd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6194136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48e3a30b8d39f2e6434ff10c1130366a5bfeac640bc8ecb88f89e6e996cdc4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c853f4fd5c9ee2e18e52b4399ccc43726449928a43d040161f83d3f67f596dd`  
		Last Modified: Mon, 06 May 2024 23:08:35 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca2d91782956c7a9591fd3f9edb724367e6a2770f04a809c6088a8ea623ea7f`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 109.3 KB (109328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5c07db0e07d757431d4458ea14990c3cc0b06aa9577b0e29f8db33fc51921b`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 2.8 MB (2839076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21633262023f9a6ae09f480b39a8a9a7109a0201b779ccdba90e721204cb20ae`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893c3463887c0e33218f5af72fe7534fe9bebd41fd26e976944bbd03c13a9d22`  
		Last Modified: Mon, 06 May 2024 23:08:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:4184448ad3b3ff9a34654847c26c9ad677ce54b07e8a96eedb429e8c509fe5e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04225924b78526836b6ef1d8f4bd3d25e994e9f858bedc4d73fbf5308500d074`

```dockerfile
```

-	Layers:
	-	`sha256:562178e7885ee7492a868cc754c309fe7cf0a52b74299dc570dc9959ecfc0c10`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d1f3d52b695ee750a517e356c17e9f3b6a3778f607f791f558ae9e31397df3f`  
		Last Modified: Mon, 06 May 2024 23:08:35 GMT  
		Size: 19.4 KB (19420 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:4b1fdeda480d0b679c2b9fa5a09c508dabaf7bf0bf1600d0078fcae81e004dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6407037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf112675855fb5780056fbde79f0822c329da1cfb19ca47270289ec2ac966e77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25735f744a453fbf0af2d088f79a0fa6de45cc2699601389d42141b2de2f21d3`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a61320e5e6694b8436a4074ba6280369b9b29e2474231252683fa11606b8e6`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 123.4 KB (123401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e809f0a1acfe802b3158bb0d4d370427885e8c5ba2ce6b98549da9bbac597e`  
		Last Modified: Mon, 06 May 2024 23:39:16 GMT  
		Size: 2.9 MB (2923638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99dc3c24ef4a44c763efcf66a6e3e44d31d723683dd339c343770bd43523007`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0b13828c450ce09acf99d42e4d9e625dbc1991b6f87a5727ff595e3e62a06c`  
		Last Modified: Mon, 06 May 2024 23:39:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d1dc50ec127cc25ab5b90bbe3fccaf4c5cda1379629dcd1760fa93b6cab32718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7934a2d41084621a7a7ff3aafbea88a9edfb76ded1149d611483fb61826d661`

```dockerfile
```

-	Layers:
	-	`sha256:dedf3264102cee8df6c9d7e964dedede98ab6b3865d8df8f76e88eeb42290632`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b25fbb2f936e2b3483885e59398fdcffdf62a984c55d6171eb02b6a8b6ef44d7`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 19.4 KB (19376 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:16979dbfdc08cb52efcfffcdfdff35be32426e49b90065b36155882be545d88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6151853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cca463729a03d73b6abb17295ed77bc6a13a336b4bc01a3b1c03a176f34fa06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
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
	-	`sha256:37d6a06c9130de338c39b57baed51f1e62b01cf60bb33a109ac31927ab8c775f`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 2.8 MB (2794432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db042a56f7b2a4ea616aa34e4b563284ea5d38557c0ff85c04706fc945bc905`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e7dbc7d250abc9822b7e752e47c8b83dd404648d74f9331600b392ac836970`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b885694442ff65cade16142bde9307eda742f797b4c4e48b95e2ecd62c262746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023ebbf730f939171a6dd74509e836130fe404e073174c8b1be5b28fd09e514e`

```dockerfile
```

-	Layers:
	-	`sha256:b18acb410267cb31ce209d09681474ba43f18c2f4af00288845c4061bd220974`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48c7d2c81f6bbcf60c7bbca78ec3114f620154531205c592fe14d252cb9daf08`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 19.3 KB (19309 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine3.19`

```console
$ docker pull memcached@sha256:4ee2d6582442b4920f0c9de6565947a81e18abc48089804df10251eedf388d66
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
$ docker pull memcached@sha256:cf854f636d506c0834dc1159ad5b472fea96028e88702014088384915a7c08dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6535198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21047320ccba2e62e0ee66c1ffa169149658e039ee012547c37ed6aa0130ad2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59605d18a5ec7e6531bd08f0238da758082d075c4fdd6a4ec8c00fd6f792425b`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8691b75405b7042ea4a853223cc80432131a0e21745f3baf9b21b00073207ace`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 104.2 KB (104211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8925d4d8379f9d71921da012b62d23d71f826e429777c701a1b0d4d56d0399ac`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 3.0 MB (3020613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86013193f6f292637e997c2518f84ab28fec9d7a494cda4090d07457058f10de`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cfe77bbca77075d0b682e8546bca4d6d045cfbff0be0336d51b7bbe1116983`  
		Last Modified: Mon, 06 May 2024 23:08:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:d4a846cbc9f47d5db83dbb38f019064556e6af28dad33264b1f851bebbb2858b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ab3ae8df84416fe4351914e6bb061214bfad4b0cb01537aef674b02c008994`

```dockerfile
```

-	Layers:
	-	`sha256:59634fa6bbcc5be09a70b3894761425c9ea7b231a189445bce9ae40b97f09675`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2fd487a2e71a464ab83cce092819d041b742e29af0ecb901bcb36ac21fc7c2c`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 19.5 KB (19475 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:8a6f18eb424270a1dca99143a613014d570cb7376c9cb7d212b72d74c569b12a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6381171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ddcb41c8f4d78c4720e1ad02b3c978ef7af38607d717e52219f0c53ab6fb64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859f5f148ebb49ed2dfc712d036c8e1162fd5c08307e622f420c9e722f459c15`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a85abddca9696d1381e2dbbf52914e6119f22bd22e71c1ffc49aa385ca2d79`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 120.9 KB (120900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f80774db5f2d9cd2ec4f0bf8e7256768ab2ff5b90e1a822c70e5fb0a8d0a42`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 2.9 MB (2910908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fff6ea9e3e8e56264cef5ba1ceaacc5db1aa37fb687bf4cb684629a462a4e04`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e6b3e687f63ee869e2595d746eecfc9a9a64e49c7972eea118f9af26f3a02f`  
		Last Modified: Mon, 06 May 2024 23:43:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:7677dd609f55b7dac25e997d7fc4942f1b433f1084ca54e71a01175c8608fedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce1cbd3428e47f29034986dc018cfef4ed121b030aef195db0d03c8a65cc79d`

```dockerfile
```

-	Layers:
	-	`sha256:c80e817fe71d2bd7ff1d9709ab1ac3d7ac30315b7cfd1b528ca1c316fecabc2f`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b568b0dd9cb0ef2428bd10a39e9ee3afe06fe97f6911abc8c1ae5e642b27094`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 19.3 KB (19326 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.19` - linux; 386

```console
$ docker pull memcached@sha256:1557e39ed6b5f943d53c54797d59f4ea27755c53c9e7004cbfb633c08757abd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6194136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48e3a30b8d39f2e6434ff10c1130366a5bfeac640bc8ecb88f89e6e996cdc4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c853f4fd5c9ee2e18e52b4399ccc43726449928a43d040161f83d3f67f596dd`  
		Last Modified: Mon, 06 May 2024 23:08:35 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca2d91782956c7a9591fd3f9edb724367e6a2770f04a809c6088a8ea623ea7f`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 109.3 KB (109328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5c07db0e07d757431d4458ea14990c3cc0b06aa9577b0e29f8db33fc51921b`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 2.8 MB (2839076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21633262023f9a6ae09f480b39a8a9a7109a0201b779ccdba90e721204cb20ae`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893c3463887c0e33218f5af72fe7534fe9bebd41fd26e976944bbd03c13a9d22`  
		Last Modified: Mon, 06 May 2024 23:08:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:4184448ad3b3ff9a34654847c26c9ad677ce54b07e8a96eedb429e8c509fe5e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04225924b78526836b6ef1d8f4bd3d25e994e9f858bedc4d73fbf5308500d074`

```dockerfile
```

-	Layers:
	-	`sha256:562178e7885ee7492a868cc754c309fe7cf0a52b74299dc570dc9959ecfc0c10`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d1f3d52b695ee750a517e356c17e9f3b6a3778f607f791f558ae9e31397df3f`  
		Last Modified: Mon, 06 May 2024 23:08:35 GMT  
		Size: 19.4 KB (19420 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.19` - linux; ppc64le

```console
$ docker pull memcached@sha256:4b1fdeda480d0b679c2b9fa5a09c508dabaf7bf0bf1600d0078fcae81e004dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6407037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf112675855fb5780056fbde79f0822c329da1cfb19ca47270289ec2ac966e77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25735f744a453fbf0af2d088f79a0fa6de45cc2699601389d42141b2de2f21d3`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a61320e5e6694b8436a4074ba6280369b9b29e2474231252683fa11606b8e6`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 123.4 KB (123401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e809f0a1acfe802b3158bb0d4d370427885e8c5ba2ce6b98549da9bbac597e`  
		Last Modified: Mon, 06 May 2024 23:39:16 GMT  
		Size: 2.9 MB (2923638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99dc3c24ef4a44c763efcf66a6e3e44d31d723683dd339c343770bd43523007`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0b13828c450ce09acf99d42e4d9e625dbc1991b6f87a5727ff595e3e62a06c`  
		Last Modified: Mon, 06 May 2024 23:39:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:d1dc50ec127cc25ab5b90bbe3fccaf4c5cda1379629dcd1760fa93b6cab32718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7934a2d41084621a7a7ff3aafbea88a9edfb76ded1149d611483fb61826d661`

```dockerfile
```

-	Layers:
	-	`sha256:dedf3264102cee8df6c9d7e964dedede98ab6b3865d8df8f76e88eeb42290632`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b25fbb2f936e2b3483885e59398fdcffdf62a984c55d6171eb02b6a8b6ef44d7`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 19.4 KB (19376 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.19` - linux; s390x

```console
$ docker pull memcached@sha256:16979dbfdc08cb52efcfffcdfdff35be32426e49b90065b36155882be545d88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6151853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cca463729a03d73b6abb17295ed77bc6a13a336b4bc01a3b1c03a176f34fa06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
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
	-	`sha256:37d6a06c9130de338c39b57baed51f1e62b01cf60bb33a109ac31927ab8c775f`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 2.8 MB (2794432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db042a56f7b2a4ea616aa34e4b563284ea5d38557c0ff85c04706fc945bc905`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e7dbc7d250abc9822b7e752e47c8b83dd404648d74f9331600b392ac836970`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:b885694442ff65cade16142bde9307eda742f797b4c4e48b95e2ecd62c262746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023ebbf730f939171a6dd74509e836130fe404e073174c8b1be5b28fd09e514e`

```dockerfile
```

-	Layers:
	-	`sha256:b18acb410267cb31ce209d09681474ba43f18c2f4af00288845c4061bd220974`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48c7d2c81f6bbcf60c7bbca78ec3114f620154531205c592fe14d252cb9daf08`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 19.3 KB (19309 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-bookworm`

```console
$ docker pull memcached@sha256:2585b867c96c722e5f4b9d3986a64b3ad67b956f55e31fdf4469f1e5dc157bdc
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
$ docker pull memcached@sha256:29dde2f0a4b996fa7684041ce78bb31e7c2b1a9c8aa6abe467364e8215c57035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38691245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec8c94e66592eab160b4534afad21e21800362694048e80f2c8e82b20c060a78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105cdbf392f0d274b354ff593187bc8b5c883e9087567f7ae4974eea189e7847`  
		Last Modified: Mon, 06 May 2024 23:08:23 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ef4162d3aae0771395e4e1b7ce0c5431fc5fbf987c9c410b7e5b959e302a40`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 2.5 MB (2488488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be957db0d2fe09ea0c4fe874c335ee65f4a0a268476fbc1e646c611ca6b0b1f8`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 7.1 MB (7050761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028dbe498f2fd4131b262e14a863a793bb71221f0cc5b9488822c6a1bb1b0c8c`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7239ceaa87f6c0fc3415c2d6d064020f0b8d2427a548364ecbde0f044094cfdb`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:dce70377f5e30a5563e4d8507edfff7f8947a7575b6ebfe7283407d9fcce4458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c9ef74fba5a31fccf3f549b4fd48b6c4db07bef69a0e574ecb6e9c5bc37448a`

```dockerfile
```

-	Layers:
	-	`sha256:67f37454203d55985eef3fd618246f415a13be9dd32f789dc93d5ee36efcd7e2`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 2.3 MB (2261261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1481c59e0b769395485e713e760e5b60c337edf6600a053a98eaacdcb4a121eb`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 21.1 KB (21146 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:d04280085fd0255be4cf80a6c19c28266f51615eddfe506d718c588dd762a01c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.9 MB (34885683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac68380af8a0798b278fdebe3bfeaf85e0f6d53f505d959ae42ae2eb4de89c15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:53:11 GMT
ADD file:0140ab9be4171f94aae33901f189ffd8822ce6da4a052798883fd66d03b79be9 in / 
# Wed, 24 Apr 2024 03:53:12 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2c9444d4d8a989f4536a8afd8b41a3461ede5b15d490d87c3369b051095d7ae3`  
		Last Modified: Wed, 24 Apr 2024 03:56:28 GMT  
		Size: 26.9 MB (26910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad3b02f635c19a5c749474c01db78c0d1bd9f6465178c236ac42079364c167e`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c82b33e3a41551599953fed1e04a047e0a017d6de973951e88a2319d4eb3b5`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 2.1 MB (2089520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f05e3ac287ed1762995abf279872754c6f943b51b3f1a25e8a2a4b17c08657`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 5.9 MB (5884617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764bff9a4b0a489e9c8c1102b502bf6142559e169252ba08d486d8f0a5b60c90`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e968f84d0f8d617f917f72762217ea784201f4dbd8d958e7c679479a25500e22`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:6bfcd444a59b433ecbc80cb2f9ce87fc6ec5ebc6e20d69b79ab258a8df83d8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1b6d39e43bcacaafbba90473dd410c5e07008c7b5e8f6c5e0053a1cd81e4d2`

```dockerfile
```

-	Layers:
	-	`sha256:d15574302d09f987aff6a1dd074dfa1a5bcf39d50d2488e2bf25204432517fce`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 2.3 MB (2264549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcb55f3be2aa40dd40b859884d496c08b3c104f6782ea068c88df7430c224b5b`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 21.1 KB (21119 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:dcb3196cd0eaf5593a642df75f5c68b0962b89335e489c41d2bd2f50106b2990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.5 MB (38539477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:453e18c2977a4810fadaaeefd26b1cc5b3ddf8aea9a337463475b66a7eb5cf3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea3b2534cc10b3982041c25f3e3e46bc54885fb85a56a850e5d87825605d959`  
		Last Modified: Mon, 06 May 2024 23:40:33 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8c0c56b8ceb323ad11adf63e3d67d815207d779b691a1e144ecbbc509a56c6`  
		Last Modified: Mon, 06 May 2024 23:40:34 GMT  
		Size: 2.3 MB (2346198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b93f0391bd3380825799bef11d6a6236d36dd2a538fddf37ffe5eb89f606aa`  
		Last Modified: Mon, 06 May 2024 23:40:34 GMT  
		Size: 7.0 MB (7011826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5b9d9447753339dd1b2be478d2d2153513530b8476657fe41a93507ac389b2`  
		Last Modified: Mon, 06 May 2024 23:40:33 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd2e6309ee48b90c1469e3408f664e9277e5a348c13026648488c2ac26abc3e`  
		Last Modified: Mon, 06 May 2024 23:40:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:12c2959e59ca59159b3810394cf53899988571d57d4df9c4f0c63950fda39f80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c238d1722683e731e558126fa120d76c1f59a8c0e1fc8cdf25fadb97937810b6`

```dockerfile
```

-	Layers:
	-	`sha256:a23cc33f240eaa7b71c6e81fd3a50f2ba3a4c5c20de8d43766527e3f3cc40832`  
		Last Modified: Mon, 06 May 2024 23:40:34 GMT  
		Size: 2.3 MB (2261490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bc0c2167dc9c0dce55a2cb122d4d7721644ccca44d35b0906c74bac6eb00bfc`  
		Last Modified: Mon, 06 May 2024 23:40:33 GMT  
		Size: 21.0 KB (20997 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:3f542cc336b40813213949d5eb8e2da1a57005f88566c0d51c3b8624cc911916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33914242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a44cb325942314e83e433868ace554ffea1c0ef303993f238620f928b36bbcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa82d06bb0cba58ed3fae5da8ee9c6248a027c9d105f1c1e2094d1973ab2f78`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf14cdbfbd6ea1d7231b4119cb6c85336718c7ccee9bc57573aadcc210f05e2`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 2.5 MB (2492686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bed32b6d0ec7a40384a2ba4d5fa14871afba5fd572025e99ebc3c30541ee6bf`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 1.3 MB (1257406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07ba6ac3de2271f181cd17c67b57573da49f54d516ad3c852a2610d138c85b3`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a700f395f10bfe9002c02677754b0a58c0ee8ca0f1fc73477ef1b86dc734103b`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:8932028ec9d6cdd607a57df36f524623a045c35db7110aa26040859db5599b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303c5c842506ac0858dd708f266252ee2b586ba9dd6f506ef93e95c9d4d06402`

```dockerfile
```

-	Layers:
	-	`sha256:e55268858bc5b4c5b04534306d270b5c41b3d3dccd563cae845878933e3d7a1c`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 2.3 MB (2258359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4afdfadae6d39596deea4cc7598059a6d7cdd84a4bf4036bfd609cacb9347c22`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:54a6cf440988b85512b266a181d2e83efe8a6a16530029f48b2fd002efb2e251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38171114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac4ac5a7759abeb1658c052e8e13a0cdc6e05c7af62e12528e0d65428805b7b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:14:18 GMT
ADD file:a3e63beab80160854bfc2d48f69e7c70a9542cdfaf3c5b50f1d6248a998b75ae in / 
# Wed, 24 Apr 2024 03:14:22 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af25825be002e7bdd52bf28c2fbef5bae0ba9fcef8118e5591a874e7a70b2a62`  
		Last Modified: Wed, 24 Apr 2024 03:25:20 GMT  
		Size: 29.1 MB (29144174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70b69867f90cc0cd6ccf8b72f07ee05c80179a59283d6ce971d9191eaf11afe`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361f75ee595f0c436f725a5dd64b1009cb0da358d19361f68345abf27c392f03`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 1.9 MB (1937740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1d3e5a5aad136d9ada8e95bd8e9f609baf923df5c9a48a8021e50206e4e93d`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 7.1 MB (7087680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913b327051e93299424d31038856dead21e1781ab1e47927437d8d135ea97338`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a025835eff1c0dfdae38dce98ddefd33f8609362934acbc3106f445279e8b050`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:062ba12de9ac3ea604948fc8045fa1f18254e15045b75fd40ba397ca49ddac94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f78c9e4c785d57060d12fdc33b3579dde0c50533361c63c38632718921c39d`

```dockerfile
```

-	Layers:
	-	`sha256:0f87aa3b54f1e190b0d04cc9d1960d4d745a6c99015f572091bc1c532c971e12`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:00e8c12c53be74f05f1d407b5e6d79dc9f3c03eaf6bcc42d7fde84b55135c65b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43803388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c5835d941db2f784baf56126916def72cb031f8bf87f0eb9c85d38ab2a99006`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:13 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Wed, 24 Apr 2024 03:21:15 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7fcd02d677f7b314809120f00d6b081965b5807827188e6ebf3081436f54c9`  
		Last Modified: Mon, 06 May 2024 23:36:28 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7857db5dc94e4b30fbaed58c503c6aa7cf416363b6ebd7bfe4eb21d81bd3d54e`  
		Last Modified: Mon, 06 May 2024 23:36:29 GMT  
		Size: 2.7 MB (2698389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4129214713c04309f826d05e9dead290efde58d33f38bf8cc51796ce3d02392`  
		Last Modified: Mon, 06 May 2024 23:36:29 GMT  
		Size: 8.0 MB (7962280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009ed91ac73d01b73721c2c68710b06d4067d836af63780f5260d075df4cfa57`  
		Last Modified: Mon, 06 May 2024 23:36:29 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db194260f1714761a294b97e37fb2d51544c26f4447b3ff81009b1a9a07cd992`  
		Last Modified: Mon, 06 May 2024 23:36:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:577d80832f1718d990d4526e62c1abfd9b09fe17643600c30a82b75a5a0ad018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842a6e10e139ec873043472602e0301d3b0e0d09e7123af5c4739b4da4d20616`

```dockerfile
```

-	Layers:
	-	`sha256:0f8c1c8dfeeac8f6c9be4a58fec56319cd72fb7e52b664e29d21a1f603698b5f`  
		Last Modified: Mon, 06 May 2024 23:36:29 GMT  
		Size: 2.3 MB (2265632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c9b981b4bff189bd3a4d6c0d3c9a51794ea3d75674dc37ed4a0c88494b1d553`  
		Last Modified: Mon, 06 May 2024 23:36:29 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:f1eded0e1e184f274872c917b0898ea33d458ce85cf84dcfdd7fd612ccf43f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35763592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13d7f11723a6c3c0292b7fc87542450d38bec719b123b35792a28d4f0ee5cc3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:43:18 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Wed, 24 Apr 2024 03:43:21 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
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
	-	`sha256:31591ca6b7d175a856e1a87b1fcdba950a0189086a123e820f1638b43fd955e6`  
		Last Modified: Mon, 06 May 2024 23:39:10 GMT  
		Size: 6.1 MB (6097067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf96459eefa11b754c53ffaa240db16c5e7ca96d1187924dadb4717e9001079`  
		Last Modified: Mon, 06 May 2024 23:39:10 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c2b7746d8228729836f11aa3c212bc49ad4769651a8d03525966c158e0e828`  
		Last Modified: Mon, 06 May 2024 23:39:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:38c86b4cfae8572747cee6ca551e6e8e82e52321c96c1c8d178e87febf12857b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09d6f045f1e26176704badc902459105cc38b94d2b84961f936773844e9df075`

```dockerfile
```

-	Layers:
	-	`sha256:bb75dfb1e8a87ed594faee6dfd29fe3744905435891a990c608d532312e5c908`  
		Last Modified: Mon, 06 May 2024 23:39:10 GMT  
		Size: 2.3 MB (2261082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b711f312fd8f0ae434954fd2d919960b4b8522210024b2611eb5af0b5de5414`  
		Last Modified: Mon, 06 May 2024 23:39:10 GMT  
		Size: 21.0 KB (20979 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.27`

```console
$ docker pull memcached@sha256:2585b867c96c722e5f4b9d3986a64b3ad67b956f55e31fdf4469f1e5dc157bdc
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

### `memcached:1.6.27` - linux; amd64

```console
$ docker pull memcached@sha256:29dde2f0a4b996fa7684041ce78bb31e7c2b1a9c8aa6abe467364e8215c57035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38691245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec8c94e66592eab160b4534afad21e21800362694048e80f2c8e82b20c060a78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105cdbf392f0d274b354ff593187bc8b5c883e9087567f7ae4974eea189e7847`  
		Last Modified: Mon, 06 May 2024 23:08:23 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ef4162d3aae0771395e4e1b7ce0c5431fc5fbf987c9c410b7e5b959e302a40`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 2.5 MB (2488488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be957db0d2fe09ea0c4fe874c335ee65f4a0a268476fbc1e646c611ca6b0b1f8`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 7.1 MB (7050761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028dbe498f2fd4131b262e14a863a793bb71221f0cc5b9488822c6a1bb1b0c8c`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7239ceaa87f6c0fc3415c2d6d064020f0b8d2427a548364ecbde0f044094cfdb`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27` - unknown; unknown

```console
$ docker pull memcached@sha256:dce70377f5e30a5563e4d8507edfff7f8947a7575b6ebfe7283407d9fcce4458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c9ef74fba5a31fccf3f549b4fd48b6c4db07bef69a0e574ecb6e9c5bc37448a`

```dockerfile
```

-	Layers:
	-	`sha256:67f37454203d55985eef3fd618246f415a13be9dd32f789dc93d5ee36efcd7e2`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 2.3 MB (2261261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1481c59e0b769395485e713e760e5b60c337edf6600a053a98eaacdcb4a121eb`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 21.1 KB (21146 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.27` - linux; arm variant v5

```console
$ docker pull memcached@sha256:d04280085fd0255be4cf80a6c19c28266f51615eddfe506d718c588dd762a01c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.9 MB (34885683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac68380af8a0798b278fdebe3bfeaf85e0f6d53f505d959ae42ae2eb4de89c15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:53:11 GMT
ADD file:0140ab9be4171f94aae33901f189ffd8822ce6da4a052798883fd66d03b79be9 in / 
# Wed, 24 Apr 2024 03:53:12 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2c9444d4d8a989f4536a8afd8b41a3461ede5b15d490d87c3369b051095d7ae3`  
		Last Modified: Wed, 24 Apr 2024 03:56:28 GMT  
		Size: 26.9 MB (26910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad3b02f635c19a5c749474c01db78c0d1bd9f6465178c236ac42079364c167e`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c82b33e3a41551599953fed1e04a047e0a017d6de973951e88a2319d4eb3b5`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 2.1 MB (2089520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f05e3ac287ed1762995abf279872754c6f943b51b3f1a25e8a2a4b17c08657`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 5.9 MB (5884617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764bff9a4b0a489e9c8c1102b502bf6142559e169252ba08d486d8f0a5b60c90`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e968f84d0f8d617f917f72762217ea784201f4dbd8d958e7c679479a25500e22`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27` - unknown; unknown

```console
$ docker pull memcached@sha256:6bfcd444a59b433ecbc80cb2f9ce87fc6ec5ebc6e20d69b79ab258a8df83d8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1b6d39e43bcacaafbba90473dd410c5e07008c7b5e8f6c5e0053a1cd81e4d2`

```dockerfile
```

-	Layers:
	-	`sha256:d15574302d09f987aff6a1dd074dfa1a5bcf39d50d2488e2bf25204432517fce`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 2.3 MB (2264549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcb55f3be2aa40dd40b859884d496c08b3c104f6782ea068c88df7430c224b5b`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 21.1 KB (21119 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.27` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:dcb3196cd0eaf5593a642df75f5c68b0962b89335e489c41d2bd2f50106b2990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.5 MB (38539477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:453e18c2977a4810fadaaeefd26b1cc5b3ddf8aea9a337463475b66a7eb5cf3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea3b2534cc10b3982041c25f3e3e46bc54885fb85a56a850e5d87825605d959`  
		Last Modified: Mon, 06 May 2024 23:40:33 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8c0c56b8ceb323ad11adf63e3d67d815207d779b691a1e144ecbbc509a56c6`  
		Last Modified: Mon, 06 May 2024 23:40:34 GMT  
		Size: 2.3 MB (2346198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b93f0391bd3380825799bef11d6a6236d36dd2a538fddf37ffe5eb89f606aa`  
		Last Modified: Mon, 06 May 2024 23:40:34 GMT  
		Size: 7.0 MB (7011826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5b9d9447753339dd1b2be478d2d2153513530b8476657fe41a93507ac389b2`  
		Last Modified: Mon, 06 May 2024 23:40:33 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd2e6309ee48b90c1469e3408f664e9277e5a348c13026648488c2ac26abc3e`  
		Last Modified: Mon, 06 May 2024 23:40:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27` - unknown; unknown

```console
$ docker pull memcached@sha256:12c2959e59ca59159b3810394cf53899988571d57d4df9c4f0c63950fda39f80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c238d1722683e731e558126fa120d76c1f59a8c0e1fc8cdf25fadb97937810b6`

```dockerfile
```

-	Layers:
	-	`sha256:a23cc33f240eaa7b71c6e81fd3a50f2ba3a4c5c20de8d43766527e3f3cc40832`  
		Last Modified: Mon, 06 May 2024 23:40:34 GMT  
		Size: 2.3 MB (2261490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bc0c2167dc9c0dce55a2cb122d4d7721644ccca44d35b0906c74bac6eb00bfc`  
		Last Modified: Mon, 06 May 2024 23:40:33 GMT  
		Size: 21.0 KB (20997 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.27` - linux; 386

```console
$ docker pull memcached@sha256:3f542cc336b40813213949d5eb8e2da1a57005f88566c0d51c3b8624cc911916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33914242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a44cb325942314e83e433868ace554ffea1c0ef303993f238620f928b36bbcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa82d06bb0cba58ed3fae5da8ee9c6248a027c9d105f1c1e2094d1973ab2f78`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf14cdbfbd6ea1d7231b4119cb6c85336718c7ccee9bc57573aadcc210f05e2`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 2.5 MB (2492686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bed32b6d0ec7a40384a2ba4d5fa14871afba5fd572025e99ebc3c30541ee6bf`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 1.3 MB (1257406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07ba6ac3de2271f181cd17c67b57573da49f54d516ad3c852a2610d138c85b3`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a700f395f10bfe9002c02677754b0a58c0ee8ca0f1fc73477ef1b86dc734103b`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27` - unknown; unknown

```console
$ docker pull memcached@sha256:8932028ec9d6cdd607a57df36f524623a045c35db7110aa26040859db5599b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303c5c842506ac0858dd708f266252ee2b586ba9dd6f506ef93e95c9d4d06402`

```dockerfile
```

-	Layers:
	-	`sha256:e55268858bc5b4c5b04534306d270b5c41b3d3dccd563cae845878933e3d7a1c`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 2.3 MB (2258359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4afdfadae6d39596deea4cc7598059a6d7cdd84a4bf4036bfd609cacb9347c22`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.27` - linux; mips64le

```console
$ docker pull memcached@sha256:54a6cf440988b85512b266a181d2e83efe8a6a16530029f48b2fd002efb2e251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38171114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac4ac5a7759abeb1658c052e8e13a0cdc6e05c7af62e12528e0d65428805b7b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:14:18 GMT
ADD file:a3e63beab80160854bfc2d48f69e7c70a9542cdfaf3c5b50f1d6248a998b75ae in / 
# Wed, 24 Apr 2024 03:14:22 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af25825be002e7bdd52bf28c2fbef5bae0ba9fcef8118e5591a874e7a70b2a62`  
		Last Modified: Wed, 24 Apr 2024 03:25:20 GMT  
		Size: 29.1 MB (29144174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70b69867f90cc0cd6ccf8b72f07ee05c80179a59283d6ce971d9191eaf11afe`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361f75ee595f0c436f725a5dd64b1009cb0da358d19361f68345abf27c392f03`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 1.9 MB (1937740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1d3e5a5aad136d9ada8e95bd8e9f609baf923df5c9a48a8021e50206e4e93d`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 7.1 MB (7087680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913b327051e93299424d31038856dead21e1781ab1e47927437d8d135ea97338`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a025835eff1c0dfdae38dce98ddefd33f8609362934acbc3106f445279e8b050`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27` - unknown; unknown

```console
$ docker pull memcached@sha256:062ba12de9ac3ea604948fc8045fa1f18254e15045b75fd40ba397ca49ddac94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f78c9e4c785d57060d12fdc33b3579dde0c50533361c63c38632718921c39d`

```dockerfile
```

-	Layers:
	-	`sha256:0f87aa3b54f1e190b0d04cc9d1960d4d745a6c99015f572091bc1c532c971e12`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.27` - linux; ppc64le

```console
$ docker pull memcached@sha256:00e8c12c53be74f05f1d407b5e6d79dc9f3c03eaf6bcc42d7fde84b55135c65b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43803388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c5835d941db2f784baf56126916def72cb031f8bf87f0eb9c85d38ab2a99006`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:13 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Wed, 24 Apr 2024 03:21:15 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7fcd02d677f7b314809120f00d6b081965b5807827188e6ebf3081436f54c9`  
		Last Modified: Mon, 06 May 2024 23:36:28 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7857db5dc94e4b30fbaed58c503c6aa7cf416363b6ebd7bfe4eb21d81bd3d54e`  
		Last Modified: Mon, 06 May 2024 23:36:29 GMT  
		Size: 2.7 MB (2698389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4129214713c04309f826d05e9dead290efde58d33f38bf8cc51796ce3d02392`  
		Last Modified: Mon, 06 May 2024 23:36:29 GMT  
		Size: 8.0 MB (7962280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009ed91ac73d01b73721c2c68710b06d4067d836af63780f5260d075df4cfa57`  
		Last Modified: Mon, 06 May 2024 23:36:29 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db194260f1714761a294b97e37fb2d51544c26f4447b3ff81009b1a9a07cd992`  
		Last Modified: Mon, 06 May 2024 23:36:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27` - unknown; unknown

```console
$ docker pull memcached@sha256:577d80832f1718d990d4526e62c1abfd9b09fe17643600c30a82b75a5a0ad018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842a6e10e139ec873043472602e0301d3b0e0d09e7123af5c4739b4da4d20616`

```dockerfile
```

-	Layers:
	-	`sha256:0f8c1c8dfeeac8f6c9be4a58fec56319cd72fb7e52b664e29d21a1f603698b5f`  
		Last Modified: Mon, 06 May 2024 23:36:29 GMT  
		Size: 2.3 MB (2265632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c9b981b4bff189bd3a4d6c0d3c9a51794ea3d75674dc37ed4a0c88494b1d553`  
		Last Modified: Mon, 06 May 2024 23:36:29 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.27` - linux; s390x

```console
$ docker pull memcached@sha256:f1eded0e1e184f274872c917b0898ea33d458ce85cf84dcfdd7fd612ccf43f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35763592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13d7f11723a6c3c0292b7fc87542450d38bec719b123b35792a28d4f0ee5cc3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:43:18 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Wed, 24 Apr 2024 03:43:21 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
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
	-	`sha256:31591ca6b7d175a856e1a87b1fcdba950a0189086a123e820f1638b43fd955e6`  
		Last Modified: Mon, 06 May 2024 23:39:10 GMT  
		Size: 6.1 MB (6097067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf96459eefa11b754c53ffaa240db16c5e7ca96d1187924dadb4717e9001079`  
		Last Modified: Mon, 06 May 2024 23:39:10 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c2b7746d8228729836f11aa3c212bc49ad4769651a8d03525966c158e0e828`  
		Last Modified: Mon, 06 May 2024 23:39:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27` - unknown; unknown

```console
$ docker pull memcached@sha256:38c86b4cfae8572747cee6ca551e6e8e82e52321c96c1c8d178e87febf12857b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09d6f045f1e26176704badc902459105cc38b94d2b84961f936773844e9df075`

```dockerfile
```

-	Layers:
	-	`sha256:bb75dfb1e8a87ed594faee6dfd29fe3744905435891a990c608d532312e5c908`  
		Last Modified: Mon, 06 May 2024 23:39:10 GMT  
		Size: 2.3 MB (2261082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b711f312fd8f0ae434954fd2d919960b4b8522210024b2611eb5af0b5de5414`  
		Last Modified: Mon, 06 May 2024 23:39:10 GMT  
		Size: 21.0 KB (20979 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.27-alpine`

```console
$ docker pull memcached@sha256:4ee2d6582442b4920f0c9de6565947a81e18abc48089804df10251eedf388d66
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

### `memcached:1.6.27-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:cf854f636d506c0834dc1159ad5b472fea96028e88702014088384915a7c08dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6535198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21047320ccba2e62e0ee66c1ffa169149658e039ee012547c37ed6aa0130ad2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59605d18a5ec7e6531bd08f0238da758082d075c4fdd6a4ec8c00fd6f792425b`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8691b75405b7042ea4a853223cc80432131a0e21745f3baf9b21b00073207ace`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 104.2 KB (104211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8925d4d8379f9d71921da012b62d23d71f826e429777c701a1b0d4d56d0399ac`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 3.0 MB (3020613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86013193f6f292637e997c2518f84ab28fec9d7a494cda4090d07457058f10de`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cfe77bbca77075d0b682e8546bca4d6d045cfbff0be0336d51b7bbe1116983`  
		Last Modified: Mon, 06 May 2024 23:08:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d4a846cbc9f47d5db83dbb38f019064556e6af28dad33264b1f851bebbb2858b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ab3ae8df84416fe4351914e6bb061214bfad4b0cb01537aef674b02c008994`

```dockerfile
```

-	Layers:
	-	`sha256:59634fa6bbcc5be09a70b3894761425c9ea7b231a189445bce9ae40b97f09675`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2fd487a2e71a464ab83cce092819d041b742e29af0ecb901bcb36ac21fc7c2c`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 19.5 KB (19475 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.27-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:8a6f18eb424270a1dca99143a613014d570cb7376c9cb7d212b72d74c569b12a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6381171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ddcb41c8f4d78c4720e1ad02b3c978ef7af38607d717e52219f0c53ab6fb64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859f5f148ebb49ed2dfc712d036c8e1162fd5c08307e622f420c9e722f459c15`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a85abddca9696d1381e2dbbf52914e6119f22bd22e71c1ffc49aa385ca2d79`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 120.9 KB (120900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f80774db5f2d9cd2ec4f0bf8e7256768ab2ff5b90e1a822c70e5fb0a8d0a42`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 2.9 MB (2910908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fff6ea9e3e8e56264cef5ba1ceaacc5db1aa37fb687bf4cb684629a462a4e04`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e6b3e687f63ee869e2595d746eecfc9a9a64e49c7972eea118f9af26f3a02f`  
		Last Modified: Mon, 06 May 2024 23:43:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7677dd609f55b7dac25e997d7fc4942f1b433f1084ca54e71a01175c8608fedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce1cbd3428e47f29034986dc018cfef4ed121b030aef195db0d03c8a65cc79d`

```dockerfile
```

-	Layers:
	-	`sha256:c80e817fe71d2bd7ff1d9709ab1ac3d7ac30315b7cfd1b528ca1c316fecabc2f`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b568b0dd9cb0ef2428bd10a39e9ee3afe06fe97f6911abc8c1ae5e642b27094`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 19.3 KB (19326 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.27-alpine` - linux; 386

```console
$ docker pull memcached@sha256:1557e39ed6b5f943d53c54797d59f4ea27755c53c9e7004cbfb633c08757abd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6194136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48e3a30b8d39f2e6434ff10c1130366a5bfeac640bc8ecb88f89e6e996cdc4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c853f4fd5c9ee2e18e52b4399ccc43726449928a43d040161f83d3f67f596dd`  
		Last Modified: Mon, 06 May 2024 23:08:35 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca2d91782956c7a9591fd3f9edb724367e6a2770f04a809c6088a8ea623ea7f`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 109.3 KB (109328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5c07db0e07d757431d4458ea14990c3cc0b06aa9577b0e29f8db33fc51921b`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 2.8 MB (2839076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21633262023f9a6ae09f480b39a8a9a7109a0201b779ccdba90e721204cb20ae`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893c3463887c0e33218f5af72fe7534fe9bebd41fd26e976944bbd03c13a9d22`  
		Last Modified: Mon, 06 May 2024 23:08:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:4184448ad3b3ff9a34654847c26c9ad677ce54b07e8a96eedb429e8c509fe5e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04225924b78526836b6ef1d8f4bd3d25e994e9f858bedc4d73fbf5308500d074`

```dockerfile
```

-	Layers:
	-	`sha256:562178e7885ee7492a868cc754c309fe7cf0a52b74299dc570dc9959ecfc0c10`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d1f3d52b695ee750a517e356c17e9f3b6a3778f607f791f558ae9e31397df3f`  
		Last Modified: Mon, 06 May 2024 23:08:35 GMT  
		Size: 19.4 KB (19420 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.27-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:4b1fdeda480d0b679c2b9fa5a09c508dabaf7bf0bf1600d0078fcae81e004dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6407037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf112675855fb5780056fbde79f0822c329da1cfb19ca47270289ec2ac966e77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25735f744a453fbf0af2d088f79a0fa6de45cc2699601389d42141b2de2f21d3`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a61320e5e6694b8436a4074ba6280369b9b29e2474231252683fa11606b8e6`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 123.4 KB (123401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e809f0a1acfe802b3158bb0d4d370427885e8c5ba2ce6b98549da9bbac597e`  
		Last Modified: Mon, 06 May 2024 23:39:16 GMT  
		Size: 2.9 MB (2923638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99dc3c24ef4a44c763efcf66a6e3e44d31d723683dd339c343770bd43523007`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0b13828c450ce09acf99d42e4d9e625dbc1991b6f87a5727ff595e3e62a06c`  
		Last Modified: Mon, 06 May 2024 23:39:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d1dc50ec127cc25ab5b90bbe3fccaf4c5cda1379629dcd1760fa93b6cab32718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7934a2d41084621a7a7ff3aafbea88a9edfb76ded1149d611483fb61826d661`

```dockerfile
```

-	Layers:
	-	`sha256:dedf3264102cee8df6c9d7e964dedede98ab6b3865d8df8f76e88eeb42290632`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b25fbb2f936e2b3483885e59398fdcffdf62a984c55d6171eb02b6a8b6ef44d7`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 19.4 KB (19376 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.27-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:16979dbfdc08cb52efcfffcdfdff35be32426e49b90065b36155882be545d88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6151853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cca463729a03d73b6abb17295ed77bc6a13a336b4bc01a3b1c03a176f34fa06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
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
	-	`sha256:37d6a06c9130de338c39b57baed51f1e62b01cf60bb33a109ac31927ab8c775f`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 2.8 MB (2794432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db042a56f7b2a4ea616aa34e4b563284ea5d38557c0ff85c04706fc945bc905`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e7dbc7d250abc9822b7e752e47c8b83dd404648d74f9331600b392ac836970`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b885694442ff65cade16142bde9307eda742f797b4c4e48b95e2ecd62c262746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023ebbf730f939171a6dd74509e836130fe404e073174c8b1be5b28fd09e514e`

```dockerfile
```

-	Layers:
	-	`sha256:b18acb410267cb31ce209d09681474ba43f18c2f4af00288845c4061bd220974`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48c7d2c81f6bbcf60c7bbca78ec3114f620154531205c592fe14d252cb9daf08`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 19.3 KB (19309 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.27-alpine3.19`

```console
$ docker pull memcached@sha256:4ee2d6582442b4920f0c9de6565947a81e18abc48089804df10251eedf388d66
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

### `memcached:1.6.27-alpine3.19` - linux; amd64

```console
$ docker pull memcached@sha256:cf854f636d506c0834dc1159ad5b472fea96028e88702014088384915a7c08dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6535198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21047320ccba2e62e0ee66c1ffa169149658e039ee012547c37ed6aa0130ad2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59605d18a5ec7e6531bd08f0238da758082d075c4fdd6a4ec8c00fd6f792425b`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8691b75405b7042ea4a853223cc80432131a0e21745f3baf9b21b00073207ace`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 104.2 KB (104211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8925d4d8379f9d71921da012b62d23d71f826e429777c701a1b0d4d56d0399ac`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 3.0 MB (3020613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86013193f6f292637e997c2518f84ab28fec9d7a494cda4090d07457058f10de`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cfe77bbca77075d0b682e8546bca4d6d045cfbff0be0336d51b7bbe1116983`  
		Last Modified: Mon, 06 May 2024 23:08:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:d4a846cbc9f47d5db83dbb38f019064556e6af28dad33264b1f851bebbb2858b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ab3ae8df84416fe4351914e6bb061214bfad4b0cb01537aef674b02c008994`

```dockerfile
```

-	Layers:
	-	`sha256:59634fa6bbcc5be09a70b3894761425c9ea7b231a189445bce9ae40b97f09675`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2fd487a2e71a464ab83cce092819d041b742e29af0ecb901bcb36ac21fc7c2c`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 19.5 KB (19475 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.27-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:8a6f18eb424270a1dca99143a613014d570cb7376c9cb7d212b72d74c569b12a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6381171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ddcb41c8f4d78c4720e1ad02b3c978ef7af38607d717e52219f0c53ab6fb64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859f5f148ebb49ed2dfc712d036c8e1162fd5c08307e622f420c9e722f459c15`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a85abddca9696d1381e2dbbf52914e6119f22bd22e71c1ffc49aa385ca2d79`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 120.9 KB (120900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f80774db5f2d9cd2ec4f0bf8e7256768ab2ff5b90e1a822c70e5fb0a8d0a42`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 2.9 MB (2910908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fff6ea9e3e8e56264cef5ba1ceaacc5db1aa37fb687bf4cb684629a462a4e04`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e6b3e687f63ee869e2595d746eecfc9a9a64e49c7972eea118f9af26f3a02f`  
		Last Modified: Mon, 06 May 2024 23:43:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:7677dd609f55b7dac25e997d7fc4942f1b433f1084ca54e71a01175c8608fedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce1cbd3428e47f29034986dc018cfef4ed121b030aef195db0d03c8a65cc79d`

```dockerfile
```

-	Layers:
	-	`sha256:c80e817fe71d2bd7ff1d9709ab1ac3d7ac30315b7cfd1b528ca1c316fecabc2f`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b568b0dd9cb0ef2428bd10a39e9ee3afe06fe97f6911abc8c1ae5e642b27094`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 19.3 KB (19326 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.27-alpine3.19` - linux; 386

```console
$ docker pull memcached@sha256:1557e39ed6b5f943d53c54797d59f4ea27755c53c9e7004cbfb633c08757abd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6194136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48e3a30b8d39f2e6434ff10c1130366a5bfeac640bc8ecb88f89e6e996cdc4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c853f4fd5c9ee2e18e52b4399ccc43726449928a43d040161f83d3f67f596dd`  
		Last Modified: Mon, 06 May 2024 23:08:35 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca2d91782956c7a9591fd3f9edb724367e6a2770f04a809c6088a8ea623ea7f`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 109.3 KB (109328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5c07db0e07d757431d4458ea14990c3cc0b06aa9577b0e29f8db33fc51921b`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 2.8 MB (2839076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21633262023f9a6ae09f480b39a8a9a7109a0201b779ccdba90e721204cb20ae`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893c3463887c0e33218f5af72fe7534fe9bebd41fd26e976944bbd03c13a9d22`  
		Last Modified: Mon, 06 May 2024 23:08:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:4184448ad3b3ff9a34654847c26c9ad677ce54b07e8a96eedb429e8c509fe5e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04225924b78526836b6ef1d8f4bd3d25e994e9f858bedc4d73fbf5308500d074`

```dockerfile
```

-	Layers:
	-	`sha256:562178e7885ee7492a868cc754c309fe7cf0a52b74299dc570dc9959ecfc0c10`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d1f3d52b695ee750a517e356c17e9f3b6a3778f607f791f558ae9e31397df3f`  
		Last Modified: Mon, 06 May 2024 23:08:35 GMT  
		Size: 19.4 KB (19420 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.27-alpine3.19` - linux; ppc64le

```console
$ docker pull memcached@sha256:4b1fdeda480d0b679c2b9fa5a09c508dabaf7bf0bf1600d0078fcae81e004dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6407037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf112675855fb5780056fbde79f0822c329da1cfb19ca47270289ec2ac966e77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25735f744a453fbf0af2d088f79a0fa6de45cc2699601389d42141b2de2f21d3`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a61320e5e6694b8436a4074ba6280369b9b29e2474231252683fa11606b8e6`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 123.4 KB (123401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e809f0a1acfe802b3158bb0d4d370427885e8c5ba2ce6b98549da9bbac597e`  
		Last Modified: Mon, 06 May 2024 23:39:16 GMT  
		Size: 2.9 MB (2923638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99dc3c24ef4a44c763efcf66a6e3e44d31d723683dd339c343770bd43523007`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0b13828c450ce09acf99d42e4d9e625dbc1991b6f87a5727ff595e3e62a06c`  
		Last Modified: Mon, 06 May 2024 23:39:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:d1dc50ec127cc25ab5b90bbe3fccaf4c5cda1379629dcd1760fa93b6cab32718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7934a2d41084621a7a7ff3aafbea88a9edfb76ded1149d611483fb61826d661`

```dockerfile
```

-	Layers:
	-	`sha256:dedf3264102cee8df6c9d7e964dedede98ab6b3865d8df8f76e88eeb42290632`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b25fbb2f936e2b3483885e59398fdcffdf62a984c55d6171eb02b6a8b6ef44d7`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 19.4 KB (19376 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.27-alpine3.19` - linux; s390x

```console
$ docker pull memcached@sha256:16979dbfdc08cb52efcfffcdfdff35be32426e49b90065b36155882be545d88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6151853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cca463729a03d73b6abb17295ed77bc6a13a336b4bc01a3b1c03a176f34fa06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
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
	-	`sha256:37d6a06c9130de338c39b57baed51f1e62b01cf60bb33a109ac31927ab8c775f`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 2.8 MB (2794432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db042a56f7b2a4ea616aa34e4b563284ea5d38557c0ff85c04706fc945bc905`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e7dbc7d250abc9822b7e752e47c8b83dd404648d74f9331600b392ac836970`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:b885694442ff65cade16142bde9307eda742f797b4c4e48b95e2ecd62c262746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023ebbf730f939171a6dd74509e836130fe404e073174c8b1be5b28fd09e514e`

```dockerfile
```

-	Layers:
	-	`sha256:b18acb410267cb31ce209d09681474ba43f18c2f4af00288845c4061bd220974`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48c7d2c81f6bbcf60c7bbca78ec3114f620154531205c592fe14d252cb9daf08`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 19.3 KB (19309 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.27-bookworm`

```console
$ docker pull memcached@sha256:2585b867c96c722e5f4b9d3986a64b3ad67b956f55e31fdf4469f1e5dc157bdc
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

### `memcached:1.6.27-bookworm` - linux; amd64

```console
$ docker pull memcached@sha256:29dde2f0a4b996fa7684041ce78bb31e7c2b1a9c8aa6abe467364e8215c57035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38691245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec8c94e66592eab160b4534afad21e21800362694048e80f2c8e82b20c060a78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105cdbf392f0d274b354ff593187bc8b5c883e9087567f7ae4974eea189e7847`  
		Last Modified: Mon, 06 May 2024 23:08:23 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ef4162d3aae0771395e4e1b7ce0c5431fc5fbf987c9c410b7e5b959e302a40`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 2.5 MB (2488488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be957db0d2fe09ea0c4fe874c335ee65f4a0a268476fbc1e646c611ca6b0b1f8`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 7.1 MB (7050761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028dbe498f2fd4131b262e14a863a793bb71221f0cc5b9488822c6a1bb1b0c8c`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7239ceaa87f6c0fc3415c2d6d064020f0b8d2427a548364ecbde0f044094cfdb`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:dce70377f5e30a5563e4d8507edfff7f8947a7575b6ebfe7283407d9fcce4458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c9ef74fba5a31fccf3f549b4fd48b6c4db07bef69a0e574ecb6e9c5bc37448a`

```dockerfile
```

-	Layers:
	-	`sha256:67f37454203d55985eef3fd618246f415a13be9dd32f789dc93d5ee36efcd7e2`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 2.3 MB (2261261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1481c59e0b769395485e713e760e5b60c337edf6600a053a98eaacdcb4a121eb`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 21.1 KB (21146 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.27-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:d04280085fd0255be4cf80a6c19c28266f51615eddfe506d718c588dd762a01c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.9 MB (34885683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac68380af8a0798b278fdebe3bfeaf85e0f6d53f505d959ae42ae2eb4de89c15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:53:11 GMT
ADD file:0140ab9be4171f94aae33901f189ffd8822ce6da4a052798883fd66d03b79be9 in / 
# Wed, 24 Apr 2024 03:53:12 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2c9444d4d8a989f4536a8afd8b41a3461ede5b15d490d87c3369b051095d7ae3`  
		Last Modified: Wed, 24 Apr 2024 03:56:28 GMT  
		Size: 26.9 MB (26910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad3b02f635c19a5c749474c01db78c0d1bd9f6465178c236ac42079364c167e`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c82b33e3a41551599953fed1e04a047e0a017d6de973951e88a2319d4eb3b5`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 2.1 MB (2089520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f05e3ac287ed1762995abf279872754c6f943b51b3f1a25e8a2a4b17c08657`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 5.9 MB (5884617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764bff9a4b0a489e9c8c1102b502bf6142559e169252ba08d486d8f0a5b60c90`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e968f84d0f8d617f917f72762217ea784201f4dbd8d958e7c679479a25500e22`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:6bfcd444a59b433ecbc80cb2f9ce87fc6ec5ebc6e20d69b79ab258a8df83d8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1b6d39e43bcacaafbba90473dd410c5e07008c7b5e8f6c5e0053a1cd81e4d2`

```dockerfile
```

-	Layers:
	-	`sha256:d15574302d09f987aff6a1dd074dfa1a5bcf39d50d2488e2bf25204432517fce`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 2.3 MB (2264549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcb55f3be2aa40dd40b859884d496c08b3c104f6782ea068c88df7430c224b5b`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 21.1 KB (21119 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.27-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:dcb3196cd0eaf5593a642df75f5c68b0962b89335e489c41d2bd2f50106b2990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.5 MB (38539477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:453e18c2977a4810fadaaeefd26b1cc5b3ddf8aea9a337463475b66a7eb5cf3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea3b2534cc10b3982041c25f3e3e46bc54885fb85a56a850e5d87825605d959`  
		Last Modified: Mon, 06 May 2024 23:40:33 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8c0c56b8ceb323ad11adf63e3d67d815207d779b691a1e144ecbbc509a56c6`  
		Last Modified: Mon, 06 May 2024 23:40:34 GMT  
		Size: 2.3 MB (2346198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b93f0391bd3380825799bef11d6a6236d36dd2a538fddf37ffe5eb89f606aa`  
		Last Modified: Mon, 06 May 2024 23:40:34 GMT  
		Size: 7.0 MB (7011826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5b9d9447753339dd1b2be478d2d2153513530b8476657fe41a93507ac389b2`  
		Last Modified: Mon, 06 May 2024 23:40:33 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd2e6309ee48b90c1469e3408f664e9277e5a348c13026648488c2ac26abc3e`  
		Last Modified: Mon, 06 May 2024 23:40:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:12c2959e59ca59159b3810394cf53899988571d57d4df9c4f0c63950fda39f80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c238d1722683e731e558126fa120d76c1f59a8c0e1fc8cdf25fadb97937810b6`

```dockerfile
```

-	Layers:
	-	`sha256:a23cc33f240eaa7b71c6e81fd3a50f2ba3a4c5c20de8d43766527e3f3cc40832`  
		Last Modified: Mon, 06 May 2024 23:40:34 GMT  
		Size: 2.3 MB (2261490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bc0c2167dc9c0dce55a2cb122d4d7721644ccca44d35b0906c74bac6eb00bfc`  
		Last Modified: Mon, 06 May 2024 23:40:33 GMT  
		Size: 21.0 KB (20997 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.27-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:3f542cc336b40813213949d5eb8e2da1a57005f88566c0d51c3b8624cc911916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33914242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a44cb325942314e83e433868ace554ffea1c0ef303993f238620f928b36bbcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa82d06bb0cba58ed3fae5da8ee9c6248a027c9d105f1c1e2094d1973ab2f78`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf14cdbfbd6ea1d7231b4119cb6c85336718c7ccee9bc57573aadcc210f05e2`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 2.5 MB (2492686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bed32b6d0ec7a40384a2ba4d5fa14871afba5fd572025e99ebc3c30541ee6bf`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 1.3 MB (1257406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07ba6ac3de2271f181cd17c67b57573da49f54d516ad3c852a2610d138c85b3`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a700f395f10bfe9002c02677754b0a58c0ee8ca0f1fc73477ef1b86dc734103b`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:8932028ec9d6cdd607a57df36f524623a045c35db7110aa26040859db5599b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303c5c842506ac0858dd708f266252ee2b586ba9dd6f506ef93e95c9d4d06402`

```dockerfile
```

-	Layers:
	-	`sha256:e55268858bc5b4c5b04534306d270b5c41b3d3dccd563cae845878933e3d7a1c`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 2.3 MB (2258359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4afdfadae6d39596deea4cc7598059a6d7cdd84a4bf4036bfd609cacb9347c22`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.27-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:54a6cf440988b85512b266a181d2e83efe8a6a16530029f48b2fd002efb2e251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38171114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac4ac5a7759abeb1658c052e8e13a0cdc6e05c7af62e12528e0d65428805b7b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:14:18 GMT
ADD file:a3e63beab80160854bfc2d48f69e7c70a9542cdfaf3c5b50f1d6248a998b75ae in / 
# Wed, 24 Apr 2024 03:14:22 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af25825be002e7bdd52bf28c2fbef5bae0ba9fcef8118e5591a874e7a70b2a62`  
		Last Modified: Wed, 24 Apr 2024 03:25:20 GMT  
		Size: 29.1 MB (29144174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70b69867f90cc0cd6ccf8b72f07ee05c80179a59283d6ce971d9191eaf11afe`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361f75ee595f0c436f725a5dd64b1009cb0da358d19361f68345abf27c392f03`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 1.9 MB (1937740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1d3e5a5aad136d9ada8e95bd8e9f609baf923df5c9a48a8021e50206e4e93d`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 7.1 MB (7087680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913b327051e93299424d31038856dead21e1781ab1e47927437d8d135ea97338`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a025835eff1c0dfdae38dce98ddefd33f8609362934acbc3106f445279e8b050`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:062ba12de9ac3ea604948fc8045fa1f18254e15045b75fd40ba397ca49ddac94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f78c9e4c785d57060d12fdc33b3579dde0c50533361c63c38632718921c39d`

```dockerfile
```

-	Layers:
	-	`sha256:0f87aa3b54f1e190b0d04cc9d1960d4d745a6c99015f572091bc1c532c971e12`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.27-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:00e8c12c53be74f05f1d407b5e6d79dc9f3c03eaf6bcc42d7fde84b55135c65b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43803388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c5835d941db2f784baf56126916def72cb031f8bf87f0eb9c85d38ab2a99006`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:13 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Wed, 24 Apr 2024 03:21:15 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7fcd02d677f7b314809120f00d6b081965b5807827188e6ebf3081436f54c9`  
		Last Modified: Mon, 06 May 2024 23:36:28 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7857db5dc94e4b30fbaed58c503c6aa7cf416363b6ebd7bfe4eb21d81bd3d54e`  
		Last Modified: Mon, 06 May 2024 23:36:29 GMT  
		Size: 2.7 MB (2698389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4129214713c04309f826d05e9dead290efde58d33f38bf8cc51796ce3d02392`  
		Last Modified: Mon, 06 May 2024 23:36:29 GMT  
		Size: 8.0 MB (7962280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009ed91ac73d01b73721c2c68710b06d4067d836af63780f5260d075df4cfa57`  
		Last Modified: Mon, 06 May 2024 23:36:29 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db194260f1714761a294b97e37fb2d51544c26f4447b3ff81009b1a9a07cd992`  
		Last Modified: Mon, 06 May 2024 23:36:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:577d80832f1718d990d4526e62c1abfd9b09fe17643600c30a82b75a5a0ad018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842a6e10e139ec873043472602e0301d3b0e0d09e7123af5c4739b4da4d20616`

```dockerfile
```

-	Layers:
	-	`sha256:0f8c1c8dfeeac8f6c9be4a58fec56319cd72fb7e52b664e29d21a1f603698b5f`  
		Last Modified: Mon, 06 May 2024 23:36:29 GMT  
		Size: 2.3 MB (2265632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c9b981b4bff189bd3a4d6c0d3c9a51794ea3d75674dc37ed4a0c88494b1d553`  
		Last Modified: Mon, 06 May 2024 23:36:29 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.27-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:f1eded0e1e184f274872c917b0898ea33d458ce85cf84dcfdd7fd612ccf43f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35763592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13d7f11723a6c3c0292b7fc87542450d38bec719b123b35792a28d4f0ee5cc3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:43:18 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Wed, 24 Apr 2024 03:43:21 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
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
	-	`sha256:31591ca6b7d175a856e1a87b1fcdba950a0189086a123e820f1638b43fd955e6`  
		Last Modified: Mon, 06 May 2024 23:39:10 GMT  
		Size: 6.1 MB (6097067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf96459eefa11b754c53ffaa240db16c5e7ca96d1187924dadb4717e9001079`  
		Last Modified: Mon, 06 May 2024 23:39:10 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c2b7746d8228729836f11aa3c212bc49ad4769651a8d03525966c158e0e828`  
		Last Modified: Mon, 06 May 2024 23:39:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:38c86b4cfae8572747cee6ca551e6e8e82e52321c96c1c8d178e87febf12857b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09d6f045f1e26176704badc902459105cc38b94d2b84961f936773844e9df075`

```dockerfile
```

-	Layers:
	-	`sha256:bb75dfb1e8a87ed594faee6dfd29fe3744905435891a990c608d532312e5c908`  
		Last Modified: Mon, 06 May 2024 23:39:10 GMT  
		Size: 2.3 MB (2261082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b711f312fd8f0ae434954fd2d919960b4b8522210024b2611eb5af0b5de5414`  
		Last Modified: Mon, 06 May 2024 23:39:10 GMT  
		Size: 21.0 KB (20979 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine`

```console
$ docker pull memcached@sha256:4ee2d6582442b4920f0c9de6565947a81e18abc48089804df10251eedf388d66
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
$ docker pull memcached@sha256:cf854f636d506c0834dc1159ad5b472fea96028e88702014088384915a7c08dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6535198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21047320ccba2e62e0ee66c1ffa169149658e039ee012547c37ed6aa0130ad2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59605d18a5ec7e6531bd08f0238da758082d075c4fdd6a4ec8c00fd6f792425b`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8691b75405b7042ea4a853223cc80432131a0e21745f3baf9b21b00073207ace`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 104.2 KB (104211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8925d4d8379f9d71921da012b62d23d71f826e429777c701a1b0d4d56d0399ac`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 3.0 MB (3020613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86013193f6f292637e997c2518f84ab28fec9d7a494cda4090d07457058f10de`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cfe77bbca77075d0b682e8546bca4d6d045cfbff0be0336d51b7bbe1116983`  
		Last Modified: Mon, 06 May 2024 23:08:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d4a846cbc9f47d5db83dbb38f019064556e6af28dad33264b1f851bebbb2858b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ab3ae8df84416fe4351914e6bb061214bfad4b0cb01537aef674b02c008994`

```dockerfile
```

-	Layers:
	-	`sha256:59634fa6bbcc5be09a70b3894761425c9ea7b231a189445bce9ae40b97f09675`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2fd487a2e71a464ab83cce092819d041b742e29af0ecb901bcb36ac21fc7c2c`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 19.5 KB (19475 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:8a6f18eb424270a1dca99143a613014d570cb7376c9cb7d212b72d74c569b12a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6381171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ddcb41c8f4d78c4720e1ad02b3c978ef7af38607d717e52219f0c53ab6fb64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859f5f148ebb49ed2dfc712d036c8e1162fd5c08307e622f420c9e722f459c15`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a85abddca9696d1381e2dbbf52914e6119f22bd22e71c1ffc49aa385ca2d79`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 120.9 KB (120900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f80774db5f2d9cd2ec4f0bf8e7256768ab2ff5b90e1a822c70e5fb0a8d0a42`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 2.9 MB (2910908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fff6ea9e3e8e56264cef5ba1ceaacc5db1aa37fb687bf4cb684629a462a4e04`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e6b3e687f63ee869e2595d746eecfc9a9a64e49c7972eea118f9af26f3a02f`  
		Last Modified: Mon, 06 May 2024 23:43:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7677dd609f55b7dac25e997d7fc4942f1b433f1084ca54e71a01175c8608fedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce1cbd3428e47f29034986dc018cfef4ed121b030aef195db0d03c8a65cc79d`

```dockerfile
```

-	Layers:
	-	`sha256:c80e817fe71d2bd7ff1d9709ab1ac3d7ac30315b7cfd1b528ca1c316fecabc2f`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b568b0dd9cb0ef2428bd10a39e9ee3afe06fe97f6911abc8c1ae5e642b27094`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 19.3 KB (19326 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:1557e39ed6b5f943d53c54797d59f4ea27755c53c9e7004cbfb633c08757abd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6194136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48e3a30b8d39f2e6434ff10c1130366a5bfeac640bc8ecb88f89e6e996cdc4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c853f4fd5c9ee2e18e52b4399ccc43726449928a43d040161f83d3f67f596dd`  
		Last Modified: Mon, 06 May 2024 23:08:35 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca2d91782956c7a9591fd3f9edb724367e6a2770f04a809c6088a8ea623ea7f`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 109.3 KB (109328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5c07db0e07d757431d4458ea14990c3cc0b06aa9577b0e29f8db33fc51921b`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 2.8 MB (2839076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21633262023f9a6ae09f480b39a8a9a7109a0201b779ccdba90e721204cb20ae`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893c3463887c0e33218f5af72fe7534fe9bebd41fd26e976944bbd03c13a9d22`  
		Last Modified: Mon, 06 May 2024 23:08:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:4184448ad3b3ff9a34654847c26c9ad677ce54b07e8a96eedb429e8c509fe5e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04225924b78526836b6ef1d8f4bd3d25e994e9f858bedc4d73fbf5308500d074`

```dockerfile
```

-	Layers:
	-	`sha256:562178e7885ee7492a868cc754c309fe7cf0a52b74299dc570dc9959ecfc0c10`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d1f3d52b695ee750a517e356c17e9f3b6a3778f607f791f558ae9e31397df3f`  
		Last Modified: Mon, 06 May 2024 23:08:35 GMT  
		Size: 19.4 KB (19420 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:4b1fdeda480d0b679c2b9fa5a09c508dabaf7bf0bf1600d0078fcae81e004dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6407037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf112675855fb5780056fbde79f0822c329da1cfb19ca47270289ec2ac966e77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25735f744a453fbf0af2d088f79a0fa6de45cc2699601389d42141b2de2f21d3`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a61320e5e6694b8436a4074ba6280369b9b29e2474231252683fa11606b8e6`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 123.4 KB (123401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e809f0a1acfe802b3158bb0d4d370427885e8c5ba2ce6b98549da9bbac597e`  
		Last Modified: Mon, 06 May 2024 23:39:16 GMT  
		Size: 2.9 MB (2923638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99dc3c24ef4a44c763efcf66a6e3e44d31d723683dd339c343770bd43523007`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0b13828c450ce09acf99d42e4d9e625dbc1991b6f87a5727ff595e3e62a06c`  
		Last Modified: Mon, 06 May 2024 23:39:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d1dc50ec127cc25ab5b90bbe3fccaf4c5cda1379629dcd1760fa93b6cab32718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7934a2d41084621a7a7ff3aafbea88a9edfb76ded1149d611483fb61826d661`

```dockerfile
```

-	Layers:
	-	`sha256:dedf3264102cee8df6c9d7e964dedede98ab6b3865d8df8f76e88eeb42290632`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b25fbb2f936e2b3483885e59398fdcffdf62a984c55d6171eb02b6a8b6ef44d7`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 19.4 KB (19376 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; s390x

```console
$ docker pull memcached@sha256:16979dbfdc08cb52efcfffcdfdff35be32426e49b90065b36155882be545d88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6151853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cca463729a03d73b6abb17295ed77bc6a13a336b4bc01a3b1c03a176f34fa06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
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
	-	`sha256:37d6a06c9130de338c39b57baed51f1e62b01cf60bb33a109ac31927ab8c775f`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 2.8 MB (2794432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db042a56f7b2a4ea616aa34e4b563284ea5d38557c0ff85c04706fc945bc905`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e7dbc7d250abc9822b7e752e47c8b83dd404648d74f9331600b392ac836970`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b885694442ff65cade16142bde9307eda742f797b4c4e48b95e2ecd62c262746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023ebbf730f939171a6dd74509e836130fe404e073174c8b1be5b28fd09e514e`

```dockerfile
```

-	Layers:
	-	`sha256:b18acb410267cb31ce209d09681474ba43f18c2f4af00288845c4061bd220974`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48c7d2c81f6bbcf60c7bbca78ec3114f620154531205c592fe14d252cb9daf08`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 19.3 KB (19309 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine3.19`

```console
$ docker pull memcached@sha256:4ee2d6582442b4920f0c9de6565947a81e18abc48089804df10251eedf388d66
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
$ docker pull memcached@sha256:cf854f636d506c0834dc1159ad5b472fea96028e88702014088384915a7c08dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6535198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21047320ccba2e62e0ee66c1ffa169149658e039ee012547c37ed6aa0130ad2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59605d18a5ec7e6531bd08f0238da758082d075c4fdd6a4ec8c00fd6f792425b`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8691b75405b7042ea4a853223cc80432131a0e21745f3baf9b21b00073207ace`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 104.2 KB (104211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8925d4d8379f9d71921da012b62d23d71f826e429777c701a1b0d4d56d0399ac`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 3.0 MB (3020613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86013193f6f292637e997c2518f84ab28fec9d7a494cda4090d07457058f10de`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cfe77bbca77075d0b682e8546bca4d6d045cfbff0be0336d51b7bbe1116983`  
		Last Modified: Mon, 06 May 2024 23:08:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:d4a846cbc9f47d5db83dbb38f019064556e6af28dad33264b1f851bebbb2858b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ab3ae8df84416fe4351914e6bb061214bfad4b0cb01537aef674b02c008994`

```dockerfile
```

-	Layers:
	-	`sha256:59634fa6bbcc5be09a70b3894761425c9ea7b231a189445bce9ae40b97f09675`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2fd487a2e71a464ab83cce092819d041b742e29af0ecb901bcb36ac21fc7c2c`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 19.5 KB (19475 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:8a6f18eb424270a1dca99143a613014d570cb7376c9cb7d212b72d74c569b12a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6381171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ddcb41c8f4d78c4720e1ad02b3c978ef7af38607d717e52219f0c53ab6fb64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859f5f148ebb49ed2dfc712d036c8e1162fd5c08307e622f420c9e722f459c15`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a85abddca9696d1381e2dbbf52914e6119f22bd22e71c1ffc49aa385ca2d79`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 120.9 KB (120900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f80774db5f2d9cd2ec4f0bf8e7256768ab2ff5b90e1a822c70e5fb0a8d0a42`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 2.9 MB (2910908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fff6ea9e3e8e56264cef5ba1ceaacc5db1aa37fb687bf4cb684629a462a4e04`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e6b3e687f63ee869e2595d746eecfc9a9a64e49c7972eea118f9af26f3a02f`  
		Last Modified: Mon, 06 May 2024 23:43:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:7677dd609f55b7dac25e997d7fc4942f1b433f1084ca54e71a01175c8608fedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce1cbd3428e47f29034986dc018cfef4ed121b030aef195db0d03c8a65cc79d`

```dockerfile
```

-	Layers:
	-	`sha256:c80e817fe71d2bd7ff1d9709ab1ac3d7ac30315b7cfd1b528ca1c316fecabc2f`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b568b0dd9cb0ef2428bd10a39e9ee3afe06fe97f6911abc8c1ae5e642b27094`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 19.3 KB (19326 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.19` - linux; 386

```console
$ docker pull memcached@sha256:1557e39ed6b5f943d53c54797d59f4ea27755c53c9e7004cbfb633c08757abd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6194136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48e3a30b8d39f2e6434ff10c1130366a5bfeac640bc8ecb88f89e6e996cdc4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c853f4fd5c9ee2e18e52b4399ccc43726449928a43d040161f83d3f67f596dd`  
		Last Modified: Mon, 06 May 2024 23:08:35 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca2d91782956c7a9591fd3f9edb724367e6a2770f04a809c6088a8ea623ea7f`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 109.3 KB (109328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5c07db0e07d757431d4458ea14990c3cc0b06aa9577b0e29f8db33fc51921b`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 2.8 MB (2839076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21633262023f9a6ae09f480b39a8a9a7109a0201b779ccdba90e721204cb20ae`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893c3463887c0e33218f5af72fe7534fe9bebd41fd26e976944bbd03c13a9d22`  
		Last Modified: Mon, 06 May 2024 23:08:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:4184448ad3b3ff9a34654847c26c9ad677ce54b07e8a96eedb429e8c509fe5e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04225924b78526836b6ef1d8f4bd3d25e994e9f858bedc4d73fbf5308500d074`

```dockerfile
```

-	Layers:
	-	`sha256:562178e7885ee7492a868cc754c309fe7cf0a52b74299dc570dc9959ecfc0c10`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d1f3d52b695ee750a517e356c17e9f3b6a3778f607f791f558ae9e31397df3f`  
		Last Modified: Mon, 06 May 2024 23:08:35 GMT  
		Size: 19.4 KB (19420 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.19` - linux; ppc64le

```console
$ docker pull memcached@sha256:4b1fdeda480d0b679c2b9fa5a09c508dabaf7bf0bf1600d0078fcae81e004dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6407037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf112675855fb5780056fbde79f0822c329da1cfb19ca47270289ec2ac966e77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25735f744a453fbf0af2d088f79a0fa6de45cc2699601389d42141b2de2f21d3`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a61320e5e6694b8436a4074ba6280369b9b29e2474231252683fa11606b8e6`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 123.4 KB (123401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e809f0a1acfe802b3158bb0d4d370427885e8c5ba2ce6b98549da9bbac597e`  
		Last Modified: Mon, 06 May 2024 23:39:16 GMT  
		Size: 2.9 MB (2923638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99dc3c24ef4a44c763efcf66a6e3e44d31d723683dd339c343770bd43523007`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0b13828c450ce09acf99d42e4d9e625dbc1991b6f87a5727ff595e3e62a06c`  
		Last Modified: Mon, 06 May 2024 23:39:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:d1dc50ec127cc25ab5b90bbe3fccaf4c5cda1379629dcd1760fa93b6cab32718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7934a2d41084621a7a7ff3aafbea88a9edfb76ded1149d611483fb61826d661`

```dockerfile
```

-	Layers:
	-	`sha256:dedf3264102cee8df6c9d7e964dedede98ab6b3865d8df8f76e88eeb42290632`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b25fbb2f936e2b3483885e59398fdcffdf62a984c55d6171eb02b6a8b6ef44d7`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 19.4 KB (19376 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.19` - linux; s390x

```console
$ docker pull memcached@sha256:16979dbfdc08cb52efcfffcdfdff35be32426e49b90065b36155882be545d88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6151853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cca463729a03d73b6abb17295ed77bc6a13a336b4bc01a3b1c03a176f34fa06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
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
	-	`sha256:37d6a06c9130de338c39b57baed51f1e62b01cf60bb33a109ac31927ab8c775f`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 2.8 MB (2794432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db042a56f7b2a4ea616aa34e4b563284ea5d38557c0ff85c04706fc945bc905`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e7dbc7d250abc9822b7e752e47c8b83dd404648d74f9331600b392ac836970`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:b885694442ff65cade16142bde9307eda742f797b4c4e48b95e2ecd62c262746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023ebbf730f939171a6dd74509e836130fe404e073174c8b1be5b28fd09e514e`

```dockerfile
```

-	Layers:
	-	`sha256:b18acb410267cb31ce209d09681474ba43f18c2f4af00288845c4061bd220974`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48c7d2c81f6bbcf60c7bbca78ec3114f620154531205c592fe14d252cb9daf08`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 19.3 KB (19309 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:bookworm`

```console
$ docker pull memcached@sha256:2585b867c96c722e5f4b9d3986a64b3ad67b956f55e31fdf4469f1e5dc157bdc
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
$ docker pull memcached@sha256:29dde2f0a4b996fa7684041ce78bb31e7c2b1a9c8aa6abe467364e8215c57035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38691245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec8c94e66592eab160b4534afad21e21800362694048e80f2c8e82b20c060a78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105cdbf392f0d274b354ff593187bc8b5c883e9087567f7ae4974eea189e7847`  
		Last Modified: Mon, 06 May 2024 23:08:23 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ef4162d3aae0771395e4e1b7ce0c5431fc5fbf987c9c410b7e5b959e302a40`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 2.5 MB (2488488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be957db0d2fe09ea0c4fe874c335ee65f4a0a268476fbc1e646c611ca6b0b1f8`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 7.1 MB (7050761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028dbe498f2fd4131b262e14a863a793bb71221f0cc5b9488822c6a1bb1b0c8c`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7239ceaa87f6c0fc3415c2d6d064020f0b8d2427a548364ecbde0f044094cfdb`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:dce70377f5e30a5563e4d8507edfff7f8947a7575b6ebfe7283407d9fcce4458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c9ef74fba5a31fccf3f549b4fd48b6c4db07bef69a0e574ecb6e9c5bc37448a`

```dockerfile
```

-	Layers:
	-	`sha256:67f37454203d55985eef3fd618246f415a13be9dd32f789dc93d5ee36efcd7e2`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 2.3 MB (2261261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1481c59e0b769395485e713e760e5b60c337edf6600a053a98eaacdcb4a121eb`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 21.1 KB (21146 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:d04280085fd0255be4cf80a6c19c28266f51615eddfe506d718c588dd762a01c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.9 MB (34885683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac68380af8a0798b278fdebe3bfeaf85e0f6d53f505d959ae42ae2eb4de89c15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:53:11 GMT
ADD file:0140ab9be4171f94aae33901f189ffd8822ce6da4a052798883fd66d03b79be9 in / 
# Wed, 24 Apr 2024 03:53:12 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2c9444d4d8a989f4536a8afd8b41a3461ede5b15d490d87c3369b051095d7ae3`  
		Last Modified: Wed, 24 Apr 2024 03:56:28 GMT  
		Size: 26.9 MB (26910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad3b02f635c19a5c749474c01db78c0d1bd9f6465178c236ac42079364c167e`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c82b33e3a41551599953fed1e04a047e0a017d6de973951e88a2319d4eb3b5`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 2.1 MB (2089520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f05e3ac287ed1762995abf279872754c6f943b51b3f1a25e8a2a4b17c08657`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 5.9 MB (5884617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764bff9a4b0a489e9c8c1102b502bf6142559e169252ba08d486d8f0a5b60c90`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e968f84d0f8d617f917f72762217ea784201f4dbd8d958e7c679479a25500e22`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:6bfcd444a59b433ecbc80cb2f9ce87fc6ec5ebc6e20d69b79ab258a8df83d8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1b6d39e43bcacaafbba90473dd410c5e07008c7b5e8f6c5e0053a1cd81e4d2`

```dockerfile
```

-	Layers:
	-	`sha256:d15574302d09f987aff6a1dd074dfa1a5bcf39d50d2488e2bf25204432517fce`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 2.3 MB (2264549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcb55f3be2aa40dd40b859884d496c08b3c104f6782ea068c88df7430c224b5b`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 21.1 KB (21119 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:dcb3196cd0eaf5593a642df75f5c68b0962b89335e489c41d2bd2f50106b2990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.5 MB (38539477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:453e18c2977a4810fadaaeefd26b1cc5b3ddf8aea9a337463475b66a7eb5cf3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea3b2534cc10b3982041c25f3e3e46bc54885fb85a56a850e5d87825605d959`  
		Last Modified: Mon, 06 May 2024 23:40:33 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8c0c56b8ceb323ad11adf63e3d67d815207d779b691a1e144ecbbc509a56c6`  
		Last Modified: Mon, 06 May 2024 23:40:34 GMT  
		Size: 2.3 MB (2346198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b93f0391bd3380825799bef11d6a6236d36dd2a538fddf37ffe5eb89f606aa`  
		Last Modified: Mon, 06 May 2024 23:40:34 GMT  
		Size: 7.0 MB (7011826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5b9d9447753339dd1b2be478d2d2153513530b8476657fe41a93507ac389b2`  
		Last Modified: Mon, 06 May 2024 23:40:33 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd2e6309ee48b90c1469e3408f664e9277e5a348c13026648488c2ac26abc3e`  
		Last Modified: Mon, 06 May 2024 23:40:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:12c2959e59ca59159b3810394cf53899988571d57d4df9c4f0c63950fda39f80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c238d1722683e731e558126fa120d76c1f59a8c0e1fc8cdf25fadb97937810b6`

```dockerfile
```

-	Layers:
	-	`sha256:a23cc33f240eaa7b71c6e81fd3a50f2ba3a4c5c20de8d43766527e3f3cc40832`  
		Last Modified: Mon, 06 May 2024 23:40:34 GMT  
		Size: 2.3 MB (2261490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bc0c2167dc9c0dce55a2cb122d4d7721644ccca44d35b0906c74bac6eb00bfc`  
		Last Modified: Mon, 06 May 2024 23:40:33 GMT  
		Size: 21.0 KB (20997 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; 386

```console
$ docker pull memcached@sha256:3f542cc336b40813213949d5eb8e2da1a57005f88566c0d51c3b8624cc911916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33914242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a44cb325942314e83e433868ace554ffea1c0ef303993f238620f928b36bbcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa82d06bb0cba58ed3fae5da8ee9c6248a027c9d105f1c1e2094d1973ab2f78`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf14cdbfbd6ea1d7231b4119cb6c85336718c7ccee9bc57573aadcc210f05e2`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 2.5 MB (2492686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bed32b6d0ec7a40384a2ba4d5fa14871afba5fd572025e99ebc3c30541ee6bf`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 1.3 MB (1257406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07ba6ac3de2271f181cd17c67b57573da49f54d516ad3c852a2610d138c85b3`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a700f395f10bfe9002c02677754b0a58c0ee8ca0f1fc73477ef1b86dc734103b`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:8932028ec9d6cdd607a57df36f524623a045c35db7110aa26040859db5599b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303c5c842506ac0858dd708f266252ee2b586ba9dd6f506ef93e95c9d4d06402`

```dockerfile
```

-	Layers:
	-	`sha256:e55268858bc5b4c5b04534306d270b5c41b3d3dccd563cae845878933e3d7a1c`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 2.3 MB (2258359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4afdfadae6d39596deea4cc7598059a6d7cdd84a4bf4036bfd609cacb9347c22`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:54a6cf440988b85512b266a181d2e83efe8a6a16530029f48b2fd002efb2e251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38171114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac4ac5a7759abeb1658c052e8e13a0cdc6e05c7af62e12528e0d65428805b7b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:14:18 GMT
ADD file:a3e63beab80160854bfc2d48f69e7c70a9542cdfaf3c5b50f1d6248a998b75ae in / 
# Wed, 24 Apr 2024 03:14:22 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af25825be002e7bdd52bf28c2fbef5bae0ba9fcef8118e5591a874e7a70b2a62`  
		Last Modified: Wed, 24 Apr 2024 03:25:20 GMT  
		Size: 29.1 MB (29144174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70b69867f90cc0cd6ccf8b72f07ee05c80179a59283d6ce971d9191eaf11afe`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361f75ee595f0c436f725a5dd64b1009cb0da358d19361f68345abf27c392f03`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 1.9 MB (1937740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1d3e5a5aad136d9ada8e95bd8e9f609baf923df5c9a48a8021e50206e4e93d`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 7.1 MB (7087680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913b327051e93299424d31038856dead21e1781ab1e47927437d8d135ea97338`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a025835eff1c0dfdae38dce98ddefd33f8609362934acbc3106f445279e8b050`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:062ba12de9ac3ea604948fc8045fa1f18254e15045b75fd40ba397ca49ddac94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f78c9e4c785d57060d12fdc33b3579dde0c50533361c63c38632718921c39d`

```dockerfile
```

-	Layers:
	-	`sha256:0f87aa3b54f1e190b0d04cc9d1960d4d745a6c99015f572091bc1c532c971e12`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:00e8c12c53be74f05f1d407b5e6d79dc9f3c03eaf6bcc42d7fde84b55135c65b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43803388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c5835d941db2f784baf56126916def72cb031f8bf87f0eb9c85d38ab2a99006`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:13 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Wed, 24 Apr 2024 03:21:15 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7fcd02d677f7b314809120f00d6b081965b5807827188e6ebf3081436f54c9`  
		Last Modified: Mon, 06 May 2024 23:36:28 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7857db5dc94e4b30fbaed58c503c6aa7cf416363b6ebd7bfe4eb21d81bd3d54e`  
		Last Modified: Mon, 06 May 2024 23:36:29 GMT  
		Size: 2.7 MB (2698389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4129214713c04309f826d05e9dead290efde58d33f38bf8cc51796ce3d02392`  
		Last Modified: Mon, 06 May 2024 23:36:29 GMT  
		Size: 8.0 MB (7962280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009ed91ac73d01b73721c2c68710b06d4067d836af63780f5260d075df4cfa57`  
		Last Modified: Mon, 06 May 2024 23:36:29 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db194260f1714761a294b97e37fb2d51544c26f4447b3ff81009b1a9a07cd992`  
		Last Modified: Mon, 06 May 2024 23:36:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:577d80832f1718d990d4526e62c1abfd9b09fe17643600c30a82b75a5a0ad018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842a6e10e139ec873043472602e0301d3b0e0d09e7123af5c4739b4da4d20616`

```dockerfile
```

-	Layers:
	-	`sha256:0f8c1c8dfeeac8f6c9be4a58fec56319cd72fb7e52b664e29d21a1f603698b5f`  
		Last Modified: Mon, 06 May 2024 23:36:29 GMT  
		Size: 2.3 MB (2265632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c9b981b4bff189bd3a4d6c0d3c9a51794ea3d75674dc37ed4a0c88494b1d553`  
		Last Modified: Mon, 06 May 2024 23:36:29 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:f1eded0e1e184f274872c917b0898ea33d458ce85cf84dcfdd7fd612ccf43f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35763592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13d7f11723a6c3c0292b7fc87542450d38bec719b123b35792a28d4f0ee5cc3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:43:18 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Wed, 24 Apr 2024 03:43:21 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
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
	-	`sha256:31591ca6b7d175a856e1a87b1fcdba950a0189086a123e820f1638b43fd955e6`  
		Last Modified: Mon, 06 May 2024 23:39:10 GMT  
		Size: 6.1 MB (6097067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf96459eefa11b754c53ffaa240db16c5e7ca96d1187924dadb4717e9001079`  
		Last Modified: Mon, 06 May 2024 23:39:10 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c2b7746d8228729836f11aa3c212bc49ad4769651a8d03525966c158e0e828`  
		Last Modified: Mon, 06 May 2024 23:39:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:38c86b4cfae8572747cee6ca551e6e8e82e52321c96c1c8d178e87febf12857b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09d6f045f1e26176704badc902459105cc38b94d2b84961f936773844e9df075`

```dockerfile
```

-	Layers:
	-	`sha256:bb75dfb1e8a87ed594faee6dfd29fe3744905435891a990c608d532312e5c908`  
		Last Modified: Mon, 06 May 2024 23:39:10 GMT  
		Size: 2.3 MB (2261082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b711f312fd8f0ae434954fd2d919960b4b8522210024b2611eb5af0b5de5414`  
		Last Modified: Mon, 06 May 2024 23:39:10 GMT  
		Size: 21.0 KB (20979 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:latest`

```console
$ docker pull memcached@sha256:2585b867c96c722e5f4b9d3986a64b3ad67b956f55e31fdf4469f1e5dc157bdc
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
$ docker pull memcached@sha256:29dde2f0a4b996fa7684041ce78bb31e7c2b1a9c8aa6abe467364e8215c57035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38691245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec8c94e66592eab160b4534afad21e21800362694048e80f2c8e82b20c060a78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105cdbf392f0d274b354ff593187bc8b5c883e9087567f7ae4974eea189e7847`  
		Last Modified: Mon, 06 May 2024 23:08:23 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ef4162d3aae0771395e4e1b7ce0c5431fc5fbf987c9c410b7e5b959e302a40`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 2.5 MB (2488488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be957db0d2fe09ea0c4fe874c335ee65f4a0a268476fbc1e646c611ca6b0b1f8`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 7.1 MB (7050761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028dbe498f2fd4131b262e14a863a793bb71221f0cc5b9488822c6a1bb1b0c8c`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7239ceaa87f6c0fc3415c2d6d064020f0b8d2427a548364ecbde0f044094cfdb`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:dce70377f5e30a5563e4d8507edfff7f8947a7575b6ebfe7283407d9fcce4458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c9ef74fba5a31fccf3f549b4fd48b6c4db07bef69a0e574ecb6e9c5bc37448a`

```dockerfile
```

-	Layers:
	-	`sha256:67f37454203d55985eef3fd618246f415a13be9dd32f789dc93d5ee36efcd7e2`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 2.3 MB (2261261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1481c59e0b769395485e713e760e5b60c337edf6600a053a98eaacdcb4a121eb`  
		Last Modified: Mon, 06 May 2024 23:08:24 GMT  
		Size: 21.1 KB (21146 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:d04280085fd0255be4cf80a6c19c28266f51615eddfe506d718c588dd762a01c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.9 MB (34885683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac68380af8a0798b278fdebe3bfeaf85e0f6d53f505d959ae42ae2eb4de89c15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:53:11 GMT
ADD file:0140ab9be4171f94aae33901f189ffd8822ce6da4a052798883fd66d03b79be9 in / 
# Wed, 24 Apr 2024 03:53:12 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2c9444d4d8a989f4536a8afd8b41a3461ede5b15d490d87c3369b051095d7ae3`  
		Last Modified: Wed, 24 Apr 2024 03:56:28 GMT  
		Size: 26.9 MB (26910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad3b02f635c19a5c749474c01db78c0d1bd9f6465178c236ac42079364c167e`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c82b33e3a41551599953fed1e04a047e0a017d6de973951e88a2319d4eb3b5`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 2.1 MB (2089520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f05e3ac287ed1762995abf279872754c6f943b51b3f1a25e8a2a4b17c08657`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 5.9 MB (5884617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764bff9a4b0a489e9c8c1102b502bf6142559e169252ba08d486d8f0a5b60c90`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e968f84d0f8d617f917f72762217ea784201f4dbd8d958e7c679479a25500e22`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:6bfcd444a59b433ecbc80cb2f9ce87fc6ec5ebc6e20d69b79ab258a8df83d8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1b6d39e43bcacaafbba90473dd410c5e07008c7b5e8f6c5e0053a1cd81e4d2`

```dockerfile
```

-	Layers:
	-	`sha256:d15574302d09f987aff6a1dd074dfa1a5bcf39d50d2488e2bf25204432517fce`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 2.3 MB (2264549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcb55f3be2aa40dd40b859884d496c08b3c104f6782ea068c88df7430c224b5b`  
		Last Modified: Mon, 06 May 2024 23:13:40 GMT  
		Size: 21.1 KB (21119 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:dcb3196cd0eaf5593a642df75f5c68b0962b89335e489c41d2bd2f50106b2990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.5 MB (38539477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:453e18c2977a4810fadaaeefd26b1cc5b3ddf8aea9a337463475b66a7eb5cf3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea3b2534cc10b3982041c25f3e3e46bc54885fb85a56a850e5d87825605d959`  
		Last Modified: Mon, 06 May 2024 23:40:33 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8c0c56b8ceb323ad11adf63e3d67d815207d779b691a1e144ecbbc509a56c6`  
		Last Modified: Mon, 06 May 2024 23:40:34 GMT  
		Size: 2.3 MB (2346198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b93f0391bd3380825799bef11d6a6236d36dd2a538fddf37ffe5eb89f606aa`  
		Last Modified: Mon, 06 May 2024 23:40:34 GMT  
		Size: 7.0 MB (7011826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5b9d9447753339dd1b2be478d2d2153513530b8476657fe41a93507ac389b2`  
		Last Modified: Mon, 06 May 2024 23:40:33 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd2e6309ee48b90c1469e3408f664e9277e5a348c13026648488c2ac26abc3e`  
		Last Modified: Mon, 06 May 2024 23:40:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:12c2959e59ca59159b3810394cf53899988571d57d4df9c4f0c63950fda39f80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c238d1722683e731e558126fa120d76c1f59a8c0e1fc8cdf25fadb97937810b6`

```dockerfile
```

-	Layers:
	-	`sha256:a23cc33f240eaa7b71c6e81fd3a50f2ba3a4c5c20de8d43766527e3f3cc40832`  
		Last Modified: Mon, 06 May 2024 23:40:34 GMT  
		Size: 2.3 MB (2261490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bc0c2167dc9c0dce55a2cb122d4d7721644ccca44d35b0906c74bac6eb00bfc`  
		Last Modified: Mon, 06 May 2024 23:40:33 GMT  
		Size: 21.0 KB (20997 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:3f542cc336b40813213949d5eb8e2da1a57005f88566c0d51c3b8624cc911916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33914242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a44cb325942314e83e433868ace554ffea1c0ef303993f238620f928b36bbcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa82d06bb0cba58ed3fae5da8ee9c6248a027c9d105f1c1e2094d1973ab2f78`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf14cdbfbd6ea1d7231b4119cb6c85336718c7ccee9bc57573aadcc210f05e2`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 2.5 MB (2492686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bed32b6d0ec7a40384a2ba4d5fa14871afba5fd572025e99ebc3c30541ee6bf`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 1.3 MB (1257406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07ba6ac3de2271f181cd17c67b57573da49f54d516ad3c852a2610d138c85b3`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a700f395f10bfe9002c02677754b0a58c0ee8ca0f1fc73477ef1b86dc734103b`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:8932028ec9d6cdd607a57df36f524623a045c35db7110aa26040859db5599b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303c5c842506ac0858dd708f266252ee2b586ba9dd6f506ef93e95c9d4d06402`

```dockerfile
```

-	Layers:
	-	`sha256:e55268858bc5b4c5b04534306d270b5c41b3d3dccd563cae845878933e3d7a1c`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 2.3 MB (2258359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4afdfadae6d39596deea4cc7598059a6d7cdd84a4bf4036bfd609cacb9347c22`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; mips64le

```console
$ docker pull memcached@sha256:54a6cf440988b85512b266a181d2e83efe8a6a16530029f48b2fd002efb2e251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38171114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac4ac5a7759abeb1658c052e8e13a0cdc6e05c7af62e12528e0d65428805b7b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:14:18 GMT
ADD file:a3e63beab80160854bfc2d48f69e7c70a9542cdfaf3c5b50f1d6248a998b75ae in / 
# Wed, 24 Apr 2024 03:14:22 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af25825be002e7bdd52bf28c2fbef5bae0ba9fcef8118e5591a874e7a70b2a62`  
		Last Modified: Wed, 24 Apr 2024 03:25:20 GMT  
		Size: 29.1 MB (29144174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70b69867f90cc0cd6ccf8b72f07ee05c80179a59283d6ce971d9191eaf11afe`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361f75ee595f0c436f725a5dd64b1009cb0da358d19361f68345abf27c392f03`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 1.9 MB (1937740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1d3e5a5aad136d9ada8e95bd8e9f609baf923df5c9a48a8021e50206e4e93d`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 7.1 MB (7087680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913b327051e93299424d31038856dead21e1781ab1e47927437d8d135ea97338`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a025835eff1c0dfdae38dce98ddefd33f8609362934acbc3106f445279e8b050`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:062ba12de9ac3ea604948fc8045fa1f18254e15045b75fd40ba397ca49ddac94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f78c9e4c785d57060d12fdc33b3579dde0c50533361c63c38632718921c39d`

```dockerfile
```

-	Layers:
	-	`sha256:0f87aa3b54f1e190b0d04cc9d1960d4d745a6c99015f572091bc1c532c971e12`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:00e8c12c53be74f05f1d407b5e6d79dc9f3c03eaf6bcc42d7fde84b55135c65b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43803388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c5835d941db2f784baf56126916def72cb031f8bf87f0eb9c85d38ab2a99006`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:13 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Wed, 24 Apr 2024 03:21:15 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7fcd02d677f7b314809120f00d6b081965b5807827188e6ebf3081436f54c9`  
		Last Modified: Mon, 06 May 2024 23:36:28 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7857db5dc94e4b30fbaed58c503c6aa7cf416363b6ebd7bfe4eb21d81bd3d54e`  
		Last Modified: Mon, 06 May 2024 23:36:29 GMT  
		Size: 2.7 MB (2698389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4129214713c04309f826d05e9dead290efde58d33f38bf8cc51796ce3d02392`  
		Last Modified: Mon, 06 May 2024 23:36:29 GMT  
		Size: 8.0 MB (7962280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009ed91ac73d01b73721c2c68710b06d4067d836af63780f5260d075df4cfa57`  
		Last Modified: Mon, 06 May 2024 23:36:29 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db194260f1714761a294b97e37fb2d51544c26f4447b3ff81009b1a9a07cd992`  
		Last Modified: Mon, 06 May 2024 23:36:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:577d80832f1718d990d4526e62c1abfd9b09fe17643600c30a82b75a5a0ad018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842a6e10e139ec873043472602e0301d3b0e0d09e7123af5c4739b4da4d20616`

```dockerfile
```

-	Layers:
	-	`sha256:0f8c1c8dfeeac8f6c9be4a58fec56319cd72fb7e52b664e29d21a1f603698b5f`  
		Last Modified: Mon, 06 May 2024 23:36:29 GMT  
		Size: 2.3 MB (2265632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c9b981b4bff189bd3a4d6c0d3c9a51794ea3d75674dc37ed4a0c88494b1d553`  
		Last Modified: Mon, 06 May 2024 23:36:29 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:f1eded0e1e184f274872c917b0898ea33d458ce85cf84dcfdd7fd612ccf43f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35763592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13d7f11723a6c3c0292b7fc87542450d38bec719b123b35792a28d4f0ee5cc3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:43:18 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Wed, 24 Apr 2024 03:43:21 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
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
	-	`sha256:31591ca6b7d175a856e1a87b1fcdba950a0189086a123e820f1638b43fd955e6`  
		Last Modified: Mon, 06 May 2024 23:39:10 GMT  
		Size: 6.1 MB (6097067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf96459eefa11b754c53ffaa240db16c5e7ca96d1187924dadb4717e9001079`  
		Last Modified: Mon, 06 May 2024 23:39:10 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c2b7746d8228729836f11aa3c212bc49ad4769651a8d03525966c158e0e828`  
		Last Modified: Mon, 06 May 2024 23:39:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:38c86b4cfae8572747cee6ca551e6e8e82e52321c96c1c8d178e87febf12857b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09d6f045f1e26176704badc902459105cc38b94d2b84961f936773844e9df075`

```dockerfile
```

-	Layers:
	-	`sha256:bb75dfb1e8a87ed594faee6dfd29fe3744905435891a990c608d532312e5c908`  
		Last Modified: Mon, 06 May 2024 23:39:10 GMT  
		Size: 2.3 MB (2261082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b711f312fd8f0ae434954fd2d919960b4b8522210024b2611eb5af0b5de5414`  
		Last Modified: Mon, 06 May 2024 23:39:10 GMT  
		Size: 21.0 KB (20979 bytes)  
		MIME: application/vnd.in-toto+json
