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
-	[`memcached:1.6.41`](#memcached1641)
-	[`memcached:1.6.41-alpine`](#memcached1641-alpine)
-	[`memcached:1.6.41-alpine3.23`](#memcached1641-alpine323)
-	[`memcached:1.6.41-trixie`](#memcached1641-trixie)
-	[`memcached:alpine`](#memcachedalpine)
-	[`memcached:alpine3.23`](#memcachedalpine323)
-	[`memcached:latest`](#memcachedlatest)
-	[`memcached:trixie`](#memcachedtrixie)

## `memcached:1`

```console
$ docker pull memcached@sha256:f7a252e7ba3fbbe9672c483354c5081d02b780122c3bb97bd311d5662b54d0ad
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
$ docker pull memcached@sha256:5f9197399e5aefcabef61b7c94d4e9578698e4a0ac391f6a4b34eb0dcd493df2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32198719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5474f3cc4ab6f46b8613ec8b77a7c6ec75f3b8944c8674fa5c02be437ee6567b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:22:04 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 19:22:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:24:53 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 19:24:53 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 19:24:53 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 19:24:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 19:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:24:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:24:54 GMT
USER memcache
# Fri, 08 May 2026 19:24:54 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 19:24:54 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95946911721deafff321fd508db9ba36e3babc47097ecd6c6bdf2ba0dd470257`  
		Last Modified: Fri, 08 May 2026 19:24:59 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2951237283f3070819f0121ee72d97873d9e5287f4ff5cd5b450147eb57c72`  
		Last Modified: Fri, 08 May 2026 19:24:59 GMT  
		Size: 136.7 KB (136676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f29d81d44c4b3a8bb7866171f79f5054acda551367bbcf5ae523080623b437d`  
		Last Modified: Fri, 08 May 2026 19:25:00 GMT  
		Size: 2.3 MB (2280301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb056d99db8480655d7742fb357ad1bd6de6b78556d46d005628eb93210eecf4`  
		Last Modified: Fri, 08 May 2026 19:24:59 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de908d42b697f6622dffc88cdd09d0a1ddb3127cbabf42fa000970465a9e1f8`  
		Last Modified: Fri, 08 May 2026 19:25:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:34e381cf324225b9dee5ca26f3ecb0ccc5f1f460edfde42459740d7a519e0328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1bcfe0acd4621e7447b151a6a20f2248402d84d7ff8d93c46b90f669ab88e2e`

```dockerfile
```

-	Layers:
	-	`sha256:4ddea0123ac32de5d1b564e296f88cb637634e258c91e4381b8bee9b175654bb`  
		Last Modified: Fri, 08 May 2026 19:25:00 GMT  
		Size: 2.0 MB (2008326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72b234be41aa76eb975368e76c3a352a83f7b9e17ea4311b77d264ba3245480f`  
		Last Modified: Fri, 08 May 2026 19:24:59 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v5

```console
$ docker pull memcached@sha256:9bb2e143dc3647a49e4e8f85d5c418bca9b08ce1c1765c5ad7f32f5ab3d8596f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30305327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1b9575bad28b94e1186f365ab00d1a786bf0e90cc8fb820378cf08aa68513b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:25:56 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 20:26:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:29:16 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 20:29:16 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 20:29:16 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 20:29:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 20:29:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:29:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 20:29:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 20:29:16 GMT
USER memcache
# Fri, 08 May 2026 20:29:16 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 20:29:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8f774e9b92b540806fc05167db7ce09a3e1b12abdb9d496f7b8c82138656065a`  
		Last Modified: Fri, 08 May 2026 18:33:49 GMT  
		Size: 27.9 MB (27948200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b5f67bec55f95884a3889baf69e54663718d70194c4ad200c3189a69ed4f77`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0bc2199b80394dc4c86e2ec47bb2bacfa524afadd19cd9436e2cde86accf84b`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 144.2 KB (144163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652d72e4ec6b0cb1a3ca6f0de801f39fbe579385f24fdf2fa903d000df01ef7e`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 2.2 MB (2211447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e003813362a92e41a38ce899360dfc51977add71013d1cac48643e6d9361ec43`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b9b40076d0562644d2bec445a0a7fdefbf4dd5d545c7d8cbdfef18f171b99a`  
		Last Modified: Fri, 08 May 2026 20:29:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:d83c846fc98d19ba355a9a5d1c59147c565e7894fed7c5b582bd5b4bde92d90d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6056bef38756043ff8218f82594c154e80dc8d2097dd770a7bd7bb09a8e6e3e6`

```dockerfile
```

-	Layers:
	-	`sha256:4b4fd92902f7c83c67f43e813275bc5676ec6370639df11fe1394ce7fa7eef2d`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 2.0 MB (2011329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d8b1829f761528fa20afdac852bde73a128edf4c6f11e990f7e7c7fcbcfbf61`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v7

```console
$ docker pull memcached@sha256:3d1cfa4c23d23705cf3f8b9302ff26048e2ac216027f45be24e93b8f0817a952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28516943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:582f213c6b868ce82f6e14b78c661812d0781e91331e3ca32ce462777a0529fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:16:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 19:16:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:19:15 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 19:19:15 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 19:19:15 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 19:19:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 19:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:19:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:19:15 GMT
USER memcache
# Fri, 08 May 2026 19:19:15 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 19:19:15 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f1433620eadfdfe016c8054b954f619ae5bca159f35a9459c36a76d9ef4d39c3`  
		Last Modified: Fri, 08 May 2026 18:37:58 GMT  
		Size: 26.2 MB (26214912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851a3dc4d05ac8ea75d436c9d8de99f7ca3c80f159cadffd985253ae10a40069`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18a5b288c05e8d152bf1530b1c4248c0ea5c08902853e0955c6838d5d418b33`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 135.4 KB (135388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff024d65a6401c67cefb240a3ef3d181382530d66cfbb03f13ff32d81500525`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 2.2 MB (2165127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0613bb171f6d5dee88871aafa9a91daf991e3d262feb8682aa8fb5696046579`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c1a297997b8b44cdcad29c590e65efa7934da84dacae1fbddd2b017bb0dd03`  
		Last Modified: Fri, 08 May 2026 19:19:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:e7210267977b9ce03df4bc38f1d1ea5760217f9f582f392ac648876a13580041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120a3ae5c0ce21313dc99a5a24a7d9ae48f434e40717325fda7675fc368c3a9e`

```dockerfile
```

-	Layers:
	-	`sha256:b2f6d69af7f79690357135d68c570ab105358d093cb3ef2b6b37d8c0c4b8766a`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 2.0 MB (2009786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19ecae093d7ef811fe61bf6ed6706bf88a86ab363852e511e19d077fea8bdf22`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:4a47319c5ea763766ec14f7f49c71294e7621973dbf1d934330b273a50d86ae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32560787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea04a0e8415a1e901722a2dc626f036034b99c11dd819b6aab54fe2172610825`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:21:07 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 19:21:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:24:08 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 19:24:08 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 19:24:08 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 19:24:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 19:24:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:24:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:24:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:24:08 GMT
USER memcache
# Fri, 08 May 2026 19:24:08 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 19:24:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73f16d12b26b60a37ae242c9f12503fa0bb655f780014ce964bf39b960ea39a`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f45dfab4b00618ca4983d73b6acabb6fe1e056339b0cafcc1c0268303c02b89`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 153.5 KB (153496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91da4495c7aeb14802d9e2f3854b2226395b2886efcb91a3f91778774632602`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 2.3 MB (2262131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91f17f562e485ed0d6523251b77ca57f1df60d00243de97a13459b077fb30df`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70d0b5c5805a6bd639b55f25e9fb45c11035876f9fca3e2ab607fb2d818b01f`  
		Last Modified: Fri, 08 May 2026 19:24:15 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:003da519f1303287f7dbac93d59fd8f7cd3bd4f7c1c3f59e2ea25f3e1933a4a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b34e9510fcd3b35da3965f941f9c4d3bdf0eff1c30985a7ce5621b638e4c237e`

```dockerfile
```

-	Layers:
	-	`sha256:6041a557446d392656291f000150951d92c8392a387515be5c7e384d175a1967`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 2.0 MB (2008642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e39754d938ea3671f3babce3fbab5d612247a51cbc9f172de306c3fcf60e3a1b`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:ae0c2a4ef3d5a1336f8204efdb14230b37402d5f8c4096295ddd0f53b7e041ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33670271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d71af2d7fff4e8bb864857f69883ac131a512bb9311bb23de7031cb892e38a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:17:17 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 19:17:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:20:22 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 19:20:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 19:20:22 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 19:20:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 19:20:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:20:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:20:22 GMT
USER memcache
# Fri, 08 May 2026 19:20:22 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 19:20:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:43e2ffbaa23260ffb4e3de716920f2ed9e6af56e465ca1233a2d84c2cc1cf005`  
		Last Modified: Fri, 08 May 2026 18:32:48 GMT  
		Size: 31.3 MB (31296400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2ce2fa16a9ab3457f94c9628fc05a5fd6d54e5d6d3d8a9e1e506ba4e5a37aa`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540be255286e8d861d09681ddd0cd64a25a1b5fa161cca9b859487c03bfb0b6e`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 147.5 KB (147521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913676b9d51d935a10d363087959dec4494fbae5fdf82b80b84e9ecaae370ad3`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 2.2 MB (2224836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224690b120957a082d3ef84ebd501af44b1437fdbf4fcefad6e8faee78e234a5`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d0c777c8b52f9e74da7bf3fd5be45dbd51ab10be8dde37fea12fc96f59cd09`  
		Last Modified: Fri, 08 May 2026 19:20:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:15a21e26469f168e5a065467f48dfed23a1a06d5e0d2b6ffdfcfcc38ff62a560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c3412186834b790b4fbbad4cfe5adfd0f39d11688631b5059120339ee474dc`

```dockerfile
```

-	Layers:
	-	`sha256:ffb482f3d82d9bd4136d15e9b8e08adece9f35076c719e0288e1de86156221e4`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 2.0 MB (2005483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe947a7402c9e03fc064053a531c1cecc9c253a0235c40625608b22c9a860d2f`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:fb4333344bfd32af4cefd042b89dff6ea8ba4bc5ab8168cbe3d29f8c9da5566a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36164277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d865655c5194d1b0446688e3b4f406d0d233869ddf3dcc2b4863b7a8721f32f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:35:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 20:35:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:38:30 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 20:38:30 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 20:38:30 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 20:38:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 20:38:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:38:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 20:38:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 20:38:31 GMT
USER memcache
# Fri, 08 May 2026 20:38:31 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 20:38:31 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2805acf219c32faae551498121eb47f3d7d32bc2a908969bd1ac04c3f49017fe`  
		Last Modified: Fri, 08 May 2026 20:38:41 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278e7e1caa6b74657254421ed3e5193837e9b6f3dde9e041e7e95383e6e68443`  
		Last Modified: Fri, 08 May 2026 20:38:42 GMT  
		Size: 170.4 KB (170351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df05fb319f87f70759df5de69b2f40702ca122c47d614f2f8861ce256eb0b61`  
		Last Modified: Fri, 08 May 2026 20:38:42 GMT  
		Size: 2.4 MB (2394326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f6a1fd9b6e9a261288b936182122f173180b726d490646ee6164ae5c95d84c`  
		Last Modified: Fri, 08 May 2026 20:38:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b93469fb91621a5f46b7dd80327995f9ca6d8361137dbe55159ef455e2976c`  
		Last Modified: Fri, 08 May 2026 20:38:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:e82c5b578718de9c7774bc11902f22157b7c49e1a253ddfe0e3496d4a461d760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89bf5432c3d996440e1d10de68af644b31627fdeeac778ee395c95a88263010a`

```dockerfile
```

-	Layers:
	-	`sha256:8a5017f90fa8e1dd648f24d4c3fa871a8dc77b8e529fe26ee3f0034a79bdd955`  
		Last Modified: Fri, 08 May 2026 20:38:42 GMT  
		Size: 2.0 MB (2011927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e26de34ce99baa5e3d603d8a2dddfc874c4b7cf85ae36baf53e81232916879a8`  
		Last Modified: Fri, 08 May 2026 20:38:41 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; riscv64

```console
$ docker pull memcached@sha256:5ddab235954c3cde3c815b6a5be674885381502972ebc53794c4811df335843c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30623277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b6d17550b0133cd405553af720539d51b95b0d50475bbcdbf6c2173bd5280b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 16:09:52 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 09 May 2026 16:10:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 16:23:27 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 09 May 2026 16:23:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 09 May 2026 16:23:27 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 09 May 2026 16:23:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 09 May 2026 16:23:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 09 May 2026 16:23:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 09 May 2026 16:23:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 09 May 2026 16:23:28 GMT
USER memcache
# Sat, 09 May 2026 16:23:28 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 09 May 2026 16:23:28 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1e9edef871271ebe58c5a713c7c062e88ff414be0976a2c7baf0aba83823c954`  
		Last Modified: Fri, 08 May 2026 20:38:39 GMT  
		Size: 28.3 MB (28280232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9888105b7154ad185e8f5227e002ba1af0f905cba713450e54261fb929e80afe`  
		Last Modified: Sat, 09 May 2026 16:24:13 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea9dc216a8ac7e5ff5123e9cec2e0c1650d9afc96015312e8f304adc6c255a0`  
		Last Modified: Sat, 09 May 2026 16:24:13 GMT  
		Size: 133.1 KB (133086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e544f8419fe19b80d411a515c9201c8c35d068e9a3ff1127e23e53c495a036c9`  
		Last Modified: Sat, 09 May 2026 16:24:13 GMT  
		Size: 2.2 MB (2208450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b939f3eba847b32e2c08af32b5870190d0195179c8dfcfba89b9abd0d24865b8`  
		Last Modified: Sat, 09 May 2026 16:24:13 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0a4092dbf93f8a2db331d4bb00d34313567e7245e5753310064f99299a2919`  
		Last Modified: Sat, 09 May 2026 16:24:14 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:84361ecaeb53a4b02619fac3c96e92f016548a953b0bb4909dbce2605c50c27e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e712edaa1f4a23a51ec2552dadfb1ba38310fc63ac1066e30c4ccd5f2d388ce8`

```dockerfile
```

-	Layers:
	-	`sha256:b27196635d6011055da056ccc202d4d6df3c0d9296b913ab5b40505f5efb56b9`  
		Last Modified: Sat, 09 May 2026 16:24:13 GMT  
		Size: 2.0 MB (2002290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f31718fda9bdd1f0330201f0a2069f169fd2f79967b828cb3138dad392f06e0d`  
		Last Modified: Sat, 09 May 2026 16:24:12 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:7f194d0409eee2a5b0bb8903485384802c30d3e8f3db4edc714dccedd365197b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32280599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71da9b051066a3ea5be228e76446413fcc99d1b892a8e007445d21d95254a5d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:18:08 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 19:18:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:21:32 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 19:21:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 19:21:32 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 19:21:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 19:21:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:21:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:21:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:21:32 GMT
USER memcache
# Fri, 08 May 2026 19:21:32 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 19:21:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875e7d47d55cac3b3811a3503e8330c2b49b3264583a0e3ffbc8380fe58dd8d3`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e487f7a355c714fc8533d060a278791698afaed2353417768b8f02bd7844e06`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 140.5 KB (140519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6bb469173a6734f9ba49a4aa2f9a1d3e6513740633df30a2d3bc37c3b9d4279`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 2.3 MB (2298219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7e59c6d93f04c1f009cbda35d2e5b25d8087cadff3126c5de7636d0c10b5c0`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa99c508f7dc7874b69603543390bb5c9a5b3bb0689bde04f6d7d53db1ce25bd`  
		Last Modified: Fri, 08 May 2026 19:21:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:b257f9c0883422f85a5c40a24940bb3401de8aac9c08bc12a87f5732d143082c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff10b6e9f782a5c6eee93b5e143ea12b75800a8ef331ebc5d73519e32464d829`

```dockerfile
```

-	Layers:
	-	`sha256:3f4b79e225835bdf97992cd4741626b92fb8ad5438feb251afbf7d6bb442a01d`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 2.0 MB (2009763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff63eebb23b55a364393e4d41fbc25ca8e9a760278a9403379c7fb549f8a1248`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:65c80b311a9601ef5ca8af3814e5cd06a9c4277ea139d80bd53da6b4d39eb46e
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
$ docker pull memcached@sha256:7b962825022657b112923d502400d5734870d5eb12c19e7f1f6585f7534a6795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5959872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b58f7e71f30daaa3f466fa31d855fddb7101e42c0c42fac520be5d1d43ec32e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:46 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:47 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:20:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:20:22 GMT
USER memcache
# Wed, 15 Apr 2026 20:20:22 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:20:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73d5ffe265b83073ce3c7211fb3c15ebbd5e7146d870d9ce69d2e7dfc493348`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cb4fdd95ced0d5a9528e97ff0f20742749cbd9ef6dc1322d13e682a7085a67`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 106.1 KB (106063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe17fc291d9444fbae93d7f45eab008318f87302c016c06e6e911c1a571a053`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 2.0 MB (1988274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1948bd131d2cbd05c6bf2962d18b15d105abee6f42f398bab3c13737537f197`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bde8ceae30a2a0890715bbc591167ee301c57d7f75023e80be460035187def`  
		Last Modified: Wed, 15 Apr 2026 20:20:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:58ed333482f8a8530c82ad7399d5917a7db85fbcdf70fc1dec55fbedcdf09253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4255278359004afd8c94db1a7fe6129fc984d0716c33665c9eca3168476fdcb`

```dockerfile
```

-	Layers:
	-	`sha256:5f47d88d89d22d065a3590d477ae130520b882176ab07e95862afb4d8b69b214`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 94.9 KB (94901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab2d532e4a6ce2f362d25c79dfaeb88d333fe6efe7c1b5b293630bf6ca292eb8`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 20.5 KB (20530 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:47a06cd0daead339b96ed90e425336a8a49a75e4e358b5ec1ea63a630720f704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3947facc9e9fae3eee283f24b611a8ae87e353b6d6447bc6f582e90f2fce3743`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:58 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:21:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:21:03 GMT
USER memcache
# Wed, 15 Apr 2026 20:21:03 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:21:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77001163fdaab47f07a85fc5bb15f3512a8cb9b9b049cec7e0c88bcbbdb5bb5d`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee1b43c0cfbf2ee56e39441933ff06803264d22918fe867d8b5ba7d5adfb9c3`  
		Last Modified: Wed, 15 Apr 2026 20:21:06 GMT  
		Size: 102.6 KB (102630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c041bfac12e599ad87749289dec9672dac36e8c0e16779f13fa695d10f2f0cc5`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 1.9 MB (1937835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2dfd492dd0f295311a0c314fae06f4b325ae22cb0e673a53e0705f3d4e0504`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671c66eac839c2f0a5b2e64d1f581069c4cdf119e784bff16540ecc94e2c2b10`  
		Last Modified: Wed, 15 Apr 2026 20:21:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2a6148a6aebb042e55781b40ed626d0c5871833be4ae8dc303af7aace07d9d60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbaadfaacfaf0e7c226b35236bb84c2268d4c6eb017efd435a3999a44edfcc77`

```dockerfile
```

-	Layers:
	-	`sha256:c68bb3ee35fc0ac716bca45cc759f3b1ff52b1d5a0acae9876eaf0aa55aa667d`  
		Last Modified: Wed, 15 Apr 2026 20:21:06 GMT  
		Size: 20.5 KB (20466 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:fb58bae12ffa00c9cbafc8bee2341b43ffdccacbde7085fa707ef6c7f2d69e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd4e85c30e4df5803b553b8a7f84084c3dae6f72531ac70fcabf7099cfa8148`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:14:38 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 21:14:39 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 21:17:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:17:34 GMT
USER memcache
# Wed, 15 Apr 2026 21:17:34 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 21:17:34 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e312136cfedda9620407d42650d0595220e60d3c40ae8853bfbdd83f392b9e6`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53697a39f37b691917c91310ac4e107308674bddcc9017e3bbc0d0134eaf4c3e`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 92.4 KB (92369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5e4be9e0df543f152c376fe2cc74b89b75585793fdbd7d12476737d386d8e1`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 1.9 MB (1896191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a083f41edf5f859feb4367eeeea0955dc9799c8202fb8a67c40915ed5b195002`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c43503b1f4f42ffc5e0e4415befe45199dec730bc26347df151298345ba640`  
		Last Modified: Wed, 15 Apr 2026 21:17:40 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7535cf6b6a140771131c2c524301d4616f34856fcd8ecbe3e52300108c49de2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d73c906894a0a3d178edd69991f310225c0daef314e6faa83a0b9adecfbeb34`

```dockerfile
```

-	Layers:
	-	`sha256:8f1fddd7d14560fb90f381b09cde9302dfc9253e6702adf28c55961d755b1ad8`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 94.3 KB (94319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fcf119d246607aa25330c4c05fe14a64cebda69b02d14507862a9f07c1404e6`  
		Last Modified: Wed, 15 Apr 2026 21:17:38 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:6d70439467a65065c52894232a3085c724da2810a9b3205130d5e434ab411e3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6288798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4be3e105216d2507b68e772f7d08d52a5076dd55fad35c29775038d05c24112`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:15:23 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:15:24 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:18:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:18:13 GMT
USER memcache
# Wed, 15 Apr 2026 20:18:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:18:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81758f5fc2e8fa13e3625f253d7c999560ac666121c026f7251dbfb919cca611`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d735737d3a0cf1eda63bd72c09f64eb679313e9c5f8a105849848bdd779e1d`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 121.8 KB (121846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ac0921d2cc2b3388e0f006a6672c5a9e1098a59e570121dde092104d845c51`  
		Last Modified: Wed, 15 Apr 2026 20:18:19 GMT  
		Size: 2.0 MB (1965733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca9cf731b18a76c3ac25cc3add219660d57516c12680d7b1f1ece282406eb82`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717a6b23dd1cd76b686bf26066af23265e0d002ed6a3e87f6aa4f79264b7da11`  
		Last Modified: Wed, 15 Apr 2026 20:18:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7e5232b868d3222e3ce2b0ee39c62f6cb294bea27456b00940fbc4e3c8c3f84d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:780bf975a24d5fdc511c857720c04cb077d64abcfe4c93ea0db7c9487c323718`

```dockerfile
```

-	Layers:
	-	`sha256:addb0f46e3b5adb674175c11fc85526d4628e24d74d210c8b00c9a945b44407c`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 94.4 KB (94355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3364e418b74b6f6ca17deec7d55783a6e1554de3783ab0a6d5e56496d935ddb0`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:80328bf779fa1494f7677b441ad1c16c2134f126e6556953deb3cfab1c4c9770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5744816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d957405dd0811f1cd15fe39563938a60c2008204d2f63ebc7e39f8989c796f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:20:45 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 22:20:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 22:23:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 22:23:32 GMT
USER memcache
# Wed, 15 Apr 2026 22:23:32 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 22:23:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0617a09eee85c2032f5596ded56b733366513074f9096177315b50dc45485e20`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c67275dbc381ac3ae0b21dda20edaf245e2ca54d6f5dc3af8805db03c17cc93`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 110.7 KB (110715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6ecb23f1f4bc89d5c315aac493f29fe7bb33061c70d926c904f4f55d374461`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 1.9 MB (1942309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e782df8f482a58603ea70ef9e04e838d044a6070c7e4cd116c90a09b917ed940`  
		Last Modified: Wed, 15 Apr 2026 22:23:38 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616df56d574e39c00ae772c6a29e2b724698048a83cc29ea17049573f9073b10`  
		Last Modified: Wed, 15 Apr 2026 22:23:38 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c726e7abf461d963e544818339e4cd12fd2f31e41436475f0e51818a0885fbdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12e41b9d6f745d686c2649255bd14fe4e0b97a3477d383e719490e5ef66b27ae`

```dockerfile
```

-	Layers:
	-	`sha256:b44003cd1ea209090a063c5abfb4ee881849abba47e8711191b7637f86d8ee8b`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 94.9 KB (94856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f431de53d9b6c7e2cbc847af9daec064d061f8bd625615734012051336c495a`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 20.5 KB (20472 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:8182e35a9a404f0b522cb3c176d3dc4aade974e5556184c0a5a19e800721868a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6034321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c6f532e81b50ea71c3520a80da0c8154b4cb14ebc17f87eb3a026862b47ed8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:43 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:20:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:20:22 GMT
USER memcache
# Wed, 15 Apr 2026 20:20:22 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:20:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee88d1c88fa46aa906a297c2919c9a085e74d04f20e4f827ca240a20f10ad34`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c574329cc1ebf156e2d89ab608bd58a3c0db550845c0ec394d265aa98fc5c4`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 126.3 KB (126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2a28510bcba91734e7b38682847296011b63458db8a87a4bcecd180b8de7b5`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 2.1 MB (2075767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c524eb15ef0a41bf969efc93ef579db92dc59e8df57c9abfd099e7f6ff0756`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bde8ceae30a2a0890715bbc591167ee301c57d7f75023e80be460035187def`  
		Last Modified: Wed, 15 Apr 2026 20:20:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:4051408ef6c5bf4d4f37abf19c13f0298d8baa81770fcbfb588221e49e3bb834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec3a4d49e6f325e484db43c9c9981f4eaa0223d9ae98282d95c3ee20c2089cb`

```dockerfile
```

-	Layers:
	-	`sha256:0e4e65db585f857844a67a831eb876dbb0a8a40d9269393d6c0fa83a2df995ae`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 94.3 KB (94308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50f58ec8aff3c96cc7b58e689122c27ee26121c598034cdc59ec95fd6423effe`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:f3209d1ca2c4ce827614d16445231d96372944d218f18fd22850eec83874e5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5772332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e30170e0826b89d0ca59ffcae54b850ded07e6ae9451ecf1fd60f3ca8adcc725`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 00:00:48 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 16 Apr 2026 00:00:52 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Thu, 16 Apr 2026 00:14:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 16 Apr 2026 00:14:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Apr 2026 00:14:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 16 Apr 2026 00:14:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Apr 2026 00:14:22 GMT
USER memcache
# Thu, 16 Apr 2026 00:14:22 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 16 Apr 2026 00:14:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62b143e34f5b89277e3a88ed4d722339d188a094d4bb534e222ca80e7741031`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfff7c64f831ba03c491874cdf9a1c3f42bff72bb0e1951c63d8cf718854cff`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 108.9 KB (108903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69aef1050272a61cfbfd97c041d3776f96bdd03b102f2c3c54bbb0af2e1235a5`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 2.1 MB (2074414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ce340fb37f86db0d3aa774c23880b7c8322d2af8e3adc27a6ffa25d67c2122`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e40c6fb92d819994d38fae7accdffd583465eb6e645834b66f3ce9f0562f69`  
		Last Modified: Thu, 16 Apr 2026 00:14:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2caae198d1efb7d4df14da45a3ff360a697982b544a61a3f907076b414983ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1503bd38f4b30bc91be18dd93359e7376a9da1c7cb652ade64efd154064543fe`

```dockerfile
```

-	Layers:
	-	`sha256:e2d79fb634d76e28f055ab09953f59c371b93599e2b79f20f3d758f2c9520118`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 94.3 KB (94304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3614ad9b1715c3d6aa488496fca74d7143ea095d227f599407c933c62ec266aa`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 20.6 KB (20604 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:1da27660ae89a83aaf603e1affd51be573e5b8dac6c07ed592aee2a3a2b20581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5859702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13aa64df69a308e46b054bbd8e7a5d2f1e079005771f61748dae0d049889ba7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:14:40 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:14:41 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:17:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:17:58 GMT
USER memcache
# Wed, 15 Apr 2026 20:17:58 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:17:58 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c42733e5f451590186b9b76c4b374ae5a84b657f7f1fd405647f5ba82c65bcd`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a14431ac88e8fe205b07f09b7e4843bb254de41cbc044725d6eaee3c2f822f`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 114.3 KB (114293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6377b7d98f32173cd47682aa73b32e4eba42781fa9224b9eb7a6f87367d37f94`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 2.0 MB (2017525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d022ae992296922747a4b69694b0185a0ce1f6cdece7f794e39e74dab92d250`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255cb3a435cbd623c1235d0429160faf72c244a6c1a613525df36f58a8c1f784`  
		Last Modified: Wed, 15 Apr 2026 20:18:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:531ee140f06db77d73b71bce7339abec3c6d976092bb80542bb337bb406acdbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b17d6f7e71efe3ee05ebcdb8ae90c28cf60db9ef069b0a98fe442c949740a6c`

```dockerfile
```

-	Layers:
	-	`sha256:820a080f49bf9e33948dbe5c13f6254f135d90bcb2b2277e3d2fd2430626c1a2`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 94.2 KB (94250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8ab82f4f240f46f9e34b74691925ab4af7f1cbb12ad3cb8639e0f317cf06653`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine3.23`

```console
$ docker pull memcached@sha256:65c80b311a9601ef5ca8af3814e5cd06a9c4277ea139d80bd53da6b4d39eb46e
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
$ docker pull memcached@sha256:7b962825022657b112923d502400d5734870d5eb12c19e7f1f6585f7534a6795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5959872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b58f7e71f30daaa3f466fa31d855fddb7101e42c0c42fac520be5d1d43ec32e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:46 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:47 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:20:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:20:22 GMT
USER memcache
# Wed, 15 Apr 2026 20:20:22 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:20:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73d5ffe265b83073ce3c7211fb3c15ebbd5e7146d870d9ce69d2e7dfc493348`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cb4fdd95ced0d5a9528e97ff0f20742749cbd9ef6dc1322d13e682a7085a67`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 106.1 KB (106063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe17fc291d9444fbae93d7f45eab008318f87302c016c06e6e911c1a571a053`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 2.0 MB (1988274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1948bd131d2cbd05c6bf2962d18b15d105abee6f42f398bab3c13737537f197`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bde8ceae30a2a0890715bbc591167ee301c57d7f75023e80be460035187def`  
		Last Modified: Wed, 15 Apr 2026 20:20:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:58ed333482f8a8530c82ad7399d5917a7db85fbcdf70fc1dec55fbedcdf09253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4255278359004afd8c94db1a7fe6129fc984d0716c33665c9eca3168476fdcb`

```dockerfile
```

-	Layers:
	-	`sha256:5f47d88d89d22d065a3590d477ae130520b882176ab07e95862afb4d8b69b214`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 94.9 KB (94901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab2d532e4a6ce2f362d25c79dfaeb88d333fe6efe7c1b5b293630bf6ca292eb8`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 20.5 KB (20530 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; arm variant v6

```console
$ docker pull memcached@sha256:47a06cd0daead339b96ed90e425336a8a49a75e4e358b5ec1ea63a630720f704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3947facc9e9fae3eee283f24b611a8ae87e353b6d6447bc6f582e90f2fce3743`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:58 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:21:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:21:03 GMT
USER memcache
# Wed, 15 Apr 2026 20:21:03 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:21:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77001163fdaab47f07a85fc5bb15f3512a8cb9b9b049cec7e0c88bcbbdb5bb5d`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee1b43c0cfbf2ee56e39441933ff06803264d22918fe867d8b5ba7d5adfb9c3`  
		Last Modified: Wed, 15 Apr 2026 20:21:06 GMT  
		Size: 102.6 KB (102630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c041bfac12e599ad87749289dec9672dac36e8c0e16779f13fa695d10f2f0cc5`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 1.9 MB (1937835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2dfd492dd0f295311a0c314fae06f4b325ae22cb0e673a53e0705f3d4e0504`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671c66eac839c2f0a5b2e64d1f581069c4cdf119e784bff16540ecc94e2c2b10`  
		Last Modified: Wed, 15 Apr 2026 20:21:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:2a6148a6aebb042e55781b40ed626d0c5871833be4ae8dc303af7aace07d9d60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbaadfaacfaf0e7c226b35236bb84c2268d4c6eb017efd435a3999a44edfcc77`

```dockerfile
```

-	Layers:
	-	`sha256:c68bb3ee35fc0ac716bca45cc759f3b1ff52b1d5a0acae9876eaf0aa55aa667d`  
		Last Modified: Wed, 15 Apr 2026 20:21:06 GMT  
		Size: 20.5 KB (20466 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; arm variant v7

```console
$ docker pull memcached@sha256:fb58bae12ffa00c9cbafc8bee2341b43ffdccacbde7085fa707ef6c7f2d69e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd4e85c30e4df5803b553b8a7f84084c3dae6f72531ac70fcabf7099cfa8148`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:14:38 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 21:14:39 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 21:17:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:17:34 GMT
USER memcache
# Wed, 15 Apr 2026 21:17:34 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 21:17:34 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e312136cfedda9620407d42650d0595220e60d3c40ae8853bfbdd83f392b9e6`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53697a39f37b691917c91310ac4e107308674bddcc9017e3bbc0d0134eaf4c3e`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 92.4 KB (92369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5e4be9e0df543f152c376fe2cc74b89b75585793fdbd7d12476737d386d8e1`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 1.9 MB (1896191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a083f41edf5f859feb4367eeeea0955dc9799c8202fb8a67c40915ed5b195002`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c43503b1f4f42ffc5e0e4415befe45199dec730bc26347df151298345ba640`  
		Last Modified: Wed, 15 Apr 2026 21:17:40 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:7535cf6b6a140771131c2c524301d4616f34856fcd8ecbe3e52300108c49de2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d73c906894a0a3d178edd69991f310225c0daef314e6faa83a0b9adecfbeb34`

```dockerfile
```

-	Layers:
	-	`sha256:8f1fddd7d14560fb90f381b09cde9302dfc9253e6702adf28c55961d755b1ad8`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 94.3 KB (94319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fcf119d246607aa25330c4c05fe14a64cebda69b02d14507862a9f07c1404e6`  
		Last Modified: Wed, 15 Apr 2026 21:17:38 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:6d70439467a65065c52894232a3085c724da2810a9b3205130d5e434ab411e3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6288798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4be3e105216d2507b68e772f7d08d52a5076dd55fad35c29775038d05c24112`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:15:23 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:15:24 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:18:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:18:13 GMT
USER memcache
# Wed, 15 Apr 2026 20:18:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:18:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81758f5fc2e8fa13e3625f253d7c999560ac666121c026f7251dbfb919cca611`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d735737d3a0cf1eda63bd72c09f64eb679313e9c5f8a105849848bdd779e1d`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 121.8 KB (121846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ac0921d2cc2b3388e0f006a6672c5a9e1098a59e570121dde092104d845c51`  
		Last Modified: Wed, 15 Apr 2026 20:18:19 GMT  
		Size: 2.0 MB (1965733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca9cf731b18a76c3ac25cc3add219660d57516c12680d7b1f1ece282406eb82`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717a6b23dd1cd76b686bf26066af23265e0d002ed6a3e87f6aa4f79264b7da11`  
		Last Modified: Wed, 15 Apr 2026 20:18:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:7e5232b868d3222e3ce2b0ee39c62f6cb294bea27456b00940fbc4e3c8c3f84d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:780bf975a24d5fdc511c857720c04cb077d64abcfe4c93ea0db7c9487c323718`

```dockerfile
```

-	Layers:
	-	`sha256:addb0f46e3b5adb674175c11fc85526d4628e24d74d210c8b00c9a945b44407c`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 94.4 KB (94355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3364e418b74b6f6ca17deec7d55783a6e1554de3783ab0a6d5e56496d935ddb0`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; 386

```console
$ docker pull memcached@sha256:80328bf779fa1494f7677b441ad1c16c2134f126e6556953deb3cfab1c4c9770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5744816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d957405dd0811f1cd15fe39563938a60c2008204d2f63ebc7e39f8989c796f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:20:45 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 22:20:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 22:23:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 22:23:32 GMT
USER memcache
# Wed, 15 Apr 2026 22:23:32 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 22:23:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0617a09eee85c2032f5596ded56b733366513074f9096177315b50dc45485e20`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c67275dbc381ac3ae0b21dda20edaf245e2ca54d6f5dc3af8805db03c17cc93`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 110.7 KB (110715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6ecb23f1f4bc89d5c315aac493f29fe7bb33061c70d926c904f4f55d374461`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 1.9 MB (1942309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e782df8f482a58603ea70ef9e04e838d044a6070c7e4cd116c90a09b917ed940`  
		Last Modified: Wed, 15 Apr 2026 22:23:38 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616df56d574e39c00ae772c6a29e2b724698048a83cc29ea17049573f9073b10`  
		Last Modified: Wed, 15 Apr 2026 22:23:38 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:c726e7abf461d963e544818339e4cd12fd2f31e41436475f0e51818a0885fbdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12e41b9d6f745d686c2649255bd14fe4e0b97a3477d383e719490e5ef66b27ae`

```dockerfile
```

-	Layers:
	-	`sha256:b44003cd1ea209090a063c5abfb4ee881849abba47e8711191b7637f86d8ee8b`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 94.9 KB (94856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f431de53d9b6c7e2cbc847af9daec064d061f8bd625615734012051336c495a`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 20.5 KB (20472 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; ppc64le

```console
$ docker pull memcached@sha256:8182e35a9a404f0b522cb3c176d3dc4aade974e5556184c0a5a19e800721868a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6034321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c6f532e81b50ea71c3520a80da0c8154b4cb14ebc17f87eb3a026862b47ed8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:43 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:20:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:20:22 GMT
USER memcache
# Wed, 15 Apr 2026 20:20:22 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:20:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee88d1c88fa46aa906a297c2919c9a085e74d04f20e4f827ca240a20f10ad34`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c574329cc1ebf156e2d89ab608bd58a3c0db550845c0ec394d265aa98fc5c4`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 126.3 KB (126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2a28510bcba91734e7b38682847296011b63458db8a87a4bcecd180b8de7b5`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 2.1 MB (2075767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c524eb15ef0a41bf969efc93ef579db92dc59e8df57c9abfd099e7f6ff0756`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bde8ceae30a2a0890715bbc591167ee301c57d7f75023e80be460035187def`  
		Last Modified: Wed, 15 Apr 2026 20:20:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:4051408ef6c5bf4d4f37abf19c13f0298d8baa81770fcbfb588221e49e3bb834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec3a4d49e6f325e484db43c9c9981f4eaa0223d9ae98282d95c3ee20c2089cb`

```dockerfile
```

-	Layers:
	-	`sha256:0e4e65db585f857844a67a831eb876dbb0a8a40d9269393d6c0fa83a2df995ae`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 94.3 KB (94308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50f58ec8aff3c96cc7b58e689122c27ee26121c598034cdc59ec95fd6423effe`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; riscv64

```console
$ docker pull memcached@sha256:f3209d1ca2c4ce827614d16445231d96372944d218f18fd22850eec83874e5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5772332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e30170e0826b89d0ca59ffcae54b850ded07e6ae9451ecf1fd60f3ca8adcc725`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 00:00:48 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 16 Apr 2026 00:00:52 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Thu, 16 Apr 2026 00:14:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 16 Apr 2026 00:14:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Apr 2026 00:14:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 16 Apr 2026 00:14:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Apr 2026 00:14:22 GMT
USER memcache
# Thu, 16 Apr 2026 00:14:22 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 16 Apr 2026 00:14:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62b143e34f5b89277e3a88ed4d722339d188a094d4bb534e222ca80e7741031`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfff7c64f831ba03c491874cdf9a1c3f42bff72bb0e1951c63d8cf718854cff`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 108.9 KB (108903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69aef1050272a61cfbfd97c041d3776f96bdd03b102f2c3c54bbb0af2e1235a5`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 2.1 MB (2074414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ce340fb37f86db0d3aa774c23880b7c8322d2af8e3adc27a6ffa25d67c2122`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e40c6fb92d819994d38fae7accdffd583465eb6e645834b66f3ce9f0562f69`  
		Last Modified: Thu, 16 Apr 2026 00:14:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:2caae198d1efb7d4df14da45a3ff360a697982b544a61a3f907076b414983ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1503bd38f4b30bc91be18dd93359e7376a9da1c7cb652ade64efd154064543fe`

```dockerfile
```

-	Layers:
	-	`sha256:e2d79fb634d76e28f055ab09953f59c371b93599e2b79f20f3d758f2c9520118`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 94.3 KB (94304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3614ad9b1715c3d6aa488496fca74d7143ea095d227f599407c933c62ec266aa`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 20.6 KB (20604 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; s390x

```console
$ docker pull memcached@sha256:1da27660ae89a83aaf603e1affd51be573e5b8dac6c07ed592aee2a3a2b20581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5859702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13aa64df69a308e46b054bbd8e7a5d2f1e079005771f61748dae0d049889ba7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:14:40 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:14:41 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:17:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:17:58 GMT
USER memcache
# Wed, 15 Apr 2026 20:17:58 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:17:58 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c42733e5f451590186b9b76c4b374ae5a84b657f7f1fd405647f5ba82c65bcd`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a14431ac88e8fe205b07f09b7e4843bb254de41cbc044725d6eaee3c2f822f`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 114.3 KB (114293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6377b7d98f32173cd47682aa73b32e4eba42781fa9224b9eb7a6f87367d37f94`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 2.0 MB (2017525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d022ae992296922747a4b69694b0185a0ce1f6cdece7f794e39e74dab92d250`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255cb3a435cbd623c1235d0429160faf72c244a6c1a613525df36f58a8c1f784`  
		Last Modified: Wed, 15 Apr 2026 20:18:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:531ee140f06db77d73b71bce7339abec3c6d976092bb80542bb337bb406acdbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b17d6f7e71efe3ee05ebcdb8ae90c28cf60db9ef069b0a98fe442c949740a6c`

```dockerfile
```

-	Layers:
	-	`sha256:820a080f49bf9e33948dbe5c13f6254f135d90bcb2b2277e3d2fd2430626c1a2`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 94.2 KB (94250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8ab82f4f240f46f9e34b74691925ab4af7f1cbb12ad3cb8639e0f317cf06653`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-trixie`

```console
$ docker pull memcached@sha256:f7a252e7ba3fbbe9672c483354c5081d02b780122c3bb97bd311d5662b54d0ad
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
$ docker pull memcached@sha256:5f9197399e5aefcabef61b7c94d4e9578698e4a0ac391f6a4b34eb0dcd493df2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32198719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5474f3cc4ab6f46b8613ec8b77a7c6ec75f3b8944c8674fa5c02be437ee6567b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:22:04 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 19:22:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:24:53 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 19:24:53 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 19:24:53 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 19:24:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 19:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:24:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:24:54 GMT
USER memcache
# Fri, 08 May 2026 19:24:54 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 19:24:54 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95946911721deafff321fd508db9ba36e3babc47097ecd6c6bdf2ba0dd470257`  
		Last Modified: Fri, 08 May 2026 19:24:59 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2951237283f3070819f0121ee72d97873d9e5287f4ff5cd5b450147eb57c72`  
		Last Modified: Fri, 08 May 2026 19:24:59 GMT  
		Size: 136.7 KB (136676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f29d81d44c4b3a8bb7866171f79f5054acda551367bbcf5ae523080623b437d`  
		Last Modified: Fri, 08 May 2026 19:25:00 GMT  
		Size: 2.3 MB (2280301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb056d99db8480655d7742fb357ad1bd6de6b78556d46d005628eb93210eecf4`  
		Last Modified: Fri, 08 May 2026 19:24:59 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de908d42b697f6622dffc88cdd09d0a1ddb3127cbabf42fa000970465a9e1f8`  
		Last Modified: Fri, 08 May 2026 19:25:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:34e381cf324225b9dee5ca26f3ecb0ccc5f1f460edfde42459740d7a519e0328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1bcfe0acd4621e7447b151a6a20f2248402d84d7ff8d93c46b90f669ab88e2e`

```dockerfile
```

-	Layers:
	-	`sha256:4ddea0123ac32de5d1b564e296f88cb637634e258c91e4381b8bee9b175654bb`  
		Last Modified: Fri, 08 May 2026 19:25:00 GMT  
		Size: 2.0 MB (2008326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72b234be41aa76eb975368e76c3a352a83f7b9e17ea4311b77d264ba3245480f`  
		Last Modified: Fri, 08 May 2026 19:24:59 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:9bb2e143dc3647a49e4e8f85d5c418bca9b08ce1c1765c5ad7f32f5ab3d8596f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30305327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1b9575bad28b94e1186f365ab00d1a786bf0e90cc8fb820378cf08aa68513b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:25:56 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 20:26:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:29:16 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 20:29:16 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 20:29:16 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 20:29:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 20:29:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:29:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 20:29:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 20:29:16 GMT
USER memcache
# Fri, 08 May 2026 20:29:16 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 20:29:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8f774e9b92b540806fc05167db7ce09a3e1b12abdb9d496f7b8c82138656065a`  
		Last Modified: Fri, 08 May 2026 18:33:49 GMT  
		Size: 27.9 MB (27948200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b5f67bec55f95884a3889baf69e54663718d70194c4ad200c3189a69ed4f77`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0bc2199b80394dc4c86e2ec47bb2bacfa524afadd19cd9436e2cde86accf84b`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 144.2 KB (144163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652d72e4ec6b0cb1a3ca6f0de801f39fbe579385f24fdf2fa903d000df01ef7e`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 2.2 MB (2211447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e003813362a92e41a38ce899360dfc51977add71013d1cac48643e6d9361ec43`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b9b40076d0562644d2bec445a0a7fdefbf4dd5d545c7d8cbdfef18f171b99a`  
		Last Modified: Fri, 08 May 2026 20:29:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:d83c846fc98d19ba355a9a5d1c59147c565e7894fed7c5b582bd5b4bde92d90d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6056bef38756043ff8218f82594c154e80dc8d2097dd770a7bd7bb09a8e6e3e6`

```dockerfile
```

-	Layers:
	-	`sha256:4b4fd92902f7c83c67f43e813275bc5676ec6370639df11fe1394ce7fa7eef2d`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 2.0 MB (2011329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d8b1829f761528fa20afdac852bde73a128edf4c6f11e990f7e7c7fcbcfbf61`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:3d1cfa4c23d23705cf3f8b9302ff26048e2ac216027f45be24e93b8f0817a952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28516943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:582f213c6b868ce82f6e14b78c661812d0781e91331e3ca32ce462777a0529fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:16:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 19:16:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:19:15 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 19:19:15 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 19:19:15 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 19:19:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 19:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:19:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:19:15 GMT
USER memcache
# Fri, 08 May 2026 19:19:15 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 19:19:15 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f1433620eadfdfe016c8054b954f619ae5bca159f35a9459c36a76d9ef4d39c3`  
		Last Modified: Fri, 08 May 2026 18:37:58 GMT  
		Size: 26.2 MB (26214912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851a3dc4d05ac8ea75d436c9d8de99f7ca3c80f159cadffd985253ae10a40069`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18a5b288c05e8d152bf1530b1c4248c0ea5c08902853e0955c6838d5d418b33`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 135.4 KB (135388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff024d65a6401c67cefb240a3ef3d181382530d66cfbb03f13ff32d81500525`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 2.2 MB (2165127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0613bb171f6d5dee88871aafa9a91daf991e3d262feb8682aa8fb5696046579`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c1a297997b8b44cdcad29c590e65efa7934da84dacae1fbddd2b017bb0dd03`  
		Last Modified: Fri, 08 May 2026 19:19:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:e7210267977b9ce03df4bc38f1d1ea5760217f9f582f392ac648876a13580041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120a3ae5c0ce21313dc99a5a24a7d9ae48f434e40717325fda7675fc368c3a9e`

```dockerfile
```

-	Layers:
	-	`sha256:b2f6d69af7f79690357135d68c570ab105358d093cb3ef2b6b37d8c0c4b8766a`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 2.0 MB (2009786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19ecae093d7ef811fe61bf6ed6706bf88a86ab363852e511e19d077fea8bdf22`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:4a47319c5ea763766ec14f7f49c71294e7621973dbf1d934330b273a50d86ae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32560787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea04a0e8415a1e901722a2dc626f036034b99c11dd819b6aab54fe2172610825`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:21:07 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 19:21:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:24:08 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 19:24:08 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 19:24:08 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 19:24:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 19:24:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:24:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:24:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:24:08 GMT
USER memcache
# Fri, 08 May 2026 19:24:08 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 19:24:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73f16d12b26b60a37ae242c9f12503fa0bb655f780014ce964bf39b960ea39a`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f45dfab4b00618ca4983d73b6acabb6fe1e056339b0cafcc1c0268303c02b89`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 153.5 KB (153496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91da4495c7aeb14802d9e2f3854b2226395b2886efcb91a3f91778774632602`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 2.3 MB (2262131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91f17f562e485ed0d6523251b77ca57f1df60d00243de97a13459b077fb30df`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70d0b5c5805a6bd639b55f25e9fb45c11035876f9fca3e2ab607fb2d818b01f`  
		Last Modified: Fri, 08 May 2026 19:24:15 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:003da519f1303287f7dbac93d59fd8f7cd3bd4f7c1c3f59e2ea25f3e1933a4a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b34e9510fcd3b35da3965f941f9c4d3bdf0eff1c30985a7ce5621b638e4c237e`

```dockerfile
```

-	Layers:
	-	`sha256:6041a557446d392656291f000150951d92c8392a387515be5c7e384d175a1967`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 2.0 MB (2008642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e39754d938ea3671f3babce3fbab5d612247a51cbc9f172de306c3fcf60e3a1b`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; 386

```console
$ docker pull memcached@sha256:ae0c2a4ef3d5a1336f8204efdb14230b37402d5f8c4096295ddd0f53b7e041ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33670271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d71af2d7fff4e8bb864857f69883ac131a512bb9311bb23de7031cb892e38a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:17:17 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 19:17:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:20:22 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 19:20:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 19:20:22 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 19:20:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 19:20:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:20:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:20:22 GMT
USER memcache
# Fri, 08 May 2026 19:20:22 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 19:20:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:43e2ffbaa23260ffb4e3de716920f2ed9e6af56e465ca1233a2d84c2cc1cf005`  
		Last Modified: Fri, 08 May 2026 18:32:48 GMT  
		Size: 31.3 MB (31296400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2ce2fa16a9ab3457f94c9628fc05a5fd6d54e5d6d3d8a9e1e506ba4e5a37aa`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540be255286e8d861d09681ddd0cd64a25a1b5fa161cca9b859487c03bfb0b6e`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 147.5 KB (147521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913676b9d51d935a10d363087959dec4494fbae5fdf82b80b84e9ecaae370ad3`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 2.2 MB (2224836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224690b120957a082d3ef84ebd501af44b1437fdbf4fcefad6e8faee78e234a5`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d0c777c8b52f9e74da7bf3fd5be45dbd51ab10be8dde37fea12fc96f59cd09`  
		Last Modified: Fri, 08 May 2026 19:20:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:15a21e26469f168e5a065467f48dfed23a1a06d5e0d2b6ffdfcfcc38ff62a560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c3412186834b790b4fbbad4cfe5adfd0f39d11688631b5059120339ee474dc`

```dockerfile
```

-	Layers:
	-	`sha256:ffb482f3d82d9bd4136d15e9b8e08adece9f35076c719e0288e1de86156221e4`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 2.0 MB (2005483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe947a7402c9e03fc064053a531c1cecc9c253a0235c40625608b22c9a860d2f`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:fb4333344bfd32af4cefd042b89dff6ea8ba4bc5ab8168cbe3d29f8c9da5566a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36164277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d865655c5194d1b0446688e3b4f406d0d233869ddf3dcc2b4863b7a8721f32f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:35:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 20:35:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:38:30 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 20:38:30 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 20:38:30 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 20:38:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 20:38:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:38:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 20:38:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 20:38:31 GMT
USER memcache
# Fri, 08 May 2026 20:38:31 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 20:38:31 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2805acf219c32faae551498121eb47f3d7d32bc2a908969bd1ac04c3f49017fe`  
		Last Modified: Fri, 08 May 2026 20:38:41 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278e7e1caa6b74657254421ed3e5193837e9b6f3dde9e041e7e95383e6e68443`  
		Last Modified: Fri, 08 May 2026 20:38:42 GMT  
		Size: 170.4 KB (170351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df05fb319f87f70759df5de69b2f40702ca122c47d614f2f8861ce256eb0b61`  
		Last Modified: Fri, 08 May 2026 20:38:42 GMT  
		Size: 2.4 MB (2394326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f6a1fd9b6e9a261288b936182122f173180b726d490646ee6164ae5c95d84c`  
		Last Modified: Fri, 08 May 2026 20:38:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b93469fb91621a5f46b7dd80327995f9ca6d8361137dbe55159ef455e2976c`  
		Last Modified: Fri, 08 May 2026 20:38:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:e82c5b578718de9c7774bc11902f22157b7c49e1a253ddfe0e3496d4a461d760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89bf5432c3d996440e1d10de68af644b31627fdeeac778ee395c95a88263010a`

```dockerfile
```

-	Layers:
	-	`sha256:8a5017f90fa8e1dd648f24d4c3fa871a8dc77b8e529fe26ee3f0034a79bdd955`  
		Last Modified: Fri, 08 May 2026 20:38:42 GMT  
		Size: 2.0 MB (2011927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e26de34ce99baa5e3d603d8a2dddfc874c4b7cf85ae36baf53e81232916879a8`  
		Last Modified: Fri, 08 May 2026 20:38:41 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:5ddab235954c3cde3c815b6a5be674885381502972ebc53794c4811df335843c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30623277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b6d17550b0133cd405553af720539d51b95b0d50475bbcdbf6c2173bd5280b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 16:09:52 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 09 May 2026 16:10:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 16:23:27 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 09 May 2026 16:23:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 09 May 2026 16:23:27 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 09 May 2026 16:23:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 09 May 2026 16:23:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 09 May 2026 16:23:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 09 May 2026 16:23:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 09 May 2026 16:23:28 GMT
USER memcache
# Sat, 09 May 2026 16:23:28 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 09 May 2026 16:23:28 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1e9edef871271ebe58c5a713c7c062e88ff414be0976a2c7baf0aba83823c954`  
		Last Modified: Fri, 08 May 2026 20:38:39 GMT  
		Size: 28.3 MB (28280232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9888105b7154ad185e8f5227e002ba1af0f905cba713450e54261fb929e80afe`  
		Last Modified: Sat, 09 May 2026 16:24:13 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea9dc216a8ac7e5ff5123e9cec2e0c1650d9afc96015312e8f304adc6c255a0`  
		Last Modified: Sat, 09 May 2026 16:24:13 GMT  
		Size: 133.1 KB (133086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e544f8419fe19b80d411a515c9201c8c35d068e9a3ff1127e23e53c495a036c9`  
		Last Modified: Sat, 09 May 2026 16:24:13 GMT  
		Size: 2.2 MB (2208450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b939f3eba847b32e2c08af32b5870190d0195179c8dfcfba89b9abd0d24865b8`  
		Last Modified: Sat, 09 May 2026 16:24:13 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0a4092dbf93f8a2db331d4bb00d34313567e7245e5753310064f99299a2919`  
		Last Modified: Sat, 09 May 2026 16:24:14 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:84361ecaeb53a4b02619fac3c96e92f016548a953b0bb4909dbce2605c50c27e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e712edaa1f4a23a51ec2552dadfb1ba38310fc63ac1066e30c4ccd5f2d388ce8`

```dockerfile
```

-	Layers:
	-	`sha256:b27196635d6011055da056ccc202d4d6df3c0d9296b913ab5b40505f5efb56b9`  
		Last Modified: Sat, 09 May 2026 16:24:13 GMT  
		Size: 2.0 MB (2002290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f31718fda9bdd1f0330201f0a2069f169fd2f79967b828cb3138dad392f06e0d`  
		Last Modified: Sat, 09 May 2026 16:24:12 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:7f194d0409eee2a5b0bb8903485384802c30d3e8f3db4edc714dccedd365197b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32280599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71da9b051066a3ea5be228e76446413fcc99d1b892a8e007445d21d95254a5d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:18:08 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 19:18:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:21:32 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 19:21:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 19:21:32 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 19:21:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 19:21:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:21:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:21:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:21:32 GMT
USER memcache
# Fri, 08 May 2026 19:21:32 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 19:21:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875e7d47d55cac3b3811a3503e8330c2b49b3264583a0e3ffbc8380fe58dd8d3`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e487f7a355c714fc8533d060a278791698afaed2353417768b8f02bd7844e06`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 140.5 KB (140519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6bb469173a6734f9ba49a4aa2f9a1d3e6513740633df30a2d3bc37c3b9d4279`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 2.3 MB (2298219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7e59c6d93f04c1f009cbda35d2e5b25d8087cadff3126c5de7636d0c10b5c0`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa99c508f7dc7874b69603543390bb5c9a5b3bb0689bde04f6d7d53db1ce25bd`  
		Last Modified: Fri, 08 May 2026 19:21:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:b257f9c0883422f85a5c40a24940bb3401de8aac9c08bc12a87f5732d143082c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff10b6e9f782a5c6eee93b5e143ea12b75800a8ef331ebc5d73519e32464d829`

```dockerfile
```

-	Layers:
	-	`sha256:3f4b79e225835bdf97992cd4741626b92fb8ad5438feb251afbf7d6bb442a01d`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 2.0 MB (2009763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff63eebb23b55a364393e4d41fbc25ca8e9a760278a9403379c7fb549f8a1248`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6`

```console
$ docker pull memcached@sha256:f7a252e7ba3fbbe9672c483354c5081d02b780122c3bb97bd311d5662b54d0ad
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
$ docker pull memcached@sha256:5f9197399e5aefcabef61b7c94d4e9578698e4a0ac391f6a4b34eb0dcd493df2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32198719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5474f3cc4ab6f46b8613ec8b77a7c6ec75f3b8944c8674fa5c02be437ee6567b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:22:04 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 19:22:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:24:53 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 19:24:53 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 19:24:53 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 19:24:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 19:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:24:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:24:54 GMT
USER memcache
# Fri, 08 May 2026 19:24:54 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 19:24:54 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95946911721deafff321fd508db9ba36e3babc47097ecd6c6bdf2ba0dd470257`  
		Last Modified: Fri, 08 May 2026 19:24:59 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2951237283f3070819f0121ee72d97873d9e5287f4ff5cd5b450147eb57c72`  
		Last Modified: Fri, 08 May 2026 19:24:59 GMT  
		Size: 136.7 KB (136676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f29d81d44c4b3a8bb7866171f79f5054acda551367bbcf5ae523080623b437d`  
		Last Modified: Fri, 08 May 2026 19:25:00 GMT  
		Size: 2.3 MB (2280301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb056d99db8480655d7742fb357ad1bd6de6b78556d46d005628eb93210eecf4`  
		Last Modified: Fri, 08 May 2026 19:24:59 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de908d42b697f6622dffc88cdd09d0a1ddb3127cbabf42fa000970465a9e1f8`  
		Last Modified: Fri, 08 May 2026 19:25:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:34e381cf324225b9dee5ca26f3ecb0ccc5f1f460edfde42459740d7a519e0328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1bcfe0acd4621e7447b151a6a20f2248402d84d7ff8d93c46b90f669ab88e2e`

```dockerfile
```

-	Layers:
	-	`sha256:4ddea0123ac32de5d1b564e296f88cb637634e258c91e4381b8bee9b175654bb`  
		Last Modified: Fri, 08 May 2026 19:25:00 GMT  
		Size: 2.0 MB (2008326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72b234be41aa76eb975368e76c3a352a83f7b9e17ea4311b77d264ba3245480f`  
		Last Modified: Fri, 08 May 2026 19:24:59 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:9bb2e143dc3647a49e4e8f85d5c418bca9b08ce1c1765c5ad7f32f5ab3d8596f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30305327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1b9575bad28b94e1186f365ab00d1a786bf0e90cc8fb820378cf08aa68513b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:25:56 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 20:26:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:29:16 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 20:29:16 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 20:29:16 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 20:29:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 20:29:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:29:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 20:29:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 20:29:16 GMT
USER memcache
# Fri, 08 May 2026 20:29:16 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 20:29:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8f774e9b92b540806fc05167db7ce09a3e1b12abdb9d496f7b8c82138656065a`  
		Last Modified: Fri, 08 May 2026 18:33:49 GMT  
		Size: 27.9 MB (27948200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b5f67bec55f95884a3889baf69e54663718d70194c4ad200c3189a69ed4f77`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0bc2199b80394dc4c86e2ec47bb2bacfa524afadd19cd9436e2cde86accf84b`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 144.2 KB (144163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652d72e4ec6b0cb1a3ca6f0de801f39fbe579385f24fdf2fa903d000df01ef7e`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 2.2 MB (2211447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e003813362a92e41a38ce899360dfc51977add71013d1cac48643e6d9361ec43`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b9b40076d0562644d2bec445a0a7fdefbf4dd5d545c7d8cbdfef18f171b99a`  
		Last Modified: Fri, 08 May 2026 20:29:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:d83c846fc98d19ba355a9a5d1c59147c565e7894fed7c5b582bd5b4bde92d90d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6056bef38756043ff8218f82594c154e80dc8d2097dd770a7bd7bb09a8e6e3e6`

```dockerfile
```

-	Layers:
	-	`sha256:4b4fd92902f7c83c67f43e813275bc5676ec6370639df11fe1394ce7fa7eef2d`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 2.0 MB (2011329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d8b1829f761528fa20afdac852bde73a128edf4c6f11e990f7e7c7fcbcfbf61`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v7

```console
$ docker pull memcached@sha256:3d1cfa4c23d23705cf3f8b9302ff26048e2ac216027f45be24e93b8f0817a952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28516943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:582f213c6b868ce82f6e14b78c661812d0781e91331e3ca32ce462777a0529fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:16:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 19:16:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:19:15 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 19:19:15 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 19:19:15 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 19:19:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 19:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:19:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:19:15 GMT
USER memcache
# Fri, 08 May 2026 19:19:15 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 19:19:15 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f1433620eadfdfe016c8054b954f619ae5bca159f35a9459c36a76d9ef4d39c3`  
		Last Modified: Fri, 08 May 2026 18:37:58 GMT  
		Size: 26.2 MB (26214912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851a3dc4d05ac8ea75d436c9d8de99f7ca3c80f159cadffd985253ae10a40069`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18a5b288c05e8d152bf1530b1c4248c0ea5c08902853e0955c6838d5d418b33`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 135.4 KB (135388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff024d65a6401c67cefb240a3ef3d181382530d66cfbb03f13ff32d81500525`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 2.2 MB (2165127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0613bb171f6d5dee88871aafa9a91daf991e3d262feb8682aa8fb5696046579`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c1a297997b8b44cdcad29c590e65efa7934da84dacae1fbddd2b017bb0dd03`  
		Last Modified: Fri, 08 May 2026 19:19:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:e7210267977b9ce03df4bc38f1d1ea5760217f9f582f392ac648876a13580041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120a3ae5c0ce21313dc99a5a24a7d9ae48f434e40717325fda7675fc368c3a9e`

```dockerfile
```

-	Layers:
	-	`sha256:b2f6d69af7f79690357135d68c570ab105358d093cb3ef2b6b37d8c0c4b8766a`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 2.0 MB (2009786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19ecae093d7ef811fe61bf6ed6706bf88a86ab363852e511e19d077fea8bdf22`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:4a47319c5ea763766ec14f7f49c71294e7621973dbf1d934330b273a50d86ae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32560787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea04a0e8415a1e901722a2dc626f036034b99c11dd819b6aab54fe2172610825`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:21:07 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 19:21:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:24:08 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 19:24:08 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 19:24:08 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 19:24:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 19:24:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:24:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:24:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:24:08 GMT
USER memcache
# Fri, 08 May 2026 19:24:08 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 19:24:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73f16d12b26b60a37ae242c9f12503fa0bb655f780014ce964bf39b960ea39a`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f45dfab4b00618ca4983d73b6acabb6fe1e056339b0cafcc1c0268303c02b89`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 153.5 KB (153496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91da4495c7aeb14802d9e2f3854b2226395b2886efcb91a3f91778774632602`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 2.3 MB (2262131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91f17f562e485ed0d6523251b77ca57f1df60d00243de97a13459b077fb30df`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70d0b5c5805a6bd639b55f25e9fb45c11035876f9fca3e2ab607fb2d818b01f`  
		Last Modified: Fri, 08 May 2026 19:24:15 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:003da519f1303287f7dbac93d59fd8f7cd3bd4f7c1c3f59e2ea25f3e1933a4a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b34e9510fcd3b35da3965f941f9c4d3bdf0eff1c30985a7ce5621b638e4c237e`

```dockerfile
```

-	Layers:
	-	`sha256:6041a557446d392656291f000150951d92c8392a387515be5c7e384d175a1967`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 2.0 MB (2008642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e39754d938ea3671f3babce3fbab5d612247a51cbc9f172de306c3fcf60e3a1b`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; 386

```console
$ docker pull memcached@sha256:ae0c2a4ef3d5a1336f8204efdb14230b37402d5f8c4096295ddd0f53b7e041ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33670271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d71af2d7fff4e8bb864857f69883ac131a512bb9311bb23de7031cb892e38a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:17:17 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 19:17:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:20:22 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 19:20:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 19:20:22 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 19:20:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 19:20:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:20:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:20:22 GMT
USER memcache
# Fri, 08 May 2026 19:20:22 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 19:20:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:43e2ffbaa23260ffb4e3de716920f2ed9e6af56e465ca1233a2d84c2cc1cf005`  
		Last Modified: Fri, 08 May 2026 18:32:48 GMT  
		Size: 31.3 MB (31296400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2ce2fa16a9ab3457f94c9628fc05a5fd6d54e5d6d3d8a9e1e506ba4e5a37aa`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540be255286e8d861d09681ddd0cd64a25a1b5fa161cca9b859487c03bfb0b6e`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 147.5 KB (147521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913676b9d51d935a10d363087959dec4494fbae5fdf82b80b84e9ecaae370ad3`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 2.2 MB (2224836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224690b120957a082d3ef84ebd501af44b1437fdbf4fcefad6e8faee78e234a5`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d0c777c8b52f9e74da7bf3fd5be45dbd51ab10be8dde37fea12fc96f59cd09`  
		Last Modified: Fri, 08 May 2026 19:20:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:15a21e26469f168e5a065467f48dfed23a1a06d5e0d2b6ffdfcfcc38ff62a560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c3412186834b790b4fbbad4cfe5adfd0f39d11688631b5059120339ee474dc`

```dockerfile
```

-	Layers:
	-	`sha256:ffb482f3d82d9bd4136d15e9b8e08adece9f35076c719e0288e1de86156221e4`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 2.0 MB (2005483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe947a7402c9e03fc064053a531c1cecc9c253a0235c40625608b22c9a860d2f`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:fb4333344bfd32af4cefd042b89dff6ea8ba4bc5ab8168cbe3d29f8c9da5566a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36164277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d865655c5194d1b0446688e3b4f406d0d233869ddf3dcc2b4863b7a8721f32f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:35:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 20:35:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:38:30 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 20:38:30 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 20:38:30 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 20:38:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 20:38:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:38:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 20:38:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 20:38:31 GMT
USER memcache
# Fri, 08 May 2026 20:38:31 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 20:38:31 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2805acf219c32faae551498121eb47f3d7d32bc2a908969bd1ac04c3f49017fe`  
		Last Modified: Fri, 08 May 2026 20:38:41 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278e7e1caa6b74657254421ed3e5193837e9b6f3dde9e041e7e95383e6e68443`  
		Last Modified: Fri, 08 May 2026 20:38:42 GMT  
		Size: 170.4 KB (170351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df05fb319f87f70759df5de69b2f40702ca122c47d614f2f8861ce256eb0b61`  
		Last Modified: Fri, 08 May 2026 20:38:42 GMT  
		Size: 2.4 MB (2394326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f6a1fd9b6e9a261288b936182122f173180b726d490646ee6164ae5c95d84c`  
		Last Modified: Fri, 08 May 2026 20:38:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b93469fb91621a5f46b7dd80327995f9ca6d8361137dbe55159ef455e2976c`  
		Last Modified: Fri, 08 May 2026 20:38:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:e82c5b578718de9c7774bc11902f22157b7c49e1a253ddfe0e3496d4a461d760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89bf5432c3d996440e1d10de68af644b31627fdeeac778ee395c95a88263010a`

```dockerfile
```

-	Layers:
	-	`sha256:8a5017f90fa8e1dd648f24d4c3fa871a8dc77b8e529fe26ee3f0034a79bdd955`  
		Last Modified: Fri, 08 May 2026 20:38:42 GMT  
		Size: 2.0 MB (2011927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e26de34ce99baa5e3d603d8a2dddfc874c4b7cf85ae36baf53e81232916879a8`  
		Last Modified: Fri, 08 May 2026 20:38:41 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; riscv64

```console
$ docker pull memcached@sha256:5ddab235954c3cde3c815b6a5be674885381502972ebc53794c4811df335843c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30623277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b6d17550b0133cd405553af720539d51b95b0d50475bbcdbf6c2173bd5280b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 16:09:52 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 09 May 2026 16:10:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 16:23:27 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 09 May 2026 16:23:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 09 May 2026 16:23:27 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 09 May 2026 16:23:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 09 May 2026 16:23:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 09 May 2026 16:23:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 09 May 2026 16:23:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 09 May 2026 16:23:28 GMT
USER memcache
# Sat, 09 May 2026 16:23:28 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 09 May 2026 16:23:28 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1e9edef871271ebe58c5a713c7c062e88ff414be0976a2c7baf0aba83823c954`  
		Last Modified: Fri, 08 May 2026 20:38:39 GMT  
		Size: 28.3 MB (28280232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9888105b7154ad185e8f5227e002ba1af0f905cba713450e54261fb929e80afe`  
		Last Modified: Sat, 09 May 2026 16:24:13 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea9dc216a8ac7e5ff5123e9cec2e0c1650d9afc96015312e8f304adc6c255a0`  
		Last Modified: Sat, 09 May 2026 16:24:13 GMT  
		Size: 133.1 KB (133086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e544f8419fe19b80d411a515c9201c8c35d068e9a3ff1127e23e53c495a036c9`  
		Last Modified: Sat, 09 May 2026 16:24:13 GMT  
		Size: 2.2 MB (2208450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b939f3eba847b32e2c08af32b5870190d0195179c8dfcfba89b9abd0d24865b8`  
		Last Modified: Sat, 09 May 2026 16:24:13 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0a4092dbf93f8a2db331d4bb00d34313567e7245e5753310064f99299a2919`  
		Last Modified: Sat, 09 May 2026 16:24:14 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:84361ecaeb53a4b02619fac3c96e92f016548a953b0bb4909dbce2605c50c27e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e712edaa1f4a23a51ec2552dadfb1ba38310fc63ac1066e30c4ccd5f2d388ce8`

```dockerfile
```

-	Layers:
	-	`sha256:b27196635d6011055da056ccc202d4d6df3c0d9296b913ab5b40505f5efb56b9`  
		Last Modified: Sat, 09 May 2026 16:24:13 GMT  
		Size: 2.0 MB (2002290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f31718fda9bdd1f0330201f0a2069f169fd2f79967b828cb3138dad392f06e0d`  
		Last Modified: Sat, 09 May 2026 16:24:12 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; s390x

```console
$ docker pull memcached@sha256:7f194d0409eee2a5b0bb8903485384802c30d3e8f3db4edc714dccedd365197b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32280599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71da9b051066a3ea5be228e76446413fcc99d1b892a8e007445d21d95254a5d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:18:08 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 19:18:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:21:32 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 19:21:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 19:21:32 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 19:21:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 19:21:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:21:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:21:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:21:32 GMT
USER memcache
# Fri, 08 May 2026 19:21:32 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 19:21:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875e7d47d55cac3b3811a3503e8330c2b49b3264583a0e3ffbc8380fe58dd8d3`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e487f7a355c714fc8533d060a278791698afaed2353417768b8f02bd7844e06`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 140.5 KB (140519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6bb469173a6734f9ba49a4aa2f9a1d3e6513740633df30a2d3bc37c3b9d4279`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 2.3 MB (2298219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7e59c6d93f04c1f009cbda35d2e5b25d8087cadff3126c5de7636d0c10b5c0`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa99c508f7dc7874b69603543390bb5c9a5b3bb0689bde04f6d7d53db1ce25bd`  
		Last Modified: Fri, 08 May 2026 19:21:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:b257f9c0883422f85a5c40a24940bb3401de8aac9c08bc12a87f5732d143082c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff10b6e9f782a5c6eee93b5e143ea12b75800a8ef331ebc5d73519e32464d829`

```dockerfile
```

-	Layers:
	-	`sha256:3f4b79e225835bdf97992cd4741626b92fb8ad5438feb251afbf7d6bb442a01d`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 2.0 MB (2009763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff63eebb23b55a364393e4d41fbc25ca8e9a760278a9403379c7fb549f8a1248`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine`

```console
$ docker pull memcached@sha256:65c80b311a9601ef5ca8af3814e5cd06a9c4277ea139d80bd53da6b4d39eb46e
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
$ docker pull memcached@sha256:7b962825022657b112923d502400d5734870d5eb12c19e7f1f6585f7534a6795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5959872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b58f7e71f30daaa3f466fa31d855fddb7101e42c0c42fac520be5d1d43ec32e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:46 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:47 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:20:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:20:22 GMT
USER memcache
# Wed, 15 Apr 2026 20:20:22 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:20:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73d5ffe265b83073ce3c7211fb3c15ebbd5e7146d870d9ce69d2e7dfc493348`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cb4fdd95ced0d5a9528e97ff0f20742749cbd9ef6dc1322d13e682a7085a67`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 106.1 KB (106063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe17fc291d9444fbae93d7f45eab008318f87302c016c06e6e911c1a571a053`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 2.0 MB (1988274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1948bd131d2cbd05c6bf2962d18b15d105abee6f42f398bab3c13737537f197`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bde8ceae30a2a0890715bbc591167ee301c57d7f75023e80be460035187def`  
		Last Modified: Wed, 15 Apr 2026 20:20:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:58ed333482f8a8530c82ad7399d5917a7db85fbcdf70fc1dec55fbedcdf09253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4255278359004afd8c94db1a7fe6129fc984d0716c33665c9eca3168476fdcb`

```dockerfile
```

-	Layers:
	-	`sha256:5f47d88d89d22d065a3590d477ae130520b882176ab07e95862afb4d8b69b214`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 94.9 KB (94901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab2d532e4a6ce2f362d25c79dfaeb88d333fe6efe7c1b5b293630bf6ca292eb8`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 20.5 KB (20530 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:47a06cd0daead339b96ed90e425336a8a49a75e4e358b5ec1ea63a630720f704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3947facc9e9fae3eee283f24b611a8ae87e353b6d6447bc6f582e90f2fce3743`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:58 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:21:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:21:03 GMT
USER memcache
# Wed, 15 Apr 2026 20:21:03 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:21:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77001163fdaab47f07a85fc5bb15f3512a8cb9b9b049cec7e0c88bcbbdb5bb5d`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee1b43c0cfbf2ee56e39441933ff06803264d22918fe867d8b5ba7d5adfb9c3`  
		Last Modified: Wed, 15 Apr 2026 20:21:06 GMT  
		Size: 102.6 KB (102630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c041bfac12e599ad87749289dec9672dac36e8c0e16779f13fa695d10f2f0cc5`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 1.9 MB (1937835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2dfd492dd0f295311a0c314fae06f4b325ae22cb0e673a53e0705f3d4e0504`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671c66eac839c2f0a5b2e64d1f581069c4cdf119e784bff16540ecc94e2c2b10`  
		Last Modified: Wed, 15 Apr 2026 20:21:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2a6148a6aebb042e55781b40ed626d0c5871833be4ae8dc303af7aace07d9d60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbaadfaacfaf0e7c226b35236bb84c2268d4c6eb017efd435a3999a44edfcc77`

```dockerfile
```

-	Layers:
	-	`sha256:c68bb3ee35fc0ac716bca45cc759f3b1ff52b1d5a0acae9876eaf0aa55aa667d`  
		Last Modified: Wed, 15 Apr 2026 20:21:06 GMT  
		Size: 20.5 KB (20466 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:fb58bae12ffa00c9cbafc8bee2341b43ffdccacbde7085fa707ef6c7f2d69e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd4e85c30e4df5803b553b8a7f84084c3dae6f72531ac70fcabf7099cfa8148`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:14:38 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 21:14:39 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 21:17:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:17:34 GMT
USER memcache
# Wed, 15 Apr 2026 21:17:34 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 21:17:34 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e312136cfedda9620407d42650d0595220e60d3c40ae8853bfbdd83f392b9e6`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53697a39f37b691917c91310ac4e107308674bddcc9017e3bbc0d0134eaf4c3e`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 92.4 KB (92369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5e4be9e0df543f152c376fe2cc74b89b75585793fdbd7d12476737d386d8e1`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 1.9 MB (1896191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a083f41edf5f859feb4367eeeea0955dc9799c8202fb8a67c40915ed5b195002`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c43503b1f4f42ffc5e0e4415befe45199dec730bc26347df151298345ba640`  
		Last Modified: Wed, 15 Apr 2026 21:17:40 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7535cf6b6a140771131c2c524301d4616f34856fcd8ecbe3e52300108c49de2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d73c906894a0a3d178edd69991f310225c0daef314e6faa83a0b9adecfbeb34`

```dockerfile
```

-	Layers:
	-	`sha256:8f1fddd7d14560fb90f381b09cde9302dfc9253e6702adf28c55961d755b1ad8`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 94.3 KB (94319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fcf119d246607aa25330c4c05fe14a64cebda69b02d14507862a9f07c1404e6`  
		Last Modified: Wed, 15 Apr 2026 21:17:38 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:6d70439467a65065c52894232a3085c724da2810a9b3205130d5e434ab411e3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6288798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4be3e105216d2507b68e772f7d08d52a5076dd55fad35c29775038d05c24112`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:15:23 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:15:24 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:18:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:18:13 GMT
USER memcache
# Wed, 15 Apr 2026 20:18:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:18:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81758f5fc2e8fa13e3625f253d7c999560ac666121c026f7251dbfb919cca611`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d735737d3a0cf1eda63bd72c09f64eb679313e9c5f8a105849848bdd779e1d`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 121.8 KB (121846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ac0921d2cc2b3388e0f006a6672c5a9e1098a59e570121dde092104d845c51`  
		Last Modified: Wed, 15 Apr 2026 20:18:19 GMT  
		Size: 2.0 MB (1965733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca9cf731b18a76c3ac25cc3add219660d57516c12680d7b1f1ece282406eb82`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717a6b23dd1cd76b686bf26066af23265e0d002ed6a3e87f6aa4f79264b7da11`  
		Last Modified: Wed, 15 Apr 2026 20:18:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7e5232b868d3222e3ce2b0ee39c62f6cb294bea27456b00940fbc4e3c8c3f84d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:780bf975a24d5fdc511c857720c04cb077d64abcfe4c93ea0db7c9487c323718`

```dockerfile
```

-	Layers:
	-	`sha256:addb0f46e3b5adb674175c11fc85526d4628e24d74d210c8b00c9a945b44407c`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 94.4 KB (94355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3364e418b74b6f6ca17deec7d55783a6e1554de3783ab0a6d5e56496d935ddb0`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:80328bf779fa1494f7677b441ad1c16c2134f126e6556953deb3cfab1c4c9770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5744816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d957405dd0811f1cd15fe39563938a60c2008204d2f63ebc7e39f8989c796f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:20:45 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 22:20:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 22:23:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 22:23:32 GMT
USER memcache
# Wed, 15 Apr 2026 22:23:32 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 22:23:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0617a09eee85c2032f5596ded56b733366513074f9096177315b50dc45485e20`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c67275dbc381ac3ae0b21dda20edaf245e2ca54d6f5dc3af8805db03c17cc93`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 110.7 KB (110715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6ecb23f1f4bc89d5c315aac493f29fe7bb33061c70d926c904f4f55d374461`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 1.9 MB (1942309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e782df8f482a58603ea70ef9e04e838d044a6070c7e4cd116c90a09b917ed940`  
		Last Modified: Wed, 15 Apr 2026 22:23:38 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616df56d574e39c00ae772c6a29e2b724698048a83cc29ea17049573f9073b10`  
		Last Modified: Wed, 15 Apr 2026 22:23:38 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c726e7abf461d963e544818339e4cd12fd2f31e41436475f0e51818a0885fbdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12e41b9d6f745d686c2649255bd14fe4e0b97a3477d383e719490e5ef66b27ae`

```dockerfile
```

-	Layers:
	-	`sha256:b44003cd1ea209090a063c5abfb4ee881849abba47e8711191b7637f86d8ee8b`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 94.9 KB (94856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f431de53d9b6c7e2cbc847af9daec064d061f8bd625615734012051336c495a`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 20.5 KB (20472 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:8182e35a9a404f0b522cb3c176d3dc4aade974e5556184c0a5a19e800721868a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6034321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c6f532e81b50ea71c3520a80da0c8154b4cb14ebc17f87eb3a026862b47ed8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:43 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:20:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:20:22 GMT
USER memcache
# Wed, 15 Apr 2026 20:20:22 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:20:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee88d1c88fa46aa906a297c2919c9a085e74d04f20e4f827ca240a20f10ad34`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c574329cc1ebf156e2d89ab608bd58a3c0db550845c0ec394d265aa98fc5c4`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 126.3 KB (126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2a28510bcba91734e7b38682847296011b63458db8a87a4bcecd180b8de7b5`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 2.1 MB (2075767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c524eb15ef0a41bf969efc93ef579db92dc59e8df57c9abfd099e7f6ff0756`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bde8ceae30a2a0890715bbc591167ee301c57d7f75023e80be460035187def`  
		Last Modified: Wed, 15 Apr 2026 20:20:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:4051408ef6c5bf4d4f37abf19c13f0298d8baa81770fcbfb588221e49e3bb834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec3a4d49e6f325e484db43c9c9981f4eaa0223d9ae98282d95c3ee20c2089cb`

```dockerfile
```

-	Layers:
	-	`sha256:0e4e65db585f857844a67a831eb876dbb0a8a40d9269393d6c0fa83a2df995ae`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 94.3 KB (94308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50f58ec8aff3c96cc7b58e689122c27ee26121c598034cdc59ec95fd6423effe`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:f3209d1ca2c4ce827614d16445231d96372944d218f18fd22850eec83874e5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5772332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e30170e0826b89d0ca59ffcae54b850ded07e6ae9451ecf1fd60f3ca8adcc725`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 00:00:48 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 16 Apr 2026 00:00:52 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Thu, 16 Apr 2026 00:14:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 16 Apr 2026 00:14:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Apr 2026 00:14:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 16 Apr 2026 00:14:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Apr 2026 00:14:22 GMT
USER memcache
# Thu, 16 Apr 2026 00:14:22 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 16 Apr 2026 00:14:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62b143e34f5b89277e3a88ed4d722339d188a094d4bb534e222ca80e7741031`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfff7c64f831ba03c491874cdf9a1c3f42bff72bb0e1951c63d8cf718854cff`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 108.9 KB (108903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69aef1050272a61cfbfd97c041d3776f96bdd03b102f2c3c54bbb0af2e1235a5`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 2.1 MB (2074414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ce340fb37f86db0d3aa774c23880b7c8322d2af8e3adc27a6ffa25d67c2122`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e40c6fb92d819994d38fae7accdffd583465eb6e645834b66f3ce9f0562f69`  
		Last Modified: Thu, 16 Apr 2026 00:14:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2caae198d1efb7d4df14da45a3ff360a697982b544a61a3f907076b414983ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1503bd38f4b30bc91be18dd93359e7376a9da1c7cb652ade64efd154064543fe`

```dockerfile
```

-	Layers:
	-	`sha256:e2d79fb634d76e28f055ab09953f59c371b93599e2b79f20f3d758f2c9520118`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 94.3 KB (94304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3614ad9b1715c3d6aa488496fca74d7143ea095d227f599407c933c62ec266aa`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 20.6 KB (20604 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:1da27660ae89a83aaf603e1affd51be573e5b8dac6c07ed592aee2a3a2b20581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5859702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13aa64df69a308e46b054bbd8e7a5d2f1e079005771f61748dae0d049889ba7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:14:40 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:14:41 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:17:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:17:58 GMT
USER memcache
# Wed, 15 Apr 2026 20:17:58 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:17:58 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c42733e5f451590186b9b76c4b374ae5a84b657f7f1fd405647f5ba82c65bcd`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a14431ac88e8fe205b07f09b7e4843bb254de41cbc044725d6eaee3c2f822f`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 114.3 KB (114293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6377b7d98f32173cd47682aa73b32e4eba42781fa9224b9eb7a6f87367d37f94`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 2.0 MB (2017525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d022ae992296922747a4b69694b0185a0ce1f6cdece7f794e39e74dab92d250`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255cb3a435cbd623c1235d0429160faf72c244a6c1a613525df36f58a8c1f784`  
		Last Modified: Wed, 15 Apr 2026 20:18:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:531ee140f06db77d73b71bce7339abec3c6d976092bb80542bb337bb406acdbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b17d6f7e71efe3ee05ebcdb8ae90c28cf60db9ef069b0a98fe442c949740a6c`

```dockerfile
```

-	Layers:
	-	`sha256:820a080f49bf9e33948dbe5c13f6254f135d90bcb2b2277e3d2fd2430626c1a2`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 94.2 KB (94250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8ab82f4f240f46f9e34b74691925ab4af7f1cbb12ad3cb8639e0f317cf06653`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine3.23`

```console
$ docker pull memcached@sha256:65c80b311a9601ef5ca8af3814e5cd06a9c4277ea139d80bd53da6b4d39eb46e
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
$ docker pull memcached@sha256:7b962825022657b112923d502400d5734870d5eb12c19e7f1f6585f7534a6795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5959872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b58f7e71f30daaa3f466fa31d855fddb7101e42c0c42fac520be5d1d43ec32e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:46 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:47 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:20:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:20:22 GMT
USER memcache
# Wed, 15 Apr 2026 20:20:22 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:20:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73d5ffe265b83073ce3c7211fb3c15ebbd5e7146d870d9ce69d2e7dfc493348`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cb4fdd95ced0d5a9528e97ff0f20742749cbd9ef6dc1322d13e682a7085a67`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 106.1 KB (106063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe17fc291d9444fbae93d7f45eab008318f87302c016c06e6e911c1a571a053`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 2.0 MB (1988274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1948bd131d2cbd05c6bf2962d18b15d105abee6f42f398bab3c13737537f197`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bde8ceae30a2a0890715bbc591167ee301c57d7f75023e80be460035187def`  
		Last Modified: Wed, 15 Apr 2026 20:20:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:58ed333482f8a8530c82ad7399d5917a7db85fbcdf70fc1dec55fbedcdf09253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4255278359004afd8c94db1a7fe6129fc984d0716c33665c9eca3168476fdcb`

```dockerfile
```

-	Layers:
	-	`sha256:5f47d88d89d22d065a3590d477ae130520b882176ab07e95862afb4d8b69b214`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 94.9 KB (94901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab2d532e4a6ce2f362d25c79dfaeb88d333fe6efe7c1b5b293630bf6ca292eb8`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 20.5 KB (20530 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; arm variant v6

```console
$ docker pull memcached@sha256:47a06cd0daead339b96ed90e425336a8a49a75e4e358b5ec1ea63a630720f704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3947facc9e9fae3eee283f24b611a8ae87e353b6d6447bc6f582e90f2fce3743`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:58 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:21:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:21:03 GMT
USER memcache
# Wed, 15 Apr 2026 20:21:03 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:21:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77001163fdaab47f07a85fc5bb15f3512a8cb9b9b049cec7e0c88bcbbdb5bb5d`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee1b43c0cfbf2ee56e39441933ff06803264d22918fe867d8b5ba7d5adfb9c3`  
		Last Modified: Wed, 15 Apr 2026 20:21:06 GMT  
		Size: 102.6 KB (102630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c041bfac12e599ad87749289dec9672dac36e8c0e16779f13fa695d10f2f0cc5`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 1.9 MB (1937835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2dfd492dd0f295311a0c314fae06f4b325ae22cb0e673a53e0705f3d4e0504`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671c66eac839c2f0a5b2e64d1f581069c4cdf119e784bff16540ecc94e2c2b10`  
		Last Modified: Wed, 15 Apr 2026 20:21:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:2a6148a6aebb042e55781b40ed626d0c5871833be4ae8dc303af7aace07d9d60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbaadfaacfaf0e7c226b35236bb84c2268d4c6eb017efd435a3999a44edfcc77`

```dockerfile
```

-	Layers:
	-	`sha256:c68bb3ee35fc0ac716bca45cc759f3b1ff52b1d5a0acae9876eaf0aa55aa667d`  
		Last Modified: Wed, 15 Apr 2026 20:21:06 GMT  
		Size: 20.5 KB (20466 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; arm variant v7

```console
$ docker pull memcached@sha256:fb58bae12ffa00c9cbafc8bee2341b43ffdccacbde7085fa707ef6c7f2d69e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd4e85c30e4df5803b553b8a7f84084c3dae6f72531ac70fcabf7099cfa8148`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:14:38 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 21:14:39 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 21:17:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:17:34 GMT
USER memcache
# Wed, 15 Apr 2026 21:17:34 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 21:17:34 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e312136cfedda9620407d42650d0595220e60d3c40ae8853bfbdd83f392b9e6`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53697a39f37b691917c91310ac4e107308674bddcc9017e3bbc0d0134eaf4c3e`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 92.4 KB (92369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5e4be9e0df543f152c376fe2cc74b89b75585793fdbd7d12476737d386d8e1`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 1.9 MB (1896191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a083f41edf5f859feb4367eeeea0955dc9799c8202fb8a67c40915ed5b195002`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c43503b1f4f42ffc5e0e4415befe45199dec730bc26347df151298345ba640`  
		Last Modified: Wed, 15 Apr 2026 21:17:40 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:7535cf6b6a140771131c2c524301d4616f34856fcd8ecbe3e52300108c49de2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d73c906894a0a3d178edd69991f310225c0daef314e6faa83a0b9adecfbeb34`

```dockerfile
```

-	Layers:
	-	`sha256:8f1fddd7d14560fb90f381b09cde9302dfc9253e6702adf28c55961d755b1ad8`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 94.3 KB (94319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fcf119d246607aa25330c4c05fe14a64cebda69b02d14507862a9f07c1404e6`  
		Last Modified: Wed, 15 Apr 2026 21:17:38 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:6d70439467a65065c52894232a3085c724da2810a9b3205130d5e434ab411e3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6288798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4be3e105216d2507b68e772f7d08d52a5076dd55fad35c29775038d05c24112`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:15:23 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:15:24 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:18:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:18:13 GMT
USER memcache
# Wed, 15 Apr 2026 20:18:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:18:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81758f5fc2e8fa13e3625f253d7c999560ac666121c026f7251dbfb919cca611`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d735737d3a0cf1eda63bd72c09f64eb679313e9c5f8a105849848bdd779e1d`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 121.8 KB (121846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ac0921d2cc2b3388e0f006a6672c5a9e1098a59e570121dde092104d845c51`  
		Last Modified: Wed, 15 Apr 2026 20:18:19 GMT  
		Size: 2.0 MB (1965733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca9cf731b18a76c3ac25cc3add219660d57516c12680d7b1f1ece282406eb82`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717a6b23dd1cd76b686bf26066af23265e0d002ed6a3e87f6aa4f79264b7da11`  
		Last Modified: Wed, 15 Apr 2026 20:18:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:7e5232b868d3222e3ce2b0ee39c62f6cb294bea27456b00940fbc4e3c8c3f84d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:780bf975a24d5fdc511c857720c04cb077d64abcfe4c93ea0db7c9487c323718`

```dockerfile
```

-	Layers:
	-	`sha256:addb0f46e3b5adb674175c11fc85526d4628e24d74d210c8b00c9a945b44407c`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 94.4 KB (94355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3364e418b74b6f6ca17deec7d55783a6e1554de3783ab0a6d5e56496d935ddb0`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; 386

```console
$ docker pull memcached@sha256:80328bf779fa1494f7677b441ad1c16c2134f126e6556953deb3cfab1c4c9770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5744816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d957405dd0811f1cd15fe39563938a60c2008204d2f63ebc7e39f8989c796f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:20:45 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 22:20:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 22:23:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 22:23:32 GMT
USER memcache
# Wed, 15 Apr 2026 22:23:32 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 22:23:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0617a09eee85c2032f5596ded56b733366513074f9096177315b50dc45485e20`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c67275dbc381ac3ae0b21dda20edaf245e2ca54d6f5dc3af8805db03c17cc93`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 110.7 KB (110715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6ecb23f1f4bc89d5c315aac493f29fe7bb33061c70d926c904f4f55d374461`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 1.9 MB (1942309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e782df8f482a58603ea70ef9e04e838d044a6070c7e4cd116c90a09b917ed940`  
		Last Modified: Wed, 15 Apr 2026 22:23:38 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616df56d574e39c00ae772c6a29e2b724698048a83cc29ea17049573f9073b10`  
		Last Modified: Wed, 15 Apr 2026 22:23:38 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:c726e7abf461d963e544818339e4cd12fd2f31e41436475f0e51818a0885fbdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12e41b9d6f745d686c2649255bd14fe4e0b97a3477d383e719490e5ef66b27ae`

```dockerfile
```

-	Layers:
	-	`sha256:b44003cd1ea209090a063c5abfb4ee881849abba47e8711191b7637f86d8ee8b`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 94.9 KB (94856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f431de53d9b6c7e2cbc847af9daec064d061f8bd625615734012051336c495a`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 20.5 KB (20472 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; ppc64le

```console
$ docker pull memcached@sha256:8182e35a9a404f0b522cb3c176d3dc4aade974e5556184c0a5a19e800721868a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6034321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c6f532e81b50ea71c3520a80da0c8154b4cb14ebc17f87eb3a026862b47ed8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:43 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:20:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:20:22 GMT
USER memcache
# Wed, 15 Apr 2026 20:20:22 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:20:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee88d1c88fa46aa906a297c2919c9a085e74d04f20e4f827ca240a20f10ad34`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c574329cc1ebf156e2d89ab608bd58a3c0db550845c0ec394d265aa98fc5c4`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 126.3 KB (126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2a28510bcba91734e7b38682847296011b63458db8a87a4bcecd180b8de7b5`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 2.1 MB (2075767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c524eb15ef0a41bf969efc93ef579db92dc59e8df57c9abfd099e7f6ff0756`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bde8ceae30a2a0890715bbc591167ee301c57d7f75023e80be460035187def`  
		Last Modified: Wed, 15 Apr 2026 20:20:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:4051408ef6c5bf4d4f37abf19c13f0298d8baa81770fcbfb588221e49e3bb834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec3a4d49e6f325e484db43c9c9981f4eaa0223d9ae98282d95c3ee20c2089cb`

```dockerfile
```

-	Layers:
	-	`sha256:0e4e65db585f857844a67a831eb876dbb0a8a40d9269393d6c0fa83a2df995ae`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 94.3 KB (94308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50f58ec8aff3c96cc7b58e689122c27ee26121c598034cdc59ec95fd6423effe`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; riscv64

```console
$ docker pull memcached@sha256:f3209d1ca2c4ce827614d16445231d96372944d218f18fd22850eec83874e5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5772332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e30170e0826b89d0ca59ffcae54b850ded07e6ae9451ecf1fd60f3ca8adcc725`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 00:00:48 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 16 Apr 2026 00:00:52 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Thu, 16 Apr 2026 00:14:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 16 Apr 2026 00:14:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Apr 2026 00:14:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 16 Apr 2026 00:14:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Apr 2026 00:14:22 GMT
USER memcache
# Thu, 16 Apr 2026 00:14:22 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 16 Apr 2026 00:14:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62b143e34f5b89277e3a88ed4d722339d188a094d4bb534e222ca80e7741031`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfff7c64f831ba03c491874cdf9a1c3f42bff72bb0e1951c63d8cf718854cff`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 108.9 KB (108903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69aef1050272a61cfbfd97c041d3776f96bdd03b102f2c3c54bbb0af2e1235a5`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 2.1 MB (2074414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ce340fb37f86db0d3aa774c23880b7c8322d2af8e3adc27a6ffa25d67c2122`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e40c6fb92d819994d38fae7accdffd583465eb6e645834b66f3ce9f0562f69`  
		Last Modified: Thu, 16 Apr 2026 00:14:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:2caae198d1efb7d4df14da45a3ff360a697982b544a61a3f907076b414983ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1503bd38f4b30bc91be18dd93359e7376a9da1c7cb652ade64efd154064543fe`

```dockerfile
```

-	Layers:
	-	`sha256:e2d79fb634d76e28f055ab09953f59c371b93599e2b79f20f3d758f2c9520118`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 94.3 KB (94304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3614ad9b1715c3d6aa488496fca74d7143ea095d227f599407c933c62ec266aa`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 20.6 KB (20604 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; s390x

```console
$ docker pull memcached@sha256:1da27660ae89a83aaf603e1affd51be573e5b8dac6c07ed592aee2a3a2b20581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5859702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13aa64df69a308e46b054bbd8e7a5d2f1e079005771f61748dae0d049889ba7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:14:40 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:14:41 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:17:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:17:58 GMT
USER memcache
# Wed, 15 Apr 2026 20:17:58 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:17:58 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c42733e5f451590186b9b76c4b374ae5a84b657f7f1fd405647f5ba82c65bcd`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a14431ac88e8fe205b07f09b7e4843bb254de41cbc044725d6eaee3c2f822f`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 114.3 KB (114293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6377b7d98f32173cd47682aa73b32e4eba42781fa9224b9eb7a6f87367d37f94`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 2.0 MB (2017525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d022ae992296922747a4b69694b0185a0ce1f6cdece7f794e39e74dab92d250`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255cb3a435cbd623c1235d0429160faf72c244a6c1a613525df36f58a8c1f784`  
		Last Modified: Wed, 15 Apr 2026 20:18:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:531ee140f06db77d73b71bce7339abec3c6d976092bb80542bb337bb406acdbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b17d6f7e71efe3ee05ebcdb8ae90c28cf60db9ef069b0a98fe442c949740a6c`

```dockerfile
```

-	Layers:
	-	`sha256:820a080f49bf9e33948dbe5c13f6254f135d90bcb2b2277e3d2fd2430626c1a2`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 94.2 KB (94250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8ab82f4f240f46f9e34b74691925ab4af7f1cbb12ad3cb8639e0f317cf06653`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-trixie`

```console
$ docker pull memcached@sha256:f7a252e7ba3fbbe9672c483354c5081d02b780122c3bb97bd311d5662b54d0ad
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
$ docker pull memcached@sha256:5f9197399e5aefcabef61b7c94d4e9578698e4a0ac391f6a4b34eb0dcd493df2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32198719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5474f3cc4ab6f46b8613ec8b77a7c6ec75f3b8944c8674fa5c02be437ee6567b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:22:04 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 19:22:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:24:53 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 19:24:53 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 19:24:53 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 19:24:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 19:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:24:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:24:54 GMT
USER memcache
# Fri, 08 May 2026 19:24:54 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 19:24:54 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95946911721deafff321fd508db9ba36e3babc47097ecd6c6bdf2ba0dd470257`  
		Last Modified: Fri, 08 May 2026 19:24:59 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2951237283f3070819f0121ee72d97873d9e5287f4ff5cd5b450147eb57c72`  
		Last Modified: Fri, 08 May 2026 19:24:59 GMT  
		Size: 136.7 KB (136676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f29d81d44c4b3a8bb7866171f79f5054acda551367bbcf5ae523080623b437d`  
		Last Modified: Fri, 08 May 2026 19:25:00 GMT  
		Size: 2.3 MB (2280301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb056d99db8480655d7742fb357ad1bd6de6b78556d46d005628eb93210eecf4`  
		Last Modified: Fri, 08 May 2026 19:24:59 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de908d42b697f6622dffc88cdd09d0a1ddb3127cbabf42fa000970465a9e1f8`  
		Last Modified: Fri, 08 May 2026 19:25:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:34e381cf324225b9dee5ca26f3ecb0ccc5f1f460edfde42459740d7a519e0328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1bcfe0acd4621e7447b151a6a20f2248402d84d7ff8d93c46b90f669ab88e2e`

```dockerfile
```

-	Layers:
	-	`sha256:4ddea0123ac32de5d1b564e296f88cb637634e258c91e4381b8bee9b175654bb`  
		Last Modified: Fri, 08 May 2026 19:25:00 GMT  
		Size: 2.0 MB (2008326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72b234be41aa76eb975368e76c3a352a83f7b9e17ea4311b77d264ba3245480f`  
		Last Modified: Fri, 08 May 2026 19:24:59 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:9bb2e143dc3647a49e4e8f85d5c418bca9b08ce1c1765c5ad7f32f5ab3d8596f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30305327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1b9575bad28b94e1186f365ab00d1a786bf0e90cc8fb820378cf08aa68513b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:25:56 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 20:26:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:29:16 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 20:29:16 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 20:29:16 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 20:29:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 20:29:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:29:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 20:29:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 20:29:16 GMT
USER memcache
# Fri, 08 May 2026 20:29:16 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 20:29:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8f774e9b92b540806fc05167db7ce09a3e1b12abdb9d496f7b8c82138656065a`  
		Last Modified: Fri, 08 May 2026 18:33:49 GMT  
		Size: 27.9 MB (27948200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b5f67bec55f95884a3889baf69e54663718d70194c4ad200c3189a69ed4f77`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0bc2199b80394dc4c86e2ec47bb2bacfa524afadd19cd9436e2cde86accf84b`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 144.2 KB (144163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652d72e4ec6b0cb1a3ca6f0de801f39fbe579385f24fdf2fa903d000df01ef7e`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 2.2 MB (2211447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e003813362a92e41a38ce899360dfc51977add71013d1cac48643e6d9361ec43`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b9b40076d0562644d2bec445a0a7fdefbf4dd5d545c7d8cbdfef18f171b99a`  
		Last Modified: Fri, 08 May 2026 20:29:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:d83c846fc98d19ba355a9a5d1c59147c565e7894fed7c5b582bd5b4bde92d90d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6056bef38756043ff8218f82594c154e80dc8d2097dd770a7bd7bb09a8e6e3e6`

```dockerfile
```

-	Layers:
	-	`sha256:4b4fd92902f7c83c67f43e813275bc5676ec6370639df11fe1394ce7fa7eef2d`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 2.0 MB (2011329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d8b1829f761528fa20afdac852bde73a128edf4c6f11e990f7e7c7fcbcfbf61`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:3d1cfa4c23d23705cf3f8b9302ff26048e2ac216027f45be24e93b8f0817a952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28516943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:582f213c6b868ce82f6e14b78c661812d0781e91331e3ca32ce462777a0529fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:16:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 19:16:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:19:15 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 19:19:15 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 19:19:15 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 19:19:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 19:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:19:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:19:15 GMT
USER memcache
# Fri, 08 May 2026 19:19:15 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 19:19:15 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f1433620eadfdfe016c8054b954f619ae5bca159f35a9459c36a76d9ef4d39c3`  
		Last Modified: Fri, 08 May 2026 18:37:58 GMT  
		Size: 26.2 MB (26214912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851a3dc4d05ac8ea75d436c9d8de99f7ca3c80f159cadffd985253ae10a40069`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18a5b288c05e8d152bf1530b1c4248c0ea5c08902853e0955c6838d5d418b33`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 135.4 KB (135388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff024d65a6401c67cefb240a3ef3d181382530d66cfbb03f13ff32d81500525`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 2.2 MB (2165127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0613bb171f6d5dee88871aafa9a91daf991e3d262feb8682aa8fb5696046579`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c1a297997b8b44cdcad29c590e65efa7934da84dacae1fbddd2b017bb0dd03`  
		Last Modified: Fri, 08 May 2026 19:19:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:e7210267977b9ce03df4bc38f1d1ea5760217f9f582f392ac648876a13580041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120a3ae5c0ce21313dc99a5a24a7d9ae48f434e40717325fda7675fc368c3a9e`

```dockerfile
```

-	Layers:
	-	`sha256:b2f6d69af7f79690357135d68c570ab105358d093cb3ef2b6b37d8c0c4b8766a`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 2.0 MB (2009786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19ecae093d7ef811fe61bf6ed6706bf88a86ab363852e511e19d077fea8bdf22`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:4a47319c5ea763766ec14f7f49c71294e7621973dbf1d934330b273a50d86ae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32560787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea04a0e8415a1e901722a2dc626f036034b99c11dd819b6aab54fe2172610825`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:21:07 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 19:21:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:24:08 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 19:24:08 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 19:24:08 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 19:24:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 19:24:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:24:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:24:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:24:08 GMT
USER memcache
# Fri, 08 May 2026 19:24:08 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 19:24:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73f16d12b26b60a37ae242c9f12503fa0bb655f780014ce964bf39b960ea39a`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f45dfab4b00618ca4983d73b6acabb6fe1e056339b0cafcc1c0268303c02b89`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 153.5 KB (153496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91da4495c7aeb14802d9e2f3854b2226395b2886efcb91a3f91778774632602`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 2.3 MB (2262131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91f17f562e485ed0d6523251b77ca57f1df60d00243de97a13459b077fb30df`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70d0b5c5805a6bd639b55f25e9fb45c11035876f9fca3e2ab607fb2d818b01f`  
		Last Modified: Fri, 08 May 2026 19:24:15 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:003da519f1303287f7dbac93d59fd8f7cd3bd4f7c1c3f59e2ea25f3e1933a4a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b34e9510fcd3b35da3965f941f9c4d3bdf0eff1c30985a7ce5621b638e4c237e`

```dockerfile
```

-	Layers:
	-	`sha256:6041a557446d392656291f000150951d92c8392a387515be5c7e384d175a1967`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 2.0 MB (2008642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e39754d938ea3671f3babce3fbab5d612247a51cbc9f172de306c3fcf60e3a1b`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; 386

```console
$ docker pull memcached@sha256:ae0c2a4ef3d5a1336f8204efdb14230b37402d5f8c4096295ddd0f53b7e041ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33670271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d71af2d7fff4e8bb864857f69883ac131a512bb9311bb23de7031cb892e38a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:17:17 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 19:17:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:20:22 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 19:20:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 19:20:22 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 19:20:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 19:20:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:20:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:20:22 GMT
USER memcache
# Fri, 08 May 2026 19:20:22 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 19:20:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:43e2ffbaa23260ffb4e3de716920f2ed9e6af56e465ca1233a2d84c2cc1cf005`  
		Last Modified: Fri, 08 May 2026 18:32:48 GMT  
		Size: 31.3 MB (31296400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2ce2fa16a9ab3457f94c9628fc05a5fd6d54e5d6d3d8a9e1e506ba4e5a37aa`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540be255286e8d861d09681ddd0cd64a25a1b5fa161cca9b859487c03bfb0b6e`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 147.5 KB (147521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913676b9d51d935a10d363087959dec4494fbae5fdf82b80b84e9ecaae370ad3`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 2.2 MB (2224836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224690b120957a082d3ef84ebd501af44b1437fdbf4fcefad6e8faee78e234a5`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d0c777c8b52f9e74da7bf3fd5be45dbd51ab10be8dde37fea12fc96f59cd09`  
		Last Modified: Fri, 08 May 2026 19:20:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:15a21e26469f168e5a065467f48dfed23a1a06d5e0d2b6ffdfcfcc38ff62a560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c3412186834b790b4fbbad4cfe5adfd0f39d11688631b5059120339ee474dc`

```dockerfile
```

-	Layers:
	-	`sha256:ffb482f3d82d9bd4136d15e9b8e08adece9f35076c719e0288e1de86156221e4`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 2.0 MB (2005483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe947a7402c9e03fc064053a531c1cecc9c253a0235c40625608b22c9a860d2f`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:fb4333344bfd32af4cefd042b89dff6ea8ba4bc5ab8168cbe3d29f8c9da5566a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36164277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d865655c5194d1b0446688e3b4f406d0d233869ddf3dcc2b4863b7a8721f32f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:35:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 20:35:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:38:30 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 20:38:30 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 20:38:30 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 20:38:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 20:38:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:38:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 20:38:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 20:38:31 GMT
USER memcache
# Fri, 08 May 2026 20:38:31 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 20:38:31 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2805acf219c32faae551498121eb47f3d7d32bc2a908969bd1ac04c3f49017fe`  
		Last Modified: Fri, 08 May 2026 20:38:41 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278e7e1caa6b74657254421ed3e5193837e9b6f3dde9e041e7e95383e6e68443`  
		Last Modified: Fri, 08 May 2026 20:38:42 GMT  
		Size: 170.4 KB (170351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df05fb319f87f70759df5de69b2f40702ca122c47d614f2f8861ce256eb0b61`  
		Last Modified: Fri, 08 May 2026 20:38:42 GMT  
		Size: 2.4 MB (2394326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f6a1fd9b6e9a261288b936182122f173180b726d490646ee6164ae5c95d84c`  
		Last Modified: Fri, 08 May 2026 20:38:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b93469fb91621a5f46b7dd80327995f9ca6d8361137dbe55159ef455e2976c`  
		Last Modified: Fri, 08 May 2026 20:38:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:e82c5b578718de9c7774bc11902f22157b7c49e1a253ddfe0e3496d4a461d760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89bf5432c3d996440e1d10de68af644b31627fdeeac778ee395c95a88263010a`

```dockerfile
```

-	Layers:
	-	`sha256:8a5017f90fa8e1dd648f24d4c3fa871a8dc77b8e529fe26ee3f0034a79bdd955`  
		Last Modified: Fri, 08 May 2026 20:38:42 GMT  
		Size: 2.0 MB (2011927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e26de34ce99baa5e3d603d8a2dddfc874c4b7cf85ae36baf53e81232916879a8`  
		Last Modified: Fri, 08 May 2026 20:38:41 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:5ddab235954c3cde3c815b6a5be674885381502972ebc53794c4811df335843c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30623277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b6d17550b0133cd405553af720539d51b95b0d50475bbcdbf6c2173bd5280b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 16:09:52 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 09 May 2026 16:10:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 16:23:27 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 09 May 2026 16:23:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 09 May 2026 16:23:27 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 09 May 2026 16:23:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 09 May 2026 16:23:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 09 May 2026 16:23:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 09 May 2026 16:23:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 09 May 2026 16:23:28 GMT
USER memcache
# Sat, 09 May 2026 16:23:28 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 09 May 2026 16:23:28 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1e9edef871271ebe58c5a713c7c062e88ff414be0976a2c7baf0aba83823c954`  
		Last Modified: Fri, 08 May 2026 20:38:39 GMT  
		Size: 28.3 MB (28280232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9888105b7154ad185e8f5227e002ba1af0f905cba713450e54261fb929e80afe`  
		Last Modified: Sat, 09 May 2026 16:24:13 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea9dc216a8ac7e5ff5123e9cec2e0c1650d9afc96015312e8f304adc6c255a0`  
		Last Modified: Sat, 09 May 2026 16:24:13 GMT  
		Size: 133.1 KB (133086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e544f8419fe19b80d411a515c9201c8c35d068e9a3ff1127e23e53c495a036c9`  
		Last Modified: Sat, 09 May 2026 16:24:13 GMT  
		Size: 2.2 MB (2208450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b939f3eba847b32e2c08af32b5870190d0195179c8dfcfba89b9abd0d24865b8`  
		Last Modified: Sat, 09 May 2026 16:24:13 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0a4092dbf93f8a2db331d4bb00d34313567e7245e5753310064f99299a2919`  
		Last Modified: Sat, 09 May 2026 16:24:14 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:84361ecaeb53a4b02619fac3c96e92f016548a953b0bb4909dbce2605c50c27e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e712edaa1f4a23a51ec2552dadfb1ba38310fc63ac1066e30c4ccd5f2d388ce8`

```dockerfile
```

-	Layers:
	-	`sha256:b27196635d6011055da056ccc202d4d6df3c0d9296b913ab5b40505f5efb56b9`  
		Last Modified: Sat, 09 May 2026 16:24:13 GMT  
		Size: 2.0 MB (2002290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f31718fda9bdd1f0330201f0a2069f169fd2f79967b828cb3138dad392f06e0d`  
		Last Modified: Sat, 09 May 2026 16:24:12 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:7f194d0409eee2a5b0bb8903485384802c30d3e8f3db4edc714dccedd365197b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32280599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71da9b051066a3ea5be228e76446413fcc99d1b892a8e007445d21d95254a5d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:18:08 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 19:18:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:21:32 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 19:21:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 19:21:32 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 19:21:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 19:21:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:21:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:21:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:21:32 GMT
USER memcache
# Fri, 08 May 2026 19:21:32 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 19:21:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875e7d47d55cac3b3811a3503e8330c2b49b3264583a0e3ffbc8380fe58dd8d3`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e487f7a355c714fc8533d060a278791698afaed2353417768b8f02bd7844e06`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 140.5 KB (140519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6bb469173a6734f9ba49a4aa2f9a1d3e6513740633df30a2d3bc37c3b9d4279`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 2.3 MB (2298219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7e59c6d93f04c1f009cbda35d2e5b25d8087cadff3126c5de7636d0c10b5c0`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa99c508f7dc7874b69603543390bb5c9a5b3bb0689bde04f6d7d53db1ce25bd`  
		Last Modified: Fri, 08 May 2026 19:21:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:b257f9c0883422f85a5c40a24940bb3401de8aac9c08bc12a87f5732d143082c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff10b6e9f782a5c6eee93b5e143ea12b75800a8ef331ebc5d73519e32464d829`

```dockerfile
```

-	Layers:
	-	`sha256:3f4b79e225835bdf97992cd4741626b92fb8ad5438feb251afbf7d6bb442a01d`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 2.0 MB (2009763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff63eebb23b55a364393e4d41fbc25ca8e9a760278a9403379c7fb549f8a1248`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.41`

```console
$ docker pull memcached@sha256:f7a252e7ba3fbbe9672c483354c5081d02b780122c3bb97bd311d5662b54d0ad
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

### `memcached:1.6.41` - linux; amd64

```console
$ docker pull memcached@sha256:5f9197399e5aefcabef61b7c94d4e9578698e4a0ac391f6a4b34eb0dcd493df2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32198719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5474f3cc4ab6f46b8613ec8b77a7c6ec75f3b8944c8674fa5c02be437ee6567b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:22:04 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 19:22:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:24:53 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 19:24:53 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 19:24:53 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 19:24:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 19:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:24:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:24:54 GMT
USER memcache
# Fri, 08 May 2026 19:24:54 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 19:24:54 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95946911721deafff321fd508db9ba36e3babc47097ecd6c6bdf2ba0dd470257`  
		Last Modified: Fri, 08 May 2026 19:24:59 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2951237283f3070819f0121ee72d97873d9e5287f4ff5cd5b450147eb57c72`  
		Last Modified: Fri, 08 May 2026 19:24:59 GMT  
		Size: 136.7 KB (136676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f29d81d44c4b3a8bb7866171f79f5054acda551367bbcf5ae523080623b437d`  
		Last Modified: Fri, 08 May 2026 19:25:00 GMT  
		Size: 2.3 MB (2280301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb056d99db8480655d7742fb357ad1bd6de6b78556d46d005628eb93210eecf4`  
		Last Modified: Fri, 08 May 2026 19:24:59 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de908d42b697f6622dffc88cdd09d0a1ddb3127cbabf42fa000970465a9e1f8`  
		Last Modified: Fri, 08 May 2026 19:25:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41` - unknown; unknown

```console
$ docker pull memcached@sha256:34e381cf324225b9dee5ca26f3ecb0ccc5f1f460edfde42459740d7a519e0328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1bcfe0acd4621e7447b151a6a20f2248402d84d7ff8d93c46b90f669ab88e2e`

```dockerfile
```

-	Layers:
	-	`sha256:4ddea0123ac32de5d1b564e296f88cb637634e258c91e4381b8bee9b175654bb`  
		Last Modified: Fri, 08 May 2026 19:25:00 GMT  
		Size: 2.0 MB (2008326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72b234be41aa76eb975368e76c3a352a83f7b9e17ea4311b77d264ba3245480f`  
		Last Modified: Fri, 08 May 2026 19:24:59 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41` - linux; arm variant v5

```console
$ docker pull memcached@sha256:9bb2e143dc3647a49e4e8f85d5c418bca9b08ce1c1765c5ad7f32f5ab3d8596f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30305327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1b9575bad28b94e1186f365ab00d1a786bf0e90cc8fb820378cf08aa68513b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:25:56 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 20:26:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:29:16 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 20:29:16 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 20:29:16 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 20:29:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 20:29:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:29:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 20:29:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 20:29:16 GMT
USER memcache
# Fri, 08 May 2026 20:29:16 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 20:29:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8f774e9b92b540806fc05167db7ce09a3e1b12abdb9d496f7b8c82138656065a`  
		Last Modified: Fri, 08 May 2026 18:33:49 GMT  
		Size: 27.9 MB (27948200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b5f67bec55f95884a3889baf69e54663718d70194c4ad200c3189a69ed4f77`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0bc2199b80394dc4c86e2ec47bb2bacfa524afadd19cd9436e2cde86accf84b`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 144.2 KB (144163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652d72e4ec6b0cb1a3ca6f0de801f39fbe579385f24fdf2fa903d000df01ef7e`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 2.2 MB (2211447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e003813362a92e41a38ce899360dfc51977add71013d1cac48643e6d9361ec43`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b9b40076d0562644d2bec445a0a7fdefbf4dd5d545c7d8cbdfef18f171b99a`  
		Last Modified: Fri, 08 May 2026 20:29:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41` - unknown; unknown

```console
$ docker pull memcached@sha256:d83c846fc98d19ba355a9a5d1c59147c565e7894fed7c5b582bd5b4bde92d90d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6056bef38756043ff8218f82594c154e80dc8d2097dd770a7bd7bb09a8e6e3e6`

```dockerfile
```

-	Layers:
	-	`sha256:4b4fd92902f7c83c67f43e813275bc5676ec6370639df11fe1394ce7fa7eef2d`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 2.0 MB (2011329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d8b1829f761528fa20afdac852bde73a128edf4c6f11e990f7e7c7fcbcfbf61`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41` - linux; arm variant v7

```console
$ docker pull memcached@sha256:3d1cfa4c23d23705cf3f8b9302ff26048e2ac216027f45be24e93b8f0817a952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28516943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:582f213c6b868ce82f6e14b78c661812d0781e91331e3ca32ce462777a0529fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:16:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 19:16:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:19:15 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 19:19:15 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 19:19:15 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 19:19:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 19:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:19:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:19:15 GMT
USER memcache
# Fri, 08 May 2026 19:19:15 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 19:19:15 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f1433620eadfdfe016c8054b954f619ae5bca159f35a9459c36a76d9ef4d39c3`  
		Last Modified: Fri, 08 May 2026 18:37:58 GMT  
		Size: 26.2 MB (26214912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851a3dc4d05ac8ea75d436c9d8de99f7ca3c80f159cadffd985253ae10a40069`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18a5b288c05e8d152bf1530b1c4248c0ea5c08902853e0955c6838d5d418b33`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 135.4 KB (135388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff024d65a6401c67cefb240a3ef3d181382530d66cfbb03f13ff32d81500525`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 2.2 MB (2165127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0613bb171f6d5dee88871aafa9a91daf991e3d262feb8682aa8fb5696046579`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c1a297997b8b44cdcad29c590e65efa7934da84dacae1fbddd2b017bb0dd03`  
		Last Modified: Fri, 08 May 2026 19:19:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41` - unknown; unknown

```console
$ docker pull memcached@sha256:e7210267977b9ce03df4bc38f1d1ea5760217f9f582f392ac648876a13580041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120a3ae5c0ce21313dc99a5a24a7d9ae48f434e40717325fda7675fc368c3a9e`

```dockerfile
```

-	Layers:
	-	`sha256:b2f6d69af7f79690357135d68c570ab105358d093cb3ef2b6b37d8c0c4b8766a`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 2.0 MB (2009786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19ecae093d7ef811fe61bf6ed6706bf88a86ab363852e511e19d077fea8bdf22`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:4a47319c5ea763766ec14f7f49c71294e7621973dbf1d934330b273a50d86ae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32560787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea04a0e8415a1e901722a2dc626f036034b99c11dd819b6aab54fe2172610825`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:21:07 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 19:21:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:24:08 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 19:24:08 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 19:24:08 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 19:24:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 19:24:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:24:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:24:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:24:08 GMT
USER memcache
# Fri, 08 May 2026 19:24:08 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 19:24:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73f16d12b26b60a37ae242c9f12503fa0bb655f780014ce964bf39b960ea39a`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f45dfab4b00618ca4983d73b6acabb6fe1e056339b0cafcc1c0268303c02b89`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 153.5 KB (153496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91da4495c7aeb14802d9e2f3854b2226395b2886efcb91a3f91778774632602`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 2.3 MB (2262131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91f17f562e485ed0d6523251b77ca57f1df60d00243de97a13459b077fb30df`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70d0b5c5805a6bd639b55f25e9fb45c11035876f9fca3e2ab607fb2d818b01f`  
		Last Modified: Fri, 08 May 2026 19:24:15 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41` - unknown; unknown

```console
$ docker pull memcached@sha256:003da519f1303287f7dbac93d59fd8f7cd3bd4f7c1c3f59e2ea25f3e1933a4a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b34e9510fcd3b35da3965f941f9c4d3bdf0eff1c30985a7ce5621b638e4c237e`

```dockerfile
```

-	Layers:
	-	`sha256:6041a557446d392656291f000150951d92c8392a387515be5c7e384d175a1967`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 2.0 MB (2008642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e39754d938ea3671f3babce3fbab5d612247a51cbc9f172de306c3fcf60e3a1b`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41` - linux; 386

```console
$ docker pull memcached@sha256:ae0c2a4ef3d5a1336f8204efdb14230b37402d5f8c4096295ddd0f53b7e041ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33670271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d71af2d7fff4e8bb864857f69883ac131a512bb9311bb23de7031cb892e38a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:17:17 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 19:17:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:20:22 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 19:20:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 19:20:22 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 19:20:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 19:20:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:20:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:20:22 GMT
USER memcache
# Fri, 08 May 2026 19:20:22 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 19:20:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:43e2ffbaa23260ffb4e3de716920f2ed9e6af56e465ca1233a2d84c2cc1cf005`  
		Last Modified: Fri, 08 May 2026 18:32:48 GMT  
		Size: 31.3 MB (31296400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2ce2fa16a9ab3457f94c9628fc05a5fd6d54e5d6d3d8a9e1e506ba4e5a37aa`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540be255286e8d861d09681ddd0cd64a25a1b5fa161cca9b859487c03bfb0b6e`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 147.5 KB (147521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913676b9d51d935a10d363087959dec4494fbae5fdf82b80b84e9ecaae370ad3`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 2.2 MB (2224836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224690b120957a082d3ef84ebd501af44b1437fdbf4fcefad6e8faee78e234a5`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d0c777c8b52f9e74da7bf3fd5be45dbd51ab10be8dde37fea12fc96f59cd09`  
		Last Modified: Fri, 08 May 2026 19:20:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41` - unknown; unknown

```console
$ docker pull memcached@sha256:15a21e26469f168e5a065467f48dfed23a1a06d5e0d2b6ffdfcfcc38ff62a560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c3412186834b790b4fbbad4cfe5adfd0f39d11688631b5059120339ee474dc`

```dockerfile
```

-	Layers:
	-	`sha256:ffb482f3d82d9bd4136d15e9b8e08adece9f35076c719e0288e1de86156221e4`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 2.0 MB (2005483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe947a7402c9e03fc064053a531c1cecc9c253a0235c40625608b22c9a860d2f`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41` - linux; ppc64le

```console
$ docker pull memcached@sha256:fb4333344bfd32af4cefd042b89dff6ea8ba4bc5ab8168cbe3d29f8c9da5566a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36164277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d865655c5194d1b0446688e3b4f406d0d233869ddf3dcc2b4863b7a8721f32f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:35:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 20:35:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:38:30 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 20:38:30 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 20:38:30 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 20:38:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 20:38:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:38:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 20:38:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 20:38:31 GMT
USER memcache
# Fri, 08 May 2026 20:38:31 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 20:38:31 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2805acf219c32faae551498121eb47f3d7d32bc2a908969bd1ac04c3f49017fe`  
		Last Modified: Fri, 08 May 2026 20:38:41 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278e7e1caa6b74657254421ed3e5193837e9b6f3dde9e041e7e95383e6e68443`  
		Last Modified: Fri, 08 May 2026 20:38:42 GMT  
		Size: 170.4 KB (170351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df05fb319f87f70759df5de69b2f40702ca122c47d614f2f8861ce256eb0b61`  
		Last Modified: Fri, 08 May 2026 20:38:42 GMT  
		Size: 2.4 MB (2394326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f6a1fd9b6e9a261288b936182122f173180b726d490646ee6164ae5c95d84c`  
		Last Modified: Fri, 08 May 2026 20:38:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b93469fb91621a5f46b7dd80327995f9ca6d8361137dbe55159ef455e2976c`  
		Last Modified: Fri, 08 May 2026 20:38:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41` - unknown; unknown

```console
$ docker pull memcached@sha256:e82c5b578718de9c7774bc11902f22157b7c49e1a253ddfe0e3496d4a461d760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89bf5432c3d996440e1d10de68af644b31627fdeeac778ee395c95a88263010a`

```dockerfile
```

-	Layers:
	-	`sha256:8a5017f90fa8e1dd648f24d4c3fa871a8dc77b8e529fe26ee3f0034a79bdd955`  
		Last Modified: Fri, 08 May 2026 20:38:42 GMT  
		Size: 2.0 MB (2011927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e26de34ce99baa5e3d603d8a2dddfc874c4b7cf85ae36baf53e81232916879a8`  
		Last Modified: Fri, 08 May 2026 20:38:41 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41` - linux; riscv64

```console
$ docker pull memcached@sha256:5ddab235954c3cde3c815b6a5be674885381502972ebc53794c4811df335843c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30623277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b6d17550b0133cd405553af720539d51b95b0d50475bbcdbf6c2173bd5280b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 16:09:52 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 09 May 2026 16:10:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 16:23:27 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 09 May 2026 16:23:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 09 May 2026 16:23:27 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 09 May 2026 16:23:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 09 May 2026 16:23:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 09 May 2026 16:23:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 09 May 2026 16:23:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 09 May 2026 16:23:28 GMT
USER memcache
# Sat, 09 May 2026 16:23:28 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 09 May 2026 16:23:28 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1e9edef871271ebe58c5a713c7c062e88ff414be0976a2c7baf0aba83823c954`  
		Last Modified: Fri, 08 May 2026 20:38:39 GMT  
		Size: 28.3 MB (28280232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9888105b7154ad185e8f5227e002ba1af0f905cba713450e54261fb929e80afe`  
		Last Modified: Sat, 09 May 2026 16:24:13 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea9dc216a8ac7e5ff5123e9cec2e0c1650d9afc96015312e8f304adc6c255a0`  
		Last Modified: Sat, 09 May 2026 16:24:13 GMT  
		Size: 133.1 KB (133086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e544f8419fe19b80d411a515c9201c8c35d068e9a3ff1127e23e53c495a036c9`  
		Last Modified: Sat, 09 May 2026 16:24:13 GMT  
		Size: 2.2 MB (2208450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b939f3eba847b32e2c08af32b5870190d0195179c8dfcfba89b9abd0d24865b8`  
		Last Modified: Sat, 09 May 2026 16:24:13 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0a4092dbf93f8a2db331d4bb00d34313567e7245e5753310064f99299a2919`  
		Last Modified: Sat, 09 May 2026 16:24:14 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41` - unknown; unknown

```console
$ docker pull memcached@sha256:84361ecaeb53a4b02619fac3c96e92f016548a953b0bb4909dbce2605c50c27e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e712edaa1f4a23a51ec2552dadfb1ba38310fc63ac1066e30c4ccd5f2d388ce8`

```dockerfile
```

-	Layers:
	-	`sha256:b27196635d6011055da056ccc202d4d6df3c0d9296b913ab5b40505f5efb56b9`  
		Last Modified: Sat, 09 May 2026 16:24:13 GMT  
		Size: 2.0 MB (2002290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f31718fda9bdd1f0330201f0a2069f169fd2f79967b828cb3138dad392f06e0d`  
		Last Modified: Sat, 09 May 2026 16:24:12 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41` - linux; s390x

```console
$ docker pull memcached@sha256:7f194d0409eee2a5b0bb8903485384802c30d3e8f3db4edc714dccedd365197b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32280599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71da9b051066a3ea5be228e76446413fcc99d1b892a8e007445d21d95254a5d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:18:08 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 19:18:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:21:32 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 19:21:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 19:21:32 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 19:21:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 19:21:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:21:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:21:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:21:32 GMT
USER memcache
# Fri, 08 May 2026 19:21:32 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 19:21:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875e7d47d55cac3b3811a3503e8330c2b49b3264583a0e3ffbc8380fe58dd8d3`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e487f7a355c714fc8533d060a278791698afaed2353417768b8f02bd7844e06`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 140.5 KB (140519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6bb469173a6734f9ba49a4aa2f9a1d3e6513740633df30a2d3bc37c3b9d4279`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 2.3 MB (2298219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7e59c6d93f04c1f009cbda35d2e5b25d8087cadff3126c5de7636d0c10b5c0`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa99c508f7dc7874b69603543390bb5c9a5b3bb0689bde04f6d7d53db1ce25bd`  
		Last Modified: Fri, 08 May 2026 19:21:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41` - unknown; unknown

```console
$ docker pull memcached@sha256:b257f9c0883422f85a5c40a24940bb3401de8aac9c08bc12a87f5732d143082c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff10b6e9f782a5c6eee93b5e143ea12b75800a8ef331ebc5d73519e32464d829`

```dockerfile
```

-	Layers:
	-	`sha256:3f4b79e225835bdf97992cd4741626b92fb8ad5438feb251afbf7d6bb442a01d`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 2.0 MB (2009763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff63eebb23b55a364393e4d41fbc25ca8e9a760278a9403379c7fb549f8a1248`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.41-alpine`

```console
$ docker pull memcached@sha256:65c80b311a9601ef5ca8af3814e5cd06a9c4277ea139d80bd53da6b4d39eb46e
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

### `memcached:1.6.41-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:7b962825022657b112923d502400d5734870d5eb12c19e7f1f6585f7534a6795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5959872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b58f7e71f30daaa3f466fa31d855fddb7101e42c0c42fac520be5d1d43ec32e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:46 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:47 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:20:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:20:22 GMT
USER memcache
# Wed, 15 Apr 2026 20:20:22 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:20:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73d5ffe265b83073ce3c7211fb3c15ebbd5e7146d870d9ce69d2e7dfc493348`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cb4fdd95ced0d5a9528e97ff0f20742749cbd9ef6dc1322d13e682a7085a67`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 106.1 KB (106063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe17fc291d9444fbae93d7f45eab008318f87302c016c06e6e911c1a571a053`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 2.0 MB (1988274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1948bd131d2cbd05c6bf2962d18b15d105abee6f42f398bab3c13737537f197`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bde8ceae30a2a0890715bbc591167ee301c57d7f75023e80be460035187def`  
		Last Modified: Wed, 15 Apr 2026 20:20:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:58ed333482f8a8530c82ad7399d5917a7db85fbcdf70fc1dec55fbedcdf09253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4255278359004afd8c94db1a7fe6129fc984d0716c33665c9eca3168476fdcb`

```dockerfile
```

-	Layers:
	-	`sha256:5f47d88d89d22d065a3590d477ae130520b882176ab07e95862afb4d8b69b214`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 94.9 KB (94901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab2d532e4a6ce2f362d25c79dfaeb88d333fe6efe7c1b5b293630bf6ca292eb8`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 20.5 KB (20530 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:47a06cd0daead339b96ed90e425336a8a49a75e4e358b5ec1ea63a630720f704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3947facc9e9fae3eee283f24b611a8ae87e353b6d6447bc6f582e90f2fce3743`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:58 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:21:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:21:03 GMT
USER memcache
# Wed, 15 Apr 2026 20:21:03 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:21:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77001163fdaab47f07a85fc5bb15f3512a8cb9b9b049cec7e0c88bcbbdb5bb5d`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee1b43c0cfbf2ee56e39441933ff06803264d22918fe867d8b5ba7d5adfb9c3`  
		Last Modified: Wed, 15 Apr 2026 20:21:06 GMT  
		Size: 102.6 KB (102630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c041bfac12e599ad87749289dec9672dac36e8c0e16779f13fa695d10f2f0cc5`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 1.9 MB (1937835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2dfd492dd0f295311a0c314fae06f4b325ae22cb0e673a53e0705f3d4e0504`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671c66eac839c2f0a5b2e64d1f581069c4cdf119e784bff16540ecc94e2c2b10`  
		Last Modified: Wed, 15 Apr 2026 20:21:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2a6148a6aebb042e55781b40ed626d0c5871833be4ae8dc303af7aace07d9d60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbaadfaacfaf0e7c226b35236bb84c2268d4c6eb017efd435a3999a44edfcc77`

```dockerfile
```

-	Layers:
	-	`sha256:c68bb3ee35fc0ac716bca45cc759f3b1ff52b1d5a0acae9876eaf0aa55aa667d`  
		Last Modified: Wed, 15 Apr 2026 20:21:06 GMT  
		Size: 20.5 KB (20466 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:fb58bae12ffa00c9cbafc8bee2341b43ffdccacbde7085fa707ef6c7f2d69e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd4e85c30e4df5803b553b8a7f84084c3dae6f72531ac70fcabf7099cfa8148`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:14:38 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 21:14:39 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 21:17:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:17:34 GMT
USER memcache
# Wed, 15 Apr 2026 21:17:34 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 21:17:34 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e312136cfedda9620407d42650d0595220e60d3c40ae8853bfbdd83f392b9e6`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53697a39f37b691917c91310ac4e107308674bddcc9017e3bbc0d0134eaf4c3e`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 92.4 KB (92369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5e4be9e0df543f152c376fe2cc74b89b75585793fdbd7d12476737d386d8e1`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 1.9 MB (1896191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a083f41edf5f859feb4367eeeea0955dc9799c8202fb8a67c40915ed5b195002`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c43503b1f4f42ffc5e0e4415befe45199dec730bc26347df151298345ba640`  
		Last Modified: Wed, 15 Apr 2026 21:17:40 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7535cf6b6a140771131c2c524301d4616f34856fcd8ecbe3e52300108c49de2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d73c906894a0a3d178edd69991f310225c0daef314e6faa83a0b9adecfbeb34`

```dockerfile
```

-	Layers:
	-	`sha256:8f1fddd7d14560fb90f381b09cde9302dfc9253e6702adf28c55961d755b1ad8`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 94.3 KB (94319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fcf119d246607aa25330c4c05fe14a64cebda69b02d14507862a9f07c1404e6`  
		Last Modified: Wed, 15 Apr 2026 21:17:38 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:6d70439467a65065c52894232a3085c724da2810a9b3205130d5e434ab411e3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6288798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4be3e105216d2507b68e772f7d08d52a5076dd55fad35c29775038d05c24112`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:15:23 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:15:24 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:18:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:18:13 GMT
USER memcache
# Wed, 15 Apr 2026 20:18:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:18:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81758f5fc2e8fa13e3625f253d7c999560ac666121c026f7251dbfb919cca611`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d735737d3a0cf1eda63bd72c09f64eb679313e9c5f8a105849848bdd779e1d`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 121.8 KB (121846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ac0921d2cc2b3388e0f006a6672c5a9e1098a59e570121dde092104d845c51`  
		Last Modified: Wed, 15 Apr 2026 20:18:19 GMT  
		Size: 2.0 MB (1965733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca9cf731b18a76c3ac25cc3add219660d57516c12680d7b1f1ece282406eb82`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717a6b23dd1cd76b686bf26066af23265e0d002ed6a3e87f6aa4f79264b7da11`  
		Last Modified: Wed, 15 Apr 2026 20:18:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7e5232b868d3222e3ce2b0ee39c62f6cb294bea27456b00940fbc4e3c8c3f84d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:780bf975a24d5fdc511c857720c04cb077d64abcfe4c93ea0db7c9487c323718`

```dockerfile
```

-	Layers:
	-	`sha256:addb0f46e3b5adb674175c11fc85526d4628e24d74d210c8b00c9a945b44407c`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 94.4 KB (94355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3364e418b74b6f6ca17deec7d55783a6e1554de3783ab0a6d5e56496d935ddb0`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-alpine` - linux; 386

```console
$ docker pull memcached@sha256:80328bf779fa1494f7677b441ad1c16c2134f126e6556953deb3cfab1c4c9770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5744816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d957405dd0811f1cd15fe39563938a60c2008204d2f63ebc7e39f8989c796f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:20:45 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 22:20:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 22:23:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 22:23:32 GMT
USER memcache
# Wed, 15 Apr 2026 22:23:32 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 22:23:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0617a09eee85c2032f5596ded56b733366513074f9096177315b50dc45485e20`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c67275dbc381ac3ae0b21dda20edaf245e2ca54d6f5dc3af8805db03c17cc93`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 110.7 KB (110715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6ecb23f1f4bc89d5c315aac493f29fe7bb33061c70d926c904f4f55d374461`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 1.9 MB (1942309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e782df8f482a58603ea70ef9e04e838d044a6070c7e4cd116c90a09b917ed940`  
		Last Modified: Wed, 15 Apr 2026 22:23:38 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616df56d574e39c00ae772c6a29e2b724698048a83cc29ea17049573f9073b10`  
		Last Modified: Wed, 15 Apr 2026 22:23:38 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c726e7abf461d963e544818339e4cd12fd2f31e41436475f0e51818a0885fbdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12e41b9d6f745d686c2649255bd14fe4e0b97a3477d383e719490e5ef66b27ae`

```dockerfile
```

-	Layers:
	-	`sha256:b44003cd1ea209090a063c5abfb4ee881849abba47e8711191b7637f86d8ee8b`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 94.9 KB (94856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f431de53d9b6c7e2cbc847af9daec064d061f8bd625615734012051336c495a`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 20.5 KB (20472 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:8182e35a9a404f0b522cb3c176d3dc4aade974e5556184c0a5a19e800721868a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6034321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c6f532e81b50ea71c3520a80da0c8154b4cb14ebc17f87eb3a026862b47ed8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:43 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:20:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:20:22 GMT
USER memcache
# Wed, 15 Apr 2026 20:20:22 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:20:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee88d1c88fa46aa906a297c2919c9a085e74d04f20e4f827ca240a20f10ad34`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c574329cc1ebf156e2d89ab608bd58a3c0db550845c0ec394d265aa98fc5c4`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 126.3 KB (126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2a28510bcba91734e7b38682847296011b63458db8a87a4bcecd180b8de7b5`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 2.1 MB (2075767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c524eb15ef0a41bf969efc93ef579db92dc59e8df57c9abfd099e7f6ff0756`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bde8ceae30a2a0890715bbc591167ee301c57d7f75023e80be460035187def`  
		Last Modified: Wed, 15 Apr 2026 20:20:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:4051408ef6c5bf4d4f37abf19c13f0298d8baa81770fcbfb588221e49e3bb834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec3a4d49e6f325e484db43c9c9981f4eaa0223d9ae98282d95c3ee20c2089cb`

```dockerfile
```

-	Layers:
	-	`sha256:0e4e65db585f857844a67a831eb876dbb0a8a40d9269393d6c0fa83a2df995ae`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 94.3 KB (94308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50f58ec8aff3c96cc7b58e689122c27ee26121c598034cdc59ec95fd6423effe`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:f3209d1ca2c4ce827614d16445231d96372944d218f18fd22850eec83874e5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5772332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e30170e0826b89d0ca59ffcae54b850ded07e6ae9451ecf1fd60f3ca8adcc725`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 00:00:48 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 16 Apr 2026 00:00:52 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Thu, 16 Apr 2026 00:14:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 16 Apr 2026 00:14:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Apr 2026 00:14:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 16 Apr 2026 00:14:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Apr 2026 00:14:22 GMT
USER memcache
# Thu, 16 Apr 2026 00:14:22 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 16 Apr 2026 00:14:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62b143e34f5b89277e3a88ed4d722339d188a094d4bb534e222ca80e7741031`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfff7c64f831ba03c491874cdf9a1c3f42bff72bb0e1951c63d8cf718854cff`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 108.9 KB (108903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69aef1050272a61cfbfd97c041d3776f96bdd03b102f2c3c54bbb0af2e1235a5`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 2.1 MB (2074414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ce340fb37f86db0d3aa774c23880b7c8322d2af8e3adc27a6ffa25d67c2122`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e40c6fb92d819994d38fae7accdffd583465eb6e645834b66f3ce9f0562f69`  
		Last Modified: Thu, 16 Apr 2026 00:14:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2caae198d1efb7d4df14da45a3ff360a697982b544a61a3f907076b414983ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1503bd38f4b30bc91be18dd93359e7376a9da1c7cb652ade64efd154064543fe`

```dockerfile
```

-	Layers:
	-	`sha256:e2d79fb634d76e28f055ab09953f59c371b93599e2b79f20f3d758f2c9520118`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 94.3 KB (94304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3614ad9b1715c3d6aa488496fca74d7143ea095d227f599407c933c62ec266aa`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 20.6 KB (20604 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:1da27660ae89a83aaf603e1affd51be573e5b8dac6c07ed592aee2a3a2b20581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5859702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13aa64df69a308e46b054bbd8e7a5d2f1e079005771f61748dae0d049889ba7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:14:40 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:14:41 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:17:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:17:58 GMT
USER memcache
# Wed, 15 Apr 2026 20:17:58 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:17:58 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c42733e5f451590186b9b76c4b374ae5a84b657f7f1fd405647f5ba82c65bcd`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a14431ac88e8fe205b07f09b7e4843bb254de41cbc044725d6eaee3c2f822f`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 114.3 KB (114293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6377b7d98f32173cd47682aa73b32e4eba42781fa9224b9eb7a6f87367d37f94`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 2.0 MB (2017525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d022ae992296922747a4b69694b0185a0ce1f6cdece7f794e39e74dab92d250`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255cb3a435cbd623c1235d0429160faf72c244a6c1a613525df36f58a8c1f784`  
		Last Modified: Wed, 15 Apr 2026 20:18:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:531ee140f06db77d73b71bce7339abec3c6d976092bb80542bb337bb406acdbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b17d6f7e71efe3ee05ebcdb8ae90c28cf60db9ef069b0a98fe442c949740a6c`

```dockerfile
```

-	Layers:
	-	`sha256:820a080f49bf9e33948dbe5c13f6254f135d90bcb2b2277e3d2fd2430626c1a2`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 94.2 KB (94250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8ab82f4f240f46f9e34b74691925ab4af7f1cbb12ad3cb8639e0f317cf06653`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.41-alpine3.23`

```console
$ docker pull memcached@sha256:65c80b311a9601ef5ca8af3814e5cd06a9c4277ea139d80bd53da6b4d39eb46e
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

### `memcached:1.6.41-alpine3.23` - linux; amd64

```console
$ docker pull memcached@sha256:7b962825022657b112923d502400d5734870d5eb12c19e7f1f6585f7534a6795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5959872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b58f7e71f30daaa3f466fa31d855fddb7101e42c0c42fac520be5d1d43ec32e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:46 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:47 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:20:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:20:22 GMT
USER memcache
# Wed, 15 Apr 2026 20:20:22 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:20:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73d5ffe265b83073ce3c7211fb3c15ebbd5e7146d870d9ce69d2e7dfc493348`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cb4fdd95ced0d5a9528e97ff0f20742749cbd9ef6dc1322d13e682a7085a67`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 106.1 KB (106063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe17fc291d9444fbae93d7f45eab008318f87302c016c06e6e911c1a571a053`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 2.0 MB (1988274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1948bd131d2cbd05c6bf2962d18b15d105abee6f42f398bab3c13737537f197`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bde8ceae30a2a0890715bbc591167ee301c57d7f75023e80be460035187def`  
		Last Modified: Wed, 15 Apr 2026 20:20:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:58ed333482f8a8530c82ad7399d5917a7db85fbcdf70fc1dec55fbedcdf09253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4255278359004afd8c94db1a7fe6129fc984d0716c33665c9eca3168476fdcb`

```dockerfile
```

-	Layers:
	-	`sha256:5f47d88d89d22d065a3590d477ae130520b882176ab07e95862afb4d8b69b214`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 94.9 KB (94901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab2d532e4a6ce2f362d25c79dfaeb88d333fe6efe7c1b5b293630bf6ca292eb8`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 20.5 KB (20530 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-alpine3.23` - linux; arm variant v6

```console
$ docker pull memcached@sha256:47a06cd0daead339b96ed90e425336a8a49a75e4e358b5ec1ea63a630720f704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3947facc9e9fae3eee283f24b611a8ae87e353b6d6447bc6f582e90f2fce3743`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:58 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:21:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:21:03 GMT
USER memcache
# Wed, 15 Apr 2026 20:21:03 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:21:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77001163fdaab47f07a85fc5bb15f3512a8cb9b9b049cec7e0c88bcbbdb5bb5d`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee1b43c0cfbf2ee56e39441933ff06803264d22918fe867d8b5ba7d5adfb9c3`  
		Last Modified: Wed, 15 Apr 2026 20:21:06 GMT  
		Size: 102.6 KB (102630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c041bfac12e599ad87749289dec9672dac36e8c0e16779f13fa695d10f2f0cc5`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 1.9 MB (1937835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2dfd492dd0f295311a0c314fae06f4b325ae22cb0e673a53e0705f3d4e0504`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671c66eac839c2f0a5b2e64d1f581069c4cdf119e784bff16540ecc94e2c2b10`  
		Last Modified: Wed, 15 Apr 2026 20:21:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:2a6148a6aebb042e55781b40ed626d0c5871833be4ae8dc303af7aace07d9d60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbaadfaacfaf0e7c226b35236bb84c2268d4c6eb017efd435a3999a44edfcc77`

```dockerfile
```

-	Layers:
	-	`sha256:c68bb3ee35fc0ac716bca45cc759f3b1ff52b1d5a0acae9876eaf0aa55aa667d`  
		Last Modified: Wed, 15 Apr 2026 20:21:06 GMT  
		Size: 20.5 KB (20466 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-alpine3.23` - linux; arm variant v7

```console
$ docker pull memcached@sha256:fb58bae12ffa00c9cbafc8bee2341b43ffdccacbde7085fa707ef6c7f2d69e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd4e85c30e4df5803b553b8a7f84084c3dae6f72531ac70fcabf7099cfa8148`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:14:38 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 21:14:39 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 21:17:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:17:34 GMT
USER memcache
# Wed, 15 Apr 2026 21:17:34 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 21:17:34 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e312136cfedda9620407d42650d0595220e60d3c40ae8853bfbdd83f392b9e6`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53697a39f37b691917c91310ac4e107308674bddcc9017e3bbc0d0134eaf4c3e`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 92.4 KB (92369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5e4be9e0df543f152c376fe2cc74b89b75585793fdbd7d12476737d386d8e1`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 1.9 MB (1896191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a083f41edf5f859feb4367eeeea0955dc9799c8202fb8a67c40915ed5b195002`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c43503b1f4f42ffc5e0e4415befe45199dec730bc26347df151298345ba640`  
		Last Modified: Wed, 15 Apr 2026 21:17:40 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:7535cf6b6a140771131c2c524301d4616f34856fcd8ecbe3e52300108c49de2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d73c906894a0a3d178edd69991f310225c0daef314e6faa83a0b9adecfbeb34`

```dockerfile
```

-	Layers:
	-	`sha256:8f1fddd7d14560fb90f381b09cde9302dfc9253e6702adf28c55961d755b1ad8`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 94.3 KB (94319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fcf119d246607aa25330c4c05fe14a64cebda69b02d14507862a9f07c1404e6`  
		Last Modified: Wed, 15 Apr 2026 21:17:38 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:6d70439467a65065c52894232a3085c724da2810a9b3205130d5e434ab411e3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6288798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4be3e105216d2507b68e772f7d08d52a5076dd55fad35c29775038d05c24112`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:15:23 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:15:24 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:18:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:18:13 GMT
USER memcache
# Wed, 15 Apr 2026 20:18:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:18:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81758f5fc2e8fa13e3625f253d7c999560ac666121c026f7251dbfb919cca611`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d735737d3a0cf1eda63bd72c09f64eb679313e9c5f8a105849848bdd779e1d`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 121.8 KB (121846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ac0921d2cc2b3388e0f006a6672c5a9e1098a59e570121dde092104d845c51`  
		Last Modified: Wed, 15 Apr 2026 20:18:19 GMT  
		Size: 2.0 MB (1965733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca9cf731b18a76c3ac25cc3add219660d57516c12680d7b1f1ece282406eb82`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717a6b23dd1cd76b686bf26066af23265e0d002ed6a3e87f6aa4f79264b7da11`  
		Last Modified: Wed, 15 Apr 2026 20:18:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:7e5232b868d3222e3ce2b0ee39c62f6cb294bea27456b00940fbc4e3c8c3f84d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:780bf975a24d5fdc511c857720c04cb077d64abcfe4c93ea0db7c9487c323718`

```dockerfile
```

-	Layers:
	-	`sha256:addb0f46e3b5adb674175c11fc85526d4628e24d74d210c8b00c9a945b44407c`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 94.4 KB (94355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3364e418b74b6f6ca17deec7d55783a6e1554de3783ab0a6d5e56496d935ddb0`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-alpine3.23` - linux; 386

```console
$ docker pull memcached@sha256:80328bf779fa1494f7677b441ad1c16c2134f126e6556953deb3cfab1c4c9770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5744816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d957405dd0811f1cd15fe39563938a60c2008204d2f63ebc7e39f8989c796f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:20:45 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 22:20:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 22:23:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 22:23:32 GMT
USER memcache
# Wed, 15 Apr 2026 22:23:32 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 22:23:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0617a09eee85c2032f5596ded56b733366513074f9096177315b50dc45485e20`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c67275dbc381ac3ae0b21dda20edaf245e2ca54d6f5dc3af8805db03c17cc93`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 110.7 KB (110715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6ecb23f1f4bc89d5c315aac493f29fe7bb33061c70d926c904f4f55d374461`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 1.9 MB (1942309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e782df8f482a58603ea70ef9e04e838d044a6070c7e4cd116c90a09b917ed940`  
		Last Modified: Wed, 15 Apr 2026 22:23:38 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616df56d574e39c00ae772c6a29e2b724698048a83cc29ea17049573f9073b10`  
		Last Modified: Wed, 15 Apr 2026 22:23:38 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:c726e7abf461d963e544818339e4cd12fd2f31e41436475f0e51818a0885fbdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12e41b9d6f745d686c2649255bd14fe4e0b97a3477d383e719490e5ef66b27ae`

```dockerfile
```

-	Layers:
	-	`sha256:b44003cd1ea209090a063c5abfb4ee881849abba47e8711191b7637f86d8ee8b`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 94.9 KB (94856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f431de53d9b6c7e2cbc847af9daec064d061f8bd625615734012051336c495a`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 20.5 KB (20472 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-alpine3.23` - linux; ppc64le

```console
$ docker pull memcached@sha256:8182e35a9a404f0b522cb3c176d3dc4aade974e5556184c0a5a19e800721868a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6034321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c6f532e81b50ea71c3520a80da0c8154b4cb14ebc17f87eb3a026862b47ed8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:43 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:20:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:20:22 GMT
USER memcache
# Wed, 15 Apr 2026 20:20:22 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:20:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee88d1c88fa46aa906a297c2919c9a085e74d04f20e4f827ca240a20f10ad34`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c574329cc1ebf156e2d89ab608bd58a3c0db550845c0ec394d265aa98fc5c4`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 126.3 KB (126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2a28510bcba91734e7b38682847296011b63458db8a87a4bcecd180b8de7b5`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 2.1 MB (2075767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c524eb15ef0a41bf969efc93ef579db92dc59e8df57c9abfd099e7f6ff0756`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bde8ceae30a2a0890715bbc591167ee301c57d7f75023e80be460035187def`  
		Last Modified: Wed, 15 Apr 2026 20:20:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:4051408ef6c5bf4d4f37abf19c13f0298d8baa81770fcbfb588221e49e3bb834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec3a4d49e6f325e484db43c9c9981f4eaa0223d9ae98282d95c3ee20c2089cb`

```dockerfile
```

-	Layers:
	-	`sha256:0e4e65db585f857844a67a831eb876dbb0a8a40d9269393d6c0fa83a2df995ae`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 94.3 KB (94308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50f58ec8aff3c96cc7b58e689122c27ee26121c598034cdc59ec95fd6423effe`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-alpine3.23` - linux; riscv64

```console
$ docker pull memcached@sha256:f3209d1ca2c4ce827614d16445231d96372944d218f18fd22850eec83874e5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5772332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e30170e0826b89d0ca59ffcae54b850ded07e6ae9451ecf1fd60f3ca8adcc725`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 00:00:48 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 16 Apr 2026 00:00:52 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Thu, 16 Apr 2026 00:14:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 16 Apr 2026 00:14:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Apr 2026 00:14:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 16 Apr 2026 00:14:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Apr 2026 00:14:22 GMT
USER memcache
# Thu, 16 Apr 2026 00:14:22 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 16 Apr 2026 00:14:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62b143e34f5b89277e3a88ed4d722339d188a094d4bb534e222ca80e7741031`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfff7c64f831ba03c491874cdf9a1c3f42bff72bb0e1951c63d8cf718854cff`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 108.9 KB (108903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69aef1050272a61cfbfd97c041d3776f96bdd03b102f2c3c54bbb0af2e1235a5`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 2.1 MB (2074414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ce340fb37f86db0d3aa774c23880b7c8322d2af8e3adc27a6ffa25d67c2122`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e40c6fb92d819994d38fae7accdffd583465eb6e645834b66f3ce9f0562f69`  
		Last Modified: Thu, 16 Apr 2026 00:14:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:2caae198d1efb7d4df14da45a3ff360a697982b544a61a3f907076b414983ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1503bd38f4b30bc91be18dd93359e7376a9da1c7cb652ade64efd154064543fe`

```dockerfile
```

-	Layers:
	-	`sha256:e2d79fb634d76e28f055ab09953f59c371b93599e2b79f20f3d758f2c9520118`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 94.3 KB (94304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3614ad9b1715c3d6aa488496fca74d7143ea095d227f599407c933c62ec266aa`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 20.6 KB (20604 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-alpine3.23` - linux; s390x

```console
$ docker pull memcached@sha256:1da27660ae89a83aaf603e1affd51be573e5b8dac6c07ed592aee2a3a2b20581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5859702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13aa64df69a308e46b054bbd8e7a5d2f1e079005771f61748dae0d049889ba7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:14:40 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:14:41 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:17:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:17:58 GMT
USER memcache
# Wed, 15 Apr 2026 20:17:58 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:17:58 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c42733e5f451590186b9b76c4b374ae5a84b657f7f1fd405647f5ba82c65bcd`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a14431ac88e8fe205b07f09b7e4843bb254de41cbc044725d6eaee3c2f822f`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 114.3 KB (114293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6377b7d98f32173cd47682aa73b32e4eba42781fa9224b9eb7a6f87367d37f94`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 2.0 MB (2017525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d022ae992296922747a4b69694b0185a0ce1f6cdece7f794e39e74dab92d250`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255cb3a435cbd623c1235d0429160faf72c244a6c1a613525df36f58a8c1f784`  
		Last Modified: Wed, 15 Apr 2026 20:18:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:531ee140f06db77d73b71bce7339abec3c6d976092bb80542bb337bb406acdbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b17d6f7e71efe3ee05ebcdb8ae90c28cf60db9ef069b0a98fe442c949740a6c`

```dockerfile
```

-	Layers:
	-	`sha256:820a080f49bf9e33948dbe5c13f6254f135d90bcb2b2277e3d2fd2430626c1a2`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 94.2 KB (94250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8ab82f4f240f46f9e34b74691925ab4af7f1cbb12ad3cb8639e0f317cf06653`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.41-trixie`

```console
$ docker pull memcached@sha256:f7a252e7ba3fbbe9672c483354c5081d02b780122c3bb97bd311d5662b54d0ad
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

### `memcached:1.6.41-trixie` - linux; amd64

```console
$ docker pull memcached@sha256:5f9197399e5aefcabef61b7c94d4e9578698e4a0ac391f6a4b34eb0dcd493df2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32198719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5474f3cc4ab6f46b8613ec8b77a7c6ec75f3b8944c8674fa5c02be437ee6567b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:22:04 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 19:22:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:24:53 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 19:24:53 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 19:24:53 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 19:24:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 19:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:24:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:24:54 GMT
USER memcache
# Fri, 08 May 2026 19:24:54 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 19:24:54 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95946911721deafff321fd508db9ba36e3babc47097ecd6c6bdf2ba0dd470257`  
		Last Modified: Fri, 08 May 2026 19:24:59 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2951237283f3070819f0121ee72d97873d9e5287f4ff5cd5b450147eb57c72`  
		Last Modified: Fri, 08 May 2026 19:24:59 GMT  
		Size: 136.7 KB (136676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f29d81d44c4b3a8bb7866171f79f5054acda551367bbcf5ae523080623b437d`  
		Last Modified: Fri, 08 May 2026 19:25:00 GMT  
		Size: 2.3 MB (2280301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb056d99db8480655d7742fb357ad1bd6de6b78556d46d005628eb93210eecf4`  
		Last Modified: Fri, 08 May 2026 19:24:59 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de908d42b697f6622dffc88cdd09d0a1ddb3127cbabf42fa000970465a9e1f8`  
		Last Modified: Fri, 08 May 2026 19:25:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:34e381cf324225b9dee5ca26f3ecb0ccc5f1f460edfde42459740d7a519e0328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1bcfe0acd4621e7447b151a6a20f2248402d84d7ff8d93c46b90f669ab88e2e`

```dockerfile
```

-	Layers:
	-	`sha256:4ddea0123ac32de5d1b564e296f88cb637634e258c91e4381b8bee9b175654bb`  
		Last Modified: Fri, 08 May 2026 19:25:00 GMT  
		Size: 2.0 MB (2008326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72b234be41aa76eb975368e76c3a352a83f7b9e17ea4311b77d264ba3245480f`  
		Last Modified: Fri, 08 May 2026 19:24:59 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:9bb2e143dc3647a49e4e8f85d5c418bca9b08ce1c1765c5ad7f32f5ab3d8596f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30305327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1b9575bad28b94e1186f365ab00d1a786bf0e90cc8fb820378cf08aa68513b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:25:56 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 20:26:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:29:16 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 20:29:16 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 20:29:16 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 20:29:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 20:29:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:29:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 20:29:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 20:29:16 GMT
USER memcache
# Fri, 08 May 2026 20:29:16 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 20:29:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8f774e9b92b540806fc05167db7ce09a3e1b12abdb9d496f7b8c82138656065a`  
		Last Modified: Fri, 08 May 2026 18:33:49 GMT  
		Size: 27.9 MB (27948200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b5f67bec55f95884a3889baf69e54663718d70194c4ad200c3189a69ed4f77`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0bc2199b80394dc4c86e2ec47bb2bacfa524afadd19cd9436e2cde86accf84b`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 144.2 KB (144163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652d72e4ec6b0cb1a3ca6f0de801f39fbe579385f24fdf2fa903d000df01ef7e`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 2.2 MB (2211447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e003813362a92e41a38ce899360dfc51977add71013d1cac48643e6d9361ec43`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b9b40076d0562644d2bec445a0a7fdefbf4dd5d545c7d8cbdfef18f171b99a`  
		Last Modified: Fri, 08 May 2026 20:29:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:d83c846fc98d19ba355a9a5d1c59147c565e7894fed7c5b582bd5b4bde92d90d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6056bef38756043ff8218f82594c154e80dc8d2097dd770a7bd7bb09a8e6e3e6`

```dockerfile
```

-	Layers:
	-	`sha256:4b4fd92902f7c83c67f43e813275bc5676ec6370639df11fe1394ce7fa7eef2d`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 2.0 MB (2011329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d8b1829f761528fa20afdac852bde73a128edf4c6f11e990f7e7c7fcbcfbf61`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:3d1cfa4c23d23705cf3f8b9302ff26048e2ac216027f45be24e93b8f0817a952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28516943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:582f213c6b868ce82f6e14b78c661812d0781e91331e3ca32ce462777a0529fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:16:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 19:16:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:19:15 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 19:19:15 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 19:19:15 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 19:19:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 19:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:19:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:19:15 GMT
USER memcache
# Fri, 08 May 2026 19:19:15 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 19:19:15 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f1433620eadfdfe016c8054b954f619ae5bca159f35a9459c36a76d9ef4d39c3`  
		Last Modified: Fri, 08 May 2026 18:37:58 GMT  
		Size: 26.2 MB (26214912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851a3dc4d05ac8ea75d436c9d8de99f7ca3c80f159cadffd985253ae10a40069`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18a5b288c05e8d152bf1530b1c4248c0ea5c08902853e0955c6838d5d418b33`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 135.4 KB (135388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff024d65a6401c67cefb240a3ef3d181382530d66cfbb03f13ff32d81500525`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 2.2 MB (2165127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0613bb171f6d5dee88871aafa9a91daf991e3d262feb8682aa8fb5696046579`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c1a297997b8b44cdcad29c590e65efa7934da84dacae1fbddd2b017bb0dd03`  
		Last Modified: Fri, 08 May 2026 19:19:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:e7210267977b9ce03df4bc38f1d1ea5760217f9f582f392ac648876a13580041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120a3ae5c0ce21313dc99a5a24a7d9ae48f434e40717325fda7675fc368c3a9e`

```dockerfile
```

-	Layers:
	-	`sha256:b2f6d69af7f79690357135d68c570ab105358d093cb3ef2b6b37d8c0c4b8766a`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 2.0 MB (2009786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19ecae093d7ef811fe61bf6ed6706bf88a86ab363852e511e19d077fea8bdf22`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:4a47319c5ea763766ec14f7f49c71294e7621973dbf1d934330b273a50d86ae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32560787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea04a0e8415a1e901722a2dc626f036034b99c11dd819b6aab54fe2172610825`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:21:07 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 19:21:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:24:08 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 19:24:08 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 19:24:08 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 19:24:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 19:24:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:24:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:24:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:24:08 GMT
USER memcache
# Fri, 08 May 2026 19:24:08 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 19:24:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73f16d12b26b60a37ae242c9f12503fa0bb655f780014ce964bf39b960ea39a`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f45dfab4b00618ca4983d73b6acabb6fe1e056339b0cafcc1c0268303c02b89`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 153.5 KB (153496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91da4495c7aeb14802d9e2f3854b2226395b2886efcb91a3f91778774632602`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 2.3 MB (2262131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91f17f562e485ed0d6523251b77ca57f1df60d00243de97a13459b077fb30df`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70d0b5c5805a6bd639b55f25e9fb45c11035876f9fca3e2ab607fb2d818b01f`  
		Last Modified: Fri, 08 May 2026 19:24:15 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:003da519f1303287f7dbac93d59fd8f7cd3bd4f7c1c3f59e2ea25f3e1933a4a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b34e9510fcd3b35da3965f941f9c4d3bdf0eff1c30985a7ce5621b638e4c237e`

```dockerfile
```

-	Layers:
	-	`sha256:6041a557446d392656291f000150951d92c8392a387515be5c7e384d175a1967`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 2.0 MB (2008642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e39754d938ea3671f3babce3fbab5d612247a51cbc9f172de306c3fcf60e3a1b`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-trixie` - linux; 386

```console
$ docker pull memcached@sha256:ae0c2a4ef3d5a1336f8204efdb14230b37402d5f8c4096295ddd0f53b7e041ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33670271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d71af2d7fff4e8bb864857f69883ac131a512bb9311bb23de7031cb892e38a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:17:17 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 19:17:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:20:22 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 19:20:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 19:20:22 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 19:20:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 19:20:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:20:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:20:22 GMT
USER memcache
# Fri, 08 May 2026 19:20:22 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 19:20:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:43e2ffbaa23260ffb4e3de716920f2ed9e6af56e465ca1233a2d84c2cc1cf005`  
		Last Modified: Fri, 08 May 2026 18:32:48 GMT  
		Size: 31.3 MB (31296400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2ce2fa16a9ab3457f94c9628fc05a5fd6d54e5d6d3d8a9e1e506ba4e5a37aa`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540be255286e8d861d09681ddd0cd64a25a1b5fa161cca9b859487c03bfb0b6e`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 147.5 KB (147521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913676b9d51d935a10d363087959dec4494fbae5fdf82b80b84e9ecaae370ad3`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 2.2 MB (2224836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224690b120957a082d3ef84ebd501af44b1437fdbf4fcefad6e8faee78e234a5`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d0c777c8b52f9e74da7bf3fd5be45dbd51ab10be8dde37fea12fc96f59cd09`  
		Last Modified: Fri, 08 May 2026 19:20:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:15a21e26469f168e5a065467f48dfed23a1a06d5e0d2b6ffdfcfcc38ff62a560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c3412186834b790b4fbbad4cfe5adfd0f39d11688631b5059120339ee474dc`

```dockerfile
```

-	Layers:
	-	`sha256:ffb482f3d82d9bd4136d15e9b8e08adece9f35076c719e0288e1de86156221e4`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 2.0 MB (2005483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe947a7402c9e03fc064053a531c1cecc9c253a0235c40625608b22c9a860d2f`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:fb4333344bfd32af4cefd042b89dff6ea8ba4bc5ab8168cbe3d29f8c9da5566a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36164277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d865655c5194d1b0446688e3b4f406d0d233869ddf3dcc2b4863b7a8721f32f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:35:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 20:35:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:38:30 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 20:38:30 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 20:38:30 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 20:38:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 20:38:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:38:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 20:38:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 20:38:31 GMT
USER memcache
# Fri, 08 May 2026 20:38:31 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 20:38:31 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2805acf219c32faae551498121eb47f3d7d32bc2a908969bd1ac04c3f49017fe`  
		Last Modified: Fri, 08 May 2026 20:38:41 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278e7e1caa6b74657254421ed3e5193837e9b6f3dde9e041e7e95383e6e68443`  
		Last Modified: Fri, 08 May 2026 20:38:42 GMT  
		Size: 170.4 KB (170351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df05fb319f87f70759df5de69b2f40702ca122c47d614f2f8861ce256eb0b61`  
		Last Modified: Fri, 08 May 2026 20:38:42 GMT  
		Size: 2.4 MB (2394326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f6a1fd9b6e9a261288b936182122f173180b726d490646ee6164ae5c95d84c`  
		Last Modified: Fri, 08 May 2026 20:38:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b93469fb91621a5f46b7dd80327995f9ca6d8361137dbe55159ef455e2976c`  
		Last Modified: Fri, 08 May 2026 20:38:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:e82c5b578718de9c7774bc11902f22157b7c49e1a253ddfe0e3496d4a461d760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89bf5432c3d996440e1d10de68af644b31627fdeeac778ee395c95a88263010a`

```dockerfile
```

-	Layers:
	-	`sha256:8a5017f90fa8e1dd648f24d4c3fa871a8dc77b8e529fe26ee3f0034a79bdd955`  
		Last Modified: Fri, 08 May 2026 20:38:42 GMT  
		Size: 2.0 MB (2011927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e26de34ce99baa5e3d603d8a2dddfc874c4b7cf85ae36baf53e81232916879a8`  
		Last Modified: Fri, 08 May 2026 20:38:41 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:5ddab235954c3cde3c815b6a5be674885381502972ebc53794c4811df335843c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30623277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b6d17550b0133cd405553af720539d51b95b0d50475bbcdbf6c2173bd5280b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 16:09:52 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 09 May 2026 16:10:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 16:23:27 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 09 May 2026 16:23:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 09 May 2026 16:23:27 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 09 May 2026 16:23:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 09 May 2026 16:23:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 09 May 2026 16:23:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 09 May 2026 16:23:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 09 May 2026 16:23:28 GMT
USER memcache
# Sat, 09 May 2026 16:23:28 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 09 May 2026 16:23:28 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1e9edef871271ebe58c5a713c7c062e88ff414be0976a2c7baf0aba83823c954`  
		Last Modified: Fri, 08 May 2026 20:38:39 GMT  
		Size: 28.3 MB (28280232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9888105b7154ad185e8f5227e002ba1af0f905cba713450e54261fb929e80afe`  
		Last Modified: Sat, 09 May 2026 16:24:13 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea9dc216a8ac7e5ff5123e9cec2e0c1650d9afc96015312e8f304adc6c255a0`  
		Last Modified: Sat, 09 May 2026 16:24:13 GMT  
		Size: 133.1 KB (133086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e544f8419fe19b80d411a515c9201c8c35d068e9a3ff1127e23e53c495a036c9`  
		Last Modified: Sat, 09 May 2026 16:24:13 GMT  
		Size: 2.2 MB (2208450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b939f3eba847b32e2c08af32b5870190d0195179c8dfcfba89b9abd0d24865b8`  
		Last Modified: Sat, 09 May 2026 16:24:13 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0a4092dbf93f8a2db331d4bb00d34313567e7245e5753310064f99299a2919`  
		Last Modified: Sat, 09 May 2026 16:24:14 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:84361ecaeb53a4b02619fac3c96e92f016548a953b0bb4909dbce2605c50c27e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e712edaa1f4a23a51ec2552dadfb1ba38310fc63ac1066e30c4ccd5f2d388ce8`

```dockerfile
```

-	Layers:
	-	`sha256:b27196635d6011055da056ccc202d4d6df3c0d9296b913ab5b40505f5efb56b9`  
		Last Modified: Sat, 09 May 2026 16:24:13 GMT  
		Size: 2.0 MB (2002290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f31718fda9bdd1f0330201f0a2069f169fd2f79967b828cb3138dad392f06e0d`  
		Last Modified: Sat, 09 May 2026 16:24:12 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:7f194d0409eee2a5b0bb8903485384802c30d3e8f3db4edc714dccedd365197b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32280599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71da9b051066a3ea5be228e76446413fcc99d1b892a8e007445d21d95254a5d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:18:08 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 19:18:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:21:32 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 19:21:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 19:21:32 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 19:21:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 19:21:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:21:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:21:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:21:32 GMT
USER memcache
# Fri, 08 May 2026 19:21:32 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 19:21:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875e7d47d55cac3b3811a3503e8330c2b49b3264583a0e3ffbc8380fe58dd8d3`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e487f7a355c714fc8533d060a278791698afaed2353417768b8f02bd7844e06`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 140.5 KB (140519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6bb469173a6734f9ba49a4aa2f9a1d3e6513740633df30a2d3bc37c3b9d4279`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 2.3 MB (2298219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7e59c6d93f04c1f009cbda35d2e5b25d8087cadff3126c5de7636d0c10b5c0`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa99c508f7dc7874b69603543390bb5c9a5b3bb0689bde04f6d7d53db1ce25bd`  
		Last Modified: Fri, 08 May 2026 19:21:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:b257f9c0883422f85a5c40a24940bb3401de8aac9c08bc12a87f5732d143082c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff10b6e9f782a5c6eee93b5e143ea12b75800a8ef331ebc5d73519e32464d829`

```dockerfile
```

-	Layers:
	-	`sha256:3f4b79e225835bdf97992cd4741626b92fb8ad5438feb251afbf7d6bb442a01d`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 2.0 MB (2009763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff63eebb23b55a364393e4d41fbc25ca8e9a760278a9403379c7fb549f8a1248`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine`

```console
$ docker pull memcached@sha256:65c80b311a9601ef5ca8af3814e5cd06a9c4277ea139d80bd53da6b4d39eb46e
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
$ docker pull memcached@sha256:7b962825022657b112923d502400d5734870d5eb12c19e7f1f6585f7534a6795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5959872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b58f7e71f30daaa3f466fa31d855fddb7101e42c0c42fac520be5d1d43ec32e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:46 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:47 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:20:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:20:22 GMT
USER memcache
# Wed, 15 Apr 2026 20:20:22 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:20:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73d5ffe265b83073ce3c7211fb3c15ebbd5e7146d870d9ce69d2e7dfc493348`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cb4fdd95ced0d5a9528e97ff0f20742749cbd9ef6dc1322d13e682a7085a67`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 106.1 KB (106063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe17fc291d9444fbae93d7f45eab008318f87302c016c06e6e911c1a571a053`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 2.0 MB (1988274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1948bd131d2cbd05c6bf2962d18b15d105abee6f42f398bab3c13737537f197`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bde8ceae30a2a0890715bbc591167ee301c57d7f75023e80be460035187def`  
		Last Modified: Wed, 15 Apr 2026 20:20:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:58ed333482f8a8530c82ad7399d5917a7db85fbcdf70fc1dec55fbedcdf09253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4255278359004afd8c94db1a7fe6129fc984d0716c33665c9eca3168476fdcb`

```dockerfile
```

-	Layers:
	-	`sha256:5f47d88d89d22d065a3590d477ae130520b882176ab07e95862afb4d8b69b214`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 94.9 KB (94901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab2d532e4a6ce2f362d25c79dfaeb88d333fe6efe7c1b5b293630bf6ca292eb8`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 20.5 KB (20530 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:47a06cd0daead339b96ed90e425336a8a49a75e4e358b5ec1ea63a630720f704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3947facc9e9fae3eee283f24b611a8ae87e353b6d6447bc6f582e90f2fce3743`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:58 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:21:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:21:03 GMT
USER memcache
# Wed, 15 Apr 2026 20:21:03 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:21:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77001163fdaab47f07a85fc5bb15f3512a8cb9b9b049cec7e0c88bcbbdb5bb5d`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee1b43c0cfbf2ee56e39441933ff06803264d22918fe867d8b5ba7d5adfb9c3`  
		Last Modified: Wed, 15 Apr 2026 20:21:06 GMT  
		Size: 102.6 KB (102630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c041bfac12e599ad87749289dec9672dac36e8c0e16779f13fa695d10f2f0cc5`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 1.9 MB (1937835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2dfd492dd0f295311a0c314fae06f4b325ae22cb0e673a53e0705f3d4e0504`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671c66eac839c2f0a5b2e64d1f581069c4cdf119e784bff16540ecc94e2c2b10`  
		Last Modified: Wed, 15 Apr 2026 20:21:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2a6148a6aebb042e55781b40ed626d0c5871833be4ae8dc303af7aace07d9d60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbaadfaacfaf0e7c226b35236bb84c2268d4c6eb017efd435a3999a44edfcc77`

```dockerfile
```

-	Layers:
	-	`sha256:c68bb3ee35fc0ac716bca45cc759f3b1ff52b1d5a0acae9876eaf0aa55aa667d`  
		Last Modified: Wed, 15 Apr 2026 20:21:06 GMT  
		Size: 20.5 KB (20466 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:fb58bae12ffa00c9cbafc8bee2341b43ffdccacbde7085fa707ef6c7f2d69e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd4e85c30e4df5803b553b8a7f84084c3dae6f72531ac70fcabf7099cfa8148`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:14:38 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 21:14:39 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 21:17:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:17:34 GMT
USER memcache
# Wed, 15 Apr 2026 21:17:34 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 21:17:34 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e312136cfedda9620407d42650d0595220e60d3c40ae8853bfbdd83f392b9e6`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53697a39f37b691917c91310ac4e107308674bddcc9017e3bbc0d0134eaf4c3e`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 92.4 KB (92369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5e4be9e0df543f152c376fe2cc74b89b75585793fdbd7d12476737d386d8e1`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 1.9 MB (1896191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a083f41edf5f859feb4367eeeea0955dc9799c8202fb8a67c40915ed5b195002`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c43503b1f4f42ffc5e0e4415befe45199dec730bc26347df151298345ba640`  
		Last Modified: Wed, 15 Apr 2026 21:17:40 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7535cf6b6a140771131c2c524301d4616f34856fcd8ecbe3e52300108c49de2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d73c906894a0a3d178edd69991f310225c0daef314e6faa83a0b9adecfbeb34`

```dockerfile
```

-	Layers:
	-	`sha256:8f1fddd7d14560fb90f381b09cde9302dfc9253e6702adf28c55961d755b1ad8`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 94.3 KB (94319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fcf119d246607aa25330c4c05fe14a64cebda69b02d14507862a9f07c1404e6`  
		Last Modified: Wed, 15 Apr 2026 21:17:38 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:6d70439467a65065c52894232a3085c724da2810a9b3205130d5e434ab411e3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6288798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4be3e105216d2507b68e772f7d08d52a5076dd55fad35c29775038d05c24112`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:15:23 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:15:24 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:18:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:18:13 GMT
USER memcache
# Wed, 15 Apr 2026 20:18:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:18:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81758f5fc2e8fa13e3625f253d7c999560ac666121c026f7251dbfb919cca611`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d735737d3a0cf1eda63bd72c09f64eb679313e9c5f8a105849848bdd779e1d`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 121.8 KB (121846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ac0921d2cc2b3388e0f006a6672c5a9e1098a59e570121dde092104d845c51`  
		Last Modified: Wed, 15 Apr 2026 20:18:19 GMT  
		Size: 2.0 MB (1965733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca9cf731b18a76c3ac25cc3add219660d57516c12680d7b1f1ece282406eb82`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717a6b23dd1cd76b686bf26066af23265e0d002ed6a3e87f6aa4f79264b7da11`  
		Last Modified: Wed, 15 Apr 2026 20:18:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7e5232b868d3222e3ce2b0ee39c62f6cb294bea27456b00940fbc4e3c8c3f84d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:780bf975a24d5fdc511c857720c04cb077d64abcfe4c93ea0db7c9487c323718`

```dockerfile
```

-	Layers:
	-	`sha256:addb0f46e3b5adb674175c11fc85526d4628e24d74d210c8b00c9a945b44407c`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 94.4 KB (94355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3364e418b74b6f6ca17deec7d55783a6e1554de3783ab0a6d5e56496d935ddb0`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:80328bf779fa1494f7677b441ad1c16c2134f126e6556953deb3cfab1c4c9770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5744816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d957405dd0811f1cd15fe39563938a60c2008204d2f63ebc7e39f8989c796f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:20:45 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 22:20:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 22:23:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 22:23:32 GMT
USER memcache
# Wed, 15 Apr 2026 22:23:32 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 22:23:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0617a09eee85c2032f5596ded56b733366513074f9096177315b50dc45485e20`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c67275dbc381ac3ae0b21dda20edaf245e2ca54d6f5dc3af8805db03c17cc93`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 110.7 KB (110715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6ecb23f1f4bc89d5c315aac493f29fe7bb33061c70d926c904f4f55d374461`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 1.9 MB (1942309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e782df8f482a58603ea70ef9e04e838d044a6070c7e4cd116c90a09b917ed940`  
		Last Modified: Wed, 15 Apr 2026 22:23:38 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616df56d574e39c00ae772c6a29e2b724698048a83cc29ea17049573f9073b10`  
		Last Modified: Wed, 15 Apr 2026 22:23:38 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c726e7abf461d963e544818339e4cd12fd2f31e41436475f0e51818a0885fbdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12e41b9d6f745d686c2649255bd14fe4e0b97a3477d383e719490e5ef66b27ae`

```dockerfile
```

-	Layers:
	-	`sha256:b44003cd1ea209090a063c5abfb4ee881849abba47e8711191b7637f86d8ee8b`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 94.9 KB (94856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f431de53d9b6c7e2cbc847af9daec064d061f8bd625615734012051336c495a`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 20.5 KB (20472 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:8182e35a9a404f0b522cb3c176d3dc4aade974e5556184c0a5a19e800721868a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6034321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c6f532e81b50ea71c3520a80da0c8154b4cb14ebc17f87eb3a026862b47ed8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:43 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:20:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:20:22 GMT
USER memcache
# Wed, 15 Apr 2026 20:20:22 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:20:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee88d1c88fa46aa906a297c2919c9a085e74d04f20e4f827ca240a20f10ad34`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c574329cc1ebf156e2d89ab608bd58a3c0db550845c0ec394d265aa98fc5c4`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 126.3 KB (126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2a28510bcba91734e7b38682847296011b63458db8a87a4bcecd180b8de7b5`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 2.1 MB (2075767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c524eb15ef0a41bf969efc93ef579db92dc59e8df57c9abfd099e7f6ff0756`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bde8ceae30a2a0890715bbc591167ee301c57d7f75023e80be460035187def`  
		Last Modified: Wed, 15 Apr 2026 20:20:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:4051408ef6c5bf4d4f37abf19c13f0298d8baa81770fcbfb588221e49e3bb834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec3a4d49e6f325e484db43c9c9981f4eaa0223d9ae98282d95c3ee20c2089cb`

```dockerfile
```

-	Layers:
	-	`sha256:0e4e65db585f857844a67a831eb876dbb0a8a40d9269393d6c0fa83a2df995ae`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 94.3 KB (94308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50f58ec8aff3c96cc7b58e689122c27ee26121c598034cdc59ec95fd6423effe`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:f3209d1ca2c4ce827614d16445231d96372944d218f18fd22850eec83874e5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5772332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e30170e0826b89d0ca59ffcae54b850ded07e6ae9451ecf1fd60f3ca8adcc725`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 00:00:48 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 16 Apr 2026 00:00:52 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Thu, 16 Apr 2026 00:14:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 16 Apr 2026 00:14:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Apr 2026 00:14:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 16 Apr 2026 00:14:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Apr 2026 00:14:22 GMT
USER memcache
# Thu, 16 Apr 2026 00:14:22 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 16 Apr 2026 00:14:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62b143e34f5b89277e3a88ed4d722339d188a094d4bb534e222ca80e7741031`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfff7c64f831ba03c491874cdf9a1c3f42bff72bb0e1951c63d8cf718854cff`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 108.9 KB (108903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69aef1050272a61cfbfd97c041d3776f96bdd03b102f2c3c54bbb0af2e1235a5`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 2.1 MB (2074414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ce340fb37f86db0d3aa774c23880b7c8322d2af8e3adc27a6ffa25d67c2122`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e40c6fb92d819994d38fae7accdffd583465eb6e645834b66f3ce9f0562f69`  
		Last Modified: Thu, 16 Apr 2026 00:14:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2caae198d1efb7d4df14da45a3ff360a697982b544a61a3f907076b414983ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1503bd38f4b30bc91be18dd93359e7376a9da1c7cb652ade64efd154064543fe`

```dockerfile
```

-	Layers:
	-	`sha256:e2d79fb634d76e28f055ab09953f59c371b93599e2b79f20f3d758f2c9520118`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 94.3 KB (94304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3614ad9b1715c3d6aa488496fca74d7143ea095d227f599407c933c62ec266aa`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 20.6 KB (20604 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; s390x

```console
$ docker pull memcached@sha256:1da27660ae89a83aaf603e1affd51be573e5b8dac6c07ed592aee2a3a2b20581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5859702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13aa64df69a308e46b054bbd8e7a5d2f1e079005771f61748dae0d049889ba7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:14:40 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:14:41 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:17:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:17:58 GMT
USER memcache
# Wed, 15 Apr 2026 20:17:58 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:17:58 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c42733e5f451590186b9b76c4b374ae5a84b657f7f1fd405647f5ba82c65bcd`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a14431ac88e8fe205b07f09b7e4843bb254de41cbc044725d6eaee3c2f822f`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 114.3 KB (114293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6377b7d98f32173cd47682aa73b32e4eba42781fa9224b9eb7a6f87367d37f94`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 2.0 MB (2017525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d022ae992296922747a4b69694b0185a0ce1f6cdece7f794e39e74dab92d250`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255cb3a435cbd623c1235d0429160faf72c244a6c1a613525df36f58a8c1f784`  
		Last Modified: Wed, 15 Apr 2026 20:18:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:531ee140f06db77d73b71bce7339abec3c6d976092bb80542bb337bb406acdbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b17d6f7e71efe3ee05ebcdb8ae90c28cf60db9ef069b0a98fe442c949740a6c`

```dockerfile
```

-	Layers:
	-	`sha256:820a080f49bf9e33948dbe5c13f6254f135d90bcb2b2277e3d2fd2430626c1a2`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 94.2 KB (94250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8ab82f4f240f46f9e34b74691925ab4af7f1cbb12ad3cb8639e0f317cf06653`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine3.23`

```console
$ docker pull memcached@sha256:65c80b311a9601ef5ca8af3814e5cd06a9c4277ea139d80bd53da6b4d39eb46e
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
$ docker pull memcached@sha256:7b962825022657b112923d502400d5734870d5eb12c19e7f1f6585f7534a6795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5959872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b58f7e71f30daaa3f466fa31d855fddb7101e42c0c42fac520be5d1d43ec32e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:46 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:47 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:20:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:20:22 GMT
USER memcache
# Wed, 15 Apr 2026 20:20:22 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:20:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73d5ffe265b83073ce3c7211fb3c15ebbd5e7146d870d9ce69d2e7dfc493348`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cb4fdd95ced0d5a9528e97ff0f20742749cbd9ef6dc1322d13e682a7085a67`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 106.1 KB (106063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe17fc291d9444fbae93d7f45eab008318f87302c016c06e6e911c1a571a053`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 2.0 MB (1988274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1948bd131d2cbd05c6bf2962d18b15d105abee6f42f398bab3c13737537f197`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bde8ceae30a2a0890715bbc591167ee301c57d7f75023e80be460035187def`  
		Last Modified: Wed, 15 Apr 2026 20:20:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:58ed333482f8a8530c82ad7399d5917a7db85fbcdf70fc1dec55fbedcdf09253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4255278359004afd8c94db1a7fe6129fc984d0716c33665c9eca3168476fdcb`

```dockerfile
```

-	Layers:
	-	`sha256:5f47d88d89d22d065a3590d477ae130520b882176ab07e95862afb4d8b69b214`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 94.9 KB (94901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab2d532e4a6ce2f362d25c79dfaeb88d333fe6efe7c1b5b293630bf6ca292eb8`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 20.5 KB (20530 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; arm variant v6

```console
$ docker pull memcached@sha256:47a06cd0daead339b96ed90e425336a8a49a75e4e358b5ec1ea63a630720f704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3947facc9e9fae3eee283f24b611a8ae87e353b6d6447bc6f582e90f2fce3743`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:58 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:21:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:21:03 GMT
USER memcache
# Wed, 15 Apr 2026 20:21:03 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:21:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77001163fdaab47f07a85fc5bb15f3512a8cb9b9b049cec7e0c88bcbbdb5bb5d`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee1b43c0cfbf2ee56e39441933ff06803264d22918fe867d8b5ba7d5adfb9c3`  
		Last Modified: Wed, 15 Apr 2026 20:21:06 GMT  
		Size: 102.6 KB (102630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c041bfac12e599ad87749289dec9672dac36e8c0e16779f13fa695d10f2f0cc5`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 1.9 MB (1937835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2dfd492dd0f295311a0c314fae06f4b325ae22cb0e673a53e0705f3d4e0504`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671c66eac839c2f0a5b2e64d1f581069c4cdf119e784bff16540ecc94e2c2b10`  
		Last Modified: Wed, 15 Apr 2026 20:21:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:2a6148a6aebb042e55781b40ed626d0c5871833be4ae8dc303af7aace07d9d60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbaadfaacfaf0e7c226b35236bb84c2268d4c6eb017efd435a3999a44edfcc77`

```dockerfile
```

-	Layers:
	-	`sha256:c68bb3ee35fc0ac716bca45cc759f3b1ff52b1d5a0acae9876eaf0aa55aa667d`  
		Last Modified: Wed, 15 Apr 2026 20:21:06 GMT  
		Size: 20.5 KB (20466 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; arm variant v7

```console
$ docker pull memcached@sha256:fb58bae12ffa00c9cbafc8bee2341b43ffdccacbde7085fa707ef6c7f2d69e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd4e85c30e4df5803b553b8a7f84084c3dae6f72531ac70fcabf7099cfa8148`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:14:38 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 21:14:39 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 21:17:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:17:34 GMT
USER memcache
# Wed, 15 Apr 2026 21:17:34 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 21:17:34 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e312136cfedda9620407d42650d0595220e60d3c40ae8853bfbdd83f392b9e6`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53697a39f37b691917c91310ac4e107308674bddcc9017e3bbc0d0134eaf4c3e`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 92.4 KB (92369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5e4be9e0df543f152c376fe2cc74b89b75585793fdbd7d12476737d386d8e1`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 1.9 MB (1896191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a083f41edf5f859feb4367eeeea0955dc9799c8202fb8a67c40915ed5b195002`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c43503b1f4f42ffc5e0e4415befe45199dec730bc26347df151298345ba640`  
		Last Modified: Wed, 15 Apr 2026 21:17:40 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:7535cf6b6a140771131c2c524301d4616f34856fcd8ecbe3e52300108c49de2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d73c906894a0a3d178edd69991f310225c0daef314e6faa83a0b9adecfbeb34`

```dockerfile
```

-	Layers:
	-	`sha256:8f1fddd7d14560fb90f381b09cde9302dfc9253e6702adf28c55961d755b1ad8`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 94.3 KB (94319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fcf119d246607aa25330c4c05fe14a64cebda69b02d14507862a9f07c1404e6`  
		Last Modified: Wed, 15 Apr 2026 21:17:38 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:6d70439467a65065c52894232a3085c724da2810a9b3205130d5e434ab411e3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6288798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4be3e105216d2507b68e772f7d08d52a5076dd55fad35c29775038d05c24112`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:15:23 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:15:24 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:18:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:18:13 GMT
USER memcache
# Wed, 15 Apr 2026 20:18:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:18:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81758f5fc2e8fa13e3625f253d7c999560ac666121c026f7251dbfb919cca611`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d735737d3a0cf1eda63bd72c09f64eb679313e9c5f8a105849848bdd779e1d`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 121.8 KB (121846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ac0921d2cc2b3388e0f006a6672c5a9e1098a59e570121dde092104d845c51`  
		Last Modified: Wed, 15 Apr 2026 20:18:19 GMT  
		Size: 2.0 MB (1965733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca9cf731b18a76c3ac25cc3add219660d57516c12680d7b1f1ece282406eb82`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717a6b23dd1cd76b686bf26066af23265e0d002ed6a3e87f6aa4f79264b7da11`  
		Last Modified: Wed, 15 Apr 2026 20:18:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:7e5232b868d3222e3ce2b0ee39c62f6cb294bea27456b00940fbc4e3c8c3f84d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:780bf975a24d5fdc511c857720c04cb077d64abcfe4c93ea0db7c9487c323718`

```dockerfile
```

-	Layers:
	-	`sha256:addb0f46e3b5adb674175c11fc85526d4628e24d74d210c8b00c9a945b44407c`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 94.4 KB (94355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3364e418b74b6f6ca17deec7d55783a6e1554de3783ab0a6d5e56496d935ddb0`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; 386

```console
$ docker pull memcached@sha256:80328bf779fa1494f7677b441ad1c16c2134f126e6556953deb3cfab1c4c9770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5744816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d957405dd0811f1cd15fe39563938a60c2008204d2f63ebc7e39f8989c796f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:20:45 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 22:20:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 22:23:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 22:23:32 GMT
USER memcache
# Wed, 15 Apr 2026 22:23:32 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 22:23:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0617a09eee85c2032f5596ded56b733366513074f9096177315b50dc45485e20`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c67275dbc381ac3ae0b21dda20edaf245e2ca54d6f5dc3af8805db03c17cc93`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 110.7 KB (110715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6ecb23f1f4bc89d5c315aac493f29fe7bb33061c70d926c904f4f55d374461`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 1.9 MB (1942309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e782df8f482a58603ea70ef9e04e838d044a6070c7e4cd116c90a09b917ed940`  
		Last Modified: Wed, 15 Apr 2026 22:23:38 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616df56d574e39c00ae772c6a29e2b724698048a83cc29ea17049573f9073b10`  
		Last Modified: Wed, 15 Apr 2026 22:23:38 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:c726e7abf461d963e544818339e4cd12fd2f31e41436475f0e51818a0885fbdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12e41b9d6f745d686c2649255bd14fe4e0b97a3477d383e719490e5ef66b27ae`

```dockerfile
```

-	Layers:
	-	`sha256:b44003cd1ea209090a063c5abfb4ee881849abba47e8711191b7637f86d8ee8b`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 94.9 KB (94856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f431de53d9b6c7e2cbc847af9daec064d061f8bd625615734012051336c495a`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 20.5 KB (20472 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; ppc64le

```console
$ docker pull memcached@sha256:8182e35a9a404f0b522cb3c176d3dc4aade974e5556184c0a5a19e800721868a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6034321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c6f532e81b50ea71c3520a80da0c8154b4cb14ebc17f87eb3a026862b47ed8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:43 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:20:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:20:22 GMT
USER memcache
# Wed, 15 Apr 2026 20:20:22 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:20:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee88d1c88fa46aa906a297c2919c9a085e74d04f20e4f827ca240a20f10ad34`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c574329cc1ebf156e2d89ab608bd58a3c0db550845c0ec394d265aa98fc5c4`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 126.3 KB (126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2a28510bcba91734e7b38682847296011b63458db8a87a4bcecd180b8de7b5`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 2.1 MB (2075767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c524eb15ef0a41bf969efc93ef579db92dc59e8df57c9abfd099e7f6ff0756`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bde8ceae30a2a0890715bbc591167ee301c57d7f75023e80be460035187def`  
		Last Modified: Wed, 15 Apr 2026 20:20:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:4051408ef6c5bf4d4f37abf19c13f0298d8baa81770fcbfb588221e49e3bb834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec3a4d49e6f325e484db43c9c9981f4eaa0223d9ae98282d95c3ee20c2089cb`

```dockerfile
```

-	Layers:
	-	`sha256:0e4e65db585f857844a67a831eb876dbb0a8a40d9269393d6c0fa83a2df995ae`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 94.3 KB (94308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50f58ec8aff3c96cc7b58e689122c27ee26121c598034cdc59ec95fd6423effe`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; riscv64

```console
$ docker pull memcached@sha256:f3209d1ca2c4ce827614d16445231d96372944d218f18fd22850eec83874e5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5772332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e30170e0826b89d0ca59ffcae54b850ded07e6ae9451ecf1fd60f3ca8adcc725`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 00:00:48 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 16 Apr 2026 00:00:52 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Thu, 16 Apr 2026 00:14:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 16 Apr 2026 00:14:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Apr 2026 00:14:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 16 Apr 2026 00:14:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Apr 2026 00:14:22 GMT
USER memcache
# Thu, 16 Apr 2026 00:14:22 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 16 Apr 2026 00:14:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62b143e34f5b89277e3a88ed4d722339d188a094d4bb534e222ca80e7741031`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfff7c64f831ba03c491874cdf9a1c3f42bff72bb0e1951c63d8cf718854cff`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 108.9 KB (108903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69aef1050272a61cfbfd97c041d3776f96bdd03b102f2c3c54bbb0af2e1235a5`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 2.1 MB (2074414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ce340fb37f86db0d3aa774c23880b7c8322d2af8e3adc27a6ffa25d67c2122`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e40c6fb92d819994d38fae7accdffd583465eb6e645834b66f3ce9f0562f69`  
		Last Modified: Thu, 16 Apr 2026 00:14:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:2caae198d1efb7d4df14da45a3ff360a697982b544a61a3f907076b414983ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1503bd38f4b30bc91be18dd93359e7376a9da1c7cb652ade64efd154064543fe`

```dockerfile
```

-	Layers:
	-	`sha256:e2d79fb634d76e28f055ab09953f59c371b93599e2b79f20f3d758f2c9520118`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 94.3 KB (94304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3614ad9b1715c3d6aa488496fca74d7143ea095d227f599407c933c62ec266aa`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 20.6 KB (20604 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; s390x

```console
$ docker pull memcached@sha256:1da27660ae89a83aaf603e1affd51be573e5b8dac6c07ed592aee2a3a2b20581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5859702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13aa64df69a308e46b054bbd8e7a5d2f1e079005771f61748dae0d049889ba7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:14:40 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:14:41 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:17:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:17:58 GMT
USER memcache
# Wed, 15 Apr 2026 20:17:58 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:17:58 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c42733e5f451590186b9b76c4b374ae5a84b657f7f1fd405647f5ba82c65bcd`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a14431ac88e8fe205b07f09b7e4843bb254de41cbc044725d6eaee3c2f822f`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 114.3 KB (114293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6377b7d98f32173cd47682aa73b32e4eba42781fa9224b9eb7a6f87367d37f94`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 2.0 MB (2017525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d022ae992296922747a4b69694b0185a0ce1f6cdece7f794e39e74dab92d250`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255cb3a435cbd623c1235d0429160faf72c244a6c1a613525df36f58a8c1f784`  
		Last Modified: Wed, 15 Apr 2026 20:18:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:531ee140f06db77d73b71bce7339abec3c6d976092bb80542bb337bb406acdbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b17d6f7e71efe3ee05ebcdb8ae90c28cf60db9ef069b0a98fe442c949740a6c`

```dockerfile
```

-	Layers:
	-	`sha256:820a080f49bf9e33948dbe5c13f6254f135d90bcb2b2277e3d2fd2430626c1a2`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 94.2 KB (94250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8ab82f4f240f46f9e34b74691925ab4af7f1cbb12ad3cb8639e0f317cf06653`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:latest`

```console
$ docker pull memcached@sha256:f7a252e7ba3fbbe9672c483354c5081d02b780122c3bb97bd311d5662b54d0ad
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
$ docker pull memcached@sha256:5f9197399e5aefcabef61b7c94d4e9578698e4a0ac391f6a4b34eb0dcd493df2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32198719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5474f3cc4ab6f46b8613ec8b77a7c6ec75f3b8944c8674fa5c02be437ee6567b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:22:04 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 19:22:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:24:53 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 19:24:53 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 19:24:53 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 19:24:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 19:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:24:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:24:54 GMT
USER memcache
# Fri, 08 May 2026 19:24:54 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 19:24:54 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95946911721deafff321fd508db9ba36e3babc47097ecd6c6bdf2ba0dd470257`  
		Last Modified: Fri, 08 May 2026 19:24:59 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2951237283f3070819f0121ee72d97873d9e5287f4ff5cd5b450147eb57c72`  
		Last Modified: Fri, 08 May 2026 19:24:59 GMT  
		Size: 136.7 KB (136676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f29d81d44c4b3a8bb7866171f79f5054acda551367bbcf5ae523080623b437d`  
		Last Modified: Fri, 08 May 2026 19:25:00 GMT  
		Size: 2.3 MB (2280301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb056d99db8480655d7742fb357ad1bd6de6b78556d46d005628eb93210eecf4`  
		Last Modified: Fri, 08 May 2026 19:24:59 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de908d42b697f6622dffc88cdd09d0a1ddb3127cbabf42fa000970465a9e1f8`  
		Last Modified: Fri, 08 May 2026 19:25:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:34e381cf324225b9dee5ca26f3ecb0ccc5f1f460edfde42459740d7a519e0328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1bcfe0acd4621e7447b151a6a20f2248402d84d7ff8d93c46b90f669ab88e2e`

```dockerfile
```

-	Layers:
	-	`sha256:4ddea0123ac32de5d1b564e296f88cb637634e258c91e4381b8bee9b175654bb`  
		Last Modified: Fri, 08 May 2026 19:25:00 GMT  
		Size: 2.0 MB (2008326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72b234be41aa76eb975368e76c3a352a83f7b9e17ea4311b77d264ba3245480f`  
		Last Modified: Fri, 08 May 2026 19:24:59 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:9bb2e143dc3647a49e4e8f85d5c418bca9b08ce1c1765c5ad7f32f5ab3d8596f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30305327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1b9575bad28b94e1186f365ab00d1a786bf0e90cc8fb820378cf08aa68513b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:25:56 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 20:26:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:29:16 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 20:29:16 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 20:29:16 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 20:29:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 20:29:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:29:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 20:29:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 20:29:16 GMT
USER memcache
# Fri, 08 May 2026 20:29:16 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 20:29:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8f774e9b92b540806fc05167db7ce09a3e1b12abdb9d496f7b8c82138656065a`  
		Last Modified: Fri, 08 May 2026 18:33:49 GMT  
		Size: 27.9 MB (27948200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b5f67bec55f95884a3889baf69e54663718d70194c4ad200c3189a69ed4f77`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0bc2199b80394dc4c86e2ec47bb2bacfa524afadd19cd9436e2cde86accf84b`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 144.2 KB (144163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652d72e4ec6b0cb1a3ca6f0de801f39fbe579385f24fdf2fa903d000df01ef7e`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 2.2 MB (2211447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e003813362a92e41a38ce899360dfc51977add71013d1cac48643e6d9361ec43`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b9b40076d0562644d2bec445a0a7fdefbf4dd5d545c7d8cbdfef18f171b99a`  
		Last Modified: Fri, 08 May 2026 20:29:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:d83c846fc98d19ba355a9a5d1c59147c565e7894fed7c5b582bd5b4bde92d90d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6056bef38756043ff8218f82594c154e80dc8d2097dd770a7bd7bb09a8e6e3e6`

```dockerfile
```

-	Layers:
	-	`sha256:4b4fd92902f7c83c67f43e813275bc5676ec6370639df11fe1394ce7fa7eef2d`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 2.0 MB (2011329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d8b1829f761528fa20afdac852bde73a128edf4c6f11e990f7e7c7fcbcfbf61`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v7

```console
$ docker pull memcached@sha256:3d1cfa4c23d23705cf3f8b9302ff26048e2ac216027f45be24e93b8f0817a952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28516943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:582f213c6b868ce82f6e14b78c661812d0781e91331e3ca32ce462777a0529fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:16:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 19:16:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:19:15 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 19:19:15 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 19:19:15 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 19:19:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 19:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:19:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:19:15 GMT
USER memcache
# Fri, 08 May 2026 19:19:15 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 19:19:15 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f1433620eadfdfe016c8054b954f619ae5bca159f35a9459c36a76d9ef4d39c3`  
		Last Modified: Fri, 08 May 2026 18:37:58 GMT  
		Size: 26.2 MB (26214912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851a3dc4d05ac8ea75d436c9d8de99f7ca3c80f159cadffd985253ae10a40069`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18a5b288c05e8d152bf1530b1c4248c0ea5c08902853e0955c6838d5d418b33`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 135.4 KB (135388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff024d65a6401c67cefb240a3ef3d181382530d66cfbb03f13ff32d81500525`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 2.2 MB (2165127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0613bb171f6d5dee88871aafa9a91daf991e3d262feb8682aa8fb5696046579`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c1a297997b8b44cdcad29c590e65efa7934da84dacae1fbddd2b017bb0dd03`  
		Last Modified: Fri, 08 May 2026 19:19:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:e7210267977b9ce03df4bc38f1d1ea5760217f9f582f392ac648876a13580041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120a3ae5c0ce21313dc99a5a24a7d9ae48f434e40717325fda7675fc368c3a9e`

```dockerfile
```

-	Layers:
	-	`sha256:b2f6d69af7f79690357135d68c570ab105358d093cb3ef2b6b37d8c0c4b8766a`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 2.0 MB (2009786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19ecae093d7ef811fe61bf6ed6706bf88a86ab363852e511e19d077fea8bdf22`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:4a47319c5ea763766ec14f7f49c71294e7621973dbf1d934330b273a50d86ae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32560787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea04a0e8415a1e901722a2dc626f036034b99c11dd819b6aab54fe2172610825`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:21:07 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 19:21:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:24:08 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 19:24:08 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 19:24:08 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 19:24:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 19:24:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:24:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:24:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:24:08 GMT
USER memcache
# Fri, 08 May 2026 19:24:08 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 19:24:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73f16d12b26b60a37ae242c9f12503fa0bb655f780014ce964bf39b960ea39a`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f45dfab4b00618ca4983d73b6acabb6fe1e056339b0cafcc1c0268303c02b89`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 153.5 KB (153496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91da4495c7aeb14802d9e2f3854b2226395b2886efcb91a3f91778774632602`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 2.3 MB (2262131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91f17f562e485ed0d6523251b77ca57f1df60d00243de97a13459b077fb30df`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70d0b5c5805a6bd639b55f25e9fb45c11035876f9fca3e2ab607fb2d818b01f`  
		Last Modified: Fri, 08 May 2026 19:24:15 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:003da519f1303287f7dbac93d59fd8f7cd3bd4f7c1c3f59e2ea25f3e1933a4a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b34e9510fcd3b35da3965f941f9c4d3bdf0eff1c30985a7ce5621b638e4c237e`

```dockerfile
```

-	Layers:
	-	`sha256:6041a557446d392656291f000150951d92c8392a387515be5c7e384d175a1967`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 2.0 MB (2008642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e39754d938ea3671f3babce3fbab5d612247a51cbc9f172de306c3fcf60e3a1b`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:ae0c2a4ef3d5a1336f8204efdb14230b37402d5f8c4096295ddd0f53b7e041ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33670271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d71af2d7fff4e8bb864857f69883ac131a512bb9311bb23de7031cb892e38a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:17:17 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 19:17:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:20:22 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 19:20:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 19:20:22 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 19:20:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 19:20:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:20:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:20:22 GMT
USER memcache
# Fri, 08 May 2026 19:20:22 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 19:20:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:43e2ffbaa23260ffb4e3de716920f2ed9e6af56e465ca1233a2d84c2cc1cf005`  
		Last Modified: Fri, 08 May 2026 18:32:48 GMT  
		Size: 31.3 MB (31296400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2ce2fa16a9ab3457f94c9628fc05a5fd6d54e5d6d3d8a9e1e506ba4e5a37aa`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540be255286e8d861d09681ddd0cd64a25a1b5fa161cca9b859487c03bfb0b6e`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 147.5 KB (147521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913676b9d51d935a10d363087959dec4494fbae5fdf82b80b84e9ecaae370ad3`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 2.2 MB (2224836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224690b120957a082d3ef84ebd501af44b1437fdbf4fcefad6e8faee78e234a5`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d0c777c8b52f9e74da7bf3fd5be45dbd51ab10be8dde37fea12fc96f59cd09`  
		Last Modified: Fri, 08 May 2026 19:20:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:15a21e26469f168e5a065467f48dfed23a1a06d5e0d2b6ffdfcfcc38ff62a560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c3412186834b790b4fbbad4cfe5adfd0f39d11688631b5059120339ee474dc`

```dockerfile
```

-	Layers:
	-	`sha256:ffb482f3d82d9bd4136d15e9b8e08adece9f35076c719e0288e1de86156221e4`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 2.0 MB (2005483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe947a7402c9e03fc064053a531c1cecc9c253a0235c40625608b22c9a860d2f`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:fb4333344bfd32af4cefd042b89dff6ea8ba4bc5ab8168cbe3d29f8c9da5566a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36164277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d865655c5194d1b0446688e3b4f406d0d233869ddf3dcc2b4863b7a8721f32f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:35:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 20:35:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:38:30 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 20:38:30 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 20:38:30 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 20:38:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 20:38:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:38:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 20:38:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 20:38:31 GMT
USER memcache
# Fri, 08 May 2026 20:38:31 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 20:38:31 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2805acf219c32faae551498121eb47f3d7d32bc2a908969bd1ac04c3f49017fe`  
		Last Modified: Fri, 08 May 2026 20:38:41 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278e7e1caa6b74657254421ed3e5193837e9b6f3dde9e041e7e95383e6e68443`  
		Last Modified: Fri, 08 May 2026 20:38:42 GMT  
		Size: 170.4 KB (170351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df05fb319f87f70759df5de69b2f40702ca122c47d614f2f8861ce256eb0b61`  
		Last Modified: Fri, 08 May 2026 20:38:42 GMT  
		Size: 2.4 MB (2394326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f6a1fd9b6e9a261288b936182122f173180b726d490646ee6164ae5c95d84c`  
		Last Modified: Fri, 08 May 2026 20:38:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b93469fb91621a5f46b7dd80327995f9ca6d8361137dbe55159ef455e2976c`  
		Last Modified: Fri, 08 May 2026 20:38:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:e82c5b578718de9c7774bc11902f22157b7c49e1a253ddfe0e3496d4a461d760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89bf5432c3d996440e1d10de68af644b31627fdeeac778ee395c95a88263010a`

```dockerfile
```

-	Layers:
	-	`sha256:8a5017f90fa8e1dd648f24d4c3fa871a8dc77b8e529fe26ee3f0034a79bdd955`  
		Last Modified: Fri, 08 May 2026 20:38:42 GMT  
		Size: 2.0 MB (2011927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e26de34ce99baa5e3d603d8a2dddfc874c4b7cf85ae36baf53e81232916879a8`  
		Last Modified: Fri, 08 May 2026 20:38:41 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; riscv64

```console
$ docker pull memcached@sha256:5ddab235954c3cde3c815b6a5be674885381502972ebc53794c4811df335843c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30623277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b6d17550b0133cd405553af720539d51b95b0d50475bbcdbf6c2173bd5280b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 16:09:52 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 09 May 2026 16:10:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 16:23:27 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 09 May 2026 16:23:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 09 May 2026 16:23:27 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 09 May 2026 16:23:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 09 May 2026 16:23:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 09 May 2026 16:23:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 09 May 2026 16:23:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 09 May 2026 16:23:28 GMT
USER memcache
# Sat, 09 May 2026 16:23:28 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 09 May 2026 16:23:28 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1e9edef871271ebe58c5a713c7c062e88ff414be0976a2c7baf0aba83823c954`  
		Last Modified: Fri, 08 May 2026 20:38:39 GMT  
		Size: 28.3 MB (28280232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9888105b7154ad185e8f5227e002ba1af0f905cba713450e54261fb929e80afe`  
		Last Modified: Sat, 09 May 2026 16:24:13 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea9dc216a8ac7e5ff5123e9cec2e0c1650d9afc96015312e8f304adc6c255a0`  
		Last Modified: Sat, 09 May 2026 16:24:13 GMT  
		Size: 133.1 KB (133086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e544f8419fe19b80d411a515c9201c8c35d068e9a3ff1127e23e53c495a036c9`  
		Last Modified: Sat, 09 May 2026 16:24:13 GMT  
		Size: 2.2 MB (2208450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b939f3eba847b32e2c08af32b5870190d0195179c8dfcfba89b9abd0d24865b8`  
		Last Modified: Sat, 09 May 2026 16:24:13 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0a4092dbf93f8a2db331d4bb00d34313567e7245e5753310064f99299a2919`  
		Last Modified: Sat, 09 May 2026 16:24:14 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:84361ecaeb53a4b02619fac3c96e92f016548a953b0bb4909dbce2605c50c27e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e712edaa1f4a23a51ec2552dadfb1ba38310fc63ac1066e30c4ccd5f2d388ce8`

```dockerfile
```

-	Layers:
	-	`sha256:b27196635d6011055da056ccc202d4d6df3c0d9296b913ab5b40505f5efb56b9`  
		Last Modified: Sat, 09 May 2026 16:24:13 GMT  
		Size: 2.0 MB (2002290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f31718fda9bdd1f0330201f0a2069f169fd2f79967b828cb3138dad392f06e0d`  
		Last Modified: Sat, 09 May 2026 16:24:12 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:7f194d0409eee2a5b0bb8903485384802c30d3e8f3db4edc714dccedd365197b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32280599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71da9b051066a3ea5be228e76446413fcc99d1b892a8e007445d21d95254a5d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:18:08 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 19:18:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:21:32 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 19:21:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 19:21:32 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 19:21:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 19:21:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:21:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:21:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:21:32 GMT
USER memcache
# Fri, 08 May 2026 19:21:32 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 19:21:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875e7d47d55cac3b3811a3503e8330c2b49b3264583a0e3ffbc8380fe58dd8d3`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e487f7a355c714fc8533d060a278791698afaed2353417768b8f02bd7844e06`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 140.5 KB (140519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6bb469173a6734f9ba49a4aa2f9a1d3e6513740633df30a2d3bc37c3b9d4279`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 2.3 MB (2298219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7e59c6d93f04c1f009cbda35d2e5b25d8087cadff3126c5de7636d0c10b5c0`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa99c508f7dc7874b69603543390bb5c9a5b3bb0689bde04f6d7d53db1ce25bd`  
		Last Modified: Fri, 08 May 2026 19:21:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:b257f9c0883422f85a5c40a24940bb3401de8aac9c08bc12a87f5732d143082c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff10b6e9f782a5c6eee93b5e143ea12b75800a8ef331ebc5d73519e32464d829`

```dockerfile
```

-	Layers:
	-	`sha256:3f4b79e225835bdf97992cd4741626b92fb8ad5438feb251afbf7d6bb442a01d`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 2.0 MB (2009763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff63eebb23b55a364393e4d41fbc25ca8e9a760278a9403379c7fb549f8a1248`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:trixie`

```console
$ docker pull memcached@sha256:f7a252e7ba3fbbe9672c483354c5081d02b780122c3bb97bd311d5662b54d0ad
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
$ docker pull memcached@sha256:5f9197399e5aefcabef61b7c94d4e9578698e4a0ac391f6a4b34eb0dcd493df2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32198719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5474f3cc4ab6f46b8613ec8b77a7c6ec75f3b8944c8674fa5c02be437ee6567b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:22:04 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 19:22:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:24:53 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 19:24:53 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 19:24:53 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 19:24:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 19:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:24:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:24:54 GMT
USER memcache
# Fri, 08 May 2026 19:24:54 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 19:24:54 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95946911721deafff321fd508db9ba36e3babc47097ecd6c6bdf2ba0dd470257`  
		Last Modified: Fri, 08 May 2026 19:24:59 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2951237283f3070819f0121ee72d97873d9e5287f4ff5cd5b450147eb57c72`  
		Last Modified: Fri, 08 May 2026 19:24:59 GMT  
		Size: 136.7 KB (136676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f29d81d44c4b3a8bb7866171f79f5054acda551367bbcf5ae523080623b437d`  
		Last Modified: Fri, 08 May 2026 19:25:00 GMT  
		Size: 2.3 MB (2280301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb056d99db8480655d7742fb357ad1bd6de6b78556d46d005628eb93210eecf4`  
		Last Modified: Fri, 08 May 2026 19:24:59 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de908d42b697f6622dffc88cdd09d0a1ddb3127cbabf42fa000970465a9e1f8`  
		Last Modified: Fri, 08 May 2026 19:25:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:34e381cf324225b9dee5ca26f3ecb0ccc5f1f460edfde42459740d7a519e0328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1bcfe0acd4621e7447b151a6a20f2248402d84d7ff8d93c46b90f669ab88e2e`

```dockerfile
```

-	Layers:
	-	`sha256:4ddea0123ac32de5d1b564e296f88cb637634e258c91e4381b8bee9b175654bb`  
		Last Modified: Fri, 08 May 2026 19:25:00 GMT  
		Size: 2.0 MB (2008326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72b234be41aa76eb975368e76c3a352a83f7b9e17ea4311b77d264ba3245480f`  
		Last Modified: Fri, 08 May 2026 19:24:59 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:9bb2e143dc3647a49e4e8f85d5c418bca9b08ce1c1765c5ad7f32f5ab3d8596f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30305327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1b9575bad28b94e1186f365ab00d1a786bf0e90cc8fb820378cf08aa68513b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:25:56 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 20:26:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:29:16 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 20:29:16 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 20:29:16 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 20:29:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 20:29:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:29:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 20:29:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 20:29:16 GMT
USER memcache
# Fri, 08 May 2026 20:29:16 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 20:29:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8f774e9b92b540806fc05167db7ce09a3e1b12abdb9d496f7b8c82138656065a`  
		Last Modified: Fri, 08 May 2026 18:33:49 GMT  
		Size: 27.9 MB (27948200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b5f67bec55f95884a3889baf69e54663718d70194c4ad200c3189a69ed4f77`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0bc2199b80394dc4c86e2ec47bb2bacfa524afadd19cd9436e2cde86accf84b`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 144.2 KB (144163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652d72e4ec6b0cb1a3ca6f0de801f39fbe579385f24fdf2fa903d000df01ef7e`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 2.2 MB (2211447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e003813362a92e41a38ce899360dfc51977add71013d1cac48643e6d9361ec43`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b9b40076d0562644d2bec445a0a7fdefbf4dd5d545c7d8cbdfef18f171b99a`  
		Last Modified: Fri, 08 May 2026 20:29:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:d83c846fc98d19ba355a9a5d1c59147c565e7894fed7c5b582bd5b4bde92d90d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6056bef38756043ff8218f82594c154e80dc8d2097dd770a7bd7bb09a8e6e3e6`

```dockerfile
```

-	Layers:
	-	`sha256:4b4fd92902f7c83c67f43e813275bc5676ec6370639df11fe1394ce7fa7eef2d`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 2.0 MB (2011329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d8b1829f761528fa20afdac852bde73a128edf4c6f11e990f7e7c7fcbcfbf61`  
		Last Modified: Fri, 08 May 2026 20:29:23 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:3d1cfa4c23d23705cf3f8b9302ff26048e2ac216027f45be24e93b8f0817a952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28516943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:582f213c6b868ce82f6e14b78c661812d0781e91331e3ca32ce462777a0529fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:16:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 19:16:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:19:15 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 19:19:15 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 19:19:15 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 19:19:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 19:19:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:19:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:19:15 GMT
USER memcache
# Fri, 08 May 2026 19:19:15 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 19:19:15 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f1433620eadfdfe016c8054b954f619ae5bca159f35a9459c36a76d9ef4d39c3`  
		Last Modified: Fri, 08 May 2026 18:37:58 GMT  
		Size: 26.2 MB (26214912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851a3dc4d05ac8ea75d436c9d8de99f7ca3c80f159cadffd985253ae10a40069`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18a5b288c05e8d152bf1530b1c4248c0ea5c08902853e0955c6838d5d418b33`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 135.4 KB (135388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff024d65a6401c67cefb240a3ef3d181382530d66cfbb03f13ff32d81500525`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 2.2 MB (2165127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0613bb171f6d5dee88871aafa9a91daf991e3d262feb8682aa8fb5696046579`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c1a297997b8b44cdcad29c590e65efa7934da84dacae1fbddd2b017bb0dd03`  
		Last Modified: Fri, 08 May 2026 19:19:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:e7210267977b9ce03df4bc38f1d1ea5760217f9f582f392ac648876a13580041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120a3ae5c0ce21313dc99a5a24a7d9ae48f434e40717325fda7675fc368c3a9e`

```dockerfile
```

-	Layers:
	-	`sha256:b2f6d69af7f79690357135d68c570ab105358d093cb3ef2b6b37d8c0c4b8766a`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 2.0 MB (2009786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19ecae093d7ef811fe61bf6ed6706bf88a86ab363852e511e19d077fea8bdf22`  
		Last Modified: Fri, 08 May 2026 19:19:21 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:4a47319c5ea763766ec14f7f49c71294e7621973dbf1d934330b273a50d86ae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32560787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea04a0e8415a1e901722a2dc626f036034b99c11dd819b6aab54fe2172610825`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:21:07 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 19:21:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:24:08 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 19:24:08 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 19:24:08 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 19:24:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 19:24:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:24:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:24:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:24:08 GMT
USER memcache
# Fri, 08 May 2026 19:24:08 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 19:24:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73f16d12b26b60a37ae242c9f12503fa0bb655f780014ce964bf39b960ea39a`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f45dfab4b00618ca4983d73b6acabb6fe1e056339b0cafcc1c0268303c02b89`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 153.5 KB (153496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91da4495c7aeb14802d9e2f3854b2226395b2886efcb91a3f91778774632602`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 2.3 MB (2262131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91f17f562e485ed0d6523251b77ca57f1df60d00243de97a13459b077fb30df`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70d0b5c5805a6bd639b55f25e9fb45c11035876f9fca3e2ab607fb2d818b01f`  
		Last Modified: Fri, 08 May 2026 19:24:15 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:003da519f1303287f7dbac93d59fd8f7cd3bd4f7c1c3f59e2ea25f3e1933a4a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b34e9510fcd3b35da3965f941f9c4d3bdf0eff1c30985a7ce5621b638e4c237e`

```dockerfile
```

-	Layers:
	-	`sha256:6041a557446d392656291f000150951d92c8392a387515be5c7e384d175a1967`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 2.0 MB (2008642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e39754d938ea3671f3babce3fbab5d612247a51cbc9f172de306c3fcf60e3a1b`  
		Last Modified: Fri, 08 May 2026 19:24:14 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; 386

```console
$ docker pull memcached@sha256:ae0c2a4ef3d5a1336f8204efdb14230b37402d5f8c4096295ddd0f53b7e041ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33670271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d71af2d7fff4e8bb864857f69883ac131a512bb9311bb23de7031cb892e38a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:17:17 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 19:17:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:20:22 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 19:20:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 19:20:22 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 19:20:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 19:20:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:20:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:20:22 GMT
USER memcache
# Fri, 08 May 2026 19:20:22 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 19:20:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:43e2ffbaa23260ffb4e3de716920f2ed9e6af56e465ca1233a2d84c2cc1cf005`  
		Last Modified: Fri, 08 May 2026 18:32:48 GMT  
		Size: 31.3 MB (31296400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2ce2fa16a9ab3457f94c9628fc05a5fd6d54e5d6d3d8a9e1e506ba4e5a37aa`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540be255286e8d861d09681ddd0cd64a25a1b5fa161cca9b859487c03bfb0b6e`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 147.5 KB (147521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913676b9d51d935a10d363087959dec4494fbae5fdf82b80b84e9ecaae370ad3`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 2.2 MB (2224836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224690b120957a082d3ef84ebd501af44b1437fdbf4fcefad6e8faee78e234a5`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d0c777c8b52f9e74da7bf3fd5be45dbd51ab10be8dde37fea12fc96f59cd09`  
		Last Modified: Fri, 08 May 2026 19:20:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:15a21e26469f168e5a065467f48dfed23a1a06d5e0d2b6ffdfcfcc38ff62a560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c3412186834b790b4fbbad4cfe5adfd0f39d11688631b5059120339ee474dc`

```dockerfile
```

-	Layers:
	-	`sha256:ffb482f3d82d9bd4136d15e9b8e08adece9f35076c719e0288e1de86156221e4`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 2.0 MB (2005483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe947a7402c9e03fc064053a531c1cecc9c253a0235c40625608b22c9a860d2f`  
		Last Modified: Fri, 08 May 2026 19:20:28 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:fb4333344bfd32af4cefd042b89dff6ea8ba4bc5ab8168cbe3d29f8c9da5566a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36164277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d865655c5194d1b0446688e3b4f406d0d233869ddf3dcc2b4863b7a8721f32f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:35:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 20:35:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:38:30 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 20:38:30 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 20:38:30 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 20:38:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 20:38:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:38:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 20:38:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 20:38:31 GMT
USER memcache
# Fri, 08 May 2026 20:38:31 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 20:38:31 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2805acf219c32faae551498121eb47f3d7d32bc2a908969bd1ac04c3f49017fe`  
		Last Modified: Fri, 08 May 2026 20:38:41 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278e7e1caa6b74657254421ed3e5193837e9b6f3dde9e041e7e95383e6e68443`  
		Last Modified: Fri, 08 May 2026 20:38:42 GMT  
		Size: 170.4 KB (170351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df05fb319f87f70759df5de69b2f40702ca122c47d614f2f8861ce256eb0b61`  
		Last Modified: Fri, 08 May 2026 20:38:42 GMT  
		Size: 2.4 MB (2394326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f6a1fd9b6e9a261288b936182122f173180b726d490646ee6164ae5c95d84c`  
		Last Modified: Fri, 08 May 2026 20:38:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b93469fb91621a5f46b7dd80327995f9ca6d8361137dbe55159ef455e2976c`  
		Last Modified: Fri, 08 May 2026 20:38:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:e82c5b578718de9c7774bc11902f22157b7c49e1a253ddfe0e3496d4a461d760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89bf5432c3d996440e1d10de68af644b31627fdeeac778ee395c95a88263010a`

```dockerfile
```

-	Layers:
	-	`sha256:8a5017f90fa8e1dd648f24d4c3fa871a8dc77b8e529fe26ee3f0034a79bdd955`  
		Last Modified: Fri, 08 May 2026 20:38:42 GMT  
		Size: 2.0 MB (2011927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e26de34ce99baa5e3d603d8a2dddfc874c4b7cf85ae36baf53e81232916879a8`  
		Last Modified: Fri, 08 May 2026 20:38:41 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:5ddab235954c3cde3c815b6a5be674885381502972ebc53794c4811df335843c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30623277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b6d17550b0133cd405553af720539d51b95b0d50475bbcdbf6c2173bd5280b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 16:09:52 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 09 May 2026 16:10:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 16:23:27 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 09 May 2026 16:23:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 09 May 2026 16:23:27 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 09 May 2026 16:23:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 09 May 2026 16:23:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 09 May 2026 16:23:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 09 May 2026 16:23:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 09 May 2026 16:23:28 GMT
USER memcache
# Sat, 09 May 2026 16:23:28 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 09 May 2026 16:23:28 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1e9edef871271ebe58c5a713c7c062e88ff414be0976a2c7baf0aba83823c954`  
		Last Modified: Fri, 08 May 2026 20:38:39 GMT  
		Size: 28.3 MB (28280232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9888105b7154ad185e8f5227e002ba1af0f905cba713450e54261fb929e80afe`  
		Last Modified: Sat, 09 May 2026 16:24:13 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea9dc216a8ac7e5ff5123e9cec2e0c1650d9afc96015312e8f304adc6c255a0`  
		Last Modified: Sat, 09 May 2026 16:24:13 GMT  
		Size: 133.1 KB (133086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e544f8419fe19b80d411a515c9201c8c35d068e9a3ff1127e23e53c495a036c9`  
		Last Modified: Sat, 09 May 2026 16:24:13 GMT  
		Size: 2.2 MB (2208450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b939f3eba847b32e2c08af32b5870190d0195179c8dfcfba89b9abd0d24865b8`  
		Last Modified: Sat, 09 May 2026 16:24:13 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0a4092dbf93f8a2db331d4bb00d34313567e7245e5753310064f99299a2919`  
		Last Modified: Sat, 09 May 2026 16:24:14 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:84361ecaeb53a4b02619fac3c96e92f016548a953b0bb4909dbce2605c50c27e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e712edaa1f4a23a51ec2552dadfb1ba38310fc63ac1066e30c4ccd5f2d388ce8`

```dockerfile
```

-	Layers:
	-	`sha256:b27196635d6011055da056ccc202d4d6df3c0d9296b913ab5b40505f5efb56b9`  
		Last Modified: Sat, 09 May 2026 16:24:13 GMT  
		Size: 2.0 MB (2002290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f31718fda9bdd1f0330201f0a2069f169fd2f79967b828cb3138dad392f06e0d`  
		Last Modified: Sat, 09 May 2026 16:24:12 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; s390x

```console
$ docker pull memcached@sha256:7f194d0409eee2a5b0bb8903485384802c30d3e8f3db4edc714dccedd365197b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32280599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71da9b051066a3ea5be228e76446413fcc99d1b892a8e007445d21d95254a5d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:18:08 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 08 May 2026 19:18:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:21:32 GMT
ENV MEMCACHED_VERSION=1.6.41
# Fri, 08 May 2026 19:21:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Fri, 08 May 2026 19:21:32 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Fri, 08 May 2026 19:21:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 08 May 2026 19:21:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:21:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 08 May 2026 19:21:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:21:32 GMT
USER memcache
# Fri, 08 May 2026 19:21:32 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 08 May 2026 19:21:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875e7d47d55cac3b3811a3503e8330c2b49b3264583a0e3ffbc8380fe58dd8d3`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e487f7a355c714fc8533d060a278791698afaed2353417768b8f02bd7844e06`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 140.5 KB (140519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6bb469173a6734f9ba49a4aa2f9a1d3e6513740633df30a2d3bc37c3b9d4279`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 2.3 MB (2298219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7e59c6d93f04c1f009cbda35d2e5b25d8087cadff3126c5de7636d0c10b5c0`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa99c508f7dc7874b69603543390bb5c9a5b3bb0689bde04f6d7d53db1ce25bd`  
		Last Modified: Fri, 08 May 2026 19:21:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:b257f9c0883422f85a5c40a24940bb3401de8aac9c08bc12a87f5732d143082c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff10b6e9f782a5c6eee93b5e143ea12b75800a8ef331ebc5d73519e32464d829`

```dockerfile
```

-	Layers:
	-	`sha256:3f4b79e225835bdf97992cd4741626b92fb8ad5438feb251afbf7d6bb442a01d`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 2.0 MB (2009763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff63eebb23b55a364393e4d41fbc25ca8e9a760278a9403379c7fb549f8a1248`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json
