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
$ docker pull memcached@sha256:6d4a394b5184f38fcdedabebc810a1e63861427e44215ec8a48a276678236df9
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
$ docker pull memcached@sha256:d8a6e6b246f27a6bbcdfda8a9a06e436178aa58c717448c641a6815f3cc38467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30627609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c80d74d8037160ffc9363dc03f0b6461d3c4cdd69da6460620b26838cb33a671`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 05:30:55 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 09 Dec 2025 05:31:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 05:56:35 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 09 Dec 2025 05:56:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 09 Dec 2025 05:56:35 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 09 Dec 2025 05:56:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 09 Dec 2025 05:56:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 05:56:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 09 Dec 2025 05:56:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Dec 2025 05:56:35 GMT
USER memcache
# Tue, 09 Dec 2025 05:56:35 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 09 Dec 2025 05:56:35 GMT
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
	-	`sha256:e9481f8b437fde8b1c89c79b65538c260df5216129bbe341f98c35935b4fe171`  
		Last Modified: Tue, 09 Dec 2025 05:57:38 GMT  
		Size: 2.2 MB (2219867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe3ccefbdcfdf466052c783e0982017ab232dd919bf46bb40b57edc66cee678`  
		Last Modified: Tue, 09 Dec 2025 05:57:38 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0be3eb5d00166beb14be204124c9c1033e288c0843f2c4aad6a372420a36c6`  
		Last Modified: Tue, 09 Dec 2025 05:57:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:0d07cca14f06f49448edd46f7de94275f31b7fd189fb725cb196bd96aa1ce642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:176f611a3de50a80e211655f970b224ae64d5ab4d2bb1aa8785a22161fe14060`

```dockerfile
```

