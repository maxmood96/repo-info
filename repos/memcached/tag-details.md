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
-	[`memcached:1.6.40`](#memcached1640)
-	[`memcached:1.6.40-alpine`](#memcached1640-alpine)
-	[`memcached:1.6.40-alpine3.23`](#memcached1640-alpine323)
-	[`memcached:1.6.40-trixie`](#memcached1640-trixie)
-	[`memcached:alpine`](#memcachedalpine)
-	[`memcached:alpine3.23`](#memcachedalpine323)
-	[`memcached:latest`](#memcachedlatest)
-	[`memcached:trixie`](#memcachedtrixie)

## `memcached:1`

```console
$ docker pull memcached@sha256:9ae868852d0bc0974e4dd39c58436f73698081a31e61b8099871983e09d79f80
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
$ docker pull memcached@sha256:c9046d2a0ade04c91892254044294c2a529006458cd7b98bdc31b4054fffbfe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32193341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6654931990345ba058b2f50cedc8d03dfcc174d6809b0e7a820c12f7b93dc09d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:35:37 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:23 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:23 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:23 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:23 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:23 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b6bc7772cb8044287682c4af75ca1c8280c4837d5ffee58adc014018f02e91`  
		Last Modified: Wed, 17 Dec 2025 21:38:42 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3af321fdb36bbbb634d6be4a6e457f7eeb47b153460c7bab6c9eae91724b08b`  
		Last Modified: Wed, 17 Dec 2025 21:38:42 GMT  
		Size: 136.7 KB (136691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a00f7c8e317ad005bdf0117005dd753e347a8674b068c660bbc29b3f93a0621`  
		Last Modified: Wed, 17 Dec 2025 21:38:42 GMT  
		Size: 2.3 MB (2278641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb739034830ce246e4bc00aa883c7d2af8a1fd59bc3e2ea17cae3607bf281074`  
		Last Modified: Wed, 17 Dec 2025 21:38:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33cfbae525009776fcee65339602ed1b2a8a5f2c51898ec9fc499fe35c60b87`  
		Last Modified: Wed, 17 Dec 2025 21:38:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:e726a4ddf8221754a6a9fa1143cee47f51785aedb20dc0329a7c7b41b4772763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd3f16921a7fcccc9bc6ee3685e192e34a0b621f1c95362d6cea5e4293e54d33`

```dockerfile
```

-	Layers:
	-	`sha256:3a55af39eac38dca280008ae509d726055b1dde6e05ce9024174d0a0bd0565c2`  
		Last Modified: Wed, 17 Dec 2025 22:34:37 GMT  
		Size: 2.0 MB (2008228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef418f126bca0d267c3b365faed9990a104832e94e7ec35841aff2c2b26510dc`  
		Last Modified: Wed, 17 Dec 2025 22:34:38 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v5

```console
$ docker pull memcached@sha256:c1a14cf6b3aa6f9ee13feee1c176a4ff104ec3d361f2df684e87a9d88a563eaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30300251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7375c421f8c059114c1a5cdc58215c8cf41dcc23355cbef325fdfa4b290df1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:39:00 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:39:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:42:24 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:42:24 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:42:24 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:42:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:42:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:42:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:42:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:42:24 GMT
USER memcache
# Wed, 17 Dec 2025 21:42:24 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:42:24 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d97bc71d0fa535127863fdab265dfddb07b3cda35b80de4dd2b9b67fe154c856`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 27.9 MB (27944187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e168dbb57c754690bc257f600efb5085929be35091c7e3d6926d35490c3391`  
		Last Modified: Wed, 17 Dec 2025 21:42:38 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78870a4506eecc7b424a3cedde90baa4c44a7c5d1174e6842b60c11b08a7984e`  
		Last Modified: Wed, 17 Dec 2025 21:42:40 GMT  
		Size: 144.2 KB (144157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e35d5393bf24a4f7ba0c87d734e7fda2d09414dec61e9139726200bed52e262`  
		Last Modified: Wed, 17 Dec 2025 21:42:39 GMT  
		Size: 2.2 MB (2210395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72c9d61ca04e663f67ab23ad2c50afcd810d29c2f52728277947d5ab78c03da`  
		Last Modified: Wed, 17 Dec 2025 21:42:38 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e89f91fff1d699acc4ebbc8ebb2a409d5f7867914100e87affef7b7d8775488`  
		Last Modified: Wed, 17 Dec 2025 21:42:38 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:3a82f6da1fa8b6c43220785849304c0e09363556371c8f763abae2126e271c5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e59d44e1c5460c7338a49dad6ec9d6d03db5b9330bb235c1d01e3e182df704ca`

```dockerfile
```

-	Layers:
	-	`sha256:2b38edaa9de8bf0d9055274c5ca1c0af276da0f57396ee1edfb8db1002dc8834`  
		Last Modified: Wed, 17 Dec 2025 22:34:42 GMT  
		Size: 2.0 MB (2011231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c70377fb854a2602cbb12ee80dd69f8a5deb00e23feb0c3c24e1b27806029b0d`  
		Last Modified: Wed, 17 Dec 2025 22:34:43 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v7

```console
$ docker pull memcached@sha256:b7ad53cb1e5a5631cc9b08d0fe984b0ba6bb7ab77da4309a552dbb97bd4ae04e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28510860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b2fbe25ebf8c8035604591c6ded5acfffe219c97c853c1c0e00421ac18abcd4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:35:20 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:30 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:30 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:30 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:30 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:30 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:30 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d46de1cc714aa644c02bc1b184e957b7330bf3473d4e97f72f454fdc8a432d`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0327c8719a60b04c8b690d8d0a0a122cdbc620f2aab391fd43789a8803b62bf1`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 135.4 KB (135362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd55327cbd82c4adf176e679bae5436e8aaf27c54595ec2cd7cfec20989b1fc`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 2.2 MB (2163972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37babf40b7b24af06cfbfc9fe6daf7d6f5863de148318182eecf29e242ba5e4c`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3daf0d6e9f1032a9bce2c34a57a6049ec4ffd4a412a20724540653fe7b6526d3`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:77b0259560abd3025ae0593b06db95eb3c4dd6dccbd2332f85286fae97d799bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd1267e1c8eb093b3e5a265d3c2d0c9b2b3784e50b6aa7edfec29ba838d4a8c`

```dockerfile
```

-	Layers:
	-	`sha256:3266292cf75a57aab22a4e279bf40458841e617570f3ee192bb26dc1d2d6e1ef`  
		Last Modified: Wed, 17 Dec 2025 22:34:47 GMT  
		Size: 2.0 MB (2009688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cc2be86d85bc478731bb7718f18d50da352f58c942412f66ca371226633d3bb`  
		Last Modified: Wed, 17 Dec 2025 22:34:48 GMT  
		Size: 22.3 KB (22303 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:230a135d43b1bf876ec5c160b78cb4f0303d1e6e98dc76a31dd524d28a4a5279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32554912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79214d48c3616d6c032db23eb36a6766c7a96a8d4619d8f8791d2fa43163cc34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:35:24 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:26 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:26 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:26 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:26 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:26 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:26 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f49eb557c72f2fe7e0eb1949c1587e8e4c86bdae514d70fac3ff429290a149`  
		Last Modified: Wed, 17 Dec 2025 21:38:46 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f764f8f3ed63ac8e640ebdcb2f5ea0371b6fb244a1f6defbe51ddfff908a34a`  
		Last Modified: Wed, 17 Dec 2025 21:38:46 GMT  
		Size: 153.5 KB (153477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9353d672d9aeb0b8a3ee269d120b0b920e9f6b81998ed7ef7765092573e4b716`  
		Last Modified: Wed, 17 Dec 2025 21:38:46 GMT  
		Size: 2.3 MB (2261292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ba4d16dc49a02e1490d18a58f5e108ec18a248f9ea83bb7b4deb8642b36f90`  
		Last Modified: Wed, 17 Dec 2025 21:38:46 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d15340fcbda1a05a50ba392408ace29b5cbb21b398bb1018750621349d3b0a`  
		Last Modified: Wed, 17 Dec 2025 21:38:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:d2a465ef21f85d63f634e52f05c50319a05c013d1aeed6321cc146b3a28a5920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c092dec716fd21afebb19ce5e88ba467a0f4bb88a40068e3e266b1f10ff6652`

```dockerfile
```

-	Layers:
	-	`sha256:b7bd1c3aaf184ba5d6dfbf328c24c2f39511de9c6e21c04b7fa212d6a26b0049`  
		Last Modified: Wed, 17 Dec 2025 22:34:53 GMT  
		Size: 2.0 MB (2008544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc6165d17a79a40bba13d288c74c5c34aa4af72304a300a74ceededf1a934bbc`  
		Last Modified: Wed, 17 Dec 2025 22:34:54 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:35df20cb1713a9d5fbb1820acac102f3c3560dfa2d0fa147fff30dfc53f209bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33665704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ccada050045e330c6b125cae2adfcf8e5edb8e23b5e044c0d53861f7762294a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:35:51 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:43 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:43 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:43 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:43 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:43 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b054f6842adaecae2d5cf75c99601b690566759a58606bc981ccae49baaae51`  
		Last Modified: Wed, 17 Dec 2025 21:38:57 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43efb4f909536827644b2ca98420204710b14f6195238a8ffdbf658c29883be`  
		Last Modified: Wed, 17 Dec 2025 21:38:57 GMT  
		Size: 147.5 KB (147519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:792eb292285447291b91c55e07bc1a75b3d4e125a3c23f80671848c5f967e042`  
		Last Modified: Wed, 17 Dec 2025 21:38:57 GMT  
		Size: 2.2 MB (2223600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe79378953d034686129f0d36718bb867ebebf130cd1f431ad68cf117a1308c6`  
		Last Modified: Wed, 17 Dec 2025 21:38:57 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92088f114f464c2f2e1217404e900d24a46a03305faa6cae793f0b873cadba52`  
		Last Modified: Wed, 17 Dec 2025 21:38:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:3a428e326360172543ee458a46a55c1b9e70d3eeeea945f2ed65839c307eddd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a62b1d6c9ce3819b6b67f9de9cc436a2f4cb362fad3a8c07627fd790e4bd8be7`

```dockerfile
```

-	Layers:
	-	`sha256:0f8e75010a0e7df5356c9c36b97dff2c5d2191f6f6e643619b4363f8c1e1dc42`  
		Last Modified: Wed, 17 Dec 2025 22:34:58 GMT  
		Size: 2.0 MB (2005385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98883c6827ebd9ca960545767f09a2be89e7580fc425e24f86364f3a9e4ea283`  
		Last Modified: Wed, 17 Dec 2025 22:34:59 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:38a236f83eb206f786b39c53e8f756815f0bda1460157b11844faf21735208bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36162589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41292f5c75fe5f3a464b809bde41e0ae8849ad8d7046918a548d0c6b2e250a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:34:54 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:28 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:28 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:28 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2b42546c7b688160cfd1a0da61a24922a019b4ebead88e23aff01482ddd477`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4efe9fd2e012174cd86a64f83d7b7facfe14ee67c9c9fa5ce994f22c24173f2c`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 170.4 KB (170393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9752985ba696f0f8d5831ac91e19bfe336342b1c403542641c575b1dc6116e`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 2.4 MB (2393786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d11c68ba0bc913d139eea51cb2957c1ddd713515fc06dfa5d4c398b119535a`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9186b8b7184cef442ae3ed6a3feadcaa8f4ccc974ed5ae6c6cf8efe37e679f23`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:00d1019e9978171df76f638253f212405bf7d53251607ef5a5933d5b28d867b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588d3d6ab54a9ea5c8baf9b013bb23c12826989ba0d09cb862431e2fa30e5189`

```dockerfile
```

-	Layers:
	-	`sha256:799ad025578a6d5d0155dc5be223bfbc25ffa3aa0548e4fb2e4bedeb0a5088d9`  
		Last Modified: Wed, 17 Dec 2025 22:35:03 GMT  
		Size: 2.0 MB (2011829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaa03114ccb63fbbd8ca04eef46baa26c8a0508f1256aa45d851f3a49f2ed47a`  
		Last Modified: Wed, 17 Dec 2025 22:35:04 GMT  
		Size: 22.2 KB (22225 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; riscv64

```console
$ docker pull memcached@sha256:5aedcd2b04ff2d8dc77fb6568e6ce96878f75508a3a01326623b60869874f8a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30615184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab5d9dd83f52434969fb6da016bd60451fd5d989e33e2cd491533dcb4553c835`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 05:30:55 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 09 Dec 2025 05:31:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Dec 2025 03:19:32 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 03:19:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 03:19:32 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 03:19:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 18 Dec 2025 03:19:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 03:19:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 03:19:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 03:19:33 GMT
USER memcache
# Thu, 18 Dec 2025 03:19:33 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 03:19:33 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb23364b88c4686dab6a11bf004aac89beea8adb8559fd39799a54dc729c23a6`  
		Last Modified: Tue, 09 Dec 2025 05:57:38 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edeeae49e27528d2079d0d5aeb702d7dd56503463fa4054ee2444f847f399650`  
		Last Modified: Tue, 09 Dec 2025 05:57:38 GMT  
		Size: 133.1 KB (133076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e584b688c99191b71a2471afe63daff415a1eedcf541b959dfcdf248eebd8577`  
		Last Modified: Thu, 18 Dec 2025 03:20:28 GMT  
		Size: 2.2 MB (2207438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b780b2b80274922cc63f0afe1ecd2680bcafae3234732fd03ba740690e3ebf1`  
		Last Modified: Thu, 18 Dec 2025 03:20:28 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5449346fa21339be4109a2e289721bfa7b0e8203b88fe202956ebb257c703a88`  
		Last Modified: Thu, 18 Dec 2025 03:20:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:bbe7bbb4c3590b1fc9c5943719d3b1b2a21670d2874ed90415040aeae5b13200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c721ad9798565707f4e9e537a1618b5efafce47c49577053fe7b40879caca9`

```dockerfile
```

-	Layers:
	-	`sha256:37125be6342f13dcb1fff2b0c3def6d6f3b808e19192f9ff68a139ce2d1d3083`  
		Last Modified: Thu, 18 Dec 2025 04:34:34 GMT  
		Size: 2.0 MB (2002192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06edc085828555adcb8aac4ef4e564c72d260338e77dde6abe811eefcdd8682d`  
		Last Modified: Thu, 18 Dec 2025 04:34:35 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:1e7fc2740e66d7d7b21982f73ae72e901616fcb9ebc6176c6f1d931c6a4732b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32273737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f632195b7b4a10526fcb27d2d66a479b07455d784656340bcbae2d31e292aa2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:34:51 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:34:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:04 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:04 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:04 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:04 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:04 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:04 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9606e3e114197b678b6fbd5b889ab574d2ad4cd8b4010407f847a98309f0f6b`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24f23dd2596713c0a8daf1cde9aabc7d26e7e9b832300ba1ce4615e8c806afc`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 140.5 KB (140507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0dd33ff71e256560cf1693538e8ecc4f92550f6483c1478697b822abf8d0f84`  
		Last Modified: Wed, 17 Dec 2025 21:38:19 GMT  
		Size: 2.3 MB (2297315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568ee6e9ecd99ef323ff6ff6b40b5fcf91b13472f56ac46f8b3036c82c705fd6`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91a63e3e27d493e5ad7b64edf0b8ae2bb8ade89a55bfc197b4dc9a393ceec4b`  
		Last Modified: Wed, 17 Dec 2025 21:38:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:d9aa5142dc8acd96ae2fb7235ceda06498adc21053e1bc5bf02ff76701213426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e87c93018f4f94a4286dcf6f6d33373729ef4263208b2f346e92a2028839a2`

```dockerfile
```

-	Layers:
	-	`sha256:c0ee3f2287a538730e473aea557f8fc2a48d18bb9e778e65ccdbf8918310ace3`  
		Last Modified: Wed, 17 Dec 2025 22:35:11 GMT  
		Size: 2.0 MB (2009665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce86917337210887b4362390f278a89c9fc6d6d1cc50e29ebf7f716bc556c877`  
		Last Modified: Wed, 17 Dec 2025 22:35:12 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:6f20032236ee1e3ae7edb0f8a060ce3d8c66cfad7a05fe84cfe88001f70a4eb1
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
$ docker pull memcached@sha256:9573a2399011fa86bb7b5d12bdab987d7931c98ddec0ef6802de7eb6d3c3e338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5956768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c79853acc5f24e9c28f15d45cef0aedc114e76bbacf7958eb6f555c22246e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:34 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:34 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:07 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:07 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:07 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c33ac8581cd04f31208409f36331e938a78e6ae3a7a3b530fe9dfebe6eb9ad`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583aae99135b9036c602a1c60743fc4fd519f261ac6d48ed60b01e1beb019e7f`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 106.0 KB (106050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ca22885c42a537f033850e8dff7eaeddbb7514902286739b48c084b55a8d6b`  
		Last Modified: Thu, 18 Dec 2025 00:32:19 GMT  
		Size: 2.0 MB (1989265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d146e2038834770bed57033a6c5d66ead5b731b8b133856dec6726ca21baee9`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c66e6c3acbe07806e3e96a97d97a2d4503713c4814d9b24a2f57f2c39200d05`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:cfdf2ea6bf2a04bb7ee1568efe0c8bd38a1f5e644250a9409479cce281891ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de792623281192b3965fdc95f31532c4d166e731f53e202be1e2a224c654633b`

```dockerfile
```

-	Layers:
	-	`sha256:87a0d23eeeda6353dfc603cc4ffee062e5383be07b611754f3a88db3fc644036`  
		Last Modified: Thu, 18 Dec 2025 01:34:48 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b73cd5efe31baa1fbf0eecea269426edcfc795cbb9b5dd74b523ff51b6f7c9f`  
		Last Modified: Thu, 18 Dec 2025 01:34:48 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:c1a12b64cc8b47f50ea4610d9c1c362da7157b3ba67deac8b4760e6b589cde75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5611647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3591f95cad049a0509bd23a95556f8f848452d2a5491ed00bae293897c7a6b2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:27:48 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:27:49 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:49:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:49:50 GMT
USER memcache
# Thu, 18 Dec 2025 00:49:50 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:49:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf585eb2bfa372c2097b9f7a5214ecb0941a30581b10fb74a26518fcc7addec`  
		Last Modified: Thu, 18 Dec 2025 00:50:01 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bb148ea8fbe93dd8097d85f9ee3cf547d314e669748b4239c05711b0d5f719`  
		Last Modified: Thu, 18 Dec 2025 00:50:02 GMT  
		Size: 102.7 KB (102652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6549359cda37ac41cf41a5ece5f37f1322a82f6b232f12e446c62840637093e`  
		Last Modified: Thu, 18 Dec 2025 00:50:02 GMT  
		Size: 1.9 MB (1939215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041e37eaffefcfb0809564ddea591be3cd818de5530e2c853c0bc9a2fa25c116`  
		Last Modified: Thu, 18 Dec 2025 00:50:05 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7907ae218c75b36c9a9002be8554131c271cde78b0280cb7a85029f99ad0bcdc`  
		Last Modified: Thu, 18 Dec 2025 00:50:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:a9c26fc290551b691574e093d3c28f4fe7b558b3f8173b3c99eb8a664c83a8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ca65d7156e6586d96310ea3162facd9849d5460d2939b461a25247b06a4d59`

```dockerfile
```

-	Layers:
	-	`sha256:d9c217dc241f1175812c47b6489d325a0574c0da554c6f8aa0b86a2d8aff05f9`  
		Last Modified: Thu, 18 Dec 2025 01:34:52 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:cee00a47bf7b8b5899a6cf1f5c692494df31b454f52b81f3c4886905a0c9bdd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91d78dbe118f2b7b0d6e850e1115de72c4fe3e30c55a5b53d8a844d14357d16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:56 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:30:57 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:33:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:33:51 GMT
USER memcache
# Thu, 18 Dec 2025 00:33:51 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:33:51 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa22c446792763e48f4680945ccc68d43c7906ef35a92e0b908f57ef53e72f0`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954155078f2265364295ebdf16fb114e991b1938d8a6951fb511163ab3b2b385`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 92.4 KB (92378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a25584b03ac5e45c66c3c616acfd9df1848e5db25219ef20feb2868c30c6332`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 1.9 MB (1897191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f237be962bb57c3f749904b5925c8e1d7e9013dfac7dd52cc9611ada81858e`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b07d9170b246a631c262d9f5d57f49278f7cd4805463b90b14aeca4dc61d93`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:64abe011fed6a9cf7b3290c752c50bffe81bb2e65cf6337e023efda87d49b451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b251b9c15ab7c5742bd3ab725df09f0ecb9f2491f92cf1c825bec598a31f4407`

```dockerfile
```

-	Layers:
	-	`sha256:1882c6d4361100a29fd5ab265587f65fa27b1df15e7f9349b30dac454facf98e`  
		Last Modified: Thu, 18 Dec 2025 01:34:55 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf0a88ab3838de6beab653497ab62a64cfb87b1dc83c5fa5b6f3907abfd88080`  
		Last Modified: Thu, 18 Dec 2025 01:34:56 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b6c3042e2bf09ec3d3f054d03b81313e8df717a49371ce916ff743e602796bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6285509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6691028570bbd843e6da26558c46162b8383212fcaaefcecb2d3f919e3401429`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:19 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:06 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:06 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb7b8445facedfc145b9478f74880f520776460f153005b7f437ec339aee530`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1853c901134389608b6e80aaa3e43cd67a35c71aecfdde4b5b7ed3b989a03c`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 121.9 KB (121860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a01d1ac5ce47f4494363e411e1cd25dea26438213a2d18d6bb104d0974d9a52`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 2.0 MB (1966561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115624f24ba74d393c2da3d65ed5b35a7afb3fa9ad143d3fb82c64953b3d0401`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87bba524314294ca97195ce65a35ec6d42d3f9f18c9cc0c05c064c9a3cf85c0`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2feda8921a7d67cd9f2f3d7186ed69ceb0d3c22af7a20bd230664e9bcf39096c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73c6548a24cc8ce7782d03377e89a4b4b0e4c2a48cd3a03a79193320fc4d834`

```dockerfile
```

-	Layers:
	-	`sha256:984e438122735983bf56bc3d638fb1b0baf8cfb26ce26f71e0a9b847d25f76b5`  
		Last Modified: Thu, 18 Dec 2025 01:34:59 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d6e8d91ca57b45f0050ec3833a8f09a7ce62f7ba9ec70e1ae12881ad4b2bb6f`  
		Last Modified: Thu, 18 Dec 2025 01:35:00 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:df1ba8af73cd6e3f8227557b097cd6b128ec0d410a3bbe7a2c282089c5641b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5740953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78dbfc1f8ea65ad6466795e278180963d4afe98dfbca4a4497bc73c99f07ed4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:43 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:44 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:29 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:29 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37ec5bf455c1d98d22e6f3dacb5b971dac8ea96d1fe9b9177a07c5277530646`  
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b2862af05c1582c8625c82ea0863dc2b6474e410d3e6a32876c920e0152c73`  
		Last Modified: Thu, 18 Dec 2025 00:32:42 GMT  
		Size: 110.7 KB (110740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30872a43f6c591fd9b979b49b0fb32107b4bfa8c1155657fa255aa199cf0b83b`  
		Last Modified: Thu, 18 Dec 2025 00:32:42 GMT  
		Size: 1.9 MB (1942762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a62c11b4aeceaba2e5e73a1bc29aa8b4fc42ccd0c7e8512cc11b96e48aef2f`  
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f553d362a11992264bf5364cfe13d248403c5baf2ecac784c26f444dbfb90388`  
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:e3b020c2afd9ae372e234c6ab67456908861fd24200448fd3cf741503a8a6f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abfcddfb1575f6cc07e51c6a379141589de7ea8c329a9bc5c1592f3186e6fda`

```dockerfile
```

-	Layers:
	-	`sha256:ff9be8ef1bab92275eb15ae5fd6a05e767abc1fe855455766200b3c0a1866e33`  
		Last Modified: Thu, 18 Dec 2025 01:35:03 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d7026bdf84e278b6976f0ccab2297ddc0284cf329414f56d12608dbc2acb940`  
		Last Modified: Thu, 18 Dec 2025 01:35:04 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:7292c7b145e08f87f78644bf2c3355fad1d0b4d9366f173ffa0634c3ec93addf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6031729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae72ba97ecea986f01bda1eb392aee1ded4b5a86b2edcabe92a2034143e155b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:33:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:33:42 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:36:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:36:14 GMT
USER memcache
# Thu, 18 Dec 2025 00:36:14 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:36:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c95450233dfe3e06529eb39ca4b46e6ad51ccf338cab64157669ff1fc0a8d72`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4079a2d61bafcf146b8f57b35f0e39bf2548e0963be10cff5086f9a56ccdd9d`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 126.3 KB (126257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f69efa1066815d67cf415d0aac5dcd305032257b6bded5a4c57a7444a1e7fd4`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 2.1 MB (2076363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357f4165f53a3d4c66ef270bcb5b5283a066af50f79924cccc7c73f6a4f6f4ab`  
		Last Modified: Thu, 18 Dec 2025 00:36:36 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a65ff5cefcbfc874c1cac0857339eaee0b07147dd26b6bfa18c00921b4f30c`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:1d06281345f2ac44a607d40d5e87de6abb99bbc6ee82d319e73f3794602d0282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4867a5aa08041c7e5ec69dfc84214226a7323d1ce703747ae2117675e2f74bcd`

```dockerfile
```

-	Layers:
	-	`sha256:282960f007d3f1f008333191d98a2ded5ff0f83075ace30043349b6c082c18fd`  
		Last Modified: Thu, 18 Dec 2025 01:35:08 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4755fffd5924e8405adfbed0f328ad9792eff20e2b8ad2025e1f5c85bca88618`  
		Last Modified: Thu, 18 Dec 2025 01:35:09 GMT  
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
$ docker pull memcached@sha256:e011484878fd5d1e2da6de478ac11d01ae80f0bdef1902dcde3ed53728803741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5857090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689ea71c305b80e206c68a215481290a1378e6375e32ad059455f7d041396aa6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:26 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:30:27 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:33:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:33:46 GMT
USER memcache
# Thu, 18 Dec 2025 00:33:46 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:33:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4594a6826f7ed03c8c4f9f2aebb9716eb6e16d5b5ab7e1bc247783b503c5b10`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f270744f8d8b82bc6657387109b33836a76d6dbf8faa645a997db7ea290cdb`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 114.3 KB (114299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91f8ee8f36703944a7bdcaf57cc5772fe9f79c74a088c33fa1b6da7de119f93`  
		Last Modified: Thu, 18 Dec 2025 00:34:02 GMT  
		Size: 2.0 MB (2017131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21d2db88668745770273c7b36d4d2c1e87a80b0118b8d775813860b467384c8`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd847159e169b898a67d4454fd5a22406c5ae623b16889d084a1d5f2d46a499`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:33ab737cb23dcde22de59a58e40f1f80d2c5e808ff3036519ae7d9db228fa37d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3562f7fd7806da24b1865c01a2246ac041b5e98d69c10ce6cbbe479f9408f9a1`

```dockerfile
```

-	Layers:
	-	`sha256:d5f43e64a79ee525bd0354a06e3284444fd642bbe6c1a782aa45ec2e20462f1d`  
		Last Modified: Thu, 18 Dec 2025 01:35:19 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bd2c024010f4f53d350bde9967c349efb3a58a2a812b14e17b29ddbd19eab87`  
		Last Modified: Thu, 18 Dec 2025 01:35:20 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine3.23`

```console
$ docker pull memcached@sha256:6f20032236ee1e3ae7edb0f8a060ce3d8c66cfad7a05fe84cfe88001f70a4eb1
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
$ docker pull memcached@sha256:9573a2399011fa86bb7b5d12bdab987d7931c98ddec0ef6802de7eb6d3c3e338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5956768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c79853acc5f24e9c28f15d45cef0aedc114e76bbacf7958eb6f555c22246e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:34 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:34 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:07 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:07 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:07 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c33ac8581cd04f31208409f36331e938a78e6ae3a7a3b530fe9dfebe6eb9ad`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583aae99135b9036c602a1c60743fc4fd519f261ac6d48ed60b01e1beb019e7f`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 106.0 KB (106050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ca22885c42a537f033850e8dff7eaeddbb7514902286739b48c084b55a8d6b`  
		Last Modified: Thu, 18 Dec 2025 00:32:19 GMT  
		Size: 2.0 MB (1989265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d146e2038834770bed57033a6c5d66ead5b731b8b133856dec6726ca21baee9`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c66e6c3acbe07806e3e96a97d97a2d4503713c4814d9b24a2f57f2c39200d05`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:cfdf2ea6bf2a04bb7ee1568efe0c8bd38a1f5e644250a9409479cce281891ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de792623281192b3965fdc95f31532c4d166e731f53e202be1e2a224c654633b`

```dockerfile
```

-	Layers:
	-	`sha256:87a0d23eeeda6353dfc603cc4ffee062e5383be07b611754f3a88db3fc644036`  
		Last Modified: Thu, 18 Dec 2025 01:34:48 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b73cd5efe31baa1fbf0eecea269426edcfc795cbb9b5dd74b523ff51b6f7c9f`  
		Last Modified: Thu, 18 Dec 2025 01:34:48 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; arm variant v6

```console
$ docker pull memcached@sha256:c1a12b64cc8b47f50ea4610d9c1c362da7157b3ba67deac8b4760e6b589cde75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5611647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3591f95cad049a0509bd23a95556f8f848452d2a5491ed00bae293897c7a6b2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:27:48 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:27:49 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:49:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:49:50 GMT
USER memcache
# Thu, 18 Dec 2025 00:49:50 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:49:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf585eb2bfa372c2097b9f7a5214ecb0941a30581b10fb74a26518fcc7addec`  
		Last Modified: Thu, 18 Dec 2025 00:50:01 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bb148ea8fbe93dd8097d85f9ee3cf547d314e669748b4239c05711b0d5f719`  
		Last Modified: Thu, 18 Dec 2025 00:50:02 GMT  
		Size: 102.7 KB (102652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6549359cda37ac41cf41a5ece5f37f1322a82f6b232f12e446c62840637093e`  
		Last Modified: Thu, 18 Dec 2025 00:50:02 GMT  
		Size: 1.9 MB (1939215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041e37eaffefcfb0809564ddea591be3cd818de5530e2c853c0bc9a2fa25c116`  
		Last Modified: Thu, 18 Dec 2025 00:50:05 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7907ae218c75b36c9a9002be8554131c271cde78b0280cb7a85029f99ad0bcdc`  
		Last Modified: Thu, 18 Dec 2025 00:50:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:a9c26fc290551b691574e093d3c28f4fe7b558b3f8173b3c99eb8a664c83a8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ca65d7156e6586d96310ea3162facd9849d5460d2939b461a25247b06a4d59`

```dockerfile
```

-	Layers:
	-	`sha256:d9c217dc241f1175812c47b6489d325a0574c0da554c6f8aa0b86a2d8aff05f9`  
		Last Modified: Thu, 18 Dec 2025 01:34:52 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; arm variant v7

```console
$ docker pull memcached@sha256:cee00a47bf7b8b5899a6cf1f5c692494df31b454f52b81f3c4886905a0c9bdd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91d78dbe118f2b7b0d6e850e1115de72c4fe3e30c55a5b53d8a844d14357d16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:56 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:30:57 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:33:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:33:51 GMT
USER memcache
# Thu, 18 Dec 2025 00:33:51 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:33:51 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa22c446792763e48f4680945ccc68d43c7906ef35a92e0b908f57ef53e72f0`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954155078f2265364295ebdf16fb114e991b1938d8a6951fb511163ab3b2b385`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 92.4 KB (92378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a25584b03ac5e45c66c3c616acfd9df1848e5db25219ef20feb2868c30c6332`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 1.9 MB (1897191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f237be962bb57c3f749904b5925c8e1d7e9013dfac7dd52cc9611ada81858e`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b07d9170b246a631c262d9f5d57f49278f7cd4805463b90b14aeca4dc61d93`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:64abe011fed6a9cf7b3290c752c50bffe81bb2e65cf6337e023efda87d49b451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b251b9c15ab7c5742bd3ab725df09f0ecb9f2491f92cf1c825bec598a31f4407`

```dockerfile
```

-	Layers:
	-	`sha256:1882c6d4361100a29fd5ab265587f65fa27b1df15e7f9349b30dac454facf98e`  
		Last Modified: Thu, 18 Dec 2025 01:34:55 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf0a88ab3838de6beab653497ab62a64cfb87b1dc83c5fa5b6f3907abfd88080`  
		Last Modified: Thu, 18 Dec 2025 01:34:56 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b6c3042e2bf09ec3d3f054d03b81313e8df717a49371ce916ff743e602796bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6285509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6691028570bbd843e6da26558c46162b8383212fcaaefcecb2d3f919e3401429`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:19 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:06 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:06 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb7b8445facedfc145b9478f74880f520776460f153005b7f437ec339aee530`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1853c901134389608b6e80aaa3e43cd67a35c71aecfdde4b5b7ed3b989a03c`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 121.9 KB (121860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a01d1ac5ce47f4494363e411e1cd25dea26438213a2d18d6bb104d0974d9a52`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 2.0 MB (1966561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115624f24ba74d393c2da3d65ed5b35a7afb3fa9ad143d3fb82c64953b3d0401`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87bba524314294ca97195ce65a35ec6d42d3f9f18c9cc0c05c064c9a3cf85c0`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:2feda8921a7d67cd9f2f3d7186ed69ceb0d3c22af7a20bd230664e9bcf39096c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73c6548a24cc8ce7782d03377e89a4b4b0e4c2a48cd3a03a79193320fc4d834`

```dockerfile
```

-	Layers:
	-	`sha256:984e438122735983bf56bc3d638fb1b0baf8cfb26ce26f71e0a9b847d25f76b5`  
		Last Modified: Thu, 18 Dec 2025 01:34:59 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d6e8d91ca57b45f0050ec3833a8f09a7ce62f7ba9ec70e1ae12881ad4b2bb6f`  
		Last Modified: Thu, 18 Dec 2025 01:35:00 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; 386

```console
$ docker pull memcached@sha256:df1ba8af73cd6e3f8227557b097cd6b128ec0d410a3bbe7a2c282089c5641b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5740953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78dbfc1f8ea65ad6466795e278180963d4afe98dfbca4a4497bc73c99f07ed4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:43 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:44 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:29 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:29 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37ec5bf455c1d98d22e6f3dacb5b971dac8ea96d1fe9b9177a07c5277530646`  
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b2862af05c1582c8625c82ea0863dc2b6474e410d3e6a32876c920e0152c73`  
		Last Modified: Thu, 18 Dec 2025 00:32:42 GMT  
		Size: 110.7 KB (110740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30872a43f6c591fd9b979b49b0fb32107b4bfa8c1155657fa255aa199cf0b83b`  
		Last Modified: Thu, 18 Dec 2025 00:32:42 GMT  
		Size: 1.9 MB (1942762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a62c11b4aeceaba2e5e73a1bc29aa8b4fc42ccd0c7e8512cc11b96e48aef2f`  
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f553d362a11992264bf5364cfe13d248403c5baf2ecac784c26f444dbfb90388`  
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:e3b020c2afd9ae372e234c6ab67456908861fd24200448fd3cf741503a8a6f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abfcddfb1575f6cc07e51c6a379141589de7ea8c329a9bc5c1592f3186e6fda`

```dockerfile
```

-	Layers:
	-	`sha256:ff9be8ef1bab92275eb15ae5fd6a05e767abc1fe855455766200b3c0a1866e33`  
		Last Modified: Thu, 18 Dec 2025 01:35:03 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d7026bdf84e278b6976f0ccab2297ddc0284cf329414f56d12608dbc2acb940`  
		Last Modified: Thu, 18 Dec 2025 01:35:04 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; ppc64le

```console
$ docker pull memcached@sha256:7292c7b145e08f87f78644bf2c3355fad1d0b4d9366f173ffa0634c3ec93addf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6031729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae72ba97ecea986f01bda1eb392aee1ded4b5a86b2edcabe92a2034143e155b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:33:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:33:42 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:36:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:36:14 GMT
USER memcache
# Thu, 18 Dec 2025 00:36:14 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:36:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c95450233dfe3e06529eb39ca4b46e6ad51ccf338cab64157669ff1fc0a8d72`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4079a2d61bafcf146b8f57b35f0e39bf2548e0963be10cff5086f9a56ccdd9d`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 126.3 KB (126257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f69efa1066815d67cf415d0aac5dcd305032257b6bded5a4c57a7444a1e7fd4`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 2.1 MB (2076363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357f4165f53a3d4c66ef270bcb5b5283a066af50f79924cccc7c73f6a4f6f4ab`  
		Last Modified: Thu, 18 Dec 2025 00:36:36 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a65ff5cefcbfc874c1cac0857339eaee0b07147dd26b6bfa18c00921b4f30c`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:1d06281345f2ac44a607d40d5e87de6abb99bbc6ee82d319e73f3794602d0282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4867a5aa08041c7e5ec69dfc84214226a7323d1ce703747ae2117675e2f74bcd`

```dockerfile
```

-	Layers:
	-	`sha256:282960f007d3f1f008333191d98a2ded5ff0f83075ace30043349b6c082c18fd`  
		Last Modified: Thu, 18 Dec 2025 01:35:08 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4755fffd5924e8405adfbed0f328ad9792eff20e2b8ad2025e1f5c85bca88618`  
		Last Modified: Thu, 18 Dec 2025 01:35:09 GMT  
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
$ docker pull memcached@sha256:e011484878fd5d1e2da6de478ac11d01ae80f0bdef1902dcde3ed53728803741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5857090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689ea71c305b80e206c68a215481290a1378e6375e32ad059455f7d041396aa6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:26 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:30:27 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:33:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:33:46 GMT
USER memcache
# Thu, 18 Dec 2025 00:33:46 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:33:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4594a6826f7ed03c8c4f9f2aebb9716eb6e16d5b5ab7e1bc247783b503c5b10`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f270744f8d8b82bc6657387109b33836a76d6dbf8faa645a997db7ea290cdb`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 114.3 KB (114299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91f8ee8f36703944a7bdcaf57cc5772fe9f79c74a088c33fa1b6da7de119f93`  
		Last Modified: Thu, 18 Dec 2025 00:34:02 GMT  
		Size: 2.0 MB (2017131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21d2db88668745770273c7b36d4d2c1e87a80b0118b8d775813860b467384c8`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd847159e169b898a67d4454fd5a22406c5ae623b16889d084a1d5f2d46a499`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:33ab737cb23dcde22de59a58e40f1f80d2c5e808ff3036519ae7d9db228fa37d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3562f7fd7806da24b1865c01a2246ac041b5e98d69c10ce6cbbe479f9408f9a1`

```dockerfile
```

-	Layers:
	-	`sha256:d5f43e64a79ee525bd0354a06e3284444fd642bbe6c1a782aa45ec2e20462f1d`  
		Last Modified: Thu, 18 Dec 2025 01:35:19 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bd2c024010f4f53d350bde9967c349efb3a58a2a812b14e17b29ddbd19eab87`  
		Last Modified: Thu, 18 Dec 2025 01:35:20 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-trixie`

```console
$ docker pull memcached@sha256:9ae868852d0bc0974e4dd39c58436f73698081a31e61b8099871983e09d79f80
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
$ docker pull memcached@sha256:c9046d2a0ade04c91892254044294c2a529006458cd7b98bdc31b4054fffbfe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32193341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6654931990345ba058b2f50cedc8d03dfcc174d6809b0e7a820c12f7b93dc09d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:35:37 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:23 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:23 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:23 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:23 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:23 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b6bc7772cb8044287682c4af75ca1c8280c4837d5ffee58adc014018f02e91`  
		Last Modified: Wed, 17 Dec 2025 21:38:42 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3af321fdb36bbbb634d6be4a6e457f7eeb47b153460c7bab6c9eae91724b08b`  
		Last Modified: Wed, 17 Dec 2025 21:38:42 GMT  
		Size: 136.7 KB (136691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a00f7c8e317ad005bdf0117005dd753e347a8674b068c660bbc29b3f93a0621`  
		Last Modified: Wed, 17 Dec 2025 21:38:42 GMT  
		Size: 2.3 MB (2278641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb739034830ce246e4bc00aa883c7d2af8a1fd59bc3e2ea17cae3607bf281074`  
		Last Modified: Wed, 17 Dec 2025 21:38:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33cfbae525009776fcee65339602ed1b2a8a5f2c51898ec9fc499fe35c60b87`  
		Last Modified: Wed, 17 Dec 2025 21:38:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:e726a4ddf8221754a6a9fa1143cee47f51785aedb20dc0329a7c7b41b4772763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd3f16921a7fcccc9bc6ee3685e192e34a0b621f1c95362d6cea5e4293e54d33`

```dockerfile
```

-	Layers:
	-	`sha256:3a55af39eac38dca280008ae509d726055b1dde6e05ce9024174d0a0bd0565c2`  
		Last Modified: Wed, 17 Dec 2025 22:34:37 GMT  
		Size: 2.0 MB (2008228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef418f126bca0d267c3b365faed9990a104832e94e7ec35841aff2c2b26510dc`  
		Last Modified: Wed, 17 Dec 2025 22:34:38 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:c1a14cf6b3aa6f9ee13feee1c176a4ff104ec3d361f2df684e87a9d88a563eaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30300251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7375c421f8c059114c1a5cdc58215c8cf41dcc23355cbef325fdfa4b290df1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:39:00 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:39:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:42:24 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:42:24 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:42:24 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:42:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:42:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:42:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:42:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:42:24 GMT
USER memcache
# Wed, 17 Dec 2025 21:42:24 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:42:24 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d97bc71d0fa535127863fdab265dfddb07b3cda35b80de4dd2b9b67fe154c856`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 27.9 MB (27944187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e168dbb57c754690bc257f600efb5085929be35091c7e3d6926d35490c3391`  
		Last Modified: Wed, 17 Dec 2025 21:42:38 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78870a4506eecc7b424a3cedde90baa4c44a7c5d1174e6842b60c11b08a7984e`  
		Last Modified: Wed, 17 Dec 2025 21:42:40 GMT  
		Size: 144.2 KB (144157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e35d5393bf24a4f7ba0c87d734e7fda2d09414dec61e9139726200bed52e262`  
		Last Modified: Wed, 17 Dec 2025 21:42:39 GMT  
		Size: 2.2 MB (2210395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72c9d61ca04e663f67ab23ad2c50afcd810d29c2f52728277947d5ab78c03da`  
		Last Modified: Wed, 17 Dec 2025 21:42:38 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e89f91fff1d699acc4ebbc8ebb2a409d5f7867914100e87affef7b7d8775488`  
		Last Modified: Wed, 17 Dec 2025 21:42:38 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:3a82f6da1fa8b6c43220785849304c0e09363556371c8f763abae2126e271c5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e59d44e1c5460c7338a49dad6ec9d6d03db5b9330bb235c1d01e3e182df704ca`

```dockerfile
```

-	Layers:
	-	`sha256:2b38edaa9de8bf0d9055274c5ca1c0af276da0f57396ee1edfb8db1002dc8834`  
		Last Modified: Wed, 17 Dec 2025 22:34:42 GMT  
		Size: 2.0 MB (2011231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c70377fb854a2602cbb12ee80dd69f8a5deb00e23feb0c3c24e1b27806029b0d`  
		Last Modified: Wed, 17 Dec 2025 22:34:43 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:b7ad53cb1e5a5631cc9b08d0fe984b0ba6bb7ab77da4309a552dbb97bd4ae04e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28510860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b2fbe25ebf8c8035604591c6ded5acfffe219c97c853c1c0e00421ac18abcd4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:35:20 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:30 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:30 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:30 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:30 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:30 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:30 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d46de1cc714aa644c02bc1b184e957b7330bf3473d4e97f72f454fdc8a432d`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0327c8719a60b04c8b690d8d0a0a122cdbc620f2aab391fd43789a8803b62bf1`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 135.4 KB (135362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd55327cbd82c4adf176e679bae5436e8aaf27c54595ec2cd7cfec20989b1fc`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 2.2 MB (2163972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37babf40b7b24af06cfbfc9fe6daf7d6f5863de148318182eecf29e242ba5e4c`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3daf0d6e9f1032a9bce2c34a57a6049ec4ffd4a412a20724540653fe7b6526d3`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:77b0259560abd3025ae0593b06db95eb3c4dd6dccbd2332f85286fae97d799bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd1267e1c8eb093b3e5a265d3c2d0c9b2b3784e50b6aa7edfec29ba838d4a8c`

```dockerfile
```

-	Layers:
	-	`sha256:3266292cf75a57aab22a4e279bf40458841e617570f3ee192bb26dc1d2d6e1ef`  
		Last Modified: Wed, 17 Dec 2025 22:34:47 GMT  
		Size: 2.0 MB (2009688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cc2be86d85bc478731bb7718f18d50da352f58c942412f66ca371226633d3bb`  
		Last Modified: Wed, 17 Dec 2025 22:34:48 GMT  
		Size: 22.3 KB (22303 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:230a135d43b1bf876ec5c160b78cb4f0303d1e6e98dc76a31dd524d28a4a5279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32554912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79214d48c3616d6c032db23eb36a6766c7a96a8d4619d8f8791d2fa43163cc34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:35:24 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:26 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:26 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:26 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:26 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:26 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:26 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f49eb557c72f2fe7e0eb1949c1587e8e4c86bdae514d70fac3ff429290a149`  
		Last Modified: Wed, 17 Dec 2025 21:38:46 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f764f8f3ed63ac8e640ebdcb2f5ea0371b6fb244a1f6defbe51ddfff908a34a`  
		Last Modified: Wed, 17 Dec 2025 21:38:46 GMT  
		Size: 153.5 KB (153477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9353d672d9aeb0b8a3ee269d120b0b920e9f6b81998ed7ef7765092573e4b716`  
		Last Modified: Wed, 17 Dec 2025 21:38:46 GMT  
		Size: 2.3 MB (2261292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ba4d16dc49a02e1490d18a58f5e108ec18a248f9ea83bb7b4deb8642b36f90`  
		Last Modified: Wed, 17 Dec 2025 21:38:46 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d15340fcbda1a05a50ba392408ace29b5cbb21b398bb1018750621349d3b0a`  
		Last Modified: Wed, 17 Dec 2025 21:38:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:d2a465ef21f85d63f634e52f05c50319a05c013d1aeed6321cc146b3a28a5920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c092dec716fd21afebb19ce5e88ba467a0f4bb88a40068e3e266b1f10ff6652`

```dockerfile
```

-	Layers:
	-	`sha256:b7bd1c3aaf184ba5d6dfbf328c24c2f39511de9c6e21c04b7fa212d6a26b0049`  
		Last Modified: Wed, 17 Dec 2025 22:34:53 GMT  
		Size: 2.0 MB (2008544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc6165d17a79a40bba13d288c74c5c34aa4af72304a300a74ceededf1a934bbc`  
		Last Modified: Wed, 17 Dec 2025 22:34:54 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; 386

```console
$ docker pull memcached@sha256:35df20cb1713a9d5fbb1820acac102f3c3560dfa2d0fa147fff30dfc53f209bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33665704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ccada050045e330c6b125cae2adfcf8e5edb8e23b5e044c0d53861f7762294a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:35:51 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:43 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:43 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:43 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:43 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:43 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b054f6842adaecae2d5cf75c99601b690566759a58606bc981ccae49baaae51`  
		Last Modified: Wed, 17 Dec 2025 21:38:57 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43efb4f909536827644b2ca98420204710b14f6195238a8ffdbf658c29883be`  
		Last Modified: Wed, 17 Dec 2025 21:38:57 GMT  
		Size: 147.5 KB (147519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:792eb292285447291b91c55e07bc1a75b3d4e125a3c23f80671848c5f967e042`  
		Last Modified: Wed, 17 Dec 2025 21:38:57 GMT  
		Size: 2.2 MB (2223600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe79378953d034686129f0d36718bb867ebebf130cd1f431ad68cf117a1308c6`  
		Last Modified: Wed, 17 Dec 2025 21:38:57 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92088f114f464c2f2e1217404e900d24a46a03305faa6cae793f0b873cadba52`  
		Last Modified: Wed, 17 Dec 2025 21:38:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:3a428e326360172543ee458a46a55c1b9e70d3eeeea945f2ed65839c307eddd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a62b1d6c9ce3819b6b67f9de9cc436a2f4cb362fad3a8c07627fd790e4bd8be7`

```dockerfile
```

-	Layers:
	-	`sha256:0f8e75010a0e7df5356c9c36b97dff2c5d2191f6f6e643619b4363f8c1e1dc42`  
		Last Modified: Wed, 17 Dec 2025 22:34:58 GMT  
		Size: 2.0 MB (2005385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98883c6827ebd9ca960545767f09a2be89e7580fc425e24f86364f3a9e4ea283`  
		Last Modified: Wed, 17 Dec 2025 22:34:59 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:38a236f83eb206f786b39c53e8f756815f0bda1460157b11844faf21735208bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36162589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41292f5c75fe5f3a464b809bde41e0ae8849ad8d7046918a548d0c6b2e250a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:34:54 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:28 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:28 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:28 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2b42546c7b688160cfd1a0da61a24922a019b4ebead88e23aff01482ddd477`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4efe9fd2e012174cd86a64f83d7b7facfe14ee67c9c9fa5ce994f22c24173f2c`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 170.4 KB (170393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9752985ba696f0f8d5831ac91e19bfe336342b1c403542641c575b1dc6116e`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 2.4 MB (2393786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d11c68ba0bc913d139eea51cb2957c1ddd713515fc06dfa5d4c398b119535a`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9186b8b7184cef442ae3ed6a3feadcaa8f4ccc974ed5ae6c6cf8efe37e679f23`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:00d1019e9978171df76f638253f212405bf7d53251607ef5a5933d5b28d867b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588d3d6ab54a9ea5c8baf9b013bb23c12826989ba0d09cb862431e2fa30e5189`

```dockerfile
```

-	Layers:
	-	`sha256:799ad025578a6d5d0155dc5be223bfbc25ffa3aa0548e4fb2e4bedeb0a5088d9`  
		Last Modified: Wed, 17 Dec 2025 22:35:03 GMT  
		Size: 2.0 MB (2011829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaa03114ccb63fbbd8ca04eef46baa26c8a0508f1256aa45d851f3a49f2ed47a`  
		Last Modified: Wed, 17 Dec 2025 22:35:04 GMT  
		Size: 22.2 KB (22225 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:5aedcd2b04ff2d8dc77fb6568e6ce96878f75508a3a01326623b60869874f8a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30615184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab5d9dd83f52434969fb6da016bd60451fd5d989e33e2cd491533dcb4553c835`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 05:30:55 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 09 Dec 2025 05:31:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Dec 2025 03:19:32 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 03:19:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 03:19:32 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 03:19:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 18 Dec 2025 03:19:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 03:19:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 03:19:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 03:19:33 GMT
USER memcache
# Thu, 18 Dec 2025 03:19:33 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 03:19:33 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb23364b88c4686dab6a11bf004aac89beea8adb8559fd39799a54dc729c23a6`  
		Last Modified: Tue, 09 Dec 2025 05:57:38 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edeeae49e27528d2079d0d5aeb702d7dd56503463fa4054ee2444f847f399650`  
		Last Modified: Tue, 09 Dec 2025 05:57:38 GMT  
		Size: 133.1 KB (133076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e584b688c99191b71a2471afe63daff415a1eedcf541b959dfcdf248eebd8577`  
		Last Modified: Thu, 18 Dec 2025 03:20:28 GMT  
		Size: 2.2 MB (2207438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b780b2b80274922cc63f0afe1ecd2680bcafae3234732fd03ba740690e3ebf1`  
		Last Modified: Thu, 18 Dec 2025 03:20:28 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5449346fa21339be4109a2e289721bfa7b0e8203b88fe202956ebb257c703a88`  
		Last Modified: Thu, 18 Dec 2025 03:20:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:bbe7bbb4c3590b1fc9c5943719d3b1b2a21670d2874ed90415040aeae5b13200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c721ad9798565707f4e9e537a1618b5efafce47c49577053fe7b40879caca9`

```dockerfile
```

-	Layers:
	-	`sha256:37125be6342f13dcb1fff2b0c3def6d6f3b808e19192f9ff68a139ce2d1d3083`  
		Last Modified: Thu, 18 Dec 2025 04:34:34 GMT  
		Size: 2.0 MB (2002192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06edc085828555adcb8aac4ef4e564c72d260338e77dde6abe811eefcdd8682d`  
		Last Modified: Thu, 18 Dec 2025 04:34:35 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:1e7fc2740e66d7d7b21982f73ae72e901616fcb9ebc6176c6f1d931c6a4732b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32273737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f632195b7b4a10526fcb27d2d66a479b07455d784656340bcbae2d31e292aa2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:34:51 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:34:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:04 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:04 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:04 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:04 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:04 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:04 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9606e3e114197b678b6fbd5b889ab574d2ad4cd8b4010407f847a98309f0f6b`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24f23dd2596713c0a8daf1cde9aabc7d26e7e9b832300ba1ce4615e8c806afc`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 140.5 KB (140507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0dd33ff71e256560cf1693538e8ecc4f92550f6483c1478697b822abf8d0f84`  
		Last Modified: Wed, 17 Dec 2025 21:38:19 GMT  
		Size: 2.3 MB (2297315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568ee6e9ecd99ef323ff6ff6b40b5fcf91b13472f56ac46f8b3036c82c705fd6`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91a63e3e27d493e5ad7b64edf0b8ae2bb8ade89a55bfc197b4dc9a393ceec4b`  
		Last Modified: Wed, 17 Dec 2025 21:38:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:d9aa5142dc8acd96ae2fb7235ceda06498adc21053e1bc5bf02ff76701213426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e87c93018f4f94a4286dcf6f6d33373729ef4263208b2f346e92a2028839a2`

```dockerfile
```

-	Layers:
	-	`sha256:c0ee3f2287a538730e473aea557f8fc2a48d18bb9e778e65ccdbf8918310ace3`  
		Last Modified: Wed, 17 Dec 2025 22:35:11 GMT  
		Size: 2.0 MB (2009665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce86917337210887b4362390f278a89c9fc6d6d1cc50e29ebf7f716bc556c877`  
		Last Modified: Wed, 17 Dec 2025 22:35:12 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6`

```console
$ docker pull memcached@sha256:9ae868852d0bc0974e4dd39c58436f73698081a31e61b8099871983e09d79f80
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
$ docker pull memcached@sha256:c9046d2a0ade04c91892254044294c2a529006458cd7b98bdc31b4054fffbfe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32193341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6654931990345ba058b2f50cedc8d03dfcc174d6809b0e7a820c12f7b93dc09d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:35:37 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:23 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:23 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:23 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:23 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:23 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b6bc7772cb8044287682c4af75ca1c8280c4837d5ffee58adc014018f02e91`  
		Last Modified: Wed, 17 Dec 2025 21:38:42 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3af321fdb36bbbb634d6be4a6e457f7eeb47b153460c7bab6c9eae91724b08b`  
		Last Modified: Wed, 17 Dec 2025 21:38:42 GMT  
		Size: 136.7 KB (136691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a00f7c8e317ad005bdf0117005dd753e347a8674b068c660bbc29b3f93a0621`  
		Last Modified: Wed, 17 Dec 2025 21:38:42 GMT  
		Size: 2.3 MB (2278641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb739034830ce246e4bc00aa883c7d2af8a1fd59bc3e2ea17cae3607bf281074`  
		Last Modified: Wed, 17 Dec 2025 21:38:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33cfbae525009776fcee65339602ed1b2a8a5f2c51898ec9fc499fe35c60b87`  
		Last Modified: Wed, 17 Dec 2025 21:38:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:e726a4ddf8221754a6a9fa1143cee47f51785aedb20dc0329a7c7b41b4772763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd3f16921a7fcccc9bc6ee3685e192e34a0b621f1c95362d6cea5e4293e54d33`

```dockerfile
```

-	Layers:
	-	`sha256:3a55af39eac38dca280008ae509d726055b1dde6e05ce9024174d0a0bd0565c2`  
		Last Modified: Wed, 17 Dec 2025 22:34:37 GMT  
		Size: 2.0 MB (2008228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef418f126bca0d267c3b365faed9990a104832e94e7ec35841aff2c2b26510dc`  
		Last Modified: Wed, 17 Dec 2025 22:34:38 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:c1a14cf6b3aa6f9ee13feee1c176a4ff104ec3d361f2df684e87a9d88a563eaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30300251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7375c421f8c059114c1a5cdc58215c8cf41dcc23355cbef325fdfa4b290df1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:39:00 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:39:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:42:24 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:42:24 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:42:24 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:42:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:42:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:42:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:42:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:42:24 GMT
USER memcache
# Wed, 17 Dec 2025 21:42:24 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:42:24 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d97bc71d0fa535127863fdab265dfddb07b3cda35b80de4dd2b9b67fe154c856`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 27.9 MB (27944187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e168dbb57c754690bc257f600efb5085929be35091c7e3d6926d35490c3391`  
		Last Modified: Wed, 17 Dec 2025 21:42:38 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78870a4506eecc7b424a3cedde90baa4c44a7c5d1174e6842b60c11b08a7984e`  
		Last Modified: Wed, 17 Dec 2025 21:42:40 GMT  
		Size: 144.2 KB (144157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e35d5393bf24a4f7ba0c87d734e7fda2d09414dec61e9139726200bed52e262`  
		Last Modified: Wed, 17 Dec 2025 21:42:39 GMT  
		Size: 2.2 MB (2210395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72c9d61ca04e663f67ab23ad2c50afcd810d29c2f52728277947d5ab78c03da`  
		Last Modified: Wed, 17 Dec 2025 21:42:38 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e89f91fff1d699acc4ebbc8ebb2a409d5f7867914100e87affef7b7d8775488`  
		Last Modified: Wed, 17 Dec 2025 21:42:38 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:3a82f6da1fa8b6c43220785849304c0e09363556371c8f763abae2126e271c5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e59d44e1c5460c7338a49dad6ec9d6d03db5b9330bb235c1d01e3e182df704ca`

```dockerfile
```

-	Layers:
	-	`sha256:2b38edaa9de8bf0d9055274c5ca1c0af276da0f57396ee1edfb8db1002dc8834`  
		Last Modified: Wed, 17 Dec 2025 22:34:42 GMT  
		Size: 2.0 MB (2011231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c70377fb854a2602cbb12ee80dd69f8a5deb00e23feb0c3c24e1b27806029b0d`  
		Last Modified: Wed, 17 Dec 2025 22:34:43 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v7

```console
$ docker pull memcached@sha256:b7ad53cb1e5a5631cc9b08d0fe984b0ba6bb7ab77da4309a552dbb97bd4ae04e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28510860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b2fbe25ebf8c8035604591c6ded5acfffe219c97c853c1c0e00421ac18abcd4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:35:20 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:30 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:30 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:30 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:30 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:30 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:30 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d46de1cc714aa644c02bc1b184e957b7330bf3473d4e97f72f454fdc8a432d`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0327c8719a60b04c8b690d8d0a0a122cdbc620f2aab391fd43789a8803b62bf1`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 135.4 KB (135362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd55327cbd82c4adf176e679bae5436e8aaf27c54595ec2cd7cfec20989b1fc`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 2.2 MB (2163972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37babf40b7b24af06cfbfc9fe6daf7d6f5863de148318182eecf29e242ba5e4c`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3daf0d6e9f1032a9bce2c34a57a6049ec4ffd4a412a20724540653fe7b6526d3`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:77b0259560abd3025ae0593b06db95eb3c4dd6dccbd2332f85286fae97d799bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd1267e1c8eb093b3e5a265d3c2d0c9b2b3784e50b6aa7edfec29ba838d4a8c`

```dockerfile
```

-	Layers:
	-	`sha256:3266292cf75a57aab22a4e279bf40458841e617570f3ee192bb26dc1d2d6e1ef`  
		Last Modified: Wed, 17 Dec 2025 22:34:47 GMT  
		Size: 2.0 MB (2009688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cc2be86d85bc478731bb7718f18d50da352f58c942412f66ca371226633d3bb`  
		Last Modified: Wed, 17 Dec 2025 22:34:48 GMT  
		Size: 22.3 KB (22303 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:230a135d43b1bf876ec5c160b78cb4f0303d1e6e98dc76a31dd524d28a4a5279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32554912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79214d48c3616d6c032db23eb36a6766c7a96a8d4619d8f8791d2fa43163cc34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:35:24 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:26 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:26 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:26 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:26 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:26 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:26 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f49eb557c72f2fe7e0eb1949c1587e8e4c86bdae514d70fac3ff429290a149`  
		Last Modified: Wed, 17 Dec 2025 21:38:46 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f764f8f3ed63ac8e640ebdcb2f5ea0371b6fb244a1f6defbe51ddfff908a34a`  
		Last Modified: Wed, 17 Dec 2025 21:38:46 GMT  
		Size: 153.5 KB (153477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9353d672d9aeb0b8a3ee269d120b0b920e9f6b81998ed7ef7765092573e4b716`  
		Last Modified: Wed, 17 Dec 2025 21:38:46 GMT  
		Size: 2.3 MB (2261292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ba4d16dc49a02e1490d18a58f5e108ec18a248f9ea83bb7b4deb8642b36f90`  
		Last Modified: Wed, 17 Dec 2025 21:38:46 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d15340fcbda1a05a50ba392408ace29b5cbb21b398bb1018750621349d3b0a`  
		Last Modified: Wed, 17 Dec 2025 21:38:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:d2a465ef21f85d63f634e52f05c50319a05c013d1aeed6321cc146b3a28a5920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c092dec716fd21afebb19ce5e88ba467a0f4bb88a40068e3e266b1f10ff6652`

```dockerfile
```

-	Layers:
	-	`sha256:b7bd1c3aaf184ba5d6dfbf328c24c2f39511de9c6e21c04b7fa212d6a26b0049`  
		Last Modified: Wed, 17 Dec 2025 22:34:53 GMT  
		Size: 2.0 MB (2008544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc6165d17a79a40bba13d288c74c5c34aa4af72304a300a74ceededf1a934bbc`  
		Last Modified: Wed, 17 Dec 2025 22:34:54 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; 386

```console
$ docker pull memcached@sha256:35df20cb1713a9d5fbb1820acac102f3c3560dfa2d0fa147fff30dfc53f209bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33665704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ccada050045e330c6b125cae2adfcf8e5edb8e23b5e044c0d53861f7762294a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:35:51 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:43 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:43 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:43 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:43 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:43 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b054f6842adaecae2d5cf75c99601b690566759a58606bc981ccae49baaae51`  
		Last Modified: Wed, 17 Dec 2025 21:38:57 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43efb4f909536827644b2ca98420204710b14f6195238a8ffdbf658c29883be`  
		Last Modified: Wed, 17 Dec 2025 21:38:57 GMT  
		Size: 147.5 KB (147519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:792eb292285447291b91c55e07bc1a75b3d4e125a3c23f80671848c5f967e042`  
		Last Modified: Wed, 17 Dec 2025 21:38:57 GMT  
		Size: 2.2 MB (2223600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe79378953d034686129f0d36718bb867ebebf130cd1f431ad68cf117a1308c6`  
		Last Modified: Wed, 17 Dec 2025 21:38:57 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92088f114f464c2f2e1217404e900d24a46a03305faa6cae793f0b873cadba52`  
		Last Modified: Wed, 17 Dec 2025 21:38:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:3a428e326360172543ee458a46a55c1b9e70d3eeeea945f2ed65839c307eddd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a62b1d6c9ce3819b6b67f9de9cc436a2f4cb362fad3a8c07627fd790e4bd8be7`

```dockerfile
```

-	Layers:
	-	`sha256:0f8e75010a0e7df5356c9c36b97dff2c5d2191f6f6e643619b4363f8c1e1dc42`  
		Last Modified: Wed, 17 Dec 2025 22:34:58 GMT  
		Size: 2.0 MB (2005385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98883c6827ebd9ca960545767f09a2be89e7580fc425e24f86364f3a9e4ea283`  
		Last Modified: Wed, 17 Dec 2025 22:34:59 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:38a236f83eb206f786b39c53e8f756815f0bda1460157b11844faf21735208bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36162589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41292f5c75fe5f3a464b809bde41e0ae8849ad8d7046918a548d0c6b2e250a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:34:54 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:28 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:28 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:28 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2b42546c7b688160cfd1a0da61a24922a019b4ebead88e23aff01482ddd477`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4efe9fd2e012174cd86a64f83d7b7facfe14ee67c9c9fa5ce994f22c24173f2c`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 170.4 KB (170393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9752985ba696f0f8d5831ac91e19bfe336342b1c403542641c575b1dc6116e`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 2.4 MB (2393786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d11c68ba0bc913d139eea51cb2957c1ddd713515fc06dfa5d4c398b119535a`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9186b8b7184cef442ae3ed6a3feadcaa8f4ccc974ed5ae6c6cf8efe37e679f23`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:00d1019e9978171df76f638253f212405bf7d53251607ef5a5933d5b28d867b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588d3d6ab54a9ea5c8baf9b013bb23c12826989ba0d09cb862431e2fa30e5189`

```dockerfile
```

-	Layers:
	-	`sha256:799ad025578a6d5d0155dc5be223bfbc25ffa3aa0548e4fb2e4bedeb0a5088d9`  
		Last Modified: Wed, 17 Dec 2025 22:35:03 GMT  
		Size: 2.0 MB (2011829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaa03114ccb63fbbd8ca04eef46baa26c8a0508f1256aa45d851f3a49f2ed47a`  
		Last Modified: Wed, 17 Dec 2025 22:35:04 GMT  
		Size: 22.2 KB (22225 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; riscv64

```console
$ docker pull memcached@sha256:5aedcd2b04ff2d8dc77fb6568e6ce96878f75508a3a01326623b60869874f8a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30615184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab5d9dd83f52434969fb6da016bd60451fd5d989e33e2cd491533dcb4553c835`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 05:30:55 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 09 Dec 2025 05:31:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Dec 2025 03:19:32 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 03:19:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 03:19:32 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 03:19:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 18 Dec 2025 03:19:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 03:19:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 03:19:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 03:19:33 GMT
USER memcache
# Thu, 18 Dec 2025 03:19:33 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 03:19:33 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb23364b88c4686dab6a11bf004aac89beea8adb8559fd39799a54dc729c23a6`  
		Last Modified: Tue, 09 Dec 2025 05:57:38 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edeeae49e27528d2079d0d5aeb702d7dd56503463fa4054ee2444f847f399650`  
		Last Modified: Tue, 09 Dec 2025 05:57:38 GMT  
		Size: 133.1 KB (133076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e584b688c99191b71a2471afe63daff415a1eedcf541b959dfcdf248eebd8577`  
		Last Modified: Thu, 18 Dec 2025 03:20:28 GMT  
		Size: 2.2 MB (2207438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b780b2b80274922cc63f0afe1ecd2680bcafae3234732fd03ba740690e3ebf1`  
		Last Modified: Thu, 18 Dec 2025 03:20:28 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5449346fa21339be4109a2e289721bfa7b0e8203b88fe202956ebb257c703a88`  
		Last Modified: Thu, 18 Dec 2025 03:20:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:bbe7bbb4c3590b1fc9c5943719d3b1b2a21670d2874ed90415040aeae5b13200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c721ad9798565707f4e9e537a1618b5efafce47c49577053fe7b40879caca9`

```dockerfile
```

-	Layers:
	-	`sha256:37125be6342f13dcb1fff2b0c3def6d6f3b808e19192f9ff68a139ce2d1d3083`  
		Last Modified: Thu, 18 Dec 2025 04:34:34 GMT  
		Size: 2.0 MB (2002192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06edc085828555adcb8aac4ef4e564c72d260338e77dde6abe811eefcdd8682d`  
		Last Modified: Thu, 18 Dec 2025 04:34:35 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; s390x

```console
$ docker pull memcached@sha256:1e7fc2740e66d7d7b21982f73ae72e901616fcb9ebc6176c6f1d931c6a4732b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32273737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f632195b7b4a10526fcb27d2d66a479b07455d784656340bcbae2d31e292aa2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:34:51 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:34:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:04 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:04 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:04 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:04 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:04 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:04 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9606e3e114197b678b6fbd5b889ab574d2ad4cd8b4010407f847a98309f0f6b`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24f23dd2596713c0a8daf1cde9aabc7d26e7e9b832300ba1ce4615e8c806afc`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 140.5 KB (140507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0dd33ff71e256560cf1693538e8ecc4f92550f6483c1478697b822abf8d0f84`  
		Last Modified: Wed, 17 Dec 2025 21:38:19 GMT  
		Size: 2.3 MB (2297315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568ee6e9ecd99ef323ff6ff6b40b5fcf91b13472f56ac46f8b3036c82c705fd6`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91a63e3e27d493e5ad7b64edf0b8ae2bb8ade89a55bfc197b4dc9a393ceec4b`  
		Last Modified: Wed, 17 Dec 2025 21:38:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:d9aa5142dc8acd96ae2fb7235ceda06498adc21053e1bc5bf02ff76701213426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e87c93018f4f94a4286dcf6f6d33373729ef4263208b2f346e92a2028839a2`

```dockerfile
```

-	Layers:
	-	`sha256:c0ee3f2287a538730e473aea557f8fc2a48d18bb9e778e65ccdbf8918310ace3`  
		Last Modified: Wed, 17 Dec 2025 22:35:11 GMT  
		Size: 2.0 MB (2009665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce86917337210887b4362390f278a89c9fc6d6d1cc50e29ebf7f716bc556c877`  
		Last Modified: Wed, 17 Dec 2025 22:35:12 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine`

```console
$ docker pull memcached@sha256:6f20032236ee1e3ae7edb0f8a060ce3d8c66cfad7a05fe84cfe88001f70a4eb1
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
$ docker pull memcached@sha256:9573a2399011fa86bb7b5d12bdab987d7931c98ddec0ef6802de7eb6d3c3e338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5956768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c79853acc5f24e9c28f15d45cef0aedc114e76bbacf7958eb6f555c22246e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:34 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:34 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:07 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:07 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:07 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c33ac8581cd04f31208409f36331e938a78e6ae3a7a3b530fe9dfebe6eb9ad`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583aae99135b9036c602a1c60743fc4fd519f261ac6d48ed60b01e1beb019e7f`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 106.0 KB (106050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ca22885c42a537f033850e8dff7eaeddbb7514902286739b48c084b55a8d6b`  
		Last Modified: Thu, 18 Dec 2025 00:32:19 GMT  
		Size: 2.0 MB (1989265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d146e2038834770bed57033a6c5d66ead5b731b8b133856dec6726ca21baee9`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c66e6c3acbe07806e3e96a97d97a2d4503713c4814d9b24a2f57f2c39200d05`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:cfdf2ea6bf2a04bb7ee1568efe0c8bd38a1f5e644250a9409479cce281891ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de792623281192b3965fdc95f31532c4d166e731f53e202be1e2a224c654633b`

```dockerfile
```

-	Layers:
	-	`sha256:87a0d23eeeda6353dfc603cc4ffee062e5383be07b611754f3a88db3fc644036`  
		Last Modified: Thu, 18 Dec 2025 01:34:48 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b73cd5efe31baa1fbf0eecea269426edcfc795cbb9b5dd74b523ff51b6f7c9f`  
		Last Modified: Thu, 18 Dec 2025 01:34:48 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:c1a12b64cc8b47f50ea4610d9c1c362da7157b3ba67deac8b4760e6b589cde75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5611647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3591f95cad049a0509bd23a95556f8f848452d2a5491ed00bae293897c7a6b2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:27:48 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:27:49 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:49:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:49:50 GMT
USER memcache
# Thu, 18 Dec 2025 00:49:50 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:49:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf585eb2bfa372c2097b9f7a5214ecb0941a30581b10fb74a26518fcc7addec`  
		Last Modified: Thu, 18 Dec 2025 00:50:01 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bb148ea8fbe93dd8097d85f9ee3cf547d314e669748b4239c05711b0d5f719`  
		Last Modified: Thu, 18 Dec 2025 00:50:02 GMT  
		Size: 102.7 KB (102652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6549359cda37ac41cf41a5ece5f37f1322a82f6b232f12e446c62840637093e`  
		Last Modified: Thu, 18 Dec 2025 00:50:02 GMT  
		Size: 1.9 MB (1939215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041e37eaffefcfb0809564ddea591be3cd818de5530e2c853c0bc9a2fa25c116`  
		Last Modified: Thu, 18 Dec 2025 00:50:05 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7907ae218c75b36c9a9002be8554131c271cde78b0280cb7a85029f99ad0bcdc`  
		Last Modified: Thu, 18 Dec 2025 00:50:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:a9c26fc290551b691574e093d3c28f4fe7b558b3f8173b3c99eb8a664c83a8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ca65d7156e6586d96310ea3162facd9849d5460d2939b461a25247b06a4d59`

```dockerfile
```

-	Layers:
	-	`sha256:d9c217dc241f1175812c47b6489d325a0574c0da554c6f8aa0b86a2d8aff05f9`  
		Last Modified: Thu, 18 Dec 2025 01:34:52 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:cee00a47bf7b8b5899a6cf1f5c692494df31b454f52b81f3c4886905a0c9bdd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91d78dbe118f2b7b0d6e850e1115de72c4fe3e30c55a5b53d8a844d14357d16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:56 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:30:57 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:33:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:33:51 GMT
USER memcache
# Thu, 18 Dec 2025 00:33:51 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:33:51 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa22c446792763e48f4680945ccc68d43c7906ef35a92e0b908f57ef53e72f0`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954155078f2265364295ebdf16fb114e991b1938d8a6951fb511163ab3b2b385`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 92.4 KB (92378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a25584b03ac5e45c66c3c616acfd9df1848e5db25219ef20feb2868c30c6332`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 1.9 MB (1897191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f237be962bb57c3f749904b5925c8e1d7e9013dfac7dd52cc9611ada81858e`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b07d9170b246a631c262d9f5d57f49278f7cd4805463b90b14aeca4dc61d93`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:64abe011fed6a9cf7b3290c752c50bffe81bb2e65cf6337e023efda87d49b451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b251b9c15ab7c5742bd3ab725df09f0ecb9f2491f92cf1c825bec598a31f4407`

```dockerfile
```

-	Layers:
	-	`sha256:1882c6d4361100a29fd5ab265587f65fa27b1df15e7f9349b30dac454facf98e`  
		Last Modified: Thu, 18 Dec 2025 01:34:55 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf0a88ab3838de6beab653497ab62a64cfb87b1dc83c5fa5b6f3907abfd88080`  
		Last Modified: Thu, 18 Dec 2025 01:34:56 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b6c3042e2bf09ec3d3f054d03b81313e8df717a49371ce916ff743e602796bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6285509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6691028570bbd843e6da26558c46162b8383212fcaaefcecb2d3f919e3401429`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:19 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:06 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:06 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb7b8445facedfc145b9478f74880f520776460f153005b7f437ec339aee530`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1853c901134389608b6e80aaa3e43cd67a35c71aecfdde4b5b7ed3b989a03c`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 121.9 KB (121860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a01d1ac5ce47f4494363e411e1cd25dea26438213a2d18d6bb104d0974d9a52`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 2.0 MB (1966561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115624f24ba74d393c2da3d65ed5b35a7afb3fa9ad143d3fb82c64953b3d0401`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87bba524314294ca97195ce65a35ec6d42d3f9f18c9cc0c05c064c9a3cf85c0`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2feda8921a7d67cd9f2f3d7186ed69ceb0d3c22af7a20bd230664e9bcf39096c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73c6548a24cc8ce7782d03377e89a4b4b0e4c2a48cd3a03a79193320fc4d834`

```dockerfile
```

-	Layers:
	-	`sha256:984e438122735983bf56bc3d638fb1b0baf8cfb26ce26f71e0a9b847d25f76b5`  
		Last Modified: Thu, 18 Dec 2025 01:34:59 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d6e8d91ca57b45f0050ec3833a8f09a7ce62f7ba9ec70e1ae12881ad4b2bb6f`  
		Last Modified: Thu, 18 Dec 2025 01:35:00 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:df1ba8af73cd6e3f8227557b097cd6b128ec0d410a3bbe7a2c282089c5641b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5740953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78dbfc1f8ea65ad6466795e278180963d4afe98dfbca4a4497bc73c99f07ed4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:43 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:44 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:29 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:29 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37ec5bf455c1d98d22e6f3dacb5b971dac8ea96d1fe9b9177a07c5277530646`  
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b2862af05c1582c8625c82ea0863dc2b6474e410d3e6a32876c920e0152c73`  
		Last Modified: Thu, 18 Dec 2025 00:32:42 GMT  
		Size: 110.7 KB (110740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30872a43f6c591fd9b979b49b0fb32107b4bfa8c1155657fa255aa199cf0b83b`  
		Last Modified: Thu, 18 Dec 2025 00:32:42 GMT  
		Size: 1.9 MB (1942762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a62c11b4aeceaba2e5e73a1bc29aa8b4fc42ccd0c7e8512cc11b96e48aef2f`  
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f553d362a11992264bf5364cfe13d248403c5baf2ecac784c26f444dbfb90388`  
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:e3b020c2afd9ae372e234c6ab67456908861fd24200448fd3cf741503a8a6f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abfcddfb1575f6cc07e51c6a379141589de7ea8c329a9bc5c1592f3186e6fda`

```dockerfile
```

-	Layers:
	-	`sha256:ff9be8ef1bab92275eb15ae5fd6a05e767abc1fe855455766200b3c0a1866e33`  
		Last Modified: Thu, 18 Dec 2025 01:35:03 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d7026bdf84e278b6976f0ccab2297ddc0284cf329414f56d12608dbc2acb940`  
		Last Modified: Thu, 18 Dec 2025 01:35:04 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:7292c7b145e08f87f78644bf2c3355fad1d0b4d9366f173ffa0634c3ec93addf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6031729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae72ba97ecea986f01bda1eb392aee1ded4b5a86b2edcabe92a2034143e155b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:33:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:33:42 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:36:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:36:14 GMT
USER memcache
# Thu, 18 Dec 2025 00:36:14 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:36:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c95450233dfe3e06529eb39ca4b46e6ad51ccf338cab64157669ff1fc0a8d72`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4079a2d61bafcf146b8f57b35f0e39bf2548e0963be10cff5086f9a56ccdd9d`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 126.3 KB (126257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f69efa1066815d67cf415d0aac5dcd305032257b6bded5a4c57a7444a1e7fd4`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 2.1 MB (2076363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357f4165f53a3d4c66ef270bcb5b5283a066af50f79924cccc7c73f6a4f6f4ab`  
		Last Modified: Thu, 18 Dec 2025 00:36:36 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a65ff5cefcbfc874c1cac0857339eaee0b07147dd26b6bfa18c00921b4f30c`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:1d06281345f2ac44a607d40d5e87de6abb99bbc6ee82d319e73f3794602d0282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4867a5aa08041c7e5ec69dfc84214226a7323d1ce703747ae2117675e2f74bcd`

```dockerfile
```

-	Layers:
	-	`sha256:282960f007d3f1f008333191d98a2ded5ff0f83075ace30043349b6c082c18fd`  
		Last Modified: Thu, 18 Dec 2025 01:35:08 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4755fffd5924e8405adfbed0f328ad9792eff20e2b8ad2025e1f5c85bca88618`  
		Last Modified: Thu, 18 Dec 2025 01:35:09 GMT  
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
$ docker pull memcached@sha256:e011484878fd5d1e2da6de478ac11d01ae80f0bdef1902dcde3ed53728803741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5857090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689ea71c305b80e206c68a215481290a1378e6375e32ad059455f7d041396aa6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:26 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:30:27 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:33:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:33:46 GMT
USER memcache
# Thu, 18 Dec 2025 00:33:46 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:33:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4594a6826f7ed03c8c4f9f2aebb9716eb6e16d5b5ab7e1bc247783b503c5b10`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f270744f8d8b82bc6657387109b33836a76d6dbf8faa645a997db7ea290cdb`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 114.3 KB (114299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91f8ee8f36703944a7bdcaf57cc5772fe9f79c74a088c33fa1b6da7de119f93`  
		Last Modified: Thu, 18 Dec 2025 00:34:02 GMT  
		Size: 2.0 MB (2017131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21d2db88668745770273c7b36d4d2c1e87a80b0118b8d775813860b467384c8`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd847159e169b898a67d4454fd5a22406c5ae623b16889d084a1d5f2d46a499`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:33ab737cb23dcde22de59a58e40f1f80d2c5e808ff3036519ae7d9db228fa37d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3562f7fd7806da24b1865c01a2246ac041b5e98d69c10ce6cbbe479f9408f9a1`

```dockerfile
```

-	Layers:
	-	`sha256:d5f43e64a79ee525bd0354a06e3284444fd642bbe6c1a782aa45ec2e20462f1d`  
		Last Modified: Thu, 18 Dec 2025 01:35:19 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bd2c024010f4f53d350bde9967c349efb3a58a2a812b14e17b29ddbd19eab87`  
		Last Modified: Thu, 18 Dec 2025 01:35:20 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine3.23`

```console
$ docker pull memcached@sha256:6f20032236ee1e3ae7edb0f8a060ce3d8c66cfad7a05fe84cfe88001f70a4eb1
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
$ docker pull memcached@sha256:9573a2399011fa86bb7b5d12bdab987d7931c98ddec0ef6802de7eb6d3c3e338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5956768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c79853acc5f24e9c28f15d45cef0aedc114e76bbacf7958eb6f555c22246e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:34 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:34 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:07 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:07 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:07 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c33ac8581cd04f31208409f36331e938a78e6ae3a7a3b530fe9dfebe6eb9ad`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583aae99135b9036c602a1c60743fc4fd519f261ac6d48ed60b01e1beb019e7f`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 106.0 KB (106050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ca22885c42a537f033850e8dff7eaeddbb7514902286739b48c084b55a8d6b`  
		Last Modified: Thu, 18 Dec 2025 00:32:19 GMT  
		Size: 2.0 MB (1989265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d146e2038834770bed57033a6c5d66ead5b731b8b133856dec6726ca21baee9`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c66e6c3acbe07806e3e96a97d97a2d4503713c4814d9b24a2f57f2c39200d05`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:cfdf2ea6bf2a04bb7ee1568efe0c8bd38a1f5e644250a9409479cce281891ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de792623281192b3965fdc95f31532c4d166e731f53e202be1e2a224c654633b`

```dockerfile
```

-	Layers:
	-	`sha256:87a0d23eeeda6353dfc603cc4ffee062e5383be07b611754f3a88db3fc644036`  
		Last Modified: Thu, 18 Dec 2025 01:34:48 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b73cd5efe31baa1fbf0eecea269426edcfc795cbb9b5dd74b523ff51b6f7c9f`  
		Last Modified: Thu, 18 Dec 2025 01:34:48 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; arm variant v6

```console
$ docker pull memcached@sha256:c1a12b64cc8b47f50ea4610d9c1c362da7157b3ba67deac8b4760e6b589cde75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5611647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3591f95cad049a0509bd23a95556f8f848452d2a5491ed00bae293897c7a6b2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:27:48 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:27:49 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:49:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:49:50 GMT
USER memcache
# Thu, 18 Dec 2025 00:49:50 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:49:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf585eb2bfa372c2097b9f7a5214ecb0941a30581b10fb74a26518fcc7addec`  
		Last Modified: Thu, 18 Dec 2025 00:50:01 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bb148ea8fbe93dd8097d85f9ee3cf547d314e669748b4239c05711b0d5f719`  
		Last Modified: Thu, 18 Dec 2025 00:50:02 GMT  
		Size: 102.7 KB (102652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6549359cda37ac41cf41a5ece5f37f1322a82f6b232f12e446c62840637093e`  
		Last Modified: Thu, 18 Dec 2025 00:50:02 GMT  
		Size: 1.9 MB (1939215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041e37eaffefcfb0809564ddea591be3cd818de5530e2c853c0bc9a2fa25c116`  
		Last Modified: Thu, 18 Dec 2025 00:50:05 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7907ae218c75b36c9a9002be8554131c271cde78b0280cb7a85029f99ad0bcdc`  
		Last Modified: Thu, 18 Dec 2025 00:50:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:a9c26fc290551b691574e093d3c28f4fe7b558b3f8173b3c99eb8a664c83a8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ca65d7156e6586d96310ea3162facd9849d5460d2939b461a25247b06a4d59`

```dockerfile
```

-	Layers:
	-	`sha256:d9c217dc241f1175812c47b6489d325a0574c0da554c6f8aa0b86a2d8aff05f9`  
		Last Modified: Thu, 18 Dec 2025 01:34:52 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; arm variant v7

```console
$ docker pull memcached@sha256:cee00a47bf7b8b5899a6cf1f5c692494df31b454f52b81f3c4886905a0c9bdd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91d78dbe118f2b7b0d6e850e1115de72c4fe3e30c55a5b53d8a844d14357d16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:56 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:30:57 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:33:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:33:51 GMT
USER memcache
# Thu, 18 Dec 2025 00:33:51 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:33:51 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa22c446792763e48f4680945ccc68d43c7906ef35a92e0b908f57ef53e72f0`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954155078f2265364295ebdf16fb114e991b1938d8a6951fb511163ab3b2b385`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 92.4 KB (92378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a25584b03ac5e45c66c3c616acfd9df1848e5db25219ef20feb2868c30c6332`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 1.9 MB (1897191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f237be962bb57c3f749904b5925c8e1d7e9013dfac7dd52cc9611ada81858e`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b07d9170b246a631c262d9f5d57f49278f7cd4805463b90b14aeca4dc61d93`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:64abe011fed6a9cf7b3290c752c50bffe81bb2e65cf6337e023efda87d49b451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b251b9c15ab7c5742bd3ab725df09f0ecb9f2491f92cf1c825bec598a31f4407`

```dockerfile
```

-	Layers:
	-	`sha256:1882c6d4361100a29fd5ab265587f65fa27b1df15e7f9349b30dac454facf98e`  
		Last Modified: Thu, 18 Dec 2025 01:34:55 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf0a88ab3838de6beab653497ab62a64cfb87b1dc83c5fa5b6f3907abfd88080`  
		Last Modified: Thu, 18 Dec 2025 01:34:56 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b6c3042e2bf09ec3d3f054d03b81313e8df717a49371ce916ff743e602796bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6285509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6691028570bbd843e6da26558c46162b8383212fcaaefcecb2d3f919e3401429`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:19 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:06 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:06 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb7b8445facedfc145b9478f74880f520776460f153005b7f437ec339aee530`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1853c901134389608b6e80aaa3e43cd67a35c71aecfdde4b5b7ed3b989a03c`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 121.9 KB (121860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a01d1ac5ce47f4494363e411e1cd25dea26438213a2d18d6bb104d0974d9a52`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 2.0 MB (1966561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115624f24ba74d393c2da3d65ed5b35a7afb3fa9ad143d3fb82c64953b3d0401`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87bba524314294ca97195ce65a35ec6d42d3f9f18c9cc0c05c064c9a3cf85c0`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:2feda8921a7d67cd9f2f3d7186ed69ceb0d3c22af7a20bd230664e9bcf39096c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73c6548a24cc8ce7782d03377e89a4b4b0e4c2a48cd3a03a79193320fc4d834`

```dockerfile
```

-	Layers:
	-	`sha256:984e438122735983bf56bc3d638fb1b0baf8cfb26ce26f71e0a9b847d25f76b5`  
		Last Modified: Thu, 18 Dec 2025 01:34:59 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d6e8d91ca57b45f0050ec3833a8f09a7ce62f7ba9ec70e1ae12881ad4b2bb6f`  
		Last Modified: Thu, 18 Dec 2025 01:35:00 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; 386

```console
$ docker pull memcached@sha256:df1ba8af73cd6e3f8227557b097cd6b128ec0d410a3bbe7a2c282089c5641b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5740953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78dbfc1f8ea65ad6466795e278180963d4afe98dfbca4a4497bc73c99f07ed4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:43 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:44 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:29 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:29 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37ec5bf455c1d98d22e6f3dacb5b971dac8ea96d1fe9b9177a07c5277530646`  
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b2862af05c1582c8625c82ea0863dc2b6474e410d3e6a32876c920e0152c73`  
		Last Modified: Thu, 18 Dec 2025 00:32:42 GMT  
		Size: 110.7 KB (110740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30872a43f6c591fd9b979b49b0fb32107b4bfa8c1155657fa255aa199cf0b83b`  
		Last Modified: Thu, 18 Dec 2025 00:32:42 GMT  
		Size: 1.9 MB (1942762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a62c11b4aeceaba2e5e73a1bc29aa8b4fc42ccd0c7e8512cc11b96e48aef2f`  
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f553d362a11992264bf5364cfe13d248403c5baf2ecac784c26f444dbfb90388`  
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:e3b020c2afd9ae372e234c6ab67456908861fd24200448fd3cf741503a8a6f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abfcddfb1575f6cc07e51c6a379141589de7ea8c329a9bc5c1592f3186e6fda`

```dockerfile
```

-	Layers:
	-	`sha256:ff9be8ef1bab92275eb15ae5fd6a05e767abc1fe855455766200b3c0a1866e33`  
		Last Modified: Thu, 18 Dec 2025 01:35:03 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d7026bdf84e278b6976f0ccab2297ddc0284cf329414f56d12608dbc2acb940`  
		Last Modified: Thu, 18 Dec 2025 01:35:04 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; ppc64le

```console
$ docker pull memcached@sha256:7292c7b145e08f87f78644bf2c3355fad1d0b4d9366f173ffa0634c3ec93addf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6031729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae72ba97ecea986f01bda1eb392aee1ded4b5a86b2edcabe92a2034143e155b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:33:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:33:42 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:36:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:36:14 GMT
USER memcache
# Thu, 18 Dec 2025 00:36:14 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:36:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c95450233dfe3e06529eb39ca4b46e6ad51ccf338cab64157669ff1fc0a8d72`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4079a2d61bafcf146b8f57b35f0e39bf2548e0963be10cff5086f9a56ccdd9d`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 126.3 KB (126257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f69efa1066815d67cf415d0aac5dcd305032257b6bded5a4c57a7444a1e7fd4`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 2.1 MB (2076363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357f4165f53a3d4c66ef270bcb5b5283a066af50f79924cccc7c73f6a4f6f4ab`  
		Last Modified: Thu, 18 Dec 2025 00:36:36 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a65ff5cefcbfc874c1cac0857339eaee0b07147dd26b6bfa18c00921b4f30c`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:1d06281345f2ac44a607d40d5e87de6abb99bbc6ee82d319e73f3794602d0282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4867a5aa08041c7e5ec69dfc84214226a7323d1ce703747ae2117675e2f74bcd`

```dockerfile
```

-	Layers:
	-	`sha256:282960f007d3f1f008333191d98a2ded5ff0f83075ace30043349b6c082c18fd`  
		Last Modified: Thu, 18 Dec 2025 01:35:08 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4755fffd5924e8405adfbed0f328ad9792eff20e2b8ad2025e1f5c85bca88618`  
		Last Modified: Thu, 18 Dec 2025 01:35:09 GMT  
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
$ docker pull memcached@sha256:e011484878fd5d1e2da6de478ac11d01ae80f0bdef1902dcde3ed53728803741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5857090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689ea71c305b80e206c68a215481290a1378e6375e32ad059455f7d041396aa6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:26 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:30:27 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:33:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:33:46 GMT
USER memcache
# Thu, 18 Dec 2025 00:33:46 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:33:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4594a6826f7ed03c8c4f9f2aebb9716eb6e16d5b5ab7e1bc247783b503c5b10`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f270744f8d8b82bc6657387109b33836a76d6dbf8faa645a997db7ea290cdb`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 114.3 KB (114299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91f8ee8f36703944a7bdcaf57cc5772fe9f79c74a088c33fa1b6da7de119f93`  
		Last Modified: Thu, 18 Dec 2025 00:34:02 GMT  
		Size: 2.0 MB (2017131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21d2db88668745770273c7b36d4d2c1e87a80b0118b8d775813860b467384c8`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd847159e169b898a67d4454fd5a22406c5ae623b16889d084a1d5f2d46a499`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:33ab737cb23dcde22de59a58e40f1f80d2c5e808ff3036519ae7d9db228fa37d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3562f7fd7806da24b1865c01a2246ac041b5e98d69c10ce6cbbe479f9408f9a1`

```dockerfile
```

-	Layers:
	-	`sha256:d5f43e64a79ee525bd0354a06e3284444fd642bbe6c1a782aa45ec2e20462f1d`  
		Last Modified: Thu, 18 Dec 2025 01:35:19 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bd2c024010f4f53d350bde9967c349efb3a58a2a812b14e17b29ddbd19eab87`  
		Last Modified: Thu, 18 Dec 2025 01:35:20 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-trixie`

```console
$ docker pull memcached@sha256:9ae868852d0bc0974e4dd39c58436f73698081a31e61b8099871983e09d79f80
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
$ docker pull memcached@sha256:c9046d2a0ade04c91892254044294c2a529006458cd7b98bdc31b4054fffbfe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32193341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6654931990345ba058b2f50cedc8d03dfcc174d6809b0e7a820c12f7b93dc09d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:35:37 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:23 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:23 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:23 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:23 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:23 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b6bc7772cb8044287682c4af75ca1c8280c4837d5ffee58adc014018f02e91`  
		Last Modified: Wed, 17 Dec 2025 21:38:42 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3af321fdb36bbbb634d6be4a6e457f7eeb47b153460c7bab6c9eae91724b08b`  
		Last Modified: Wed, 17 Dec 2025 21:38:42 GMT  
		Size: 136.7 KB (136691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a00f7c8e317ad005bdf0117005dd753e347a8674b068c660bbc29b3f93a0621`  
		Last Modified: Wed, 17 Dec 2025 21:38:42 GMT  
		Size: 2.3 MB (2278641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb739034830ce246e4bc00aa883c7d2af8a1fd59bc3e2ea17cae3607bf281074`  
		Last Modified: Wed, 17 Dec 2025 21:38:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33cfbae525009776fcee65339602ed1b2a8a5f2c51898ec9fc499fe35c60b87`  
		Last Modified: Wed, 17 Dec 2025 21:38:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:e726a4ddf8221754a6a9fa1143cee47f51785aedb20dc0329a7c7b41b4772763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd3f16921a7fcccc9bc6ee3685e192e34a0b621f1c95362d6cea5e4293e54d33`

```dockerfile
```

-	Layers:
	-	`sha256:3a55af39eac38dca280008ae509d726055b1dde6e05ce9024174d0a0bd0565c2`  
		Last Modified: Wed, 17 Dec 2025 22:34:37 GMT  
		Size: 2.0 MB (2008228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef418f126bca0d267c3b365faed9990a104832e94e7ec35841aff2c2b26510dc`  
		Last Modified: Wed, 17 Dec 2025 22:34:38 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:c1a14cf6b3aa6f9ee13feee1c176a4ff104ec3d361f2df684e87a9d88a563eaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30300251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7375c421f8c059114c1a5cdc58215c8cf41dcc23355cbef325fdfa4b290df1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:39:00 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:39:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:42:24 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:42:24 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:42:24 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:42:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:42:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:42:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:42:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:42:24 GMT
USER memcache
# Wed, 17 Dec 2025 21:42:24 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:42:24 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d97bc71d0fa535127863fdab265dfddb07b3cda35b80de4dd2b9b67fe154c856`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 27.9 MB (27944187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e168dbb57c754690bc257f600efb5085929be35091c7e3d6926d35490c3391`  
		Last Modified: Wed, 17 Dec 2025 21:42:38 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78870a4506eecc7b424a3cedde90baa4c44a7c5d1174e6842b60c11b08a7984e`  
		Last Modified: Wed, 17 Dec 2025 21:42:40 GMT  
		Size: 144.2 KB (144157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e35d5393bf24a4f7ba0c87d734e7fda2d09414dec61e9139726200bed52e262`  
		Last Modified: Wed, 17 Dec 2025 21:42:39 GMT  
		Size: 2.2 MB (2210395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72c9d61ca04e663f67ab23ad2c50afcd810d29c2f52728277947d5ab78c03da`  
		Last Modified: Wed, 17 Dec 2025 21:42:38 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e89f91fff1d699acc4ebbc8ebb2a409d5f7867914100e87affef7b7d8775488`  
		Last Modified: Wed, 17 Dec 2025 21:42:38 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:3a82f6da1fa8b6c43220785849304c0e09363556371c8f763abae2126e271c5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e59d44e1c5460c7338a49dad6ec9d6d03db5b9330bb235c1d01e3e182df704ca`

```dockerfile
```

-	Layers:
	-	`sha256:2b38edaa9de8bf0d9055274c5ca1c0af276da0f57396ee1edfb8db1002dc8834`  
		Last Modified: Wed, 17 Dec 2025 22:34:42 GMT  
		Size: 2.0 MB (2011231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c70377fb854a2602cbb12ee80dd69f8a5deb00e23feb0c3c24e1b27806029b0d`  
		Last Modified: Wed, 17 Dec 2025 22:34:43 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:b7ad53cb1e5a5631cc9b08d0fe984b0ba6bb7ab77da4309a552dbb97bd4ae04e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28510860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b2fbe25ebf8c8035604591c6ded5acfffe219c97c853c1c0e00421ac18abcd4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:35:20 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:30 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:30 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:30 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:30 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:30 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:30 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d46de1cc714aa644c02bc1b184e957b7330bf3473d4e97f72f454fdc8a432d`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0327c8719a60b04c8b690d8d0a0a122cdbc620f2aab391fd43789a8803b62bf1`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 135.4 KB (135362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd55327cbd82c4adf176e679bae5436e8aaf27c54595ec2cd7cfec20989b1fc`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 2.2 MB (2163972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37babf40b7b24af06cfbfc9fe6daf7d6f5863de148318182eecf29e242ba5e4c`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3daf0d6e9f1032a9bce2c34a57a6049ec4ffd4a412a20724540653fe7b6526d3`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:77b0259560abd3025ae0593b06db95eb3c4dd6dccbd2332f85286fae97d799bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd1267e1c8eb093b3e5a265d3c2d0c9b2b3784e50b6aa7edfec29ba838d4a8c`

```dockerfile
```

-	Layers:
	-	`sha256:3266292cf75a57aab22a4e279bf40458841e617570f3ee192bb26dc1d2d6e1ef`  
		Last Modified: Wed, 17 Dec 2025 22:34:47 GMT  
		Size: 2.0 MB (2009688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cc2be86d85bc478731bb7718f18d50da352f58c942412f66ca371226633d3bb`  
		Last Modified: Wed, 17 Dec 2025 22:34:48 GMT  
		Size: 22.3 KB (22303 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:230a135d43b1bf876ec5c160b78cb4f0303d1e6e98dc76a31dd524d28a4a5279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32554912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79214d48c3616d6c032db23eb36a6766c7a96a8d4619d8f8791d2fa43163cc34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:35:24 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:26 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:26 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:26 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:26 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:26 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:26 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f49eb557c72f2fe7e0eb1949c1587e8e4c86bdae514d70fac3ff429290a149`  
		Last Modified: Wed, 17 Dec 2025 21:38:46 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f764f8f3ed63ac8e640ebdcb2f5ea0371b6fb244a1f6defbe51ddfff908a34a`  
		Last Modified: Wed, 17 Dec 2025 21:38:46 GMT  
		Size: 153.5 KB (153477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9353d672d9aeb0b8a3ee269d120b0b920e9f6b81998ed7ef7765092573e4b716`  
		Last Modified: Wed, 17 Dec 2025 21:38:46 GMT  
		Size: 2.3 MB (2261292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ba4d16dc49a02e1490d18a58f5e108ec18a248f9ea83bb7b4deb8642b36f90`  
		Last Modified: Wed, 17 Dec 2025 21:38:46 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d15340fcbda1a05a50ba392408ace29b5cbb21b398bb1018750621349d3b0a`  
		Last Modified: Wed, 17 Dec 2025 21:38:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:d2a465ef21f85d63f634e52f05c50319a05c013d1aeed6321cc146b3a28a5920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c092dec716fd21afebb19ce5e88ba467a0f4bb88a40068e3e266b1f10ff6652`

```dockerfile
```

-	Layers:
	-	`sha256:b7bd1c3aaf184ba5d6dfbf328c24c2f39511de9c6e21c04b7fa212d6a26b0049`  
		Last Modified: Wed, 17 Dec 2025 22:34:53 GMT  
		Size: 2.0 MB (2008544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc6165d17a79a40bba13d288c74c5c34aa4af72304a300a74ceededf1a934bbc`  
		Last Modified: Wed, 17 Dec 2025 22:34:54 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; 386

```console
$ docker pull memcached@sha256:35df20cb1713a9d5fbb1820acac102f3c3560dfa2d0fa147fff30dfc53f209bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33665704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ccada050045e330c6b125cae2adfcf8e5edb8e23b5e044c0d53861f7762294a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:35:51 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:43 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:43 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:43 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:43 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:43 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b054f6842adaecae2d5cf75c99601b690566759a58606bc981ccae49baaae51`  
		Last Modified: Wed, 17 Dec 2025 21:38:57 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43efb4f909536827644b2ca98420204710b14f6195238a8ffdbf658c29883be`  
		Last Modified: Wed, 17 Dec 2025 21:38:57 GMT  
		Size: 147.5 KB (147519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:792eb292285447291b91c55e07bc1a75b3d4e125a3c23f80671848c5f967e042`  
		Last Modified: Wed, 17 Dec 2025 21:38:57 GMT  
		Size: 2.2 MB (2223600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe79378953d034686129f0d36718bb867ebebf130cd1f431ad68cf117a1308c6`  
		Last Modified: Wed, 17 Dec 2025 21:38:57 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92088f114f464c2f2e1217404e900d24a46a03305faa6cae793f0b873cadba52`  
		Last Modified: Wed, 17 Dec 2025 21:38:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:3a428e326360172543ee458a46a55c1b9e70d3eeeea945f2ed65839c307eddd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a62b1d6c9ce3819b6b67f9de9cc436a2f4cb362fad3a8c07627fd790e4bd8be7`

```dockerfile
```

-	Layers:
	-	`sha256:0f8e75010a0e7df5356c9c36b97dff2c5d2191f6f6e643619b4363f8c1e1dc42`  
		Last Modified: Wed, 17 Dec 2025 22:34:58 GMT  
		Size: 2.0 MB (2005385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98883c6827ebd9ca960545767f09a2be89e7580fc425e24f86364f3a9e4ea283`  
		Last Modified: Wed, 17 Dec 2025 22:34:59 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:38a236f83eb206f786b39c53e8f756815f0bda1460157b11844faf21735208bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36162589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41292f5c75fe5f3a464b809bde41e0ae8849ad8d7046918a548d0c6b2e250a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:34:54 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:28 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:28 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:28 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2b42546c7b688160cfd1a0da61a24922a019b4ebead88e23aff01482ddd477`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4efe9fd2e012174cd86a64f83d7b7facfe14ee67c9c9fa5ce994f22c24173f2c`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 170.4 KB (170393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9752985ba696f0f8d5831ac91e19bfe336342b1c403542641c575b1dc6116e`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 2.4 MB (2393786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d11c68ba0bc913d139eea51cb2957c1ddd713515fc06dfa5d4c398b119535a`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9186b8b7184cef442ae3ed6a3feadcaa8f4ccc974ed5ae6c6cf8efe37e679f23`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:00d1019e9978171df76f638253f212405bf7d53251607ef5a5933d5b28d867b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588d3d6ab54a9ea5c8baf9b013bb23c12826989ba0d09cb862431e2fa30e5189`

```dockerfile
```

-	Layers:
	-	`sha256:799ad025578a6d5d0155dc5be223bfbc25ffa3aa0548e4fb2e4bedeb0a5088d9`  
		Last Modified: Wed, 17 Dec 2025 22:35:03 GMT  
		Size: 2.0 MB (2011829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaa03114ccb63fbbd8ca04eef46baa26c8a0508f1256aa45d851f3a49f2ed47a`  
		Last Modified: Wed, 17 Dec 2025 22:35:04 GMT  
		Size: 22.2 KB (22225 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:5aedcd2b04ff2d8dc77fb6568e6ce96878f75508a3a01326623b60869874f8a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30615184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab5d9dd83f52434969fb6da016bd60451fd5d989e33e2cd491533dcb4553c835`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 05:30:55 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 09 Dec 2025 05:31:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Dec 2025 03:19:32 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 03:19:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 03:19:32 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 03:19:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 18 Dec 2025 03:19:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 03:19:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 03:19:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 03:19:33 GMT
USER memcache
# Thu, 18 Dec 2025 03:19:33 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 03:19:33 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb23364b88c4686dab6a11bf004aac89beea8adb8559fd39799a54dc729c23a6`  
		Last Modified: Tue, 09 Dec 2025 05:57:38 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edeeae49e27528d2079d0d5aeb702d7dd56503463fa4054ee2444f847f399650`  
		Last Modified: Tue, 09 Dec 2025 05:57:38 GMT  
		Size: 133.1 KB (133076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e584b688c99191b71a2471afe63daff415a1eedcf541b959dfcdf248eebd8577`  
		Last Modified: Thu, 18 Dec 2025 03:20:28 GMT  
		Size: 2.2 MB (2207438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b780b2b80274922cc63f0afe1ecd2680bcafae3234732fd03ba740690e3ebf1`  
		Last Modified: Thu, 18 Dec 2025 03:20:28 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5449346fa21339be4109a2e289721bfa7b0e8203b88fe202956ebb257c703a88`  
		Last Modified: Thu, 18 Dec 2025 03:20:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:bbe7bbb4c3590b1fc9c5943719d3b1b2a21670d2874ed90415040aeae5b13200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c721ad9798565707f4e9e537a1618b5efafce47c49577053fe7b40879caca9`

```dockerfile
```

-	Layers:
	-	`sha256:37125be6342f13dcb1fff2b0c3def6d6f3b808e19192f9ff68a139ce2d1d3083`  
		Last Modified: Thu, 18 Dec 2025 04:34:34 GMT  
		Size: 2.0 MB (2002192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06edc085828555adcb8aac4ef4e564c72d260338e77dde6abe811eefcdd8682d`  
		Last Modified: Thu, 18 Dec 2025 04:34:35 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:1e7fc2740e66d7d7b21982f73ae72e901616fcb9ebc6176c6f1d931c6a4732b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32273737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f632195b7b4a10526fcb27d2d66a479b07455d784656340bcbae2d31e292aa2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:34:51 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:34:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:04 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:04 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:04 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:04 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:04 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:04 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9606e3e114197b678b6fbd5b889ab574d2ad4cd8b4010407f847a98309f0f6b`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24f23dd2596713c0a8daf1cde9aabc7d26e7e9b832300ba1ce4615e8c806afc`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 140.5 KB (140507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0dd33ff71e256560cf1693538e8ecc4f92550f6483c1478697b822abf8d0f84`  
		Last Modified: Wed, 17 Dec 2025 21:38:19 GMT  
		Size: 2.3 MB (2297315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568ee6e9ecd99ef323ff6ff6b40b5fcf91b13472f56ac46f8b3036c82c705fd6`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91a63e3e27d493e5ad7b64edf0b8ae2bb8ade89a55bfc197b4dc9a393ceec4b`  
		Last Modified: Wed, 17 Dec 2025 21:38:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:d9aa5142dc8acd96ae2fb7235ceda06498adc21053e1bc5bf02ff76701213426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e87c93018f4f94a4286dcf6f6d33373729ef4263208b2f346e92a2028839a2`

```dockerfile
```

-	Layers:
	-	`sha256:c0ee3f2287a538730e473aea557f8fc2a48d18bb9e778e65ccdbf8918310ace3`  
		Last Modified: Wed, 17 Dec 2025 22:35:11 GMT  
		Size: 2.0 MB (2009665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce86917337210887b4362390f278a89c9fc6d6d1cc50e29ebf7f716bc556c877`  
		Last Modified: Wed, 17 Dec 2025 22:35:12 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.40`

```console
$ docker pull memcached@sha256:9ae868852d0bc0974e4dd39c58436f73698081a31e61b8099871983e09d79f80
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

### `memcached:1.6.40` - linux; amd64

```console
$ docker pull memcached@sha256:c9046d2a0ade04c91892254044294c2a529006458cd7b98bdc31b4054fffbfe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32193341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6654931990345ba058b2f50cedc8d03dfcc174d6809b0e7a820c12f7b93dc09d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:35:37 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:23 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:23 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:23 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:23 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:23 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b6bc7772cb8044287682c4af75ca1c8280c4837d5ffee58adc014018f02e91`  
		Last Modified: Wed, 17 Dec 2025 21:38:42 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3af321fdb36bbbb634d6be4a6e457f7eeb47b153460c7bab6c9eae91724b08b`  
		Last Modified: Wed, 17 Dec 2025 21:38:42 GMT  
		Size: 136.7 KB (136691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a00f7c8e317ad005bdf0117005dd753e347a8674b068c660bbc29b3f93a0621`  
		Last Modified: Wed, 17 Dec 2025 21:38:42 GMT  
		Size: 2.3 MB (2278641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb739034830ce246e4bc00aa883c7d2af8a1fd59bc3e2ea17cae3607bf281074`  
		Last Modified: Wed, 17 Dec 2025 21:38:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33cfbae525009776fcee65339602ed1b2a8a5f2c51898ec9fc499fe35c60b87`  
		Last Modified: Wed, 17 Dec 2025 21:38:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40` - unknown; unknown

```console
$ docker pull memcached@sha256:e726a4ddf8221754a6a9fa1143cee47f51785aedb20dc0329a7c7b41b4772763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd3f16921a7fcccc9bc6ee3685e192e34a0b621f1c95362d6cea5e4293e54d33`

```dockerfile
```

-	Layers:
	-	`sha256:3a55af39eac38dca280008ae509d726055b1dde6e05ce9024174d0a0bd0565c2`  
		Last Modified: Wed, 17 Dec 2025 22:34:37 GMT  
		Size: 2.0 MB (2008228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef418f126bca0d267c3b365faed9990a104832e94e7ec35841aff2c2b26510dc`  
		Last Modified: Wed, 17 Dec 2025 22:34:38 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40` - linux; arm variant v5

```console
$ docker pull memcached@sha256:c1a14cf6b3aa6f9ee13feee1c176a4ff104ec3d361f2df684e87a9d88a563eaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30300251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7375c421f8c059114c1a5cdc58215c8cf41dcc23355cbef325fdfa4b290df1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:39:00 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:39:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:42:24 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:42:24 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:42:24 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:42:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:42:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:42:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:42:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:42:24 GMT
USER memcache
# Wed, 17 Dec 2025 21:42:24 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:42:24 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d97bc71d0fa535127863fdab265dfddb07b3cda35b80de4dd2b9b67fe154c856`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 27.9 MB (27944187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e168dbb57c754690bc257f600efb5085929be35091c7e3d6926d35490c3391`  
		Last Modified: Wed, 17 Dec 2025 21:42:38 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78870a4506eecc7b424a3cedde90baa4c44a7c5d1174e6842b60c11b08a7984e`  
		Last Modified: Wed, 17 Dec 2025 21:42:40 GMT  
		Size: 144.2 KB (144157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e35d5393bf24a4f7ba0c87d734e7fda2d09414dec61e9139726200bed52e262`  
		Last Modified: Wed, 17 Dec 2025 21:42:39 GMT  
		Size: 2.2 MB (2210395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72c9d61ca04e663f67ab23ad2c50afcd810d29c2f52728277947d5ab78c03da`  
		Last Modified: Wed, 17 Dec 2025 21:42:38 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e89f91fff1d699acc4ebbc8ebb2a409d5f7867914100e87affef7b7d8775488`  
		Last Modified: Wed, 17 Dec 2025 21:42:38 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40` - unknown; unknown

```console
$ docker pull memcached@sha256:3a82f6da1fa8b6c43220785849304c0e09363556371c8f763abae2126e271c5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e59d44e1c5460c7338a49dad6ec9d6d03db5b9330bb235c1d01e3e182df704ca`

```dockerfile
```

-	Layers:
	-	`sha256:2b38edaa9de8bf0d9055274c5ca1c0af276da0f57396ee1edfb8db1002dc8834`  
		Last Modified: Wed, 17 Dec 2025 22:34:42 GMT  
		Size: 2.0 MB (2011231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c70377fb854a2602cbb12ee80dd69f8a5deb00e23feb0c3c24e1b27806029b0d`  
		Last Modified: Wed, 17 Dec 2025 22:34:43 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40` - linux; arm variant v7

```console
$ docker pull memcached@sha256:b7ad53cb1e5a5631cc9b08d0fe984b0ba6bb7ab77da4309a552dbb97bd4ae04e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28510860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b2fbe25ebf8c8035604591c6ded5acfffe219c97c853c1c0e00421ac18abcd4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:35:20 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:30 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:30 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:30 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:30 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:30 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:30 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d46de1cc714aa644c02bc1b184e957b7330bf3473d4e97f72f454fdc8a432d`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0327c8719a60b04c8b690d8d0a0a122cdbc620f2aab391fd43789a8803b62bf1`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 135.4 KB (135362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd55327cbd82c4adf176e679bae5436e8aaf27c54595ec2cd7cfec20989b1fc`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 2.2 MB (2163972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37babf40b7b24af06cfbfc9fe6daf7d6f5863de148318182eecf29e242ba5e4c`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3daf0d6e9f1032a9bce2c34a57a6049ec4ffd4a412a20724540653fe7b6526d3`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40` - unknown; unknown

```console
$ docker pull memcached@sha256:77b0259560abd3025ae0593b06db95eb3c4dd6dccbd2332f85286fae97d799bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd1267e1c8eb093b3e5a265d3c2d0c9b2b3784e50b6aa7edfec29ba838d4a8c`

```dockerfile
```

-	Layers:
	-	`sha256:3266292cf75a57aab22a4e279bf40458841e617570f3ee192bb26dc1d2d6e1ef`  
		Last Modified: Wed, 17 Dec 2025 22:34:47 GMT  
		Size: 2.0 MB (2009688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cc2be86d85bc478731bb7718f18d50da352f58c942412f66ca371226633d3bb`  
		Last Modified: Wed, 17 Dec 2025 22:34:48 GMT  
		Size: 22.3 KB (22303 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:230a135d43b1bf876ec5c160b78cb4f0303d1e6e98dc76a31dd524d28a4a5279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32554912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79214d48c3616d6c032db23eb36a6766c7a96a8d4619d8f8791d2fa43163cc34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:35:24 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:26 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:26 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:26 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:26 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:26 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:26 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f49eb557c72f2fe7e0eb1949c1587e8e4c86bdae514d70fac3ff429290a149`  
		Last Modified: Wed, 17 Dec 2025 21:38:46 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f764f8f3ed63ac8e640ebdcb2f5ea0371b6fb244a1f6defbe51ddfff908a34a`  
		Last Modified: Wed, 17 Dec 2025 21:38:46 GMT  
		Size: 153.5 KB (153477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9353d672d9aeb0b8a3ee269d120b0b920e9f6b81998ed7ef7765092573e4b716`  
		Last Modified: Wed, 17 Dec 2025 21:38:46 GMT  
		Size: 2.3 MB (2261292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ba4d16dc49a02e1490d18a58f5e108ec18a248f9ea83bb7b4deb8642b36f90`  
		Last Modified: Wed, 17 Dec 2025 21:38:46 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d15340fcbda1a05a50ba392408ace29b5cbb21b398bb1018750621349d3b0a`  
		Last Modified: Wed, 17 Dec 2025 21:38:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40` - unknown; unknown

```console
$ docker pull memcached@sha256:d2a465ef21f85d63f634e52f05c50319a05c013d1aeed6321cc146b3a28a5920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c092dec716fd21afebb19ce5e88ba467a0f4bb88a40068e3e266b1f10ff6652`

```dockerfile
```

-	Layers:
	-	`sha256:b7bd1c3aaf184ba5d6dfbf328c24c2f39511de9c6e21c04b7fa212d6a26b0049`  
		Last Modified: Wed, 17 Dec 2025 22:34:53 GMT  
		Size: 2.0 MB (2008544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc6165d17a79a40bba13d288c74c5c34aa4af72304a300a74ceededf1a934bbc`  
		Last Modified: Wed, 17 Dec 2025 22:34:54 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40` - linux; 386

```console
$ docker pull memcached@sha256:35df20cb1713a9d5fbb1820acac102f3c3560dfa2d0fa147fff30dfc53f209bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33665704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ccada050045e330c6b125cae2adfcf8e5edb8e23b5e044c0d53861f7762294a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:35:51 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:43 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:43 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:43 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:43 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:43 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b054f6842adaecae2d5cf75c99601b690566759a58606bc981ccae49baaae51`  
		Last Modified: Wed, 17 Dec 2025 21:38:57 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43efb4f909536827644b2ca98420204710b14f6195238a8ffdbf658c29883be`  
		Last Modified: Wed, 17 Dec 2025 21:38:57 GMT  
		Size: 147.5 KB (147519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:792eb292285447291b91c55e07bc1a75b3d4e125a3c23f80671848c5f967e042`  
		Last Modified: Wed, 17 Dec 2025 21:38:57 GMT  
		Size: 2.2 MB (2223600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe79378953d034686129f0d36718bb867ebebf130cd1f431ad68cf117a1308c6`  
		Last Modified: Wed, 17 Dec 2025 21:38:57 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92088f114f464c2f2e1217404e900d24a46a03305faa6cae793f0b873cadba52`  
		Last Modified: Wed, 17 Dec 2025 21:38:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40` - unknown; unknown

```console
$ docker pull memcached@sha256:3a428e326360172543ee458a46a55c1b9e70d3eeeea945f2ed65839c307eddd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a62b1d6c9ce3819b6b67f9de9cc436a2f4cb362fad3a8c07627fd790e4bd8be7`

```dockerfile
```

-	Layers:
	-	`sha256:0f8e75010a0e7df5356c9c36b97dff2c5d2191f6f6e643619b4363f8c1e1dc42`  
		Last Modified: Wed, 17 Dec 2025 22:34:58 GMT  
		Size: 2.0 MB (2005385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98883c6827ebd9ca960545767f09a2be89e7580fc425e24f86364f3a9e4ea283`  
		Last Modified: Wed, 17 Dec 2025 22:34:59 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40` - linux; ppc64le

```console
$ docker pull memcached@sha256:38a236f83eb206f786b39c53e8f756815f0bda1460157b11844faf21735208bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36162589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41292f5c75fe5f3a464b809bde41e0ae8849ad8d7046918a548d0c6b2e250a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:34:54 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:28 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:28 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:28 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2b42546c7b688160cfd1a0da61a24922a019b4ebead88e23aff01482ddd477`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4efe9fd2e012174cd86a64f83d7b7facfe14ee67c9c9fa5ce994f22c24173f2c`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 170.4 KB (170393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9752985ba696f0f8d5831ac91e19bfe336342b1c403542641c575b1dc6116e`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 2.4 MB (2393786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d11c68ba0bc913d139eea51cb2957c1ddd713515fc06dfa5d4c398b119535a`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9186b8b7184cef442ae3ed6a3feadcaa8f4ccc974ed5ae6c6cf8efe37e679f23`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40` - unknown; unknown

```console
$ docker pull memcached@sha256:00d1019e9978171df76f638253f212405bf7d53251607ef5a5933d5b28d867b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588d3d6ab54a9ea5c8baf9b013bb23c12826989ba0d09cb862431e2fa30e5189`

```dockerfile
```

-	Layers:
	-	`sha256:799ad025578a6d5d0155dc5be223bfbc25ffa3aa0548e4fb2e4bedeb0a5088d9`  
		Last Modified: Wed, 17 Dec 2025 22:35:03 GMT  
		Size: 2.0 MB (2011829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaa03114ccb63fbbd8ca04eef46baa26c8a0508f1256aa45d851f3a49f2ed47a`  
		Last Modified: Wed, 17 Dec 2025 22:35:04 GMT  
		Size: 22.2 KB (22225 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40` - linux; riscv64

```console
$ docker pull memcached@sha256:5aedcd2b04ff2d8dc77fb6568e6ce96878f75508a3a01326623b60869874f8a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30615184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab5d9dd83f52434969fb6da016bd60451fd5d989e33e2cd491533dcb4553c835`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 05:30:55 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 09 Dec 2025 05:31:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Dec 2025 03:19:32 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 03:19:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 03:19:32 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 03:19:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 18 Dec 2025 03:19:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 03:19:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 03:19:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 03:19:33 GMT
USER memcache
# Thu, 18 Dec 2025 03:19:33 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 03:19:33 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb23364b88c4686dab6a11bf004aac89beea8adb8559fd39799a54dc729c23a6`  
		Last Modified: Tue, 09 Dec 2025 05:57:38 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edeeae49e27528d2079d0d5aeb702d7dd56503463fa4054ee2444f847f399650`  
		Last Modified: Tue, 09 Dec 2025 05:57:38 GMT  
		Size: 133.1 KB (133076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e584b688c99191b71a2471afe63daff415a1eedcf541b959dfcdf248eebd8577`  
		Last Modified: Thu, 18 Dec 2025 03:20:28 GMT  
		Size: 2.2 MB (2207438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b780b2b80274922cc63f0afe1ecd2680bcafae3234732fd03ba740690e3ebf1`  
		Last Modified: Thu, 18 Dec 2025 03:20:28 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5449346fa21339be4109a2e289721bfa7b0e8203b88fe202956ebb257c703a88`  
		Last Modified: Thu, 18 Dec 2025 03:20:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40` - unknown; unknown

```console
$ docker pull memcached@sha256:bbe7bbb4c3590b1fc9c5943719d3b1b2a21670d2874ed90415040aeae5b13200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c721ad9798565707f4e9e537a1618b5efafce47c49577053fe7b40879caca9`

```dockerfile
```

-	Layers:
	-	`sha256:37125be6342f13dcb1fff2b0c3def6d6f3b808e19192f9ff68a139ce2d1d3083`  
		Last Modified: Thu, 18 Dec 2025 04:34:34 GMT  
		Size: 2.0 MB (2002192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06edc085828555adcb8aac4ef4e564c72d260338e77dde6abe811eefcdd8682d`  
		Last Modified: Thu, 18 Dec 2025 04:34:35 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40` - linux; s390x

```console
$ docker pull memcached@sha256:1e7fc2740e66d7d7b21982f73ae72e901616fcb9ebc6176c6f1d931c6a4732b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32273737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f632195b7b4a10526fcb27d2d66a479b07455d784656340bcbae2d31e292aa2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:34:51 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:34:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:04 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:04 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:04 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:04 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:04 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:04 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9606e3e114197b678b6fbd5b889ab574d2ad4cd8b4010407f847a98309f0f6b`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24f23dd2596713c0a8daf1cde9aabc7d26e7e9b832300ba1ce4615e8c806afc`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 140.5 KB (140507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0dd33ff71e256560cf1693538e8ecc4f92550f6483c1478697b822abf8d0f84`  
		Last Modified: Wed, 17 Dec 2025 21:38:19 GMT  
		Size: 2.3 MB (2297315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568ee6e9ecd99ef323ff6ff6b40b5fcf91b13472f56ac46f8b3036c82c705fd6`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91a63e3e27d493e5ad7b64edf0b8ae2bb8ade89a55bfc197b4dc9a393ceec4b`  
		Last Modified: Wed, 17 Dec 2025 21:38:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40` - unknown; unknown

```console
$ docker pull memcached@sha256:d9aa5142dc8acd96ae2fb7235ceda06498adc21053e1bc5bf02ff76701213426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e87c93018f4f94a4286dcf6f6d33373729ef4263208b2f346e92a2028839a2`

```dockerfile
```

-	Layers:
	-	`sha256:c0ee3f2287a538730e473aea557f8fc2a48d18bb9e778e65ccdbf8918310ace3`  
		Last Modified: Wed, 17 Dec 2025 22:35:11 GMT  
		Size: 2.0 MB (2009665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce86917337210887b4362390f278a89c9fc6d6d1cc50e29ebf7f716bc556c877`  
		Last Modified: Wed, 17 Dec 2025 22:35:12 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.40-alpine`

```console
$ docker pull memcached@sha256:7c4b90ed70984e92d9b6a6fb5fdfe66eafb466fd40e93cb6994959cfeb4b6a24
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `memcached:1.6.40-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:9573a2399011fa86bb7b5d12bdab987d7931c98ddec0ef6802de7eb6d3c3e338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5956768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c79853acc5f24e9c28f15d45cef0aedc114e76bbacf7958eb6f555c22246e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:34 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:34 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:07 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:07 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:07 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c33ac8581cd04f31208409f36331e938a78e6ae3a7a3b530fe9dfebe6eb9ad`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583aae99135b9036c602a1c60743fc4fd519f261ac6d48ed60b01e1beb019e7f`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 106.0 KB (106050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ca22885c42a537f033850e8dff7eaeddbb7514902286739b48c084b55a8d6b`  
		Last Modified: Thu, 18 Dec 2025 00:32:19 GMT  
		Size: 2.0 MB (1989265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d146e2038834770bed57033a6c5d66ead5b731b8b133856dec6726ca21baee9`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c66e6c3acbe07806e3e96a97d97a2d4503713c4814d9b24a2f57f2c39200d05`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:cfdf2ea6bf2a04bb7ee1568efe0c8bd38a1f5e644250a9409479cce281891ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de792623281192b3965fdc95f31532c4d166e731f53e202be1e2a224c654633b`

```dockerfile
```

-	Layers:
	-	`sha256:87a0d23eeeda6353dfc603cc4ffee062e5383be07b611754f3a88db3fc644036`  
		Last Modified: Thu, 18 Dec 2025 01:34:48 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b73cd5efe31baa1fbf0eecea269426edcfc795cbb9b5dd74b523ff51b6f7c9f`  
		Last Modified: Thu, 18 Dec 2025 01:34:48 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:c1a12b64cc8b47f50ea4610d9c1c362da7157b3ba67deac8b4760e6b589cde75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5611647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3591f95cad049a0509bd23a95556f8f848452d2a5491ed00bae293897c7a6b2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:27:48 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:27:49 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:49:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:49:50 GMT
USER memcache
# Thu, 18 Dec 2025 00:49:50 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:49:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf585eb2bfa372c2097b9f7a5214ecb0941a30581b10fb74a26518fcc7addec`  
		Last Modified: Thu, 18 Dec 2025 00:50:01 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bb148ea8fbe93dd8097d85f9ee3cf547d314e669748b4239c05711b0d5f719`  
		Last Modified: Thu, 18 Dec 2025 00:50:02 GMT  
		Size: 102.7 KB (102652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6549359cda37ac41cf41a5ece5f37f1322a82f6b232f12e446c62840637093e`  
		Last Modified: Thu, 18 Dec 2025 00:50:02 GMT  
		Size: 1.9 MB (1939215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041e37eaffefcfb0809564ddea591be3cd818de5530e2c853c0bc9a2fa25c116`  
		Last Modified: Thu, 18 Dec 2025 00:50:05 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7907ae218c75b36c9a9002be8554131c271cde78b0280cb7a85029f99ad0bcdc`  
		Last Modified: Thu, 18 Dec 2025 00:50:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:a9c26fc290551b691574e093d3c28f4fe7b558b3f8173b3c99eb8a664c83a8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ca65d7156e6586d96310ea3162facd9849d5460d2939b461a25247b06a4d59`

```dockerfile
```

-	Layers:
	-	`sha256:d9c217dc241f1175812c47b6489d325a0574c0da554c6f8aa0b86a2d8aff05f9`  
		Last Modified: Thu, 18 Dec 2025 01:34:52 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:cee00a47bf7b8b5899a6cf1f5c692494df31b454f52b81f3c4886905a0c9bdd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91d78dbe118f2b7b0d6e850e1115de72c4fe3e30c55a5b53d8a844d14357d16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:56 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:30:57 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:33:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:33:51 GMT
USER memcache
# Thu, 18 Dec 2025 00:33:51 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:33:51 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa22c446792763e48f4680945ccc68d43c7906ef35a92e0b908f57ef53e72f0`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954155078f2265364295ebdf16fb114e991b1938d8a6951fb511163ab3b2b385`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 92.4 KB (92378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a25584b03ac5e45c66c3c616acfd9df1848e5db25219ef20feb2868c30c6332`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 1.9 MB (1897191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f237be962bb57c3f749904b5925c8e1d7e9013dfac7dd52cc9611ada81858e`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b07d9170b246a631c262d9f5d57f49278f7cd4805463b90b14aeca4dc61d93`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:64abe011fed6a9cf7b3290c752c50bffe81bb2e65cf6337e023efda87d49b451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b251b9c15ab7c5742bd3ab725df09f0ecb9f2491f92cf1c825bec598a31f4407`

```dockerfile
```

-	Layers:
	-	`sha256:1882c6d4361100a29fd5ab265587f65fa27b1df15e7f9349b30dac454facf98e`  
		Last Modified: Thu, 18 Dec 2025 01:34:55 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf0a88ab3838de6beab653497ab62a64cfb87b1dc83c5fa5b6f3907abfd88080`  
		Last Modified: Thu, 18 Dec 2025 01:34:56 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b6c3042e2bf09ec3d3f054d03b81313e8df717a49371ce916ff743e602796bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6285509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6691028570bbd843e6da26558c46162b8383212fcaaefcecb2d3f919e3401429`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:19 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:06 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:06 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb7b8445facedfc145b9478f74880f520776460f153005b7f437ec339aee530`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1853c901134389608b6e80aaa3e43cd67a35c71aecfdde4b5b7ed3b989a03c`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 121.9 KB (121860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a01d1ac5ce47f4494363e411e1cd25dea26438213a2d18d6bb104d0974d9a52`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 2.0 MB (1966561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115624f24ba74d393c2da3d65ed5b35a7afb3fa9ad143d3fb82c64953b3d0401`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87bba524314294ca97195ce65a35ec6d42d3f9f18c9cc0c05c064c9a3cf85c0`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2feda8921a7d67cd9f2f3d7186ed69ceb0d3c22af7a20bd230664e9bcf39096c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73c6548a24cc8ce7782d03377e89a4b4b0e4c2a48cd3a03a79193320fc4d834`

```dockerfile
```

-	Layers:
	-	`sha256:984e438122735983bf56bc3d638fb1b0baf8cfb26ce26f71e0a9b847d25f76b5`  
		Last Modified: Thu, 18 Dec 2025 01:34:59 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d6e8d91ca57b45f0050ec3833a8f09a7ce62f7ba9ec70e1ae12881ad4b2bb6f`  
		Last Modified: Thu, 18 Dec 2025 01:35:00 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine` - linux; 386

```console
$ docker pull memcached@sha256:df1ba8af73cd6e3f8227557b097cd6b128ec0d410a3bbe7a2c282089c5641b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5740953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78dbfc1f8ea65ad6466795e278180963d4afe98dfbca4a4497bc73c99f07ed4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:43 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:44 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:29 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:29 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37ec5bf455c1d98d22e6f3dacb5b971dac8ea96d1fe9b9177a07c5277530646`  
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b2862af05c1582c8625c82ea0863dc2b6474e410d3e6a32876c920e0152c73`  
		Last Modified: Thu, 18 Dec 2025 00:32:42 GMT  
		Size: 110.7 KB (110740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30872a43f6c591fd9b979b49b0fb32107b4bfa8c1155657fa255aa199cf0b83b`  
		Last Modified: Thu, 18 Dec 2025 00:32:42 GMT  
		Size: 1.9 MB (1942762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a62c11b4aeceaba2e5e73a1bc29aa8b4fc42ccd0c7e8512cc11b96e48aef2f`  
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f553d362a11992264bf5364cfe13d248403c5baf2ecac784c26f444dbfb90388`  
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:e3b020c2afd9ae372e234c6ab67456908861fd24200448fd3cf741503a8a6f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abfcddfb1575f6cc07e51c6a379141589de7ea8c329a9bc5c1592f3186e6fda`

```dockerfile
```

-	Layers:
	-	`sha256:ff9be8ef1bab92275eb15ae5fd6a05e767abc1fe855455766200b3c0a1866e33`  
		Last Modified: Thu, 18 Dec 2025 01:35:03 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d7026bdf84e278b6976f0ccab2297ddc0284cf329414f56d12608dbc2acb940`  
		Last Modified: Thu, 18 Dec 2025 01:35:04 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:7292c7b145e08f87f78644bf2c3355fad1d0b4d9366f173ffa0634c3ec93addf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6031729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae72ba97ecea986f01bda1eb392aee1ded4b5a86b2edcabe92a2034143e155b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:33:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:33:42 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:36:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:36:14 GMT
USER memcache
# Thu, 18 Dec 2025 00:36:14 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:36:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c95450233dfe3e06529eb39ca4b46e6ad51ccf338cab64157669ff1fc0a8d72`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4079a2d61bafcf146b8f57b35f0e39bf2548e0963be10cff5086f9a56ccdd9d`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 126.3 KB (126257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f69efa1066815d67cf415d0aac5dcd305032257b6bded5a4c57a7444a1e7fd4`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 2.1 MB (2076363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357f4165f53a3d4c66ef270bcb5b5283a066af50f79924cccc7c73f6a4f6f4ab`  
		Last Modified: Thu, 18 Dec 2025 00:36:36 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a65ff5cefcbfc874c1cac0857339eaee0b07147dd26b6bfa18c00921b4f30c`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:1d06281345f2ac44a607d40d5e87de6abb99bbc6ee82d319e73f3794602d0282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4867a5aa08041c7e5ec69dfc84214226a7323d1ce703747ae2117675e2f74bcd`

```dockerfile
```

-	Layers:
	-	`sha256:282960f007d3f1f008333191d98a2ded5ff0f83075ace30043349b6c082c18fd`  
		Last Modified: Thu, 18 Dec 2025 01:35:08 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4755fffd5924e8405adfbed0f328ad9792eff20e2b8ad2025e1f5c85bca88618`  
		Last Modified: Thu, 18 Dec 2025 01:35:09 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:e011484878fd5d1e2da6de478ac11d01ae80f0bdef1902dcde3ed53728803741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5857090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689ea71c305b80e206c68a215481290a1378e6375e32ad059455f7d041396aa6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:26 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:30:27 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:33:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:33:46 GMT
USER memcache
# Thu, 18 Dec 2025 00:33:46 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:33:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4594a6826f7ed03c8c4f9f2aebb9716eb6e16d5b5ab7e1bc247783b503c5b10`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f270744f8d8b82bc6657387109b33836a76d6dbf8faa645a997db7ea290cdb`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 114.3 KB (114299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91f8ee8f36703944a7bdcaf57cc5772fe9f79c74a088c33fa1b6da7de119f93`  
		Last Modified: Thu, 18 Dec 2025 00:34:02 GMT  
		Size: 2.0 MB (2017131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21d2db88668745770273c7b36d4d2c1e87a80b0118b8d775813860b467384c8`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd847159e169b898a67d4454fd5a22406c5ae623b16889d084a1d5f2d46a499`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:33ab737cb23dcde22de59a58e40f1f80d2c5e808ff3036519ae7d9db228fa37d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3562f7fd7806da24b1865c01a2246ac041b5e98d69c10ce6cbbe479f9408f9a1`

```dockerfile
```

-	Layers:
	-	`sha256:d5f43e64a79ee525bd0354a06e3284444fd642bbe6c1a782aa45ec2e20462f1d`  
		Last Modified: Thu, 18 Dec 2025 01:35:19 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bd2c024010f4f53d350bde9967c349efb3a58a2a812b14e17b29ddbd19eab87`  
		Last Modified: Thu, 18 Dec 2025 01:35:20 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.40-alpine3.23`

```console
$ docker pull memcached@sha256:7c4b90ed70984e92d9b6a6fb5fdfe66eafb466fd40e93cb6994959cfeb4b6a24
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `memcached:1.6.40-alpine3.23` - linux; amd64

```console
$ docker pull memcached@sha256:9573a2399011fa86bb7b5d12bdab987d7931c98ddec0ef6802de7eb6d3c3e338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5956768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c79853acc5f24e9c28f15d45cef0aedc114e76bbacf7958eb6f555c22246e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:34 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:34 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:07 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:07 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:07 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c33ac8581cd04f31208409f36331e938a78e6ae3a7a3b530fe9dfebe6eb9ad`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583aae99135b9036c602a1c60743fc4fd519f261ac6d48ed60b01e1beb019e7f`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 106.0 KB (106050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ca22885c42a537f033850e8dff7eaeddbb7514902286739b48c084b55a8d6b`  
		Last Modified: Thu, 18 Dec 2025 00:32:19 GMT  
		Size: 2.0 MB (1989265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d146e2038834770bed57033a6c5d66ead5b731b8b133856dec6726ca21baee9`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c66e6c3acbe07806e3e96a97d97a2d4503713c4814d9b24a2f57f2c39200d05`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:cfdf2ea6bf2a04bb7ee1568efe0c8bd38a1f5e644250a9409479cce281891ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de792623281192b3965fdc95f31532c4d166e731f53e202be1e2a224c654633b`

```dockerfile
```

-	Layers:
	-	`sha256:87a0d23eeeda6353dfc603cc4ffee062e5383be07b611754f3a88db3fc644036`  
		Last Modified: Thu, 18 Dec 2025 01:34:48 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b73cd5efe31baa1fbf0eecea269426edcfc795cbb9b5dd74b523ff51b6f7c9f`  
		Last Modified: Thu, 18 Dec 2025 01:34:48 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine3.23` - linux; arm variant v6

```console
$ docker pull memcached@sha256:c1a12b64cc8b47f50ea4610d9c1c362da7157b3ba67deac8b4760e6b589cde75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5611647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3591f95cad049a0509bd23a95556f8f848452d2a5491ed00bae293897c7a6b2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:27:48 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:27:49 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:49:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:49:50 GMT
USER memcache
# Thu, 18 Dec 2025 00:49:50 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:49:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf585eb2bfa372c2097b9f7a5214ecb0941a30581b10fb74a26518fcc7addec`  
		Last Modified: Thu, 18 Dec 2025 00:50:01 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bb148ea8fbe93dd8097d85f9ee3cf547d314e669748b4239c05711b0d5f719`  
		Last Modified: Thu, 18 Dec 2025 00:50:02 GMT  
		Size: 102.7 KB (102652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6549359cda37ac41cf41a5ece5f37f1322a82f6b232f12e446c62840637093e`  
		Last Modified: Thu, 18 Dec 2025 00:50:02 GMT  
		Size: 1.9 MB (1939215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041e37eaffefcfb0809564ddea591be3cd818de5530e2c853c0bc9a2fa25c116`  
		Last Modified: Thu, 18 Dec 2025 00:50:05 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7907ae218c75b36c9a9002be8554131c271cde78b0280cb7a85029f99ad0bcdc`  
		Last Modified: Thu, 18 Dec 2025 00:50:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:a9c26fc290551b691574e093d3c28f4fe7b558b3f8173b3c99eb8a664c83a8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ca65d7156e6586d96310ea3162facd9849d5460d2939b461a25247b06a4d59`

```dockerfile
```

-	Layers:
	-	`sha256:d9c217dc241f1175812c47b6489d325a0574c0da554c6f8aa0b86a2d8aff05f9`  
		Last Modified: Thu, 18 Dec 2025 01:34:52 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine3.23` - linux; arm variant v7

```console
$ docker pull memcached@sha256:cee00a47bf7b8b5899a6cf1f5c692494df31b454f52b81f3c4886905a0c9bdd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91d78dbe118f2b7b0d6e850e1115de72c4fe3e30c55a5b53d8a844d14357d16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:56 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:30:57 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:33:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:33:51 GMT
USER memcache
# Thu, 18 Dec 2025 00:33:51 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:33:51 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa22c446792763e48f4680945ccc68d43c7906ef35a92e0b908f57ef53e72f0`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954155078f2265364295ebdf16fb114e991b1938d8a6951fb511163ab3b2b385`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 92.4 KB (92378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a25584b03ac5e45c66c3c616acfd9df1848e5db25219ef20feb2868c30c6332`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 1.9 MB (1897191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f237be962bb57c3f749904b5925c8e1d7e9013dfac7dd52cc9611ada81858e`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b07d9170b246a631c262d9f5d57f49278f7cd4805463b90b14aeca4dc61d93`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:64abe011fed6a9cf7b3290c752c50bffe81bb2e65cf6337e023efda87d49b451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b251b9c15ab7c5742bd3ab725df09f0ecb9f2491f92cf1c825bec598a31f4407`

```dockerfile
```

-	Layers:
	-	`sha256:1882c6d4361100a29fd5ab265587f65fa27b1df15e7f9349b30dac454facf98e`  
		Last Modified: Thu, 18 Dec 2025 01:34:55 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf0a88ab3838de6beab653497ab62a64cfb87b1dc83c5fa5b6f3907abfd88080`  
		Last Modified: Thu, 18 Dec 2025 01:34:56 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b6c3042e2bf09ec3d3f054d03b81313e8df717a49371ce916ff743e602796bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6285509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6691028570bbd843e6da26558c46162b8383212fcaaefcecb2d3f919e3401429`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:19 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:06 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:06 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb7b8445facedfc145b9478f74880f520776460f153005b7f437ec339aee530`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1853c901134389608b6e80aaa3e43cd67a35c71aecfdde4b5b7ed3b989a03c`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 121.9 KB (121860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a01d1ac5ce47f4494363e411e1cd25dea26438213a2d18d6bb104d0974d9a52`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 2.0 MB (1966561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115624f24ba74d393c2da3d65ed5b35a7afb3fa9ad143d3fb82c64953b3d0401`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87bba524314294ca97195ce65a35ec6d42d3f9f18c9cc0c05c064c9a3cf85c0`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:2feda8921a7d67cd9f2f3d7186ed69ceb0d3c22af7a20bd230664e9bcf39096c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73c6548a24cc8ce7782d03377e89a4b4b0e4c2a48cd3a03a79193320fc4d834`

```dockerfile
```

-	Layers:
	-	`sha256:984e438122735983bf56bc3d638fb1b0baf8cfb26ce26f71e0a9b847d25f76b5`  
		Last Modified: Thu, 18 Dec 2025 01:34:59 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d6e8d91ca57b45f0050ec3833a8f09a7ce62f7ba9ec70e1ae12881ad4b2bb6f`  
		Last Modified: Thu, 18 Dec 2025 01:35:00 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine3.23` - linux; 386

```console
$ docker pull memcached@sha256:df1ba8af73cd6e3f8227557b097cd6b128ec0d410a3bbe7a2c282089c5641b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5740953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78dbfc1f8ea65ad6466795e278180963d4afe98dfbca4a4497bc73c99f07ed4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:43 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:44 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:29 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:29 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37ec5bf455c1d98d22e6f3dacb5b971dac8ea96d1fe9b9177a07c5277530646`  
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b2862af05c1582c8625c82ea0863dc2b6474e410d3e6a32876c920e0152c73`  
		Last Modified: Thu, 18 Dec 2025 00:32:42 GMT  
		Size: 110.7 KB (110740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30872a43f6c591fd9b979b49b0fb32107b4bfa8c1155657fa255aa199cf0b83b`  
		Last Modified: Thu, 18 Dec 2025 00:32:42 GMT  
		Size: 1.9 MB (1942762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a62c11b4aeceaba2e5e73a1bc29aa8b4fc42ccd0c7e8512cc11b96e48aef2f`  
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f553d362a11992264bf5364cfe13d248403c5baf2ecac784c26f444dbfb90388`  
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:e3b020c2afd9ae372e234c6ab67456908861fd24200448fd3cf741503a8a6f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abfcddfb1575f6cc07e51c6a379141589de7ea8c329a9bc5c1592f3186e6fda`

```dockerfile
```

-	Layers:
	-	`sha256:ff9be8ef1bab92275eb15ae5fd6a05e767abc1fe855455766200b3c0a1866e33`  
		Last Modified: Thu, 18 Dec 2025 01:35:03 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d7026bdf84e278b6976f0ccab2297ddc0284cf329414f56d12608dbc2acb940`  
		Last Modified: Thu, 18 Dec 2025 01:35:04 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine3.23` - linux; ppc64le

```console
$ docker pull memcached@sha256:7292c7b145e08f87f78644bf2c3355fad1d0b4d9366f173ffa0634c3ec93addf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6031729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae72ba97ecea986f01bda1eb392aee1ded4b5a86b2edcabe92a2034143e155b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:33:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:33:42 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:36:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:36:14 GMT
USER memcache
# Thu, 18 Dec 2025 00:36:14 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:36:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c95450233dfe3e06529eb39ca4b46e6ad51ccf338cab64157669ff1fc0a8d72`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4079a2d61bafcf146b8f57b35f0e39bf2548e0963be10cff5086f9a56ccdd9d`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 126.3 KB (126257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f69efa1066815d67cf415d0aac5dcd305032257b6bded5a4c57a7444a1e7fd4`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 2.1 MB (2076363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357f4165f53a3d4c66ef270bcb5b5283a066af50f79924cccc7c73f6a4f6f4ab`  
		Last Modified: Thu, 18 Dec 2025 00:36:36 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a65ff5cefcbfc874c1cac0857339eaee0b07147dd26b6bfa18c00921b4f30c`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:1d06281345f2ac44a607d40d5e87de6abb99bbc6ee82d319e73f3794602d0282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4867a5aa08041c7e5ec69dfc84214226a7323d1ce703747ae2117675e2f74bcd`

```dockerfile
```

-	Layers:
	-	`sha256:282960f007d3f1f008333191d98a2ded5ff0f83075ace30043349b6c082c18fd`  
		Last Modified: Thu, 18 Dec 2025 01:35:08 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4755fffd5924e8405adfbed0f328ad9792eff20e2b8ad2025e1f5c85bca88618`  
		Last Modified: Thu, 18 Dec 2025 01:35:09 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine3.23` - linux; s390x

```console
$ docker pull memcached@sha256:e011484878fd5d1e2da6de478ac11d01ae80f0bdef1902dcde3ed53728803741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5857090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689ea71c305b80e206c68a215481290a1378e6375e32ad059455f7d041396aa6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:26 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:30:27 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:33:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:33:46 GMT
USER memcache
# Thu, 18 Dec 2025 00:33:46 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:33:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4594a6826f7ed03c8c4f9f2aebb9716eb6e16d5b5ab7e1bc247783b503c5b10`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f270744f8d8b82bc6657387109b33836a76d6dbf8faa645a997db7ea290cdb`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 114.3 KB (114299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91f8ee8f36703944a7bdcaf57cc5772fe9f79c74a088c33fa1b6da7de119f93`  
		Last Modified: Thu, 18 Dec 2025 00:34:02 GMT  
		Size: 2.0 MB (2017131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21d2db88668745770273c7b36d4d2c1e87a80b0118b8d775813860b467384c8`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd847159e169b898a67d4454fd5a22406c5ae623b16889d084a1d5f2d46a499`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:33ab737cb23dcde22de59a58e40f1f80d2c5e808ff3036519ae7d9db228fa37d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3562f7fd7806da24b1865c01a2246ac041b5e98d69c10ce6cbbe479f9408f9a1`

```dockerfile
```

-	Layers:
	-	`sha256:d5f43e64a79ee525bd0354a06e3284444fd642bbe6c1a782aa45ec2e20462f1d`  
		Last Modified: Thu, 18 Dec 2025 01:35:19 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bd2c024010f4f53d350bde9967c349efb3a58a2a812b14e17b29ddbd19eab87`  
		Last Modified: Thu, 18 Dec 2025 01:35:20 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.40-trixie`

```console
$ docker pull memcached@sha256:9ae868852d0bc0974e4dd39c58436f73698081a31e61b8099871983e09d79f80
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

### `memcached:1.6.40-trixie` - linux; amd64

```console
$ docker pull memcached@sha256:c9046d2a0ade04c91892254044294c2a529006458cd7b98bdc31b4054fffbfe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32193341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6654931990345ba058b2f50cedc8d03dfcc174d6809b0e7a820c12f7b93dc09d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:35:37 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:23 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:23 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:23 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:23 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:23 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b6bc7772cb8044287682c4af75ca1c8280c4837d5ffee58adc014018f02e91`  
		Last Modified: Wed, 17 Dec 2025 21:38:42 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3af321fdb36bbbb634d6be4a6e457f7eeb47b153460c7bab6c9eae91724b08b`  
		Last Modified: Wed, 17 Dec 2025 21:38:42 GMT  
		Size: 136.7 KB (136691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a00f7c8e317ad005bdf0117005dd753e347a8674b068c660bbc29b3f93a0621`  
		Last Modified: Wed, 17 Dec 2025 21:38:42 GMT  
		Size: 2.3 MB (2278641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb739034830ce246e4bc00aa883c7d2af8a1fd59bc3e2ea17cae3607bf281074`  
		Last Modified: Wed, 17 Dec 2025 21:38:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33cfbae525009776fcee65339602ed1b2a8a5f2c51898ec9fc499fe35c60b87`  
		Last Modified: Wed, 17 Dec 2025 21:38:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:e726a4ddf8221754a6a9fa1143cee47f51785aedb20dc0329a7c7b41b4772763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd3f16921a7fcccc9bc6ee3685e192e34a0b621f1c95362d6cea5e4293e54d33`

```dockerfile
```

-	Layers:
	-	`sha256:3a55af39eac38dca280008ae509d726055b1dde6e05ce9024174d0a0bd0565c2`  
		Last Modified: Wed, 17 Dec 2025 22:34:37 GMT  
		Size: 2.0 MB (2008228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef418f126bca0d267c3b365faed9990a104832e94e7ec35841aff2c2b26510dc`  
		Last Modified: Wed, 17 Dec 2025 22:34:38 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:c1a14cf6b3aa6f9ee13feee1c176a4ff104ec3d361f2df684e87a9d88a563eaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30300251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7375c421f8c059114c1a5cdc58215c8cf41dcc23355cbef325fdfa4b290df1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:39:00 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:39:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:42:24 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:42:24 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:42:24 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:42:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:42:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:42:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:42:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:42:24 GMT
USER memcache
# Wed, 17 Dec 2025 21:42:24 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:42:24 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d97bc71d0fa535127863fdab265dfddb07b3cda35b80de4dd2b9b67fe154c856`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 27.9 MB (27944187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e168dbb57c754690bc257f600efb5085929be35091c7e3d6926d35490c3391`  
		Last Modified: Wed, 17 Dec 2025 21:42:38 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78870a4506eecc7b424a3cedde90baa4c44a7c5d1174e6842b60c11b08a7984e`  
		Last Modified: Wed, 17 Dec 2025 21:42:40 GMT  
		Size: 144.2 KB (144157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e35d5393bf24a4f7ba0c87d734e7fda2d09414dec61e9139726200bed52e262`  
		Last Modified: Wed, 17 Dec 2025 21:42:39 GMT  
		Size: 2.2 MB (2210395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72c9d61ca04e663f67ab23ad2c50afcd810d29c2f52728277947d5ab78c03da`  
		Last Modified: Wed, 17 Dec 2025 21:42:38 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e89f91fff1d699acc4ebbc8ebb2a409d5f7867914100e87affef7b7d8775488`  
		Last Modified: Wed, 17 Dec 2025 21:42:38 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:3a82f6da1fa8b6c43220785849304c0e09363556371c8f763abae2126e271c5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e59d44e1c5460c7338a49dad6ec9d6d03db5b9330bb235c1d01e3e182df704ca`

```dockerfile
```

-	Layers:
	-	`sha256:2b38edaa9de8bf0d9055274c5ca1c0af276da0f57396ee1edfb8db1002dc8834`  
		Last Modified: Wed, 17 Dec 2025 22:34:42 GMT  
		Size: 2.0 MB (2011231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c70377fb854a2602cbb12ee80dd69f8a5deb00e23feb0c3c24e1b27806029b0d`  
		Last Modified: Wed, 17 Dec 2025 22:34:43 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:b7ad53cb1e5a5631cc9b08d0fe984b0ba6bb7ab77da4309a552dbb97bd4ae04e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28510860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b2fbe25ebf8c8035604591c6ded5acfffe219c97c853c1c0e00421ac18abcd4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:35:20 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:30 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:30 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:30 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:30 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:30 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:30 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d46de1cc714aa644c02bc1b184e957b7330bf3473d4e97f72f454fdc8a432d`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0327c8719a60b04c8b690d8d0a0a122cdbc620f2aab391fd43789a8803b62bf1`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 135.4 KB (135362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd55327cbd82c4adf176e679bae5436e8aaf27c54595ec2cd7cfec20989b1fc`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 2.2 MB (2163972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37babf40b7b24af06cfbfc9fe6daf7d6f5863de148318182eecf29e242ba5e4c`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3daf0d6e9f1032a9bce2c34a57a6049ec4ffd4a412a20724540653fe7b6526d3`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:77b0259560abd3025ae0593b06db95eb3c4dd6dccbd2332f85286fae97d799bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd1267e1c8eb093b3e5a265d3c2d0c9b2b3784e50b6aa7edfec29ba838d4a8c`

```dockerfile
```

-	Layers:
	-	`sha256:3266292cf75a57aab22a4e279bf40458841e617570f3ee192bb26dc1d2d6e1ef`  
		Last Modified: Wed, 17 Dec 2025 22:34:47 GMT  
		Size: 2.0 MB (2009688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cc2be86d85bc478731bb7718f18d50da352f58c942412f66ca371226633d3bb`  
		Last Modified: Wed, 17 Dec 2025 22:34:48 GMT  
		Size: 22.3 KB (22303 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:230a135d43b1bf876ec5c160b78cb4f0303d1e6e98dc76a31dd524d28a4a5279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32554912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79214d48c3616d6c032db23eb36a6766c7a96a8d4619d8f8791d2fa43163cc34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:35:24 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:26 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:26 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:26 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:26 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:26 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:26 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f49eb557c72f2fe7e0eb1949c1587e8e4c86bdae514d70fac3ff429290a149`  
		Last Modified: Wed, 17 Dec 2025 21:38:46 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f764f8f3ed63ac8e640ebdcb2f5ea0371b6fb244a1f6defbe51ddfff908a34a`  
		Last Modified: Wed, 17 Dec 2025 21:38:46 GMT  
		Size: 153.5 KB (153477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9353d672d9aeb0b8a3ee269d120b0b920e9f6b81998ed7ef7765092573e4b716`  
		Last Modified: Wed, 17 Dec 2025 21:38:46 GMT  
		Size: 2.3 MB (2261292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ba4d16dc49a02e1490d18a58f5e108ec18a248f9ea83bb7b4deb8642b36f90`  
		Last Modified: Wed, 17 Dec 2025 21:38:46 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d15340fcbda1a05a50ba392408ace29b5cbb21b398bb1018750621349d3b0a`  
		Last Modified: Wed, 17 Dec 2025 21:38:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:d2a465ef21f85d63f634e52f05c50319a05c013d1aeed6321cc146b3a28a5920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c092dec716fd21afebb19ce5e88ba467a0f4bb88a40068e3e266b1f10ff6652`

```dockerfile
```

-	Layers:
	-	`sha256:b7bd1c3aaf184ba5d6dfbf328c24c2f39511de9c6e21c04b7fa212d6a26b0049`  
		Last Modified: Wed, 17 Dec 2025 22:34:53 GMT  
		Size: 2.0 MB (2008544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc6165d17a79a40bba13d288c74c5c34aa4af72304a300a74ceededf1a934bbc`  
		Last Modified: Wed, 17 Dec 2025 22:34:54 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-trixie` - linux; 386

```console
$ docker pull memcached@sha256:35df20cb1713a9d5fbb1820acac102f3c3560dfa2d0fa147fff30dfc53f209bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33665704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ccada050045e330c6b125cae2adfcf8e5edb8e23b5e044c0d53861f7762294a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:35:51 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:43 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:43 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:43 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:43 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:43 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b054f6842adaecae2d5cf75c99601b690566759a58606bc981ccae49baaae51`  
		Last Modified: Wed, 17 Dec 2025 21:38:57 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43efb4f909536827644b2ca98420204710b14f6195238a8ffdbf658c29883be`  
		Last Modified: Wed, 17 Dec 2025 21:38:57 GMT  
		Size: 147.5 KB (147519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:792eb292285447291b91c55e07bc1a75b3d4e125a3c23f80671848c5f967e042`  
		Last Modified: Wed, 17 Dec 2025 21:38:57 GMT  
		Size: 2.2 MB (2223600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe79378953d034686129f0d36718bb867ebebf130cd1f431ad68cf117a1308c6`  
		Last Modified: Wed, 17 Dec 2025 21:38:57 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92088f114f464c2f2e1217404e900d24a46a03305faa6cae793f0b873cadba52`  
		Last Modified: Wed, 17 Dec 2025 21:38:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:3a428e326360172543ee458a46a55c1b9e70d3eeeea945f2ed65839c307eddd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a62b1d6c9ce3819b6b67f9de9cc436a2f4cb362fad3a8c07627fd790e4bd8be7`

```dockerfile
```

-	Layers:
	-	`sha256:0f8e75010a0e7df5356c9c36b97dff2c5d2191f6f6e643619b4363f8c1e1dc42`  
		Last Modified: Wed, 17 Dec 2025 22:34:58 GMT  
		Size: 2.0 MB (2005385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98883c6827ebd9ca960545767f09a2be89e7580fc425e24f86364f3a9e4ea283`  
		Last Modified: Wed, 17 Dec 2025 22:34:59 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:38a236f83eb206f786b39c53e8f756815f0bda1460157b11844faf21735208bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36162589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41292f5c75fe5f3a464b809bde41e0ae8849ad8d7046918a548d0c6b2e250a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:34:54 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:28 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:28 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:28 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2b42546c7b688160cfd1a0da61a24922a019b4ebead88e23aff01482ddd477`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4efe9fd2e012174cd86a64f83d7b7facfe14ee67c9c9fa5ce994f22c24173f2c`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 170.4 KB (170393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9752985ba696f0f8d5831ac91e19bfe336342b1c403542641c575b1dc6116e`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 2.4 MB (2393786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d11c68ba0bc913d139eea51cb2957c1ddd713515fc06dfa5d4c398b119535a`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9186b8b7184cef442ae3ed6a3feadcaa8f4ccc974ed5ae6c6cf8efe37e679f23`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:00d1019e9978171df76f638253f212405bf7d53251607ef5a5933d5b28d867b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588d3d6ab54a9ea5c8baf9b013bb23c12826989ba0d09cb862431e2fa30e5189`

```dockerfile
```

-	Layers:
	-	`sha256:799ad025578a6d5d0155dc5be223bfbc25ffa3aa0548e4fb2e4bedeb0a5088d9`  
		Last Modified: Wed, 17 Dec 2025 22:35:03 GMT  
		Size: 2.0 MB (2011829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaa03114ccb63fbbd8ca04eef46baa26c8a0508f1256aa45d851f3a49f2ed47a`  
		Last Modified: Wed, 17 Dec 2025 22:35:04 GMT  
		Size: 22.2 KB (22225 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:5aedcd2b04ff2d8dc77fb6568e6ce96878f75508a3a01326623b60869874f8a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30615184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab5d9dd83f52434969fb6da016bd60451fd5d989e33e2cd491533dcb4553c835`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 05:30:55 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 09 Dec 2025 05:31:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Dec 2025 03:19:32 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 03:19:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 03:19:32 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 03:19:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 18 Dec 2025 03:19:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 03:19:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 03:19:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 03:19:33 GMT
USER memcache
# Thu, 18 Dec 2025 03:19:33 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 03:19:33 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb23364b88c4686dab6a11bf004aac89beea8adb8559fd39799a54dc729c23a6`  
		Last Modified: Tue, 09 Dec 2025 05:57:38 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edeeae49e27528d2079d0d5aeb702d7dd56503463fa4054ee2444f847f399650`  
		Last Modified: Tue, 09 Dec 2025 05:57:38 GMT  
		Size: 133.1 KB (133076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e584b688c99191b71a2471afe63daff415a1eedcf541b959dfcdf248eebd8577`  
		Last Modified: Thu, 18 Dec 2025 03:20:28 GMT  
		Size: 2.2 MB (2207438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b780b2b80274922cc63f0afe1ecd2680bcafae3234732fd03ba740690e3ebf1`  
		Last Modified: Thu, 18 Dec 2025 03:20:28 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5449346fa21339be4109a2e289721bfa7b0e8203b88fe202956ebb257c703a88`  
		Last Modified: Thu, 18 Dec 2025 03:20:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:bbe7bbb4c3590b1fc9c5943719d3b1b2a21670d2874ed90415040aeae5b13200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c721ad9798565707f4e9e537a1618b5efafce47c49577053fe7b40879caca9`

```dockerfile
```

-	Layers:
	-	`sha256:37125be6342f13dcb1fff2b0c3def6d6f3b808e19192f9ff68a139ce2d1d3083`  
		Last Modified: Thu, 18 Dec 2025 04:34:34 GMT  
		Size: 2.0 MB (2002192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06edc085828555adcb8aac4ef4e564c72d260338e77dde6abe811eefcdd8682d`  
		Last Modified: Thu, 18 Dec 2025 04:34:35 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:1e7fc2740e66d7d7b21982f73ae72e901616fcb9ebc6176c6f1d931c6a4732b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32273737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f632195b7b4a10526fcb27d2d66a479b07455d784656340bcbae2d31e292aa2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:34:51 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:34:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:04 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:04 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:04 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:04 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:04 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:04 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9606e3e114197b678b6fbd5b889ab574d2ad4cd8b4010407f847a98309f0f6b`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24f23dd2596713c0a8daf1cde9aabc7d26e7e9b832300ba1ce4615e8c806afc`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 140.5 KB (140507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0dd33ff71e256560cf1693538e8ecc4f92550f6483c1478697b822abf8d0f84`  
		Last Modified: Wed, 17 Dec 2025 21:38:19 GMT  
		Size: 2.3 MB (2297315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568ee6e9ecd99ef323ff6ff6b40b5fcf91b13472f56ac46f8b3036c82c705fd6`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91a63e3e27d493e5ad7b64edf0b8ae2bb8ade89a55bfc197b4dc9a393ceec4b`  
		Last Modified: Wed, 17 Dec 2025 21:38:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:d9aa5142dc8acd96ae2fb7235ceda06498adc21053e1bc5bf02ff76701213426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e87c93018f4f94a4286dcf6f6d33373729ef4263208b2f346e92a2028839a2`

```dockerfile
```

-	Layers:
	-	`sha256:c0ee3f2287a538730e473aea557f8fc2a48d18bb9e778e65ccdbf8918310ace3`  
		Last Modified: Wed, 17 Dec 2025 22:35:11 GMT  
		Size: 2.0 MB (2009665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce86917337210887b4362390f278a89c9fc6d6d1cc50e29ebf7f716bc556c877`  
		Last Modified: Wed, 17 Dec 2025 22:35:12 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine`

```console
$ docker pull memcached@sha256:6f20032236ee1e3ae7edb0f8a060ce3d8c66cfad7a05fe84cfe88001f70a4eb1
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
$ docker pull memcached@sha256:9573a2399011fa86bb7b5d12bdab987d7931c98ddec0ef6802de7eb6d3c3e338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5956768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c79853acc5f24e9c28f15d45cef0aedc114e76bbacf7958eb6f555c22246e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:34 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:34 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:07 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:07 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:07 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c33ac8581cd04f31208409f36331e938a78e6ae3a7a3b530fe9dfebe6eb9ad`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583aae99135b9036c602a1c60743fc4fd519f261ac6d48ed60b01e1beb019e7f`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 106.0 KB (106050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ca22885c42a537f033850e8dff7eaeddbb7514902286739b48c084b55a8d6b`  
		Last Modified: Thu, 18 Dec 2025 00:32:19 GMT  
		Size: 2.0 MB (1989265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d146e2038834770bed57033a6c5d66ead5b731b8b133856dec6726ca21baee9`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c66e6c3acbe07806e3e96a97d97a2d4503713c4814d9b24a2f57f2c39200d05`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:cfdf2ea6bf2a04bb7ee1568efe0c8bd38a1f5e644250a9409479cce281891ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de792623281192b3965fdc95f31532c4d166e731f53e202be1e2a224c654633b`

```dockerfile
```

-	Layers:
	-	`sha256:87a0d23eeeda6353dfc603cc4ffee062e5383be07b611754f3a88db3fc644036`  
		Last Modified: Thu, 18 Dec 2025 01:34:48 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b73cd5efe31baa1fbf0eecea269426edcfc795cbb9b5dd74b523ff51b6f7c9f`  
		Last Modified: Thu, 18 Dec 2025 01:34:48 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:c1a12b64cc8b47f50ea4610d9c1c362da7157b3ba67deac8b4760e6b589cde75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5611647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3591f95cad049a0509bd23a95556f8f848452d2a5491ed00bae293897c7a6b2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:27:48 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:27:49 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:49:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:49:50 GMT
USER memcache
# Thu, 18 Dec 2025 00:49:50 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:49:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf585eb2bfa372c2097b9f7a5214ecb0941a30581b10fb74a26518fcc7addec`  
		Last Modified: Thu, 18 Dec 2025 00:50:01 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bb148ea8fbe93dd8097d85f9ee3cf547d314e669748b4239c05711b0d5f719`  
		Last Modified: Thu, 18 Dec 2025 00:50:02 GMT  
		Size: 102.7 KB (102652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6549359cda37ac41cf41a5ece5f37f1322a82f6b232f12e446c62840637093e`  
		Last Modified: Thu, 18 Dec 2025 00:50:02 GMT  
		Size: 1.9 MB (1939215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041e37eaffefcfb0809564ddea591be3cd818de5530e2c853c0bc9a2fa25c116`  
		Last Modified: Thu, 18 Dec 2025 00:50:05 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7907ae218c75b36c9a9002be8554131c271cde78b0280cb7a85029f99ad0bcdc`  
		Last Modified: Thu, 18 Dec 2025 00:50:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:a9c26fc290551b691574e093d3c28f4fe7b558b3f8173b3c99eb8a664c83a8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ca65d7156e6586d96310ea3162facd9849d5460d2939b461a25247b06a4d59`

```dockerfile
```

-	Layers:
	-	`sha256:d9c217dc241f1175812c47b6489d325a0574c0da554c6f8aa0b86a2d8aff05f9`  
		Last Modified: Thu, 18 Dec 2025 01:34:52 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:cee00a47bf7b8b5899a6cf1f5c692494df31b454f52b81f3c4886905a0c9bdd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91d78dbe118f2b7b0d6e850e1115de72c4fe3e30c55a5b53d8a844d14357d16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:56 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:30:57 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:33:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:33:51 GMT
USER memcache
# Thu, 18 Dec 2025 00:33:51 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:33:51 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa22c446792763e48f4680945ccc68d43c7906ef35a92e0b908f57ef53e72f0`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954155078f2265364295ebdf16fb114e991b1938d8a6951fb511163ab3b2b385`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 92.4 KB (92378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a25584b03ac5e45c66c3c616acfd9df1848e5db25219ef20feb2868c30c6332`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 1.9 MB (1897191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f237be962bb57c3f749904b5925c8e1d7e9013dfac7dd52cc9611ada81858e`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b07d9170b246a631c262d9f5d57f49278f7cd4805463b90b14aeca4dc61d93`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:64abe011fed6a9cf7b3290c752c50bffe81bb2e65cf6337e023efda87d49b451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b251b9c15ab7c5742bd3ab725df09f0ecb9f2491f92cf1c825bec598a31f4407`

```dockerfile
```

-	Layers:
	-	`sha256:1882c6d4361100a29fd5ab265587f65fa27b1df15e7f9349b30dac454facf98e`  
		Last Modified: Thu, 18 Dec 2025 01:34:55 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf0a88ab3838de6beab653497ab62a64cfb87b1dc83c5fa5b6f3907abfd88080`  
		Last Modified: Thu, 18 Dec 2025 01:34:56 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b6c3042e2bf09ec3d3f054d03b81313e8df717a49371ce916ff743e602796bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6285509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6691028570bbd843e6da26558c46162b8383212fcaaefcecb2d3f919e3401429`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:19 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:06 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:06 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb7b8445facedfc145b9478f74880f520776460f153005b7f437ec339aee530`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1853c901134389608b6e80aaa3e43cd67a35c71aecfdde4b5b7ed3b989a03c`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 121.9 KB (121860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a01d1ac5ce47f4494363e411e1cd25dea26438213a2d18d6bb104d0974d9a52`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 2.0 MB (1966561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115624f24ba74d393c2da3d65ed5b35a7afb3fa9ad143d3fb82c64953b3d0401`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87bba524314294ca97195ce65a35ec6d42d3f9f18c9cc0c05c064c9a3cf85c0`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2feda8921a7d67cd9f2f3d7186ed69ceb0d3c22af7a20bd230664e9bcf39096c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73c6548a24cc8ce7782d03377e89a4b4b0e4c2a48cd3a03a79193320fc4d834`

```dockerfile
```

-	Layers:
	-	`sha256:984e438122735983bf56bc3d638fb1b0baf8cfb26ce26f71e0a9b847d25f76b5`  
		Last Modified: Thu, 18 Dec 2025 01:34:59 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d6e8d91ca57b45f0050ec3833a8f09a7ce62f7ba9ec70e1ae12881ad4b2bb6f`  
		Last Modified: Thu, 18 Dec 2025 01:35:00 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:df1ba8af73cd6e3f8227557b097cd6b128ec0d410a3bbe7a2c282089c5641b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5740953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78dbfc1f8ea65ad6466795e278180963d4afe98dfbca4a4497bc73c99f07ed4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:43 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:44 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:29 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:29 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37ec5bf455c1d98d22e6f3dacb5b971dac8ea96d1fe9b9177a07c5277530646`  
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b2862af05c1582c8625c82ea0863dc2b6474e410d3e6a32876c920e0152c73`  
		Last Modified: Thu, 18 Dec 2025 00:32:42 GMT  
		Size: 110.7 KB (110740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30872a43f6c591fd9b979b49b0fb32107b4bfa8c1155657fa255aa199cf0b83b`  
		Last Modified: Thu, 18 Dec 2025 00:32:42 GMT  
		Size: 1.9 MB (1942762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a62c11b4aeceaba2e5e73a1bc29aa8b4fc42ccd0c7e8512cc11b96e48aef2f`  
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f553d362a11992264bf5364cfe13d248403c5baf2ecac784c26f444dbfb90388`  
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:e3b020c2afd9ae372e234c6ab67456908861fd24200448fd3cf741503a8a6f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abfcddfb1575f6cc07e51c6a379141589de7ea8c329a9bc5c1592f3186e6fda`

```dockerfile
```

-	Layers:
	-	`sha256:ff9be8ef1bab92275eb15ae5fd6a05e767abc1fe855455766200b3c0a1866e33`  
		Last Modified: Thu, 18 Dec 2025 01:35:03 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d7026bdf84e278b6976f0ccab2297ddc0284cf329414f56d12608dbc2acb940`  
		Last Modified: Thu, 18 Dec 2025 01:35:04 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:7292c7b145e08f87f78644bf2c3355fad1d0b4d9366f173ffa0634c3ec93addf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6031729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae72ba97ecea986f01bda1eb392aee1ded4b5a86b2edcabe92a2034143e155b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:33:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:33:42 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:36:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:36:14 GMT
USER memcache
# Thu, 18 Dec 2025 00:36:14 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:36:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c95450233dfe3e06529eb39ca4b46e6ad51ccf338cab64157669ff1fc0a8d72`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4079a2d61bafcf146b8f57b35f0e39bf2548e0963be10cff5086f9a56ccdd9d`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 126.3 KB (126257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f69efa1066815d67cf415d0aac5dcd305032257b6bded5a4c57a7444a1e7fd4`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 2.1 MB (2076363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357f4165f53a3d4c66ef270bcb5b5283a066af50f79924cccc7c73f6a4f6f4ab`  
		Last Modified: Thu, 18 Dec 2025 00:36:36 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a65ff5cefcbfc874c1cac0857339eaee0b07147dd26b6bfa18c00921b4f30c`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:1d06281345f2ac44a607d40d5e87de6abb99bbc6ee82d319e73f3794602d0282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4867a5aa08041c7e5ec69dfc84214226a7323d1ce703747ae2117675e2f74bcd`

```dockerfile
```

-	Layers:
	-	`sha256:282960f007d3f1f008333191d98a2ded5ff0f83075ace30043349b6c082c18fd`  
		Last Modified: Thu, 18 Dec 2025 01:35:08 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4755fffd5924e8405adfbed0f328ad9792eff20e2b8ad2025e1f5c85bca88618`  
		Last Modified: Thu, 18 Dec 2025 01:35:09 GMT  
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
$ docker pull memcached@sha256:e011484878fd5d1e2da6de478ac11d01ae80f0bdef1902dcde3ed53728803741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5857090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689ea71c305b80e206c68a215481290a1378e6375e32ad059455f7d041396aa6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:26 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:30:27 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:33:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:33:46 GMT
USER memcache
# Thu, 18 Dec 2025 00:33:46 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:33:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4594a6826f7ed03c8c4f9f2aebb9716eb6e16d5b5ab7e1bc247783b503c5b10`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f270744f8d8b82bc6657387109b33836a76d6dbf8faa645a997db7ea290cdb`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 114.3 KB (114299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91f8ee8f36703944a7bdcaf57cc5772fe9f79c74a088c33fa1b6da7de119f93`  
		Last Modified: Thu, 18 Dec 2025 00:34:02 GMT  
		Size: 2.0 MB (2017131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21d2db88668745770273c7b36d4d2c1e87a80b0118b8d775813860b467384c8`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd847159e169b898a67d4454fd5a22406c5ae623b16889d084a1d5f2d46a499`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:33ab737cb23dcde22de59a58e40f1f80d2c5e808ff3036519ae7d9db228fa37d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3562f7fd7806da24b1865c01a2246ac041b5e98d69c10ce6cbbe479f9408f9a1`

```dockerfile
```

-	Layers:
	-	`sha256:d5f43e64a79ee525bd0354a06e3284444fd642bbe6c1a782aa45ec2e20462f1d`  
		Last Modified: Thu, 18 Dec 2025 01:35:19 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bd2c024010f4f53d350bde9967c349efb3a58a2a812b14e17b29ddbd19eab87`  
		Last Modified: Thu, 18 Dec 2025 01:35:20 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine3.23`

```console
$ docker pull memcached@sha256:6f20032236ee1e3ae7edb0f8a060ce3d8c66cfad7a05fe84cfe88001f70a4eb1
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
$ docker pull memcached@sha256:9573a2399011fa86bb7b5d12bdab987d7931c98ddec0ef6802de7eb6d3c3e338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5956768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c79853acc5f24e9c28f15d45cef0aedc114e76bbacf7958eb6f555c22246e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:34 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:34 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:07 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:07 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:07 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c33ac8581cd04f31208409f36331e938a78e6ae3a7a3b530fe9dfebe6eb9ad`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583aae99135b9036c602a1c60743fc4fd519f261ac6d48ed60b01e1beb019e7f`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 106.0 KB (106050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ca22885c42a537f033850e8dff7eaeddbb7514902286739b48c084b55a8d6b`  
		Last Modified: Thu, 18 Dec 2025 00:32:19 GMT  
		Size: 2.0 MB (1989265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d146e2038834770bed57033a6c5d66ead5b731b8b133856dec6726ca21baee9`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c66e6c3acbe07806e3e96a97d97a2d4503713c4814d9b24a2f57f2c39200d05`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:cfdf2ea6bf2a04bb7ee1568efe0c8bd38a1f5e644250a9409479cce281891ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de792623281192b3965fdc95f31532c4d166e731f53e202be1e2a224c654633b`

```dockerfile
```

-	Layers:
	-	`sha256:87a0d23eeeda6353dfc603cc4ffee062e5383be07b611754f3a88db3fc644036`  
		Last Modified: Thu, 18 Dec 2025 01:34:48 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b73cd5efe31baa1fbf0eecea269426edcfc795cbb9b5dd74b523ff51b6f7c9f`  
		Last Modified: Thu, 18 Dec 2025 01:34:48 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; arm variant v6

```console
$ docker pull memcached@sha256:c1a12b64cc8b47f50ea4610d9c1c362da7157b3ba67deac8b4760e6b589cde75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5611647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3591f95cad049a0509bd23a95556f8f848452d2a5491ed00bae293897c7a6b2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:27:48 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:27:49 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:49:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:49:50 GMT
USER memcache
# Thu, 18 Dec 2025 00:49:50 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:49:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf585eb2bfa372c2097b9f7a5214ecb0941a30581b10fb74a26518fcc7addec`  
		Last Modified: Thu, 18 Dec 2025 00:50:01 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bb148ea8fbe93dd8097d85f9ee3cf547d314e669748b4239c05711b0d5f719`  
		Last Modified: Thu, 18 Dec 2025 00:50:02 GMT  
		Size: 102.7 KB (102652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6549359cda37ac41cf41a5ece5f37f1322a82f6b232f12e446c62840637093e`  
		Last Modified: Thu, 18 Dec 2025 00:50:02 GMT  
		Size: 1.9 MB (1939215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041e37eaffefcfb0809564ddea591be3cd818de5530e2c853c0bc9a2fa25c116`  
		Last Modified: Thu, 18 Dec 2025 00:50:05 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7907ae218c75b36c9a9002be8554131c271cde78b0280cb7a85029f99ad0bcdc`  
		Last Modified: Thu, 18 Dec 2025 00:50:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:a9c26fc290551b691574e093d3c28f4fe7b558b3f8173b3c99eb8a664c83a8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ca65d7156e6586d96310ea3162facd9849d5460d2939b461a25247b06a4d59`

```dockerfile
```

-	Layers:
	-	`sha256:d9c217dc241f1175812c47b6489d325a0574c0da554c6f8aa0b86a2d8aff05f9`  
		Last Modified: Thu, 18 Dec 2025 01:34:52 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; arm variant v7

```console
$ docker pull memcached@sha256:cee00a47bf7b8b5899a6cf1f5c692494df31b454f52b81f3c4886905a0c9bdd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91d78dbe118f2b7b0d6e850e1115de72c4fe3e30c55a5b53d8a844d14357d16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:56 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:30:57 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:33:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:33:51 GMT
USER memcache
# Thu, 18 Dec 2025 00:33:51 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:33:51 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa22c446792763e48f4680945ccc68d43c7906ef35a92e0b908f57ef53e72f0`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954155078f2265364295ebdf16fb114e991b1938d8a6951fb511163ab3b2b385`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 92.4 KB (92378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a25584b03ac5e45c66c3c616acfd9df1848e5db25219ef20feb2868c30c6332`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 1.9 MB (1897191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f237be962bb57c3f749904b5925c8e1d7e9013dfac7dd52cc9611ada81858e`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b07d9170b246a631c262d9f5d57f49278f7cd4805463b90b14aeca4dc61d93`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:64abe011fed6a9cf7b3290c752c50bffe81bb2e65cf6337e023efda87d49b451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b251b9c15ab7c5742bd3ab725df09f0ecb9f2491f92cf1c825bec598a31f4407`

```dockerfile
```

-	Layers:
	-	`sha256:1882c6d4361100a29fd5ab265587f65fa27b1df15e7f9349b30dac454facf98e`  
		Last Modified: Thu, 18 Dec 2025 01:34:55 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf0a88ab3838de6beab653497ab62a64cfb87b1dc83c5fa5b6f3907abfd88080`  
		Last Modified: Thu, 18 Dec 2025 01:34:56 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b6c3042e2bf09ec3d3f054d03b81313e8df717a49371ce916ff743e602796bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6285509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6691028570bbd843e6da26558c46162b8383212fcaaefcecb2d3f919e3401429`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:19 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:06 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:06 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb7b8445facedfc145b9478f74880f520776460f153005b7f437ec339aee530`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1853c901134389608b6e80aaa3e43cd67a35c71aecfdde4b5b7ed3b989a03c`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 121.9 KB (121860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a01d1ac5ce47f4494363e411e1cd25dea26438213a2d18d6bb104d0974d9a52`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 2.0 MB (1966561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115624f24ba74d393c2da3d65ed5b35a7afb3fa9ad143d3fb82c64953b3d0401`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87bba524314294ca97195ce65a35ec6d42d3f9f18c9cc0c05c064c9a3cf85c0`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:2feda8921a7d67cd9f2f3d7186ed69ceb0d3c22af7a20bd230664e9bcf39096c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73c6548a24cc8ce7782d03377e89a4b4b0e4c2a48cd3a03a79193320fc4d834`

```dockerfile
```

-	Layers:
	-	`sha256:984e438122735983bf56bc3d638fb1b0baf8cfb26ce26f71e0a9b847d25f76b5`  
		Last Modified: Thu, 18 Dec 2025 01:34:59 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d6e8d91ca57b45f0050ec3833a8f09a7ce62f7ba9ec70e1ae12881ad4b2bb6f`  
		Last Modified: Thu, 18 Dec 2025 01:35:00 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; 386

```console
$ docker pull memcached@sha256:df1ba8af73cd6e3f8227557b097cd6b128ec0d410a3bbe7a2c282089c5641b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5740953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78dbfc1f8ea65ad6466795e278180963d4afe98dfbca4a4497bc73c99f07ed4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:43 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:44 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:29 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:29 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37ec5bf455c1d98d22e6f3dacb5b971dac8ea96d1fe9b9177a07c5277530646`  
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b2862af05c1582c8625c82ea0863dc2b6474e410d3e6a32876c920e0152c73`  
		Last Modified: Thu, 18 Dec 2025 00:32:42 GMT  
		Size: 110.7 KB (110740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30872a43f6c591fd9b979b49b0fb32107b4bfa8c1155657fa255aa199cf0b83b`  
		Last Modified: Thu, 18 Dec 2025 00:32:42 GMT  
		Size: 1.9 MB (1942762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a62c11b4aeceaba2e5e73a1bc29aa8b4fc42ccd0c7e8512cc11b96e48aef2f`  
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f553d362a11992264bf5364cfe13d248403c5baf2ecac784c26f444dbfb90388`  
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:e3b020c2afd9ae372e234c6ab67456908861fd24200448fd3cf741503a8a6f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abfcddfb1575f6cc07e51c6a379141589de7ea8c329a9bc5c1592f3186e6fda`

```dockerfile
```

-	Layers:
	-	`sha256:ff9be8ef1bab92275eb15ae5fd6a05e767abc1fe855455766200b3c0a1866e33`  
		Last Modified: Thu, 18 Dec 2025 01:35:03 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d7026bdf84e278b6976f0ccab2297ddc0284cf329414f56d12608dbc2acb940`  
		Last Modified: Thu, 18 Dec 2025 01:35:04 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; ppc64le

```console
$ docker pull memcached@sha256:7292c7b145e08f87f78644bf2c3355fad1d0b4d9366f173ffa0634c3ec93addf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6031729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae72ba97ecea986f01bda1eb392aee1ded4b5a86b2edcabe92a2034143e155b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:33:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:33:42 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:36:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:36:14 GMT
USER memcache
# Thu, 18 Dec 2025 00:36:14 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:36:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c95450233dfe3e06529eb39ca4b46e6ad51ccf338cab64157669ff1fc0a8d72`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4079a2d61bafcf146b8f57b35f0e39bf2548e0963be10cff5086f9a56ccdd9d`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 126.3 KB (126257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f69efa1066815d67cf415d0aac5dcd305032257b6bded5a4c57a7444a1e7fd4`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 2.1 MB (2076363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357f4165f53a3d4c66ef270bcb5b5283a066af50f79924cccc7c73f6a4f6f4ab`  
		Last Modified: Thu, 18 Dec 2025 00:36:36 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a65ff5cefcbfc874c1cac0857339eaee0b07147dd26b6bfa18c00921b4f30c`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:1d06281345f2ac44a607d40d5e87de6abb99bbc6ee82d319e73f3794602d0282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4867a5aa08041c7e5ec69dfc84214226a7323d1ce703747ae2117675e2f74bcd`

```dockerfile
```

-	Layers:
	-	`sha256:282960f007d3f1f008333191d98a2ded5ff0f83075ace30043349b6c082c18fd`  
		Last Modified: Thu, 18 Dec 2025 01:35:08 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4755fffd5924e8405adfbed0f328ad9792eff20e2b8ad2025e1f5c85bca88618`  
		Last Modified: Thu, 18 Dec 2025 01:35:09 GMT  
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
$ docker pull memcached@sha256:e011484878fd5d1e2da6de478ac11d01ae80f0bdef1902dcde3ed53728803741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5857090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689ea71c305b80e206c68a215481290a1378e6375e32ad059455f7d041396aa6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:26 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:30:27 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:33:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:33:46 GMT
USER memcache
# Thu, 18 Dec 2025 00:33:46 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:33:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4594a6826f7ed03c8c4f9f2aebb9716eb6e16d5b5ab7e1bc247783b503c5b10`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f270744f8d8b82bc6657387109b33836a76d6dbf8faa645a997db7ea290cdb`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 114.3 KB (114299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91f8ee8f36703944a7bdcaf57cc5772fe9f79c74a088c33fa1b6da7de119f93`  
		Last Modified: Thu, 18 Dec 2025 00:34:02 GMT  
		Size: 2.0 MB (2017131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21d2db88668745770273c7b36d4d2c1e87a80b0118b8d775813860b467384c8`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd847159e169b898a67d4454fd5a22406c5ae623b16889d084a1d5f2d46a499`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:33ab737cb23dcde22de59a58e40f1f80d2c5e808ff3036519ae7d9db228fa37d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3562f7fd7806da24b1865c01a2246ac041b5e98d69c10ce6cbbe479f9408f9a1`

```dockerfile
```

-	Layers:
	-	`sha256:d5f43e64a79ee525bd0354a06e3284444fd642bbe6c1a782aa45ec2e20462f1d`  
		Last Modified: Thu, 18 Dec 2025 01:35:19 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bd2c024010f4f53d350bde9967c349efb3a58a2a812b14e17b29ddbd19eab87`  
		Last Modified: Thu, 18 Dec 2025 01:35:20 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:latest`

```console
$ docker pull memcached@sha256:9ae868852d0bc0974e4dd39c58436f73698081a31e61b8099871983e09d79f80
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
$ docker pull memcached@sha256:c9046d2a0ade04c91892254044294c2a529006458cd7b98bdc31b4054fffbfe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32193341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6654931990345ba058b2f50cedc8d03dfcc174d6809b0e7a820c12f7b93dc09d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:35:37 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:23 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:23 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:23 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:23 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:23 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b6bc7772cb8044287682c4af75ca1c8280c4837d5ffee58adc014018f02e91`  
		Last Modified: Wed, 17 Dec 2025 21:38:42 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3af321fdb36bbbb634d6be4a6e457f7eeb47b153460c7bab6c9eae91724b08b`  
		Last Modified: Wed, 17 Dec 2025 21:38:42 GMT  
		Size: 136.7 KB (136691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a00f7c8e317ad005bdf0117005dd753e347a8674b068c660bbc29b3f93a0621`  
		Last Modified: Wed, 17 Dec 2025 21:38:42 GMT  
		Size: 2.3 MB (2278641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb739034830ce246e4bc00aa883c7d2af8a1fd59bc3e2ea17cae3607bf281074`  
		Last Modified: Wed, 17 Dec 2025 21:38:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33cfbae525009776fcee65339602ed1b2a8a5f2c51898ec9fc499fe35c60b87`  
		Last Modified: Wed, 17 Dec 2025 21:38:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:e726a4ddf8221754a6a9fa1143cee47f51785aedb20dc0329a7c7b41b4772763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd3f16921a7fcccc9bc6ee3685e192e34a0b621f1c95362d6cea5e4293e54d33`

```dockerfile
```

-	Layers:
	-	`sha256:3a55af39eac38dca280008ae509d726055b1dde6e05ce9024174d0a0bd0565c2`  
		Last Modified: Wed, 17 Dec 2025 22:34:37 GMT  
		Size: 2.0 MB (2008228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef418f126bca0d267c3b365faed9990a104832e94e7ec35841aff2c2b26510dc`  
		Last Modified: Wed, 17 Dec 2025 22:34:38 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:c1a14cf6b3aa6f9ee13feee1c176a4ff104ec3d361f2df684e87a9d88a563eaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30300251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7375c421f8c059114c1a5cdc58215c8cf41dcc23355cbef325fdfa4b290df1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:39:00 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:39:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:42:24 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:42:24 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:42:24 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:42:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:42:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:42:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:42:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:42:24 GMT
USER memcache
# Wed, 17 Dec 2025 21:42:24 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:42:24 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d97bc71d0fa535127863fdab265dfddb07b3cda35b80de4dd2b9b67fe154c856`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 27.9 MB (27944187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e168dbb57c754690bc257f600efb5085929be35091c7e3d6926d35490c3391`  
		Last Modified: Wed, 17 Dec 2025 21:42:38 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78870a4506eecc7b424a3cedde90baa4c44a7c5d1174e6842b60c11b08a7984e`  
		Last Modified: Wed, 17 Dec 2025 21:42:40 GMT  
		Size: 144.2 KB (144157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e35d5393bf24a4f7ba0c87d734e7fda2d09414dec61e9139726200bed52e262`  
		Last Modified: Wed, 17 Dec 2025 21:42:39 GMT  
		Size: 2.2 MB (2210395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72c9d61ca04e663f67ab23ad2c50afcd810d29c2f52728277947d5ab78c03da`  
		Last Modified: Wed, 17 Dec 2025 21:42:38 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e89f91fff1d699acc4ebbc8ebb2a409d5f7867914100e87affef7b7d8775488`  
		Last Modified: Wed, 17 Dec 2025 21:42:38 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:3a82f6da1fa8b6c43220785849304c0e09363556371c8f763abae2126e271c5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e59d44e1c5460c7338a49dad6ec9d6d03db5b9330bb235c1d01e3e182df704ca`

```dockerfile
```

-	Layers:
	-	`sha256:2b38edaa9de8bf0d9055274c5ca1c0af276da0f57396ee1edfb8db1002dc8834`  
		Last Modified: Wed, 17 Dec 2025 22:34:42 GMT  
		Size: 2.0 MB (2011231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c70377fb854a2602cbb12ee80dd69f8a5deb00e23feb0c3c24e1b27806029b0d`  
		Last Modified: Wed, 17 Dec 2025 22:34:43 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v7

```console
$ docker pull memcached@sha256:b7ad53cb1e5a5631cc9b08d0fe984b0ba6bb7ab77da4309a552dbb97bd4ae04e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28510860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b2fbe25ebf8c8035604591c6ded5acfffe219c97c853c1c0e00421ac18abcd4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:35:20 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:30 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:30 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:30 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:30 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:30 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:30 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d46de1cc714aa644c02bc1b184e957b7330bf3473d4e97f72f454fdc8a432d`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0327c8719a60b04c8b690d8d0a0a122cdbc620f2aab391fd43789a8803b62bf1`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 135.4 KB (135362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd55327cbd82c4adf176e679bae5436e8aaf27c54595ec2cd7cfec20989b1fc`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 2.2 MB (2163972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37babf40b7b24af06cfbfc9fe6daf7d6f5863de148318182eecf29e242ba5e4c`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3daf0d6e9f1032a9bce2c34a57a6049ec4ffd4a412a20724540653fe7b6526d3`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:77b0259560abd3025ae0593b06db95eb3c4dd6dccbd2332f85286fae97d799bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd1267e1c8eb093b3e5a265d3c2d0c9b2b3784e50b6aa7edfec29ba838d4a8c`

```dockerfile
```

-	Layers:
	-	`sha256:3266292cf75a57aab22a4e279bf40458841e617570f3ee192bb26dc1d2d6e1ef`  
		Last Modified: Wed, 17 Dec 2025 22:34:47 GMT  
		Size: 2.0 MB (2009688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cc2be86d85bc478731bb7718f18d50da352f58c942412f66ca371226633d3bb`  
		Last Modified: Wed, 17 Dec 2025 22:34:48 GMT  
		Size: 22.3 KB (22303 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:230a135d43b1bf876ec5c160b78cb4f0303d1e6e98dc76a31dd524d28a4a5279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32554912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79214d48c3616d6c032db23eb36a6766c7a96a8d4619d8f8791d2fa43163cc34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:35:24 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:26 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:26 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:26 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:26 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:26 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:26 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f49eb557c72f2fe7e0eb1949c1587e8e4c86bdae514d70fac3ff429290a149`  
		Last Modified: Wed, 17 Dec 2025 21:38:46 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f764f8f3ed63ac8e640ebdcb2f5ea0371b6fb244a1f6defbe51ddfff908a34a`  
		Last Modified: Wed, 17 Dec 2025 21:38:46 GMT  
		Size: 153.5 KB (153477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9353d672d9aeb0b8a3ee269d120b0b920e9f6b81998ed7ef7765092573e4b716`  
		Last Modified: Wed, 17 Dec 2025 21:38:46 GMT  
		Size: 2.3 MB (2261292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ba4d16dc49a02e1490d18a58f5e108ec18a248f9ea83bb7b4deb8642b36f90`  
		Last Modified: Wed, 17 Dec 2025 21:38:46 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d15340fcbda1a05a50ba392408ace29b5cbb21b398bb1018750621349d3b0a`  
		Last Modified: Wed, 17 Dec 2025 21:38:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:d2a465ef21f85d63f634e52f05c50319a05c013d1aeed6321cc146b3a28a5920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c092dec716fd21afebb19ce5e88ba467a0f4bb88a40068e3e266b1f10ff6652`

```dockerfile
```

-	Layers:
	-	`sha256:b7bd1c3aaf184ba5d6dfbf328c24c2f39511de9c6e21c04b7fa212d6a26b0049`  
		Last Modified: Wed, 17 Dec 2025 22:34:53 GMT  
		Size: 2.0 MB (2008544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc6165d17a79a40bba13d288c74c5c34aa4af72304a300a74ceededf1a934bbc`  
		Last Modified: Wed, 17 Dec 2025 22:34:54 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:35df20cb1713a9d5fbb1820acac102f3c3560dfa2d0fa147fff30dfc53f209bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33665704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ccada050045e330c6b125cae2adfcf8e5edb8e23b5e044c0d53861f7762294a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:35:51 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:43 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:43 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:43 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:43 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:43 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b054f6842adaecae2d5cf75c99601b690566759a58606bc981ccae49baaae51`  
		Last Modified: Wed, 17 Dec 2025 21:38:57 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43efb4f909536827644b2ca98420204710b14f6195238a8ffdbf658c29883be`  
		Last Modified: Wed, 17 Dec 2025 21:38:57 GMT  
		Size: 147.5 KB (147519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:792eb292285447291b91c55e07bc1a75b3d4e125a3c23f80671848c5f967e042`  
		Last Modified: Wed, 17 Dec 2025 21:38:57 GMT  
		Size: 2.2 MB (2223600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe79378953d034686129f0d36718bb867ebebf130cd1f431ad68cf117a1308c6`  
		Last Modified: Wed, 17 Dec 2025 21:38:57 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92088f114f464c2f2e1217404e900d24a46a03305faa6cae793f0b873cadba52`  
		Last Modified: Wed, 17 Dec 2025 21:38:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:3a428e326360172543ee458a46a55c1b9e70d3eeeea945f2ed65839c307eddd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a62b1d6c9ce3819b6b67f9de9cc436a2f4cb362fad3a8c07627fd790e4bd8be7`

```dockerfile
```

-	Layers:
	-	`sha256:0f8e75010a0e7df5356c9c36b97dff2c5d2191f6f6e643619b4363f8c1e1dc42`  
		Last Modified: Wed, 17 Dec 2025 22:34:58 GMT  
		Size: 2.0 MB (2005385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98883c6827ebd9ca960545767f09a2be89e7580fc425e24f86364f3a9e4ea283`  
		Last Modified: Wed, 17 Dec 2025 22:34:59 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:38a236f83eb206f786b39c53e8f756815f0bda1460157b11844faf21735208bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36162589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41292f5c75fe5f3a464b809bde41e0ae8849ad8d7046918a548d0c6b2e250a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:34:54 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:28 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:28 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:28 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2b42546c7b688160cfd1a0da61a24922a019b4ebead88e23aff01482ddd477`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4efe9fd2e012174cd86a64f83d7b7facfe14ee67c9c9fa5ce994f22c24173f2c`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 170.4 KB (170393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9752985ba696f0f8d5831ac91e19bfe336342b1c403542641c575b1dc6116e`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 2.4 MB (2393786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d11c68ba0bc913d139eea51cb2957c1ddd713515fc06dfa5d4c398b119535a`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9186b8b7184cef442ae3ed6a3feadcaa8f4ccc974ed5ae6c6cf8efe37e679f23`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:00d1019e9978171df76f638253f212405bf7d53251607ef5a5933d5b28d867b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588d3d6ab54a9ea5c8baf9b013bb23c12826989ba0d09cb862431e2fa30e5189`

```dockerfile
```

-	Layers:
	-	`sha256:799ad025578a6d5d0155dc5be223bfbc25ffa3aa0548e4fb2e4bedeb0a5088d9`  
		Last Modified: Wed, 17 Dec 2025 22:35:03 GMT  
		Size: 2.0 MB (2011829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaa03114ccb63fbbd8ca04eef46baa26c8a0508f1256aa45d851f3a49f2ed47a`  
		Last Modified: Wed, 17 Dec 2025 22:35:04 GMT  
		Size: 22.2 KB (22225 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; riscv64

```console
$ docker pull memcached@sha256:5aedcd2b04ff2d8dc77fb6568e6ce96878f75508a3a01326623b60869874f8a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30615184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab5d9dd83f52434969fb6da016bd60451fd5d989e33e2cd491533dcb4553c835`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 05:30:55 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 09 Dec 2025 05:31:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Dec 2025 03:19:32 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 03:19:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 03:19:32 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 03:19:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 18 Dec 2025 03:19:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 03:19:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 03:19:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 03:19:33 GMT
USER memcache
# Thu, 18 Dec 2025 03:19:33 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 03:19:33 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb23364b88c4686dab6a11bf004aac89beea8adb8559fd39799a54dc729c23a6`  
		Last Modified: Tue, 09 Dec 2025 05:57:38 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edeeae49e27528d2079d0d5aeb702d7dd56503463fa4054ee2444f847f399650`  
		Last Modified: Tue, 09 Dec 2025 05:57:38 GMT  
		Size: 133.1 KB (133076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e584b688c99191b71a2471afe63daff415a1eedcf541b959dfcdf248eebd8577`  
		Last Modified: Thu, 18 Dec 2025 03:20:28 GMT  
		Size: 2.2 MB (2207438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b780b2b80274922cc63f0afe1ecd2680bcafae3234732fd03ba740690e3ebf1`  
		Last Modified: Thu, 18 Dec 2025 03:20:28 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5449346fa21339be4109a2e289721bfa7b0e8203b88fe202956ebb257c703a88`  
		Last Modified: Thu, 18 Dec 2025 03:20:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:bbe7bbb4c3590b1fc9c5943719d3b1b2a21670d2874ed90415040aeae5b13200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c721ad9798565707f4e9e537a1618b5efafce47c49577053fe7b40879caca9`

```dockerfile
```

-	Layers:
	-	`sha256:37125be6342f13dcb1fff2b0c3def6d6f3b808e19192f9ff68a139ce2d1d3083`  
		Last Modified: Thu, 18 Dec 2025 04:34:34 GMT  
		Size: 2.0 MB (2002192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06edc085828555adcb8aac4ef4e564c72d260338e77dde6abe811eefcdd8682d`  
		Last Modified: Thu, 18 Dec 2025 04:34:35 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:1e7fc2740e66d7d7b21982f73ae72e901616fcb9ebc6176c6f1d931c6a4732b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32273737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f632195b7b4a10526fcb27d2d66a479b07455d784656340bcbae2d31e292aa2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:34:51 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:34:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:04 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:04 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:04 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:04 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:04 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:04 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9606e3e114197b678b6fbd5b889ab574d2ad4cd8b4010407f847a98309f0f6b`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24f23dd2596713c0a8daf1cde9aabc7d26e7e9b832300ba1ce4615e8c806afc`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 140.5 KB (140507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0dd33ff71e256560cf1693538e8ecc4f92550f6483c1478697b822abf8d0f84`  
		Last Modified: Wed, 17 Dec 2025 21:38:19 GMT  
		Size: 2.3 MB (2297315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568ee6e9ecd99ef323ff6ff6b40b5fcf91b13472f56ac46f8b3036c82c705fd6`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91a63e3e27d493e5ad7b64edf0b8ae2bb8ade89a55bfc197b4dc9a393ceec4b`  
		Last Modified: Wed, 17 Dec 2025 21:38:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:d9aa5142dc8acd96ae2fb7235ceda06498adc21053e1bc5bf02ff76701213426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e87c93018f4f94a4286dcf6f6d33373729ef4263208b2f346e92a2028839a2`

```dockerfile
```

-	Layers:
	-	`sha256:c0ee3f2287a538730e473aea557f8fc2a48d18bb9e778e65ccdbf8918310ace3`  
		Last Modified: Wed, 17 Dec 2025 22:35:11 GMT  
		Size: 2.0 MB (2009665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce86917337210887b4362390f278a89c9fc6d6d1cc50e29ebf7f716bc556c877`  
		Last Modified: Wed, 17 Dec 2025 22:35:12 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:trixie`

```console
$ docker pull memcached@sha256:9ae868852d0bc0974e4dd39c58436f73698081a31e61b8099871983e09d79f80
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
$ docker pull memcached@sha256:c9046d2a0ade04c91892254044294c2a529006458cd7b98bdc31b4054fffbfe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32193341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6654931990345ba058b2f50cedc8d03dfcc174d6809b0e7a820c12f7b93dc09d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:35:37 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:23 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:23 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:23 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:23 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:23 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b6bc7772cb8044287682c4af75ca1c8280c4837d5ffee58adc014018f02e91`  
		Last Modified: Wed, 17 Dec 2025 21:38:42 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3af321fdb36bbbb634d6be4a6e457f7eeb47b153460c7bab6c9eae91724b08b`  
		Last Modified: Wed, 17 Dec 2025 21:38:42 GMT  
		Size: 136.7 KB (136691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a00f7c8e317ad005bdf0117005dd753e347a8674b068c660bbc29b3f93a0621`  
		Last Modified: Wed, 17 Dec 2025 21:38:42 GMT  
		Size: 2.3 MB (2278641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb739034830ce246e4bc00aa883c7d2af8a1fd59bc3e2ea17cae3607bf281074`  
		Last Modified: Wed, 17 Dec 2025 21:38:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33cfbae525009776fcee65339602ed1b2a8a5f2c51898ec9fc499fe35c60b87`  
		Last Modified: Wed, 17 Dec 2025 21:38:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:e726a4ddf8221754a6a9fa1143cee47f51785aedb20dc0329a7c7b41b4772763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd3f16921a7fcccc9bc6ee3685e192e34a0b621f1c95362d6cea5e4293e54d33`

```dockerfile
```

-	Layers:
	-	`sha256:3a55af39eac38dca280008ae509d726055b1dde6e05ce9024174d0a0bd0565c2`  
		Last Modified: Wed, 17 Dec 2025 22:34:37 GMT  
		Size: 2.0 MB (2008228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef418f126bca0d267c3b365faed9990a104832e94e7ec35841aff2c2b26510dc`  
		Last Modified: Wed, 17 Dec 2025 22:34:38 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:c1a14cf6b3aa6f9ee13feee1c176a4ff104ec3d361f2df684e87a9d88a563eaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30300251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7375c421f8c059114c1a5cdc58215c8cf41dcc23355cbef325fdfa4b290df1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:39:00 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:39:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:42:24 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:42:24 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:42:24 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:42:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:42:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:42:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:42:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:42:24 GMT
USER memcache
# Wed, 17 Dec 2025 21:42:24 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:42:24 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d97bc71d0fa535127863fdab265dfddb07b3cda35b80de4dd2b9b67fe154c856`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 27.9 MB (27944187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e168dbb57c754690bc257f600efb5085929be35091c7e3d6926d35490c3391`  
		Last Modified: Wed, 17 Dec 2025 21:42:38 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78870a4506eecc7b424a3cedde90baa4c44a7c5d1174e6842b60c11b08a7984e`  
		Last Modified: Wed, 17 Dec 2025 21:42:40 GMT  
		Size: 144.2 KB (144157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e35d5393bf24a4f7ba0c87d734e7fda2d09414dec61e9139726200bed52e262`  
		Last Modified: Wed, 17 Dec 2025 21:42:39 GMT  
		Size: 2.2 MB (2210395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72c9d61ca04e663f67ab23ad2c50afcd810d29c2f52728277947d5ab78c03da`  
		Last Modified: Wed, 17 Dec 2025 21:42:38 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e89f91fff1d699acc4ebbc8ebb2a409d5f7867914100e87affef7b7d8775488`  
		Last Modified: Wed, 17 Dec 2025 21:42:38 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:3a82f6da1fa8b6c43220785849304c0e09363556371c8f763abae2126e271c5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e59d44e1c5460c7338a49dad6ec9d6d03db5b9330bb235c1d01e3e182df704ca`

```dockerfile
```

-	Layers:
	-	`sha256:2b38edaa9de8bf0d9055274c5ca1c0af276da0f57396ee1edfb8db1002dc8834`  
		Last Modified: Wed, 17 Dec 2025 22:34:42 GMT  
		Size: 2.0 MB (2011231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c70377fb854a2602cbb12ee80dd69f8a5deb00e23feb0c3c24e1b27806029b0d`  
		Last Modified: Wed, 17 Dec 2025 22:34:43 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:b7ad53cb1e5a5631cc9b08d0fe984b0ba6bb7ab77da4309a552dbb97bd4ae04e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28510860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b2fbe25ebf8c8035604591c6ded5acfffe219c97c853c1c0e00421ac18abcd4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:35:20 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:30 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:30 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:30 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:30 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:30 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:30 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d46de1cc714aa644c02bc1b184e957b7330bf3473d4e97f72f454fdc8a432d`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0327c8719a60b04c8b690d8d0a0a122cdbc620f2aab391fd43789a8803b62bf1`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 135.4 KB (135362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd55327cbd82c4adf176e679bae5436e8aaf27c54595ec2cd7cfec20989b1fc`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 2.2 MB (2163972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37babf40b7b24af06cfbfc9fe6daf7d6f5863de148318182eecf29e242ba5e4c`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3daf0d6e9f1032a9bce2c34a57a6049ec4ffd4a412a20724540653fe7b6526d3`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:77b0259560abd3025ae0593b06db95eb3c4dd6dccbd2332f85286fae97d799bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd1267e1c8eb093b3e5a265d3c2d0c9b2b3784e50b6aa7edfec29ba838d4a8c`

```dockerfile
```

-	Layers:
	-	`sha256:3266292cf75a57aab22a4e279bf40458841e617570f3ee192bb26dc1d2d6e1ef`  
		Last Modified: Wed, 17 Dec 2025 22:34:47 GMT  
		Size: 2.0 MB (2009688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cc2be86d85bc478731bb7718f18d50da352f58c942412f66ca371226633d3bb`  
		Last Modified: Wed, 17 Dec 2025 22:34:48 GMT  
		Size: 22.3 KB (22303 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:230a135d43b1bf876ec5c160b78cb4f0303d1e6e98dc76a31dd524d28a4a5279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32554912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79214d48c3616d6c032db23eb36a6766c7a96a8d4619d8f8791d2fa43163cc34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:35:24 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:26 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:26 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:26 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:26 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:26 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:26 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f49eb557c72f2fe7e0eb1949c1587e8e4c86bdae514d70fac3ff429290a149`  
		Last Modified: Wed, 17 Dec 2025 21:38:46 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f764f8f3ed63ac8e640ebdcb2f5ea0371b6fb244a1f6defbe51ddfff908a34a`  
		Last Modified: Wed, 17 Dec 2025 21:38:46 GMT  
		Size: 153.5 KB (153477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9353d672d9aeb0b8a3ee269d120b0b920e9f6b81998ed7ef7765092573e4b716`  
		Last Modified: Wed, 17 Dec 2025 21:38:46 GMT  
		Size: 2.3 MB (2261292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ba4d16dc49a02e1490d18a58f5e108ec18a248f9ea83bb7b4deb8642b36f90`  
		Last Modified: Wed, 17 Dec 2025 21:38:46 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d15340fcbda1a05a50ba392408ace29b5cbb21b398bb1018750621349d3b0a`  
		Last Modified: Wed, 17 Dec 2025 21:38:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:d2a465ef21f85d63f634e52f05c50319a05c013d1aeed6321cc146b3a28a5920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c092dec716fd21afebb19ce5e88ba467a0f4bb88a40068e3e266b1f10ff6652`

```dockerfile
```

-	Layers:
	-	`sha256:b7bd1c3aaf184ba5d6dfbf328c24c2f39511de9c6e21c04b7fa212d6a26b0049`  
		Last Modified: Wed, 17 Dec 2025 22:34:53 GMT  
		Size: 2.0 MB (2008544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc6165d17a79a40bba13d288c74c5c34aa4af72304a300a74ceededf1a934bbc`  
		Last Modified: Wed, 17 Dec 2025 22:34:54 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; 386

```console
$ docker pull memcached@sha256:35df20cb1713a9d5fbb1820acac102f3c3560dfa2d0fa147fff30dfc53f209bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33665704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ccada050045e330c6b125cae2adfcf8e5edb8e23b5e044c0d53861f7762294a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:35:51 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:43 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:43 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:43 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:43 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:43 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b054f6842adaecae2d5cf75c99601b690566759a58606bc981ccae49baaae51`  
		Last Modified: Wed, 17 Dec 2025 21:38:57 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43efb4f909536827644b2ca98420204710b14f6195238a8ffdbf658c29883be`  
		Last Modified: Wed, 17 Dec 2025 21:38:57 GMT  
		Size: 147.5 KB (147519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:792eb292285447291b91c55e07bc1a75b3d4e125a3c23f80671848c5f967e042`  
		Last Modified: Wed, 17 Dec 2025 21:38:57 GMT  
		Size: 2.2 MB (2223600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe79378953d034686129f0d36718bb867ebebf130cd1f431ad68cf117a1308c6`  
		Last Modified: Wed, 17 Dec 2025 21:38:57 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92088f114f464c2f2e1217404e900d24a46a03305faa6cae793f0b873cadba52`  
		Last Modified: Wed, 17 Dec 2025 21:38:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:3a428e326360172543ee458a46a55c1b9e70d3eeeea945f2ed65839c307eddd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a62b1d6c9ce3819b6b67f9de9cc436a2f4cb362fad3a8c07627fd790e4bd8be7`

```dockerfile
```

-	Layers:
	-	`sha256:0f8e75010a0e7df5356c9c36b97dff2c5d2191f6f6e643619b4363f8c1e1dc42`  
		Last Modified: Wed, 17 Dec 2025 22:34:58 GMT  
		Size: 2.0 MB (2005385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98883c6827ebd9ca960545767f09a2be89e7580fc425e24f86364f3a9e4ea283`  
		Last Modified: Wed, 17 Dec 2025 22:34:59 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:38a236f83eb206f786b39c53e8f756815f0bda1460157b11844faf21735208bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36162589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41292f5c75fe5f3a464b809bde41e0ae8849ad8d7046918a548d0c6b2e250a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:34:54 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:28 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:28 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:28 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2b42546c7b688160cfd1a0da61a24922a019b4ebead88e23aff01482ddd477`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4efe9fd2e012174cd86a64f83d7b7facfe14ee67c9c9fa5ce994f22c24173f2c`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 170.4 KB (170393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9752985ba696f0f8d5831ac91e19bfe336342b1c403542641c575b1dc6116e`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 2.4 MB (2393786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d11c68ba0bc913d139eea51cb2957c1ddd713515fc06dfa5d4c398b119535a`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9186b8b7184cef442ae3ed6a3feadcaa8f4ccc974ed5ae6c6cf8efe37e679f23`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:00d1019e9978171df76f638253f212405bf7d53251607ef5a5933d5b28d867b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588d3d6ab54a9ea5c8baf9b013bb23c12826989ba0d09cb862431e2fa30e5189`

```dockerfile
```

-	Layers:
	-	`sha256:799ad025578a6d5d0155dc5be223bfbc25ffa3aa0548e4fb2e4bedeb0a5088d9`  
		Last Modified: Wed, 17 Dec 2025 22:35:03 GMT  
		Size: 2.0 MB (2011829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaa03114ccb63fbbd8ca04eef46baa26c8a0508f1256aa45d851f3a49f2ed47a`  
		Last Modified: Wed, 17 Dec 2025 22:35:04 GMT  
		Size: 22.2 KB (22225 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:5aedcd2b04ff2d8dc77fb6568e6ce96878f75508a3a01326623b60869874f8a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30615184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab5d9dd83f52434969fb6da016bd60451fd5d989e33e2cd491533dcb4553c835`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 05:30:55 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 09 Dec 2025 05:31:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Dec 2025 03:19:32 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 03:19:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 03:19:32 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 03:19:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 18 Dec 2025 03:19:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 03:19:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 03:19:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 03:19:33 GMT
USER memcache
# Thu, 18 Dec 2025 03:19:33 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 03:19:33 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb23364b88c4686dab6a11bf004aac89beea8adb8559fd39799a54dc729c23a6`  
		Last Modified: Tue, 09 Dec 2025 05:57:38 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edeeae49e27528d2079d0d5aeb702d7dd56503463fa4054ee2444f847f399650`  
		Last Modified: Tue, 09 Dec 2025 05:57:38 GMT  
		Size: 133.1 KB (133076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e584b688c99191b71a2471afe63daff415a1eedcf541b959dfcdf248eebd8577`  
		Last Modified: Thu, 18 Dec 2025 03:20:28 GMT  
		Size: 2.2 MB (2207438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b780b2b80274922cc63f0afe1ecd2680bcafae3234732fd03ba740690e3ebf1`  
		Last Modified: Thu, 18 Dec 2025 03:20:28 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5449346fa21339be4109a2e289721bfa7b0e8203b88fe202956ebb257c703a88`  
		Last Modified: Thu, 18 Dec 2025 03:20:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:bbe7bbb4c3590b1fc9c5943719d3b1b2a21670d2874ed90415040aeae5b13200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c721ad9798565707f4e9e537a1618b5efafce47c49577053fe7b40879caca9`

```dockerfile
```

-	Layers:
	-	`sha256:37125be6342f13dcb1fff2b0c3def6d6f3b808e19192f9ff68a139ce2d1d3083`  
		Last Modified: Thu, 18 Dec 2025 04:34:34 GMT  
		Size: 2.0 MB (2002192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06edc085828555adcb8aac4ef4e564c72d260338e77dde6abe811eefcdd8682d`  
		Last Modified: Thu, 18 Dec 2025 04:34:35 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; s390x

```console
$ docker pull memcached@sha256:1e7fc2740e66d7d7b21982f73ae72e901616fcb9ebc6176c6f1d931c6a4732b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32273737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f632195b7b4a10526fcb27d2d66a479b07455d784656340bcbae2d31e292aa2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:34:51 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:34:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:04 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:04 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:04 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:04 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:04 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:04 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9606e3e114197b678b6fbd5b889ab574d2ad4cd8b4010407f847a98309f0f6b`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24f23dd2596713c0a8daf1cde9aabc7d26e7e9b832300ba1ce4615e8c806afc`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 140.5 KB (140507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0dd33ff71e256560cf1693538e8ecc4f92550f6483c1478697b822abf8d0f84`  
		Last Modified: Wed, 17 Dec 2025 21:38:19 GMT  
		Size: 2.3 MB (2297315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568ee6e9ecd99ef323ff6ff6b40b5fcf91b13472f56ac46f8b3036c82c705fd6`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91a63e3e27d493e5ad7b64edf0b8ae2bb8ade89a55bfc197b4dc9a393ceec4b`  
		Last Modified: Wed, 17 Dec 2025 21:38:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:d9aa5142dc8acd96ae2fb7235ceda06498adc21053e1bc5bf02ff76701213426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e87c93018f4f94a4286dcf6f6d33373729ef4263208b2f346e92a2028839a2`

```dockerfile
```

-	Layers:
	-	`sha256:c0ee3f2287a538730e473aea557f8fc2a48d18bb9e778e65ccdbf8918310ace3`  
		Last Modified: Wed, 17 Dec 2025 22:35:11 GMT  
		Size: 2.0 MB (2009665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce86917337210887b4362390f278a89c9fc6d6d1cc50e29ebf7f716bc556c877`  
		Last Modified: Wed, 17 Dec 2025 22:35:12 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json
