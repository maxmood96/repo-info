<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `memcached`

-	[`memcached:1`](#memcached1)
-	[`memcached:1-alpine`](#memcached1-alpine)
-	[`memcached:1-alpine3.23`](#memcached1-alpine323)
-	[`memcached:1-trixie`](#memcached1-trixie)
-	[`memcached:1.6`](#memcached16)
-	[`memcached:1.6-alpine`](#memcached16-alpine)
-	[`memcached:1.6-alpine3.23`](#memcached16-alpine323)
-	[`memcached:1.6-trixie`](#memcached16-trixie)
-	[`memcached:1.6.39`](#memcached1639)
-	[`memcached:1.6.39-alpine`](#memcached1639-alpine)
-	[`memcached:1.6.39-alpine3.23`](#memcached1639-alpine323)
-	[`memcached:1.6.39-trixie`](#memcached1639-trixie)
-	[`memcached:alpine`](#memcachedalpine)
-	[`memcached:alpine3.23`](#memcachedalpine323)
-	[`memcached:latest`](#memcachedlatest)
-	[`memcached:trixie`](#memcachedtrixie)

## `memcached:1`

```console
$ docker pull memcached@sha256:c7628370ae681c42dbd48ccf02320d77a2bc0234f9ba3a968b5da3a7c0112469
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:1` - linux; amd64

```console
$ docker pull memcached@sha256:153e4ed762fd3bc07fe607f64631647939278d6101759d91fac0b756cceb2272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32208551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa0c800d7278560e11e4d0f14defc4d2d850224d0859d1bd0e9205cc962478d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:38:46 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:38:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:41:30 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:41:30 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:41:30 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:41:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:41:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:41:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:41:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:41:30 GMT
USER memcache
# Mon, 08 Dec 2025 22:41:30 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:41:30 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e33b5452dc8ba5d42cd13b42745898ef870af3e8d5a65b06b8b174f06b1d50`  
		Last Modified: Mon, 08 Dec 2025 22:41:43 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce4ec629da8029212ce5d775073648d04f1f014a89e49f73f1fc848bc405dd5`  
		Last Modified: Mon, 08 Dec 2025 22:41:43 GMT  
		Size: 136.7 KB (136697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6210dfd46759cbe6922de2db75ddf6d17c1f033a434ee6bcf2e82d56ce59f449`  
		Last Modified: Mon, 08 Dec 2025 22:41:43 GMT  
		Size: 2.3 MB (2293845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffbb5d472cb4680299753b978d2e8eeb6d2288ee4caec01e65541f4358516a6`  
		Last Modified: Mon, 08 Dec 2025 22:41:43 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e474cc606bdb91c69d2f124d38e5ebd93ed9ab64d219ab51845cc238a5904aa`  
		Last Modified: Mon, 08 Dec 2025 22:41:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:45cb4f875b600a26ef6e0388db256b09a14580b17ddcaa485fd2c25cbff56056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6483c69793152c682b93375229933004781cbf7df7f059d288d2d7e04335b2c8`

```dockerfile
```

-	Layers:
	-	`sha256:c3beab005b14cd0614637cc43c84460edfb07d9c68b1138ee676ab5bd3dc05ac`  
		Last Modified: Tue, 09 Dec 2025 01:34:56 GMT  
		Size: 2.0 MB (2008228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6ce8cbbfb878c257688fdf1d5e1a9c428b68061ee92f8e07a240ab0fe4b812e`  
		Last Modified: Tue, 09 Dec 2025 01:34:57 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v5

```console
$ docker pull memcached@sha256:5a7b1183ed0a0ca89ce3d88e335fca2672422eee8d05921621cd4ed617965ed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30317206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1552234329fddb68f43cfe1abdf3dff1b1499edbb12eb6d84c481f3d7fbe2c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:34:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:37:32 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:37:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:37:32 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:37:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:37:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:37:32 GMT
USER memcache
# Mon, 08 Dec 2025 22:37:32 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:37:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d97bc71d0fa535127863fdab265dfddb07b3cda35b80de4dd2b9b67fe154c856`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 27.9 MB (27944187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d0d6688f3764bd09c70b0fdb00a12bc517f76c47fc187448da8cf7958b4b98`  
		Last Modified: Mon, 08 Dec 2025 22:37:44 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1a7c3cdaa260d51a1e04177297af5b7e205abe78e98f0782c38369f1a49034`  
		Last Modified: Mon, 08 Dec 2025 22:37:45 GMT  
		Size: 144.1 KB (144146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e35266d4886f5160ecccf89b51e0317cf6c7ad5a063a40d74c0dd0baa75b974`  
		Last Modified: Mon, 08 Dec 2025 22:37:45 GMT  
		Size: 2.2 MB (2227364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3324af035e2f7b73ce2f8c3d5ee46e80ed9063e2ae219caf112d6bafe3d935a3`  
		Last Modified: Mon, 08 Dec 2025 22:37:44 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae7d716f59ff9d69d00b890308b431e236e3a1d530f0dfa1ccaabdd01ea7df2`  
		Last Modified: Mon, 08 Dec 2025 22:37:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:077fa23fa7fd08a421aff7ec84a802bb72f53e3f31c9fb2bba4df39b99ae3923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92bd65e20c21649e0ebcbd5810944fd9e43ecf788ec1d580bfc3c04722bf6fa4`

```dockerfile
```

-	Layers:
	-	`sha256:02c0b341ef4c59b9ffa7a8de46289cbd08d3a3b029c0a64224da804b55e2e854`  
		Last Modified: Tue, 09 Dec 2025 01:35:01 GMT  
		Size: 2.0 MB (2011231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb1ede44c11856b6e3f7c4f6ba238d3df5677af459242c47b9f24b4a1c184db0`  
		Last Modified: Tue, 09 Dec 2025 01:35:02 GMT  
		Size: 22.3 KB (22302 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v7

```console
$ docker pull memcached@sha256:cb9b94d371b2da6a520b577dd688b99c959dac8ad5e81f17aaf8e5b6ed1968ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28529520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a8988937956147836c267576a47663f836997a1d6a21750c17c7d2e52982c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:38:02 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:38:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:41:09 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:41:09 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:41:09 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:41:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:41:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:41:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:41:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:41:09 GMT
USER memcache
# Mon, 08 Dec 2025 22:41:09 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:41:09 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15599337d37fa53f93b66130266f60f942cc7c2c4e2e8458c672f9b61b921350`  
		Last Modified: Mon, 08 Dec 2025 22:41:22 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4e148e811da2c8aeb3f52da0f7e137c9e2dbf7e07ea25ed2a8ec2bc3db340d`  
		Last Modified: Mon, 08 Dec 2025 22:41:25 GMT  
		Size: 135.4 KB (135363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248d1bdc7fd809ba8d6d01e877ae1ff16258cd1b26203215342935af2305c133`  
		Last Modified: Mon, 08 Dec 2025 22:41:22 GMT  
		Size: 2.2 MB (2182634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4dca52427f97b68739a35240dde721713ae992674b8f6fe50fc71d987512c4`  
		Last Modified: Mon, 08 Dec 2025 22:41:22 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2961ef381f352090fe3d59e2ff32ae5c2979defa070a22f5fc846bb2b5f0f30`  
		Last Modified: Mon, 08 Dec 2025 22:41:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:cff996fea1034ca7a74465fdf5489ef45c78f70859319df22468100dc3c84e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e8d92fa13df244234c51ab1b93e9a4c39ad977f40dd5b49cef4e8ed0de7e3a`

```dockerfile
```

-	Layers:
	-	`sha256:d08663eef9d4f14b4b344cf2d8924f04dee694d602df55d600a90830f505069b`  
		Last Modified: Tue, 09 Dec 2025 01:35:06 GMT  
		Size: 2.0 MB (2009688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb1b323cef393d68691ca1f808424d4c4ca9aa868a63329889d55c9e53c30671`  
		Last Modified: Tue, 09 Dec 2025 01:35:06 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:6230125fff57e6f22504aae8db1ed049b738d97c3e325a68a9733a186fab61e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32568877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2f55b9564478802d59f2ab50cadac0b6e11704297ea84bc7fdcc4e9fb3ba76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:38:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:38:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:41:20 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:41:20 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:41:20 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:41:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:41:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:41:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:41:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:41:20 GMT
USER memcache
# Mon, 08 Dec 2025 22:41:20 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:41:20 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91cd2e642e1c9b79606d81fe7ae3f5599c2e1a2ebb80864a1c25f4771502b02`  
		Last Modified: Mon, 08 Dec 2025 22:41:32 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9b5941656d039525e2c86c6dad7b225e0dfe8a89bda1c33c46f84b7e1f05f0`  
		Last Modified: Mon, 08 Dec 2025 22:41:32 GMT  
		Size: 153.5 KB (153454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc829d43c3195e76b119f7ef9e8519d7c64f130e104b29b5317d18e709d3796`  
		Last Modified: Mon, 08 Dec 2025 22:41:32 GMT  
		Size: 2.3 MB (2275286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685e3db2e1ea7f3a85650a5cac398166f6fe54b1767d8ab65fd070fc9f08f903`  
		Last Modified: Mon, 08 Dec 2025 22:41:32 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bedd2011ff5fea2608113c25dac443f7f67fd30b9f049d14304a5eeba342453`  
		Last Modified: Mon, 08 Dec 2025 22:41:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:5be232fd0ce753823a0a00a2e155ca7ed374028d0a228270604974765be63286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ad988781bd90f9b424c8530a983604f0dea5e9ff5d39be9ca322ea793f7044`

```dockerfile
```

-	Layers:
	-	`sha256:2f225cf8fe800d6f4631961cb099b7f796ad28fbe325df7943d5fd182391187f`  
		Last Modified: Tue, 09 Dec 2025 01:35:10 GMT  
		Size: 2.0 MB (2008544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd6800d8108ddffdecd1e6d030f8948b6ed22cff74e19779380d731dfd189d0d`  
		Last Modified: Tue, 09 Dec 2025 01:35:11 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:9c8dd1c0a7d71ffb9540bcdac40c6c72661b05ad12d1a0dcacb86ba0dad353b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33686582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a221f2cf3f75cb38b8be293e0d315a4453967306dc401835f3732a7ec18482d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:17 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:33:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:36:13 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:36:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:36:13 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:36:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:36:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:36:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:36:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:36:13 GMT
USER memcache
# Mon, 08 Dec 2025 22:36:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:36:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c63a49351bc91fd837d81e97ce862507215607bc756f1133f1d887e94e1cc4e`  
		Last Modified: Mon, 08 Dec 2025 22:36:26 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7073e103108a28c5e5a1458be46ac8c708375f2b4327423a59471a77bbf2c0c6`  
		Last Modified: Mon, 08 Dec 2025 22:36:26 GMT  
		Size: 147.5 KB (147516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbfa39b86ad2206ef2fdf5ec3f3a55aa40c422a9f3fca094c7c2f003e7d4a63`  
		Last Modified: Mon, 08 Dec 2025 22:36:26 GMT  
		Size: 2.2 MB (2244483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1ade71ea049e11fc9cea7c16944632ffd753dfe7130e3bb4e1730281daffb5`  
		Last Modified: Mon, 08 Dec 2025 22:36:26 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5eb870312490559d775f9d994ba10b9fcae44c680e23a647a43c1c55f49b54`  
		Last Modified: Mon, 08 Dec 2025 22:36:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:e5ea0a4780f0574f775d4cf8c4ffff6f6b836e33d54d6d241047fa36e54d70b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1425c202287fb1c6f81bb3962bb416b9f23b14b12da6119772ac599ae7af4b`

```dockerfile
```

-	Layers:
	-	`sha256:9d6ed296b190f0f66c6f54ffafa76bd9f86d72e2a463ed9841c2654abf7282d0`  
		Last Modified: Tue, 09 Dec 2025 01:35:16 GMT  
		Size: 2.0 MB (2005385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d9f28b39486b665dcd60f89a225a5fce2e4060feaed50b57eaf89bc54345129`  
		Last Modified: Tue, 09 Dec 2025 01:35:17 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:9a5a8c51d01a2dde31ee88dc7739b61aad1cd244c1592033d64b89e71ea9d086
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36185779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62a722a142df5369183f571c8eecacbc8041e72fb89888b569e2e558947291b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:32:15 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 09 Dec 2025 00:32:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:35:25 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 09 Dec 2025 00:35:25 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 09 Dec 2025 00:35:25 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 09 Dec 2025 00:35:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 09 Dec 2025 00:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 00:35:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 09 Dec 2025 00:35:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Dec 2025 00:35:26 GMT
USER memcache
# Tue, 09 Dec 2025 00:35:26 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 09 Dec 2025 00:35:26 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca80ecfb634d24079bf04d5695260ea9dce9f468064fb83123a71959d22b7c4`  
		Last Modified: Tue, 09 Dec 2025 00:35:51 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb90fb01769b3666ac21d77bcba16bd54161463250fa6f304710eb00d5ab5411`  
		Last Modified: Tue, 09 Dec 2025 00:35:51 GMT  
		Size: 170.4 KB (170375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be675ba49db497b747d37543689ff0b8fc0ef4398cd718c2fadd28302d88141b`  
		Last Modified: Tue, 09 Dec 2025 00:35:51 GMT  
		Size: 2.4 MB (2417005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882b9516d2a74a32203b37778b6025dc9c68a30838e1fa420559c34fe0319141`  
		Last Modified: Tue, 09 Dec 2025 00:35:51 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5cfa5b161387b536b9f8a94f199ffd006893e19e7bff82a8f1f9a7aa578a73`  
		Last Modified: Tue, 09 Dec 2025 00:35:51 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:6ea51b9da9219f68c45e3345bed106b961bce70b2c9aecbb6e1300060e04217d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f87eac26bbbb68ef23dfd63867d0415ddc04fe2567863569701f2891733279d6`

```dockerfile
```

-	Layers:
	-	`sha256:6f8bb9e427f03eea07711eb22a22462b3548d9ed3bf7b82f412aea5a623b10ff`  
		Last Modified: Tue, 09 Dec 2025 04:34:42 GMT  
		Size: 2.0 MB (2011829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1705de570678d9ecda7c8bb1da82748111d8547fb22bfbfb43fbbf41808b5b67`  
		Last Modified: Tue, 09 Dec 2025 04:34:43 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; riscv64

```console
$ docker pull memcached@sha256:05d76bdff41209572f5e6c4d21717d0717a794340a2bc2c086af7a863f5c19af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30627687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c785d7526540c98189bc45e1c3ad5a9862a6ed744c2b49e94165199ba9dcd7ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 10:11:36 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 10:12:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 10:53:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 10:53:11 GMT
USER memcache
# Tue, 18 Nov 2025 10:53:11 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 10:53:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f7062dea9fa0a796a2eacb7b265e4b2000be3d07bc91c20a5abc6538e5a68c`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f8a04356a93113399cb041ac377cf221db2df7d9fc3a6d630a061a923eb1e6`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 133.1 KB (133088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4bbee7a68150daca8b6b94e26e1a04551afc5a77dfb08a4e04aadc0933c456`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 2.2 MB (2219954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085465091dfa79c5f79dd2c74f56f75a8e078b89272039f8d8ed5a1d2adac41b`  
		Last Modified: Tue, 18 Nov 2025 10:54:06 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea3aae46e46f60ca268fd3c445c8b9ed827d7daba7e6d611310cfc9dc4d5291`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:7a8af6c2848585e79b5cb65b6a760b1f78f0de3a59fb604d7a026c79f05a77b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c73002e7361572816b1c22cbb73aced8ce908f6492f2b5d15371b7c0a0514546`

```dockerfile
```

-	Layers:
	-	`sha256:059e3337eaf5c7461d584e0f4b5c7c660bf41a1bb79e90aa917a3992eba4c855`  
		Last Modified: Tue, 18 Nov 2025 16:35:44 GMT  
		Size: 2.0 MB (2002192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cf39200d9e698624fc7d7abe914cab80bda5407ae30f111eb22846e8fd28bba`  
		Last Modified: Tue, 18 Nov 2025 16:35:45 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:332c41cfc207814782dda23a2b840d653abb751f335f7f02f6b238ce79c1c08c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32290312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2be68b3a60f2d8e906983e133fcaffe03bd1a82c9acc69a3dcbe3e307d7b8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:21 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:33:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:36:33 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:36:33 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:36:33 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:36:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:36:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:36:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:36:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:36:34 GMT
USER memcache
# Mon, 08 Dec 2025 22:36:34 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:36:34 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc040aa39039515a9f8b38dc90047178bd8fa0d8234856954f045f05050e52c`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e235f00f3da465d44b7ac18782958812c19e974f091dedfc097442ba632a3d`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 140.5 KB (140505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284c7cc2b7cc68de54eb5bce5de02ed5229cb403476e794b8066eee16babb6e1`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 2.3 MB (2313897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5059135976f7ec26a104b2fb6340b0ae8adc5756ea159deede93c8532613fd24`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd63939e0e5898afa1d51d59354c263e9a7ebfba3e418395baf21445315251de`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:8a7be7ae9cfd628f1585c887ce286f74e97f7780cc20009ffe07f9c92623b34c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c6fbc39d1b80ba4ed6852329a8ddfcaaeed5500129f5019fbc5a8904a7cd659`

```dockerfile
```

-	Layers:
	-	`sha256:0a66a7a3c4891f559fc098f2c13e48d32804e22f559857d3c89074b829300c25`  
		Last Modified: Tue, 09 Dec 2025 01:35:26 GMT  
		Size: 2.0 MB (2009665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24d3a4bbcde50a51a341ad980cc2d92d652ec5f9394c80d55c8a70ded47d8927`  
		Last Modified: Tue, 09 Dec 2025 01:35:27 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:c8503d4491edd3110cc07d0465089d3a41cf1daf8645e71149e39a51835e92cd
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
$ docker pull memcached@sha256:aac456c35cd29635b5501fefac58a2e954752006c9d159fbf520dd785e09cbba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5973577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6411cdd430a5f0c33aea6496062ab90fbc7da776f1c937108cf51b7a40e090f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:20:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:20:42 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:23:18 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:23:18 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:23:18 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:23:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:23:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:23:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:23:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:23:18 GMT
USER memcache
# Thu, 04 Dec 2025 19:23:18 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:23:18 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e377e19df274e9919dbfbe05b510e54db0f8451ac0985b108aba9123048001d8`  
		Last Modified: Thu, 04 Dec 2025 19:23:54 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0d9328fb6b4452be1f62a5c6db62b8425a6b48c40ce2408ae0f526b101c80c`  
		Last Modified: Thu, 04 Dec 2025 19:23:55 GMT  
		Size: 106.0 KB (106047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a1eb06c51acdaf80ce22a4524ea827613ecc609e23cb0fa481005e89b22d4f`  
		Last Modified: Thu, 04 Dec 2025 19:23:54 GMT  
		Size: 2.0 MB (2006867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4829db5772d5079a1be438e2b4d4921e584e88e6becb7ca1819f33cc6ddd962c`  
		Last Modified: Thu, 04 Dec 2025 19:23:54 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b919142486c25c1941bfb65c0f6f26ff49ed2820b62db8ee149ac5a386bcd76c`  
		Last Modified: Thu, 04 Dec 2025 19:23:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:849b937b30f8457f48d4a2b4dee48812e3f3fef3740e8553fbeb950ef1e6a405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3eb9da9040350a8be21d03f2423ac5b520d62898c8656b204d89a46be87cca`

```dockerfile
```

-	Layers:
	-	`sha256:a6a585b25dcf23d45fe100d658f3fc872a69be33f37f5b142951380b902e1a65`  
		Last Modified: Thu, 04 Dec 2025 22:34:43 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91e8f143d354857f78ae4fd0e5416b79eb34dc3599af1f3df2161a4fa1885af9`  
		Last Modified: Thu, 04 Dec 2025 22:34:44 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:a7003e700207ebf4fd102e5d81432129cd3e4776c613ee53fa01b0dbd5e9f19b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5629653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36796824ef2ab4ff08673e2fdd2ff3529a8c6c476c842ec665b90db7e63fad02`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:21:33 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:21:34 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:33:55 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:33:55 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:33:55 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:33:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:33:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:33:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:33:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:33:55 GMT
USER memcache
# Thu, 04 Dec 2025 19:33:55 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:33:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2477fbd5a498e104db4354cbb88ebe3bf7d7f22609c3d9f3996ee3d6f2b311`  
		Last Modified: Thu, 04 Dec 2025 19:34:10 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d610e2e19bb7ad98b2e77e581123187db039c4259f548f8e16e1b5015d0ec85`  
		Last Modified: Thu, 04 Dec 2025 19:34:10 GMT  
		Size: 102.6 KB (102642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5e9f0ad4522a9fedea5ba5229899ef09d25774a89a517cf59cae7a36e4ea92`  
		Last Modified: Thu, 04 Dec 2025 19:34:10 GMT  
		Size: 2.0 MB (1957764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8b426cdf478aef96c3b7780b5b6c81b458a0787358d6251799150a9f714aaf`  
		Last Modified: Thu, 04 Dec 2025 19:34:10 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd456d3218701485ecd1ce99f10c7a08986e44f71d19a49e419582aeb4924f52`  
		Last Modified: Thu, 04 Dec 2025 19:34:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:95ab79e458ab0908467ebbdf5539b688045b04421a068fa6821d557eece2f67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569a816a11d27d030ea4089563f4a23efecb872605941df1c53c0c4152fbd211`

```dockerfile
```

-	Layers:
	-	`sha256:dd9475807057d6ac4c96f526dc77e867efe6bb682d09ef1c7c0557b6f2dad356`  
		Last Modified: Thu, 04 Dec 2025 22:34:47 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:6b1fcd05fdcf13d4b7650d85e6043cdeaf423fe9ec57036c0f203e4eef6bff12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5289618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca393e3ead8035915d8cd6bcea0e8ccbe82d8ae05b9cad79126dd93567ff2889`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:43 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:19:44 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:22:37 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:22:37 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:22:37 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:22:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:22:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:22:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:22:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:22:37 GMT
USER memcache
# Thu, 04 Dec 2025 19:22:37 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:22:37 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdc28d0a8cb5092fb181830a0ef7fb2c55b0dcec915fb49171721470a36990e`  
		Last Modified: Thu, 04 Dec 2025 19:22:53 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d64ac2dd6859410fc8786621ad68f29d5cf9799784bd6181fa0fd9b16f10b5`  
		Last Modified: Thu, 04 Dec 2025 19:22:53 GMT  
		Size: 92.4 KB (92376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf39f9a50690d556c95f99315866a17736de133854b3f4a1f01c007e8ea52e8c`  
		Last Modified: Thu, 04 Dec 2025 19:22:53 GMT  
		Size: 1.9 MB (1917424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5adf2295dafdfb5341494ff56dfa3c9fef413e476cc7e0ea0a44ea325856fd40`  
		Last Modified: Thu, 04 Dec 2025 19:22:53 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f68652d871fbfba49b4bdb6f0555e3d086490ac907f630de1960481a50b5982`  
		Last Modified: Thu, 04 Dec 2025 19:22:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:726bec6c0e6bb11f92cf809b0eff6ee10fc86a30eae935ac85e0b82f2fc110d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:489bd5540d03661ecd23b22a8d9070b7dc18f542d91bc1ed60efaa1790080a39`

```dockerfile
```

-	Layers:
	-	`sha256:35def5ffffb77a9cc93b2d806351b5bc638603257621ee3ea2fcab826508b445`  
		Last Modified: Thu, 04 Dec 2025 22:34:50 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b55f58069fda39e67b560d97ac46c79e035b513a560bc8652e5383cd3f82a35`  
		Last Modified: Thu, 04 Dec 2025 22:34:51 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b263323af06e550df9becd8c2cf8450400be7ae4381392593565dc8247bb230f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6304413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:038de42e33564e147549bf3846c2490c168364063ebc7744c8cdd580e202c191`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:20:28 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:20:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:23:16 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:23:16 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:23:16 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:23:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:23:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:23:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:23:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:23:16 GMT
USER memcache
# Thu, 04 Dec 2025 19:23:16 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:23:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4ea1ce2b4c6bdcd3eec4d60b1aa2e3563da544759bff4e7a46469132a86438`  
		Last Modified: Thu, 04 Dec 2025 19:23:27 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc9938ef133bd132ee91a60f23198ae468dca72e6b547301fc4b29e4136bc9e`  
		Last Modified: Thu, 04 Dec 2025 19:23:28 GMT  
		Size: 121.9 KB (121870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fbb7f498823838642f0cbc3dfbcce9ec16c50549649b23872df57076fed9e7`  
		Last Modified: Thu, 04 Dec 2025 19:23:28 GMT  
		Size: 2.0 MB (1985993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341b9a721d462e12012b285eb88cdd865e1fa62f664d8343c3223d3b18b5ed0c`  
		Last Modified: Thu, 04 Dec 2025 19:23:27 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f879a6e1902c8a256d8dea45afd4efc95caa82bd9fcf3291b6730a20d2c5a0`  
		Last Modified: Thu, 04 Dec 2025 19:23:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9e1d743b77c8856403d4e8420e9936de4aa1bc6fc88642c47112e318e10e2655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556ecd6a50c7ec0f18eea0bb6b6a3c2a30163cdbf6e0a9314ef069819efdb628`

```dockerfile
```

-	Layers:
	-	`sha256:57a22eef052f1e8ba0bdbfa2e165923ea29a9572ab9d397f6652f44a895c34c9`  
		Last Modified: Thu, 04 Dec 2025 22:34:54 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea1714f2bc9b4e6925e95bfc0d324fe4686d662ad257e5959451179599d072e6`  
		Last Modified: Thu, 04 Dec 2025 22:34:55 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:b3d88ad28118ac190ff8cfd6be5b29a4aff4e4f772124ba8a6cb7335eb909152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5762624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfa1253f0cf9e80c36b723ff6f79bb43b3cb4c3146f4340f605aaf0bb812eaa1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:20:00 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:20:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:22:43 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:22:43 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:22:43 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:22:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:22:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:22:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:22:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:22:43 GMT
USER memcache
# Thu, 04 Dec 2025 19:22:43 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:22:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3527b4f952d5950d8caa74dc0d1759215000f2f0a195344f0239c7e2805fe2fc`  
		Last Modified: Wed, 03 Dec 2025 19:30:41 GMT  
		Size: 3.7 MB (3685856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801e2ef7c6c58c48cfc036b3ffd9de546ffd13f67044c4c296b3624d08852398`  
		Last Modified: Thu, 04 Dec 2025 19:22:57 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7528d81de6e75b8aa074f7b96d6b9f2650422ca25fc0f5485dadf33879a4eb7`  
		Last Modified: Thu, 04 Dec 2025 19:22:57 GMT  
		Size: 110.7 KB (110732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40cb203b33be80dad7c861215d0c69239f729987a3942b71d4fc7b17423658e`  
		Last Modified: Thu, 04 Dec 2025 19:22:58 GMT  
		Size: 2.0 MB (1964688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbaa8273de612bce797fce27339a8adb341655d9b03a120aa874e80bfc438ba`  
		Last Modified: Thu, 04 Dec 2025 19:22:57 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a62b5e894734682a138338f04d49ebcb3e61a322469798019f9737e8ef19b33`  
		Last Modified: Thu, 04 Dec 2025 19:22:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:a8428c10b46dc321be308528a9dc3904db404457e03384a035c6e8c7bf32d05e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c97e68a8fd4c390f7dac3c43eda5f00b0b29eb2b838b877b0926ec7a55ec29`

```dockerfile
```

-	Layers:
	-	`sha256:5414f83497841dc88789d15a422792cf5c1818a72a4ebe7fa9f569a4824ce99f`  
		Last Modified: Thu, 04 Dec 2025 22:34:58 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19ce16735c127991fab0a49081d04170d61fc3b2c60261704ec9247a0edc119f`  
		Last Modified: Thu, 04 Dec 2025 22:35:02 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:6ff6570e2a8fb560a3b830e0f1475d488961b29b93e711d03fd52464844926b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6058459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9360c3d396b9f5081cdc222d176f25b51a35c42c688d1ff1da3ad33a71befeb9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:22 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:19:24 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:21:48 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:21:48 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:21:48 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:21:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:21:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:21:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:21:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:21:49 GMT
USER memcache
# Thu, 04 Dec 2025 19:21:49 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:21:49 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23500700235e36a847f2b35c25e17b359b4cec377d3a0fbafdfff7ec561ecf74`  
		Last Modified: Thu, 04 Dec 2025 19:22:05 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47c608c5e84b70e2288ed6c722d682394718aa7029f3614c85bb3faa2d1a0ab`  
		Last Modified: Thu, 04 Dec 2025 19:22:05 GMT  
		Size: 126.3 KB (126267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251cee6c1abe9d3d9e832748d0edb232d4e43fbbdfc78f3fad887409eff7a658`  
		Last Modified: Thu, 04 Dec 2025 19:22:06 GMT  
		Size: 2.1 MB (2103821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82b7a39ab647b07cb8e684e6fbe6e0c40959b95f23e8b6fba544f6412e08e10`  
		Last Modified: Thu, 04 Dec 2025 19:22:05 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e989166bceb7b8bb922420cfda5d2c1c362b469900fbbd86593fb4422e6f2fb6`  
		Last Modified: Thu, 04 Dec 2025 19:22:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ad7264b3f464d43618d5e997d3c544a46d5d00112555908bab3e31ddfb719fd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da20be024f8583ae82747476a5a8b1054a0d2018ceade3cfcc11e0b460a369e3`

```dockerfile
```

-	Layers:
	-	`sha256:08dd8ac2fb865783b3720303c0b7abe96c0d831dd8dbd89f5ce48f64f5d93577`  
		Last Modified: Thu, 04 Dec 2025 22:35:05 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52998ad89b5d31b02c435f1dabae41e0023686389189f0729699301d2b2dceba`  
		Last Modified: Thu, 04 Dec 2025 22:35:06 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:82618728d34fd5e3c642277cb563310bed5e815337b99361c23d0d4225e3a1ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5793289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95bfdee9049204386f5f9675313ec0cf6437686f3e41ac46a02d7491c4ebd031`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:39 GMT
ADD alpine-minirootfs-3.23.0-riscv64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:39 GMT
CMD ["/bin/sh"]
# Fri, 05 Dec 2025 02:28:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 05 Dec 2025 02:28:43 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 05 Dec 2025 02:42:05 GMT
ENV MEMCACHED_VERSION=1.6.39
# Fri, 05 Dec 2025 02:42:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Fri, 05 Dec 2025 02:42:05 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Fri, 05 Dec 2025 02:42:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 05 Dec 2025 02:42:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Dec 2025 02:42:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Dec 2025 02:42:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Dec 2025 02:42:06 GMT
USER memcache
# Fri, 05 Dec 2025 02:42:06 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Dec 2025 02:42:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9929557817a4c85b33d6dbeb491f7396ef32added7e77de7ac1b644ed0975313`  
		Last Modified: Wed, 03 Dec 2025 19:30:17 GMT  
		Size: 3.6 MB (3583519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04477eae70c2e3cb1bd666913116b231bd91f758fef0ce0487128436edf54e3`  
		Last Modified: Fri, 05 Dec 2025 02:42:36 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27775dcc23cac586ff5717daea95b160d3515a30312e73dc28db55554bcbdd12`  
		Last Modified: Fri, 05 Dec 2025 02:42:37 GMT  
		Size: 108.9 KB (108892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d493e7dad99e12ada2c869111712bae9f61d05aabeb2139df6297985982f119`  
		Last Modified: Fri, 05 Dec 2025 02:42:37 GMT  
		Size: 2.1 MB (2099525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf14d0478c213567d1f2646d01cd27ca8c3db42c197fceb2c2fe55c1ea5bfd84`  
		Last Modified: Fri, 05 Dec 2025 02:42:37 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb60cadd22d3f64cee1f02bcfccb5472502730fea2408ffa893c00d4cae9e97c`  
		Last Modified: Fri, 05 Dec 2025 02:42:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:6607c3431ad2ac598c8476330688ee82114c9b3c0e9b2849f86d95addf5e48eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8406d4978e549630fb362ff2901a3645f7d325e1cce867bbfddade8ceb14232`

```dockerfile
```

-	Layers:
	-	`sha256:5ae6f5f57506c9cba95d087771e8253c7ee7c129dcbc4fdd524a99f4feeafec9`  
		Last Modified: Fri, 05 Dec 2025 04:34:37 GMT  
		Size: 94.3 KB (94276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b9a49d787a1cd02fea8b8affc293bd2d718765b8ef3d8cf26d839f80d072eea`  
		Last Modified: Fri, 05 Dec 2025 04:34:38 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:b23b3b07e717d7651a02ec547a675f198e684f410c7217a09bd305de6c20e664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5878802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e586dd7e72674888df0e6f0ade73d053d2a5a94b7d890a276fb6f13fba7e4cc3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:22 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:19:24 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:22:39 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:22:39 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:22:39 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:22:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:22:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:22:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:22:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:22:39 GMT
USER memcache
# Thu, 04 Dec 2025 19:22:39 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:22:39 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a188510a1e7e85e0e83a71da1abed06b459c07887a679cf331da7789673755`  
		Last Modified: Thu, 04 Dec 2025 19:23:03 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67afe5cdcebd55aec1e59a816853f758650056c83c63ea4d99d6e06e15f60fd`  
		Last Modified: Thu, 04 Dec 2025 19:23:03 GMT  
		Size: 114.3 KB (114286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377a08e6b7dd38664aeee34c52a61b8f7edf9165adabbaee0e0b923423a60242`  
		Last Modified: Thu, 04 Dec 2025 19:23:03 GMT  
		Size: 2.0 MB (2039357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c47067ba1641d8aa2a1f3d7df1e359c1ef226673c5b60eeecc3824f3609e9b`  
		Last Modified: Thu, 04 Dec 2025 19:23:03 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e307cf70f379099e1c944f0972ea3478099fc2221e7ae304d3c47858cb9c8b`  
		Last Modified: Thu, 04 Dec 2025 19:23:03 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:db1f4e6b802cb9b4ee6a404e244522a143516b6c5dfe88d706e7d657e8a3c6c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e21cb3a2b9f702a014eac05118559131c607052ca17bd1adb7ddb02107d291d0`

```dockerfile
```

-	Layers:
	-	`sha256:a484d75866b9f2198dfeccc7d70aa01018c27dd00a8bdad7b47bb8f659ee35d1`  
		Last Modified: Thu, 04 Dec 2025 22:35:09 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e39d44972f86c94e48a8ba761774c90c693cfd7248b9b3fa84a7905217f0c57a`  
		Last Modified: Thu, 04 Dec 2025 22:35:10 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine3.23`

```console
$ docker pull memcached@sha256:c8503d4491edd3110cc07d0465089d3a41cf1daf8645e71149e39a51835e92cd
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

### `memcached:1-alpine3.23` - linux; amd64

```console
$ docker pull memcached@sha256:aac456c35cd29635b5501fefac58a2e954752006c9d159fbf520dd785e09cbba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5973577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6411cdd430a5f0c33aea6496062ab90fbc7da776f1c937108cf51b7a40e090f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:20:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:20:42 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:23:18 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:23:18 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:23:18 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:23:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:23:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:23:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:23:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:23:18 GMT
USER memcache
# Thu, 04 Dec 2025 19:23:18 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:23:18 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e377e19df274e9919dbfbe05b510e54db0f8451ac0985b108aba9123048001d8`  
		Last Modified: Thu, 04 Dec 2025 19:23:54 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0d9328fb6b4452be1f62a5c6db62b8425a6b48c40ce2408ae0f526b101c80c`  
		Last Modified: Thu, 04 Dec 2025 19:23:55 GMT  
		Size: 106.0 KB (106047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a1eb06c51acdaf80ce22a4524ea827613ecc609e23cb0fa481005e89b22d4f`  
		Last Modified: Thu, 04 Dec 2025 19:23:54 GMT  
		Size: 2.0 MB (2006867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4829db5772d5079a1be438e2b4d4921e584e88e6becb7ca1819f33cc6ddd962c`  
		Last Modified: Thu, 04 Dec 2025 19:23:54 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b919142486c25c1941bfb65c0f6f26ff49ed2820b62db8ee149ac5a386bcd76c`  
		Last Modified: Thu, 04 Dec 2025 19:23:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:849b937b30f8457f48d4a2b4dee48812e3f3fef3740e8553fbeb950ef1e6a405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3eb9da9040350a8be21d03f2423ac5b520d62898c8656b204d89a46be87cca`

```dockerfile
```

-	Layers:
	-	`sha256:a6a585b25dcf23d45fe100d658f3fc872a69be33f37f5b142951380b902e1a65`  
		Last Modified: Thu, 04 Dec 2025 22:34:43 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91e8f143d354857f78ae4fd0e5416b79eb34dc3599af1f3df2161a4fa1885af9`  
		Last Modified: Thu, 04 Dec 2025 22:34:44 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; arm variant v6

```console
$ docker pull memcached@sha256:a7003e700207ebf4fd102e5d81432129cd3e4776c613ee53fa01b0dbd5e9f19b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5629653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36796824ef2ab4ff08673e2fdd2ff3529a8c6c476c842ec665b90db7e63fad02`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:21:33 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:21:34 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:33:55 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:33:55 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:33:55 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:33:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:33:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:33:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:33:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:33:55 GMT
USER memcache
# Thu, 04 Dec 2025 19:33:55 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:33:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2477fbd5a498e104db4354cbb88ebe3bf7d7f22609c3d9f3996ee3d6f2b311`  
		Last Modified: Thu, 04 Dec 2025 19:34:10 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d610e2e19bb7ad98b2e77e581123187db039c4259f548f8e16e1b5015d0ec85`  
		Last Modified: Thu, 04 Dec 2025 19:34:10 GMT  
		Size: 102.6 KB (102642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5e9f0ad4522a9fedea5ba5229899ef09d25774a89a517cf59cae7a36e4ea92`  
		Last Modified: Thu, 04 Dec 2025 19:34:10 GMT  
		Size: 2.0 MB (1957764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8b426cdf478aef96c3b7780b5b6c81b458a0787358d6251799150a9f714aaf`  
		Last Modified: Thu, 04 Dec 2025 19:34:10 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd456d3218701485ecd1ce99f10c7a08986e44f71d19a49e419582aeb4924f52`  
		Last Modified: Thu, 04 Dec 2025 19:34:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:95ab79e458ab0908467ebbdf5539b688045b04421a068fa6821d557eece2f67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569a816a11d27d030ea4089563f4a23efecb872605941df1c53c0c4152fbd211`

```dockerfile
```

-	Layers:
	-	`sha256:dd9475807057d6ac4c96f526dc77e867efe6bb682d09ef1c7c0557b6f2dad356`  
		Last Modified: Thu, 04 Dec 2025 22:34:47 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; arm variant v7

```console
$ docker pull memcached@sha256:6b1fcd05fdcf13d4b7650d85e6043cdeaf423fe9ec57036c0f203e4eef6bff12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5289618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca393e3ead8035915d8cd6bcea0e8ccbe82d8ae05b9cad79126dd93567ff2889`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:43 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:19:44 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:22:37 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:22:37 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:22:37 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:22:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:22:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:22:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:22:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:22:37 GMT
USER memcache
# Thu, 04 Dec 2025 19:22:37 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:22:37 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdc28d0a8cb5092fb181830a0ef7fb2c55b0dcec915fb49171721470a36990e`  
		Last Modified: Thu, 04 Dec 2025 19:22:53 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d64ac2dd6859410fc8786621ad68f29d5cf9799784bd6181fa0fd9b16f10b5`  
		Last Modified: Thu, 04 Dec 2025 19:22:53 GMT  
		Size: 92.4 KB (92376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf39f9a50690d556c95f99315866a17736de133854b3f4a1f01c007e8ea52e8c`  
		Last Modified: Thu, 04 Dec 2025 19:22:53 GMT  
		Size: 1.9 MB (1917424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5adf2295dafdfb5341494ff56dfa3c9fef413e476cc7e0ea0a44ea325856fd40`  
		Last Modified: Thu, 04 Dec 2025 19:22:53 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f68652d871fbfba49b4bdb6f0555e3d086490ac907f630de1960481a50b5982`  
		Last Modified: Thu, 04 Dec 2025 19:22:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:726bec6c0e6bb11f92cf809b0eff6ee10fc86a30eae935ac85e0b82f2fc110d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:489bd5540d03661ecd23b22a8d9070b7dc18f542d91bc1ed60efaa1790080a39`

```dockerfile
```

-	Layers:
	-	`sha256:35def5ffffb77a9cc93b2d806351b5bc638603257621ee3ea2fcab826508b445`  
		Last Modified: Thu, 04 Dec 2025 22:34:50 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b55f58069fda39e67b560d97ac46c79e035b513a560bc8652e5383cd3f82a35`  
		Last Modified: Thu, 04 Dec 2025 22:34:51 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b263323af06e550df9becd8c2cf8450400be7ae4381392593565dc8247bb230f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6304413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:038de42e33564e147549bf3846c2490c168364063ebc7744c8cdd580e202c191`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:20:28 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:20:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:23:16 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:23:16 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:23:16 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:23:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:23:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:23:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:23:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:23:16 GMT
USER memcache
# Thu, 04 Dec 2025 19:23:16 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:23:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4ea1ce2b4c6bdcd3eec4d60b1aa2e3563da544759bff4e7a46469132a86438`  
		Last Modified: Thu, 04 Dec 2025 19:23:27 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc9938ef133bd132ee91a60f23198ae468dca72e6b547301fc4b29e4136bc9e`  
		Last Modified: Thu, 04 Dec 2025 19:23:28 GMT  
		Size: 121.9 KB (121870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fbb7f498823838642f0cbc3dfbcce9ec16c50549649b23872df57076fed9e7`  
		Last Modified: Thu, 04 Dec 2025 19:23:28 GMT  
		Size: 2.0 MB (1985993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341b9a721d462e12012b285eb88cdd865e1fa62f664d8343c3223d3b18b5ed0c`  
		Last Modified: Thu, 04 Dec 2025 19:23:27 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f879a6e1902c8a256d8dea45afd4efc95caa82bd9fcf3291b6730a20d2c5a0`  
		Last Modified: Thu, 04 Dec 2025 19:23:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:9e1d743b77c8856403d4e8420e9936de4aa1bc6fc88642c47112e318e10e2655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556ecd6a50c7ec0f18eea0bb6b6a3c2a30163cdbf6e0a9314ef069819efdb628`

```dockerfile
```

-	Layers:
	-	`sha256:57a22eef052f1e8ba0bdbfa2e165923ea29a9572ab9d397f6652f44a895c34c9`  
		Last Modified: Thu, 04 Dec 2025 22:34:54 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea1714f2bc9b4e6925e95bfc0d324fe4686d662ad257e5959451179599d072e6`  
		Last Modified: Thu, 04 Dec 2025 22:34:55 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; 386

```console
$ docker pull memcached@sha256:b3d88ad28118ac190ff8cfd6be5b29a4aff4e4f772124ba8a6cb7335eb909152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5762624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfa1253f0cf9e80c36b723ff6f79bb43b3cb4c3146f4340f605aaf0bb812eaa1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:20:00 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:20:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:22:43 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:22:43 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:22:43 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:22:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:22:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:22:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:22:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:22:43 GMT
USER memcache
# Thu, 04 Dec 2025 19:22:43 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:22:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3527b4f952d5950d8caa74dc0d1759215000f2f0a195344f0239c7e2805fe2fc`  
		Last Modified: Wed, 03 Dec 2025 19:30:41 GMT  
		Size: 3.7 MB (3685856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801e2ef7c6c58c48cfc036b3ffd9de546ffd13f67044c4c296b3624d08852398`  
		Last Modified: Thu, 04 Dec 2025 19:22:57 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7528d81de6e75b8aa074f7b96d6b9f2650422ca25fc0f5485dadf33879a4eb7`  
		Last Modified: Thu, 04 Dec 2025 19:22:57 GMT  
		Size: 110.7 KB (110732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40cb203b33be80dad7c861215d0c69239f729987a3942b71d4fc7b17423658e`  
		Last Modified: Thu, 04 Dec 2025 19:22:58 GMT  
		Size: 2.0 MB (1964688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbaa8273de612bce797fce27339a8adb341655d9b03a120aa874e80bfc438ba`  
		Last Modified: Thu, 04 Dec 2025 19:22:57 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a62b5e894734682a138338f04d49ebcb3e61a322469798019f9737e8ef19b33`  
		Last Modified: Thu, 04 Dec 2025 19:22:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:a8428c10b46dc321be308528a9dc3904db404457e03384a035c6e8c7bf32d05e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c97e68a8fd4c390f7dac3c43eda5f00b0b29eb2b838b877b0926ec7a55ec29`

```dockerfile
```

-	Layers:
	-	`sha256:5414f83497841dc88789d15a422792cf5c1818a72a4ebe7fa9f569a4824ce99f`  
		Last Modified: Thu, 04 Dec 2025 22:34:58 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19ce16735c127991fab0a49081d04170d61fc3b2c60261704ec9247a0edc119f`  
		Last Modified: Thu, 04 Dec 2025 22:35:02 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; ppc64le

```console
$ docker pull memcached@sha256:6ff6570e2a8fb560a3b830e0f1475d488961b29b93e711d03fd52464844926b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6058459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9360c3d396b9f5081cdc222d176f25b51a35c42c688d1ff1da3ad33a71befeb9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:22 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:19:24 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:21:48 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:21:48 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:21:48 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:21:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:21:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:21:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:21:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:21:49 GMT
USER memcache
# Thu, 04 Dec 2025 19:21:49 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:21:49 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23500700235e36a847f2b35c25e17b359b4cec377d3a0fbafdfff7ec561ecf74`  
		Last Modified: Thu, 04 Dec 2025 19:22:05 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47c608c5e84b70e2288ed6c722d682394718aa7029f3614c85bb3faa2d1a0ab`  
		Last Modified: Thu, 04 Dec 2025 19:22:05 GMT  
		Size: 126.3 KB (126267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251cee6c1abe9d3d9e832748d0edb232d4e43fbbdfc78f3fad887409eff7a658`  
		Last Modified: Thu, 04 Dec 2025 19:22:06 GMT  
		Size: 2.1 MB (2103821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82b7a39ab647b07cb8e684e6fbe6e0c40959b95f23e8b6fba544f6412e08e10`  
		Last Modified: Thu, 04 Dec 2025 19:22:05 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e989166bceb7b8bb922420cfda5d2c1c362b469900fbbd86593fb4422e6f2fb6`  
		Last Modified: Thu, 04 Dec 2025 19:22:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:ad7264b3f464d43618d5e997d3c544a46d5d00112555908bab3e31ddfb719fd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da20be024f8583ae82747476a5a8b1054a0d2018ceade3cfcc11e0b460a369e3`

```dockerfile
```

-	Layers:
	-	`sha256:08dd8ac2fb865783b3720303c0b7abe96c0d831dd8dbd89f5ce48f64f5d93577`  
		Last Modified: Thu, 04 Dec 2025 22:35:05 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52998ad89b5d31b02c435f1dabae41e0023686389189f0729699301d2b2dceba`  
		Last Modified: Thu, 04 Dec 2025 22:35:06 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; riscv64

```console
$ docker pull memcached@sha256:82618728d34fd5e3c642277cb563310bed5e815337b99361c23d0d4225e3a1ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5793289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95bfdee9049204386f5f9675313ec0cf6437686f3e41ac46a02d7491c4ebd031`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:39 GMT
ADD alpine-minirootfs-3.23.0-riscv64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:39 GMT
CMD ["/bin/sh"]
# Fri, 05 Dec 2025 02:28:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 05 Dec 2025 02:28:43 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 05 Dec 2025 02:42:05 GMT
ENV MEMCACHED_VERSION=1.6.39
# Fri, 05 Dec 2025 02:42:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Fri, 05 Dec 2025 02:42:05 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Fri, 05 Dec 2025 02:42:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 05 Dec 2025 02:42:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Dec 2025 02:42:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Dec 2025 02:42:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Dec 2025 02:42:06 GMT
USER memcache
# Fri, 05 Dec 2025 02:42:06 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Dec 2025 02:42:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9929557817a4c85b33d6dbeb491f7396ef32added7e77de7ac1b644ed0975313`  
		Last Modified: Wed, 03 Dec 2025 19:30:17 GMT  
		Size: 3.6 MB (3583519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04477eae70c2e3cb1bd666913116b231bd91f758fef0ce0487128436edf54e3`  
		Last Modified: Fri, 05 Dec 2025 02:42:36 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27775dcc23cac586ff5717daea95b160d3515a30312e73dc28db55554bcbdd12`  
		Last Modified: Fri, 05 Dec 2025 02:42:37 GMT  
		Size: 108.9 KB (108892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d493e7dad99e12ada2c869111712bae9f61d05aabeb2139df6297985982f119`  
		Last Modified: Fri, 05 Dec 2025 02:42:37 GMT  
		Size: 2.1 MB (2099525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf14d0478c213567d1f2646d01cd27ca8c3db42c197fceb2c2fe55c1ea5bfd84`  
		Last Modified: Fri, 05 Dec 2025 02:42:37 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb60cadd22d3f64cee1f02bcfccb5472502730fea2408ffa893c00d4cae9e97c`  
		Last Modified: Fri, 05 Dec 2025 02:42:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:6607c3431ad2ac598c8476330688ee82114c9b3c0e9b2849f86d95addf5e48eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8406d4978e549630fb362ff2901a3645f7d325e1cce867bbfddade8ceb14232`

```dockerfile
```

-	Layers:
	-	`sha256:5ae6f5f57506c9cba95d087771e8253c7ee7c129dcbc4fdd524a99f4feeafec9`  
		Last Modified: Fri, 05 Dec 2025 04:34:37 GMT  
		Size: 94.3 KB (94276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b9a49d787a1cd02fea8b8affc293bd2d718765b8ef3d8cf26d839f80d072eea`  
		Last Modified: Fri, 05 Dec 2025 04:34:38 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; s390x

```console
$ docker pull memcached@sha256:b23b3b07e717d7651a02ec547a675f198e684f410c7217a09bd305de6c20e664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5878802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e586dd7e72674888df0e6f0ade73d053d2a5a94b7d890a276fb6f13fba7e4cc3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:22 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:19:24 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:22:39 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:22:39 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:22:39 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:22:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:22:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:22:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:22:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:22:39 GMT
USER memcache
# Thu, 04 Dec 2025 19:22:39 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:22:39 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a188510a1e7e85e0e83a71da1abed06b459c07887a679cf331da7789673755`  
		Last Modified: Thu, 04 Dec 2025 19:23:03 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67afe5cdcebd55aec1e59a816853f758650056c83c63ea4d99d6e06e15f60fd`  
		Last Modified: Thu, 04 Dec 2025 19:23:03 GMT  
		Size: 114.3 KB (114286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377a08e6b7dd38664aeee34c52a61b8f7edf9165adabbaee0e0b923423a60242`  
		Last Modified: Thu, 04 Dec 2025 19:23:03 GMT  
		Size: 2.0 MB (2039357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c47067ba1641d8aa2a1f3d7df1e359c1ef226673c5b60eeecc3824f3609e9b`  
		Last Modified: Thu, 04 Dec 2025 19:23:03 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e307cf70f379099e1c944f0972ea3478099fc2221e7ae304d3c47858cb9c8b`  
		Last Modified: Thu, 04 Dec 2025 19:23:03 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:db1f4e6b802cb9b4ee6a404e244522a143516b6c5dfe88d706e7d657e8a3c6c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e21cb3a2b9f702a014eac05118559131c607052ca17bd1adb7ddb02107d291d0`

```dockerfile
```

-	Layers:
	-	`sha256:a484d75866b9f2198dfeccc7d70aa01018c27dd00a8bdad7b47bb8f659ee35d1`  
		Last Modified: Thu, 04 Dec 2025 22:35:09 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e39d44972f86c94e48a8ba761774c90c693cfd7248b9b3fa84a7905217f0c57a`  
		Last Modified: Thu, 04 Dec 2025 22:35:10 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-trixie`

```console
$ docker pull memcached@sha256:c7628370ae681c42dbd48ccf02320d77a2bc0234f9ba3a968b5da3a7c0112469
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:1-trixie` - linux; amd64

```console
$ docker pull memcached@sha256:153e4ed762fd3bc07fe607f64631647939278d6101759d91fac0b756cceb2272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32208551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa0c800d7278560e11e4d0f14defc4d2d850224d0859d1bd0e9205cc962478d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:38:46 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:38:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:41:30 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:41:30 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:41:30 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:41:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:41:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:41:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:41:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:41:30 GMT
USER memcache
# Mon, 08 Dec 2025 22:41:30 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:41:30 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e33b5452dc8ba5d42cd13b42745898ef870af3e8d5a65b06b8b174f06b1d50`  
		Last Modified: Mon, 08 Dec 2025 22:41:43 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce4ec629da8029212ce5d775073648d04f1f014a89e49f73f1fc848bc405dd5`  
		Last Modified: Mon, 08 Dec 2025 22:41:43 GMT  
		Size: 136.7 KB (136697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6210dfd46759cbe6922de2db75ddf6d17c1f033a434ee6bcf2e82d56ce59f449`  
		Last Modified: Mon, 08 Dec 2025 22:41:43 GMT  
		Size: 2.3 MB (2293845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffbb5d472cb4680299753b978d2e8eeb6d2288ee4caec01e65541f4358516a6`  
		Last Modified: Mon, 08 Dec 2025 22:41:43 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e474cc606bdb91c69d2f124d38e5ebd93ed9ab64d219ab51845cc238a5904aa`  
		Last Modified: Mon, 08 Dec 2025 22:41:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:45cb4f875b600a26ef6e0388db256b09a14580b17ddcaa485fd2c25cbff56056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6483c69793152c682b93375229933004781cbf7df7f059d288d2d7e04335b2c8`

```dockerfile
```

-	Layers:
	-	`sha256:c3beab005b14cd0614637cc43c84460edfb07d9c68b1138ee676ab5bd3dc05ac`  
		Last Modified: Tue, 09 Dec 2025 01:34:56 GMT  
		Size: 2.0 MB (2008228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6ce8cbbfb878c257688fdf1d5e1a9c428b68061ee92f8e07a240ab0fe4b812e`  
		Last Modified: Tue, 09 Dec 2025 01:34:57 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:5a7b1183ed0a0ca89ce3d88e335fca2672422eee8d05921621cd4ed617965ed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30317206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1552234329fddb68f43cfe1abdf3dff1b1499edbb12eb6d84c481f3d7fbe2c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:34:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:37:32 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:37:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:37:32 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:37:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:37:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:37:32 GMT
USER memcache
# Mon, 08 Dec 2025 22:37:32 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:37:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d97bc71d0fa535127863fdab265dfddb07b3cda35b80de4dd2b9b67fe154c856`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 27.9 MB (27944187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d0d6688f3764bd09c70b0fdb00a12bc517f76c47fc187448da8cf7958b4b98`  
		Last Modified: Mon, 08 Dec 2025 22:37:44 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1a7c3cdaa260d51a1e04177297af5b7e205abe78e98f0782c38369f1a49034`  
		Last Modified: Mon, 08 Dec 2025 22:37:45 GMT  
		Size: 144.1 KB (144146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e35266d4886f5160ecccf89b51e0317cf6c7ad5a063a40d74c0dd0baa75b974`  
		Last Modified: Mon, 08 Dec 2025 22:37:45 GMT  
		Size: 2.2 MB (2227364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3324af035e2f7b73ce2f8c3d5ee46e80ed9063e2ae219caf112d6bafe3d935a3`  
		Last Modified: Mon, 08 Dec 2025 22:37:44 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae7d716f59ff9d69d00b890308b431e236e3a1d530f0dfa1ccaabdd01ea7df2`  
		Last Modified: Mon, 08 Dec 2025 22:37:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:077fa23fa7fd08a421aff7ec84a802bb72f53e3f31c9fb2bba4df39b99ae3923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92bd65e20c21649e0ebcbd5810944fd9e43ecf788ec1d580bfc3c04722bf6fa4`

```dockerfile
```

-	Layers:
	-	`sha256:02c0b341ef4c59b9ffa7a8de46289cbd08d3a3b029c0a64224da804b55e2e854`  
		Last Modified: Tue, 09 Dec 2025 01:35:01 GMT  
		Size: 2.0 MB (2011231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb1ede44c11856b6e3f7c4f6ba238d3df5677af459242c47b9f24b4a1c184db0`  
		Last Modified: Tue, 09 Dec 2025 01:35:02 GMT  
		Size: 22.3 KB (22302 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:cb9b94d371b2da6a520b577dd688b99c959dac8ad5e81f17aaf8e5b6ed1968ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28529520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a8988937956147836c267576a47663f836997a1d6a21750c17c7d2e52982c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:38:02 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:38:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:41:09 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:41:09 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:41:09 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:41:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:41:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:41:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:41:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:41:09 GMT
USER memcache
# Mon, 08 Dec 2025 22:41:09 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:41:09 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15599337d37fa53f93b66130266f60f942cc7c2c4e2e8458c672f9b61b921350`  
		Last Modified: Mon, 08 Dec 2025 22:41:22 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4e148e811da2c8aeb3f52da0f7e137c9e2dbf7e07ea25ed2a8ec2bc3db340d`  
		Last Modified: Mon, 08 Dec 2025 22:41:25 GMT  
		Size: 135.4 KB (135363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248d1bdc7fd809ba8d6d01e877ae1ff16258cd1b26203215342935af2305c133`  
		Last Modified: Mon, 08 Dec 2025 22:41:22 GMT  
		Size: 2.2 MB (2182634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4dca52427f97b68739a35240dde721713ae992674b8f6fe50fc71d987512c4`  
		Last Modified: Mon, 08 Dec 2025 22:41:22 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2961ef381f352090fe3d59e2ff32ae5c2979defa070a22f5fc846bb2b5f0f30`  
		Last Modified: Mon, 08 Dec 2025 22:41:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:cff996fea1034ca7a74465fdf5489ef45c78f70859319df22468100dc3c84e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e8d92fa13df244234c51ab1b93e9a4c39ad977f40dd5b49cef4e8ed0de7e3a`

```dockerfile
```

-	Layers:
	-	`sha256:d08663eef9d4f14b4b344cf2d8924f04dee694d602df55d600a90830f505069b`  
		Last Modified: Tue, 09 Dec 2025 01:35:06 GMT  
		Size: 2.0 MB (2009688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb1b323cef393d68691ca1f808424d4c4ca9aa868a63329889d55c9e53c30671`  
		Last Modified: Tue, 09 Dec 2025 01:35:06 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:6230125fff57e6f22504aae8db1ed049b738d97c3e325a68a9733a186fab61e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32568877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2f55b9564478802d59f2ab50cadac0b6e11704297ea84bc7fdcc4e9fb3ba76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:38:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:38:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:41:20 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:41:20 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:41:20 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:41:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:41:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:41:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:41:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:41:20 GMT
USER memcache
# Mon, 08 Dec 2025 22:41:20 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:41:20 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91cd2e642e1c9b79606d81fe7ae3f5599c2e1a2ebb80864a1c25f4771502b02`  
		Last Modified: Mon, 08 Dec 2025 22:41:32 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9b5941656d039525e2c86c6dad7b225e0dfe8a89bda1c33c46f84b7e1f05f0`  
		Last Modified: Mon, 08 Dec 2025 22:41:32 GMT  
		Size: 153.5 KB (153454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc829d43c3195e76b119f7ef9e8519d7c64f130e104b29b5317d18e709d3796`  
		Last Modified: Mon, 08 Dec 2025 22:41:32 GMT  
		Size: 2.3 MB (2275286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685e3db2e1ea7f3a85650a5cac398166f6fe54b1767d8ab65fd070fc9f08f903`  
		Last Modified: Mon, 08 Dec 2025 22:41:32 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bedd2011ff5fea2608113c25dac443f7f67fd30b9f049d14304a5eeba342453`  
		Last Modified: Mon, 08 Dec 2025 22:41:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:5be232fd0ce753823a0a00a2e155ca7ed374028d0a228270604974765be63286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ad988781bd90f9b424c8530a983604f0dea5e9ff5d39be9ca322ea793f7044`

```dockerfile
```

-	Layers:
	-	`sha256:2f225cf8fe800d6f4631961cb099b7f796ad28fbe325df7943d5fd182391187f`  
		Last Modified: Tue, 09 Dec 2025 01:35:10 GMT  
		Size: 2.0 MB (2008544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd6800d8108ddffdecd1e6d030f8948b6ed22cff74e19779380d731dfd189d0d`  
		Last Modified: Tue, 09 Dec 2025 01:35:11 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; 386

```console
$ docker pull memcached@sha256:9c8dd1c0a7d71ffb9540bcdac40c6c72661b05ad12d1a0dcacb86ba0dad353b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33686582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a221f2cf3f75cb38b8be293e0d315a4453967306dc401835f3732a7ec18482d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:17 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:33:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:36:13 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:36:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:36:13 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:36:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:36:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:36:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:36:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:36:13 GMT
USER memcache
# Mon, 08 Dec 2025 22:36:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:36:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c63a49351bc91fd837d81e97ce862507215607bc756f1133f1d887e94e1cc4e`  
		Last Modified: Mon, 08 Dec 2025 22:36:26 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7073e103108a28c5e5a1458be46ac8c708375f2b4327423a59471a77bbf2c0c6`  
		Last Modified: Mon, 08 Dec 2025 22:36:26 GMT  
		Size: 147.5 KB (147516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbfa39b86ad2206ef2fdf5ec3f3a55aa40c422a9f3fca094c7c2f003e7d4a63`  
		Last Modified: Mon, 08 Dec 2025 22:36:26 GMT  
		Size: 2.2 MB (2244483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1ade71ea049e11fc9cea7c16944632ffd753dfe7130e3bb4e1730281daffb5`  
		Last Modified: Mon, 08 Dec 2025 22:36:26 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5eb870312490559d775f9d994ba10b9fcae44c680e23a647a43c1c55f49b54`  
		Last Modified: Mon, 08 Dec 2025 22:36:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:e5ea0a4780f0574f775d4cf8c4ffff6f6b836e33d54d6d241047fa36e54d70b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1425c202287fb1c6f81bb3962bb416b9f23b14b12da6119772ac599ae7af4b`

```dockerfile
```

-	Layers:
	-	`sha256:9d6ed296b190f0f66c6f54ffafa76bd9f86d72e2a463ed9841c2654abf7282d0`  
		Last Modified: Tue, 09 Dec 2025 01:35:16 GMT  
		Size: 2.0 MB (2005385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d9f28b39486b665dcd60f89a225a5fce2e4060feaed50b57eaf89bc54345129`  
		Last Modified: Tue, 09 Dec 2025 01:35:17 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:9a5a8c51d01a2dde31ee88dc7739b61aad1cd244c1592033d64b89e71ea9d086
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36185779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62a722a142df5369183f571c8eecacbc8041e72fb89888b569e2e558947291b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:32:15 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 09 Dec 2025 00:32:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:35:25 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 09 Dec 2025 00:35:25 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 09 Dec 2025 00:35:25 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 09 Dec 2025 00:35:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 09 Dec 2025 00:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 00:35:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 09 Dec 2025 00:35:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Dec 2025 00:35:26 GMT
USER memcache
# Tue, 09 Dec 2025 00:35:26 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 09 Dec 2025 00:35:26 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca80ecfb634d24079bf04d5695260ea9dce9f468064fb83123a71959d22b7c4`  
		Last Modified: Tue, 09 Dec 2025 00:35:51 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb90fb01769b3666ac21d77bcba16bd54161463250fa6f304710eb00d5ab5411`  
		Last Modified: Tue, 09 Dec 2025 00:35:51 GMT  
		Size: 170.4 KB (170375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be675ba49db497b747d37543689ff0b8fc0ef4398cd718c2fadd28302d88141b`  
		Last Modified: Tue, 09 Dec 2025 00:35:51 GMT  
		Size: 2.4 MB (2417005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882b9516d2a74a32203b37778b6025dc9c68a30838e1fa420559c34fe0319141`  
		Last Modified: Tue, 09 Dec 2025 00:35:51 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5cfa5b161387b536b9f8a94f199ffd006893e19e7bff82a8f1f9a7aa578a73`  
		Last Modified: Tue, 09 Dec 2025 00:35:51 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:6ea51b9da9219f68c45e3345bed106b961bce70b2c9aecbb6e1300060e04217d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f87eac26bbbb68ef23dfd63867d0415ddc04fe2567863569701f2891733279d6`

```dockerfile
```

-	Layers:
	-	`sha256:6f8bb9e427f03eea07711eb22a22462b3548d9ed3bf7b82f412aea5a623b10ff`  
		Last Modified: Tue, 09 Dec 2025 04:34:42 GMT  
		Size: 2.0 MB (2011829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1705de570678d9ecda7c8bb1da82748111d8547fb22bfbfb43fbbf41808b5b67`  
		Last Modified: Tue, 09 Dec 2025 04:34:43 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:05d76bdff41209572f5e6c4d21717d0717a794340a2bc2c086af7a863f5c19af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30627687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c785d7526540c98189bc45e1c3ad5a9862a6ed744c2b49e94165199ba9dcd7ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 10:11:36 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 10:12:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 10:53:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 10:53:11 GMT
USER memcache
# Tue, 18 Nov 2025 10:53:11 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 10:53:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f7062dea9fa0a796a2eacb7b265e4b2000be3d07bc91c20a5abc6538e5a68c`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f8a04356a93113399cb041ac377cf221db2df7d9fc3a6d630a061a923eb1e6`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 133.1 KB (133088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4bbee7a68150daca8b6b94e26e1a04551afc5a77dfb08a4e04aadc0933c456`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 2.2 MB (2219954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085465091dfa79c5f79dd2c74f56f75a8e078b89272039f8d8ed5a1d2adac41b`  
		Last Modified: Tue, 18 Nov 2025 10:54:06 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea3aae46e46f60ca268fd3c445c8b9ed827d7daba7e6d611310cfc9dc4d5291`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:7a8af6c2848585e79b5cb65b6a760b1f78f0de3a59fb604d7a026c79f05a77b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c73002e7361572816b1c22cbb73aced8ce908f6492f2b5d15371b7c0a0514546`

```dockerfile
```

-	Layers:
	-	`sha256:059e3337eaf5c7461d584e0f4b5c7c660bf41a1bb79e90aa917a3992eba4c855`  
		Last Modified: Tue, 18 Nov 2025 16:35:44 GMT  
		Size: 2.0 MB (2002192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cf39200d9e698624fc7d7abe914cab80bda5407ae30f111eb22846e8fd28bba`  
		Last Modified: Tue, 18 Nov 2025 16:35:45 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:332c41cfc207814782dda23a2b840d653abb751f335f7f02f6b238ce79c1c08c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32290312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2be68b3a60f2d8e906983e133fcaffe03bd1a82c9acc69a3dcbe3e307d7b8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:21 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:33:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:36:33 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:36:33 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:36:33 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:36:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:36:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:36:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:36:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:36:34 GMT
USER memcache
# Mon, 08 Dec 2025 22:36:34 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:36:34 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc040aa39039515a9f8b38dc90047178bd8fa0d8234856954f045f05050e52c`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e235f00f3da465d44b7ac18782958812c19e974f091dedfc097442ba632a3d`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 140.5 KB (140505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284c7cc2b7cc68de54eb5bce5de02ed5229cb403476e794b8066eee16babb6e1`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 2.3 MB (2313897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5059135976f7ec26a104b2fb6340b0ae8adc5756ea159deede93c8532613fd24`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd63939e0e5898afa1d51d59354c263e9a7ebfba3e418395baf21445315251de`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:8a7be7ae9cfd628f1585c887ce286f74e97f7780cc20009ffe07f9c92623b34c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c6fbc39d1b80ba4ed6852329a8ddfcaaeed5500129f5019fbc5a8904a7cd659`

```dockerfile
```

-	Layers:
	-	`sha256:0a66a7a3c4891f559fc098f2c13e48d32804e22f559857d3c89074b829300c25`  
		Last Modified: Tue, 09 Dec 2025 01:35:26 GMT  
		Size: 2.0 MB (2009665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24d3a4bbcde50a51a341ad980cc2d92d652ec5f9394c80d55c8a70ded47d8927`  
		Last Modified: Tue, 09 Dec 2025 01:35:27 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6`

```console
$ docker pull memcached@sha256:c7628370ae681c42dbd48ccf02320d77a2bc0234f9ba3a968b5da3a7c0112469
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:1.6` - linux; amd64

```console
$ docker pull memcached@sha256:153e4ed762fd3bc07fe607f64631647939278d6101759d91fac0b756cceb2272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32208551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa0c800d7278560e11e4d0f14defc4d2d850224d0859d1bd0e9205cc962478d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:38:46 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:38:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:41:30 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:41:30 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:41:30 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:41:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:41:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:41:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:41:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:41:30 GMT
USER memcache
# Mon, 08 Dec 2025 22:41:30 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:41:30 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e33b5452dc8ba5d42cd13b42745898ef870af3e8d5a65b06b8b174f06b1d50`  
		Last Modified: Mon, 08 Dec 2025 22:41:43 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce4ec629da8029212ce5d775073648d04f1f014a89e49f73f1fc848bc405dd5`  
		Last Modified: Mon, 08 Dec 2025 22:41:43 GMT  
		Size: 136.7 KB (136697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6210dfd46759cbe6922de2db75ddf6d17c1f033a434ee6bcf2e82d56ce59f449`  
		Last Modified: Mon, 08 Dec 2025 22:41:43 GMT  
		Size: 2.3 MB (2293845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffbb5d472cb4680299753b978d2e8eeb6d2288ee4caec01e65541f4358516a6`  
		Last Modified: Mon, 08 Dec 2025 22:41:43 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e474cc606bdb91c69d2f124d38e5ebd93ed9ab64d219ab51845cc238a5904aa`  
		Last Modified: Mon, 08 Dec 2025 22:41:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:45cb4f875b600a26ef6e0388db256b09a14580b17ddcaa485fd2c25cbff56056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6483c69793152c682b93375229933004781cbf7df7f059d288d2d7e04335b2c8`

```dockerfile
```

-	Layers:
	-	`sha256:c3beab005b14cd0614637cc43c84460edfb07d9c68b1138ee676ab5bd3dc05ac`  
		Last Modified: Tue, 09 Dec 2025 01:34:56 GMT  
		Size: 2.0 MB (2008228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6ce8cbbfb878c257688fdf1d5e1a9c428b68061ee92f8e07a240ab0fe4b812e`  
		Last Modified: Tue, 09 Dec 2025 01:34:57 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:5a7b1183ed0a0ca89ce3d88e335fca2672422eee8d05921621cd4ed617965ed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30317206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1552234329fddb68f43cfe1abdf3dff1b1499edbb12eb6d84c481f3d7fbe2c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:34:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:37:32 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:37:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:37:32 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:37:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:37:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:37:32 GMT
USER memcache
# Mon, 08 Dec 2025 22:37:32 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:37:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d97bc71d0fa535127863fdab265dfddb07b3cda35b80de4dd2b9b67fe154c856`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 27.9 MB (27944187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d0d6688f3764bd09c70b0fdb00a12bc517f76c47fc187448da8cf7958b4b98`  
		Last Modified: Mon, 08 Dec 2025 22:37:44 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1a7c3cdaa260d51a1e04177297af5b7e205abe78e98f0782c38369f1a49034`  
		Last Modified: Mon, 08 Dec 2025 22:37:45 GMT  
		Size: 144.1 KB (144146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e35266d4886f5160ecccf89b51e0317cf6c7ad5a063a40d74c0dd0baa75b974`  
		Last Modified: Mon, 08 Dec 2025 22:37:45 GMT  
		Size: 2.2 MB (2227364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3324af035e2f7b73ce2f8c3d5ee46e80ed9063e2ae219caf112d6bafe3d935a3`  
		Last Modified: Mon, 08 Dec 2025 22:37:44 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae7d716f59ff9d69d00b890308b431e236e3a1d530f0dfa1ccaabdd01ea7df2`  
		Last Modified: Mon, 08 Dec 2025 22:37:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:077fa23fa7fd08a421aff7ec84a802bb72f53e3f31c9fb2bba4df39b99ae3923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92bd65e20c21649e0ebcbd5810944fd9e43ecf788ec1d580bfc3c04722bf6fa4`

```dockerfile
```

-	Layers:
	-	`sha256:02c0b341ef4c59b9ffa7a8de46289cbd08d3a3b029c0a64224da804b55e2e854`  
		Last Modified: Tue, 09 Dec 2025 01:35:01 GMT  
		Size: 2.0 MB (2011231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb1ede44c11856b6e3f7c4f6ba238d3df5677af459242c47b9f24b4a1c184db0`  
		Last Modified: Tue, 09 Dec 2025 01:35:02 GMT  
		Size: 22.3 KB (22302 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v7

```console
$ docker pull memcached@sha256:cb9b94d371b2da6a520b577dd688b99c959dac8ad5e81f17aaf8e5b6ed1968ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28529520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a8988937956147836c267576a47663f836997a1d6a21750c17c7d2e52982c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:38:02 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:38:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:41:09 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:41:09 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:41:09 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:41:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:41:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:41:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:41:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:41:09 GMT
USER memcache
# Mon, 08 Dec 2025 22:41:09 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:41:09 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15599337d37fa53f93b66130266f60f942cc7c2c4e2e8458c672f9b61b921350`  
		Last Modified: Mon, 08 Dec 2025 22:41:22 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4e148e811da2c8aeb3f52da0f7e137c9e2dbf7e07ea25ed2a8ec2bc3db340d`  
		Last Modified: Mon, 08 Dec 2025 22:41:25 GMT  
		Size: 135.4 KB (135363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248d1bdc7fd809ba8d6d01e877ae1ff16258cd1b26203215342935af2305c133`  
		Last Modified: Mon, 08 Dec 2025 22:41:22 GMT  
		Size: 2.2 MB (2182634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4dca52427f97b68739a35240dde721713ae992674b8f6fe50fc71d987512c4`  
		Last Modified: Mon, 08 Dec 2025 22:41:22 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2961ef381f352090fe3d59e2ff32ae5c2979defa070a22f5fc846bb2b5f0f30`  
		Last Modified: Mon, 08 Dec 2025 22:41:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:cff996fea1034ca7a74465fdf5489ef45c78f70859319df22468100dc3c84e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e8d92fa13df244234c51ab1b93e9a4c39ad977f40dd5b49cef4e8ed0de7e3a`

```dockerfile
```

-	Layers:
	-	`sha256:d08663eef9d4f14b4b344cf2d8924f04dee694d602df55d600a90830f505069b`  
		Last Modified: Tue, 09 Dec 2025 01:35:06 GMT  
		Size: 2.0 MB (2009688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb1b323cef393d68691ca1f808424d4c4ca9aa868a63329889d55c9e53c30671`  
		Last Modified: Tue, 09 Dec 2025 01:35:06 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:6230125fff57e6f22504aae8db1ed049b738d97c3e325a68a9733a186fab61e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32568877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2f55b9564478802d59f2ab50cadac0b6e11704297ea84bc7fdcc4e9fb3ba76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:38:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:38:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:41:20 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:41:20 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:41:20 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:41:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:41:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:41:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:41:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:41:20 GMT
USER memcache
# Mon, 08 Dec 2025 22:41:20 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:41:20 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91cd2e642e1c9b79606d81fe7ae3f5599c2e1a2ebb80864a1c25f4771502b02`  
		Last Modified: Mon, 08 Dec 2025 22:41:32 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9b5941656d039525e2c86c6dad7b225e0dfe8a89bda1c33c46f84b7e1f05f0`  
		Last Modified: Mon, 08 Dec 2025 22:41:32 GMT  
		Size: 153.5 KB (153454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc829d43c3195e76b119f7ef9e8519d7c64f130e104b29b5317d18e709d3796`  
		Last Modified: Mon, 08 Dec 2025 22:41:32 GMT  
		Size: 2.3 MB (2275286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685e3db2e1ea7f3a85650a5cac398166f6fe54b1767d8ab65fd070fc9f08f903`  
		Last Modified: Mon, 08 Dec 2025 22:41:32 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bedd2011ff5fea2608113c25dac443f7f67fd30b9f049d14304a5eeba342453`  
		Last Modified: Mon, 08 Dec 2025 22:41:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:5be232fd0ce753823a0a00a2e155ca7ed374028d0a228270604974765be63286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ad988781bd90f9b424c8530a983604f0dea5e9ff5d39be9ca322ea793f7044`

```dockerfile
```

-	Layers:
	-	`sha256:2f225cf8fe800d6f4631961cb099b7f796ad28fbe325df7943d5fd182391187f`  
		Last Modified: Tue, 09 Dec 2025 01:35:10 GMT  
		Size: 2.0 MB (2008544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd6800d8108ddffdecd1e6d030f8948b6ed22cff74e19779380d731dfd189d0d`  
		Last Modified: Tue, 09 Dec 2025 01:35:11 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; 386

```console
$ docker pull memcached@sha256:9c8dd1c0a7d71ffb9540bcdac40c6c72661b05ad12d1a0dcacb86ba0dad353b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33686582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a221f2cf3f75cb38b8be293e0d315a4453967306dc401835f3732a7ec18482d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:17 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:33:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:36:13 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:36:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:36:13 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:36:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:36:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:36:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:36:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:36:13 GMT
USER memcache
# Mon, 08 Dec 2025 22:36:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:36:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c63a49351bc91fd837d81e97ce862507215607bc756f1133f1d887e94e1cc4e`  
		Last Modified: Mon, 08 Dec 2025 22:36:26 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7073e103108a28c5e5a1458be46ac8c708375f2b4327423a59471a77bbf2c0c6`  
		Last Modified: Mon, 08 Dec 2025 22:36:26 GMT  
		Size: 147.5 KB (147516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbfa39b86ad2206ef2fdf5ec3f3a55aa40c422a9f3fca094c7c2f003e7d4a63`  
		Last Modified: Mon, 08 Dec 2025 22:36:26 GMT  
		Size: 2.2 MB (2244483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1ade71ea049e11fc9cea7c16944632ffd753dfe7130e3bb4e1730281daffb5`  
		Last Modified: Mon, 08 Dec 2025 22:36:26 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5eb870312490559d775f9d994ba10b9fcae44c680e23a647a43c1c55f49b54`  
		Last Modified: Mon, 08 Dec 2025 22:36:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:e5ea0a4780f0574f775d4cf8c4ffff6f6b836e33d54d6d241047fa36e54d70b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1425c202287fb1c6f81bb3962bb416b9f23b14b12da6119772ac599ae7af4b`

```dockerfile
```

-	Layers:
	-	`sha256:9d6ed296b190f0f66c6f54ffafa76bd9f86d72e2a463ed9841c2654abf7282d0`  
		Last Modified: Tue, 09 Dec 2025 01:35:16 GMT  
		Size: 2.0 MB (2005385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d9f28b39486b665dcd60f89a225a5fce2e4060feaed50b57eaf89bc54345129`  
		Last Modified: Tue, 09 Dec 2025 01:35:17 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:9a5a8c51d01a2dde31ee88dc7739b61aad1cd244c1592033d64b89e71ea9d086
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36185779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62a722a142df5369183f571c8eecacbc8041e72fb89888b569e2e558947291b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:32:15 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 09 Dec 2025 00:32:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:35:25 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 09 Dec 2025 00:35:25 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 09 Dec 2025 00:35:25 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 09 Dec 2025 00:35:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 09 Dec 2025 00:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 00:35:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 09 Dec 2025 00:35:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Dec 2025 00:35:26 GMT
USER memcache
# Tue, 09 Dec 2025 00:35:26 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 09 Dec 2025 00:35:26 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca80ecfb634d24079bf04d5695260ea9dce9f468064fb83123a71959d22b7c4`  
		Last Modified: Tue, 09 Dec 2025 00:35:51 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb90fb01769b3666ac21d77bcba16bd54161463250fa6f304710eb00d5ab5411`  
		Last Modified: Tue, 09 Dec 2025 00:35:51 GMT  
		Size: 170.4 KB (170375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be675ba49db497b747d37543689ff0b8fc0ef4398cd718c2fadd28302d88141b`  
		Last Modified: Tue, 09 Dec 2025 00:35:51 GMT  
		Size: 2.4 MB (2417005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882b9516d2a74a32203b37778b6025dc9c68a30838e1fa420559c34fe0319141`  
		Last Modified: Tue, 09 Dec 2025 00:35:51 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5cfa5b161387b536b9f8a94f199ffd006893e19e7bff82a8f1f9a7aa578a73`  
		Last Modified: Tue, 09 Dec 2025 00:35:51 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:6ea51b9da9219f68c45e3345bed106b961bce70b2c9aecbb6e1300060e04217d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f87eac26bbbb68ef23dfd63867d0415ddc04fe2567863569701f2891733279d6`

```dockerfile
```

-	Layers:
	-	`sha256:6f8bb9e427f03eea07711eb22a22462b3548d9ed3bf7b82f412aea5a623b10ff`  
		Last Modified: Tue, 09 Dec 2025 04:34:42 GMT  
		Size: 2.0 MB (2011829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1705de570678d9ecda7c8bb1da82748111d8547fb22bfbfb43fbbf41808b5b67`  
		Last Modified: Tue, 09 Dec 2025 04:34:43 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; riscv64

```console
$ docker pull memcached@sha256:05d76bdff41209572f5e6c4d21717d0717a794340a2bc2c086af7a863f5c19af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30627687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c785d7526540c98189bc45e1c3ad5a9862a6ed744c2b49e94165199ba9dcd7ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 10:11:36 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 10:12:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 10:53:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 10:53:11 GMT
USER memcache
# Tue, 18 Nov 2025 10:53:11 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 10:53:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f7062dea9fa0a796a2eacb7b265e4b2000be3d07bc91c20a5abc6538e5a68c`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f8a04356a93113399cb041ac377cf221db2df7d9fc3a6d630a061a923eb1e6`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 133.1 KB (133088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4bbee7a68150daca8b6b94e26e1a04551afc5a77dfb08a4e04aadc0933c456`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 2.2 MB (2219954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085465091dfa79c5f79dd2c74f56f75a8e078b89272039f8d8ed5a1d2adac41b`  
		Last Modified: Tue, 18 Nov 2025 10:54:06 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea3aae46e46f60ca268fd3c445c8b9ed827d7daba7e6d611310cfc9dc4d5291`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:7a8af6c2848585e79b5cb65b6a760b1f78f0de3a59fb604d7a026c79f05a77b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c73002e7361572816b1c22cbb73aced8ce908f6492f2b5d15371b7c0a0514546`

```dockerfile
```

-	Layers:
	-	`sha256:059e3337eaf5c7461d584e0f4b5c7c660bf41a1bb79e90aa917a3992eba4c855`  
		Last Modified: Tue, 18 Nov 2025 16:35:44 GMT  
		Size: 2.0 MB (2002192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cf39200d9e698624fc7d7abe914cab80bda5407ae30f111eb22846e8fd28bba`  
		Last Modified: Tue, 18 Nov 2025 16:35:45 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; s390x

```console
$ docker pull memcached@sha256:332c41cfc207814782dda23a2b840d653abb751f335f7f02f6b238ce79c1c08c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32290312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2be68b3a60f2d8e906983e133fcaffe03bd1a82c9acc69a3dcbe3e307d7b8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:21 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:33:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:36:33 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:36:33 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:36:33 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:36:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:36:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:36:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:36:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:36:34 GMT
USER memcache
# Mon, 08 Dec 2025 22:36:34 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:36:34 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc040aa39039515a9f8b38dc90047178bd8fa0d8234856954f045f05050e52c`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e235f00f3da465d44b7ac18782958812c19e974f091dedfc097442ba632a3d`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 140.5 KB (140505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284c7cc2b7cc68de54eb5bce5de02ed5229cb403476e794b8066eee16babb6e1`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 2.3 MB (2313897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5059135976f7ec26a104b2fb6340b0ae8adc5756ea159deede93c8532613fd24`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd63939e0e5898afa1d51d59354c263e9a7ebfba3e418395baf21445315251de`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:8a7be7ae9cfd628f1585c887ce286f74e97f7780cc20009ffe07f9c92623b34c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c6fbc39d1b80ba4ed6852329a8ddfcaaeed5500129f5019fbc5a8904a7cd659`

```dockerfile
```

-	Layers:
	-	`sha256:0a66a7a3c4891f559fc098f2c13e48d32804e22f559857d3c89074b829300c25`  
		Last Modified: Tue, 09 Dec 2025 01:35:26 GMT  
		Size: 2.0 MB (2009665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24d3a4bbcde50a51a341ad980cc2d92d652ec5f9394c80d55c8a70ded47d8927`  
		Last Modified: Tue, 09 Dec 2025 01:35:27 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine`

```console
$ docker pull memcached@sha256:c8503d4491edd3110cc07d0465089d3a41cf1daf8645e71149e39a51835e92cd
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
$ docker pull memcached@sha256:aac456c35cd29635b5501fefac58a2e954752006c9d159fbf520dd785e09cbba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5973577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6411cdd430a5f0c33aea6496062ab90fbc7da776f1c937108cf51b7a40e090f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:20:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:20:42 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:23:18 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:23:18 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:23:18 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:23:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:23:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:23:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:23:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:23:18 GMT
USER memcache
# Thu, 04 Dec 2025 19:23:18 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:23:18 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e377e19df274e9919dbfbe05b510e54db0f8451ac0985b108aba9123048001d8`  
		Last Modified: Thu, 04 Dec 2025 19:23:54 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0d9328fb6b4452be1f62a5c6db62b8425a6b48c40ce2408ae0f526b101c80c`  
		Last Modified: Thu, 04 Dec 2025 19:23:55 GMT  
		Size: 106.0 KB (106047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a1eb06c51acdaf80ce22a4524ea827613ecc609e23cb0fa481005e89b22d4f`  
		Last Modified: Thu, 04 Dec 2025 19:23:54 GMT  
		Size: 2.0 MB (2006867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4829db5772d5079a1be438e2b4d4921e584e88e6becb7ca1819f33cc6ddd962c`  
		Last Modified: Thu, 04 Dec 2025 19:23:54 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b919142486c25c1941bfb65c0f6f26ff49ed2820b62db8ee149ac5a386bcd76c`  
		Last Modified: Thu, 04 Dec 2025 19:23:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:849b937b30f8457f48d4a2b4dee48812e3f3fef3740e8553fbeb950ef1e6a405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3eb9da9040350a8be21d03f2423ac5b520d62898c8656b204d89a46be87cca`

```dockerfile
```

-	Layers:
	-	`sha256:a6a585b25dcf23d45fe100d658f3fc872a69be33f37f5b142951380b902e1a65`  
		Last Modified: Thu, 04 Dec 2025 22:34:43 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91e8f143d354857f78ae4fd0e5416b79eb34dc3599af1f3df2161a4fa1885af9`  
		Last Modified: Thu, 04 Dec 2025 22:34:44 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:a7003e700207ebf4fd102e5d81432129cd3e4776c613ee53fa01b0dbd5e9f19b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5629653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36796824ef2ab4ff08673e2fdd2ff3529a8c6c476c842ec665b90db7e63fad02`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:21:33 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:21:34 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:33:55 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:33:55 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:33:55 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:33:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:33:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:33:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:33:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:33:55 GMT
USER memcache
# Thu, 04 Dec 2025 19:33:55 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:33:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2477fbd5a498e104db4354cbb88ebe3bf7d7f22609c3d9f3996ee3d6f2b311`  
		Last Modified: Thu, 04 Dec 2025 19:34:10 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d610e2e19bb7ad98b2e77e581123187db039c4259f548f8e16e1b5015d0ec85`  
		Last Modified: Thu, 04 Dec 2025 19:34:10 GMT  
		Size: 102.6 KB (102642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5e9f0ad4522a9fedea5ba5229899ef09d25774a89a517cf59cae7a36e4ea92`  
		Last Modified: Thu, 04 Dec 2025 19:34:10 GMT  
		Size: 2.0 MB (1957764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8b426cdf478aef96c3b7780b5b6c81b458a0787358d6251799150a9f714aaf`  
		Last Modified: Thu, 04 Dec 2025 19:34:10 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd456d3218701485ecd1ce99f10c7a08986e44f71d19a49e419582aeb4924f52`  
		Last Modified: Thu, 04 Dec 2025 19:34:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:95ab79e458ab0908467ebbdf5539b688045b04421a068fa6821d557eece2f67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569a816a11d27d030ea4089563f4a23efecb872605941df1c53c0c4152fbd211`

```dockerfile
```

-	Layers:
	-	`sha256:dd9475807057d6ac4c96f526dc77e867efe6bb682d09ef1c7c0557b6f2dad356`  
		Last Modified: Thu, 04 Dec 2025 22:34:47 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:6b1fcd05fdcf13d4b7650d85e6043cdeaf423fe9ec57036c0f203e4eef6bff12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5289618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca393e3ead8035915d8cd6bcea0e8ccbe82d8ae05b9cad79126dd93567ff2889`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:43 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:19:44 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:22:37 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:22:37 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:22:37 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:22:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:22:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:22:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:22:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:22:37 GMT
USER memcache
# Thu, 04 Dec 2025 19:22:37 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:22:37 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdc28d0a8cb5092fb181830a0ef7fb2c55b0dcec915fb49171721470a36990e`  
		Last Modified: Thu, 04 Dec 2025 19:22:53 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d64ac2dd6859410fc8786621ad68f29d5cf9799784bd6181fa0fd9b16f10b5`  
		Last Modified: Thu, 04 Dec 2025 19:22:53 GMT  
		Size: 92.4 KB (92376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf39f9a50690d556c95f99315866a17736de133854b3f4a1f01c007e8ea52e8c`  
		Last Modified: Thu, 04 Dec 2025 19:22:53 GMT  
		Size: 1.9 MB (1917424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5adf2295dafdfb5341494ff56dfa3c9fef413e476cc7e0ea0a44ea325856fd40`  
		Last Modified: Thu, 04 Dec 2025 19:22:53 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f68652d871fbfba49b4bdb6f0555e3d086490ac907f630de1960481a50b5982`  
		Last Modified: Thu, 04 Dec 2025 19:22:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:726bec6c0e6bb11f92cf809b0eff6ee10fc86a30eae935ac85e0b82f2fc110d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:489bd5540d03661ecd23b22a8d9070b7dc18f542d91bc1ed60efaa1790080a39`

```dockerfile
```

-	Layers:
	-	`sha256:35def5ffffb77a9cc93b2d806351b5bc638603257621ee3ea2fcab826508b445`  
		Last Modified: Thu, 04 Dec 2025 22:34:50 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b55f58069fda39e67b560d97ac46c79e035b513a560bc8652e5383cd3f82a35`  
		Last Modified: Thu, 04 Dec 2025 22:34:51 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b263323af06e550df9becd8c2cf8450400be7ae4381392593565dc8247bb230f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6304413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:038de42e33564e147549bf3846c2490c168364063ebc7744c8cdd580e202c191`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:20:28 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:20:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:23:16 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:23:16 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:23:16 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:23:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:23:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:23:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:23:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:23:16 GMT
USER memcache
# Thu, 04 Dec 2025 19:23:16 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:23:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4ea1ce2b4c6bdcd3eec4d60b1aa2e3563da544759bff4e7a46469132a86438`  
		Last Modified: Thu, 04 Dec 2025 19:23:27 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc9938ef133bd132ee91a60f23198ae468dca72e6b547301fc4b29e4136bc9e`  
		Last Modified: Thu, 04 Dec 2025 19:23:28 GMT  
		Size: 121.9 KB (121870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fbb7f498823838642f0cbc3dfbcce9ec16c50549649b23872df57076fed9e7`  
		Last Modified: Thu, 04 Dec 2025 19:23:28 GMT  
		Size: 2.0 MB (1985993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341b9a721d462e12012b285eb88cdd865e1fa62f664d8343c3223d3b18b5ed0c`  
		Last Modified: Thu, 04 Dec 2025 19:23:27 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f879a6e1902c8a256d8dea45afd4efc95caa82bd9fcf3291b6730a20d2c5a0`  
		Last Modified: Thu, 04 Dec 2025 19:23:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9e1d743b77c8856403d4e8420e9936de4aa1bc6fc88642c47112e318e10e2655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556ecd6a50c7ec0f18eea0bb6b6a3c2a30163cdbf6e0a9314ef069819efdb628`

```dockerfile
```

-	Layers:
	-	`sha256:57a22eef052f1e8ba0bdbfa2e165923ea29a9572ab9d397f6652f44a895c34c9`  
		Last Modified: Thu, 04 Dec 2025 22:34:54 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea1714f2bc9b4e6925e95bfc0d324fe4686d662ad257e5959451179599d072e6`  
		Last Modified: Thu, 04 Dec 2025 22:34:55 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:b3d88ad28118ac190ff8cfd6be5b29a4aff4e4f772124ba8a6cb7335eb909152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5762624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfa1253f0cf9e80c36b723ff6f79bb43b3cb4c3146f4340f605aaf0bb812eaa1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:20:00 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:20:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:22:43 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:22:43 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:22:43 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:22:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:22:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:22:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:22:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:22:43 GMT
USER memcache
# Thu, 04 Dec 2025 19:22:43 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:22:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3527b4f952d5950d8caa74dc0d1759215000f2f0a195344f0239c7e2805fe2fc`  
		Last Modified: Wed, 03 Dec 2025 19:30:41 GMT  
		Size: 3.7 MB (3685856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801e2ef7c6c58c48cfc036b3ffd9de546ffd13f67044c4c296b3624d08852398`  
		Last Modified: Thu, 04 Dec 2025 19:22:57 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7528d81de6e75b8aa074f7b96d6b9f2650422ca25fc0f5485dadf33879a4eb7`  
		Last Modified: Thu, 04 Dec 2025 19:22:57 GMT  
		Size: 110.7 KB (110732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40cb203b33be80dad7c861215d0c69239f729987a3942b71d4fc7b17423658e`  
		Last Modified: Thu, 04 Dec 2025 19:22:58 GMT  
		Size: 2.0 MB (1964688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbaa8273de612bce797fce27339a8adb341655d9b03a120aa874e80bfc438ba`  
		Last Modified: Thu, 04 Dec 2025 19:22:57 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a62b5e894734682a138338f04d49ebcb3e61a322469798019f9737e8ef19b33`  
		Last Modified: Thu, 04 Dec 2025 19:22:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:a8428c10b46dc321be308528a9dc3904db404457e03384a035c6e8c7bf32d05e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c97e68a8fd4c390f7dac3c43eda5f00b0b29eb2b838b877b0926ec7a55ec29`

```dockerfile
```

-	Layers:
	-	`sha256:5414f83497841dc88789d15a422792cf5c1818a72a4ebe7fa9f569a4824ce99f`  
		Last Modified: Thu, 04 Dec 2025 22:34:58 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19ce16735c127991fab0a49081d04170d61fc3b2c60261704ec9247a0edc119f`  
		Last Modified: Thu, 04 Dec 2025 22:35:02 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:6ff6570e2a8fb560a3b830e0f1475d488961b29b93e711d03fd52464844926b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6058459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9360c3d396b9f5081cdc222d176f25b51a35c42c688d1ff1da3ad33a71befeb9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:22 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:19:24 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:21:48 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:21:48 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:21:48 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:21:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:21:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:21:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:21:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:21:49 GMT
USER memcache
# Thu, 04 Dec 2025 19:21:49 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:21:49 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23500700235e36a847f2b35c25e17b359b4cec377d3a0fbafdfff7ec561ecf74`  
		Last Modified: Thu, 04 Dec 2025 19:22:05 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47c608c5e84b70e2288ed6c722d682394718aa7029f3614c85bb3faa2d1a0ab`  
		Last Modified: Thu, 04 Dec 2025 19:22:05 GMT  
		Size: 126.3 KB (126267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251cee6c1abe9d3d9e832748d0edb232d4e43fbbdfc78f3fad887409eff7a658`  
		Last Modified: Thu, 04 Dec 2025 19:22:06 GMT  
		Size: 2.1 MB (2103821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82b7a39ab647b07cb8e684e6fbe6e0c40959b95f23e8b6fba544f6412e08e10`  
		Last Modified: Thu, 04 Dec 2025 19:22:05 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e989166bceb7b8bb922420cfda5d2c1c362b469900fbbd86593fb4422e6f2fb6`  
		Last Modified: Thu, 04 Dec 2025 19:22:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ad7264b3f464d43618d5e997d3c544a46d5d00112555908bab3e31ddfb719fd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da20be024f8583ae82747476a5a8b1054a0d2018ceade3cfcc11e0b460a369e3`

```dockerfile
```

-	Layers:
	-	`sha256:08dd8ac2fb865783b3720303c0b7abe96c0d831dd8dbd89f5ce48f64f5d93577`  
		Last Modified: Thu, 04 Dec 2025 22:35:05 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52998ad89b5d31b02c435f1dabae41e0023686389189f0729699301d2b2dceba`  
		Last Modified: Thu, 04 Dec 2025 22:35:06 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:82618728d34fd5e3c642277cb563310bed5e815337b99361c23d0d4225e3a1ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5793289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95bfdee9049204386f5f9675313ec0cf6437686f3e41ac46a02d7491c4ebd031`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:39 GMT
ADD alpine-minirootfs-3.23.0-riscv64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:39 GMT
CMD ["/bin/sh"]
# Fri, 05 Dec 2025 02:28:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 05 Dec 2025 02:28:43 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 05 Dec 2025 02:42:05 GMT
ENV MEMCACHED_VERSION=1.6.39
# Fri, 05 Dec 2025 02:42:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Fri, 05 Dec 2025 02:42:05 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Fri, 05 Dec 2025 02:42:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 05 Dec 2025 02:42:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Dec 2025 02:42:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Dec 2025 02:42:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Dec 2025 02:42:06 GMT
USER memcache
# Fri, 05 Dec 2025 02:42:06 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Dec 2025 02:42:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9929557817a4c85b33d6dbeb491f7396ef32added7e77de7ac1b644ed0975313`  
		Last Modified: Wed, 03 Dec 2025 19:30:17 GMT  
		Size: 3.6 MB (3583519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04477eae70c2e3cb1bd666913116b231bd91f758fef0ce0487128436edf54e3`  
		Last Modified: Fri, 05 Dec 2025 02:42:36 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27775dcc23cac586ff5717daea95b160d3515a30312e73dc28db55554bcbdd12`  
		Last Modified: Fri, 05 Dec 2025 02:42:37 GMT  
		Size: 108.9 KB (108892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d493e7dad99e12ada2c869111712bae9f61d05aabeb2139df6297985982f119`  
		Last Modified: Fri, 05 Dec 2025 02:42:37 GMT  
		Size: 2.1 MB (2099525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf14d0478c213567d1f2646d01cd27ca8c3db42c197fceb2c2fe55c1ea5bfd84`  
		Last Modified: Fri, 05 Dec 2025 02:42:37 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb60cadd22d3f64cee1f02bcfccb5472502730fea2408ffa893c00d4cae9e97c`  
		Last Modified: Fri, 05 Dec 2025 02:42:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:6607c3431ad2ac598c8476330688ee82114c9b3c0e9b2849f86d95addf5e48eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8406d4978e549630fb362ff2901a3645f7d325e1cce867bbfddade8ceb14232`

```dockerfile
```

-	Layers:
	-	`sha256:5ae6f5f57506c9cba95d087771e8253c7ee7c129dcbc4fdd524a99f4feeafec9`  
		Last Modified: Fri, 05 Dec 2025 04:34:37 GMT  
		Size: 94.3 KB (94276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b9a49d787a1cd02fea8b8affc293bd2d718765b8ef3d8cf26d839f80d072eea`  
		Last Modified: Fri, 05 Dec 2025 04:34:38 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:b23b3b07e717d7651a02ec547a675f198e684f410c7217a09bd305de6c20e664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5878802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e586dd7e72674888df0e6f0ade73d053d2a5a94b7d890a276fb6f13fba7e4cc3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:22 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:19:24 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:22:39 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:22:39 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:22:39 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:22:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:22:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:22:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:22:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:22:39 GMT
USER memcache
# Thu, 04 Dec 2025 19:22:39 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:22:39 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a188510a1e7e85e0e83a71da1abed06b459c07887a679cf331da7789673755`  
		Last Modified: Thu, 04 Dec 2025 19:23:03 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67afe5cdcebd55aec1e59a816853f758650056c83c63ea4d99d6e06e15f60fd`  
		Last Modified: Thu, 04 Dec 2025 19:23:03 GMT  
		Size: 114.3 KB (114286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377a08e6b7dd38664aeee34c52a61b8f7edf9165adabbaee0e0b923423a60242`  
		Last Modified: Thu, 04 Dec 2025 19:23:03 GMT  
		Size: 2.0 MB (2039357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c47067ba1641d8aa2a1f3d7df1e359c1ef226673c5b60eeecc3824f3609e9b`  
		Last Modified: Thu, 04 Dec 2025 19:23:03 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e307cf70f379099e1c944f0972ea3478099fc2221e7ae304d3c47858cb9c8b`  
		Last Modified: Thu, 04 Dec 2025 19:23:03 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:db1f4e6b802cb9b4ee6a404e244522a143516b6c5dfe88d706e7d657e8a3c6c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e21cb3a2b9f702a014eac05118559131c607052ca17bd1adb7ddb02107d291d0`

```dockerfile
```

-	Layers:
	-	`sha256:a484d75866b9f2198dfeccc7d70aa01018c27dd00a8bdad7b47bb8f659ee35d1`  
		Last Modified: Thu, 04 Dec 2025 22:35:09 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e39d44972f86c94e48a8ba761774c90c693cfd7248b9b3fa84a7905217f0c57a`  
		Last Modified: Thu, 04 Dec 2025 22:35:10 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine3.23`

```console
$ docker pull memcached@sha256:c8503d4491edd3110cc07d0465089d3a41cf1daf8645e71149e39a51835e92cd
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

### `memcached:1.6-alpine3.23` - linux; amd64

```console
$ docker pull memcached@sha256:aac456c35cd29635b5501fefac58a2e954752006c9d159fbf520dd785e09cbba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5973577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6411cdd430a5f0c33aea6496062ab90fbc7da776f1c937108cf51b7a40e090f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:20:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:20:42 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:23:18 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:23:18 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:23:18 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:23:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:23:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:23:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:23:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:23:18 GMT
USER memcache
# Thu, 04 Dec 2025 19:23:18 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:23:18 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e377e19df274e9919dbfbe05b510e54db0f8451ac0985b108aba9123048001d8`  
		Last Modified: Thu, 04 Dec 2025 19:23:54 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0d9328fb6b4452be1f62a5c6db62b8425a6b48c40ce2408ae0f526b101c80c`  
		Last Modified: Thu, 04 Dec 2025 19:23:55 GMT  
		Size: 106.0 KB (106047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a1eb06c51acdaf80ce22a4524ea827613ecc609e23cb0fa481005e89b22d4f`  
		Last Modified: Thu, 04 Dec 2025 19:23:54 GMT  
		Size: 2.0 MB (2006867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4829db5772d5079a1be438e2b4d4921e584e88e6becb7ca1819f33cc6ddd962c`  
		Last Modified: Thu, 04 Dec 2025 19:23:54 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b919142486c25c1941bfb65c0f6f26ff49ed2820b62db8ee149ac5a386bcd76c`  
		Last Modified: Thu, 04 Dec 2025 19:23:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:849b937b30f8457f48d4a2b4dee48812e3f3fef3740e8553fbeb950ef1e6a405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3eb9da9040350a8be21d03f2423ac5b520d62898c8656b204d89a46be87cca`

```dockerfile
```

-	Layers:
	-	`sha256:a6a585b25dcf23d45fe100d658f3fc872a69be33f37f5b142951380b902e1a65`  
		Last Modified: Thu, 04 Dec 2025 22:34:43 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91e8f143d354857f78ae4fd0e5416b79eb34dc3599af1f3df2161a4fa1885af9`  
		Last Modified: Thu, 04 Dec 2025 22:34:44 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; arm variant v6

```console
$ docker pull memcached@sha256:a7003e700207ebf4fd102e5d81432129cd3e4776c613ee53fa01b0dbd5e9f19b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5629653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36796824ef2ab4ff08673e2fdd2ff3529a8c6c476c842ec665b90db7e63fad02`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:21:33 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:21:34 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:33:55 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:33:55 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:33:55 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:33:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:33:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:33:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:33:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:33:55 GMT
USER memcache
# Thu, 04 Dec 2025 19:33:55 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:33:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2477fbd5a498e104db4354cbb88ebe3bf7d7f22609c3d9f3996ee3d6f2b311`  
		Last Modified: Thu, 04 Dec 2025 19:34:10 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d610e2e19bb7ad98b2e77e581123187db039c4259f548f8e16e1b5015d0ec85`  
		Last Modified: Thu, 04 Dec 2025 19:34:10 GMT  
		Size: 102.6 KB (102642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5e9f0ad4522a9fedea5ba5229899ef09d25774a89a517cf59cae7a36e4ea92`  
		Last Modified: Thu, 04 Dec 2025 19:34:10 GMT  
		Size: 2.0 MB (1957764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8b426cdf478aef96c3b7780b5b6c81b458a0787358d6251799150a9f714aaf`  
		Last Modified: Thu, 04 Dec 2025 19:34:10 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd456d3218701485ecd1ce99f10c7a08986e44f71d19a49e419582aeb4924f52`  
		Last Modified: Thu, 04 Dec 2025 19:34:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:95ab79e458ab0908467ebbdf5539b688045b04421a068fa6821d557eece2f67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569a816a11d27d030ea4089563f4a23efecb872605941df1c53c0c4152fbd211`

```dockerfile
```

-	Layers:
	-	`sha256:dd9475807057d6ac4c96f526dc77e867efe6bb682d09ef1c7c0557b6f2dad356`  
		Last Modified: Thu, 04 Dec 2025 22:34:47 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; arm variant v7

```console
$ docker pull memcached@sha256:6b1fcd05fdcf13d4b7650d85e6043cdeaf423fe9ec57036c0f203e4eef6bff12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5289618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca393e3ead8035915d8cd6bcea0e8ccbe82d8ae05b9cad79126dd93567ff2889`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:43 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:19:44 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:22:37 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:22:37 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:22:37 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:22:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:22:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:22:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:22:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:22:37 GMT
USER memcache
# Thu, 04 Dec 2025 19:22:37 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:22:37 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdc28d0a8cb5092fb181830a0ef7fb2c55b0dcec915fb49171721470a36990e`  
		Last Modified: Thu, 04 Dec 2025 19:22:53 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d64ac2dd6859410fc8786621ad68f29d5cf9799784bd6181fa0fd9b16f10b5`  
		Last Modified: Thu, 04 Dec 2025 19:22:53 GMT  
		Size: 92.4 KB (92376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf39f9a50690d556c95f99315866a17736de133854b3f4a1f01c007e8ea52e8c`  
		Last Modified: Thu, 04 Dec 2025 19:22:53 GMT  
		Size: 1.9 MB (1917424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5adf2295dafdfb5341494ff56dfa3c9fef413e476cc7e0ea0a44ea325856fd40`  
		Last Modified: Thu, 04 Dec 2025 19:22:53 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f68652d871fbfba49b4bdb6f0555e3d086490ac907f630de1960481a50b5982`  
		Last Modified: Thu, 04 Dec 2025 19:22:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:726bec6c0e6bb11f92cf809b0eff6ee10fc86a30eae935ac85e0b82f2fc110d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:489bd5540d03661ecd23b22a8d9070b7dc18f542d91bc1ed60efaa1790080a39`

```dockerfile
```

-	Layers:
	-	`sha256:35def5ffffb77a9cc93b2d806351b5bc638603257621ee3ea2fcab826508b445`  
		Last Modified: Thu, 04 Dec 2025 22:34:50 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b55f58069fda39e67b560d97ac46c79e035b513a560bc8652e5383cd3f82a35`  
		Last Modified: Thu, 04 Dec 2025 22:34:51 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b263323af06e550df9becd8c2cf8450400be7ae4381392593565dc8247bb230f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6304413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:038de42e33564e147549bf3846c2490c168364063ebc7744c8cdd580e202c191`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:20:28 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:20:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:23:16 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:23:16 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:23:16 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:23:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:23:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:23:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:23:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:23:16 GMT
USER memcache
# Thu, 04 Dec 2025 19:23:16 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:23:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4ea1ce2b4c6bdcd3eec4d60b1aa2e3563da544759bff4e7a46469132a86438`  
		Last Modified: Thu, 04 Dec 2025 19:23:27 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc9938ef133bd132ee91a60f23198ae468dca72e6b547301fc4b29e4136bc9e`  
		Last Modified: Thu, 04 Dec 2025 19:23:28 GMT  
		Size: 121.9 KB (121870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fbb7f498823838642f0cbc3dfbcce9ec16c50549649b23872df57076fed9e7`  
		Last Modified: Thu, 04 Dec 2025 19:23:28 GMT  
		Size: 2.0 MB (1985993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341b9a721d462e12012b285eb88cdd865e1fa62f664d8343c3223d3b18b5ed0c`  
		Last Modified: Thu, 04 Dec 2025 19:23:27 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f879a6e1902c8a256d8dea45afd4efc95caa82bd9fcf3291b6730a20d2c5a0`  
		Last Modified: Thu, 04 Dec 2025 19:23:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:9e1d743b77c8856403d4e8420e9936de4aa1bc6fc88642c47112e318e10e2655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556ecd6a50c7ec0f18eea0bb6b6a3c2a30163cdbf6e0a9314ef069819efdb628`

```dockerfile
```

-	Layers:
	-	`sha256:57a22eef052f1e8ba0bdbfa2e165923ea29a9572ab9d397f6652f44a895c34c9`  
		Last Modified: Thu, 04 Dec 2025 22:34:54 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea1714f2bc9b4e6925e95bfc0d324fe4686d662ad257e5959451179599d072e6`  
		Last Modified: Thu, 04 Dec 2025 22:34:55 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; 386

```console
$ docker pull memcached@sha256:b3d88ad28118ac190ff8cfd6be5b29a4aff4e4f772124ba8a6cb7335eb909152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5762624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfa1253f0cf9e80c36b723ff6f79bb43b3cb4c3146f4340f605aaf0bb812eaa1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:20:00 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:20:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:22:43 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:22:43 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:22:43 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:22:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:22:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:22:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:22:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:22:43 GMT
USER memcache
# Thu, 04 Dec 2025 19:22:43 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:22:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3527b4f952d5950d8caa74dc0d1759215000f2f0a195344f0239c7e2805fe2fc`  
		Last Modified: Wed, 03 Dec 2025 19:30:41 GMT  
		Size: 3.7 MB (3685856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801e2ef7c6c58c48cfc036b3ffd9de546ffd13f67044c4c296b3624d08852398`  
		Last Modified: Thu, 04 Dec 2025 19:22:57 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7528d81de6e75b8aa074f7b96d6b9f2650422ca25fc0f5485dadf33879a4eb7`  
		Last Modified: Thu, 04 Dec 2025 19:22:57 GMT  
		Size: 110.7 KB (110732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40cb203b33be80dad7c861215d0c69239f729987a3942b71d4fc7b17423658e`  
		Last Modified: Thu, 04 Dec 2025 19:22:58 GMT  
		Size: 2.0 MB (1964688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbaa8273de612bce797fce27339a8adb341655d9b03a120aa874e80bfc438ba`  
		Last Modified: Thu, 04 Dec 2025 19:22:57 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a62b5e894734682a138338f04d49ebcb3e61a322469798019f9737e8ef19b33`  
		Last Modified: Thu, 04 Dec 2025 19:22:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:a8428c10b46dc321be308528a9dc3904db404457e03384a035c6e8c7bf32d05e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c97e68a8fd4c390f7dac3c43eda5f00b0b29eb2b838b877b0926ec7a55ec29`

```dockerfile
```

-	Layers:
	-	`sha256:5414f83497841dc88789d15a422792cf5c1818a72a4ebe7fa9f569a4824ce99f`  
		Last Modified: Thu, 04 Dec 2025 22:34:58 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19ce16735c127991fab0a49081d04170d61fc3b2c60261704ec9247a0edc119f`  
		Last Modified: Thu, 04 Dec 2025 22:35:02 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; ppc64le

```console
$ docker pull memcached@sha256:6ff6570e2a8fb560a3b830e0f1475d488961b29b93e711d03fd52464844926b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6058459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9360c3d396b9f5081cdc222d176f25b51a35c42c688d1ff1da3ad33a71befeb9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:22 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:19:24 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:21:48 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:21:48 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:21:48 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:21:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:21:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:21:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:21:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:21:49 GMT
USER memcache
# Thu, 04 Dec 2025 19:21:49 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:21:49 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23500700235e36a847f2b35c25e17b359b4cec377d3a0fbafdfff7ec561ecf74`  
		Last Modified: Thu, 04 Dec 2025 19:22:05 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47c608c5e84b70e2288ed6c722d682394718aa7029f3614c85bb3faa2d1a0ab`  
		Last Modified: Thu, 04 Dec 2025 19:22:05 GMT  
		Size: 126.3 KB (126267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251cee6c1abe9d3d9e832748d0edb232d4e43fbbdfc78f3fad887409eff7a658`  
		Last Modified: Thu, 04 Dec 2025 19:22:06 GMT  
		Size: 2.1 MB (2103821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82b7a39ab647b07cb8e684e6fbe6e0c40959b95f23e8b6fba544f6412e08e10`  
		Last Modified: Thu, 04 Dec 2025 19:22:05 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e989166bceb7b8bb922420cfda5d2c1c362b469900fbbd86593fb4422e6f2fb6`  
		Last Modified: Thu, 04 Dec 2025 19:22:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:ad7264b3f464d43618d5e997d3c544a46d5d00112555908bab3e31ddfb719fd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da20be024f8583ae82747476a5a8b1054a0d2018ceade3cfcc11e0b460a369e3`

```dockerfile
```

-	Layers:
	-	`sha256:08dd8ac2fb865783b3720303c0b7abe96c0d831dd8dbd89f5ce48f64f5d93577`  
		Last Modified: Thu, 04 Dec 2025 22:35:05 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52998ad89b5d31b02c435f1dabae41e0023686389189f0729699301d2b2dceba`  
		Last Modified: Thu, 04 Dec 2025 22:35:06 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; riscv64

```console
$ docker pull memcached@sha256:82618728d34fd5e3c642277cb563310bed5e815337b99361c23d0d4225e3a1ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5793289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95bfdee9049204386f5f9675313ec0cf6437686f3e41ac46a02d7491c4ebd031`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:39 GMT
ADD alpine-minirootfs-3.23.0-riscv64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:39 GMT
CMD ["/bin/sh"]
# Fri, 05 Dec 2025 02:28:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 05 Dec 2025 02:28:43 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 05 Dec 2025 02:42:05 GMT
ENV MEMCACHED_VERSION=1.6.39
# Fri, 05 Dec 2025 02:42:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Fri, 05 Dec 2025 02:42:05 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Fri, 05 Dec 2025 02:42:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 05 Dec 2025 02:42:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Dec 2025 02:42:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Dec 2025 02:42:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Dec 2025 02:42:06 GMT
USER memcache
# Fri, 05 Dec 2025 02:42:06 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Dec 2025 02:42:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9929557817a4c85b33d6dbeb491f7396ef32added7e77de7ac1b644ed0975313`  
		Last Modified: Wed, 03 Dec 2025 19:30:17 GMT  
		Size: 3.6 MB (3583519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04477eae70c2e3cb1bd666913116b231bd91f758fef0ce0487128436edf54e3`  
		Last Modified: Fri, 05 Dec 2025 02:42:36 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27775dcc23cac586ff5717daea95b160d3515a30312e73dc28db55554bcbdd12`  
		Last Modified: Fri, 05 Dec 2025 02:42:37 GMT  
		Size: 108.9 KB (108892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d493e7dad99e12ada2c869111712bae9f61d05aabeb2139df6297985982f119`  
		Last Modified: Fri, 05 Dec 2025 02:42:37 GMT  
		Size: 2.1 MB (2099525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf14d0478c213567d1f2646d01cd27ca8c3db42c197fceb2c2fe55c1ea5bfd84`  
		Last Modified: Fri, 05 Dec 2025 02:42:37 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb60cadd22d3f64cee1f02bcfccb5472502730fea2408ffa893c00d4cae9e97c`  
		Last Modified: Fri, 05 Dec 2025 02:42:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:6607c3431ad2ac598c8476330688ee82114c9b3c0e9b2849f86d95addf5e48eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8406d4978e549630fb362ff2901a3645f7d325e1cce867bbfddade8ceb14232`

```dockerfile
```

-	Layers:
	-	`sha256:5ae6f5f57506c9cba95d087771e8253c7ee7c129dcbc4fdd524a99f4feeafec9`  
		Last Modified: Fri, 05 Dec 2025 04:34:37 GMT  
		Size: 94.3 KB (94276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b9a49d787a1cd02fea8b8affc293bd2d718765b8ef3d8cf26d839f80d072eea`  
		Last Modified: Fri, 05 Dec 2025 04:34:38 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; s390x

```console
$ docker pull memcached@sha256:b23b3b07e717d7651a02ec547a675f198e684f410c7217a09bd305de6c20e664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5878802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e586dd7e72674888df0e6f0ade73d053d2a5a94b7d890a276fb6f13fba7e4cc3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:22 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:19:24 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:22:39 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:22:39 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:22:39 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:22:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:22:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:22:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:22:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:22:39 GMT
USER memcache
# Thu, 04 Dec 2025 19:22:39 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:22:39 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a188510a1e7e85e0e83a71da1abed06b459c07887a679cf331da7789673755`  
		Last Modified: Thu, 04 Dec 2025 19:23:03 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67afe5cdcebd55aec1e59a816853f758650056c83c63ea4d99d6e06e15f60fd`  
		Last Modified: Thu, 04 Dec 2025 19:23:03 GMT  
		Size: 114.3 KB (114286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377a08e6b7dd38664aeee34c52a61b8f7edf9165adabbaee0e0b923423a60242`  
		Last Modified: Thu, 04 Dec 2025 19:23:03 GMT  
		Size: 2.0 MB (2039357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c47067ba1641d8aa2a1f3d7df1e359c1ef226673c5b60eeecc3824f3609e9b`  
		Last Modified: Thu, 04 Dec 2025 19:23:03 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e307cf70f379099e1c944f0972ea3478099fc2221e7ae304d3c47858cb9c8b`  
		Last Modified: Thu, 04 Dec 2025 19:23:03 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:db1f4e6b802cb9b4ee6a404e244522a143516b6c5dfe88d706e7d657e8a3c6c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e21cb3a2b9f702a014eac05118559131c607052ca17bd1adb7ddb02107d291d0`

```dockerfile
```

-	Layers:
	-	`sha256:a484d75866b9f2198dfeccc7d70aa01018c27dd00a8bdad7b47bb8f659ee35d1`  
		Last Modified: Thu, 04 Dec 2025 22:35:09 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e39d44972f86c94e48a8ba761774c90c693cfd7248b9b3fa84a7905217f0c57a`  
		Last Modified: Thu, 04 Dec 2025 22:35:10 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-trixie`

```console
$ docker pull memcached@sha256:c7628370ae681c42dbd48ccf02320d77a2bc0234f9ba3a968b5da3a7c0112469
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:1.6-trixie` - linux; amd64

```console
$ docker pull memcached@sha256:153e4ed762fd3bc07fe607f64631647939278d6101759d91fac0b756cceb2272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32208551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa0c800d7278560e11e4d0f14defc4d2d850224d0859d1bd0e9205cc962478d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:38:46 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:38:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:41:30 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:41:30 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:41:30 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:41:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:41:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:41:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:41:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:41:30 GMT
USER memcache
# Mon, 08 Dec 2025 22:41:30 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:41:30 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e33b5452dc8ba5d42cd13b42745898ef870af3e8d5a65b06b8b174f06b1d50`  
		Last Modified: Mon, 08 Dec 2025 22:41:43 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce4ec629da8029212ce5d775073648d04f1f014a89e49f73f1fc848bc405dd5`  
		Last Modified: Mon, 08 Dec 2025 22:41:43 GMT  
		Size: 136.7 KB (136697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6210dfd46759cbe6922de2db75ddf6d17c1f033a434ee6bcf2e82d56ce59f449`  
		Last Modified: Mon, 08 Dec 2025 22:41:43 GMT  
		Size: 2.3 MB (2293845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffbb5d472cb4680299753b978d2e8eeb6d2288ee4caec01e65541f4358516a6`  
		Last Modified: Mon, 08 Dec 2025 22:41:43 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e474cc606bdb91c69d2f124d38e5ebd93ed9ab64d219ab51845cc238a5904aa`  
		Last Modified: Mon, 08 Dec 2025 22:41:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:45cb4f875b600a26ef6e0388db256b09a14580b17ddcaa485fd2c25cbff56056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6483c69793152c682b93375229933004781cbf7df7f059d288d2d7e04335b2c8`

```dockerfile
```

-	Layers:
	-	`sha256:c3beab005b14cd0614637cc43c84460edfb07d9c68b1138ee676ab5bd3dc05ac`  
		Last Modified: Tue, 09 Dec 2025 01:34:56 GMT  
		Size: 2.0 MB (2008228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6ce8cbbfb878c257688fdf1d5e1a9c428b68061ee92f8e07a240ab0fe4b812e`  
		Last Modified: Tue, 09 Dec 2025 01:34:57 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:5a7b1183ed0a0ca89ce3d88e335fca2672422eee8d05921621cd4ed617965ed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30317206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1552234329fddb68f43cfe1abdf3dff1b1499edbb12eb6d84c481f3d7fbe2c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:34:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:37:32 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:37:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:37:32 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:37:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:37:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:37:32 GMT
USER memcache
# Mon, 08 Dec 2025 22:37:32 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:37:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d97bc71d0fa535127863fdab265dfddb07b3cda35b80de4dd2b9b67fe154c856`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 27.9 MB (27944187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d0d6688f3764bd09c70b0fdb00a12bc517f76c47fc187448da8cf7958b4b98`  
		Last Modified: Mon, 08 Dec 2025 22:37:44 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1a7c3cdaa260d51a1e04177297af5b7e205abe78e98f0782c38369f1a49034`  
		Last Modified: Mon, 08 Dec 2025 22:37:45 GMT  
		Size: 144.1 KB (144146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e35266d4886f5160ecccf89b51e0317cf6c7ad5a063a40d74c0dd0baa75b974`  
		Last Modified: Mon, 08 Dec 2025 22:37:45 GMT  
		Size: 2.2 MB (2227364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3324af035e2f7b73ce2f8c3d5ee46e80ed9063e2ae219caf112d6bafe3d935a3`  
		Last Modified: Mon, 08 Dec 2025 22:37:44 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae7d716f59ff9d69d00b890308b431e236e3a1d530f0dfa1ccaabdd01ea7df2`  
		Last Modified: Mon, 08 Dec 2025 22:37:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:077fa23fa7fd08a421aff7ec84a802bb72f53e3f31c9fb2bba4df39b99ae3923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92bd65e20c21649e0ebcbd5810944fd9e43ecf788ec1d580bfc3c04722bf6fa4`

```dockerfile
```

-	Layers:
	-	`sha256:02c0b341ef4c59b9ffa7a8de46289cbd08d3a3b029c0a64224da804b55e2e854`  
		Last Modified: Tue, 09 Dec 2025 01:35:01 GMT  
		Size: 2.0 MB (2011231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb1ede44c11856b6e3f7c4f6ba238d3df5677af459242c47b9f24b4a1c184db0`  
		Last Modified: Tue, 09 Dec 2025 01:35:02 GMT  
		Size: 22.3 KB (22302 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:cb9b94d371b2da6a520b577dd688b99c959dac8ad5e81f17aaf8e5b6ed1968ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28529520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a8988937956147836c267576a47663f836997a1d6a21750c17c7d2e52982c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:38:02 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:38:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:41:09 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:41:09 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:41:09 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:41:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:41:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:41:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:41:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:41:09 GMT
USER memcache
# Mon, 08 Dec 2025 22:41:09 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:41:09 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15599337d37fa53f93b66130266f60f942cc7c2c4e2e8458c672f9b61b921350`  
		Last Modified: Mon, 08 Dec 2025 22:41:22 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4e148e811da2c8aeb3f52da0f7e137c9e2dbf7e07ea25ed2a8ec2bc3db340d`  
		Last Modified: Mon, 08 Dec 2025 22:41:25 GMT  
		Size: 135.4 KB (135363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248d1bdc7fd809ba8d6d01e877ae1ff16258cd1b26203215342935af2305c133`  
		Last Modified: Mon, 08 Dec 2025 22:41:22 GMT  
		Size: 2.2 MB (2182634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4dca52427f97b68739a35240dde721713ae992674b8f6fe50fc71d987512c4`  
		Last Modified: Mon, 08 Dec 2025 22:41:22 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2961ef381f352090fe3d59e2ff32ae5c2979defa070a22f5fc846bb2b5f0f30`  
		Last Modified: Mon, 08 Dec 2025 22:41:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:cff996fea1034ca7a74465fdf5489ef45c78f70859319df22468100dc3c84e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e8d92fa13df244234c51ab1b93e9a4c39ad977f40dd5b49cef4e8ed0de7e3a`

```dockerfile
```

-	Layers:
	-	`sha256:d08663eef9d4f14b4b344cf2d8924f04dee694d602df55d600a90830f505069b`  
		Last Modified: Tue, 09 Dec 2025 01:35:06 GMT  
		Size: 2.0 MB (2009688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb1b323cef393d68691ca1f808424d4c4ca9aa868a63329889d55c9e53c30671`  
		Last Modified: Tue, 09 Dec 2025 01:35:06 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:6230125fff57e6f22504aae8db1ed049b738d97c3e325a68a9733a186fab61e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32568877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2f55b9564478802d59f2ab50cadac0b6e11704297ea84bc7fdcc4e9fb3ba76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:38:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:38:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:41:20 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:41:20 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:41:20 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:41:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:41:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:41:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:41:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:41:20 GMT
USER memcache
# Mon, 08 Dec 2025 22:41:20 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:41:20 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91cd2e642e1c9b79606d81fe7ae3f5599c2e1a2ebb80864a1c25f4771502b02`  
		Last Modified: Mon, 08 Dec 2025 22:41:32 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9b5941656d039525e2c86c6dad7b225e0dfe8a89bda1c33c46f84b7e1f05f0`  
		Last Modified: Mon, 08 Dec 2025 22:41:32 GMT  
		Size: 153.5 KB (153454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc829d43c3195e76b119f7ef9e8519d7c64f130e104b29b5317d18e709d3796`  
		Last Modified: Mon, 08 Dec 2025 22:41:32 GMT  
		Size: 2.3 MB (2275286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685e3db2e1ea7f3a85650a5cac398166f6fe54b1767d8ab65fd070fc9f08f903`  
		Last Modified: Mon, 08 Dec 2025 22:41:32 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bedd2011ff5fea2608113c25dac443f7f67fd30b9f049d14304a5eeba342453`  
		Last Modified: Mon, 08 Dec 2025 22:41:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:5be232fd0ce753823a0a00a2e155ca7ed374028d0a228270604974765be63286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ad988781bd90f9b424c8530a983604f0dea5e9ff5d39be9ca322ea793f7044`

```dockerfile
```

-	Layers:
	-	`sha256:2f225cf8fe800d6f4631961cb099b7f796ad28fbe325df7943d5fd182391187f`  
		Last Modified: Tue, 09 Dec 2025 01:35:10 GMT  
		Size: 2.0 MB (2008544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd6800d8108ddffdecd1e6d030f8948b6ed22cff74e19779380d731dfd189d0d`  
		Last Modified: Tue, 09 Dec 2025 01:35:11 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; 386

```console
$ docker pull memcached@sha256:9c8dd1c0a7d71ffb9540bcdac40c6c72661b05ad12d1a0dcacb86ba0dad353b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33686582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a221f2cf3f75cb38b8be293e0d315a4453967306dc401835f3732a7ec18482d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:17 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:33:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:36:13 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:36:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:36:13 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:36:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:36:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:36:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:36:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:36:13 GMT
USER memcache
# Mon, 08 Dec 2025 22:36:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:36:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c63a49351bc91fd837d81e97ce862507215607bc756f1133f1d887e94e1cc4e`  
		Last Modified: Mon, 08 Dec 2025 22:36:26 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7073e103108a28c5e5a1458be46ac8c708375f2b4327423a59471a77bbf2c0c6`  
		Last Modified: Mon, 08 Dec 2025 22:36:26 GMT  
		Size: 147.5 KB (147516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbfa39b86ad2206ef2fdf5ec3f3a55aa40c422a9f3fca094c7c2f003e7d4a63`  
		Last Modified: Mon, 08 Dec 2025 22:36:26 GMT  
		Size: 2.2 MB (2244483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1ade71ea049e11fc9cea7c16944632ffd753dfe7130e3bb4e1730281daffb5`  
		Last Modified: Mon, 08 Dec 2025 22:36:26 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5eb870312490559d775f9d994ba10b9fcae44c680e23a647a43c1c55f49b54`  
		Last Modified: Mon, 08 Dec 2025 22:36:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:e5ea0a4780f0574f775d4cf8c4ffff6f6b836e33d54d6d241047fa36e54d70b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1425c202287fb1c6f81bb3962bb416b9f23b14b12da6119772ac599ae7af4b`

```dockerfile
```

-	Layers:
	-	`sha256:9d6ed296b190f0f66c6f54ffafa76bd9f86d72e2a463ed9841c2654abf7282d0`  
		Last Modified: Tue, 09 Dec 2025 01:35:16 GMT  
		Size: 2.0 MB (2005385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d9f28b39486b665dcd60f89a225a5fce2e4060feaed50b57eaf89bc54345129`  
		Last Modified: Tue, 09 Dec 2025 01:35:17 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:9a5a8c51d01a2dde31ee88dc7739b61aad1cd244c1592033d64b89e71ea9d086
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36185779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62a722a142df5369183f571c8eecacbc8041e72fb89888b569e2e558947291b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:32:15 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 09 Dec 2025 00:32:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:35:25 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 09 Dec 2025 00:35:25 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 09 Dec 2025 00:35:25 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 09 Dec 2025 00:35:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 09 Dec 2025 00:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 00:35:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 09 Dec 2025 00:35:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Dec 2025 00:35:26 GMT
USER memcache
# Tue, 09 Dec 2025 00:35:26 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 09 Dec 2025 00:35:26 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca80ecfb634d24079bf04d5695260ea9dce9f468064fb83123a71959d22b7c4`  
		Last Modified: Tue, 09 Dec 2025 00:35:51 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb90fb01769b3666ac21d77bcba16bd54161463250fa6f304710eb00d5ab5411`  
		Last Modified: Tue, 09 Dec 2025 00:35:51 GMT  
		Size: 170.4 KB (170375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be675ba49db497b747d37543689ff0b8fc0ef4398cd718c2fadd28302d88141b`  
		Last Modified: Tue, 09 Dec 2025 00:35:51 GMT  
		Size: 2.4 MB (2417005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882b9516d2a74a32203b37778b6025dc9c68a30838e1fa420559c34fe0319141`  
		Last Modified: Tue, 09 Dec 2025 00:35:51 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5cfa5b161387b536b9f8a94f199ffd006893e19e7bff82a8f1f9a7aa578a73`  
		Last Modified: Tue, 09 Dec 2025 00:35:51 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:6ea51b9da9219f68c45e3345bed106b961bce70b2c9aecbb6e1300060e04217d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f87eac26bbbb68ef23dfd63867d0415ddc04fe2567863569701f2891733279d6`

```dockerfile
```

-	Layers:
	-	`sha256:6f8bb9e427f03eea07711eb22a22462b3548d9ed3bf7b82f412aea5a623b10ff`  
		Last Modified: Tue, 09 Dec 2025 04:34:42 GMT  
		Size: 2.0 MB (2011829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1705de570678d9ecda7c8bb1da82748111d8547fb22bfbfb43fbbf41808b5b67`  
		Last Modified: Tue, 09 Dec 2025 04:34:43 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:05d76bdff41209572f5e6c4d21717d0717a794340a2bc2c086af7a863f5c19af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30627687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c785d7526540c98189bc45e1c3ad5a9862a6ed744c2b49e94165199ba9dcd7ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 10:11:36 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 10:12:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 10:53:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 10:53:11 GMT
USER memcache
# Tue, 18 Nov 2025 10:53:11 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 10:53:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f7062dea9fa0a796a2eacb7b265e4b2000be3d07bc91c20a5abc6538e5a68c`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f8a04356a93113399cb041ac377cf221db2df7d9fc3a6d630a061a923eb1e6`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 133.1 KB (133088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4bbee7a68150daca8b6b94e26e1a04551afc5a77dfb08a4e04aadc0933c456`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 2.2 MB (2219954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085465091dfa79c5f79dd2c74f56f75a8e078b89272039f8d8ed5a1d2adac41b`  
		Last Modified: Tue, 18 Nov 2025 10:54:06 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea3aae46e46f60ca268fd3c445c8b9ed827d7daba7e6d611310cfc9dc4d5291`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:7a8af6c2848585e79b5cb65b6a760b1f78f0de3a59fb604d7a026c79f05a77b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c73002e7361572816b1c22cbb73aced8ce908f6492f2b5d15371b7c0a0514546`

```dockerfile
```

-	Layers:
	-	`sha256:059e3337eaf5c7461d584e0f4b5c7c660bf41a1bb79e90aa917a3992eba4c855`  
		Last Modified: Tue, 18 Nov 2025 16:35:44 GMT  
		Size: 2.0 MB (2002192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cf39200d9e698624fc7d7abe914cab80bda5407ae30f111eb22846e8fd28bba`  
		Last Modified: Tue, 18 Nov 2025 16:35:45 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:332c41cfc207814782dda23a2b840d653abb751f335f7f02f6b238ce79c1c08c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32290312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2be68b3a60f2d8e906983e133fcaffe03bd1a82c9acc69a3dcbe3e307d7b8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:21 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:33:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:36:33 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:36:33 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:36:33 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:36:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:36:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:36:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:36:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:36:34 GMT
USER memcache
# Mon, 08 Dec 2025 22:36:34 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:36:34 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc040aa39039515a9f8b38dc90047178bd8fa0d8234856954f045f05050e52c`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e235f00f3da465d44b7ac18782958812c19e974f091dedfc097442ba632a3d`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 140.5 KB (140505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284c7cc2b7cc68de54eb5bce5de02ed5229cb403476e794b8066eee16babb6e1`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 2.3 MB (2313897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5059135976f7ec26a104b2fb6340b0ae8adc5756ea159deede93c8532613fd24`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd63939e0e5898afa1d51d59354c263e9a7ebfba3e418395baf21445315251de`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:8a7be7ae9cfd628f1585c887ce286f74e97f7780cc20009ffe07f9c92623b34c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c6fbc39d1b80ba4ed6852329a8ddfcaaeed5500129f5019fbc5a8904a7cd659`

```dockerfile
```

-	Layers:
	-	`sha256:0a66a7a3c4891f559fc098f2c13e48d32804e22f559857d3c89074b829300c25`  
		Last Modified: Tue, 09 Dec 2025 01:35:26 GMT  
		Size: 2.0 MB (2009665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24d3a4bbcde50a51a341ad980cc2d92d652ec5f9394c80d55c8a70ded47d8927`  
		Last Modified: Tue, 09 Dec 2025 01:35:27 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.39`

```console
$ docker pull memcached@sha256:c7628370ae681c42dbd48ccf02320d77a2bc0234f9ba3a968b5da3a7c0112469
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:1.6.39` - linux; amd64

```console
$ docker pull memcached@sha256:153e4ed762fd3bc07fe607f64631647939278d6101759d91fac0b756cceb2272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32208551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa0c800d7278560e11e4d0f14defc4d2d850224d0859d1bd0e9205cc962478d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:38:46 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:38:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:41:30 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:41:30 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:41:30 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:41:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:41:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:41:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:41:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:41:30 GMT
USER memcache
# Mon, 08 Dec 2025 22:41:30 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:41:30 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e33b5452dc8ba5d42cd13b42745898ef870af3e8d5a65b06b8b174f06b1d50`  
		Last Modified: Mon, 08 Dec 2025 22:41:43 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce4ec629da8029212ce5d775073648d04f1f014a89e49f73f1fc848bc405dd5`  
		Last Modified: Mon, 08 Dec 2025 22:41:43 GMT  
		Size: 136.7 KB (136697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6210dfd46759cbe6922de2db75ddf6d17c1f033a434ee6bcf2e82d56ce59f449`  
		Last Modified: Mon, 08 Dec 2025 22:41:43 GMT  
		Size: 2.3 MB (2293845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffbb5d472cb4680299753b978d2e8eeb6d2288ee4caec01e65541f4358516a6`  
		Last Modified: Mon, 08 Dec 2025 22:41:43 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e474cc606bdb91c69d2f124d38e5ebd93ed9ab64d219ab51845cc238a5904aa`  
		Last Modified: Mon, 08 Dec 2025 22:41:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39` - unknown; unknown

```console
$ docker pull memcached@sha256:45cb4f875b600a26ef6e0388db256b09a14580b17ddcaa485fd2c25cbff56056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6483c69793152c682b93375229933004781cbf7df7f059d288d2d7e04335b2c8`

```dockerfile
```

-	Layers:
	-	`sha256:c3beab005b14cd0614637cc43c84460edfb07d9c68b1138ee676ab5bd3dc05ac`  
		Last Modified: Tue, 09 Dec 2025 01:34:56 GMT  
		Size: 2.0 MB (2008228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6ce8cbbfb878c257688fdf1d5e1a9c428b68061ee92f8e07a240ab0fe4b812e`  
		Last Modified: Tue, 09 Dec 2025 01:34:57 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39` - linux; arm variant v5

```console
$ docker pull memcached@sha256:5a7b1183ed0a0ca89ce3d88e335fca2672422eee8d05921621cd4ed617965ed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30317206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1552234329fddb68f43cfe1abdf3dff1b1499edbb12eb6d84c481f3d7fbe2c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:34:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:37:32 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:37:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:37:32 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:37:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:37:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:37:32 GMT
USER memcache
# Mon, 08 Dec 2025 22:37:32 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:37:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d97bc71d0fa535127863fdab265dfddb07b3cda35b80de4dd2b9b67fe154c856`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 27.9 MB (27944187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d0d6688f3764bd09c70b0fdb00a12bc517f76c47fc187448da8cf7958b4b98`  
		Last Modified: Mon, 08 Dec 2025 22:37:44 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1a7c3cdaa260d51a1e04177297af5b7e205abe78e98f0782c38369f1a49034`  
		Last Modified: Mon, 08 Dec 2025 22:37:45 GMT  
		Size: 144.1 KB (144146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e35266d4886f5160ecccf89b51e0317cf6c7ad5a063a40d74c0dd0baa75b974`  
		Last Modified: Mon, 08 Dec 2025 22:37:45 GMT  
		Size: 2.2 MB (2227364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3324af035e2f7b73ce2f8c3d5ee46e80ed9063e2ae219caf112d6bafe3d935a3`  
		Last Modified: Mon, 08 Dec 2025 22:37:44 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae7d716f59ff9d69d00b890308b431e236e3a1d530f0dfa1ccaabdd01ea7df2`  
		Last Modified: Mon, 08 Dec 2025 22:37:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39` - unknown; unknown

```console
$ docker pull memcached@sha256:077fa23fa7fd08a421aff7ec84a802bb72f53e3f31c9fb2bba4df39b99ae3923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92bd65e20c21649e0ebcbd5810944fd9e43ecf788ec1d580bfc3c04722bf6fa4`

```dockerfile
```

-	Layers:
	-	`sha256:02c0b341ef4c59b9ffa7a8de46289cbd08d3a3b029c0a64224da804b55e2e854`  
		Last Modified: Tue, 09 Dec 2025 01:35:01 GMT  
		Size: 2.0 MB (2011231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb1ede44c11856b6e3f7c4f6ba238d3df5677af459242c47b9f24b4a1c184db0`  
		Last Modified: Tue, 09 Dec 2025 01:35:02 GMT  
		Size: 22.3 KB (22302 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39` - linux; arm variant v7

```console
$ docker pull memcached@sha256:cb9b94d371b2da6a520b577dd688b99c959dac8ad5e81f17aaf8e5b6ed1968ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28529520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a8988937956147836c267576a47663f836997a1d6a21750c17c7d2e52982c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:38:02 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:38:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:41:09 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:41:09 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:41:09 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:41:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:41:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:41:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:41:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:41:09 GMT
USER memcache
# Mon, 08 Dec 2025 22:41:09 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:41:09 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15599337d37fa53f93b66130266f60f942cc7c2c4e2e8458c672f9b61b921350`  
		Last Modified: Mon, 08 Dec 2025 22:41:22 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4e148e811da2c8aeb3f52da0f7e137c9e2dbf7e07ea25ed2a8ec2bc3db340d`  
		Last Modified: Mon, 08 Dec 2025 22:41:25 GMT  
		Size: 135.4 KB (135363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248d1bdc7fd809ba8d6d01e877ae1ff16258cd1b26203215342935af2305c133`  
		Last Modified: Mon, 08 Dec 2025 22:41:22 GMT  
		Size: 2.2 MB (2182634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4dca52427f97b68739a35240dde721713ae992674b8f6fe50fc71d987512c4`  
		Last Modified: Mon, 08 Dec 2025 22:41:22 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2961ef381f352090fe3d59e2ff32ae5c2979defa070a22f5fc846bb2b5f0f30`  
		Last Modified: Mon, 08 Dec 2025 22:41:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39` - unknown; unknown

```console
$ docker pull memcached@sha256:cff996fea1034ca7a74465fdf5489ef45c78f70859319df22468100dc3c84e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e8d92fa13df244234c51ab1b93e9a4c39ad977f40dd5b49cef4e8ed0de7e3a`

```dockerfile
```

-	Layers:
	-	`sha256:d08663eef9d4f14b4b344cf2d8924f04dee694d602df55d600a90830f505069b`  
		Last Modified: Tue, 09 Dec 2025 01:35:06 GMT  
		Size: 2.0 MB (2009688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb1b323cef393d68691ca1f808424d4c4ca9aa868a63329889d55c9e53c30671`  
		Last Modified: Tue, 09 Dec 2025 01:35:06 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:6230125fff57e6f22504aae8db1ed049b738d97c3e325a68a9733a186fab61e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32568877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2f55b9564478802d59f2ab50cadac0b6e11704297ea84bc7fdcc4e9fb3ba76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:38:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:38:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:41:20 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:41:20 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:41:20 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:41:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:41:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:41:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:41:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:41:20 GMT
USER memcache
# Mon, 08 Dec 2025 22:41:20 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:41:20 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91cd2e642e1c9b79606d81fe7ae3f5599c2e1a2ebb80864a1c25f4771502b02`  
		Last Modified: Mon, 08 Dec 2025 22:41:32 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9b5941656d039525e2c86c6dad7b225e0dfe8a89bda1c33c46f84b7e1f05f0`  
		Last Modified: Mon, 08 Dec 2025 22:41:32 GMT  
		Size: 153.5 KB (153454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc829d43c3195e76b119f7ef9e8519d7c64f130e104b29b5317d18e709d3796`  
		Last Modified: Mon, 08 Dec 2025 22:41:32 GMT  
		Size: 2.3 MB (2275286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685e3db2e1ea7f3a85650a5cac398166f6fe54b1767d8ab65fd070fc9f08f903`  
		Last Modified: Mon, 08 Dec 2025 22:41:32 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bedd2011ff5fea2608113c25dac443f7f67fd30b9f049d14304a5eeba342453`  
		Last Modified: Mon, 08 Dec 2025 22:41:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39` - unknown; unknown

```console
$ docker pull memcached@sha256:5be232fd0ce753823a0a00a2e155ca7ed374028d0a228270604974765be63286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ad988781bd90f9b424c8530a983604f0dea5e9ff5d39be9ca322ea793f7044`

```dockerfile
```

-	Layers:
	-	`sha256:2f225cf8fe800d6f4631961cb099b7f796ad28fbe325df7943d5fd182391187f`  
		Last Modified: Tue, 09 Dec 2025 01:35:10 GMT  
		Size: 2.0 MB (2008544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd6800d8108ddffdecd1e6d030f8948b6ed22cff74e19779380d731dfd189d0d`  
		Last Modified: Tue, 09 Dec 2025 01:35:11 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39` - linux; 386

```console
$ docker pull memcached@sha256:9c8dd1c0a7d71ffb9540bcdac40c6c72661b05ad12d1a0dcacb86ba0dad353b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33686582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a221f2cf3f75cb38b8be293e0d315a4453967306dc401835f3732a7ec18482d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:17 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:33:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:36:13 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:36:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:36:13 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:36:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:36:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:36:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:36:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:36:13 GMT
USER memcache
# Mon, 08 Dec 2025 22:36:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:36:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c63a49351bc91fd837d81e97ce862507215607bc756f1133f1d887e94e1cc4e`  
		Last Modified: Mon, 08 Dec 2025 22:36:26 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7073e103108a28c5e5a1458be46ac8c708375f2b4327423a59471a77bbf2c0c6`  
		Last Modified: Mon, 08 Dec 2025 22:36:26 GMT  
		Size: 147.5 KB (147516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbfa39b86ad2206ef2fdf5ec3f3a55aa40c422a9f3fca094c7c2f003e7d4a63`  
		Last Modified: Mon, 08 Dec 2025 22:36:26 GMT  
		Size: 2.2 MB (2244483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1ade71ea049e11fc9cea7c16944632ffd753dfe7130e3bb4e1730281daffb5`  
		Last Modified: Mon, 08 Dec 2025 22:36:26 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5eb870312490559d775f9d994ba10b9fcae44c680e23a647a43c1c55f49b54`  
		Last Modified: Mon, 08 Dec 2025 22:36:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39` - unknown; unknown

```console
$ docker pull memcached@sha256:e5ea0a4780f0574f775d4cf8c4ffff6f6b836e33d54d6d241047fa36e54d70b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1425c202287fb1c6f81bb3962bb416b9f23b14b12da6119772ac599ae7af4b`

```dockerfile
```

-	Layers:
	-	`sha256:9d6ed296b190f0f66c6f54ffafa76bd9f86d72e2a463ed9841c2654abf7282d0`  
		Last Modified: Tue, 09 Dec 2025 01:35:16 GMT  
		Size: 2.0 MB (2005385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d9f28b39486b665dcd60f89a225a5fce2e4060feaed50b57eaf89bc54345129`  
		Last Modified: Tue, 09 Dec 2025 01:35:17 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39` - linux; ppc64le

```console
$ docker pull memcached@sha256:9a5a8c51d01a2dde31ee88dc7739b61aad1cd244c1592033d64b89e71ea9d086
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36185779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62a722a142df5369183f571c8eecacbc8041e72fb89888b569e2e558947291b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:32:15 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 09 Dec 2025 00:32:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:35:25 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 09 Dec 2025 00:35:25 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 09 Dec 2025 00:35:25 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 09 Dec 2025 00:35:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 09 Dec 2025 00:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 00:35:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 09 Dec 2025 00:35:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Dec 2025 00:35:26 GMT
USER memcache
# Tue, 09 Dec 2025 00:35:26 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 09 Dec 2025 00:35:26 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca80ecfb634d24079bf04d5695260ea9dce9f468064fb83123a71959d22b7c4`  
		Last Modified: Tue, 09 Dec 2025 00:35:51 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb90fb01769b3666ac21d77bcba16bd54161463250fa6f304710eb00d5ab5411`  
		Last Modified: Tue, 09 Dec 2025 00:35:51 GMT  
		Size: 170.4 KB (170375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be675ba49db497b747d37543689ff0b8fc0ef4398cd718c2fadd28302d88141b`  
		Last Modified: Tue, 09 Dec 2025 00:35:51 GMT  
		Size: 2.4 MB (2417005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882b9516d2a74a32203b37778b6025dc9c68a30838e1fa420559c34fe0319141`  
		Last Modified: Tue, 09 Dec 2025 00:35:51 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5cfa5b161387b536b9f8a94f199ffd006893e19e7bff82a8f1f9a7aa578a73`  
		Last Modified: Tue, 09 Dec 2025 00:35:51 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39` - unknown; unknown

```console
$ docker pull memcached@sha256:6ea51b9da9219f68c45e3345bed106b961bce70b2c9aecbb6e1300060e04217d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f87eac26bbbb68ef23dfd63867d0415ddc04fe2567863569701f2891733279d6`

```dockerfile
```

-	Layers:
	-	`sha256:6f8bb9e427f03eea07711eb22a22462b3548d9ed3bf7b82f412aea5a623b10ff`  
		Last Modified: Tue, 09 Dec 2025 04:34:42 GMT  
		Size: 2.0 MB (2011829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1705de570678d9ecda7c8bb1da82748111d8547fb22bfbfb43fbbf41808b5b67`  
		Last Modified: Tue, 09 Dec 2025 04:34:43 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39` - linux; riscv64

```console
$ docker pull memcached@sha256:05d76bdff41209572f5e6c4d21717d0717a794340a2bc2c086af7a863f5c19af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30627687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c785d7526540c98189bc45e1c3ad5a9862a6ed744c2b49e94165199ba9dcd7ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 10:11:36 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 10:12:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 10:53:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 10:53:11 GMT
USER memcache
# Tue, 18 Nov 2025 10:53:11 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 10:53:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f7062dea9fa0a796a2eacb7b265e4b2000be3d07bc91c20a5abc6538e5a68c`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f8a04356a93113399cb041ac377cf221db2df7d9fc3a6d630a061a923eb1e6`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 133.1 KB (133088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4bbee7a68150daca8b6b94e26e1a04551afc5a77dfb08a4e04aadc0933c456`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 2.2 MB (2219954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085465091dfa79c5f79dd2c74f56f75a8e078b89272039f8d8ed5a1d2adac41b`  
		Last Modified: Tue, 18 Nov 2025 10:54:06 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea3aae46e46f60ca268fd3c445c8b9ed827d7daba7e6d611310cfc9dc4d5291`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39` - unknown; unknown

```console
$ docker pull memcached@sha256:7a8af6c2848585e79b5cb65b6a760b1f78f0de3a59fb604d7a026c79f05a77b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c73002e7361572816b1c22cbb73aced8ce908f6492f2b5d15371b7c0a0514546`

```dockerfile
```

-	Layers:
	-	`sha256:059e3337eaf5c7461d584e0f4b5c7c660bf41a1bb79e90aa917a3992eba4c855`  
		Last Modified: Tue, 18 Nov 2025 16:35:44 GMT  
		Size: 2.0 MB (2002192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cf39200d9e698624fc7d7abe914cab80bda5407ae30f111eb22846e8fd28bba`  
		Last Modified: Tue, 18 Nov 2025 16:35:45 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39` - linux; s390x

```console
$ docker pull memcached@sha256:332c41cfc207814782dda23a2b840d653abb751f335f7f02f6b238ce79c1c08c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32290312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2be68b3a60f2d8e906983e133fcaffe03bd1a82c9acc69a3dcbe3e307d7b8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:21 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:33:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:36:33 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:36:33 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:36:33 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:36:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:36:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:36:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:36:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:36:34 GMT
USER memcache
# Mon, 08 Dec 2025 22:36:34 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:36:34 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc040aa39039515a9f8b38dc90047178bd8fa0d8234856954f045f05050e52c`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e235f00f3da465d44b7ac18782958812c19e974f091dedfc097442ba632a3d`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 140.5 KB (140505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284c7cc2b7cc68de54eb5bce5de02ed5229cb403476e794b8066eee16babb6e1`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 2.3 MB (2313897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5059135976f7ec26a104b2fb6340b0ae8adc5756ea159deede93c8532613fd24`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd63939e0e5898afa1d51d59354c263e9a7ebfba3e418395baf21445315251de`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39` - unknown; unknown

```console
$ docker pull memcached@sha256:8a7be7ae9cfd628f1585c887ce286f74e97f7780cc20009ffe07f9c92623b34c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c6fbc39d1b80ba4ed6852329a8ddfcaaeed5500129f5019fbc5a8904a7cd659`

```dockerfile
```

-	Layers:
	-	`sha256:0a66a7a3c4891f559fc098f2c13e48d32804e22f559857d3c89074b829300c25`  
		Last Modified: Tue, 09 Dec 2025 01:35:26 GMT  
		Size: 2.0 MB (2009665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24d3a4bbcde50a51a341ad980cc2d92d652ec5f9394c80d55c8a70ded47d8927`  
		Last Modified: Tue, 09 Dec 2025 01:35:27 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.39-alpine`

```console
$ docker pull memcached@sha256:c8503d4491edd3110cc07d0465089d3a41cf1daf8645e71149e39a51835e92cd
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
$ docker pull memcached@sha256:aac456c35cd29635b5501fefac58a2e954752006c9d159fbf520dd785e09cbba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5973577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6411cdd430a5f0c33aea6496062ab90fbc7da776f1c937108cf51b7a40e090f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:20:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:20:42 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:23:18 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:23:18 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:23:18 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:23:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:23:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:23:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:23:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:23:18 GMT
USER memcache
# Thu, 04 Dec 2025 19:23:18 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:23:18 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e377e19df274e9919dbfbe05b510e54db0f8451ac0985b108aba9123048001d8`  
		Last Modified: Thu, 04 Dec 2025 19:23:54 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0d9328fb6b4452be1f62a5c6db62b8425a6b48c40ce2408ae0f526b101c80c`  
		Last Modified: Thu, 04 Dec 2025 19:23:55 GMT  
		Size: 106.0 KB (106047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a1eb06c51acdaf80ce22a4524ea827613ecc609e23cb0fa481005e89b22d4f`  
		Last Modified: Thu, 04 Dec 2025 19:23:54 GMT  
		Size: 2.0 MB (2006867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4829db5772d5079a1be438e2b4d4921e584e88e6becb7ca1819f33cc6ddd962c`  
		Last Modified: Thu, 04 Dec 2025 19:23:54 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b919142486c25c1941bfb65c0f6f26ff49ed2820b62db8ee149ac5a386bcd76c`  
		Last Modified: Thu, 04 Dec 2025 19:23:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:849b937b30f8457f48d4a2b4dee48812e3f3fef3740e8553fbeb950ef1e6a405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3eb9da9040350a8be21d03f2423ac5b520d62898c8656b204d89a46be87cca`

```dockerfile
```

-	Layers:
	-	`sha256:a6a585b25dcf23d45fe100d658f3fc872a69be33f37f5b142951380b902e1a65`  
		Last Modified: Thu, 04 Dec 2025 22:34:43 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91e8f143d354857f78ae4fd0e5416b79eb34dc3599af1f3df2161a4fa1885af9`  
		Last Modified: Thu, 04 Dec 2025 22:34:44 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:a7003e700207ebf4fd102e5d81432129cd3e4776c613ee53fa01b0dbd5e9f19b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5629653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36796824ef2ab4ff08673e2fdd2ff3529a8c6c476c842ec665b90db7e63fad02`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:21:33 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:21:34 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:33:55 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:33:55 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:33:55 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:33:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:33:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:33:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:33:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:33:55 GMT
USER memcache
# Thu, 04 Dec 2025 19:33:55 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:33:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2477fbd5a498e104db4354cbb88ebe3bf7d7f22609c3d9f3996ee3d6f2b311`  
		Last Modified: Thu, 04 Dec 2025 19:34:10 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d610e2e19bb7ad98b2e77e581123187db039c4259f548f8e16e1b5015d0ec85`  
		Last Modified: Thu, 04 Dec 2025 19:34:10 GMT  
		Size: 102.6 KB (102642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5e9f0ad4522a9fedea5ba5229899ef09d25774a89a517cf59cae7a36e4ea92`  
		Last Modified: Thu, 04 Dec 2025 19:34:10 GMT  
		Size: 2.0 MB (1957764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8b426cdf478aef96c3b7780b5b6c81b458a0787358d6251799150a9f714aaf`  
		Last Modified: Thu, 04 Dec 2025 19:34:10 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd456d3218701485ecd1ce99f10c7a08986e44f71d19a49e419582aeb4924f52`  
		Last Modified: Thu, 04 Dec 2025 19:34:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:95ab79e458ab0908467ebbdf5539b688045b04421a068fa6821d557eece2f67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569a816a11d27d030ea4089563f4a23efecb872605941df1c53c0c4152fbd211`

```dockerfile
```

-	Layers:
	-	`sha256:dd9475807057d6ac4c96f526dc77e867efe6bb682d09ef1c7c0557b6f2dad356`  
		Last Modified: Thu, 04 Dec 2025 22:34:47 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:6b1fcd05fdcf13d4b7650d85e6043cdeaf423fe9ec57036c0f203e4eef6bff12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5289618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca393e3ead8035915d8cd6bcea0e8ccbe82d8ae05b9cad79126dd93567ff2889`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:43 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:19:44 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:22:37 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:22:37 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:22:37 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:22:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:22:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:22:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:22:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:22:37 GMT
USER memcache
# Thu, 04 Dec 2025 19:22:37 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:22:37 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdc28d0a8cb5092fb181830a0ef7fb2c55b0dcec915fb49171721470a36990e`  
		Last Modified: Thu, 04 Dec 2025 19:22:53 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d64ac2dd6859410fc8786621ad68f29d5cf9799784bd6181fa0fd9b16f10b5`  
		Last Modified: Thu, 04 Dec 2025 19:22:53 GMT  
		Size: 92.4 KB (92376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf39f9a50690d556c95f99315866a17736de133854b3f4a1f01c007e8ea52e8c`  
		Last Modified: Thu, 04 Dec 2025 19:22:53 GMT  
		Size: 1.9 MB (1917424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5adf2295dafdfb5341494ff56dfa3c9fef413e476cc7e0ea0a44ea325856fd40`  
		Last Modified: Thu, 04 Dec 2025 19:22:53 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f68652d871fbfba49b4bdb6f0555e3d086490ac907f630de1960481a50b5982`  
		Last Modified: Thu, 04 Dec 2025 19:22:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:726bec6c0e6bb11f92cf809b0eff6ee10fc86a30eae935ac85e0b82f2fc110d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:489bd5540d03661ecd23b22a8d9070b7dc18f542d91bc1ed60efaa1790080a39`

```dockerfile
```

-	Layers:
	-	`sha256:35def5ffffb77a9cc93b2d806351b5bc638603257621ee3ea2fcab826508b445`  
		Last Modified: Thu, 04 Dec 2025 22:34:50 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b55f58069fda39e67b560d97ac46c79e035b513a560bc8652e5383cd3f82a35`  
		Last Modified: Thu, 04 Dec 2025 22:34:51 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b263323af06e550df9becd8c2cf8450400be7ae4381392593565dc8247bb230f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6304413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:038de42e33564e147549bf3846c2490c168364063ebc7744c8cdd580e202c191`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:20:28 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:20:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:23:16 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:23:16 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:23:16 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:23:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:23:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:23:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:23:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:23:16 GMT
USER memcache
# Thu, 04 Dec 2025 19:23:16 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:23:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4ea1ce2b4c6bdcd3eec4d60b1aa2e3563da544759bff4e7a46469132a86438`  
		Last Modified: Thu, 04 Dec 2025 19:23:27 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc9938ef133bd132ee91a60f23198ae468dca72e6b547301fc4b29e4136bc9e`  
		Last Modified: Thu, 04 Dec 2025 19:23:28 GMT  
		Size: 121.9 KB (121870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fbb7f498823838642f0cbc3dfbcce9ec16c50549649b23872df57076fed9e7`  
		Last Modified: Thu, 04 Dec 2025 19:23:28 GMT  
		Size: 2.0 MB (1985993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341b9a721d462e12012b285eb88cdd865e1fa62f664d8343c3223d3b18b5ed0c`  
		Last Modified: Thu, 04 Dec 2025 19:23:27 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f879a6e1902c8a256d8dea45afd4efc95caa82bd9fcf3291b6730a20d2c5a0`  
		Last Modified: Thu, 04 Dec 2025 19:23:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9e1d743b77c8856403d4e8420e9936de4aa1bc6fc88642c47112e318e10e2655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556ecd6a50c7ec0f18eea0bb6b6a3c2a30163cdbf6e0a9314ef069819efdb628`

```dockerfile
```

-	Layers:
	-	`sha256:57a22eef052f1e8ba0bdbfa2e165923ea29a9572ab9d397f6652f44a895c34c9`  
		Last Modified: Thu, 04 Dec 2025 22:34:54 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea1714f2bc9b4e6925e95bfc0d324fe4686d662ad257e5959451179599d072e6`  
		Last Modified: Thu, 04 Dec 2025 22:34:55 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine` - linux; 386

```console
$ docker pull memcached@sha256:b3d88ad28118ac190ff8cfd6be5b29a4aff4e4f772124ba8a6cb7335eb909152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5762624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfa1253f0cf9e80c36b723ff6f79bb43b3cb4c3146f4340f605aaf0bb812eaa1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:20:00 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:20:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:22:43 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:22:43 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:22:43 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:22:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:22:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:22:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:22:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:22:43 GMT
USER memcache
# Thu, 04 Dec 2025 19:22:43 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:22:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3527b4f952d5950d8caa74dc0d1759215000f2f0a195344f0239c7e2805fe2fc`  
		Last Modified: Wed, 03 Dec 2025 19:30:41 GMT  
		Size: 3.7 MB (3685856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801e2ef7c6c58c48cfc036b3ffd9de546ffd13f67044c4c296b3624d08852398`  
		Last Modified: Thu, 04 Dec 2025 19:22:57 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7528d81de6e75b8aa074f7b96d6b9f2650422ca25fc0f5485dadf33879a4eb7`  
		Last Modified: Thu, 04 Dec 2025 19:22:57 GMT  
		Size: 110.7 KB (110732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40cb203b33be80dad7c861215d0c69239f729987a3942b71d4fc7b17423658e`  
		Last Modified: Thu, 04 Dec 2025 19:22:58 GMT  
		Size: 2.0 MB (1964688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbaa8273de612bce797fce27339a8adb341655d9b03a120aa874e80bfc438ba`  
		Last Modified: Thu, 04 Dec 2025 19:22:57 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a62b5e894734682a138338f04d49ebcb3e61a322469798019f9737e8ef19b33`  
		Last Modified: Thu, 04 Dec 2025 19:22:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:a8428c10b46dc321be308528a9dc3904db404457e03384a035c6e8c7bf32d05e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c97e68a8fd4c390f7dac3c43eda5f00b0b29eb2b838b877b0926ec7a55ec29`

```dockerfile
```

-	Layers:
	-	`sha256:5414f83497841dc88789d15a422792cf5c1818a72a4ebe7fa9f569a4824ce99f`  
		Last Modified: Thu, 04 Dec 2025 22:34:58 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19ce16735c127991fab0a49081d04170d61fc3b2c60261704ec9247a0edc119f`  
		Last Modified: Thu, 04 Dec 2025 22:35:02 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:6ff6570e2a8fb560a3b830e0f1475d488961b29b93e711d03fd52464844926b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6058459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9360c3d396b9f5081cdc222d176f25b51a35c42c688d1ff1da3ad33a71befeb9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:22 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:19:24 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:21:48 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:21:48 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:21:48 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:21:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:21:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:21:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:21:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:21:49 GMT
USER memcache
# Thu, 04 Dec 2025 19:21:49 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:21:49 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23500700235e36a847f2b35c25e17b359b4cec377d3a0fbafdfff7ec561ecf74`  
		Last Modified: Thu, 04 Dec 2025 19:22:05 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47c608c5e84b70e2288ed6c722d682394718aa7029f3614c85bb3faa2d1a0ab`  
		Last Modified: Thu, 04 Dec 2025 19:22:05 GMT  
		Size: 126.3 KB (126267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251cee6c1abe9d3d9e832748d0edb232d4e43fbbdfc78f3fad887409eff7a658`  
		Last Modified: Thu, 04 Dec 2025 19:22:06 GMT  
		Size: 2.1 MB (2103821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82b7a39ab647b07cb8e684e6fbe6e0c40959b95f23e8b6fba544f6412e08e10`  
		Last Modified: Thu, 04 Dec 2025 19:22:05 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e989166bceb7b8bb922420cfda5d2c1c362b469900fbbd86593fb4422e6f2fb6`  
		Last Modified: Thu, 04 Dec 2025 19:22:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ad7264b3f464d43618d5e997d3c544a46d5d00112555908bab3e31ddfb719fd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da20be024f8583ae82747476a5a8b1054a0d2018ceade3cfcc11e0b460a369e3`

```dockerfile
```

-	Layers:
	-	`sha256:08dd8ac2fb865783b3720303c0b7abe96c0d831dd8dbd89f5ce48f64f5d93577`  
		Last Modified: Thu, 04 Dec 2025 22:35:05 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52998ad89b5d31b02c435f1dabae41e0023686389189f0729699301d2b2dceba`  
		Last Modified: Thu, 04 Dec 2025 22:35:06 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:82618728d34fd5e3c642277cb563310bed5e815337b99361c23d0d4225e3a1ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5793289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95bfdee9049204386f5f9675313ec0cf6437686f3e41ac46a02d7491c4ebd031`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:39 GMT
ADD alpine-minirootfs-3.23.0-riscv64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:39 GMT
CMD ["/bin/sh"]
# Fri, 05 Dec 2025 02:28:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 05 Dec 2025 02:28:43 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 05 Dec 2025 02:42:05 GMT
ENV MEMCACHED_VERSION=1.6.39
# Fri, 05 Dec 2025 02:42:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Fri, 05 Dec 2025 02:42:05 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Fri, 05 Dec 2025 02:42:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 05 Dec 2025 02:42:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Dec 2025 02:42:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Dec 2025 02:42:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Dec 2025 02:42:06 GMT
USER memcache
# Fri, 05 Dec 2025 02:42:06 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Dec 2025 02:42:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9929557817a4c85b33d6dbeb491f7396ef32added7e77de7ac1b644ed0975313`  
		Last Modified: Wed, 03 Dec 2025 19:30:17 GMT  
		Size: 3.6 MB (3583519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04477eae70c2e3cb1bd666913116b231bd91f758fef0ce0487128436edf54e3`  
		Last Modified: Fri, 05 Dec 2025 02:42:36 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27775dcc23cac586ff5717daea95b160d3515a30312e73dc28db55554bcbdd12`  
		Last Modified: Fri, 05 Dec 2025 02:42:37 GMT  
		Size: 108.9 KB (108892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d493e7dad99e12ada2c869111712bae9f61d05aabeb2139df6297985982f119`  
		Last Modified: Fri, 05 Dec 2025 02:42:37 GMT  
		Size: 2.1 MB (2099525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf14d0478c213567d1f2646d01cd27ca8c3db42c197fceb2c2fe55c1ea5bfd84`  
		Last Modified: Fri, 05 Dec 2025 02:42:37 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb60cadd22d3f64cee1f02bcfccb5472502730fea2408ffa893c00d4cae9e97c`  
		Last Modified: Fri, 05 Dec 2025 02:42:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:6607c3431ad2ac598c8476330688ee82114c9b3c0e9b2849f86d95addf5e48eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8406d4978e549630fb362ff2901a3645f7d325e1cce867bbfddade8ceb14232`

```dockerfile
```

-	Layers:
	-	`sha256:5ae6f5f57506c9cba95d087771e8253c7ee7c129dcbc4fdd524a99f4feeafec9`  
		Last Modified: Fri, 05 Dec 2025 04:34:37 GMT  
		Size: 94.3 KB (94276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b9a49d787a1cd02fea8b8affc293bd2d718765b8ef3d8cf26d839f80d072eea`  
		Last Modified: Fri, 05 Dec 2025 04:34:38 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:b23b3b07e717d7651a02ec547a675f198e684f410c7217a09bd305de6c20e664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5878802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e586dd7e72674888df0e6f0ade73d053d2a5a94b7d890a276fb6f13fba7e4cc3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:22 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:19:24 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:22:39 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:22:39 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:22:39 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:22:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:22:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:22:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:22:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:22:39 GMT
USER memcache
# Thu, 04 Dec 2025 19:22:39 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:22:39 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a188510a1e7e85e0e83a71da1abed06b459c07887a679cf331da7789673755`  
		Last Modified: Thu, 04 Dec 2025 19:23:03 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67afe5cdcebd55aec1e59a816853f758650056c83c63ea4d99d6e06e15f60fd`  
		Last Modified: Thu, 04 Dec 2025 19:23:03 GMT  
		Size: 114.3 KB (114286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377a08e6b7dd38664aeee34c52a61b8f7edf9165adabbaee0e0b923423a60242`  
		Last Modified: Thu, 04 Dec 2025 19:23:03 GMT  
		Size: 2.0 MB (2039357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c47067ba1641d8aa2a1f3d7df1e359c1ef226673c5b60eeecc3824f3609e9b`  
		Last Modified: Thu, 04 Dec 2025 19:23:03 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e307cf70f379099e1c944f0972ea3478099fc2221e7ae304d3c47858cb9c8b`  
		Last Modified: Thu, 04 Dec 2025 19:23:03 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:db1f4e6b802cb9b4ee6a404e244522a143516b6c5dfe88d706e7d657e8a3c6c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e21cb3a2b9f702a014eac05118559131c607052ca17bd1adb7ddb02107d291d0`

```dockerfile
```

-	Layers:
	-	`sha256:a484d75866b9f2198dfeccc7d70aa01018c27dd00a8bdad7b47bb8f659ee35d1`  
		Last Modified: Thu, 04 Dec 2025 22:35:09 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e39d44972f86c94e48a8ba761774c90c693cfd7248b9b3fa84a7905217f0c57a`  
		Last Modified: Thu, 04 Dec 2025 22:35:10 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.39-alpine3.23`

```console
$ docker pull memcached@sha256:c8503d4491edd3110cc07d0465089d3a41cf1daf8645e71149e39a51835e92cd
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

### `memcached:1.6.39-alpine3.23` - linux; amd64

```console
$ docker pull memcached@sha256:aac456c35cd29635b5501fefac58a2e954752006c9d159fbf520dd785e09cbba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5973577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6411cdd430a5f0c33aea6496062ab90fbc7da776f1c937108cf51b7a40e090f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:20:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:20:42 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:23:18 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:23:18 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:23:18 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:23:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:23:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:23:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:23:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:23:18 GMT
USER memcache
# Thu, 04 Dec 2025 19:23:18 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:23:18 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e377e19df274e9919dbfbe05b510e54db0f8451ac0985b108aba9123048001d8`  
		Last Modified: Thu, 04 Dec 2025 19:23:54 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0d9328fb6b4452be1f62a5c6db62b8425a6b48c40ce2408ae0f526b101c80c`  
		Last Modified: Thu, 04 Dec 2025 19:23:55 GMT  
		Size: 106.0 KB (106047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a1eb06c51acdaf80ce22a4524ea827613ecc609e23cb0fa481005e89b22d4f`  
		Last Modified: Thu, 04 Dec 2025 19:23:54 GMT  
		Size: 2.0 MB (2006867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4829db5772d5079a1be438e2b4d4921e584e88e6becb7ca1819f33cc6ddd962c`  
		Last Modified: Thu, 04 Dec 2025 19:23:54 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b919142486c25c1941bfb65c0f6f26ff49ed2820b62db8ee149ac5a386bcd76c`  
		Last Modified: Thu, 04 Dec 2025 19:23:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:849b937b30f8457f48d4a2b4dee48812e3f3fef3740e8553fbeb950ef1e6a405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3eb9da9040350a8be21d03f2423ac5b520d62898c8656b204d89a46be87cca`

```dockerfile
```

-	Layers:
	-	`sha256:a6a585b25dcf23d45fe100d658f3fc872a69be33f37f5b142951380b902e1a65`  
		Last Modified: Thu, 04 Dec 2025 22:34:43 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91e8f143d354857f78ae4fd0e5416b79eb34dc3599af1f3df2161a4fa1885af9`  
		Last Modified: Thu, 04 Dec 2025 22:34:44 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine3.23` - linux; arm variant v6

```console
$ docker pull memcached@sha256:a7003e700207ebf4fd102e5d81432129cd3e4776c613ee53fa01b0dbd5e9f19b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5629653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36796824ef2ab4ff08673e2fdd2ff3529a8c6c476c842ec665b90db7e63fad02`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:21:33 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:21:34 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:33:55 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:33:55 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:33:55 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:33:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:33:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:33:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:33:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:33:55 GMT
USER memcache
# Thu, 04 Dec 2025 19:33:55 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:33:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2477fbd5a498e104db4354cbb88ebe3bf7d7f22609c3d9f3996ee3d6f2b311`  
		Last Modified: Thu, 04 Dec 2025 19:34:10 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d610e2e19bb7ad98b2e77e581123187db039c4259f548f8e16e1b5015d0ec85`  
		Last Modified: Thu, 04 Dec 2025 19:34:10 GMT  
		Size: 102.6 KB (102642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5e9f0ad4522a9fedea5ba5229899ef09d25774a89a517cf59cae7a36e4ea92`  
		Last Modified: Thu, 04 Dec 2025 19:34:10 GMT  
		Size: 2.0 MB (1957764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8b426cdf478aef96c3b7780b5b6c81b458a0787358d6251799150a9f714aaf`  
		Last Modified: Thu, 04 Dec 2025 19:34:10 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd456d3218701485ecd1ce99f10c7a08986e44f71d19a49e419582aeb4924f52`  
		Last Modified: Thu, 04 Dec 2025 19:34:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:95ab79e458ab0908467ebbdf5539b688045b04421a068fa6821d557eece2f67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569a816a11d27d030ea4089563f4a23efecb872605941df1c53c0c4152fbd211`

```dockerfile
```

-	Layers:
	-	`sha256:dd9475807057d6ac4c96f526dc77e867efe6bb682d09ef1c7c0557b6f2dad356`  
		Last Modified: Thu, 04 Dec 2025 22:34:47 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine3.23` - linux; arm variant v7

```console
$ docker pull memcached@sha256:6b1fcd05fdcf13d4b7650d85e6043cdeaf423fe9ec57036c0f203e4eef6bff12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5289618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca393e3ead8035915d8cd6bcea0e8ccbe82d8ae05b9cad79126dd93567ff2889`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:43 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:19:44 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:22:37 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:22:37 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:22:37 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:22:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:22:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:22:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:22:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:22:37 GMT
USER memcache
# Thu, 04 Dec 2025 19:22:37 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:22:37 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdc28d0a8cb5092fb181830a0ef7fb2c55b0dcec915fb49171721470a36990e`  
		Last Modified: Thu, 04 Dec 2025 19:22:53 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d64ac2dd6859410fc8786621ad68f29d5cf9799784bd6181fa0fd9b16f10b5`  
		Last Modified: Thu, 04 Dec 2025 19:22:53 GMT  
		Size: 92.4 KB (92376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf39f9a50690d556c95f99315866a17736de133854b3f4a1f01c007e8ea52e8c`  
		Last Modified: Thu, 04 Dec 2025 19:22:53 GMT  
		Size: 1.9 MB (1917424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5adf2295dafdfb5341494ff56dfa3c9fef413e476cc7e0ea0a44ea325856fd40`  
		Last Modified: Thu, 04 Dec 2025 19:22:53 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f68652d871fbfba49b4bdb6f0555e3d086490ac907f630de1960481a50b5982`  
		Last Modified: Thu, 04 Dec 2025 19:22:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:726bec6c0e6bb11f92cf809b0eff6ee10fc86a30eae935ac85e0b82f2fc110d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:489bd5540d03661ecd23b22a8d9070b7dc18f542d91bc1ed60efaa1790080a39`

```dockerfile
```

-	Layers:
	-	`sha256:35def5ffffb77a9cc93b2d806351b5bc638603257621ee3ea2fcab826508b445`  
		Last Modified: Thu, 04 Dec 2025 22:34:50 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b55f58069fda39e67b560d97ac46c79e035b513a560bc8652e5383cd3f82a35`  
		Last Modified: Thu, 04 Dec 2025 22:34:51 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b263323af06e550df9becd8c2cf8450400be7ae4381392593565dc8247bb230f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6304413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:038de42e33564e147549bf3846c2490c168364063ebc7744c8cdd580e202c191`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:20:28 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:20:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:23:16 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:23:16 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:23:16 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:23:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:23:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:23:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:23:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:23:16 GMT
USER memcache
# Thu, 04 Dec 2025 19:23:16 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:23:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4ea1ce2b4c6bdcd3eec4d60b1aa2e3563da544759bff4e7a46469132a86438`  
		Last Modified: Thu, 04 Dec 2025 19:23:27 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc9938ef133bd132ee91a60f23198ae468dca72e6b547301fc4b29e4136bc9e`  
		Last Modified: Thu, 04 Dec 2025 19:23:28 GMT  
		Size: 121.9 KB (121870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fbb7f498823838642f0cbc3dfbcce9ec16c50549649b23872df57076fed9e7`  
		Last Modified: Thu, 04 Dec 2025 19:23:28 GMT  
		Size: 2.0 MB (1985993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341b9a721d462e12012b285eb88cdd865e1fa62f664d8343c3223d3b18b5ed0c`  
		Last Modified: Thu, 04 Dec 2025 19:23:27 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f879a6e1902c8a256d8dea45afd4efc95caa82bd9fcf3291b6730a20d2c5a0`  
		Last Modified: Thu, 04 Dec 2025 19:23:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:9e1d743b77c8856403d4e8420e9936de4aa1bc6fc88642c47112e318e10e2655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556ecd6a50c7ec0f18eea0bb6b6a3c2a30163cdbf6e0a9314ef069819efdb628`

```dockerfile
```

-	Layers:
	-	`sha256:57a22eef052f1e8ba0bdbfa2e165923ea29a9572ab9d397f6652f44a895c34c9`  
		Last Modified: Thu, 04 Dec 2025 22:34:54 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea1714f2bc9b4e6925e95bfc0d324fe4686d662ad257e5959451179599d072e6`  
		Last Modified: Thu, 04 Dec 2025 22:34:55 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine3.23` - linux; 386

```console
$ docker pull memcached@sha256:b3d88ad28118ac190ff8cfd6be5b29a4aff4e4f772124ba8a6cb7335eb909152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5762624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfa1253f0cf9e80c36b723ff6f79bb43b3cb4c3146f4340f605aaf0bb812eaa1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:20:00 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:20:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:22:43 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:22:43 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:22:43 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:22:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:22:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:22:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:22:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:22:43 GMT
USER memcache
# Thu, 04 Dec 2025 19:22:43 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:22:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3527b4f952d5950d8caa74dc0d1759215000f2f0a195344f0239c7e2805fe2fc`  
		Last Modified: Wed, 03 Dec 2025 19:30:41 GMT  
		Size: 3.7 MB (3685856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801e2ef7c6c58c48cfc036b3ffd9de546ffd13f67044c4c296b3624d08852398`  
		Last Modified: Thu, 04 Dec 2025 19:22:57 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7528d81de6e75b8aa074f7b96d6b9f2650422ca25fc0f5485dadf33879a4eb7`  
		Last Modified: Thu, 04 Dec 2025 19:22:57 GMT  
		Size: 110.7 KB (110732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40cb203b33be80dad7c861215d0c69239f729987a3942b71d4fc7b17423658e`  
		Last Modified: Thu, 04 Dec 2025 19:22:58 GMT  
		Size: 2.0 MB (1964688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbaa8273de612bce797fce27339a8adb341655d9b03a120aa874e80bfc438ba`  
		Last Modified: Thu, 04 Dec 2025 19:22:57 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a62b5e894734682a138338f04d49ebcb3e61a322469798019f9737e8ef19b33`  
		Last Modified: Thu, 04 Dec 2025 19:22:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:a8428c10b46dc321be308528a9dc3904db404457e03384a035c6e8c7bf32d05e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c97e68a8fd4c390f7dac3c43eda5f00b0b29eb2b838b877b0926ec7a55ec29`

```dockerfile
```

-	Layers:
	-	`sha256:5414f83497841dc88789d15a422792cf5c1818a72a4ebe7fa9f569a4824ce99f`  
		Last Modified: Thu, 04 Dec 2025 22:34:58 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19ce16735c127991fab0a49081d04170d61fc3b2c60261704ec9247a0edc119f`  
		Last Modified: Thu, 04 Dec 2025 22:35:02 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine3.23` - linux; ppc64le

```console
$ docker pull memcached@sha256:6ff6570e2a8fb560a3b830e0f1475d488961b29b93e711d03fd52464844926b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6058459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9360c3d396b9f5081cdc222d176f25b51a35c42c688d1ff1da3ad33a71befeb9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:22 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:19:24 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:21:48 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:21:48 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:21:48 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:21:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:21:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:21:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:21:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:21:49 GMT
USER memcache
# Thu, 04 Dec 2025 19:21:49 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:21:49 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23500700235e36a847f2b35c25e17b359b4cec377d3a0fbafdfff7ec561ecf74`  
		Last Modified: Thu, 04 Dec 2025 19:22:05 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47c608c5e84b70e2288ed6c722d682394718aa7029f3614c85bb3faa2d1a0ab`  
		Last Modified: Thu, 04 Dec 2025 19:22:05 GMT  
		Size: 126.3 KB (126267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251cee6c1abe9d3d9e832748d0edb232d4e43fbbdfc78f3fad887409eff7a658`  
		Last Modified: Thu, 04 Dec 2025 19:22:06 GMT  
		Size: 2.1 MB (2103821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82b7a39ab647b07cb8e684e6fbe6e0c40959b95f23e8b6fba544f6412e08e10`  
		Last Modified: Thu, 04 Dec 2025 19:22:05 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e989166bceb7b8bb922420cfda5d2c1c362b469900fbbd86593fb4422e6f2fb6`  
		Last Modified: Thu, 04 Dec 2025 19:22:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:ad7264b3f464d43618d5e997d3c544a46d5d00112555908bab3e31ddfb719fd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da20be024f8583ae82747476a5a8b1054a0d2018ceade3cfcc11e0b460a369e3`

```dockerfile
```

-	Layers:
	-	`sha256:08dd8ac2fb865783b3720303c0b7abe96c0d831dd8dbd89f5ce48f64f5d93577`  
		Last Modified: Thu, 04 Dec 2025 22:35:05 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52998ad89b5d31b02c435f1dabae41e0023686389189f0729699301d2b2dceba`  
		Last Modified: Thu, 04 Dec 2025 22:35:06 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine3.23` - linux; riscv64

```console
$ docker pull memcached@sha256:82618728d34fd5e3c642277cb563310bed5e815337b99361c23d0d4225e3a1ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5793289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95bfdee9049204386f5f9675313ec0cf6437686f3e41ac46a02d7491c4ebd031`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:39 GMT
ADD alpine-minirootfs-3.23.0-riscv64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:39 GMT
CMD ["/bin/sh"]
# Fri, 05 Dec 2025 02:28:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 05 Dec 2025 02:28:43 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 05 Dec 2025 02:42:05 GMT
ENV MEMCACHED_VERSION=1.6.39
# Fri, 05 Dec 2025 02:42:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Fri, 05 Dec 2025 02:42:05 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Fri, 05 Dec 2025 02:42:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 05 Dec 2025 02:42:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Dec 2025 02:42:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Dec 2025 02:42:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Dec 2025 02:42:06 GMT
USER memcache
# Fri, 05 Dec 2025 02:42:06 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Dec 2025 02:42:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9929557817a4c85b33d6dbeb491f7396ef32added7e77de7ac1b644ed0975313`  
		Last Modified: Wed, 03 Dec 2025 19:30:17 GMT  
		Size: 3.6 MB (3583519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04477eae70c2e3cb1bd666913116b231bd91f758fef0ce0487128436edf54e3`  
		Last Modified: Fri, 05 Dec 2025 02:42:36 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27775dcc23cac586ff5717daea95b160d3515a30312e73dc28db55554bcbdd12`  
		Last Modified: Fri, 05 Dec 2025 02:42:37 GMT  
		Size: 108.9 KB (108892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d493e7dad99e12ada2c869111712bae9f61d05aabeb2139df6297985982f119`  
		Last Modified: Fri, 05 Dec 2025 02:42:37 GMT  
		Size: 2.1 MB (2099525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf14d0478c213567d1f2646d01cd27ca8c3db42c197fceb2c2fe55c1ea5bfd84`  
		Last Modified: Fri, 05 Dec 2025 02:42:37 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb60cadd22d3f64cee1f02bcfccb5472502730fea2408ffa893c00d4cae9e97c`  
		Last Modified: Fri, 05 Dec 2025 02:42:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:6607c3431ad2ac598c8476330688ee82114c9b3c0e9b2849f86d95addf5e48eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8406d4978e549630fb362ff2901a3645f7d325e1cce867bbfddade8ceb14232`

```dockerfile
```

-	Layers:
	-	`sha256:5ae6f5f57506c9cba95d087771e8253c7ee7c129dcbc4fdd524a99f4feeafec9`  
		Last Modified: Fri, 05 Dec 2025 04:34:37 GMT  
		Size: 94.3 KB (94276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b9a49d787a1cd02fea8b8affc293bd2d718765b8ef3d8cf26d839f80d072eea`  
		Last Modified: Fri, 05 Dec 2025 04:34:38 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine3.23` - linux; s390x

```console
$ docker pull memcached@sha256:b23b3b07e717d7651a02ec547a675f198e684f410c7217a09bd305de6c20e664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5878802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e586dd7e72674888df0e6f0ade73d053d2a5a94b7d890a276fb6f13fba7e4cc3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:22 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:19:24 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:22:39 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:22:39 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:22:39 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:22:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:22:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:22:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:22:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:22:39 GMT
USER memcache
# Thu, 04 Dec 2025 19:22:39 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:22:39 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a188510a1e7e85e0e83a71da1abed06b459c07887a679cf331da7789673755`  
		Last Modified: Thu, 04 Dec 2025 19:23:03 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67afe5cdcebd55aec1e59a816853f758650056c83c63ea4d99d6e06e15f60fd`  
		Last Modified: Thu, 04 Dec 2025 19:23:03 GMT  
		Size: 114.3 KB (114286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377a08e6b7dd38664aeee34c52a61b8f7edf9165adabbaee0e0b923423a60242`  
		Last Modified: Thu, 04 Dec 2025 19:23:03 GMT  
		Size: 2.0 MB (2039357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c47067ba1641d8aa2a1f3d7df1e359c1ef226673c5b60eeecc3824f3609e9b`  
		Last Modified: Thu, 04 Dec 2025 19:23:03 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e307cf70f379099e1c944f0972ea3478099fc2221e7ae304d3c47858cb9c8b`  
		Last Modified: Thu, 04 Dec 2025 19:23:03 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:db1f4e6b802cb9b4ee6a404e244522a143516b6c5dfe88d706e7d657e8a3c6c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e21cb3a2b9f702a014eac05118559131c607052ca17bd1adb7ddb02107d291d0`

```dockerfile
```

-	Layers:
	-	`sha256:a484d75866b9f2198dfeccc7d70aa01018c27dd00a8bdad7b47bb8f659ee35d1`  
		Last Modified: Thu, 04 Dec 2025 22:35:09 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e39d44972f86c94e48a8ba761774c90c693cfd7248b9b3fa84a7905217f0c57a`  
		Last Modified: Thu, 04 Dec 2025 22:35:10 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.39-trixie`

```console
$ docker pull memcached@sha256:c7628370ae681c42dbd48ccf02320d77a2bc0234f9ba3a968b5da3a7c0112469
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:1.6.39-trixie` - linux; amd64

```console
$ docker pull memcached@sha256:153e4ed762fd3bc07fe607f64631647939278d6101759d91fac0b756cceb2272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32208551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa0c800d7278560e11e4d0f14defc4d2d850224d0859d1bd0e9205cc962478d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:38:46 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:38:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:41:30 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:41:30 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:41:30 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:41:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:41:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:41:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:41:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:41:30 GMT
USER memcache
# Mon, 08 Dec 2025 22:41:30 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:41:30 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e33b5452dc8ba5d42cd13b42745898ef870af3e8d5a65b06b8b174f06b1d50`  
		Last Modified: Mon, 08 Dec 2025 22:41:43 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce4ec629da8029212ce5d775073648d04f1f014a89e49f73f1fc848bc405dd5`  
		Last Modified: Mon, 08 Dec 2025 22:41:43 GMT  
		Size: 136.7 KB (136697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6210dfd46759cbe6922de2db75ddf6d17c1f033a434ee6bcf2e82d56ce59f449`  
		Last Modified: Mon, 08 Dec 2025 22:41:43 GMT  
		Size: 2.3 MB (2293845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffbb5d472cb4680299753b978d2e8eeb6d2288ee4caec01e65541f4358516a6`  
		Last Modified: Mon, 08 Dec 2025 22:41:43 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e474cc606bdb91c69d2f124d38e5ebd93ed9ab64d219ab51845cc238a5904aa`  
		Last Modified: Mon, 08 Dec 2025 22:41:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:45cb4f875b600a26ef6e0388db256b09a14580b17ddcaa485fd2c25cbff56056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6483c69793152c682b93375229933004781cbf7df7f059d288d2d7e04335b2c8`

```dockerfile
```

-	Layers:
	-	`sha256:c3beab005b14cd0614637cc43c84460edfb07d9c68b1138ee676ab5bd3dc05ac`  
		Last Modified: Tue, 09 Dec 2025 01:34:56 GMT  
		Size: 2.0 MB (2008228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6ce8cbbfb878c257688fdf1d5e1a9c428b68061ee92f8e07a240ab0fe4b812e`  
		Last Modified: Tue, 09 Dec 2025 01:34:57 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:5a7b1183ed0a0ca89ce3d88e335fca2672422eee8d05921621cd4ed617965ed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30317206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1552234329fddb68f43cfe1abdf3dff1b1499edbb12eb6d84c481f3d7fbe2c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:34:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:37:32 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:37:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:37:32 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:37:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:37:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:37:32 GMT
USER memcache
# Mon, 08 Dec 2025 22:37:32 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:37:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d97bc71d0fa535127863fdab265dfddb07b3cda35b80de4dd2b9b67fe154c856`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 27.9 MB (27944187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d0d6688f3764bd09c70b0fdb00a12bc517f76c47fc187448da8cf7958b4b98`  
		Last Modified: Mon, 08 Dec 2025 22:37:44 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1a7c3cdaa260d51a1e04177297af5b7e205abe78e98f0782c38369f1a49034`  
		Last Modified: Mon, 08 Dec 2025 22:37:45 GMT  
		Size: 144.1 KB (144146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e35266d4886f5160ecccf89b51e0317cf6c7ad5a063a40d74c0dd0baa75b974`  
		Last Modified: Mon, 08 Dec 2025 22:37:45 GMT  
		Size: 2.2 MB (2227364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3324af035e2f7b73ce2f8c3d5ee46e80ed9063e2ae219caf112d6bafe3d935a3`  
		Last Modified: Mon, 08 Dec 2025 22:37:44 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae7d716f59ff9d69d00b890308b431e236e3a1d530f0dfa1ccaabdd01ea7df2`  
		Last Modified: Mon, 08 Dec 2025 22:37:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:077fa23fa7fd08a421aff7ec84a802bb72f53e3f31c9fb2bba4df39b99ae3923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92bd65e20c21649e0ebcbd5810944fd9e43ecf788ec1d580bfc3c04722bf6fa4`

```dockerfile
```

-	Layers:
	-	`sha256:02c0b341ef4c59b9ffa7a8de46289cbd08d3a3b029c0a64224da804b55e2e854`  
		Last Modified: Tue, 09 Dec 2025 01:35:01 GMT  
		Size: 2.0 MB (2011231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb1ede44c11856b6e3f7c4f6ba238d3df5677af459242c47b9f24b4a1c184db0`  
		Last Modified: Tue, 09 Dec 2025 01:35:02 GMT  
		Size: 22.3 KB (22302 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:cb9b94d371b2da6a520b577dd688b99c959dac8ad5e81f17aaf8e5b6ed1968ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28529520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a8988937956147836c267576a47663f836997a1d6a21750c17c7d2e52982c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:38:02 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:38:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:41:09 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:41:09 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:41:09 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:41:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:41:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:41:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:41:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:41:09 GMT
USER memcache
# Mon, 08 Dec 2025 22:41:09 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:41:09 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15599337d37fa53f93b66130266f60f942cc7c2c4e2e8458c672f9b61b921350`  
		Last Modified: Mon, 08 Dec 2025 22:41:22 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4e148e811da2c8aeb3f52da0f7e137c9e2dbf7e07ea25ed2a8ec2bc3db340d`  
		Last Modified: Mon, 08 Dec 2025 22:41:25 GMT  
		Size: 135.4 KB (135363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248d1bdc7fd809ba8d6d01e877ae1ff16258cd1b26203215342935af2305c133`  
		Last Modified: Mon, 08 Dec 2025 22:41:22 GMT  
		Size: 2.2 MB (2182634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4dca52427f97b68739a35240dde721713ae992674b8f6fe50fc71d987512c4`  
		Last Modified: Mon, 08 Dec 2025 22:41:22 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2961ef381f352090fe3d59e2ff32ae5c2979defa070a22f5fc846bb2b5f0f30`  
		Last Modified: Mon, 08 Dec 2025 22:41:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:cff996fea1034ca7a74465fdf5489ef45c78f70859319df22468100dc3c84e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e8d92fa13df244234c51ab1b93e9a4c39ad977f40dd5b49cef4e8ed0de7e3a`

```dockerfile
```

-	Layers:
	-	`sha256:d08663eef9d4f14b4b344cf2d8924f04dee694d602df55d600a90830f505069b`  
		Last Modified: Tue, 09 Dec 2025 01:35:06 GMT  
		Size: 2.0 MB (2009688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb1b323cef393d68691ca1f808424d4c4ca9aa868a63329889d55c9e53c30671`  
		Last Modified: Tue, 09 Dec 2025 01:35:06 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:6230125fff57e6f22504aae8db1ed049b738d97c3e325a68a9733a186fab61e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32568877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2f55b9564478802d59f2ab50cadac0b6e11704297ea84bc7fdcc4e9fb3ba76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:38:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:38:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:41:20 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:41:20 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:41:20 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:41:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:41:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:41:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:41:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:41:20 GMT
USER memcache
# Mon, 08 Dec 2025 22:41:20 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:41:20 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91cd2e642e1c9b79606d81fe7ae3f5599c2e1a2ebb80864a1c25f4771502b02`  
		Last Modified: Mon, 08 Dec 2025 22:41:32 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9b5941656d039525e2c86c6dad7b225e0dfe8a89bda1c33c46f84b7e1f05f0`  
		Last Modified: Mon, 08 Dec 2025 22:41:32 GMT  
		Size: 153.5 KB (153454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc829d43c3195e76b119f7ef9e8519d7c64f130e104b29b5317d18e709d3796`  
		Last Modified: Mon, 08 Dec 2025 22:41:32 GMT  
		Size: 2.3 MB (2275286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685e3db2e1ea7f3a85650a5cac398166f6fe54b1767d8ab65fd070fc9f08f903`  
		Last Modified: Mon, 08 Dec 2025 22:41:32 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bedd2011ff5fea2608113c25dac443f7f67fd30b9f049d14304a5eeba342453`  
		Last Modified: Mon, 08 Dec 2025 22:41:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:5be232fd0ce753823a0a00a2e155ca7ed374028d0a228270604974765be63286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ad988781bd90f9b424c8530a983604f0dea5e9ff5d39be9ca322ea793f7044`

```dockerfile
```

-	Layers:
	-	`sha256:2f225cf8fe800d6f4631961cb099b7f796ad28fbe325df7943d5fd182391187f`  
		Last Modified: Tue, 09 Dec 2025 01:35:10 GMT  
		Size: 2.0 MB (2008544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd6800d8108ddffdecd1e6d030f8948b6ed22cff74e19779380d731dfd189d0d`  
		Last Modified: Tue, 09 Dec 2025 01:35:11 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-trixie` - linux; 386

```console
$ docker pull memcached@sha256:9c8dd1c0a7d71ffb9540bcdac40c6c72661b05ad12d1a0dcacb86ba0dad353b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33686582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a221f2cf3f75cb38b8be293e0d315a4453967306dc401835f3732a7ec18482d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:17 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:33:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:36:13 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:36:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:36:13 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:36:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:36:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:36:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:36:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:36:13 GMT
USER memcache
# Mon, 08 Dec 2025 22:36:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:36:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c63a49351bc91fd837d81e97ce862507215607bc756f1133f1d887e94e1cc4e`  
		Last Modified: Mon, 08 Dec 2025 22:36:26 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7073e103108a28c5e5a1458be46ac8c708375f2b4327423a59471a77bbf2c0c6`  
		Last Modified: Mon, 08 Dec 2025 22:36:26 GMT  
		Size: 147.5 KB (147516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbfa39b86ad2206ef2fdf5ec3f3a55aa40c422a9f3fca094c7c2f003e7d4a63`  
		Last Modified: Mon, 08 Dec 2025 22:36:26 GMT  
		Size: 2.2 MB (2244483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1ade71ea049e11fc9cea7c16944632ffd753dfe7130e3bb4e1730281daffb5`  
		Last Modified: Mon, 08 Dec 2025 22:36:26 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5eb870312490559d775f9d994ba10b9fcae44c680e23a647a43c1c55f49b54`  
		Last Modified: Mon, 08 Dec 2025 22:36:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:e5ea0a4780f0574f775d4cf8c4ffff6f6b836e33d54d6d241047fa36e54d70b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1425c202287fb1c6f81bb3962bb416b9f23b14b12da6119772ac599ae7af4b`

```dockerfile
```

-	Layers:
	-	`sha256:9d6ed296b190f0f66c6f54ffafa76bd9f86d72e2a463ed9841c2654abf7282d0`  
		Last Modified: Tue, 09 Dec 2025 01:35:16 GMT  
		Size: 2.0 MB (2005385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d9f28b39486b665dcd60f89a225a5fce2e4060feaed50b57eaf89bc54345129`  
		Last Modified: Tue, 09 Dec 2025 01:35:17 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:9a5a8c51d01a2dde31ee88dc7739b61aad1cd244c1592033d64b89e71ea9d086
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36185779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62a722a142df5369183f571c8eecacbc8041e72fb89888b569e2e558947291b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:32:15 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 09 Dec 2025 00:32:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:35:25 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 09 Dec 2025 00:35:25 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 09 Dec 2025 00:35:25 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 09 Dec 2025 00:35:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 09 Dec 2025 00:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 00:35:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 09 Dec 2025 00:35:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Dec 2025 00:35:26 GMT
USER memcache
# Tue, 09 Dec 2025 00:35:26 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 09 Dec 2025 00:35:26 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca80ecfb634d24079bf04d5695260ea9dce9f468064fb83123a71959d22b7c4`  
		Last Modified: Tue, 09 Dec 2025 00:35:51 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb90fb01769b3666ac21d77bcba16bd54161463250fa6f304710eb00d5ab5411`  
		Last Modified: Tue, 09 Dec 2025 00:35:51 GMT  
		Size: 170.4 KB (170375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be675ba49db497b747d37543689ff0b8fc0ef4398cd718c2fadd28302d88141b`  
		Last Modified: Tue, 09 Dec 2025 00:35:51 GMT  
		Size: 2.4 MB (2417005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882b9516d2a74a32203b37778b6025dc9c68a30838e1fa420559c34fe0319141`  
		Last Modified: Tue, 09 Dec 2025 00:35:51 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5cfa5b161387b536b9f8a94f199ffd006893e19e7bff82a8f1f9a7aa578a73`  
		Last Modified: Tue, 09 Dec 2025 00:35:51 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:6ea51b9da9219f68c45e3345bed106b961bce70b2c9aecbb6e1300060e04217d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f87eac26bbbb68ef23dfd63867d0415ddc04fe2567863569701f2891733279d6`

```dockerfile
```

-	Layers:
	-	`sha256:6f8bb9e427f03eea07711eb22a22462b3548d9ed3bf7b82f412aea5a623b10ff`  
		Last Modified: Tue, 09 Dec 2025 04:34:42 GMT  
		Size: 2.0 MB (2011829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1705de570678d9ecda7c8bb1da82748111d8547fb22bfbfb43fbbf41808b5b67`  
		Last Modified: Tue, 09 Dec 2025 04:34:43 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:05d76bdff41209572f5e6c4d21717d0717a794340a2bc2c086af7a863f5c19af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30627687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c785d7526540c98189bc45e1c3ad5a9862a6ed744c2b49e94165199ba9dcd7ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 10:11:36 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 10:12:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 10:53:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 10:53:11 GMT
USER memcache
# Tue, 18 Nov 2025 10:53:11 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 10:53:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f7062dea9fa0a796a2eacb7b265e4b2000be3d07bc91c20a5abc6538e5a68c`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f8a04356a93113399cb041ac377cf221db2df7d9fc3a6d630a061a923eb1e6`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 133.1 KB (133088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4bbee7a68150daca8b6b94e26e1a04551afc5a77dfb08a4e04aadc0933c456`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 2.2 MB (2219954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085465091dfa79c5f79dd2c74f56f75a8e078b89272039f8d8ed5a1d2adac41b`  
		Last Modified: Tue, 18 Nov 2025 10:54:06 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea3aae46e46f60ca268fd3c445c8b9ed827d7daba7e6d611310cfc9dc4d5291`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:7a8af6c2848585e79b5cb65b6a760b1f78f0de3a59fb604d7a026c79f05a77b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c73002e7361572816b1c22cbb73aced8ce908f6492f2b5d15371b7c0a0514546`

```dockerfile
```

-	Layers:
	-	`sha256:059e3337eaf5c7461d584e0f4b5c7c660bf41a1bb79e90aa917a3992eba4c855`  
		Last Modified: Tue, 18 Nov 2025 16:35:44 GMT  
		Size: 2.0 MB (2002192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cf39200d9e698624fc7d7abe914cab80bda5407ae30f111eb22846e8fd28bba`  
		Last Modified: Tue, 18 Nov 2025 16:35:45 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:332c41cfc207814782dda23a2b840d653abb751f335f7f02f6b238ce79c1c08c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32290312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2be68b3a60f2d8e906983e133fcaffe03bd1a82c9acc69a3dcbe3e307d7b8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:21 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:33:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:36:33 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:36:33 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:36:33 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:36:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:36:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:36:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:36:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:36:34 GMT
USER memcache
# Mon, 08 Dec 2025 22:36:34 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:36:34 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc040aa39039515a9f8b38dc90047178bd8fa0d8234856954f045f05050e52c`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e235f00f3da465d44b7ac18782958812c19e974f091dedfc097442ba632a3d`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 140.5 KB (140505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284c7cc2b7cc68de54eb5bce5de02ed5229cb403476e794b8066eee16babb6e1`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 2.3 MB (2313897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5059135976f7ec26a104b2fb6340b0ae8adc5756ea159deede93c8532613fd24`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd63939e0e5898afa1d51d59354c263e9a7ebfba3e418395baf21445315251de`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:8a7be7ae9cfd628f1585c887ce286f74e97f7780cc20009ffe07f9c92623b34c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c6fbc39d1b80ba4ed6852329a8ddfcaaeed5500129f5019fbc5a8904a7cd659`

```dockerfile
```

-	Layers:
	-	`sha256:0a66a7a3c4891f559fc098f2c13e48d32804e22f559857d3c89074b829300c25`  
		Last Modified: Tue, 09 Dec 2025 01:35:26 GMT  
		Size: 2.0 MB (2009665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24d3a4bbcde50a51a341ad980cc2d92d652ec5f9394c80d55c8a70ded47d8927`  
		Last Modified: Tue, 09 Dec 2025 01:35:27 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine`

```console
$ docker pull memcached@sha256:c8503d4491edd3110cc07d0465089d3a41cf1daf8645e71149e39a51835e92cd
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
$ docker pull memcached@sha256:aac456c35cd29635b5501fefac58a2e954752006c9d159fbf520dd785e09cbba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5973577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6411cdd430a5f0c33aea6496062ab90fbc7da776f1c937108cf51b7a40e090f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:20:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:20:42 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:23:18 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:23:18 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:23:18 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:23:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:23:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:23:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:23:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:23:18 GMT
USER memcache
# Thu, 04 Dec 2025 19:23:18 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:23:18 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e377e19df274e9919dbfbe05b510e54db0f8451ac0985b108aba9123048001d8`  
		Last Modified: Thu, 04 Dec 2025 19:23:54 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0d9328fb6b4452be1f62a5c6db62b8425a6b48c40ce2408ae0f526b101c80c`  
		Last Modified: Thu, 04 Dec 2025 19:23:55 GMT  
		Size: 106.0 KB (106047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a1eb06c51acdaf80ce22a4524ea827613ecc609e23cb0fa481005e89b22d4f`  
		Last Modified: Thu, 04 Dec 2025 19:23:54 GMT  
		Size: 2.0 MB (2006867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4829db5772d5079a1be438e2b4d4921e584e88e6becb7ca1819f33cc6ddd962c`  
		Last Modified: Thu, 04 Dec 2025 19:23:54 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b919142486c25c1941bfb65c0f6f26ff49ed2820b62db8ee149ac5a386bcd76c`  
		Last Modified: Thu, 04 Dec 2025 19:23:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:849b937b30f8457f48d4a2b4dee48812e3f3fef3740e8553fbeb950ef1e6a405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3eb9da9040350a8be21d03f2423ac5b520d62898c8656b204d89a46be87cca`

```dockerfile
```

-	Layers:
	-	`sha256:a6a585b25dcf23d45fe100d658f3fc872a69be33f37f5b142951380b902e1a65`  
		Last Modified: Thu, 04 Dec 2025 22:34:43 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91e8f143d354857f78ae4fd0e5416b79eb34dc3599af1f3df2161a4fa1885af9`  
		Last Modified: Thu, 04 Dec 2025 22:34:44 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:a7003e700207ebf4fd102e5d81432129cd3e4776c613ee53fa01b0dbd5e9f19b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5629653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36796824ef2ab4ff08673e2fdd2ff3529a8c6c476c842ec665b90db7e63fad02`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:21:33 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:21:34 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:33:55 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:33:55 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:33:55 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:33:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:33:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:33:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:33:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:33:55 GMT
USER memcache
# Thu, 04 Dec 2025 19:33:55 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:33:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2477fbd5a498e104db4354cbb88ebe3bf7d7f22609c3d9f3996ee3d6f2b311`  
		Last Modified: Thu, 04 Dec 2025 19:34:10 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d610e2e19bb7ad98b2e77e581123187db039c4259f548f8e16e1b5015d0ec85`  
		Last Modified: Thu, 04 Dec 2025 19:34:10 GMT  
		Size: 102.6 KB (102642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5e9f0ad4522a9fedea5ba5229899ef09d25774a89a517cf59cae7a36e4ea92`  
		Last Modified: Thu, 04 Dec 2025 19:34:10 GMT  
		Size: 2.0 MB (1957764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8b426cdf478aef96c3b7780b5b6c81b458a0787358d6251799150a9f714aaf`  
		Last Modified: Thu, 04 Dec 2025 19:34:10 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd456d3218701485ecd1ce99f10c7a08986e44f71d19a49e419582aeb4924f52`  
		Last Modified: Thu, 04 Dec 2025 19:34:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:95ab79e458ab0908467ebbdf5539b688045b04421a068fa6821d557eece2f67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569a816a11d27d030ea4089563f4a23efecb872605941df1c53c0c4152fbd211`

```dockerfile
```

-	Layers:
	-	`sha256:dd9475807057d6ac4c96f526dc77e867efe6bb682d09ef1c7c0557b6f2dad356`  
		Last Modified: Thu, 04 Dec 2025 22:34:47 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:6b1fcd05fdcf13d4b7650d85e6043cdeaf423fe9ec57036c0f203e4eef6bff12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5289618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca393e3ead8035915d8cd6bcea0e8ccbe82d8ae05b9cad79126dd93567ff2889`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:43 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:19:44 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:22:37 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:22:37 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:22:37 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:22:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:22:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:22:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:22:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:22:37 GMT
USER memcache
# Thu, 04 Dec 2025 19:22:37 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:22:37 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdc28d0a8cb5092fb181830a0ef7fb2c55b0dcec915fb49171721470a36990e`  
		Last Modified: Thu, 04 Dec 2025 19:22:53 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d64ac2dd6859410fc8786621ad68f29d5cf9799784bd6181fa0fd9b16f10b5`  
		Last Modified: Thu, 04 Dec 2025 19:22:53 GMT  
		Size: 92.4 KB (92376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf39f9a50690d556c95f99315866a17736de133854b3f4a1f01c007e8ea52e8c`  
		Last Modified: Thu, 04 Dec 2025 19:22:53 GMT  
		Size: 1.9 MB (1917424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5adf2295dafdfb5341494ff56dfa3c9fef413e476cc7e0ea0a44ea325856fd40`  
		Last Modified: Thu, 04 Dec 2025 19:22:53 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f68652d871fbfba49b4bdb6f0555e3d086490ac907f630de1960481a50b5982`  
		Last Modified: Thu, 04 Dec 2025 19:22:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:726bec6c0e6bb11f92cf809b0eff6ee10fc86a30eae935ac85e0b82f2fc110d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:489bd5540d03661ecd23b22a8d9070b7dc18f542d91bc1ed60efaa1790080a39`

```dockerfile
```

-	Layers:
	-	`sha256:35def5ffffb77a9cc93b2d806351b5bc638603257621ee3ea2fcab826508b445`  
		Last Modified: Thu, 04 Dec 2025 22:34:50 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b55f58069fda39e67b560d97ac46c79e035b513a560bc8652e5383cd3f82a35`  
		Last Modified: Thu, 04 Dec 2025 22:34:51 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b263323af06e550df9becd8c2cf8450400be7ae4381392593565dc8247bb230f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6304413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:038de42e33564e147549bf3846c2490c168364063ebc7744c8cdd580e202c191`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:20:28 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:20:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:23:16 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:23:16 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:23:16 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:23:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:23:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:23:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:23:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:23:16 GMT
USER memcache
# Thu, 04 Dec 2025 19:23:16 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:23:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4ea1ce2b4c6bdcd3eec4d60b1aa2e3563da544759bff4e7a46469132a86438`  
		Last Modified: Thu, 04 Dec 2025 19:23:27 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc9938ef133bd132ee91a60f23198ae468dca72e6b547301fc4b29e4136bc9e`  
		Last Modified: Thu, 04 Dec 2025 19:23:28 GMT  
		Size: 121.9 KB (121870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fbb7f498823838642f0cbc3dfbcce9ec16c50549649b23872df57076fed9e7`  
		Last Modified: Thu, 04 Dec 2025 19:23:28 GMT  
		Size: 2.0 MB (1985993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341b9a721d462e12012b285eb88cdd865e1fa62f664d8343c3223d3b18b5ed0c`  
		Last Modified: Thu, 04 Dec 2025 19:23:27 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f879a6e1902c8a256d8dea45afd4efc95caa82bd9fcf3291b6730a20d2c5a0`  
		Last Modified: Thu, 04 Dec 2025 19:23:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9e1d743b77c8856403d4e8420e9936de4aa1bc6fc88642c47112e318e10e2655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556ecd6a50c7ec0f18eea0bb6b6a3c2a30163cdbf6e0a9314ef069819efdb628`

```dockerfile
```

-	Layers:
	-	`sha256:57a22eef052f1e8ba0bdbfa2e165923ea29a9572ab9d397f6652f44a895c34c9`  
		Last Modified: Thu, 04 Dec 2025 22:34:54 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea1714f2bc9b4e6925e95bfc0d324fe4686d662ad257e5959451179599d072e6`  
		Last Modified: Thu, 04 Dec 2025 22:34:55 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:b3d88ad28118ac190ff8cfd6be5b29a4aff4e4f772124ba8a6cb7335eb909152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5762624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfa1253f0cf9e80c36b723ff6f79bb43b3cb4c3146f4340f605aaf0bb812eaa1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:20:00 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:20:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:22:43 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:22:43 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:22:43 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:22:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:22:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:22:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:22:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:22:43 GMT
USER memcache
# Thu, 04 Dec 2025 19:22:43 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:22:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3527b4f952d5950d8caa74dc0d1759215000f2f0a195344f0239c7e2805fe2fc`  
		Last Modified: Wed, 03 Dec 2025 19:30:41 GMT  
		Size: 3.7 MB (3685856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801e2ef7c6c58c48cfc036b3ffd9de546ffd13f67044c4c296b3624d08852398`  
		Last Modified: Thu, 04 Dec 2025 19:22:57 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7528d81de6e75b8aa074f7b96d6b9f2650422ca25fc0f5485dadf33879a4eb7`  
		Last Modified: Thu, 04 Dec 2025 19:22:57 GMT  
		Size: 110.7 KB (110732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40cb203b33be80dad7c861215d0c69239f729987a3942b71d4fc7b17423658e`  
		Last Modified: Thu, 04 Dec 2025 19:22:58 GMT  
		Size: 2.0 MB (1964688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbaa8273de612bce797fce27339a8adb341655d9b03a120aa874e80bfc438ba`  
		Last Modified: Thu, 04 Dec 2025 19:22:57 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a62b5e894734682a138338f04d49ebcb3e61a322469798019f9737e8ef19b33`  
		Last Modified: Thu, 04 Dec 2025 19:22:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:a8428c10b46dc321be308528a9dc3904db404457e03384a035c6e8c7bf32d05e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c97e68a8fd4c390f7dac3c43eda5f00b0b29eb2b838b877b0926ec7a55ec29`

```dockerfile
```

-	Layers:
	-	`sha256:5414f83497841dc88789d15a422792cf5c1818a72a4ebe7fa9f569a4824ce99f`  
		Last Modified: Thu, 04 Dec 2025 22:34:58 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19ce16735c127991fab0a49081d04170d61fc3b2c60261704ec9247a0edc119f`  
		Last Modified: Thu, 04 Dec 2025 22:35:02 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:6ff6570e2a8fb560a3b830e0f1475d488961b29b93e711d03fd52464844926b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6058459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9360c3d396b9f5081cdc222d176f25b51a35c42c688d1ff1da3ad33a71befeb9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:22 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:19:24 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:21:48 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:21:48 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:21:48 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:21:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:21:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:21:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:21:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:21:49 GMT
USER memcache
# Thu, 04 Dec 2025 19:21:49 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:21:49 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23500700235e36a847f2b35c25e17b359b4cec377d3a0fbafdfff7ec561ecf74`  
		Last Modified: Thu, 04 Dec 2025 19:22:05 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47c608c5e84b70e2288ed6c722d682394718aa7029f3614c85bb3faa2d1a0ab`  
		Last Modified: Thu, 04 Dec 2025 19:22:05 GMT  
		Size: 126.3 KB (126267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251cee6c1abe9d3d9e832748d0edb232d4e43fbbdfc78f3fad887409eff7a658`  
		Last Modified: Thu, 04 Dec 2025 19:22:06 GMT  
		Size: 2.1 MB (2103821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82b7a39ab647b07cb8e684e6fbe6e0c40959b95f23e8b6fba544f6412e08e10`  
		Last Modified: Thu, 04 Dec 2025 19:22:05 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e989166bceb7b8bb922420cfda5d2c1c362b469900fbbd86593fb4422e6f2fb6`  
		Last Modified: Thu, 04 Dec 2025 19:22:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ad7264b3f464d43618d5e997d3c544a46d5d00112555908bab3e31ddfb719fd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da20be024f8583ae82747476a5a8b1054a0d2018ceade3cfcc11e0b460a369e3`

```dockerfile
```

-	Layers:
	-	`sha256:08dd8ac2fb865783b3720303c0b7abe96c0d831dd8dbd89f5ce48f64f5d93577`  
		Last Modified: Thu, 04 Dec 2025 22:35:05 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52998ad89b5d31b02c435f1dabae41e0023686389189f0729699301d2b2dceba`  
		Last Modified: Thu, 04 Dec 2025 22:35:06 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:82618728d34fd5e3c642277cb563310bed5e815337b99361c23d0d4225e3a1ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5793289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95bfdee9049204386f5f9675313ec0cf6437686f3e41ac46a02d7491c4ebd031`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:39 GMT
ADD alpine-minirootfs-3.23.0-riscv64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:39 GMT
CMD ["/bin/sh"]
# Fri, 05 Dec 2025 02:28:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 05 Dec 2025 02:28:43 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 05 Dec 2025 02:42:05 GMT
ENV MEMCACHED_VERSION=1.6.39
# Fri, 05 Dec 2025 02:42:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Fri, 05 Dec 2025 02:42:05 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Fri, 05 Dec 2025 02:42:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 05 Dec 2025 02:42:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Dec 2025 02:42:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Dec 2025 02:42:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Dec 2025 02:42:06 GMT
USER memcache
# Fri, 05 Dec 2025 02:42:06 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Dec 2025 02:42:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9929557817a4c85b33d6dbeb491f7396ef32added7e77de7ac1b644ed0975313`  
		Last Modified: Wed, 03 Dec 2025 19:30:17 GMT  
		Size: 3.6 MB (3583519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04477eae70c2e3cb1bd666913116b231bd91f758fef0ce0487128436edf54e3`  
		Last Modified: Fri, 05 Dec 2025 02:42:36 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27775dcc23cac586ff5717daea95b160d3515a30312e73dc28db55554bcbdd12`  
		Last Modified: Fri, 05 Dec 2025 02:42:37 GMT  
		Size: 108.9 KB (108892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d493e7dad99e12ada2c869111712bae9f61d05aabeb2139df6297985982f119`  
		Last Modified: Fri, 05 Dec 2025 02:42:37 GMT  
		Size: 2.1 MB (2099525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf14d0478c213567d1f2646d01cd27ca8c3db42c197fceb2c2fe55c1ea5bfd84`  
		Last Modified: Fri, 05 Dec 2025 02:42:37 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb60cadd22d3f64cee1f02bcfccb5472502730fea2408ffa893c00d4cae9e97c`  
		Last Modified: Fri, 05 Dec 2025 02:42:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:6607c3431ad2ac598c8476330688ee82114c9b3c0e9b2849f86d95addf5e48eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8406d4978e549630fb362ff2901a3645f7d325e1cce867bbfddade8ceb14232`

```dockerfile
```

-	Layers:
	-	`sha256:5ae6f5f57506c9cba95d087771e8253c7ee7c129dcbc4fdd524a99f4feeafec9`  
		Last Modified: Fri, 05 Dec 2025 04:34:37 GMT  
		Size: 94.3 KB (94276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b9a49d787a1cd02fea8b8affc293bd2d718765b8ef3d8cf26d839f80d072eea`  
		Last Modified: Fri, 05 Dec 2025 04:34:38 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; s390x

```console
$ docker pull memcached@sha256:b23b3b07e717d7651a02ec547a675f198e684f410c7217a09bd305de6c20e664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5878802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e586dd7e72674888df0e6f0ade73d053d2a5a94b7d890a276fb6f13fba7e4cc3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:22 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:19:24 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:22:39 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:22:39 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:22:39 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:22:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:22:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:22:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:22:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:22:39 GMT
USER memcache
# Thu, 04 Dec 2025 19:22:39 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:22:39 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a188510a1e7e85e0e83a71da1abed06b459c07887a679cf331da7789673755`  
		Last Modified: Thu, 04 Dec 2025 19:23:03 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67afe5cdcebd55aec1e59a816853f758650056c83c63ea4d99d6e06e15f60fd`  
		Last Modified: Thu, 04 Dec 2025 19:23:03 GMT  
		Size: 114.3 KB (114286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377a08e6b7dd38664aeee34c52a61b8f7edf9165adabbaee0e0b923423a60242`  
		Last Modified: Thu, 04 Dec 2025 19:23:03 GMT  
		Size: 2.0 MB (2039357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c47067ba1641d8aa2a1f3d7df1e359c1ef226673c5b60eeecc3824f3609e9b`  
		Last Modified: Thu, 04 Dec 2025 19:23:03 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e307cf70f379099e1c944f0972ea3478099fc2221e7ae304d3c47858cb9c8b`  
		Last Modified: Thu, 04 Dec 2025 19:23:03 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:db1f4e6b802cb9b4ee6a404e244522a143516b6c5dfe88d706e7d657e8a3c6c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e21cb3a2b9f702a014eac05118559131c607052ca17bd1adb7ddb02107d291d0`

```dockerfile
```

-	Layers:
	-	`sha256:a484d75866b9f2198dfeccc7d70aa01018c27dd00a8bdad7b47bb8f659ee35d1`  
		Last Modified: Thu, 04 Dec 2025 22:35:09 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e39d44972f86c94e48a8ba761774c90c693cfd7248b9b3fa84a7905217f0c57a`  
		Last Modified: Thu, 04 Dec 2025 22:35:10 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine3.23`

```console
$ docker pull memcached@sha256:c8503d4491edd3110cc07d0465089d3a41cf1daf8645e71149e39a51835e92cd
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

### `memcached:alpine3.23` - linux; amd64

```console
$ docker pull memcached@sha256:aac456c35cd29635b5501fefac58a2e954752006c9d159fbf520dd785e09cbba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5973577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6411cdd430a5f0c33aea6496062ab90fbc7da776f1c937108cf51b7a40e090f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:20:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:20:42 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:23:18 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:23:18 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:23:18 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:23:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:23:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:23:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:23:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:23:18 GMT
USER memcache
# Thu, 04 Dec 2025 19:23:18 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:23:18 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e377e19df274e9919dbfbe05b510e54db0f8451ac0985b108aba9123048001d8`  
		Last Modified: Thu, 04 Dec 2025 19:23:54 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0d9328fb6b4452be1f62a5c6db62b8425a6b48c40ce2408ae0f526b101c80c`  
		Last Modified: Thu, 04 Dec 2025 19:23:55 GMT  
		Size: 106.0 KB (106047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a1eb06c51acdaf80ce22a4524ea827613ecc609e23cb0fa481005e89b22d4f`  
		Last Modified: Thu, 04 Dec 2025 19:23:54 GMT  
		Size: 2.0 MB (2006867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4829db5772d5079a1be438e2b4d4921e584e88e6becb7ca1819f33cc6ddd962c`  
		Last Modified: Thu, 04 Dec 2025 19:23:54 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b919142486c25c1941bfb65c0f6f26ff49ed2820b62db8ee149ac5a386bcd76c`  
		Last Modified: Thu, 04 Dec 2025 19:23:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:849b937b30f8457f48d4a2b4dee48812e3f3fef3740e8553fbeb950ef1e6a405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3eb9da9040350a8be21d03f2423ac5b520d62898c8656b204d89a46be87cca`

```dockerfile
```

-	Layers:
	-	`sha256:a6a585b25dcf23d45fe100d658f3fc872a69be33f37f5b142951380b902e1a65`  
		Last Modified: Thu, 04 Dec 2025 22:34:43 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91e8f143d354857f78ae4fd0e5416b79eb34dc3599af1f3df2161a4fa1885af9`  
		Last Modified: Thu, 04 Dec 2025 22:34:44 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; arm variant v6

```console
$ docker pull memcached@sha256:a7003e700207ebf4fd102e5d81432129cd3e4776c613ee53fa01b0dbd5e9f19b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5629653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36796824ef2ab4ff08673e2fdd2ff3529a8c6c476c842ec665b90db7e63fad02`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:21:33 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:21:34 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:33:55 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:33:55 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:33:55 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:33:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:33:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:33:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:33:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:33:55 GMT
USER memcache
# Thu, 04 Dec 2025 19:33:55 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:33:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2477fbd5a498e104db4354cbb88ebe3bf7d7f22609c3d9f3996ee3d6f2b311`  
		Last Modified: Thu, 04 Dec 2025 19:34:10 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d610e2e19bb7ad98b2e77e581123187db039c4259f548f8e16e1b5015d0ec85`  
		Last Modified: Thu, 04 Dec 2025 19:34:10 GMT  
		Size: 102.6 KB (102642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5e9f0ad4522a9fedea5ba5229899ef09d25774a89a517cf59cae7a36e4ea92`  
		Last Modified: Thu, 04 Dec 2025 19:34:10 GMT  
		Size: 2.0 MB (1957764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8b426cdf478aef96c3b7780b5b6c81b458a0787358d6251799150a9f714aaf`  
		Last Modified: Thu, 04 Dec 2025 19:34:10 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd456d3218701485ecd1ce99f10c7a08986e44f71d19a49e419582aeb4924f52`  
		Last Modified: Thu, 04 Dec 2025 19:34:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:95ab79e458ab0908467ebbdf5539b688045b04421a068fa6821d557eece2f67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569a816a11d27d030ea4089563f4a23efecb872605941df1c53c0c4152fbd211`

```dockerfile
```

-	Layers:
	-	`sha256:dd9475807057d6ac4c96f526dc77e867efe6bb682d09ef1c7c0557b6f2dad356`  
		Last Modified: Thu, 04 Dec 2025 22:34:47 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; arm variant v7

```console
$ docker pull memcached@sha256:6b1fcd05fdcf13d4b7650d85e6043cdeaf423fe9ec57036c0f203e4eef6bff12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5289618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca393e3ead8035915d8cd6bcea0e8ccbe82d8ae05b9cad79126dd93567ff2889`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:43 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:19:44 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:22:37 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:22:37 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:22:37 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:22:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:22:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:22:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:22:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:22:37 GMT
USER memcache
# Thu, 04 Dec 2025 19:22:37 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:22:37 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdc28d0a8cb5092fb181830a0ef7fb2c55b0dcec915fb49171721470a36990e`  
		Last Modified: Thu, 04 Dec 2025 19:22:53 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d64ac2dd6859410fc8786621ad68f29d5cf9799784bd6181fa0fd9b16f10b5`  
		Last Modified: Thu, 04 Dec 2025 19:22:53 GMT  
		Size: 92.4 KB (92376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf39f9a50690d556c95f99315866a17736de133854b3f4a1f01c007e8ea52e8c`  
		Last Modified: Thu, 04 Dec 2025 19:22:53 GMT  
		Size: 1.9 MB (1917424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5adf2295dafdfb5341494ff56dfa3c9fef413e476cc7e0ea0a44ea325856fd40`  
		Last Modified: Thu, 04 Dec 2025 19:22:53 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f68652d871fbfba49b4bdb6f0555e3d086490ac907f630de1960481a50b5982`  
		Last Modified: Thu, 04 Dec 2025 19:22:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:726bec6c0e6bb11f92cf809b0eff6ee10fc86a30eae935ac85e0b82f2fc110d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:489bd5540d03661ecd23b22a8d9070b7dc18f542d91bc1ed60efaa1790080a39`

```dockerfile
```

-	Layers:
	-	`sha256:35def5ffffb77a9cc93b2d806351b5bc638603257621ee3ea2fcab826508b445`  
		Last Modified: Thu, 04 Dec 2025 22:34:50 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b55f58069fda39e67b560d97ac46c79e035b513a560bc8652e5383cd3f82a35`  
		Last Modified: Thu, 04 Dec 2025 22:34:51 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b263323af06e550df9becd8c2cf8450400be7ae4381392593565dc8247bb230f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6304413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:038de42e33564e147549bf3846c2490c168364063ebc7744c8cdd580e202c191`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:20:28 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:20:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:23:16 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:23:16 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:23:16 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:23:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:23:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:23:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:23:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:23:16 GMT
USER memcache
# Thu, 04 Dec 2025 19:23:16 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:23:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4ea1ce2b4c6bdcd3eec4d60b1aa2e3563da544759bff4e7a46469132a86438`  
		Last Modified: Thu, 04 Dec 2025 19:23:27 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc9938ef133bd132ee91a60f23198ae468dca72e6b547301fc4b29e4136bc9e`  
		Last Modified: Thu, 04 Dec 2025 19:23:28 GMT  
		Size: 121.9 KB (121870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fbb7f498823838642f0cbc3dfbcce9ec16c50549649b23872df57076fed9e7`  
		Last Modified: Thu, 04 Dec 2025 19:23:28 GMT  
		Size: 2.0 MB (1985993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341b9a721d462e12012b285eb88cdd865e1fa62f664d8343c3223d3b18b5ed0c`  
		Last Modified: Thu, 04 Dec 2025 19:23:27 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f879a6e1902c8a256d8dea45afd4efc95caa82bd9fcf3291b6730a20d2c5a0`  
		Last Modified: Thu, 04 Dec 2025 19:23:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:9e1d743b77c8856403d4e8420e9936de4aa1bc6fc88642c47112e318e10e2655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556ecd6a50c7ec0f18eea0bb6b6a3c2a30163cdbf6e0a9314ef069819efdb628`

```dockerfile
```

-	Layers:
	-	`sha256:57a22eef052f1e8ba0bdbfa2e165923ea29a9572ab9d397f6652f44a895c34c9`  
		Last Modified: Thu, 04 Dec 2025 22:34:54 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea1714f2bc9b4e6925e95bfc0d324fe4686d662ad257e5959451179599d072e6`  
		Last Modified: Thu, 04 Dec 2025 22:34:55 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; 386

```console
$ docker pull memcached@sha256:b3d88ad28118ac190ff8cfd6be5b29a4aff4e4f772124ba8a6cb7335eb909152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5762624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfa1253f0cf9e80c36b723ff6f79bb43b3cb4c3146f4340f605aaf0bb812eaa1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:20:00 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:20:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:22:43 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:22:43 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:22:43 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:22:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:22:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:22:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:22:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:22:43 GMT
USER memcache
# Thu, 04 Dec 2025 19:22:43 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:22:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3527b4f952d5950d8caa74dc0d1759215000f2f0a195344f0239c7e2805fe2fc`  
		Last Modified: Wed, 03 Dec 2025 19:30:41 GMT  
		Size: 3.7 MB (3685856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801e2ef7c6c58c48cfc036b3ffd9de546ffd13f67044c4c296b3624d08852398`  
		Last Modified: Thu, 04 Dec 2025 19:22:57 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7528d81de6e75b8aa074f7b96d6b9f2650422ca25fc0f5485dadf33879a4eb7`  
		Last Modified: Thu, 04 Dec 2025 19:22:57 GMT  
		Size: 110.7 KB (110732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40cb203b33be80dad7c861215d0c69239f729987a3942b71d4fc7b17423658e`  
		Last Modified: Thu, 04 Dec 2025 19:22:58 GMT  
		Size: 2.0 MB (1964688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbaa8273de612bce797fce27339a8adb341655d9b03a120aa874e80bfc438ba`  
		Last Modified: Thu, 04 Dec 2025 19:22:57 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a62b5e894734682a138338f04d49ebcb3e61a322469798019f9737e8ef19b33`  
		Last Modified: Thu, 04 Dec 2025 19:22:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:a8428c10b46dc321be308528a9dc3904db404457e03384a035c6e8c7bf32d05e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c97e68a8fd4c390f7dac3c43eda5f00b0b29eb2b838b877b0926ec7a55ec29`

```dockerfile
```

-	Layers:
	-	`sha256:5414f83497841dc88789d15a422792cf5c1818a72a4ebe7fa9f569a4824ce99f`  
		Last Modified: Thu, 04 Dec 2025 22:34:58 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19ce16735c127991fab0a49081d04170d61fc3b2c60261704ec9247a0edc119f`  
		Last Modified: Thu, 04 Dec 2025 22:35:02 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; ppc64le

```console
$ docker pull memcached@sha256:6ff6570e2a8fb560a3b830e0f1475d488961b29b93e711d03fd52464844926b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6058459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9360c3d396b9f5081cdc222d176f25b51a35c42c688d1ff1da3ad33a71befeb9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:22 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:19:24 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:21:48 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:21:48 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:21:48 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:21:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:21:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:21:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:21:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:21:49 GMT
USER memcache
# Thu, 04 Dec 2025 19:21:49 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:21:49 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23500700235e36a847f2b35c25e17b359b4cec377d3a0fbafdfff7ec561ecf74`  
		Last Modified: Thu, 04 Dec 2025 19:22:05 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47c608c5e84b70e2288ed6c722d682394718aa7029f3614c85bb3faa2d1a0ab`  
		Last Modified: Thu, 04 Dec 2025 19:22:05 GMT  
		Size: 126.3 KB (126267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251cee6c1abe9d3d9e832748d0edb232d4e43fbbdfc78f3fad887409eff7a658`  
		Last Modified: Thu, 04 Dec 2025 19:22:06 GMT  
		Size: 2.1 MB (2103821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82b7a39ab647b07cb8e684e6fbe6e0c40959b95f23e8b6fba544f6412e08e10`  
		Last Modified: Thu, 04 Dec 2025 19:22:05 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e989166bceb7b8bb922420cfda5d2c1c362b469900fbbd86593fb4422e6f2fb6`  
		Last Modified: Thu, 04 Dec 2025 19:22:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:ad7264b3f464d43618d5e997d3c544a46d5d00112555908bab3e31ddfb719fd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da20be024f8583ae82747476a5a8b1054a0d2018ceade3cfcc11e0b460a369e3`

```dockerfile
```

-	Layers:
	-	`sha256:08dd8ac2fb865783b3720303c0b7abe96c0d831dd8dbd89f5ce48f64f5d93577`  
		Last Modified: Thu, 04 Dec 2025 22:35:05 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52998ad89b5d31b02c435f1dabae41e0023686389189f0729699301d2b2dceba`  
		Last Modified: Thu, 04 Dec 2025 22:35:06 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; riscv64

```console
$ docker pull memcached@sha256:82618728d34fd5e3c642277cb563310bed5e815337b99361c23d0d4225e3a1ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5793289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95bfdee9049204386f5f9675313ec0cf6437686f3e41ac46a02d7491c4ebd031`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:39 GMT
ADD alpine-minirootfs-3.23.0-riscv64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:39 GMT
CMD ["/bin/sh"]
# Fri, 05 Dec 2025 02:28:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 05 Dec 2025 02:28:43 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 05 Dec 2025 02:42:05 GMT
ENV MEMCACHED_VERSION=1.6.39
# Fri, 05 Dec 2025 02:42:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Fri, 05 Dec 2025 02:42:05 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Fri, 05 Dec 2025 02:42:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 05 Dec 2025 02:42:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Dec 2025 02:42:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Dec 2025 02:42:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Dec 2025 02:42:06 GMT
USER memcache
# Fri, 05 Dec 2025 02:42:06 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Dec 2025 02:42:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9929557817a4c85b33d6dbeb491f7396ef32added7e77de7ac1b644ed0975313`  
		Last Modified: Wed, 03 Dec 2025 19:30:17 GMT  
		Size: 3.6 MB (3583519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04477eae70c2e3cb1bd666913116b231bd91f758fef0ce0487128436edf54e3`  
		Last Modified: Fri, 05 Dec 2025 02:42:36 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27775dcc23cac586ff5717daea95b160d3515a30312e73dc28db55554bcbdd12`  
		Last Modified: Fri, 05 Dec 2025 02:42:37 GMT  
		Size: 108.9 KB (108892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d493e7dad99e12ada2c869111712bae9f61d05aabeb2139df6297985982f119`  
		Last Modified: Fri, 05 Dec 2025 02:42:37 GMT  
		Size: 2.1 MB (2099525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf14d0478c213567d1f2646d01cd27ca8c3db42c197fceb2c2fe55c1ea5bfd84`  
		Last Modified: Fri, 05 Dec 2025 02:42:37 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb60cadd22d3f64cee1f02bcfccb5472502730fea2408ffa893c00d4cae9e97c`  
		Last Modified: Fri, 05 Dec 2025 02:42:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:6607c3431ad2ac598c8476330688ee82114c9b3c0e9b2849f86d95addf5e48eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8406d4978e549630fb362ff2901a3645f7d325e1cce867bbfddade8ceb14232`

```dockerfile
```

-	Layers:
	-	`sha256:5ae6f5f57506c9cba95d087771e8253c7ee7c129dcbc4fdd524a99f4feeafec9`  
		Last Modified: Fri, 05 Dec 2025 04:34:37 GMT  
		Size: 94.3 KB (94276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b9a49d787a1cd02fea8b8affc293bd2d718765b8ef3d8cf26d839f80d072eea`  
		Last Modified: Fri, 05 Dec 2025 04:34:38 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; s390x

```console
$ docker pull memcached@sha256:b23b3b07e717d7651a02ec547a675f198e684f410c7217a09bd305de6c20e664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5878802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e586dd7e72674888df0e6f0ade73d053d2a5a94b7d890a276fb6f13fba7e4cc3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:22 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 04 Dec 2025 19:19:24 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 04 Dec 2025 19:22:39 GMT
ENV MEMCACHED_VERSION=1.6.39
# Thu, 04 Dec 2025 19:22:39 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Thu, 04 Dec 2025 19:22:39 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Thu, 04 Dec 2025 19:22:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 04 Dec 2025 19:22:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:22:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 04 Dec 2025 19:22:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:22:39 GMT
USER memcache
# Thu, 04 Dec 2025 19:22:39 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 04 Dec 2025 19:22:39 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a188510a1e7e85e0e83a71da1abed06b459c07887a679cf331da7789673755`  
		Last Modified: Thu, 04 Dec 2025 19:23:03 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67afe5cdcebd55aec1e59a816853f758650056c83c63ea4d99d6e06e15f60fd`  
		Last Modified: Thu, 04 Dec 2025 19:23:03 GMT  
		Size: 114.3 KB (114286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377a08e6b7dd38664aeee34c52a61b8f7edf9165adabbaee0e0b923423a60242`  
		Last Modified: Thu, 04 Dec 2025 19:23:03 GMT  
		Size: 2.0 MB (2039357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c47067ba1641d8aa2a1f3d7df1e359c1ef226673c5b60eeecc3824f3609e9b`  
		Last Modified: Thu, 04 Dec 2025 19:23:03 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e307cf70f379099e1c944f0972ea3478099fc2221e7ae304d3c47858cb9c8b`  
		Last Modified: Thu, 04 Dec 2025 19:23:03 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:db1f4e6b802cb9b4ee6a404e244522a143516b6c5dfe88d706e7d657e8a3c6c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e21cb3a2b9f702a014eac05118559131c607052ca17bd1adb7ddb02107d291d0`

```dockerfile
```

-	Layers:
	-	`sha256:a484d75866b9f2198dfeccc7d70aa01018c27dd00a8bdad7b47bb8f659ee35d1`  
		Last Modified: Thu, 04 Dec 2025 22:35:09 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e39d44972f86c94e48a8ba761774c90c693cfd7248b9b3fa84a7905217f0c57a`  
		Last Modified: Thu, 04 Dec 2025 22:35:10 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:latest`

```console
$ docker pull memcached@sha256:c7628370ae681c42dbd48ccf02320d77a2bc0234f9ba3a968b5da3a7c0112469
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:latest` - linux; amd64

```console
$ docker pull memcached@sha256:153e4ed762fd3bc07fe607f64631647939278d6101759d91fac0b756cceb2272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32208551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa0c800d7278560e11e4d0f14defc4d2d850224d0859d1bd0e9205cc962478d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:38:46 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:38:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:41:30 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:41:30 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:41:30 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:41:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:41:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:41:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:41:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:41:30 GMT
USER memcache
# Mon, 08 Dec 2025 22:41:30 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:41:30 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e33b5452dc8ba5d42cd13b42745898ef870af3e8d5a65b06b8b174f06b1d50`  
		Last Modified: Mon, 08 Dec 2025 22:41:43 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce4ec629da8029212ce5d775073648d04f1f014a89e49f73f1fc848bc405dd5`  
		Last Modified: Mon, 08 Dec 2025 22:41:43 GMT  
		Size: 136.7 KB (136697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6210dfd46759cbe6922de2db75ddf6d17c1f033a434ee6bcf2e82d56ce59f449`  
		Last Modified: Mon, 08 Dec 2025 22:41:43 GMT  
		Size: 2.3 MB (2293845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffbb5d472cb4680299753b978d2e8eeb6d2288ee4caec01e65541f4358516a6`  
		Last Modified: Mon, 08 Dec 2025 22:41:43 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e474cc606bdb91c69d2f124d38e5ebd93ed9ab64d219ab51845cc238a5904aa`  
		Last Modified: Mon, 08 Dec 2025 22:41:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:45cb4f875b600a26ef6e0388db256b09a14580b17ddcaa485fd2c25cbff56056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6483c69793152c682b93375229933004781cbf7df7f059d288d2d7e04335b2c8`

```dockerfile
```

-	Layers:
	-	`sha256:c3beab005b14cd0614637cc43c84460edfb07d9c68b1138ee676ab5bd3dc05ac`  
		Last Modified: Tue, 09 Dec 2025 01:34:56 GMT  
		Size: 2.0 MB (2008228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6ce8cbbfb878c257688fdf1d5e1a9c428b68061ee92f8e07a240ab0fe4b812e`  
		Last Modified: Tue, 09 Dec 2025 01:34:57 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:5a7b1183ed0a0ca89ce3d88e335fca2672422eee8d05921621cd4ed617965ed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30317206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1552234329fddb68f43cfe1abdf3dff1b1499edbb12eb6d84c481f3d7fbe2c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:34:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:37:32 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:37:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:37:32 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:37:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:37:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:37:32 GMT
USER memcache
# Mon, 08 Dec 2025 22:37:32 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:37:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d97bc71d0fa535127863fdab265dfddb07b3cda35b80de4dd2b9b67fe154c856`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 27.9 MB (27944187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d0d6688f3764bd09c70b0fdb00a12bc517f76c47fc187448da8cf7958b4b98`  
		Last Modified: Mon, 08 Dec 2025 22:37:44 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1a7c3cdaa260d51a1e04177297af5b7e205abe78e98f0782c38369f1a49034`  
		Last Modified: Mon, 08 Dec 2025 22:37:45 GMT  
		Size: 144.1 KB (144146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e35266d4886f5160ecccf89b51e0317cf6c7ad5a063a40d74c0dd0baa75b974`  
		Last Modified: Mon, 08 Dec 2025 22:37:45 GMT  
		Size: 2.2 MB (2227364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3324af035e2f7b73ce2f8c3d5ee46e80ed9063e2ae219caf112d6bafe3d935a3`  
		Last Modified: Mon, 08 Dec 2025 22:37:44 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae7d716f59ff9d69d00b890308b431e236e3a1d530f0dfa1ccaabdd01ea7df2`  
		Last Modified: Mon, 08 Dec 2025 22:37:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:077fa23fa7fd08a421aff7ec84a802bb72f53e3f31c9fb2bba4df39b99ae3923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92bd65e20c21649e0ebcbd5810944fd9e43ecf788ec1d580bfc3c04722bf6fa4`

```dockerfile
```

-	Layers:
	-	`sha256:02c0b341ef4c59b9ffa7a8de46289cbd08d3a3b029c0a64224da804b55e2e854`  
		Last Modified: Tue, 09 Dec 2025 01:35:01 GMT  
		Size: 2.0 MB (2011231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb1ede44c11856b6e3f7c4f6ba238d3df5677af459242c47b9f24b4a1c184db0`  
		Last Modified: Tue, 09 Dec 2025 01:35:02 GMT  
		Size: 22.3 KB (22302 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v7

```console
$ docker pull memcached@sha256:cb9b94d371b2da6a520b577dd688b99c959dac8ad5e81f17aaf8e5b6ed1968ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28529520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a8988937956147836c267576a47663f836997a1d6a21750c17c7d2e52982c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:38:02 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:38:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:41:09 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:41:09 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:41:09 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:41:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:41:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:41:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:41:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:41:09 GMT
USER memcache
# Mon, 08 Dec 2025 22:41:09 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:41:09 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15599337d37fa53f93b66130266f60f942cc7c2c4e2e8458c672f9b61b921350`  
		Last Modified: Mon, 08 Dec 2025 22:41:22 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4e148e811da2c8aeb3f52da0f7e137c9e2dbf7e07ea25ed2a8ec2bc3db340d`  
		Last Modified: Mon, 08 Dec 2025 22:41:25 GMT  
		Size: 135.4 KB (135363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248d1bdc7fd809ba8d6d01e877ae1ff16258cd1b26203215342935af2305c133`  
		Last Modified: Mon, 08 Dec 2025 22:41:22 GMT  
		Size: 2.2 MB (2182634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4dca52427f97b68739a35240dde721713ae992674b8f6fe50fc71d987512c4`  
		Last Modified: Mon, 08 Dec 2025 22:41:22 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2961ef381f352090fe3d59e2ff32ae5c2979defa070a22f5fc846bb2b5f0f30`  
		Last Modified: Mon, 08 Dec 2025 22:41:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:cff996fea1034ca7a74465fdf5489ef45c78f70859319df22468100dc3c84e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e8d92fa13df244234c51ab1b93e9a4c39ad977f40dd5b49cef4e8ed0de7e3a`

```dockerfile
```

-	Layers:
	-	`sha256:d08663eef9d4f14b4b344cf2d8924f04dee694d602df55d600a90830f505069b`  
		Last Modified: Tue, 09 Dec 2025 01:35:06 GMT  
		Size: 2.0 MB (2009688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb1b323cef393d68691ca1f808424d4c4ca9aa868a63329889d55c9e53c30671`  
		Last Modified: Tue, 09 Dec 2025 01:35:06 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:6230125fff57e6f22504aae8db1ed049b738d97c3e325a68a9733a186fab61e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32568877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2f55b9564478802d59f2ab50cadac0b6e11704297ea84bc7fdcc4e9fb3ba76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:38:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:38:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:41:20 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:41:20 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:41:20 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:41:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:41:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:41:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:41:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:41:20 GMT
USER memcache
# Mon, 08 Dec 2025 22:41:20 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:41:20 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91cd2e642e1c9b79606d81fe7ae3f5599c2e1a2ebb80864a1c25f4771502b02`  
		Last Modified: Mon, 08 Dec 2025 22:41:32 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9b5941656d039525e2c86c6dad7b225e0dfe8a89bda1c33c46f84b7e1f05f0`  
		Last Modified: Mon, 08 Dec 2025 22:41:32 GMT  
		Size: 153.5 KB (153454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc829d43c3195e76b119f7ef9e8519d7c64f130e104b29b5317d18e709d3796`  
		Last Modified: Mon, 08 Dec 2025 22:41:32 GMT  
		Size: 2.3 MB (2275286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685e3db2e1ea7f3a85650a5cac398166f6fe54b1767d8ab65fd070fc9f08f903`  
		Last Modified: Mon, 08 Dec 2025 22:41:32 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bedd2011ff5fea2608113c25dac443f7f67fd30b9f049d14304a5eeba342453`  
		Last Modified: Mon, 08 Dec 2025 22:41:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:5be232fd0ce753823a0a00a2e155ca7ed374028d0a228270604974765be63286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ad988781bd90f9b424c8530a983604f0dea5e9ff5d39be9ca322ea793f7044`

```dockerfile
```

-	Layers:
	-	`sha256:2f225cf8fe800d6f4631961cb099b7f796ad28fbe325df7943d5fd182391187f`  
		Last Modified: Tue, 09 Dec 2025 01:35:10 GMT  
		Size: 2.0 MB (2008544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd6800d8108ddffdecd1e6d030f8948b6ed22cff74e19779380d731dfd189d0d`  
		Last Modified: Tue, 09 Dec 2025 01:35:11 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:9c8dd1c0a7d71ffb9540bcdac40c6c72661b05ad12d1a0dcacb86ba0dad353b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33686582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a221f2cf3f75cb38b8be293e0d315a4453967306dc401835f3732a7ec18482d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:17 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:33:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:36:13 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:36:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:36:13 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:36:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:36:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:36:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:36:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:36:13 GMT
USER memcache
# Mon, 08 Dec 2025 22:36:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:36:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c63a49351bc91fd837d81e97ce862507215607bc756f1133f1d887e94e1cc4e`  
		Last Modified: Mon, 08 Dec 2025 22:36:26 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7073e103108a28c5e5a1458be46ac8c708375f2b4327423a59471a77bbf2c0c6`  
		Last Modified: Mon, 08 Dec 2025 22:36:26 GMT  
		Size: 147.5 KB (147516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbfa39b86ad2206ef2fdf5ec3f3a55aa40c422a9f3fca094c7c2f003e7d4a63`  
		Last Modified: Mon, 08 Dec 2025 22:36:26 GMT  
		Size: 2.2 MB (2244483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1ade71ea049e11fc9cea7c16944632ffd753dfe7130e3bb4e1730281daffb5`  
		Last Modified: Mon, 08 Dec 2025 22:36:26 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5eb870312490559d775f9d994ba10b9fcae44c680e23a647a43c1c55f49b54`  
		Last Modified: Mon, 08 Dec 2025 22:36:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:e5ea0a4780f0574f775d4cf8c4ffff6f6b836e33d54d6d241047fa36e54d70b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1425c202287fb1c6f81bb3962bb416b9f23b14b12da6119772ac599ae7af4b`

```dockerfile
```

-	Layers:
	-	`sha256:9d6ed296b190f0f66c6f54ffafa76bd9f86d72e2a463ed9841c2654abf7282d0`  
		Last Modified: Tue, 09 Dec 2025 01:35:16 GMT  
		Size: 2.0 MB (2005385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d9f28b39486b665dcd60f89a225a5fce2e4060feaed50b57eaf89bc54345129`  
		Last Modified: Tue, 09 Dec 2025 01:35:17 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:9a5a8c51d01a2dde31ee88dc7739b61aad1cd244c1592033d64b89e71ea9d086
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36185779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62a722a142df5369183f571c8eecacbc8041e72fb89888b569e2e558947291b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:32:15 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 09 Dec 2025 00:32:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:35:25 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 09 Dec 2025 00:35:25 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 09 Dec 2025 00:35:25 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 09 Dec 2025 00:35:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 09 Dec 2025 00:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 00:35:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 09 Dec 2025 00:35:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Dec 2025 00:35:26 GMT
USER memcache
# Tue, 09 Dec 2025 00:35:26 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 09 Dec 2025 00:35:26 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca80ecfb634d24079bf04d5695260ea9dce9f468064fb83123a71959d22b7c4`  
		Last Modified: Tue, 09 Dec 2025 00:35:51 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb90fb01769b3666ac21d77bcba16bd54161463250fa6f304710eb00d5ab5411`  
		Last Modified: Tue, 09 Dec 2025 00:35:51 GMT  
		Size: 170.4 KB (170375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be675ba49db497b747d37543689ff0b8fc0ef4398cd718c2fadd28302d88141b`  
		Last Modified: Tue, 09 Dec 2025 00:35:51 GMT  
		Size: 2.4 MB (2417005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882b9516d2a74a32203b37778b6025dc9c68a30838e1fa420559c34fe0319141`  
		Last Modified: Tue, 09 Dec 2025 00:35:51 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5cfa5b161387b536b9f8a94f199ffd006893e19e7bff82a8f1f9a7aa578a73`  
		Last Modified: Tue, 09 Dec 2025 00:35:51 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:6ea51b9da9219f68c45e3345bed106b961bce70b2c9aecbb6e1300060e04217d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f87eac26bbbb68ef23dfd63867d0415ddc04fe2567863569701f2891733279d6`

```dockerfile
```

-	Layers:
	-	`sha256:6f8bb9e427f03eea07711eb22a22462b3548d9ed3bf7b82f412aea5a623b10ff`  
		Last Modified: Tue, 09 Dec 2025 04:34:42 GMT  
		Size: 2.0 MB (2011829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1705de570678d9ecda7c8bb1da82748111d8547fb22bfbfb43fbbf41808b5b67`  
		Last Modified: Tue, 09 Dec 2025 04:34:43 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; riscv64

```console
$ docker pull memcached@sha256:05d76bdff41209572f5e6c4d21717d0717a794340a2bc2c086af7a863f5c19af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30627687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c785d7526540c98189bc45e1c3ad5a9862a6ed744c2b49e94165199ba9dcd7ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 10:11:36 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 10:12:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 10:53:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 10:53:11 GMT
USER memcache
# Tue, 18 Nov 2025 10:53:11 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 10:53:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f7062dea9fa0a796a2eacb7b265e4b2000be3d07bc91c20a5abc6538e5a68c`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f8a04356a93113399cb041ac377cf221db2df7d9fc3a6d630a061a923eb1e6`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 133.1 KB (133088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4bbee7a68150daca8b6b94e26e1a04551afc5a77dfb08a4e04aadc0933c456`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 2.2 MB (2219954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085465091dfa79c5f79dd2c74f56f75a8e078b89272039f8d8ed5a1d2adac41b`  
		Last Modified: Tue, 18 Nov 2025 10:54:06 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea3aae46e46f60ca268fd3c445c8b9ed827d7daba7e6d611310cfc9dc4d5291`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:7a8af6c2848585e79b5cb65b6a760b1f78f0de3a59fb604d7a026c79f05a77b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c73002e7361572816b1c22cbb73aced8ce908f6492f2b5d15371b7c0a0514546`

```dockerfile
```

-	Layers:
	-	`sha256:059e3337eaf5c7461d584e0f4b5c7c660bf41a1bb79e90aa917a3992eba4c855`  
		Last Modified: Tue, 18 Nov 2025 16:35:44 GMT  
		Size: 2.0 MB (2002192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cf39200d9e698624fc7d7abe914cab80bda5407ae30f111eb22846e8fd28bba`  
		Last Modified: Tue, 18 Nov 2025 16:35:45 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:332c41cfc207814782dda23a2b840d653abb751f335f7f02f6b238ce79c1c08c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32290312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2be68b3a60f2d8e906983e133fcaffe03bd1a82c9acc69a3dcbe3e307d7b8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:21 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:33:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:36:33 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:36:33 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:36:33 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:36:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:36:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:36:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:36:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:36:34 GMT
USER memcache
# Mon, 08 Dec 2025 22:36:34 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:36:34 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc040aa39039515a9f8b38dc90047178bd8fa0d8234856954f045f05050e52c`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e235f00f3da465d44b7ac18782958812c19e974f091dedfc097442ba632a3d`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 140.5 KB (140505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284c7cc2b7cc68de54eb5bce5de02ed5229cb403476e794b8066eee16babb6e1`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 2.3 MB (2313897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5059135976f7ec26a104b2fb6340b0ae8adc5756ea159deede93c8532613fd24`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd63939e0e5898afa1d51d59354c263e9a7ebfba3e418395baf21445315251de`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:8a7be7ae9cfd628f1585c887ce286f74e97f7780cc20009ffe07f9c92623b34c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c6fbc39d1b80ba4ed6852329a8ddfcaaeed5500129f5019fbc5a8904a7cd659`

```dockerfile
```

-	Layers:
	-	`sha256:0a66a7a3c4891f559fc098f2c13e48d32804e22f559857d3c89074b829300c25`  
		Last Modified: Tue, 09 Dec 2025 01:35:26 GMT  
		Size: 2.0 MB (2009665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24d3a4bbcde50a51a341ad980cc2d92d652ec5f9394c80d55c8a70ded47d8927`  
		Last Modified: Tue, 09 Dec 2025 01:35:27 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:trixie`

```console
$ docker pull memcached@sha256:c7628370ae681c42dbd48ccf02320d77a2bc0234f9ba3a968b5da3a7c0112469
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:trixie` - linux; amd64

```console
$ docker pull memcached@sha256:153e4ed762fd3bc07fe607f64631647939278d6101759d91fac0b756cceb2272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32208551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa0c800d7278560e11e4d0f14defc4d2d850224d0859d1bd0e9205cc962478d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:38:46 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:38:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:41:30 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:41:30 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:41:30 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:41:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:41:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:41:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:41:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:41:30 GMT
USER memcache
# Mon, 08 Dec 2025 22:41:30 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:41:30 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e33b5452dc8ba5d42cd13b42745898ef870af3e8d5a65b06b8b174f06b1d50`  
		Last Modified: Mon, 08 Dec 2025 22:41:43 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce4ec629da8029212ce5d775073648d04f1f014a89e49f73f1fc848bc405dd5`  
		Last Modified: Mon, 08 Dec 2025 22:41:43 GMT  
		Size: 136.7 KB (136697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6210dfd46759cbe6922de2db75ddf6d17c1f033a434ee6bcf2e82d56ce59f449`  
		Last Modified: Mon, 08 Dec 2025 22:41:43 GMT  
		Size: 2.3 MB (2293845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffbb5d472cb4680299753b978d2e8eeb6d2288ee4caec01e65541f4358516a6`  
		Last Modified: Mon, 08 Dec 2025 22:41:43 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e474cc606bdb91c69d2f124d38e5ebd93ed9ab64d219ab51845cc238a5904aa`  
		Last Modified: Mon, 08 Dec 2025 22:41:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:45cb4f875b600a26ef6e0388db256b09a14580b17ddcaa485fd2c25cbff56056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6483c69793152c682b93375229933004781cbf7df7f059d288d2d7e04335b2c8`

```dockerfile
```

-	Layers:
	-	`sha256:c3beab005b14cd0614637cc43c84460edfb07d9c68b1138ee676ab5bd3dc05ac`  
		Last Modified: Tue, 09 Dec 2025 01:34:56 GMT  
		Size: 2.0 MB (2008228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6ce8cbbfb878c257688fdf1d5e1a9c428b68061ee92f8e07a240ab0fe4b812e`  
		Last Modified: Tue, 09 Dec 2025 01:34:57 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:5a7b1183ed0a0ca89ce3d88e335fca2672422eee8d05921621cd4ed617965ed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30317206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1552234329fddb68f43cfe1abdf3dff1b1499edbb12eb6d84c481f3d7fbe2c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:34:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:37:32 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:37:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:37:32 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:37:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:37:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:37:32 GMT
USER memcache
# Mon, 08 Dec 2025 22:37:32 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:37:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d97bc71d0fa535127863fdab265dfddb07b3cda35b80de4dd2b9b67fe154c856`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 27.9 MB (27944187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d0d6688f3764bd09c70b0fdb00a12bc517f76c47fc187448da8cf7958b4b98`  
		Last Modified: Mon, 08 Dec 2025 22:37:44 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1a7c3cdaa260d51a1e04177297af5b7e205abe78e98f0782c38369f1a49034`  
		Last Modified: Mon, 08 Dec 2025 22:37:45 GMT  
		Size: 144.1 KB (144146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e35266d4886f5160ecccf89b51e0317cf6c7ad5a063a40d74c0dd0baa75b974`  
		Last Modified: Mon, 08 Dec 2025 22:37:45 GMT  
		Size: 2.2 MB (2227364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3324af035e2f7b73ce2f8c3d5ee46e80ed9063e2ae219caf112d6bafe3d935a3`  
		Last Modified: Mon, 08 Dec 2025 22:37:44 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae7d716f59ff9d69d00b890308b431e236e3a1d530f0dfa1ccaabdd01ea7df2`  
		Last Modified: Mon, 08 Dec 2025 22:37:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:077fa23fa7fd08a421aff7ec84a802bb72f53e3f31c9fb2bba4df39b99ae3923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92bd65e20c21649e0ebcbd5810944fd9e43ecf788ec1d580bfc3c04722bf6fa4`

```dockerfile
```

-	Layers:
	-	`sha256:02c0b341ef4c59b9ffa7a8de46289cbd08d3a3b029c0a64224da804b55e2e854`  
		Last Modified: Tue, 09 Dec 2025 01:35:01 GMT  
		Size: 2.0 MB (2011231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb1ede44c11856b6e3f7c4f6ba238d3df5677af459242c47b9f24b4a1c184db0`  
		Last Modified: Tue, 09 Dec 2025 01:35:02 GMT  
		Size: 22.3 KB (22302 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:cb9b94d371b2da6a520b577dd688b99c959dac8ad5e81f17aaf8e5b6ed1968ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28529520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a8988937956147836c267576a47663f836997a1d6a21750c17c7d2e52982c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:38:02 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:38:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:41:09 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:41:09 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:41:09 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:41:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:41:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:41:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:41:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:41:09 GMT
USER memcache
# Mon, 08 Dec 2025 22:41:09 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:41:09 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15599337d37fa53f93b66130266f60f942cc7c2c4e2e8458c672f9b61b921350`  
		Last Modified: Mon, 08 Dec 2025 22:41:22 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4e148e811da2c8aeb3f52da0f7e137c9e2dbf7e07ea25ed2a8ec2bc3db340d`  
		Last Modified: Mon, 08 Dec 2025 22:41:25 GMT  
		Size: 135.4 KB (135363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248d1bdc7fd809ba8d6d01e877ae1ff16258cd1b26203215342935af2305c133`  
		Last Modified: Mon, 08 Dec 2025 22:41:22 GMT  
		Size: 2.2 MB (2182634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4dca52427f97b68739a35240dde721713ae992674b8f6fe50fc71d987512c4`  
		Last Modified: Mon, 08 Dec 2025 22:41:22 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2961ef381f352090fe3d59e2ff32ae5c2979defa070a22f5fc846bb2b5f0f30`  
		Last Modified: Mon, 08 Dec 2025 22:41:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:cff996fea1034ca7a74465fdf5489ef45c78f70859319df22468100dc3c84e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e8d92fa13df244234c51ab1b93e9a4c39ad977f40dd5b49cef4e8ed0de7e3a`

```dockerfile
```

-	Layers:
	-	`sha256:d08663eef9d4f14b4b344cf2d8924f04dee694d602df55d600a90830f505069b`  
		Last Modified: Tue, 09 Dec 2025 01:35:06 GMT  
		Size: 2.0 MB (2009688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb1b323cef393d68691ca1f808424d4c4ca9aa868a63329889d55c9e53c30671`  
		Last Modified: Tue, 09 Dec 2025 01:35:06 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:6230125fff57e6f22504aae8db1ed049b738d97c3e325a68a9733a186fab61e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32568877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2f55b9564478802d59f2ab50cadac0b6e11704297ea84bc7fdcc4e9fb3ba76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:38:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:38:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:41:20 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:41:20 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:41:20 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:41:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:41:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:41:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:41:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:41:20 GMT
USER memcache
# Mon, 08 Dec 2025 22:41:20 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:41:20 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91cd2e642e1c9b79606d81fe7ae3f5599c2e1a2ebb80864a1c25f4771502b02`  
		Last Modified: Mon, 08 Dec 2025 22:41:32 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9b5941656d039525e2c86c6dad7b225e0dfe8a89bda1c33c46f84b7e1f05f0`  
		Last Modified: Mon, 08 Dec 2025 22:41:32 GMT  
		Size: 153.5 KB (153454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc829d43c3195e76b119f7ef9e8519d7c64f130e104b29b5317d18e709d3796`  
		Last Modified: Mon, 08 Dec 2025 22:41:32 GMT  
		Size: 2.3 MB (2275286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685e3db2e1ea7f3a85650a5cac398166f6fe54b1767d8ab65fd070fc9f08f903`  
		Last Modified: Mon, 08 Dec 2025 22:41:32 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bedd2011ff5fea2608113c25dac443f7f67fd30b9f049d14304a5eeba342453`  
		Last Modified: Mon, 08 Dec 2025 22:41:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:5be232fd0ce753823a0a00a2e155ca7ed374028d0a228270604974765be63286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ad988781bd90f9b424c8530a983604f0dea5e9ff5d39be9ca322ea793f7044`

```dockerfile
```

-	Layers:
	-	`sha256:2f225cf8fe800d6f4631961cb099b7f796ad28fbe325df7943d5fd182391187f`  
		Last Modified: Tue, 09 Dec 2025 01:35:10 GMT  
		Size: 2.0 MB (2008544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd6800d8108ddffdecd1e6d030f8948b6ed22cff74e19779380d731dfd189d0d`  
		Last Modified: Tue, 09 Dec 2025 01:35:11 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; 386

```console
$ docker pull memcached@sha256:9c8dd1c0a7d71ffb9540bcdac40c6c72661b05ad12d1a0dcacb86ba0dad353b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33686582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a221f2cf3f75cb38b8be293e0d315a4453967306dc401835f3732a7ec18482d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:17 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:33:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:36:13 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:36:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:36:13 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:36:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:36:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:36:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:36:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:36:13 GMT
USER memcache
# Mon, 08 Dec 2025 22:36:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:36:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c63a49351bc91fd837d81e97ce862507215607bc756f1133f1d887e94e1cc4e`  
		Last Modified: Mon, 08 Dec 2025 22:36:26 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7073e103108a28c5e5a1458be46ac8c708375f2b4327423a59471a77bbf2c0c6`  
		Last Modified: Mon, 08 Dec 2025 22:36:26 GMT  
		Size: 147.5 KB (147516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbfa39b86ad2206ef2fdf5ec3f3a55aa40c422a9f3fca094c7c2f003e7d4a63`  
		Last Modified: Mon, 08 Dec 2025 22:36:26 GMT  
		Size: 2.2 MB (2244483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1ade71ea049e11fc9cea7c16944632ffd753dfe7130e3bb4e1730281daffb5`  
		Last Modified: Mon, 08 Dec 2025 22:36:26 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5eb870312490559d775f9d994ba10b9fcae44c680e23a647a43c1c55f49b54`  
		Last Modified: Mon, 08 Dec 2025 22:36:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:e5ea0a4780f0574f775d4cf8c4ffff6f6b836e33d54d6d241047fa36e54d70b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1425c202287fb1c6f81bb3962bb416b9f23b14b12da6119772ac599ae7af4b`

```dockerfile
```

-	Layers:
	-	`sha256:9d6ed296b190f0f66c6f54ffafa76bd9f86d72e2a463ed9841c2654abf7282d0`  
		Last Modified: Tue, 09 Dec 2025 01:35:16 GMT  
		Size: 2.0 MB (2005385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d9f28b39486b665dcd60f89a225a5fce2e4060feaed50b57eaf89bc54345129`  
		Last Modified: Tue, 09 Dec 2025 01:35:17 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:9a5a8c51d01a2dde31ee88dc7739b61aad1cd244c1592033d64b89e71ea9d086
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36185779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62a722a142df5369183f571c8eecacbc8041e72fb89888b569e2e558947291b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:32:15 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 09 Dec 2025 00:32:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:35:25 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 09 Dec 2025 00:35:25 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 09 Dec 2025 00:35:25 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 09 Dec 2025 00:35:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 09 Dec 2025 00:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 00:35:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 09 Dec 2025 00:35:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Dec 2025 00:35:26 GMT
USER memcache
# Tue, 09 Dec 2025 00:35:26 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 09 Dec 2025 00:35:26 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca80ecfb634d24079bf04d5695260ea9dce9f468064fb83123a71959d22b7c4`  
		Last Modified: Tue, 09 Dec 2025 00:35:51 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb90fb01769b3666ac21d77bcba16bd54161463250fa6f304710eb00d5ab5411`  
		Last Modified: Tue, 09 Dec 2025 00:35:51 GMT  
		Size: 170.4 KB (170375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be675ba49db497b747d37543689ff0b8fc0ef4398cd718c2fadd28302d88141b`  
		Last Modified: Tue, 09 Dec 2025 00:35:51 GMT  
		Size: 2.4 MB (2417005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882b9516d2a74a32203b37778b6025dc9c68a30838e1fa420559c34fe0319141`  
		Last Modified: Tue, 09 Dec 2025 00:35:51 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5cfa5b161387b536b9f8a94f199ffd006893e19e7bff82a8f1f9a7aa578a73`  
		Last Modified: Tue, 09 Dec 2025 00:35:51 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:6ea51b9da9219f68c45e3345bed106b961bce70b2c9aecbb6e1300060e04217d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f87eac26bbbb68ef23dfd63867d0415ddc04fe2567863569701f2891733279d6`

```dockerfile
```

-	Layers:
	-	`sha256:6f8bb9e427f03eea07711eb22a22462b3548d9ed3bf7b82f412aea5a623b10ff`  
		Last Modified: Tue, 09 Dec 2025 04:34:42 GMT  
		Size: 2.0 MB (2011829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1705de570678d9ecda7c8bb1da82748111d8547fb22bfbfb43fbbf41808b5b67`  
		Last Modified: Tue, 09 Dec 2025 04:34:43 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:05d76bdff41209572f5e6c4d21717d0717a794340a2bc2c086af7a863f5c19af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30627687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c785d7526540c98189bc45e1c3ad5a9862a6ed744c2b49e94165199ba9dcd7ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 10:11:36 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 18 Nov 2025 10:12:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 18 Nov 2025 10:53:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 18 Nov 2025 10:53:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 10:53:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 10:53:11 GMT
USER memcache
# Tue, 18 Nov 2025 10:53:11 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 18 Nov 2025 10:53:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f7062dea9fa0a796a2eacb7b265e4b2000be3d07bc91c20a5abc6538e5a68c`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f8a04356a93113399cb041ac377cf221db2df7d9fc3a6d630a061a923eb1e6`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 133.1 KB (133088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4bbee7a68150daca8b6b94e26e1a04551afc5a77dfb08a4e04aadc0933c456`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 2.2 MB (2219954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085465091dfa79c5f79dd2c74f56f75a8e078b89272039f8d8ed5a1d2adac41b`  
		Last Modified: Tue, 18 Nov 2025 10:54:06 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea3aae46e46f60ca268fd3c445c8b9ed827d7daba7e6d611310cfc9dc4d5291`  
		Last Modified: Tue, 18 Nov 2025 10:54:07 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:7a8af6c2848585e79b5cb65b6a760b1f78f0de3a59fb604d7a026c79f05a77b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c73002e7361572816b1c22cbb73aced8ce908f6492f2b5d15371b7c0a0514546`

```dockerfile
```

-	Layers:
	-	`sha256:059e3337eaf5c7461d584e0f4b5c7c660bf41a1bb79e90aa917a3992eba4c855`  
		Last Modified: Tue, 18 Nov 2025 16:35:44 GMT  
		Size: 2.0 MB (2002192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cf39200d9e698624fc7d7abe914cab80bda5407ae30f111eb22846e8fd28bba`  
		Last Modified: Tue, 18 Nov 2025 16:35:45 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; s390x

```console
$ docker pull memcached@sha256:332c41cfc207814782dda23a2b840d653abb751f335f7f02f6b238ce79c1c08c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32290312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2be68b3a60f2d8e906983e133fcaffe03bd1a82c9acc69a3dcbe3e307d7b8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:21 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 08 Dec 2025 22:33:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:36:33 GMT
ENV MEMCACHED_VERSION=1.6.39
# Mon, 08 Dec 2025 22:36:33 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Mon, 08 Dec 2025 22:36:33 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Mon, 08 Dec 2025 22:36:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 08 Dec 2025 22:36:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:36:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 22:36:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:36:34 GMT
USER memcache
# Mon, 08 Dec 2025 22:36:34 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 08 Dec 2025 22:36:34 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc040aa39039515a9f8b38dc90047178bd8fa0d8234856954f045f05050e52c`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e235f00f3da465d44b7ac18782958812c19e974f091dedfc097442ba632a3d`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 140.5 KB (140505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284c7cc2b7cc68de54eb5bce5de02ed5229cb403476e794b8066eee16babb6e1`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 2.3 MB (2313897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5059135976f7ec26a104b2fb6340b0ae8adc5756ea159deede93c8532613fd24`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd63939e0e5898afa1d51d59354c263e9a7ebfba3e418395baf21445315251de`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:8a7be7ae9cfd628f1585c887ce286f74e97f7780cc20009ffe07f9c92623b34c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c6fbc39d1b80ba4ed6852329a8ddfcaaeed5500129f5019fbc5a8904a7cd659`

```dockerfile
```

-	Layers:
	-	`sha256:0a66a7a3c4891f559fc098f2c13e48d32804e22f559857d3c89074b829300c25`  
		Last Modified: Tue, 09 Dec 2025 01:35:26 GMT  
		Size: 2.0 MB (2009665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24d3a4bbcde50a51a341ad980cc2d92d652ec5f9394c80d55c8a70ded47d8927`  
		Last Modified: Tue, 09 Dec 2025 01:35:27 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json