-	Layers:
	-	`sha256:5f35bc7d6cd5ba3a512b097e6894fe90d53c248ba00f25fb4e1cc8f760d64548`  
		Last Modified: Tue, 09 Dec 2025 07:34:40 GMT  
		Size: 2.0 MB (2002192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18b98ed8b5ce7f2a905ffa540823ace4ea6f63ea74d51da31800c23d9fae6c1f`  
		Last Modified: Tue, 09 Dec 2025 07:34:41 GMT  
		Size: 22.2 KB (22226 bytes)  
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
$ docker pull memcached@sha256:4ec52eed643b17626643099f4ce0a142ef9dce004fc8bb32f582c0c31219dba9
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
$ docker pull memcached@sha256:65c25df73382e5ba4c57df3c2cccb5eb69702b813d07f9372f525e61225f0236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5955960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d33317a7accc6b056e21432db4903632531ace63c6085001ffb22caaa6d9d75b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:38:00 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:38:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:40:37 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:40:37 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:40:37 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:40:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:40:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:40:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:40:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:40:38 GMT
USER memcache
# Wed, 17 Dec 2025 21:40:38 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:40:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683f24283462cf58a8a6a81d7a140d0cd612c8120a019a56b2cb5f6f297d9465`  
		Last Modified: Wed, 17 Dec 2025 21:40:49 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450bd59379b8c57899254729c322d8ed1a1a7ca519dd92b78fc2d93e4e8a0b25`  
		Last Modified: Wed, 17 Dec 2025 21:40:49 GMT  
		Size: 106.0 KB (106041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2091c3522fccefd861318754918a244e21e5582890c29a366f8a5deb524e60af`  
		Last Modified: Wed, 17 Dec 2025 21:40:49 GMT  
		Size: 2.0 MB (1989255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9898efa8e26f703b25503f6a996e1f99a1fd8128fceb41ffe2e64c68a38599`  
		Last Modified: Wed, 17 Dec 2025 21:40:49 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2662bcfc6adeacc0aa8fd4c9d65e40532dd669f2516c02dc4a8ed4ce03647a0f`  
		Last Modified: Wed, 17 Dec 2025 21:40:49 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:e2ce9177720be2878a317e1f529eab177e45fa4f1bd45a06a69779f7c963a705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d581a35520859a173fbf6058a00db5435952fa00e8e9ee6c788563d4cae2f3`

```dockerfile
```

-	Layers:
	-	`sha256:1fe61b448f6cbc544f9c72a56a148440a1f1e60eaffe9144cbc03096adacdf37`  
		Last Modified: Wed, 17 Dec 2025 22:35:02 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea30cf376da8351a758cad58a77f03776483c271a35b12b24e81530b12868a2e`  
		Last Modified: Wed, 17 Dec 2025 22:35:03 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:ea5a1cd530f7418ba73b2ec6d05aa7d073fa3e55362ad7c272c4dce82f2ee550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5611085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e6688be943a2b0ca333de7ee49b87d11b3b103acac53a8a1cda65827e164b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:35:21 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:35:22 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:57:18 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:57:18 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:57:18 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:57:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:57:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:57:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:57:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:57:19 GMT
USER memcache
# Wed, 17 Dec 2025 21:57:19 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:57:19 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0132a447b58e699f3e930eb400504a4dab7572b48682b411e172ca2f13e3837e`  
		Last Modified: Wed, 17 Dec 2025 21:57:31 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca221542481b910c1ab1534fbed6a1daa903dd46e7dec29a8e7e45e172ee4e98`  
		Last Modified: Wed, 17 Dec 2025 21:57:31 GMT  
		Size: 102.6 KB (102643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f509979790be1d0f32b1cb145ef690501c7b24933c62c28638d664ba9c700393`  
		Last Modified: Wed, 17 Dec 2025 21:57:32 GMT  
		Size: 1.9 MB (1939202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92b99708f0757173744dcefe8c10b63d6bb57457bb22a870a97d2e466b7dbe6`  
		Last Modified: Wed, 17 Dec 2025 21:57:31 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129c905b76006e4eac5697b73920244e0b167164eda691d8c9fce48e08d9a15a`  
		Last Modified: Wed, 17 Dec 2025 21:57:31 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:a01a7f359b5b6020f56a33f6c48f6d83addd590b6ffcfb8d9f39cbb014a3f79f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b004564c274eab1f4a9d5854d0515a6b15f0a9de9abfe0403b6717464af55ca2`

```dockerfile
```

-	Layers:
	-	`sha256:223be1dd282744e43fcfc8303bb2997a6a232da86d8a573d407d550c7f356417`  
		Last Modified: Wed, 17 Dec 2025 22:35:06 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:f8a13acc5d2817ee1e9df95f26a3647b2fc9361676acb4ccca0e106d0ff8d5d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5269348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c8d4d3ca238a3133af08dd38e3cd46b3afbc7409a4df18d893b9878e5001cb8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:35:30 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:35:31 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:27 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:27 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d9d8962df55145f5fd88847d7fbf0fd846221bbe5d3fda7baf9461e1be862b`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5b6235e518eb1a135149571028b21cc0487ffc5c0fb9eb823fa9f51c9b3b7f`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 92.4 KB (92365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b5f719f7a3d4ba338f20ab53593f3250818988f89bc9d1ac7f5d3412497aa5`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 1.9 MB (1897164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6783f23f1f96fa31f44928320bb651f00a3ac7c6f74bc8d4931b527ad745771`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9186b8b7184cef442ae3ed6a3feadcaa8f4ccc974ed5ae6c6cf8efe37e679f23`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:65ab94866fe80b34478423e645bc70428ca81e1ef0e523993f4da895ba84a4ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2093447767fcc95a5f23b4567561974625baad6244721a2fadf42a60f1d61397`

```dockerfile
```

-	Layers:
	-	`sha256:a8a1bb2b759719025d140e377ef6a401d06c350a48eea3cf16e20ecb526095d9`  
		Last Modified: Wed, 17 Dec 2025 22:35:09 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b06bbe6a45bdcd2081c0e485d5ab897b548b87391fe55dfaeac6bdabf63b6e4`  
		Last Modified: Wed, 17 Dec 2025 22:35:10 GMT  
		Size: 20.7 KB (20677 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:349dc973200279dddf8e6ce28d9128babfe84da2f011c88d675fda6b53d9b435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6284972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee78c99ff858f77e454879ddf462b94812f23a4a38585a7f04722f753f72bdf4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:37:24 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:37:25 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:40:13 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:40:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:40:13 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:40:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:40:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:40:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:40:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:40:13 GMT
USER memcache
# Wed, 17 Dec 2025 21:40:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:40:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e5de81b8fd10090b357c152c289b12543ba0233b02e1fea1f31abbb41c6ce6`  
		Last Modified: Wed, 17 Dec 2025 21:40:24 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a237d3db68cd689e683d8873b9f6662b963c1da855cb61f0404b9d218ce4ab`  
		Last Modified: Wed, 17 Dec 2025 21:40:24 GMT  
		Size: 121.9 KB (121870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab92f84f0d6a5d6415bf522e99e0ccc9603a821231233c659431c00d8f166e16`  
		Last Modified: Wed, 17 Dec 2025 21:40:24 GMT  
		Size: 2.0 MB (1966553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd31b8f53d48209a8b58d7add5eaa6252a50192d7d95307012fbe2a96c887175`  
		Last Modified: Wed, 17 Dec 2025 21:40:24 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db33d4acf9261f39e1a05295122f733c54555907dbe2700043b4e721fa2acf3b`  
		Last Modified: Wed, 17 Dec 2025 21:40:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9a729809b661b20e6e8b44bb24413f513e1376d4dbe9ab0c1a4f7ed880149b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9883a54a8c4d45530843267722922526423a42a88046db1e58f74bed8bbe02d0`

```dockerfile
```

-	Layers:
	-	`sha256:a671bbb9a5464bb97f71429c00d4997635a1c127dc1b513aa48239e480106d60`  
		Last Modified: Wed, 17 Dec 2025 22:35:21 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36ef2adae88460c5dc2044a65093008d2beb76079d1f00bc5a7d862dbae0aa3b`  
		Last Modified: Wed, 17 Dec 2025 22:35:22 GMT  
		Size: 20.7 KB (20727 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:ca4c4cf71b28fb2b701d7c25e78c0cf8a8cd4de9424d86e7f906833f71f198eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5740718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f722d8a189d7c92749316efb1c7335a5873618eac12d5e5bc01d68127fb291b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:38:08 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:38:09 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:40:55 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:40:55 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:40:55 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:40:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:40:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:40:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:40:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:40:55 GMT
USER memcache
# Wed, 17 Dec 2025 21:40:55 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:40:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3527b4f952d5950d8caa74dc0d1759215000f2f0a195344f0239c7e2805fe2fc`  
		Last Modified: Wed, 03 Dec 2025 19:30:41 GMT  
		Size: 3.7 MB (3685856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d3f49b0de92207dfc061e70de94dd679b3ea12f97d99d1974a6c62164a159a`  
		Last Modified: Wed, 17 Dec 2025 21:41:06 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c266f269a50bef9007064361dc83371a1dd461aabe92bbec3d1e979412466de`  
		Last Modified: Wed, 17 Dec 2025 21:41:06 GMT  
		Size: 110.7 KB (110738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2053dfa7b6aa4f5a136466c1659669f25a4578930977fb585d209c5dfde8036d`  
		Last Modified: Wed, 17 Dec 2025 21:41:08 GMT  
		Size: 1.9 MB (1942772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ed31d7fa74d79df9efd8d4f443ada386f5729fbe324a9794e76baff2c1c493`  
		Last Modified: Wed, 17 Dec 2025 21:41:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91df285e3ed438acb3e9589dc178518e2db7c4bfa971348c72b6d0327a4ee79`  
		Last Modified: Wed, 17 Dec 2025 21:41:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:647a776f52f62548a4098b2e4b11214b4a5c1ee9685712ef80a2832ef32ca8c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40881c0a421ed132c378aef8bdbe39305aaaecc7deee9b7de9ae4f93188dcbd3`

```dockerfile
```

-	Layers:
	-	`sha256:f3beb40a7590bdda06e509d8ad4ecd2043849256a64e5ff660b19b1cd56a094a`  
		Last Modified: Wed, 17 Dec 2025 22:35:25 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38c8a2e4dad46bf55c80872707f6283533a800478b72bf885b684dd50e07eb32`  
		Last Modified: Wed, 17 Dec 2025 22:35:26 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:3b02ff737dd16e237fd7406b5f7d02a513a983b5d2d53fa6cd313f1ef00b1f8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6030994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:530bbfb00fa1800e8532eef4fb114fc753724fcf50e1d1e12af0ca80cf6752a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:34:55 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:34:56 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:37:26 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:37:26 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:37:26 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:37:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:37:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:37:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:37:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:37:38 GMT
USER memcache
# Wed, 17 Dec 2025 21:37:38 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:37:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd01e04da0d57bffa2b60a957360f7a974a6b01b4d9acff8252fdec64a69f66`  
		Last Modified: Wed, 17 Dec 2025 21:38:00 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a239f5e0c0c7e367e7f132151c23b859390ef5a4cbc40fb10415655b7e4b8029`  
		Last Modified: Wed, 17 Dec 2025 21:38:00 GMT  
		Size: 126.3 KB (126252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5bf0071779f0057bb08ae7a6ce2aba364cd026a86150629c39a6a92aba920c`  
		Last Modified: Wed, 17 Dec 2025 21:38:00 GMT  
		Size: 2.1 MB (2076368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f39797f21825b46f2a91c72f603d5a656910a53e51d3e579f5f5e791aaac92`  
		Last Modified: Wed, 17 Dec 2025 21:38:00 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48cd6c111239cce7a47ed3674b56951e2830764b3576a0d26aa6924057642d4`  
		Last Modified: Wed, 17 Dec 2025 21:38:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:31b4659d5068108cb086c10f7eff5fc0f8d77afa0eb09b15fa3955924ad138ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4951610ebef7b9fc8a4a054b6085f3840f9ba32b81602af0d8c13ad838ba68`

```dockerfile
```

-	Layers:
	-	`sha256:c3757f7ab5b65afe79fc72a82e96ca02b81c222ba9649feccf145ce714cfc4b9`  
		Last Modified: Wed, 17 Dec 2025 22:35:29 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df6d5f19cafffe602863ac2b65054f5c05d4a497fece84a762d0aebdc057b39e`  
		Last Modified: Wed, 17 Dec 2025 22:35:29 GMT  
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
$ docker pull memcached@sha256:04733682f967e9788435bbddf864edb8e1bb9cc8671e1e868c74f82093fe62c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5856574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9063d29cfc1dce3d05c19ff319a9d3e5455146c60efe56e9ce56bfbf4d3c3927`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:34:52 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:34:53 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:38:01 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:01 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:01 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:01 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a990effa92b45935b52bc06653d39a48f5ed34d054f60e892ec417f8d919a6`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50bf0a9e48ac326120a5de8b5e0cd6b991d704ed4a66448d4fcc8c6ad640d10`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 114.3 KB (114287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b26a3c60d8c62feb971cedd3bd49cd1d5f4d0d0d0149017b32b1573727914be9`  
		Last Modified: Wed, 17 Dec 2025 21:38:19 GMT  
		Size: 2.0 MB (2017127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd733ace70e5f90e389ce8159cbda2291a52bf39e53e2ee4ea6eb8cbccc625e`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821f5deda63bf425c92464f3e686b9fda7f6200ddc49ebacb324b2a45ec0d633`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:19f5876a625b474e4eea9e963de1422ad480c97357d44cd8604896e2da517d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd50fa1a24cfb1dea4e93374baa1e967c2f0fddd79dfa74422b955c193ea89a6`

```dockerfile
```

-	Layers:
	-	`sha256:4d2cbcf3625eaa8b19de7227c701c14f9bd69378a6e698f5aee36b0eb01f2167`  
		Last Modified: Wed, 17 Dec 2025 22:35:35 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:235e217cf2514537b942b1cb8a5ffbbe2ecee441b9373e75871acd7a34391107`  
		Last Modified: Wed, 17 Dec 2025 22:35:36 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine3.23`

```console
$ docker pull memcached@sha256:4ec52eed643b17626643099f4ce0a142ef9dce004fc8bb32f582c0c31219dba9
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
$ docker pull memcached@sha256:65c25df73382e5ba4c57df3c2cccb5eb69702b813d07f9372f525e61225f0236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5955960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d33317a7accc6b056e21432db4903632531ace63c6085001ffb22caaa6d9d75b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:38:00 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:38:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:40:37 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:40:37 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:40:37 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:40:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:40:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:40:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:40:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:40:38 GMT
USER memcache
# Wed, 17 Dec 2025 21:40:38 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:40:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683f24283462cf58a8a6a81d7a140d0cd612c8120a019a56b2cb5f6f297d9465`  
		Last Modified: Wed, 17 Dec 2025 21:40:49 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450bd59379b8c57899254729c322d8ed1a1a7ca519dd92b78fc2d93e4e8a0b25`  
		Last Modified: Wed, 17 Dec 2025 21:40:49 GMT  
		Size: 106.0 KB (106041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2091c3522fccefd861318754918a244e21e5582890c29a366f8a5deb524e60af`  
		Last Modified: Wed, 17 Dec 2025 21:40:49 GMT  
		Size: 2.0 MB (1989255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9898efa8e26f703b25503f6a996e1f99a1fd8128fceb41ffe2e64c68a38599`  
		Last Modified: Wed, 17 Dec 2025 21:40:49 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2662bcfc6adeacc0aa8fd4c9d65e40532dd669f2516c02dc4a8ed4ce03647a0f`  
		Last Modified: Wed, 17 Dec 2025 21:40:49 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:e2ce9177720be2878a317e1f529eab177e45fa4f1bd45a06a69779f7c963a705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d581a35520859a173fbf6058a00db5435952fa00e8e9ee6c788563d4cae2f3`

```dockerfile
```

-	Layers:
	-	`sha256:1fe61b448f6cbc544f9c72a56a148440a1f1e60eaffe9144cbc03096adacdf37`  
		Last Modified: Wed, 17 Dec 2025 22:35:02 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea30cf376da8351a758cad58a77f03776483c271a35b12b24e81530b12868a2e`  
		Last Modified: Wed, 17 Dec 2025 22:35:03 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; arm variant v6

```console
$ docker pull memcached@sha256:ea5a1cd530f7418ba73b2ec6d05aa7d073fa3e55362ad7c272c4dce82f2ee550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5611085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e6688be943a2b0ca333de7ee49b87d11b3b103acac53a8a1cda65827e164b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:35:21 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:35:22 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:57:18 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:57:18 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:57:18 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:57:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:57:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:57:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:57:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:57:19 GMT
USER memcache
# Wed, 17 Dec 2025 21:57:19 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:57:19 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0132a447b58e699f3e930eb400504a4dab7572b48682b411e172ca2f13e3837e`  
		Last Modified: Wed, 17 Dec 2025 21:57:31 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca221542481b910c1ab1534fbed6a1daa903dd46e7dec29a8e7e45e172ee4e98`  
		Last Modified: Wed, 17 Dec 2025 21:57:31 GMT  
		Size: 102.6 KB (102643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f509979790be1d0f32b1cb145ef690501c7b24933c62c28638d664ba9c700393`  
		Last Modified: Wed, 17 Dec 2025 21:57:32 GMT  
		Size: 1.9 MB (1939202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92b99708f0757173744dcefe8c10b63d6bb57457bb22a870a97d2e466b7dbe6`  
		Last Modified: Wed, 17 Dec 2025 21:57:31 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129c905b76006e4eac5697b73920244e0b167164eda691d8c9fce48e08d9a15a`  
		Last Modified: Wed, 17 Dec 2025 21:57:31 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:a01a7f359b5b6020f56a33f6c48f6d83addd590b6ffcfb8d9f39cbb014a3f79f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b004564c274eab1f4a9d5854d0515a6b15f0a9de9abfe0403b6717464af55ca2`

```dockerfile
```

-	Layers:
	-	`sha256:223be1dd282744e43fcfc8303bb2997a6a232da86d8a573d407d550c7f356417`  
		Last Modified: Wed, 17 Dec 2025 22:35:06 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; arm variant v7

```console
$ docker pull memcached@sha256:f8a13acc5d2817ee1e9df95f26a3647b2fc9361676acb4ccca0e106d0ff8d5d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5269348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c8d4d3ca238a3133af08dd38e3cd46b3afbc7409a4df18d893b9878e5001cb8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:35:30 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:35:31 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:27 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:27 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d9d8962df55145f5fd88847d7fbf0fd846221bbe5d3fda7baf9461e1be862b`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5b6235e518eb1a135149571028b21cc0487ffc5c0fb9eb823fa9f51c9b3b7f`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 92.4 KB (92365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b5f719f7a3d4ba338f20ab53593f3250818988f89bc9d1ac7f5d3412497aa5`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 1.9 MB (1897164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6783f23f1f96fa31f44928320bb651f00a3ac7c6f74bc8d4931b527ad745771`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9186b8b7184cef442ae3ed6a3feadcaa8f4ccc974ed5ae6c6cf8efe37e679f23`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:65ab94866fe80b34478423e645bc70428ca81e1ef0e523993f4da895ba84a4ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2093447767fcc95a5f23b4567561974625baad6244721a2fadf42a60f1d61397`

```dockerfile
```

-	Layers:
	-	`sha256:a8a1bb2b759719025d140e377ef6a401d06c350a48eea3cf16e20ecb526095d9`  
		Last Modified: Wed, 17 Dec 2025 22:35:09 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b06bbe6a45bdcd2081c0e485d5ab897b548b87391fe55dfaeac6bdabf63b6e4`  
		Last Modified: Wed, 17 Dec 2025 22:35:10 GMT  
		Size: 20.7 KB (20677 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:349dc973200279dddf8e6ce28d9128babfe84da2f011c88d675fda6b53d9b435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6284972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee78c99ff858f77e454879ddf462b94812f23a4a38585a7f04722f753f72bdf4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:37:24 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:37:25 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:40:13 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:40:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:40:13 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:40:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:40:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:40:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:40:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:40:13 GMT
USER memcache
# Wed, 17 Dec 2025 21:40:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:40:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e5de81b8fd10090b357c152c289b12543ba0233b02e1fea1f31abbb41c6ce6`  
		Last Modified: Wed, 17 Dec 2025 21:40:24 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a237d3db68cd689e683d8873b9f6662b963c1da855cb61f0404b9d218ce4ab`  
		Last Modified: Wed, 17 Dec 2025 21:40:24 GMT  
		Size: 121.9 KB (121870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab92f84f0d6a5d6415bf522e99e0ccc9603a821231233c659431c00d8f166e16`  
		Last Modified: Wed, 17 Dec 2025 21:40:24 GMT  
		Size: 2.0 MB (1966553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd31b8f53d48209a8b58d7add5eaa6252a50192d7d95307012fbe2a96c887175`  
		Last Modified: Wed, 17 Dec 2025 21:40:24 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db33d4acf9261f39e1a05295122f733c54555907dbe2700043b4e721fa2acf3b`  
		Last Modified: Wed, 17 Dec 2025 21:40:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:9a729809b661b20e6e8b44bb24413f513e1376d4dbe9ab0c1a4f7ed880149b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9883a54a8c4d45530843267722922526423a42a88046db1e58f74bed8bbe02d0`

```dockerfile
```

-	Layers:
	-	`sha256:a671bbb9a5464bb97f71429c00d4997635a1c127dc1b513aa48239e480106d60`  
		Last Modified: Wed, 17 Dec 2025 22:35:21 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36ef2adae88460c5dc2044a65093008d2beb76079d1f00bc5a7d862dbae0aa3b`  
		Last Modified: Wed, 17 Dec 2025 22:35:22 GMT  
		Size: 20.7 KB (20727 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; 386

```console
$ docker pull memcached@sha256:ca4c4cf71b28fb2b701d7c25e78c0cf8a8cd4de9424d86e7f906833f71f198eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5740718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f722d8a189d7c92749316efb1c7335a5873618eac12d5e5bc01d68127fb291b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:38:08 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:38:09 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:40:55 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:40:55 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:40:55 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:40:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:40:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:40:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:40:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:40:55 GMT
USER memcache
# Wed, 17 Dec 2025 21:40:55 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:40:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3527b4f952d5950d8caa74dc0d1759215000f2f0a195344f0239c7e2805fe2fc`  
		Last Modified: Wed, 03 Dec 2025 19:30:41 GMT  
		Size: 3.7 MB (3685856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d3f49b0de92207dfc061e70de94dd679b3ea12f97d99d1974a6c62164a159a`  
		Last Modified: Wed, 17 Dec 2025 21:41:06 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c266f269a50bef9007064361dc83371a1dd461aabe92bbec3d1e979412466de`  
		Last Modified: Wed, 17 Dec 2025 21:41:06 GMT  
		Size: 110.7 KB (110738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2053dfa7b6aa4f5a136466c1659669f25a4578930977fb585d209c5dfde8036d`  
		Last Modified: Wed, 17 Dec 2025 21:41:08 GMT  
		Size: 1.9 MB (1942772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ed31d7fa74d79df9efd8d4f443ada386f5729fbe324a9794e76baff2c1c493`  
		Last Modified: Wed, 17 Dec 2025 21:41:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91df285e3ed438acb3e9589dc178518e2db7c4bfa971348c72b6d0327a4ee79`  
		Last Modified: Wed, 17 Dec 2025 21:41:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:647a776f52f62548a4098b2e4b11214b4a5c1ee9685712ef80a2832ef32ca8c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40881c0a421ed132c378aef8bdbe39305aaaecc7deee9b7de9ae4f93188dcbd3`

```dockerfile
```

-	Layers:
	-	`sha256:f3beb40a7590bdda06e509d8ad4ecd2043849256a64e5ff660b19b1cd56a094a`  
		Last Modified: Wed, 17 Dec 2025 22:35:25 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38c8a2e4dad46bf55c80872707f6283533a800478b72bf885b684dd50e07eb32`  
		Last Modified: Wed, 17 Dec 2025 22:35:26 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; ppc64le

```console
$ docker pull memcached@sha256:3b02ff737dd16e237fd7406b5f7d02a513a983b5d2d53fa6cd313f1ef00b1f8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6030994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:530bbfb00fa1800e8532eef4fb114fc753724fcf50e1d1e12af0ca80cf6752a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:34:55 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:34:56 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:37:26 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:37:26 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:37:26 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:37:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:37:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:37:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:37:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:37:38 GMT
USER memcache
# Wed, 17 Dec 2025 21:37:38 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:37:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd01e04da0d57bffa2b60a957360f7a974a6b01b4d9acff8252fdec64a69f66`  
		Last Modified: Wed, 17 Dec 2025 21:38:00 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a239f5e0c0c7e367e7f132151c23b859390ef5a4cbc40fb10415655b7e4b8029`  
		Last Modified: Wed, 17 Dec 2025 21:38:00 GMT  
		Size: 126.3 KB (126252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5bf0071779f0057bb08ae7a6ce2aba364cd026a86150629c39a6a92aba920c`  
		Last Modified: Wed, 17 Dec 2025 21:38:00 GMT  
		Size: 2.1 MB (2076368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f39797f21825b46f2a91c72f603d5a656910a53e51d3e579f5f5e791aaac92`  
		Last Modified: Wed, 17 Dec 2025 21:38:00 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48cd6c111239cce7a47ed3674b56951e2830764b3576a0d26aa6924057642d4`  
		Last Modified: Wed, 17 Dec 2025 21:38:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:31b4659d5068108cb086c10f7eff5fc0f8d77afa0eb09b15fa3955924ad138ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4951610ebef7b9fc8a4a054b6085f3840f9ba32b81602af0d8c13ad838ba68`

```dockerfile
```

-	Layers:
	-	`sha256:c3757f7ab5b65afe79fc72a82e96ca02b81c222ba9649feccf145ce714cfc4b9`  
		Last Modified: Wed, 17 Dec 2025 22:35:29 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df6d5f19cafffe602863ac2b65054f5c05d4a497fece84a762d0aebdc057b39e`  
		Last Modified: Wed, 17 Dec 2025 22:35:29 GMT  
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
$ docker pull memcached@sha256:04733682f967e9788435bbddf864edb8e1bb9cc8671e1e868c74f82093fe62c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5856574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9063d29cfc1dce3d05c19ff319a9d3e5455146c60efe56e9ce56bfbf4d3c3927`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:34:52 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:34:53 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:38:01 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:01 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:01 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:01 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a990effa92b45935b52bc06653d39a48f5ed34d054f60e892ec417f8d919a6`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50bf0a9e48ac326120a5de8b5e0cd6b991d704ed4a66448d4fcc8c6ad640d10`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 114.3 KB (114287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b26a3c60d8c62feb971cedd3bd49cd1d5f4d0d0d0149017b32b1573727914be9`  
		Last Modified: Wed, 17 Dec 2025 21:38:19 GMT  
		Size: 2.0 MB (2017127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd733ace70e5f90e389ce8159cbda2291a52bf39e53e2ee4ea6eb8cbccc625e`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821f5deda63bf425c92464f3e686b9fda7f6200ddc49ebacb324b2a45ec0d633`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:19f5876a625b474e4eea9e963de1422ad480c97357d44cd8604896e2da517d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd50fa1a24cfb1dea4e93374baa1e967c2f0fddd79dfa74422b955c193ea89a6`

```dockerfile
```

-	Layers:
	-	`sha256:4d2cbcf3625eaa8b19de7227c701c14f9bd69378a6e698f5aee36b0eb01f2167`  
		Last Modified: Wed, 17 Dec 2025 22:35:35 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:235e217cf2514537b942b1cb8a5ffbbe2ecee441b9373e75871acd7a34391107`  
		Last Modified: Wed, 17 Dec 2025 22:35:36 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-trixie`

```console
$ docker pull memcached@sha256:6d4a394b5184f38fcdedabebc810a1e63861427e44215ec8a48a276678236df9
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
$ docker pull memcached@sha256:d8a6e6b246f27a6bbcdfda8a9a06e436178aa58c717448c641a6815f3cc38467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30627609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c80d74d8037160ffc9363dc03f0b6461d3c4cdd69da6460620b26838cb33a671`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 05:30:55 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 09 Dec 2025 05:31:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 05:56:35 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 09 Dec 2025 05:56:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 09 Dec 2025 05:56:35 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 09 Dec 2025 05:56:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 09 Dec 2025 05:56:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 05:56:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 09 Dec 2025 05:56:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Dec 2025 05:56:35 GMT
USER memcache
# Tue, 09 Dec 2025 05:56:35 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 09 Dec 2025 05:56:35 GMT
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
	-	`sha256:e9481f8b437fde8b1c89c79b65538c260df5216129bbe341f98c35935b4fe171`  
		Last Modified: Tue, 09 Dec 2025 05:57:38 GMT  
		Size: 2.2 MB (2219867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe3ccefbdcfdf466052c783e0982017ab232dd919bf46bb40b57edc66cee678`  
		Last Modified: Tue, 09 Dec 2025 05:57:38 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0be3eb5d00166beb14be204124c9c1033e288c0843f2c4aad6a372420a36c6`  
		Last Modified: Tue, 09 Dec 2025 05:57:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:0d07cca14f06f49448edd46f7de94275f31b7fd189fb725cb196bd96aa1ce642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:176f611a3de50a80e211655f970b224ae64d5ab4d2bb1aa8785a22161fe14060`

```dockerfile
```

-	Layers:
	-	`sha256:5f35bc7d6cd5ba3a512b097e6894fe90d53c248ba00f25fb4e1cc8f760d64548`  
		Last Modified: Tue, 09 Dec 2025 07:34:40 GMT  
		Size: 2.0 MB (2002192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18b98ed8b5ce7f2a905ffa540823ace4ea6f63ea74d51da31800c23d9fae6c1f`  
		Last Modified: Tue, 09 Dec 2025 07:34:41 GMT  
		Size: 22.2 KB (22226 bytes)  
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
$ docker pull memcached@sha256:6d4a394b5184f38fcdedabebc810a1e63861427e44215ec8a48a276678236df9
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
$ docker pull memcached@sha256:d8a6e6b246f27a6bbcdfda8a9a06e436178aa58c717448c641a6815f3cc38467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30627609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c80d74d8037160ffc9363dc03f0b6461d3c4cdd69da6460620b26838cb33a671`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 05:30:55 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 09 Dec 2025 05:31:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 05:56:35 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 09 Dec 2025 05:56:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 09 Dec 2025 05:56:35 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 09 Dec 2025 05:56:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 09 Dec 2025 05:56:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 05:56:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 09 Dec 2025 05:56:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Dec 2025 05:56:35 GMT
USER memcache
# Tue, 09 Dec 2025 05:56:35 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 09 Dec 2025 05:56:35 GMT
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
	-	`sha256:e9481f8b437fde8b1c89c79b65538c260df5216129bbe341f98c35935b4fe171`  
		Last Modified: Tue, 09 Dec 2025 05:57:38 GMT  
		Size: 2.2 MB (2219867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe3ccefbdcfdf466052c783e0982017ab232dd919bf46bb40b57edc66cee678`  
		Last Modified: Tue, 09 Dec 2025 05:57:38 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0be3eb5d00166beb14be204124c9c1033e288c0843f2c4aad6a372420a36c6`  
		Last Modified: Tue, 09 Dec 2025 05:57:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:0d07cca14f06f49448edd46f7de94275f31b7fd189fb725cb196bd96aa1ce642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:176f611a3de50a80e211655f970b224ae64d5ab4d2bb1aa8785a22161fe14060`

```dockerfile
```

-	Layers:
	-	`sha256:5f35bc7d6cd5ba3a512b097e6894fe90d53c248ba00f25fb4e1cc8f760d64548`  
		Last Modified: Tue, 09 Dec 2025 07:34:40 GMT  
		Size: 2.0 MB (2002192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18b98ed8b5ce7f2a905ffa540823ace4ea6f63ea74d51da31800c23d9fae6c1f`  
		Last Modified: Tue, 09 Dec 2025 07:34:41 GMT  
		Size: 22.2 KB (22226 bytes)  
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
$ docker pull memcached@sha256:4ec52eed643b17626643099f4ce0a142ef9dce004fc8bb32f582c0c31219dba9
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
$ docker pull memcached@sha256:65c25df73382e5ba4c57df3c2cccb5eb69702b813d07f9372f525e61225f0236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5955960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d33317a7accc6b056e21432db4903632531ace63c6085001ffb22caaa6d9d75b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:38:00 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:38:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:40:37 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:40:37 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:40:37 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:40:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:40:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:40:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:40:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:40:38 GMT
USER memcache
# Wed, 17 Dec 2025 21:40:38 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:40:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683f24283462cf58a8a6a81d7a140d0cd612c8120a019a56b2cb5f6f297d9465`  
		Last Modified: Wed, 17 Dec 2025 21:40:49 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450bd59379b8c57899254729c322d8ed1a1a7ca519dd92b78fc2d93e4e8a0b25`  
		Last Modified: Wed, 17 Dec 2025 21:40:49 GMT  
		Size: 106.0 KB (106041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2091c3522fccefd861318754918a244e21e5582890c29a366f8a5deb524e60af`  
		Last Modified: Wed, 17 Dec 2025 21:40:49 GMT  
		Size: 2.0 MB (1989255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9898efa8e26f703b25503f6a996e1f99a1fd8128fceb41ffe2e64c68a38599`  
		Last Modified: Wed, 17 Dec 2025 21:40:49 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2662bcfc6adeacc0aa8fd4c9d65e40532dd669f2516c02dc4a8ed4ce03647a0f`  
		Last Modified: Wed, 17 Dec 2025 21:40:49 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:e2ce9177720be2878a317e1f529eab177e45fa4f1bd45a06a69779f7c963a705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d581a35520859a173fbf6058a00db5435952fa00e8e9ee6c788563d4cae2f3`

```dockerfile
```

-	Layers:
	-	`sha256:1fe61b448f6cbc544f9c72a56a148440a1f1e60eaffe9144cbc03096adacdf37`  
		Last Modified: Wed, 17 Dec 2025 22:35:02 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea30cf376da8351a758cad58a77f03776483c271a35b12b24e81530b12868a2e`  
		Last Modified: Wed, 17 Dec 2025 22:35:03 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:ea5a1cd530f7418ba73b2ec6d05aa7d073fa3e55362ad7c272c4dce82f2ee550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5611085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e6688be943a2b0ca333de7ee49b87d11b3b103acac53a8a1cda65827e164b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:35:21 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:35:22 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:57:18 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:57:18 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:57:18 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:57:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:57:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:57:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:57:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:57:19 GMT
USER memcache
# Wed, 17 Dec 2025 21:57:19 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:57:19 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0132a447b58e699f3e930eb400504a4dab7572b48682b411e172ca2f13e3837e`  
		Last Modified: Wed, 17 Dec 2025 21:57:31 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca221542481b910c1ab1534fbed6a1daa903dd46e7dec29a8e7e45e172ee4e98`  
		Last Modified: Wed, 17 Dec 2025 21:57:31 GMT  
		Size: 102.6 KB (102643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f509979790be1d0f32b1cb145ef690501c7b24933c62c28638d664ba9c700393`  
		Last Modified: Wed, 17 Dec 2025 21:57:32 GMT  
		Size: 1.9 MB (1939202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92b99708f0757173744dcefe8c10b63d6bb57457bb22a870a97d2e466b7dbe6`  
		Last Modified: Wed, 17 Dec 2025 21:57:31 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129c905b76006e4eac5697b73920244e0b167164eda691d8c9fce48e08d9a15a`  
		Last Modified: Wed, 17 Dec 2025 21:57:31 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:a01a7f359b5b6020f56a33f6c48f6d83addd590b6ffcfb8d9f39cbb014a3f79f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b004564c274eab1f4a9d5854d0515a6b15f0a9de9abfe0403b6717464af55ca2`

```dockerfile
```

-	Layers:
	-	`sha256:223be1dd282744e43fcfc8303bb2997a6a232da86d8a573d407d550c7f356417`  
		Last Modified: Wed, 17 Dec 2025 22:35:06 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:f8a13acc5d2817ee1e9df95f26a3647b2fc9361676acb4ccca0e106d0ff8d5d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5269348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c8d4d3ca238a3133af08dd38e3cd46b3afbc7409a4df18d893b9878e5001cb8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:35:30 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:35:31 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:27 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:27 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d9d8962df55145f5fd88847d7fbf0fd846221bbe5d3fda7baf9461e1be862b`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5b6235e518eb1a135149571028b21cc0487ffc5c0fb9eb823fa9f51c9b3b7f`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 92.4 KB (92365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b5f719f7a3d4ba338f20ab53593f3250818988f89bc9d1ac7f5d3412497aa5`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 1.9 MB (1897164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6783f23f1f96fa31f44928320bb651f00a3ac7c6f74bc8d4931b527ad745771`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9186b8b7184cef442ae3ed6a3feadcaa8f4ccc974ed5ae6c6cf8efe37e679f23`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:65ab94866fe80b34478423e645bc70428ca81e1ef0e523993f4da895ba84a4ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2093447767fcc95a5f23b4567561974625baad6244721a2fadf42a60f1d61397`

```dockerfile
```

-	Layers:
	-	`sha256:a8a1bb2b759719025d140e377ef6a401d06c350a48eea3cf16e20ecb526095d9`  
		Last Modified: Wed, 17 Dec 2025 22:35:09 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b06bbe6a45bdcd2081c0e485d5ab897b548b87391fe55dfaeac6bdabf63b6e4`  
		Last Modified: Wed, 17 Dec 2025 22:35:10 GMT  
		Size: 20.7 KB (20677 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:349dc973200279dddf8e6ce28d9128babfe84da2f011c88d675fda6b53d9b435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6284972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee78c99ff858f77e454879ddf462b94812f23a4a38585a7f04722f753f72bdf4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:37:24 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:37:25 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:40:13 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:40:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:40:13 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:40:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:40:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:40:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:40:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:40:13 GMT
USER memcache
# Wed, 17 Dec 2025 21:40:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:40:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e5de81b8fd10090b357c152c289b12543ba0233b02e1fea1f31abbb41c6ce6`  
		Last Modified: Wed, 17 Dec 2025 21:40:24 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a237d3db68cd689e683d8873b9f6662b963c1da855cb61f0404b9d218ce4ab`  
		Last Modified: Wed, 17 Dec 2025 21:40:24 GMT  
		Size: 121.9 KB (121870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab92f84f0d6a5d6415bf522e99e0ccc9603a821231233c659431c00d8f166e16`  
		Last Modified: Wed, 17 Dec 2025 21:40:24 GMT  
		Size: 2.0 MB (1966553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd31b8f53d48209a8b58d7add5eaa6252a50192d7d95307012fbe2a96c887175`  
		Last Modified: Wed, 17 Dec 2025 21:40:24 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db33d4acf9261f39e1a05295122f733c54555907dbe2700043b4e721fa2acf3b`  
		Last Modified: Wed, 17 Dec 2025 21:40:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9a729809b661b20e6e8b44bb24413f513e1376d4dbe9ab0c1a4f7ed880149b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9883a54a8c4d45530843267722922526423a42a88046db1e58f74bed8bbe02d0`

```dockerfile
```

-	Layers:
	-	`sha256:a671bbb9a5464bb97f71429c00d4997635a1c127dc1b513aa48239e480106d60`  
		Last Modified: Wed, 17 Dec 2025 22:35:21 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36ef2adae88460c5dc2044a65093008d2beb76079d1f00bc5a7d862dbae0aa3b`  
		Last Modified: Wed, 17 Dec 2025 22:35:22 GMT  
		Size: 20.7 KB (20727 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:ca4c4cf71b28fb2b701d7c25e78c0cf8a8cd4de9424d86e7f906833f71f198eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5740718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f722d8a189d7c92749316efb1c7335a5873618eac12d5e5bc01d68127fb291b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:38:08 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:38:09 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:40:55 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:40:55 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:40:55 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:40:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:40:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:40:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:40:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:40:55 GMT
USER memcache
# Wed, 17 Dec 2025 21:40:55 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:40:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3527b4f952d5950d8caa74dc0d1759215000f2f0a195344f0239c7e2805fe2fc`  
		Last Modified: Wed, 03 Dec 2025 19:30:41 GMT  
		Size: 3.7 MB (3685856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d3f49b0de92207dfc061e70de94dd679b3ea12f97d99d1974a6c62164a159a`  
		Last Modified: Wed, 17 Dec 2025 21:41:06 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c266f269a50bef9007064361dc83371a1dd461aabe92bbec3d1e979412466de`  
		Last Modified: Wed, 17 Dec 2025 21:41:06 GMT  
		Size: 110.7 KB (110738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2053dfa7b6aa4f5a136466c1659669f25a4578930977fb585d209c5dfde8036d`  
		Last Modified: Wed, 17 Dec 2025 21:41:08 GMT  
		Size: 1.9 MB (1942772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ed31d7fa74d79df9efd8d4f443ada386f5729fbe324a9794e76baff2c1c493`  
		Last Modified: Wed, 17 Dec 2025 21:41:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91df285e3ed438acb3e9589dc178518e2db7c4bfa971348c72b6d0327a4ee79`  
		Last Modified: Wed, 17 Dec 2025 21:41:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:647a776f52f62548a4098b2e4b11214b4a5c1ee9685712ef80a2832ef32ca8c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40881c0a421ed132c378aef8bdbe39305aaaecc7deee9b7de9ae4f93188dcbd3`

```dockerfile
```

-	Layers:
	-	`sha256:f3beb40a7590bdda06e509d8ad4ecd2043849256a64e5ff660b19b1cd56a094a`  
		Last Modified: Wed, 17 Dec 2025 22:35:25 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38c8a2e4dad46bf55c80872707f6283533a800478b72bf885b684dd50e07eb32`  
		Last Modified: Wed, 17 Dec 2025 22:35:26 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:3b02ff737dd16e237fd7406b5f7d02a513a983b5d2d53fa6cd313f1ef00b1f8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6030994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:530bbfb00fa1800e8532eef4fb114fc753724fcf50e1d1e12af0ca80cf6752a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:34:55 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:34:56 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:37:26 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:37:26 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:37:26 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:37:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:37:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:37:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:37:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:37:38 GMT
USER memcache
# Wed, 17 Dec 2025 21:37:38 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:37:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd01e04da0d57bffa2b60a957360f7a974a6b01b4d9acff8252fdec64a69f66`  
		Last Modified: Wed, 17 Dec 2025 21:38:00 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a239f5e0c0c7e367e7f132151c23b859390ef5a4cbc40fb10415655b7e4b8029`  
		Last Modified: Wed, 17 Dec 2025 21:38:00 GMT  
		Size: 126.3 KB (126252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5bf0071779f0057bb08ae7a6ce2aba364cd026a86150629c39a6a92aba920c`  
		Last Modified: Wed, 17 Dec 2025 21:38:00 GMT  
		Size: 2.1 MB (2076368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f39797f21825b46f2a91c72f603d5a656910a53e51d3e579f5f5e791aaac92`  
		Last Modified: Wed, 17 Dec 2025 21:38:00 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48cd6c111239cce7a47ed3674b56951e2830764b3576a0d26aa6924057642d4`  
		Last Modified: Wed, 17 Dec 2025 21:38:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:31b4659d5068108cb086c10f7eff5fc0f8d77afa0eb09b15fa3955924ad138ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4951610ebef7b9fc8a4a054b6085f3840f9ba32b81602af0d8c13ad838ba68`

```dockerfile
```

-	Layers:
	-	`sha256:c3757f7ab5b65afe79fc72a82e96ca02b81c222ba9649feccf145ce714cfc4b9`  
		Last Modified: Wed, 17 Dec 2025 22:35:29 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df6d5f19cafffe602863ac2b65054f5c05d4a497fece84a762d0aebdc057b39e`  
		Last Modified: Wed, 17 Dec 2025 22:35:29 GMT  
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
$ docker pull memcached@sha256:04733682f967e9788435bbddf864edb8e1bb9cc8671e1e868c74f82093fe62c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5856574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9063d29cfc1dce3d05c19ff319a9d3e5455146c60efe56e9ce56bfbf4d3c3927`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:34:52 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:34:53 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:38:01 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:01 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:01 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:01 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a990effa92b45935b52bc06653d39a48f5ed34d054f60e892ec417f8d919a6`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50bf0a9e48ac326120a5de8b5e0cd6b991d704ed4a66448d4fcc8c6ad640d10`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 114.3 KB (114287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b26a3c60d8c62feb971cedd3bd49cd1d5f4d0d0d0149017b32b1573727914be9`  
		Last Modified: Wed, 17 Dec 2025 21:38:19 GMT  
		Size: 2.0 MB (2017127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd733ace70e5f90e389ce8159cbda2291a52bf39e53e2ee4ea6eb8cbccc625e`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821f5deda63bf425c92464f3e686b9fda7f6200ddc49ebacb324b2a45ec0d633`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:19f5876a625b474e4eea9e963de1422ad480c97357d44cd8604896e2da517d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd50fa1a24cfb1dea4e93374baa1e967c2f0fddd79dfa74422b955c193ea89a6`

```dockerfile
```

-	Layers:
	-	`sha256:4d2cbcf3625eaa8b19de7227c701c14f9bd69378a6e698f5aee36b0eb01f2167`  
		Last Modified: Wed, 17 Dec 2025 22:35:35 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:235e217cf2514537b942b1cb8a5ffbbe2ecee441b9373e75871acd7a34391107`  
		Last Modified: Wed, 17 Dec 2025 22:35:36 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine3.23`

```console
$ docker pull memcached@sha256:4ec52eed643b17626643099f4ce0a142ef9dce004fc8bb32f582c0c31219dba9
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
$ docker pull memcached@sha256:65c25df73382e5ba4c57df3c2cccb5eb69702b813d07f9372f525e61225f0236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5955960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d33317a7accc6b056e21432db4903632531ace63c6085001ffb22caaa6d9d75b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:38:00 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:38:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:40:37 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:40:37 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:40:37 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:40:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:40:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:40:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:40:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:40:38 GMT
USER memcache
# Wed, 17 Dec 2025 21:40:38 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:40:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683f24283462cf58a8a6a81d7a140d0cd612c8120a019a56b2cb5f6f297d9465`  
		Last Modified: Wed, 17 Dec 2025 21:40:49 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450bd59379b8c57899254729c322d8ed1a1a7ca519dd92b78fc2d93e4e8a0b25`  
		Last Modified: Wed, 17 Dec 2025 21:40:49 GMT  
		Size: 106.0 KB (106041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2091c3522fccefd861318754918a244e21e5582890c29a366f8a5deb524e60af`  
		Last Modified: Wed, 17 Dec 2025 21:40:49 GMT  
		Size: 2.0 MB (1989255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9898efa8e26f703b25503f6a996e1f99a1fd8128fceb41ffe2e64c68a38599`  
		Last Modified: Wed, 17 Dec 2025 21:40:49 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2662bcfc6adeacc0aa8fd4c9d65e40532dd669f2516c02dc4a8ed4ce03647a0f`  
		Last Modified: Wed, 17 Dec 2025 21:40:49 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:e2ce9177720be2878a317e1f529eab177e45fa4f1bd45a06a69779f7c963a705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d581a35520859a173fbf6058a00db5435952fa00e8e9ee6c788563d4cae2f3`

```dockerfile
```

-	Layers:
	-	`sha256:1fe61b448f6cbc544f9c72a56a148440a1f1e60eaffe9144cbc03096adacdf37`  
		Last Modified: Wed, 17 Dec 2025 22:35:02 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea30cf376da8351a758cad58a77f03776483c271a35b12b24e81530b12868a2e`  
		Last Modified: Wed, 17 Dec 2025 22:35:03 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; arm variant v6

```console
$ docker pull memcached@sha256:ea5a1cd530f7418ba73b2ec6d05aa7d073fa3e55362ad7c272c4dce82f2ee550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5611085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e6688be943a2b0ca333de7ee49b87d11b3b103acac53a8a1cda65827e164b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:35:21 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:35:22 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:57:18 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:57:18 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:57:18 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:57:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:57:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:57:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:57:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:57:19 GMT
USER memcache
# Wed, 17 Dec 2025 21:57:19 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:57:19 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0132a447b58e699f3e930eb400504a4dab7572b48682b411e172ca2f13e3837e`  
		Last Modified: Wed, 17 Dec 2025 21:57:31 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca221542481b910c1ab1534fbed6a1daa903dd46e7dec29a8e7e45e172ee4e98`  
		Last Modified: Wed, 17 Dec 2025 21:57:31 GMT  
		Size: 102.6 KB (102643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f509979790be1d0f32b1cb145ef690501c7b24933c62c28638d664ba9c700393`  
		Last Modified: Wed, 17 Dec 2025 21:57:32 GMT  
		Size: 1.9 MB (1939202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92b99708f0757173744dcefe8c10b63d6bb57457bb22a870a97d2e466b7dbe6`  
		Last Modified: Wed, 17 Dec 2025 21:57:31 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129c905b76006e4eac5697b73920244e0b167164eda691d8c9fce48e08d9a15a`  
		Last Modified: Wed, 17 Dec 2025 21:57:31 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:a01a7f359b5b6020f56a33f6c48f6d83addd590b6ffcfb8d9f39cbb014a3f79f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b004564c274eab1f4a9d5854d0515a6b15f0a9de9abfe0403b6717464af55ca2`

```dockerfile
```

-	Layers:
	-	`sha256:223be1dd282744e43fcfc8303bb2997a6a232da86d8a573d407d550c7f356417`  
		Last Modified: Wed, 17 Dec 2025 22:35:06 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; arm variant v7

```console
$ docker pull memcached@sha256:f8a13acc5d2817ee1e9df95f26a3647b2fc9361676acb4ccca0e106d0ff8d5d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5269348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c8d4d3ca238a3133af08dd38e3cd46b3afbc7409a4df18d893b9878e5001cb8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:35:30 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:35:31 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:27 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:27 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d9d8962df55145f5fd88847d7fbf0fd846221bbe5d3fda7baf9461e1be862b`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5b6235e518eb1a135149571028b21cc0487ffc5c0fb9eb823fa9f51c9b3b7f`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 92.4 KB (92365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b5f719f7a3d4ba338f20ab53593f3250818988f89bc9d1ac7f5d3412497aa5`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 1.9 MB (1897164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6783f23f1f96fa31f44928320bb651f00a3ac7c6f74bc8d4931b527ad745771`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9186b8b7184cef442ae3ed6a3feadcaa8f4ccc974ed5ae6c6cf8efe37e679f23`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:65ab94866fe80b34478423e645bc70428ca81e1ef0e523993f4da895ba84a4ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2093447767fcc95a5f23b4567561974625baad6244721a2fadf42a60f1d61397`

```dockerfile
```

-	Layers:
	-	`sha256:a8a1bb2b759719025d140e377ef6a401d06c350a48eea3cf16e20ecb526095d9`  
		Last Modified: Wed, 17 Dec 2025 22:35:09 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b06bbe6a45bdcd2081c0e485d5ab897b548b87391fe55dfaeac6bdabf63b6e4`  
		Last Modified: Wed, 17 Dec 2025 22:35:10 GMT  
		Size: 20.7 KB (20677 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:349dc973200279dddf8e6ce28d9128babfe84da2f011c88d675fda6b53d9b435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6284972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee78c99ff858f77e454879ddf462b94812f23a4a38585a7f04722f753f72bdf4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:37:24 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:37:25 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:40:13 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:40:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:40:13 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:40:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:40:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:40:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:40:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:40:13 GMT
USER memcache
# Wed, 17 Dec 2025 21:40:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:40:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e5de81b8fd10090b357c152c289b12543ba0233b02e1fea1f31abbb41c6ce6`  
		Last Modified: Wed, 17 Dec 2025 21:40:24 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a237d3db68cd689e683d8873b9f6662b963c1da855cb61f0404b9d218ce4ab`  
		Last Modified: Wed, 17 Dec 2025 21:40:24 GMT  
		Size: 121.9 KB (121870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab92f84f0d6a5d6415bf522e99e0ccc9603a821231233c659431c00d8f166e16`  
		Last Modified: Wed, 17 Dec 2025 21:40:24 GMT  
		Size: 2.0 MB (1966553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd31b8f53d48209a8b58d7add5eaa6252a50192d7d95307012fbe2a96c887175`  
		Last Modified: Wed, 17 Dec 2025 21:40:24 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db33d4acf9261f39e1a05295122f733c54555907dbe2700043b4e721fa2acf3b`  
		Last Modified: Wed, 17 Dec 2025 21:40:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:9a729809b661b20e6e8b44bb24413f513e1376d4dbe9ab0c1a4f7ed880149b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9883a54a8c4d45530843267722922526423a42a88046db1e58f74bed8bbe02d0`

```dockerfile
```

-	Layers:
	-	`sha256:a671bbb9a5464bb97f71429c00d4997635a1c127dc1b513aa48239e480106d60`  
		Last Modified: Wed, 17 Dec 2025 22:35:21 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36ef2adae88460c5dc2044a65093008d2beb76079d1f00bc5a7d862dbae0aa3b`  
		Last Modified: Wed, 17 Dec 2025 22:35:22 GMT  
		Size: 20.7 KB (20727 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; 386

```console
$ docker pull memcached@sha256:ca4c4cf71b28fb2b701d7c25e78c0cf8a8cd4de9424d86e7f906833f71f198eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5740718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f722d8a189d7c92749316efb1c7335a5873618eac12d5e5bc01d68127fb291b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:38:08 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:38:09 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:40:55 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:40:55 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:40:55 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:40:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:40:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:40:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:40:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:40:55 GMT
USER memcache
# Wed, 17 Dec 2025 21:40:55 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:40:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3527b4f952d5950d8caa74dc0d1759215000f2f0a195344f0239c7e2805fe2fc`  
		Last Modified: Wed, 03 Dec 2025 19:30:41 GMT  
		Size: 3.7 MB (3685856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d3f49b0de92207dfc061e70de94dd679b3ea12f97d99d1974a6c62164a159a`  
		Last Modified: Wed, 17 Dec 2025 21:41:06 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c266f269a50bef9007064361dc83371a1dd461aabe92bbec3d1e979412466de`  
		Last Modified: Wed, 17 Dec 2025 21:41:06 GMT  
		Size: 110.7 KB (110738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2053dfa7b6aa4f5a136466c1659669f25a4578930977fb585d209c5dfde8036d`  
		Last Modified: Wed, 17 Dec 2025 21:41:08 GMT  
		Size: 1.9 MB (1942772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ed31d7fa74d79df9efd8d4f443ada386f5729fbe324a9794e76baff2c1c493`  
		Last Modified: Wed, 17 Dec 2025 21:41:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91df285e3ed438acb3e9589dc178518e2db7c4bfa971348c72b6d0327a4ee79`  
		Last Modified: Wed, 17 Dec 2025 21:41:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:647a776f52f62548a4098b2e4b11214b4a5c1ee9685712ef80a2832ef32ca8c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40881c0a421ed132c378aef8bdbe39305aaaecc7deee9b7de9ae4f93188dcbd3`

```dockerfile
```

-	Layers:
	-	`sha256:f3beb40a7590bdda06e509d8ad4ecd2043849256a64e5ff660b19b1cd56a094a`  
		Last Modified: Wed, 17 Dec 2025 22:35:25 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38c8a2e4dad46bf55c80872707f6283533a800478b72bf885b684dd50e07eb32`  
		Last Modified: Wed, 17 Dec 2025 22:35:26 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; ppc64le

```console
$ docker pull memcached@sha256:3b02ff737dd16e237fd7406b5f7d02a513a983b5d2d53fa6cd313f1ef00b1f8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6030994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:530bbfb00fa1800e8532eef4fb114fc753724fcf50e1d1e12af0ca80cf6752a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:34:55 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:34:56 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:37:26 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:37:26 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:37:26 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:37:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:37:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:37:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:37:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:37:38 GMT
USER memcache
# Wed, 17 Dec 2025 21:37:38 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:37:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd01e04da0d57bffa2b60a957360f7a974a6b01b4d9acff8252fdec64a69f66`  
		Last Modified: Wed, 17 Dec 2025 21:38:00 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a239f5e0c0c7e367e7f132151c23b859390ef5a4cbc40fb10415655b7e4b8029`  
		Last Modified: Wed, 17 Dec 2025 21:38:00 GMT  
		Size: 126.3 KB (126252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5bf0071779f0057bb08ae7a6ce2aba364cd026a86150629c39a6a92aba920c`  
		Last Modified: Wed, 17 Dec 2025 21:38:00 GMT  
		Size: 2.1 MB (2076368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f39797f21825b46f2a91c72f603d5a656910a53e51d3e579f5f5e791aaac92`  
		Last Modified: Wed, 17 Dec 2025 21:38:00 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48cd6c111239cce7a47ed3674b56951e2830764b3576a0d26aa6924057642d4`  
		Last Modified: Wed, 17 Dec 2025 21:38:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:31b4659d5068108cb086c10f7eff5fc0f8d77afa0eb09b15fa3955924ad138ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4951610ebef7b9fc8a4a054b6085f3840f9ba32b81602af0d8c13ad838ba68`

```dockerfile
```

-	Layers:
	-	`sha256:c3757f7ab5b65afe79fc72a82e96ca02b81c222ba9649feccf145ce714cfc4b9`  
		Last Modified: Wed, 17 Dec 2025 22:35:29 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df6d5f19cafffe602863ac2b65054f5c05d4a497fece84a762d0aebdc057b39e`  
		Last Modified: Wed, 17 Dec 2025 22:35:29 GMT  
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
$ docker pull memcached@sha256:04733682f967e9788435bbddf864edb8e1bb9cc8671e1e868c74f82093fe62c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5856574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9063d29cfc1dce3d05c19ff319a9d3e5455146c60efe56e9ce56bfbf4d3c3927`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:34:52 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:34:53 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:38:01 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:01 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:01 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:01 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a990effa92b45935b52bc06653d39a48f5ed34d054f60e892ec417f8d919a6`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50bf0a9e48ac326120a5de8b5e0cd6b991d704ed4a66448d4fcc8c6ad640d10`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 114.3 KB (114287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b26a3c60d8c62feb971cedd3bd49cd1d5f4d0d0d0149017b32b1573727914be9`  
		Last Modified: Wed, 17 Dec 2025 21:38:19 GMT  
		Size: 2.0 MB (2017127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd733ace70e5f90e389ce8159cbda2291a52bf39e53e2ee4ea6eb8cbccc625e`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821f5deda63bf425c92464f3e686b9fda7f6200ddc49ebacb324b2a45ec0d633`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:19f5876a625b474e4eea9e963de1422ad480c97357d44cd8604896e2da517d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd50fa1a24cfb1dea4e93374baa1e967c2f0fddd79dfa74422b955c193ea89a6`

```dockerfile
```

-	Layers:
	-	`sha256:4d2cbcf3625eaa8b19de7227c701c14f9bd69378a6e698f5aee36b0eb01f2167`  
		Last Modified: Wed, 17 Dec 2025 22:35:35 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:235e217cf2514537b942b1cb8a5ffbbe2ecee441b9373e75871acd7a34391107`  
		Last Modified: Wed, 17 Dec 2025 22:35:36 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-trixie`

```console
$ docker pull memcached@sha256:6d4a394b5184f38fcdedabebc810a1e63861427e44215ec8a48a276678236df9
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
$ docker pull memcached@sha256:d8a6e6b246f27a6bbcdfda8a9a06e436178aa58c717448c641a6815f3cc38467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30627609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c80d74d8037160ffc9363dc03f0b6461d3c4cdd69da6460620b26838cb33a671`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 05:30:55 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 09 Dec 2025 05:31:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 05:56:35 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 09 Dec 2025 05:56:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 09 Dec 2025 05:56:35 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 09 Dec 2025 05:56:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 09 Dec 2025 05:56:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 05:56:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 09 Dec 2025 05:56:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Dec 2025 05:56:35 GMT
USER memcache
# Tue, 09 Dec 2025 05:56:35 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 09 Dec 2025 05:56:35 GMT
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
	-	`sha256:e9481f8b437fde8b1c89c79b65538c260df5216129bbe341f98c35935b4fe171`  
		Last Modified: Tue, 09 Dec 2025 05:57:38 GMT  
		Size: 2.2 MB (2219867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe3ccefbdcfdf466052c783e0982017ab232dd919bf46bb40b57edc66cee678`  
		Last Modified: Tue, 09 Dec 2025 05:57:38 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0be3eb5d00166beb14be204124c9c1033e288c0843f2c4aad6a372420a36c6`  
		Last Modified: Tue, 09 Dec 2025 05:57:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:0d07cca14f06f49448edd46f7de94275f31b7fd189fb725cb196bd96aa1ce642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:176f611a3de50a80e211655f970b224ae64d5ab4d2bb1aa8785a22161fe14060`

```dockerfile
```

-	Layers:
	-	`sha256:5f35bc7d6cd5ba3a512b097e6894fe90d53c248ba00f25fb4e1cc8f760d64548`  
		Last Modified: Tue, 09 Dec 2025 07:34:40 GMT  
		Size: 2.0 MB (2002192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18b98ed8b5ce7f2a905ffa540823ace4ea6f63ea74d51da31800c23d9fae6c1f`  
		Last Modified: Tue, 09 Dec 2025 07:34:41 GMT  
		Size: 22.2 KB (22226 bytes)  
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
$ docker pull memcached@sha256:19007562d3a6fbafd8deb9d6fd5cc0ac3fecdba7e4112a5e254b1cfec906a9f6
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
$ docker pull memcached@sha256:1f30c9f207fc53a00216e36f03405482d94a339b2f53937e8749309fe7506861
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
$ docker pull memcached@sha256:65c25df73382e5ba4c57df3c2cccb5eb69702b813d07f9372f525e61225f0236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5955960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d33317a7accc6b056e21432db4903632531ace63c6085001ffb22caaa6d9d75b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:38:00 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:38:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:40:37 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:40:37 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:40:37 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:40:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:40:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:40:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:40:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:40:38 GMT
USER memcache
# Wed, 17 Dec 2025 21:40:38 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:40:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683f24283462cf58a8a6a81d7a140d0cd612c8120a019a56b2cb5f6f297d9465`  
		Last Modified: Wed, 17 Dec 2025 21:40:49 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450bd59379b8c57899254729c322d8ed1a1a7ca519dd92b78fc2d93e4e8a0b25`  
		Last Modified: Wed, 17 Dec 2025 21:40:49 GMT  
		Size: 106.0 KB (106041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2091c3522fccefd861318754918a244e21e5582890c29a366f8a5deb524e60af`  
		Last Modified: Wed, 17 Dec 2025 21:40:49 GMT  
		Size: 2.0 MB (1989255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9898efa8e26f703b25503f6a996e1f99a1fd8128fceb41ffe2e64c68a38599`  
		Last Modified: Wed, 17 Dec 2025 21:40:49 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2662bcfc6adeacc0aa8fd4c9d65e40532dd669f2516c02dc4a8ed4ce03647a0f`  
		Last Modified: Wed, 17 Dec 2025 21:40:49 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:e2ce9177720be2878a317e1f529eab177e45fa4f1bd45a06a69779f7c963a705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d581a35520859a173fbf6058a00db5435952fa00e8e9ee6c788563d4cae2f3`

```dockerfile
```

-	Layers:
	-	`sha256:1fe61b448f6cbc544f9c72a56a148440a1f1e60eaffe9144cbc03096adacdf37`  
		Last Modified: Wed, 17 Dec 2025 22:35:02 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea30cf376da8351a758cad58a77f03776483c271a35b12b24e81530b12868a2e`  
		Last Modified: Wed, 17 Dec 2025 22:35:03 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:ea5a1cd530f7418ba73b2ec6d05aa7d073fa3e55362ad7c272c4dce82f2ee550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5611085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e6688be943a2b0ca333de7ee49b87d11b3b103acac53a8a1cda65827e164b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:35:21 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:35:22 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:57:18 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:57:18 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:57:18 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:57:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:57:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:57:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:57:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:57:19 GMT
USER memcache
# Wed, 17 Dec 2025 21:57:19 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:57:19 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0132a447b58e699f3e930eb400504a4dab7572b48682b411e172ca2f13e3837e`  
		Last Modified: Wed, 17 Dec 2025 21:57:31 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca221542481b910c1ab1534fbed6a1daa903dd46e7dec29a8e7e45e172ee4e98`  
		Last Modified: Wed, 17 Dec 2025 21:57:31 GMT  
		Size: 102.6 KB (102643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f509979790be1d0f32b1cb145ef690501c7b24933c62c28638d664ba9c700393`  
		Last Modified: Wed, 17 Dec 2025 21:57:32 GMT  
		Size: 1.9 MB (1939202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92b99708f0757173744dcefe8c10b63d6bb57457bb22a870a97d2e466b7dbe6`  
		Last Modified: Wed, 17 Dec 2025 21:57:31 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129c905b76006e4eac5697b73920244e0b167164eda691d8c9fce48e08d9a15a`  
		Last Modified: Wed, 17 Dec 2025 21:57:31 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:a01a7f359b5b6020f56a33f6c48f6d83addd590b6ffcfb8d9f39cbb014a3f79f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b004564c274eab1f4a9d5854d0515a6b15f0a9de9abfe0403b6717464af55ca2`

```dockerfile
```

-	Layers:
	-	`sha256:223be1dd282744e43fcfc8303bb2997a6a232da86d8a573d407d550c7f356417`  
		Last Modified: Wed, 17 Dec 2025 22:35:06 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:f8a13acc5d2817ee1e9df95f26a3647b2fc9361676acb4ccca0e106d0ff8d5d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5269348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c8d4d3ca238a3133af08dd38e3cd46b3afbc7409a4df18d893b9878e5001cb8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:35:30 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:35:31 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:27 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:27 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d9d8962df55145f5fd88847d7fbf0fd846221bbe5d3fda7baf9461e1be862b`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5b6235e518eb1a135149571028b21cc0487ffc5c0fb9eb823fa9f51c9b3b7f`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 92.4 KB (92365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b5f719f7a3d4ba338f20ab53593f3250818988f89bc9d1ac7f5d3412497aa5`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 1.9 MB (1897164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6783f23f1f96fa31f44928320bb651f00a3ac7c6f74bc8d4931b527ad745771`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9186b8b7184cef442ae3ed6a3feadcaa8f4ccc974ed5ae6c6cf8efe37e679f23`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:65ab94866fe80b34478423e645bc70428ca81e1ef0e523993f4da895ba84a4ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2093447767fcc95a5f23b4567561974625baad6244721a2fadf42a60f1d61397`

```dockerfile
```

-	Layers:
	-	`sha256:a8a1bb2b759719025d140e377ef6a401d06c350a48eea3cf16e20ecb526095d9`  
		Last Modified: Wed, 17 Dec 2025 22:35:09 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b06bbe6a45bdcd2081c0e485d5ab897b548b87391fe55dfaeac6bdabf63b6e4`  
		Last Modified: Wed, 17 Dec 2025 22:35:10 GMT  
		Size: 20.7 KB (20677 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:349dc973200279dddf8e6ce28d9128babfe84da2f011c88d675fda6b53d9b435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6284972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee78c99ff858f77e454879ddf462b94812f23a4a38585a7f04722f753f72bdf4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:37:24 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:37:25 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:40:13 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:40:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:40:13 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:40:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:40:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:40:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:40:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:40:13 GMT
USER memcache
# Wed, 17 Dec 2025 21:40:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:40:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e5de81b8fd10090b357c152c289b12543ba0233b02e1fea1f31abbb41c6ce6`  
		Last Modified: Wed, 17 Dec 2025 21:40:24 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a237d3db68cd689e683d8873b9f6662b963c1da855cb61f0404b9d218ce4ab`  
		Last Modified: Wed, 17 Dec 2025 21:40:24 GMT  
		Size: 121.9 KB (121870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab92f84f0d6a5d6415bf522e99e0ccc9603a821231233c659431c00d8f166e16`  
		Last Modified: Wed, 17 Dec 2025 21:40:24 GMT  
		Size: 2.0 MB (1966553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd31b8f53d48209a8b58d7add5eaa6252a50192d7d95307012fbe2a96c887175`  
		Last Modified: Wed, 17 Dec 2025 21:40:24 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db33d4acf9261f39e1a05295122f733c54555907dbe2700043b4e721fa2acf3b`  
		Last Modified: Wed, 17 Dec 2025 21:40:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9a729809b661b20e6e8b44bb24413f513e1376d4dbe9ab0c1a4f7ed880149b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9883a54a8c4d45530843267722922526423a42a88046db1e58f74bed8bbe02d0`

```dockerfile
```

-	Layers:
	-	`sha256:a671bbb9a5464bb97f71429c00d4997635a1c127dc1b513aa48239e480106d60`  
		Last Modified: Wed, 17 Dec 2025 22:35:21 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36ef2adae88460c5dc2044a65093008d2beb76079d1f00bc5a7d862dbae0aa3b`  
		Last Modified: Wed, 17 Dec 2025 22:35:22 GMT  
		Size: 20.7 KB (20727 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine` - linux; 386

```console
$ docker pull memcached@sha256:ca4c4cf71b28fb2b701d7c25e78c0cf8a8cd4de9424d86e7f906833f71f198eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5740718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f722d8a189d7c92749316efb1c7335a5873618eac12d5e5bc01d68127fb291b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:38:08 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:38:09 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:40:55 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:40:55 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:40:55 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:40:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:40:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:40:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:40:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:40:55 GMT
USER memcache
# Wed, 17 Dec 2025 21:40:55 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:40:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3527b4f952d5950d8caa74dc0d1759215000f2f0a195344f0239c7e2805fe2fc`  
		Last Modified: Wed, 03 Dec 2025 19:30:41 GMT  
		Size: 3.7 MB (3685856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d3f49b0de92207dfc061e70de94dd679b3ea12f97d99d1974a6c62164a159a`  
		Last Modified: Wed, 17 Dec 2025 21:41:06 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c266f269a50bef9007064361dc83371a1dd461aabe92bbec3d1e979412466de`  
		Last Modified: Wed, 17 Dec 2025 21:41:06 GMT  
		Size: 110.7 KB (110738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2053dfa7b6aa4f5a136466c1659669f25a4578930977fb585d209c5dfde8036d`  
		Last Modified: Wed, 17 Dec 2025 21:41:08 GMT  
		Size: 1.9 MB (1942772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ed31d7fa74d79df9efd8d4f443ada386f5729fbe324a9794e76baff2c1c493`  
		Last Modified: Wed, 17 Dec 2025 21:41:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91df285e3ed438acb3e9589dc178518e2db7c4bfa971348c72b6d0327a4ee79`  
		Last Modified: Wed, 17 Dec 2025 21:41:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:647a776f52f62548a4098b2e4b11214b4a5c1ee9685712ef80a2832ef32ca8c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40881c0a421ed132c378aef8bdbe39305aaaecc7deee9b7de9ae4f93188dcbd3`

```dockerfile
```

-	Layers:
	-	`sha256:f3beb40a7590bdda06e509d8ad4ecd2043849256a64e5ff660b19b1cd56a094a`  
		Last Modified: Wed, 17 Dec 2025 22:35:25 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38c8a2e4dad46bf55c80872707f6283533a800478b72bf885b684dd50e07eb32`  
		Last Modified: Wed, 17 Dec 2025 22:35:26 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:3b02ff737dd16e237fd7406b5f7d02a513a983b5d2d53fa6cd313f1ef00b1f8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6030994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:530bbfb00fa1800e8532eef4fb114fc753724fcf50e1d1e12af0ca80cf6752a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:34:55 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:34:56 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:37:26 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:37:26 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:37:26 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:37:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:37:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:37:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:37:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:37:38 GMT
USER memcache
# Wed, 17 Dec 2025 21:37:38 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:37:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd01e04da0d57bffa2b60a957360f7a974a6b01b4d9acff8252fdec64a69f66`  
		Last Modified: Wed, 17 Dec 2025 21:38:00 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a239f5e0c0c7e367e7f132151c23b859390ef5a4cbc40fb10415655b7e4b8029`  
		Last Modified: Wed, 17 Dec 2025 21:38:00 GMT  
		Size: 126.3 KB (126252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5bf0071779f0057bb08ae7a6ce2aba364cd026a86150629c39a6a92aba920c`  
		Last Modified: Wed, 17 Dec 2025 21:38:00 GMT  
		Size: 2.1 MB (2076368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f39797f21825b46f2a91c72f603d5a656910a53e51d3e579f5f5e791aaac92`  
		Last Modified: Wed, 17 Dec 2025 21:38:00 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48cd6c111239cce7a47ed3674b56951e2830764b3576a0d26aa6924057642d4`  
		Last Modified: Wed, 17 Dec 2025 21:38:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:31b4659d5068108cb086c10f7eff5fc0f8d77afa0eb09b15fa3955924ad138ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4951610ebef7b9fc8a4a054b6085f3840f9ba32b81602af0d8c13ad838ba68`

```dockerfile
```

-	Layers:
	-	`sha256:c3757f7ab5b65afe79fc72a82e96ca02b81c222ba9649feccf145ce714cfc4b9`  
		Last Modified: Wed, 17 Dec 2025 22:35:29 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df6d5f19cafffe602863ac2b65054f5c05d4a497fece84a762d0aebdc057b39e`  
		Last Modified: Wed, 17 Dec 2025 22:35:29 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:04733682f967e9788435bbddf864edb8e1bb9cc8671e1e868c74f82093fe62c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5856574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9063d29cfc1dce3d05c19ff319a9d3e5455146c60efe56e9ce56bfbf4d3c3927`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:34:52 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:34:53 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:38:01 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:01 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:01 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:01 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a990effa92b45935b52bc06653d39a48f5ed34d054f60e892ec417f8d919a6`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50bf0a9e48ac326120a5de8b5e0cd6b991d704ed4a66448d4fcc8c6ad640d10`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 114.3 KB (114287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b26a3c60d8c62feb971cedd3bd49cd1d5f4d0d0d0149017b32b1573727914be9`  
		Last Modified: Wed, 17 Dec 2025 21:38:19 GMT  
		Size: 2.0 MB (2017127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd733ace70e5f90e389ce8159cbda2291a52bf39e53e2ee4ea6eb8cbccc625e`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821f5deda63bf425c92464f3e686b9fda7f6200ddc49ebacb324b2a45ec0d633`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:19f5876a625b474e4eea9e963de1422ad480c97357d44cd8604896e2da517d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd50fa1a24cfb1dea4e93374baa1e967c2f0fddd79dfa74422b955c193ea89a6`

```dockerfile
```

-	Layers:
	-	`sha256:4d2cbcf3625eaa8b19de7227c701c14f9bd69378a6e698f5aee36b0eb01f2167`  
		Last Modified: Wed, 17 Dec 2025 22:35:35 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:235e217cf2514537b942b1cb8a5ffbbe2ecee441b9373e75871acd7a34391107`  
		Last Modified: Wed, 17 Dec 2025 22:35:36 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.40-alpine3.23`

```console
$ docker pull memcached@sha256:1f30c9f207fc53a00216e36f03405482d94a339b2f53937e8749309fe7506861
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
$ docker pull memcached@sha256:65c25df73382e5ba4c57df3c2cccb5eb69702b813d07f9372f525e61225f0236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5955960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d33317a7accc6b056e21432db4903632531ace63c6085001ffb22caaa6d9d75b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:38:00 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:38:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:40:37 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:40:37 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:40:37 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:40:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:40:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:40:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:40:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:40:38 GMT
USER memcache
# Wed, 17 Dec 2025 21:40:38 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:40:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683f24283462cf58a8a6a81d7a140d0cd612c8120a019a56b2cb5f6f297d9465`  
		Last Modified: Wed, 17 Dec 2025 21:40:49 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450bd59379b8c57899254729c322d8ed1a1a7ca519dd92b78fc2d93e4e8a0b25`  
		Last Modified: Wed, 17 Dec 2025 21:40:49 GMT  
		Size: 106.0 KB (106041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2091c3522fccefd861318754918a244e21e5582890c29a366f8a5deb524e60af`  
		Last Modified: Wed, 17 Dec 2025 21:40:49 GMT  
		Size: 2.0 MB (1989255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9898efa8e26f703b25503f6a996e1f99a1fd8128fceb41ffe2e64c68a38599`  
		Last Modified: Wed, 17 Dec 2025 21:40:49 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2662bcfc6adeacc0aa8fd4c9d65e40532dd669f2516c02dc4a8ed4ce03647a0f`  
		Last Modified: Wed, 17 Dec 2025 21:40:49 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:e2ce9177720be2878a317e1f529eab177e45fa4f1bd45a06a69779f7c963a705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d581a35520859a173fbf6058a00db5435952fa00e8e9ee6c788563d4cae2f3`

```dockerfile
```

-	Layers:
	-	`sha256:1fe61b448f6cbc544f9c72a56a148440a1f1e60eaffe9144cbc03096adacdf37`  
		Last Modified: Wed, 17 Dec 2025 22:35:02 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea30cf376da8351a758cad58a77f03776483c271a35b12b24e81530b12868a2e`  
		Last Modified: Wed, 17 Dec 2025 22:35:03 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine3.23` - linux; arm variant v6

```console
$ docker pull memcached@sha256:ea5a1cd530f7418ba73b2ec6d05aa7d073fa3e55362ad7c272c4dce82f2ee550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5611085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e6688be943a2b0ca333de7ee49b87d11b3b103acac53a8a1cda65827e164b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:35:21 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:35:22 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:57:18 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:57:18 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:57:18 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:57:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:57:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:57:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:57:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:57:19 GMT
USER memcache
# Wed, 17 Dec 2025 21:57:19 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:57:19 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0132a447b58e699f3e930eb400504a4dab7572b48682b411e172ca2f13e3837e`  
		Last Modified: Wed, 17 Dec 2025 21:57:31 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca221542481b910c1ab1534fbed6a1daa903dd46e7dec29a8e7e45e172ee4e98`  
		Last Modified: Wed, 17 Dec 2025 21:57:31 GMT  
		Size: 102.6 KB (102643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f509979790be1d0f32b1cb145ef690501c7b24933c62c28638d664ba9c700393`  
		Last Modified: Wed, 17 Dec 2025 21:57:32 GMT  
		Size: 1.9 MB (1939202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92b99708f0757173744dcefe8c10b63d6bb57457bb22a870a97d2e466b7dbe6`  
		Last Modified: Wed, 17 Dec 2025 21:57:31 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129c905b76006e4eac5697b73920244e0b167164eda691d8c9fce48e08d9a15a`  
		Last Modified: Wed, 17 Dec 2025 21:57:31 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:a01a7f359b5b6020f56a33f6c48f6d83addd590b6ffcfb8d9f39cbb014a3f79f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b004564c274eab1f4a9d5854d0515a6b15f0a9de9abfe0403b6717464af55ca2`

```dockerfile
```

-	Layers:
	-	`sha256:223be1dd282744e43fcfc8303bb2997a6a232da86d8a573d407d550c7f356417`  
		Last Modified: Wed, 17 Dec 2025 22:35:06 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine3.23` - linux; arm variant v7

```console
$ docker pull memcached@sha256:f8a13acc5d2817ee1e9df95f26a3647b2fc9361676acb4ccca0e106d0ff8d5d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5269348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c8d4d3ca238a3133af08dd38e3cd46b3afbc7409a4df18d893b9878e5001cb8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:35:30 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:35:31 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:27 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:27 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d9d8962df55145f5fd88847d7fbf0fd846221bbe5d3fda7baf9461e1be862b`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5b6235e518eb1a135149571028b21cc0487ffc5c0fb9eb823fa9f51c9b3b7f`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 92.4 KB (92365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b5f719f7a3d4ba338f20ab53593f3250818988f89bc9d1ac7f5d3412497aa5`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 1.9 MB (1897164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6783f23f1f96fa31f44928320bb651f00a3ac7c6f74bc8d4931b527ad745771`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9186b8b7184cef442ae3ed6a3feadcaa8f4ccc974ed5ae6c6cf8efe37e679f23`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:65ab94866fe80b34478423e645bc70428ca81e1ef0e523993f4da895ba84a4ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2093447767fcc95a5f23b4567561974625baad6244721a2fadf42a60f1d61397`

```dockerfile
```

-	Layers:
	-	`sha256:a8a1bb2b759719025d140e377ef6a401d06c350a48eea3cf16e20ecb526095d9`  
		Last Modified: Wed, 17 Dec 2025 22:35:09 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b06bbe6a45bdcd2081c0e485d5ab897b548b87391fe55dfaeac6bdabf63b6e4`  
		Last Modified: Wed, 17 Dec 2025 22:35:10 GMT  
		Size: 20.7 KB (20677 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:349dc973200279dddf8e6ce28d9128babfe84da2f011c88d675fda6b53d9b435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6284972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee78c99ff858f77e454879ddf462b94812f23a4a38585a7f04722f753f72bdf4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:37:24 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:37:25 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:40:13 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:40:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:40:13 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:40:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:40:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:40:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:40:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:40:13 GMT
USER memcache
# Wed, 17 Dec 2025 21:40:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:40:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e5de81b8fd10090b357c152c289b12543ba0233b02e1fea1f31abbb41c6ce6`  
		Last Modified: Wed, 17 Dec 2025 21:40:24 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a237d3db68cd689e683d8873b9f6662b963c1da855cb61f0404b9d218ce4ab`  
		Last Modified: Wed, 17 Dec 2025 21:40:24 GMT  
		Size: 121.9 KB (121870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab92f84f0d6a5d6415bf522e99e0ccc9603a821231233c659431c00d8f166e16`  
		Last Modified: Wed, 17 Dec 2025 21:40:24 GMT  
		Size: 2.0 MB (1966553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd31b8f53d48209a8b58d7add5eaa6252a50192d7d95307012fbe2a96c887175`  
		Last Modified: Wed, 17 Dec 2025 21:40:24 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db33d4acf9261f39e1a05295122f733c54555907dbe2700043b4e721fa2acf3b`  
		Last Modified: Wed, 17 Dec 2025 21:40:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:9a729809b661b20e6e8b44bb24413f513e1376d4dbe9ab0c1a4f7ed880149b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9883a54a8c4d45530843267722922526423a42a88046db1e58f74bed8bbe02d0`

```dockerfile
```

-	Layers:
	-	`sha256:a671bbb9a5464bb97f71429c00d4997635a1c127dc1b513aa48239e480106d60`  
		Last Modified: Wed, 17 Dec 2025 22:35:21 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36ef2adae88460c5dc2044a65093008d2beb76079d1f00bc5a7d862dbae0aa3b`  
		Last Modified: Wed, 17 Dec 2025 22:35:22 GMT  
		Size: 20.7 KB (20727 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine3.23` - linux; 386

```console
$ docker pull memcached@sha256:ca4c4cf71b28fb2b701d7c25e78c0cf8a8cd4de9424d86e7f906833f71f198eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5740718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f722d8a189d7c92749316efb1c7335a5873618eac12d5e5bc01d68127fb291b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:38:08 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:38:09 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:40:55 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:40:55 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:40:55 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:40:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:40:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:40:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:40:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:40:55 GMT
USER memcache
# Wed, 17 Dec 2025 21:40:55 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:40:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3527b4f952d5950d8caa74dc0d1759215000f2f0a195344f0239c7e2805fe2fc`  
		Last Modified: Wed, 03 Dec 2025 19:30:41 GMT  
		Size: 3.7 MB (3685856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d3f49b0de92207dfc061e70de94dd679b3ea12f97d99d1974a6c62164a159a`  
		Last Modified: Wed, 17 Dec 2025 21:41:06 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c266f269a50bef9007064361dc83371a1dd461aabe92bbec3d1e979412466de`  
		Last Modified: Wed, 17 Dec 2025 21:41:06 GMT  
		Size: 110.7 KB (110738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2053dfa7b6aa4f5a136466c1659669f25a4578930977fb585d209c5dfde8036d`  
		Last Modified: Wed, 17 Dec 2025 21:41:08 GMT  
		Size: 1.9 MB (1942772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ed31d7fa74d79df9efd8d4f443ada386f5729fbe324a9794e76baff2c1c493`  
		Last Modified: Wed, 17 Dec 2025 21:41:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91df285e3ed438acb3e9589dc178518e2db7c4bfa971348c72b6d0327a4ee79`  
		Last Modified: Wed, 17 Dec 2025 21:41:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:647a776f52f62548a4098b2e4b11214b4a5c1ee9685712ef80a2832ef32ca8c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40881c0a421ed132c378aef8bdbe39305aaaecc7deee9b7de9ae4f93188dcbd3`

```dockerfile
```

-	Layers:
	-	`sha256:f3beb40a7590bdda06e509d8ad4ecd2043849256a64e5ff660b19b1cd56a094a`  
		Last Modified: Wed, 17 Dec 2025 22:35:25 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38c8a2e4dad46bf55c80872707f6283533a800478b72bf885b684dd50e07eb32`  
		Last Modified: Wed, 17 Dec 2025 22:35:26 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine3.23` - linux; ppc64le

```console
$ docker pull memcached@sha256:3b02ff737dd16e237fd7406b5f7d02a513a983b5d2d53fa6cd313f1ef00b1f8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6030994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:530bbfb00fa1800e8532eef4fb114fc753724fcf50e1d1e12af0ca80cf6752a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:34:55 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:34:56 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:37:26 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:37:26 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:37:26 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:37:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:37:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:37:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:37:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:37:38 GMT
USER memcache
# Wed, 17 Dec 2025 21:37:38 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:37:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd01e04da0d57bffa2b60a957360f7a974a6b01b4d9acff8252fdec64a69f66`  
		Last Modified: Wed, 17 Dec 2025 21:38:00 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a239f5e0c0c7e367e7f132151c23b859390ef5a4cbc40fb10415655b7e4b8029`  
		Last Modified: Wed, 17 Dec 2025 21:38:00 GMT  
		Size: 126.3 KB (126252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5bf0071779f0057bb08ae7a6ce2aba364cd026a86150629c39a6a92aba920c`  
		Last Modified: Wed, 17 Dec 2025 21:38:00 GMT  
		Size: 2.1 MB (2076368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f39797f21825b46f2a91c72f603d5a656910a53e51d3e579f5f5e791aaac92`  
		Last Modified: Wed, 17 Dec 2025 21:38:00 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48cd6c111239cce7a47ed3674b56951e2830764b3576a0d26aa6924057642d4`  
		Last Modified: Wed, 17 Dec 2025 21:38:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:31b4659d5068108cb086c10f7eff5fc0f8d77afa0eb09b15fa3955924ad138ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4951610ebef7b9fc8a4a054b6085f3840f9ba32b81602af0d8c13ad838ba68`

```dockerfile
```

-	Layers:
	-	`sha256:c3757f7ab5b65afe79fc72a82e96ca02b81c222ba9649feccf145ce714cfc4b9`  
		Last Modified: Wed, 17 Dec 2025 22:35:29 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df6d5f19cafffe602863ac2b65054f5c05d4a497fece84a762d0aebdc057b39e`  
		Last Modified: Wed, 17 Dec 2025 22:35:29 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine3.23` - linux; s390x

```console
$ docker pull memcached@sha256:04733682f967e9788435bbddf864edb8e1bb9cc8671e1e868c74f82093fe62c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5856574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9063d29cfc1dce3d05c19ff319a9d3e5455146c60efe56e9ce56bfbf4d3c3927`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:34:52 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:34:53 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:38:01 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:01 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:01 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:01 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a990effa92b45935b52bc06653d39a48f5ed34d054f60e892ec417f8d919a6`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50bf0a9e48ac326120a5de8b5e0cd6b991d704ed4a66448d4fcc8c6ad640d10`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 114.3 KB (114287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b26a3c60d8c62feb971cedd3bd49cd1d5f4d0d0d0149017b32b1573727914be9`  
		Last Modified: Wed, 17 Dec 2025 21:38:19 GMT  
		Size: 2.0 MB (2017127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd733ace70e5f90e389ce8159cbda2291a52bf39e53e2ee4ea6eb8cbccc625e`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821f5deda63bf425c92464f3e686b9fda7f6200ddc49ebacb324b2a45ec0d633`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:19f5876a625b474e4eea9e963de1422ad480c97357d44cd8604896e2da517d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd50fa1a24cfb1dea4e93374baa1e967c2f0fddd79dfa74422b955c193ea89a6`

```dockerfile
```

-	Layers:
	-	`sha256:4d2cbcf3625eaa8b19de7227c701c14f9bd69378a6e698f5aee36b0eb01f2167`  
		Last Modified: Wed, 17 Dec 2025 22:35:35 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:235e217cf2514537b942b1cb8a5ffbbe2ecee441b9373e75871acd7a34391107`  
		Last Modified: Wed, 17 Dec 2025 22:35:36 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.40-trixie`

```console
$ docker pull memcached@sha256:19007562d3a6fbafd8deb9d6fd5cc0ac3fecdba7e4112a5e254b1cfec906a9f6
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
$ docker pull memcached@sha256:4ec52eed643b17626643099f4ce0a142ef9dce004fc8bb32f582c0c31219dba9
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
$ docker pull memcached@sha256:65c25df73382e5ba4c57df3c2cccb5eb69702b813d07f9372f525e61225f0236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5955960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d33317a7accc6b056e21432db4903632531ace63c6085001ffb22caaa6d9d75b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:38:00 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:38:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:40:37 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:40:37 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:40:37 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:40:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:40:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:40:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:40:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:40:38 GMT
USER memcache
# Wed, 17 Dec 2025 21:40:38 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:40:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683f24283462cf58a8a6a81d7a140d0cd612c8120a019a56b2cb5f6f297d9465`  
		Last Modified: Wed, 17 Dec 2025 21:40:49 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450bd59379b8c57899254729c322d8ed1a1a7ca519dd92b78fc2d93e4e8a0b25`  
		Last Modified: Wed, 17 Dec 2025 21:40:49 GMT  
		Size: 106.0 KB (106041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2091c3522fccefd861318754918a244e21e5582890c29a366f8a5deb524e60af`  
		Last Modified: Wed, 17 Dec 2025 21:40:49 GMT  
		Size: 2.0 MB (1989255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9898efa8e26f703b25503f6a996e1f99a1fd8128fceb41ffe2e64c68a38599`  
		Last Modified: Wed, 17 Dec 2025 21:40:49 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2662bcfc6adeacc0aa8fd4c9d65e40532dd669f2516c02dc4a8ed4ce03647a0f`  
		Last Modified: Wed, 17 Dec 2025 21:40:49 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:e2ce9177720be2878a317e1f529eab177e45fa4f1bd45a06a69779f7c963a705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d581a35520859a173fbf6058a00db5435952fa00e8e9ee6c788563d4cae2f3`

```dockerfile
```

-	Layers:
	-	`sha256:1fe61b448f6cbc544f9c72a56a148440a1f1e60eaffe9144cbc03096adacdf37`  
		Last Modified: Wed, 17 Dec 2025 22:35:02 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea30cf376da8351a758cad58a77f03776483c271a35b12b24e81530b12868a2e`  
		Last Modified: Wed, 17 Dec 2025 22:35:03 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:ea5a1cd530f7418ba73b2ec6d05aa7d073fa3e55362ad7c272c4dce82f2ee550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5611085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e6688be943a2b0ca333de7ee49b87d11b3b103acac53a8a1cda65827e164b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:35:21 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:35:22 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:57:18 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:57:18 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:57:18 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:57:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:57:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:57:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:57:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:57:19 GMT
USER memcache
# Wed, 17 Dec 2025 21:57:19 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:57:19 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0132a447b58e699f3e930eb400504a4dab7572b48682b411e172ca2f13e3837e`  
		Last Modified: Wed, 17 Dec 2025 21:57:31 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca221542481b910c1ab1534fbed6a1daa903dd46e7dec29a8e7e45e172ee4e98`  
		Last Modified: Wed, 17 Dec 2025 21:57:31 GMT  
		Size: 102.6 KB (102643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f509979790be1d0f32b1cb145ef690501c7b24933c62c28638d664ba9c700393`  
		Last Modified: Wed, 17 Dec 2025 21:57:32 GMT  
		Size: 1.9 MB (1939202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92b99708f0757173744dcefe8c10b63d6bb57457bb22a870a97d2e466b7dbe6`  
		Last Modified: Wed, 17 Dec 2025 21:57:31 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129c905b76006e4eac5697b73920244e0b167164eda691d8c9fce48e08d9a15a`  
		Last Modified: Wed, 17 Dec 2025 21:57:31 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:a01a7f359b5b6020f56a33f6c48f6d83addd590b6ffcfb8d9f39cbb014a3f79f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b004564c274eab1f4a9d5854d0515a6b15f0a9de9abfe0403b6717464af55ca2`

```dockerfile
```

-	Layers:
	-	`sha256:223be1dd282744e43fcfc8303bb2997a6a232da86d8a573d407d550c7f356417`  
		Last Modified: Wed, 17 Dec 2025 22:35:06 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:f8a13acc5d2817ee1e9df95f26a3647b2fc9361676acb4ccca0e106d0ff8d5d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5269348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c8d4d3ca238a3133af08dd38e3cd46b3afbc7409a4df18d893b9878e5001cb8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:35:30 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:35:31 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:27 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:27 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d9d8962df55145f5fd88847d7fbf0fd846221bbe5d3fda7baf9461e1be862b`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5b6235e518eb1a135149571028b21cc0487ffc5c0fb9eb823fa9f51c9b3b7f`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 92.4 KB (92365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b5f719f7a3d4ba338f20ab53593f3250818988f89bc9d1ac7f5d3412497aa5`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 1.9 MB (1897164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6783f23f1f96fa31f44928320bb651f00a3ac7c6f74bc8d4931b527ad745771`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9186b8b7184cef442ae3ed6a3feadcaa8f4ccc974ed5ae6c6cf8efe37e679f23`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:65ab94866fe80b34478423e645bc70428ca81e1ef0e523993f4da895ba84a4ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2093447767fcc95a5f23b4567561974625baad6244721a2fadf42a60f1d61397`

```dockerfile
```

-	Layers:
	-	`sha256:a8a1bb2b759719025d140e377ef6a401d06c350a48eea3cf16e20ecb526095d9`  
		Last Modified: Wed, 17 Dec 2025 22:35:09 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b06bbe6a45bdcd2081c0e485d5ab897b548b87391fe55dfaeac6bdabf63b6e4`  
		Last Modified: Wed, 17 Dec 2025 22:35:10 GMT  
		Size: 20.7 KB (20677 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:349dc973200279dddf8e6ce28d9128babfe84da2f011c88d675fda6b53d9b435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6284972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee78c99ff858f77e454879ddf462b94812f23a4a38585a7f04722f753f72bdf4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:37:24 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:37:25 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:40:13 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:40:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:40:13 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:40:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:40:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:40:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:40:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:40:13 GMT
USER memcache
# Wed, 17 Dec 2025 21:40:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:40:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e5de81b8fd10090b357c152c289b12543ba0233b02e1fea1f31abbb41c6ce6`  
		Last Modified: Wed, 17 Dec 2025 21:40:24 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a237d3db68cd689e683d8873b9f6662b963c1da855cb61f0404b9d218ce4ab`  
		Last Modified: Wed, 17 Dec 2025 21:40:24 GMT  
		Size: 121.9 KB (121870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab92f84f0d6a5d6415bf522e99e0ccc9603a821231233c659431c00d8f166e16`  
		Last Modified: Wed, 17 Dec 2025 21:40:24 GMT  
		Size: 2.0 MB (1966553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd31b8f53d48209a8b58d7add5eaa6252a50192d7d95307012fbe2a96c887175`  
		Last Modified: Wed, 17 Dec 2025 21:40:24 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db33d4acf9261f39e1a05295122f733c54555907dbe2700043b4e721fa2acf3b`  
		Last Modified: Wed, 17 Dec 2025 21:40:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9a729809b661b20e6e8b44bb24413f513e1376d4dbe9ab0c1a4f7ed880149b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9883a54a8c4d45530843267722922526423a42a88046db1e58f74bed8bbe02d0`

```dockerfile
```

-	Layers:
	-	`sha256:a671bbb9a5464bb97f71429c00d4997635a1c127dc1b513aa48239e480106d60`  
		Last Modified: Wed, 17 Dec 2025 22:35:21 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36ef2adae88460c5dc2044a65093008d2beb76079d1f00bc5a7d862dbae0aa3b`  
		Last Modified: Wed, 17 Dec 2025 22:35:22 GMT  
		Size: 20.7 KB (20727 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:ca4c4cf71b28fb2b701d7c25e78c0cf8a8cd4de9424d86e7f906833f71f198eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5740718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f722d8a189d7c92749316efb1c7335a5873618eac12d5e5bc01d68127fb291b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:38:08 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:38:09 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:40:55 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:40:55 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:40:55 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:40:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:40:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:40:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:40:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:40:55 GMT
USER memcache
# Wed, 17 Dec 2025 21:40:55 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:40:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3527b4f952d5950d8caa74dc0d1759215000f2f0a195344f0239c7e2805fe2fc`  
		Last Modified: Wed, 03 Dec 2025 19:30:41 GMT  
		Size: 3.7 MB (3685856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d3f49b0de92207dfc061e70de94dd679b3ea12f97d99d1974a6c62164a159a`  
		Last Modified: Wed, 17 Dec 2025 21:41:06 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c266f269a50bef9007064361dc83371a1dd461aabe92bbec3d1e979412466de`  
		Last Modified: Wed, 17 Dec 2025 21:41:06 GMT  
		Size: 110.7 KB (110738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2053dfa7b6aa4f5a136466c1659669f25a4578930977fb585d209c5dfde8036d`  
		Last Modified: Wed, 17 Dec 2025 21:41:08 GMT  
		Size: 1.9 MB (1942772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ed31d7fa74d79df9efd8d4f443ada386f5729fbe324a9794e76baff2c1c493`  
		Last Modified: Wed, 17 Dec 2025 21:41:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91df285e3ed438acb3e9589dc178518e2db7c4bfa971348c72b6d0327a4ee79`  
		Last Modified: Wed, 17 Dec 2025 21:41:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:647a776f52f62548a4098b2e4b11214b4a5c1ee9685712ef80a2832ef32ca8c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40881c0a421ed132c378aef8bdbe39305aaaecc7deee9b7de9ae4f93188dcbd3`

```dockerfile
```

-	Layers:
	-	`sha256:f3beb40a7590bdda06e509d8ad4ecd2043849256a64e5ff660b19b1cd56a094a`  
		Last Modified: Wed, 17 Dec 2025 22:35:25 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38c8a2e4dad46bf55c80872707f6283533a800478b72bf885b684dd50e07eb32`  
		Last Modified: Wed, 17 Dec 2025 22:35:26 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:3b02ff737dd16e237fd7406b5f7d02a513a983b5d2d53fa6cd313f1ef00b1f8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6030994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:530bbfb00fa1800e8532eef4fb114fc753724fcf50e1d1e12af0ca80cf6752a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:34:55 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:34:56 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:37:26 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:37:26 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:37:26 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:37:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:37:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:37:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:37:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:37:38 GMT
USER memcache
# Wed, 17 Dec 2025 21:37:38 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:37:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd01e04da0d57bffa2b60a957360f7a974a6b01b4d9acff8252fdec64a69f66`  
		Last Modified: Wed, 17 Dec 2025 21:38:00 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a239f5e0c0c7e367e7f132151c23b859390ef5a4cbc40fb10415655b7e4b8029`  
		Last Modified: Wed, 17 Dec 2025 21:38:00 GMT  
		Size: 126.3 KB (126252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5bf0071779f0057bb08ae7a6ce2aba364cd026a86150629c39a6a92aba920c`  
		Last Modified: Wed, 17 Dec 2025 21:38:00 GMT  
		Size: 2.1 MB (2076368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f39797f21825b46f2a91c72f603d5a656910a53e51d3e579f5f5e791aaac92`  
		Last Modified: Wed, 17 Dec 2025 21:38:00 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48cd6c111239cce7a47ed3674b56951e2830764b3576a0d26aa6924057642d4`  
		Last Modified: Wed, 17 Dec 2025 21:38:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:31b4659d5068108cb086c10f7eff5fc0f8d77afa0eb09b15fa3955924ad138ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4951610ebef7b9fc8a4a054b6085f3840f9ba32b81602af0d8c13ad838ba68`

```dockerfile
```

-	Layers:
	-	`sha256:c3757f7ab5b65afe79fc72a82e96ca02b81c222ba9649feccf145ce714cfc4b9`  
		Last Modified: Wed, 17 Dec 2025 22:35:29 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df6d5f19cafffe602863ac2b65054f5c05d4a497fece84a762d0aebdc057b39e`  
		Last Modified: Wed, 17 Dec 2025 22:35:29 GMT  
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
$ docker pull memcached@sha256:04733682f967e9788435bbddf864edb8e1bb9cc8671e1e868c74f82093fe62c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5856574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9063d29cfc1dce3d05c19ff319a9d3e5455146c60efe56e9ce56bfbf4d3c3927`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:34:52 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:34:53 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:38:01 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:01 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:01 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:01 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a990effa92b45935b52bc06653d39a48f5ed34d054f60e892ec417f8d919a6`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50bf0a9e48ac326120a5de8b5e0cd6b991d704ed4a66448d4fcc8c6ad640d10`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 114.3 KB (114287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b26a3c60d8c62feb971cedd3bd49cd1d5f4d0d0d0149017b32b1573727914be9`  
		Last Modified: Wed, 17 Dec 2025 21:38:19 GMT  
		Size: 2.0 MB (2017127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd733ace70e5f90e389ce8159cbda2291a52bf39e53e2ee4ea6eb8cbccc625e`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821f5deda63bf425c92464f3e686b9fda7f6200ddc49ebacb324b2a45ec0d633`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:19f5876a625b474e4eea9e963de1422ad480c97357d44cd8604896e2da517d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd50fa1a24cfb1dea4e93374baa1e967c2f0fddd79dfa74422b955c193ea89a6`

```dockerfile
```

-	Layers:
	-	`sha256:4d2cbcf3625eaa8b19de7227c701c14f9bd69378a6e698f5aee36b0eb01f2167`  
		Last Modified: Wed, 17 Dec 2025 22:35:35 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:235e217cf2514537b942b1cb8a5ffbbe2ecee441b9373e75871acd7a34391107`  
		Last Modified: Wed, 17 Dec 2025 22:35:36 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine3.23`

```console
$ docker pull memcached@sha256:4ec52eed643b17626643099f4ce0a142ef9dce004fc8bb32f582c0c31219dba9
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
$ docker pull memcached@sha256:65c25df73382e5ba4c57df3c2cccb5eb69702b813d07f9372f525e61225f0236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5955960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d33317a7accc6b056e21432db4903632531ace63c6085001ffb22caaa6d9d75b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:38:00 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:38:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:40:37 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:40:37 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:40:37 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:40:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:40:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:40:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:40:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:40:38 GMT
USER memcache
# Wed, 17 Dec 2025 21:40:38 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:40:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683f24283462cf58a8a6a81d7a140d0cd612c8120a019a56b2cb5f6f297d9465`  
		Last Modified: Wed, 17 Dec 2025 21:40:49 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450bd59379b8c57899254729c322d8ed1a1a7ca519dd92b78fc2d93e4e8a0b25`  
		Last Modified: Wed, 17 Dec 2025 21:40:49 GMT  
		Size: 106.0 KB (106041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2091c3522fccefd861318754918a244e21e5582890c29a366f8a5deb524e60af`  
		Last Modified: Wed, 17 Dec 2025 21:40:49 GMT  
		Size: 2.0 MB (1989255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9898efa8e26f703b25503f6a996e1f99a1fd8128fceb41ffe2e64c68a38599`  
		Last Modified: Wed, 17 Dec 2025 21:40:49 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2662bcfc6adeacc0aa8fd4c9d65e40532dd669f2516c02dc4a8ed4ce03647a0f`  
		Last Modified: Wed, 17 Dec 2025 21:40:49 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:e2ce9177720be2878a317e1f529eab177e45fa4f1bd45a06a69779f7c963a705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d581a35520859a173fbf6058a00db5435952fa00e8e9ee6c788563d4cae2f3`

```dockerfile
```

-	Layers:
	-	`sha256:1fe61b448f6cbc544f9c72a56a148440a1f1e60eaffe9144cbc03096adacdf37`  
		Last Modified: Wed, 17 Dec 2025 22:35:02 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea30cf376da8351a758cad58a77f03776483c271a35b12b24e81530b12868a2e`  
		Last Modified: Wed, 17 Dec 2025 22:35:03 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; arm variant v6

```console
$ docker pull memcached@sha256:ea5a1cd530f7418ba73b2ec6d05aa7d073fa3e55362ad7c272c4dce82f2ee550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5611085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e6688be943a2b0ca333de7ee49b87d11b3b103acac53a8a1cda65827e164b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:35:21 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:35:22 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:57:18 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:57:18 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:57:18 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:57:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:57:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:57:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:57:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:57:19 GMT
USER memcache
# Wed, 17 Dec 2025 21:57:19 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:57:19 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0132a447b58e699f3e930eb400504a4dab7572b48682b411e172ca2f13e3837e`  
		Last Modified: Wed, 17 Dec 2025 21:57:31 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca221542481b910c1ab1534fbed6a1daa903dd46e7dec29a8e7e45e172ee4e98`  
		Last Modified: Wed, 17 Dec 2025 21:57:31 GMT  
		Size: 102.6 KB (102643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f509979790be1d0f32b1cb145ef690501c7b24933c62c28638d664ba9c700393`  
		Last Modified: Wed, 17 Dec 2025 21:57:32 GMT  
		Size: 1.9 MB (1939202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92b99708f0757173744dcefe8c10b63d6bb57457bb22a870a97d2e466b7dbe6`  
		Last Modified: Wed, 17 Dec 2025 21:57:31 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129c905b76006e4eac5697b73920244e0b167164eda691d8c9fce48e08d9a15a`  
		Last Modified: Wed, 17 Dec 2025 21:57:31 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:a01a7f359b5b6020f56a33f6c48f6d83addd590b6ffcfb8d9f39cbb014a3f79f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b004564c274eab1f4a9d5854d0515a6b15f0a9de9abfe0403b6717464af55ca2`

```dockerfile
```

-	Layers:
	-	`sha256:223be1dd282744e43fcfc8303bb2997a6a232da86d8a573d407d550c7f356417`  
		Last Modified: Wed, 17 Dec 2025 22:35:06 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; arm variant v7

```console
$ docker pull memcached@sha256:f8a13acc5d2817ee1e9df95f26a3647b2fc9361676acb4ccca0e106d0ff8d5d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5269348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c8d4d3ca238a3133af08dd38e3cd46b3afbc7409a4df18d893b9878e5001cb8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:35:30 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:35:31 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:27 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:27 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d9d8962df55145f5fd88847d7fbf0fd846221bbe5d3fda7baf9461e1be862b`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5b6235e518eb1a135149571028b21cc0487ffc5c0fb9eb823fa9f51c9b3b7f`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 92.4 KB (92365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b5f719f7a3d4ba338f20ab53593f3250818988f89bc9d1ac7f5d3412497aa5`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 1.9 MB (1897164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6783f23f1f96fa31f44928320bb651f00a3ac7c6f74bc8d4931b527ad745771`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9186b8b7184cef442ae3ed6a3feadcaa8f4ccc974ed5ae6c6cf8efe37e679f23`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:65ab94866fe80b34478423e645bc70428ca81e1ef0e523993f4da895ba84a4ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2093447767fcc95a5f23b4567561974625baad6244721a2fadf42a60f1d61397`

```dockerfile
```

-	Layers:
	-	`sha256:a8a1bb2b759719025d140e377ef6a401d06c350a48eea3cf16e20ecb526095d9`  
		Last Modified: Wed, 17 Dec 2025 22:35:09 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b06bbe6a45bdcd2081c0e485d5ab897b548b87391fe55dfaeac6bdabf63b6e4`  
		Last Modified: Wed, 17 Dec 2025 22:35:10 GMT  
		Size: 20.7 KB (20677 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:349dc973200279dddf8e6ce28d9128babfe84da2f011c88d675fda6b53d9b435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6284972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee78c99ff858f77e454879ddf462b94812f23a4a38585a7f04722f753f72bdf4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:37:24 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:37:25 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:40:13 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:40:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:40:13 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:40:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:40:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:40:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:40:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:40:13 GMT
USER memcache
# Wed, 17 Dec 2025 21:40:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:40:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e5de81b8fd10090b357c152c289b12543ba0233b02e1fea1f31abbb41c6ce6`  
		Last Modified: Wed, 17 Dec 2025 21:40:24 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a237d3db68cd689e683d8873b9f6662b963c1da855cb61f0404b9d218ce4ab`  
		Last Modified: Wed, 17 Dec 2025 21:40:24 GMT  
		Size: 121.9 KB (121870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab92f84f0d6a5d6415bf522e99e0ccc9603a821231233c659431c00d8f166e16`  
		Last Modified: Wed, 17 Dec 2025 21:40:24 GMT  
		Size: 2.0 MB (1966553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd31b8f53d48209a8b58d7add5eaa6252a50192d7d95307012fbe2a96c887175`  
		Last Modified: Wed, 17 Dec 2025 21:40:24 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db33d4acf9261f39e1a05295122f733c54555907dbe2700043b4e721fa2acf3b`  
		Last Modified: Wed, 17 Dec 2025 21:40:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:9a729809b661b20e6e8b44bb24413f513e1376d4dbe9ab0c1a4f7ed880149b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9883a54a8c4d45530843267722922526423a42a88046db1e58f74bed8bbe02d0`

```dockerfile
```

-	Layers:
	-	`sha256:a671bbb9a5464bb97f71429c00d4997635a1c127dc1b513aa48239e480106d60`  
		Last Modified: Wed, 17 Dec 2025 22:35:21 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36ef2adae88460c5dc2044a65093008d2beb76079d1f00bc5a7d862dbae0aa3b`  
		Last Modified: Wed, 17 Dec 2025 22:35:22 GMT  
		Size: 20.7 KB (20727 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; 386

```console
$ docker pull memcached@sha256:ca4c4cf71b28fb2b701d7c25e78c0cf8a8cd4de9424d86e7f906833f71f198eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5740718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f722d8a189d7c92749316efb1c7335a5873618eac12d5e5bc01d68127fb291b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:38:08 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:38:09 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:40:55 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:40:55 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:40:55 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:40:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:40:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:40:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:40:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:40:55 GMT
USER memcache
# Wed, 17 Dec 2025 21:40:55 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:40:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3527b4f952d5950d8caa74dc0d1759215000f2f0a195344f0239c7e2805fe2fc`  
		Last Modified: Wed, 03 Dec 2025 19:30:41 GMT  
		Size: 3.7 MB (3685856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d3f49b0de92207dfc061e70de94dd679b3ea12f97d99d1974a6c62164a159a`  
		Last Modified: Wed, 17 Dec 2025 21:41:06 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c266f269a50bef9007064361dc83371a1dd461aabe92bbec3d1e979412466de`  
		Last Modified: Wed, 17 Dec 2025 21:41:06 GMT  
		Size: 110.7 KB (110738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2053dfa7b6aa4f5a136466c1659669f25a4578930977fb585d209c5dfde8036d`  
		Last Modified: Wed, 17 Dec 2025 21:41:08 GMT  
		Size: 1.9 MB (1942772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ed31d7fa74d79df9efd8d4f443ada386f5729fbe324a9794e76baff2c1c493`  
		Last Modified: Wed, 17 Dec 2025 21:41:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91df285e3ed438acb3e9589dc178518e2db7c4bfa971348c72b6d0327a4ee79`  
		Last Modified: Wed, 17 Dec 2025 21:41:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:647a776f52f62548a4098b2e4b11214b4a5c1ee9685712ef80a2832ef32ca8c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40881c0a421ed132c378aef8bdbe39305aaaecc7deee9b7de9ae4f93188dcbd3`

```dockerfile
```

-	Layers:
	-	`sha256:f3beb40a7590bdda06e509d8ad4ecd2043849256a64e5ff660b19b1cd56a094a`  
		Last Modified: Wed, 17 Dec 2025 22:35:25 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38c8a2e4dad46bf55c80872707f6283533a800478b72bf885b684dd50e07eb32`  
		Last Modified: Wed, 17 Dec 2025 22:35:26 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; ppc64le

```console
$ docker pull memcached@sha256:3b02ff737dd16e237fd7406b5f7d02a513a983b5d2d53fa6cd313f1ef00b1f8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6030994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:530bbfb00fa1800e8532eef4fb114fc753724fcf50e1d1e12af0ca80cf6752a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:34:55 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:34:56 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:37:26 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:37:26 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:37:26 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:37:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:37:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:37:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:37:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:37:38 GMT
USER memcache
# Wed, 17 Dec 2025 21:37:38 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:37:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd01e04da0d57bffa2b60a957360f7a974a6b01b4d9acff8252fdec64a69f66`  
		Last Modified: Wed, 17 Dec 2025 21:38:00 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a239f5e0c0c7e367e7f132151c23b859390ef5a4cbc40fb10415655b7e4b8029`  
		Last Modified: Wed, 17 Dec 2025 21:38:00 GMT  
		Size: 126.3 KB (126252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5bf0071779f0057bb08ae7a6ce2aba364cd026a86150629c39a6a92aba920c`  
		Last Modified: Wed, 17 Dec 2025 21:38:00 GMT  
		Size: 2.1 MB (2076368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f39797f21825b46f2a91c72f603d5a656910a53e51d3e579f5f5e791aaac92`  
		Last Modified: Wed, 17 Dec 2025 21:38:00 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48cd6c111239cce7a47ed3674b56951e2830764b3576a0d26aa6924057642d4`  
		Last Modified: Wed, 17 Dec 2025 21:38:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:31b4659d5068108cb086c10f7eff5fc0f8d77afa0eb09b15fa3955924ad138ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4951610ebef7b9fc8a4a054b6085f3840f9ba32b81602af0d8c13ad838ba68`

```dockerfile
```

-	Layers:
	-	`sha256:c3757f7ab5b65afe79fc72a82e96ca02b81c222ba9649feccf145ce714cfc4b9`  
		Last Modified: Wed, 17 Dec 2025 22:35:29 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df6d5f19cafffe602863ac2b65054f5c05d4a497fece84a762d0aebdc057b39e`  
		Last Modified: Wed, 17 Dec 2025 22:35:29 GMT  
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
$ docker pull memcached@sha256:04733682f967e9788435bbddf864edb8e1bb9cc8671e1e868c74f82093fe62c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5856574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9063d29cfc1dce3d05c19ff319a9d3e5455146c60efe56e9ce56bfbf4d3c3927`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:34:52 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 17 Dec 2025 21:34:53 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 17 Dec 2025 21:38:01 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:01 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:01 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:01 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a990effa92b45935b52bc06653d39a48f5ed34d054f60e892ec417f8d919a6`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50bf0a9e48ac326120a5de8b5e0cd6b991d704ed4a66448d4fcc8c6ad640d10`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 114.3 KB (114287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b26a3c60d8c62feb971cedd3bd49cd1d5f4d0d0d0149017b32b1573727914be9`  
		Last Modified: Wed, 17 Dec 2025 21:38:19 GMT  
		Size: 2.0 MB (2017127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd733ace70e5f90e389ce8159cbda2291a52bf39e53e2ee4ea6eb8cbccc625e`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821f5deda63bf425c92464f3e686b9fda7f6200ddc49ebacb324b2a45ec0d633`  
		Last Modified: Wed, 17 Dec 2025 21:38:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:19f5876a625b474e4eea9e963de1422ad480c97357d44cd8604896e2da517d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd50fa1a24cfb1dea4e93374baa1e967c2f0fddd79dfa74422b955c193ea89a6`

```dockerfile
```

-	Layers:
	-	`sha256:4d2cbcf3625eaa8b19de7227c701c14f9bd69378a6e698f5aee36b0eb01f2167`  
		Last Modified: Wed, 17 Dec 2025 22:35:35 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:235e217cf2514537b942b1cb8a5ffbbe2ecee441b9373e75871acd7a34391107`  
		Last Modified: Wed, 17 Dec 2025 22:35:36 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:latest`

```console
$ docker pull memcached@sha256:6d4a394b5184f38fcdedabebc810a1e63861427e44215ec8a48a276678236df9
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
$ docker pull memcached@sha256:d8a6e6b246f27a6bbcdfda8a9a06e436178aa58c717448c641a6815f3cc38467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30627609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c80d74d8037160ffc9363dc03f0b6461d3c4cdd69da6460620b26838cb33a671`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 05:30:55 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 09 Dec 2025 05:31:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 05:56:35 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 09 Dec 2025 05:56:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 09 Dec 2025 05:56:35 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 09 Dec 2025 05:56:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 09 Dec 2025 05:56:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 05:56:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 09 Dec 2025 05:56:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Dec 2025 05:56:35 GMT
USER memcache
# Tue, 09 Dec 2025 05:56:35 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 09 Dec 2025 05:56:35 GMT
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
	-	`sha256:e9481f8b437fde8b1c89c79b65538c260df5216129bbe341f98c35935b4fe171`  
		Last Modified: Tue, 09 Dec 2025 05:57:38 GMT  
		Size: 2.2 MB (2219867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe3ccefbdcfdf466052c783e0982017ab232dd919bf46bb40b57edc66cee678`  
		Last Modified: Tue, 09 Dec 2025 05:57:38 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0be3eb5d00166beb14be204124c9c1033e288c0843f2c4aad6a372420a36c6`  
		Last Modified: Tue, 09 Dec 2025 05:57:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:0d07cca14f06f49448edd46f7de94275f31b7fd189fb725cb196bd96aa1ce642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:176f611a3de50a80e211655f970b224ae64d5ab4d2bb1aa8785a22161fe14060`

```dockerfile
```

-	Layers:
	-	`sha256:5f35bc7d6cd5ba3a512b097e6894fe90d53c248ba00f25fb4e1cc8f760d64548`  
		Last Modified: Tue, 09 Dec 2025 07:34:40 GMT  
		Size: 2.0 MB (2002192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18b98ed8b5ce7f2a905ffa540823ace4ea6f63ea74d51da31800c23d9fae6c1f`  
		Last Modified: Tue, 09 Dec 2025 07:34:41 GMT  
		Size: 22.2 KB (22226 bytes)  
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
$ docker pull memcached@sha256:6d4a394b5184f38fcdedabebc810a1e63861427e44215ec8a48a276678236df9
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
$ docker pull memcached@sha256:d8a6e6b246f27a6bbcdfda8a9a06e436178aa58c717448c641a6815f3cc38467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30627609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c80d74d8037160ffc9363dc03f0b6461d3c4cdd69da6460620b26838cb33a671`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 05:30:55 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 09 Dec 2025 05:31:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 05:56:35 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 09 Dec 2025 05:56:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 09 Dec 2025 05:56:35 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 09 Dec 2025 05:56:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 09 Dec 2025 05:56:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 05:56:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 09 Dec 2025 05:56:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Dec 2025 05:56:35 GMT
USER memcache
# Tue, 09 Dec 2025 05:56:35 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 09 Dec 2025 05:56:35 GMT
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
	-	`sha256:e9481f8b437fde8b1c89c79b65538c260df5216129bbe341f98c35935b4fe171`  
		Last Modified: Tue, 09 Dec 2025 05:57:38 GMT  
		Size: 2.2 MB (2219867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe3ccefbdcfdf466052c783e0982017ab232dd919bf46bb40b57edc66cee678`  
		Last Modified: Tue, 09 Dec 2025 05:57:38 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0be3eb5d00166beb14be204124c9c1033e288c0843f2c4aad6a372420a36c6`  
		Last Modified: Tue, 09 Dec 2025 05:57:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:0d07cca14f06f49448edd46f7de94275f31b7fd189fb725cb196bd96aa1ce642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:176f611a3de50a80e211655f970b224ae64d5ab4d2bb1aa8785a22161fe14060`

```dockerfile
```

-	Layers:
	-	`sha256:5f35bc7d6cd5ba3a512b097e6894fe90d53c248ba00f25fb4e1cc8f760d64548`  
		Last Modified: Tue, 09 Dec 2025 07:34:40 GMT  
		Size: 2.0 MB (2002192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18b98ed8b5ce7f2a905ffa540823ace4ea6f63ea74d51da31800c23d9fae6c1f`  
		Last Modified: Tue, 09 Dec 2025 07:34:41 GMT  
		Size: 22.2 KB (22226 bytes)  
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
