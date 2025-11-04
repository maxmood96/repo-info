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
$ docker pull memcached@sha256:050de63e6c082df85f93ffed9c388004b3c6257a06f1904e8628a6f87658eb99
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
$ docker pull memcached@sha256:04cfb7a52848a5ddab7b57674b37c9b7b392d93ec11f0c9a4c300a9bbd1c19a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32209888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0b3dcfe086b67312e8b165a92d8e71b517bf64b356c0c804270d2330e2577c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:05:54 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 04:05:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:08:37 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 04:08:37 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 04:08:37 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 04:08:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 04:08:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:08:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 04:08:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 04:08:38 GMT
USER memcache
# Tue, 04 Nov 2025 04:08:38 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 04:08:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95dd2497c5fb854f1d1cb6790613048eae391c70dd7fe1d2c54ea024889782ad`  
		Last Modified: Tue, 04 Nov 2025 04:08:50 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5e80885bbbbd2ccaf87a97c9f6da9eb3a9b7395ce5e2b73a110224cfbcfb1e`  
		Last Modified: Tue, 04 Nov 2025 04:08:50 GMT  
		Size: 136.6 KB (136597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be7e82464812bb6ab2d37c74a6636ec8d73ec4154a192a75342dfa2f64cc8da`  
		Last Modified: Tue, 04 Nov 2025 04:08:50 GMT  
		Size: 2.3 MB (2293674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18ba826b4b67fa295ff82d2b102a5f2db243fabcb7cc2acac6cc3c33a1cbf4a`  
		Last Modified: Tue, 04 Nov 2025 04:08:50 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654bd5f6e9c2c18716bbdc27ac8f5eab96044427da57f1cb8ee268d2cd3b5f03`  
		Last Modified: Tue, 04 Nov 2025 04:08:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:b78568d9b4a4cd24bae6187909a2a4a808abc29638602ee6aac1885173203e35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b08f68a528f6821adc34258cb89e510c9bf97f5596cf2e47ce7b30ba202cea`

```dockerfile
```

-	Layers:
	-	`sha256:549c9101b19d3697bed0386c9c6378a334bce6d392f694130d47f2033273b571`  
		Last Modified: Tue, 04 Nov 2025 10:34:35 GMT  
		Size: 2.0 MB (2008234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26c87354a983796083082c9e84ccf372217e5a602e78aefdec01fc26eae125ce`  
		Last Modified: Tue, 04 Nov 2025 10:34:36 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v5

```console
$ docker pull memcached@sha256:cfd8f3dc480855d184b335ea9b7c334731ce495de10ef2f2f17b4f82bedf1965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30319386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4fa3d1c819bb913d28b672eedf487f5165ff2dc4e5968326e550efb418196ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 00:24:40 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 00:24:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:28:01 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 00:28:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 00:28:01 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 00:28:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 00:28:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:28:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 00:28:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:28:01 GMT
USER memcache
# Tue, 04 Nov 2025 00:28:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 00:28:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:453afc2258d7bc5729fed5672fb95bafa092e30a933b4377a12034be940a671b`  
		Last Modified: Tue, 04 Nov 2025 00:13:12 GMT  
		Size: 27.9 MB (27946438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3da1461ffd1574069e2ddea407a8d31a9f215a260352498c03bb19d38c7d7ca`  
		Last Modified: Tue, 04 Nov 2025 00:28:13 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4066eb4ba0932fcecba129384e7059abaee0e303654cc15d444f8c6aa11e69bf`  
		Last Modified: Tue, 04 Nov 2025 00:28:13 GMT  
		Size: 144.0 KB (144040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f429e8aa4399dcb073c93dceeb4c04af1a46da5d750c71a36dcff1a94ab840`  
		Last Modified: Tue, 04 Nov 2025 00:28:13 GMT  
		Size: 2.2 MB (2227397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100f4b89d2a8997d39ef62d45e5590e944f3120ba301e303025c7ccaac6da369`  
		Last Modified: Tue, 04 Nov 2025 00:28:13 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334cb0302a41a8c70f7874d7de08c32eb550581a5fc8b17c9b565b9cecdb8149`  
		Last Modified: Tue, 04 Nov 2025 00:28:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:281d772292417096430072e287dae06f36229ebd35a2c308d81eccc1862e99bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956875d70010cc91e002ae89b4a07ce9edfc12bc2a743b377162df7dd92e6f05`

```dockerfile
```

-	Layers:
	-	`sha256:c19709d33e93cfcba6b59a36ac6efba06597c00114be0ab5c2aaddf33ee8ba33`  
		Last Modified: Tue, 04 Nov 2025 07:34:24 GMT  
		Size: 2.0 MB (2011237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a60d569262f9d2f585a47be2ccf35c498002df82c55fd19ebcbaea6f9cd101f9`  
		Last Modified: Tue, 04 Nov 2025 07:34:25 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v7

```console
$ docker pull memcached@sha256:fb4a02a784ff9c44adb4a72aa161b935ed3bd148e49b37fc5e68a1f3aa30a87d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28532441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e70b324b1a195c841f52ba1facea8f75482e1bb049f38d17f8a8b69185f65166`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:06:51 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 02:06:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:09:59 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 02:09:59 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 02:09:59 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 02:09:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 02:09:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 02:09:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 02:09:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 02:09:59 GMT
USER memcache
# Tue, 04 Nov 2025 02:09:59 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 02:09:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f9bebc6d7be8fb19e90bd816cf5ea46e325d9d8d019345bd7e83bb27165e1c`  
		Last Modified: Tue, 04 Nov 2025 02:10:11 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d87b4f74b7b681280e1de65d55c7fef9af3294203ca9753541c48a7dbd67ac`  
		Last Modified: Tue, 04 Nov 2025 02:10:11 GMT  
		Size: 135.3 KB (135301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012aaeffd16b06fc90dbc9cf1682d2a8cb96482af9e0582ebc1dc6881617ba3d`  
		Last Modified: Tue, 04 Nov 2025 02:10:11 GMT  
		Size: 2.2 MB (2182590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30071a0aa370d64f866b34ab3ab9ed0d6e2f30dee5e631bc9b787ff5a9f4fdc0`  
		Last Modified: Tue, 04 Nov 2025 02:10:11 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18d6989abdf4813c6c982f04f7bc42405ebe217f82671824a3bd75a1f923f9c`  
		Last Modified: Tue, 04 Nov 2025 02:10:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:672ae9e81bd13a12a5ae6790d4619294b51a1cfd04a6af50c523797512fc75f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95641a91a03ab503b7750055d3fe6cf1474b1c75ce6288b8966a514375dddb1a`

```dockerfile
```

-	Layers:
	-	`sha256:f13ec9279ccf6461d334439358fdee3b542d225588c6a3857991636d57ce10ee`  
		Last Modified: Tue, 04 Nov 2025 10:34:42 GMT  
		Size: 2.0 MB (2009694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37374c73a31babc67e99ab9936b2166b55c09c55f1bc4cfff80e65a3c40d5425`  
		Last Modified: Tue, 04 Nov 2025 10:34:43 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:bc5ac38c2657d7c6d375374985e9293fb3744a75edbd96cb7a7524cc14c95d08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32572446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1f397ae776296a0fd6edeebc664c5cc9fbc3f08556289a5a1fe41c75626d379`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:17:41 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 01:17:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:20:41 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 01:20:41 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 01:20:41 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 01:20:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 01:20:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:20:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 01:20:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:20:41 GMT
USER memcache
# Tue, 04 Nov 2025 01:20:41 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 01:20:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db64d9b58942143a8d96f7823245feb1d4bf27c04222e71dbe7cedfce33d7e7f`  
		Last Modified: Tue, 04 Nov 2025 01:20:54 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e45c84ea5c10a0167bca67aede44a66fd08b708143ccb896170e30885ea50f1`  
		Last Modified: Tue, 04 Nov 2025 01:20:54 GMT  
		Size: 153.4 KB (153400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317fc2721e7de3ecc81d907c076c0de0aa0c4a80a7810a77e53335eab94adedc`  
		Last Modified: Tue, 04 Nov 2025 01:20:54 GMT  
		Size: 2.3 MB (2275238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a6f24d2569f3c38db7873c0a8f3942c5c7b876fa9eff4eaeca997bc6dc28df`  
		Last Modified: Tue, 04 Nov 2025 01:20:54 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d9e0c677fc63b66e178f9171abc553450378c9046b77cbcc52126068101766c`  
		Last Modified: Tue, 04 Nov 2025 01:20:54 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:8d2e6520d11120bd0b01076b34657bd1b1a785b38c6f7048bc58db91821f584f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97a00b54cc845295e717a2bf8ba5f7b91d5fb25acd85c6c399b94596dd67465`

```dockerfile
```

-	Layers:
	-	`sha256:7061efa09aee437d8b815835ea3f0afa471b9f76cb95323b8260dc846c1f49f1`  
		Last Modified: Tue, 04 Nov 2025 10:34:47 GMT  
		Size: 2.0 MB (2008550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0254e16c47bdde3eb7e8d57383df36625fad7398861b5aca562e447505806a8`  
		Last Modified: Tue, 04 Nov 2025 10:34:47 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:e950b4f76df4b7ad0e9dcc9f2357df6ae35314e232ad23b0ec4fb3c3beb2b84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33688177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9910abbdac4661a59a1d8fe6b43f96cd0abdde92371f8c995e7216d706f375bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:19:48 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 01:19:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:22:46 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 01:22:46 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 01:22:46 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 01:22:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 01:22:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:22:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 01:22:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:22:46 GMT
USER memcache
# Tue, 04 Nov 2025 01:22:46 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 01:22:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7f24a3a0c200106d0d9ab7b6264e50c689910154fb57bf08185b9eaf995db758`  
		Last Modified: Tue, 04 Nov 2025 00:13:54 GMT  
		Size: 31.3 MB (31294783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6840654bcf5429c7954c0483368ccd033e4222b3098ca64904c590f04dd07624`  
		Last Modified: Tue, 04 Nov 2025 01:22:59 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66205a10db2dcede178afb15530db6f282ec7194f11ffe734d9496d8b30e35a2`  
		Last Modified: Tue, 04 Nov 2025 01:22:59 GMT  
		Size: 147.4 KB (147440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b63b70a9c43a2f37c5f37f50e2aaf507c970f0133b7aaaea29fdb4e826c18b1`  
		Last Modified: Tue, 04 Nov 2025 01:23:00 GMT  
		Size: 2.2 MB (2244441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a3c1d29eba0037255cb4c7903d5de630770804520cfdb28ce05b112d526ed3`  
		Last Modified: Tue, 04 Nov 2025 01:22:59 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8da84bbfbc97884490625408deb986e43d5843e48291516064a41ab6d5963e`  
		Last Modified: Tue, 04 Nov 2025 01:22:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:51b41d632670fe8c786707c7977f9136c593c137bcde08516527421769778ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7473e22367c8e8c736bb1ce76169b1b4abf93fa0b057dec9103c4dccf90efc2`

```dockerfile
```

-	Layers:
	-	`sha256:f90631de8235b43d3b44250b8606b5783cd39dc12e9810fb5993f82a19dfe2ee`  
		Last Modified: Tue, 04 Nov 2025 10:34:51 GMT  
		Size: 2.0 MB (2005391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29d51086244a15fe10ebfe78e299fc7a89dd09601c8753741004d27949898c16`  
		Last Modified: Tue, 04 Nov 2025 10:34:52 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:ead041ea0e5c06d481ac304f7b4076a3339d849fcdffa3d25603418dc2fe82e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36187425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b0128aff763178ac8bb867e486c2450bacad45f79a5ff629194be435141070`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:52:27 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 01:52:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:55:40 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 01:55:40 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 01:55:40 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 01:55:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 01:55:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:55:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 01:55:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:55:41 GMT
USER memcache
# Tue, 04 Nov 2025 01:55:41 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 01:55:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126ce0c080daa81edc8784c59f60350b32083b3201304709775cf554155f80af`  
		Last Modified: Tue, 04 Nov 2025 01:56:04 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4c9857fe1f3ded2ba6c29c2f9591c7f5b2bfc46517527fac13f4c2b539a9a4`  
		Last Modified: Tue, 04 Nov 2025 01:56:04 GMT  
		Size: 170.2 KB (170244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e15beeee778428c51e89d0b8c3d6ca7931f0324e0a66f6b2bf85b101e9674a`  
		Last Modified: Tue, 04 Nov 2025 01:56:04 GMT  
		Size: 2.4 MB (2417022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d427e3c140105cfdb1a22a00010621a5a0834ce00ba3ea1059f8a63d8b0f5ee5`  
		Last Modified: Tue, 04 Nov 2025 01:56:04 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dfc7efa96996e95dcf030731f854bc07f2c7aa3349e75c4e74c04d924b3c62`  
		Last Modified: Tue, 04 Nov 2025 01:56:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:ad9b48a87b820bbf6c20cb57cd2247fa75ca6de00df26576f784a8f51703c571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1582395261fcee60bb7362c6cff0abd1d7325b4fde3cd609ac637f76aaa7ea5`

```dockerfile
```

-	Layers:
	-	`sha256:f5e9fbdfb8deeebb9142cd4facdedb0629028f8343a64b1e13d26ecb035f3c84`  
		Last Modified: Tue, 04 Nov 2025 10:34:55 GMT  
		Size: 2.0 MB (2011835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3dd30af34832aa3d277b4b6882a9786e4225d5a7387d5af5a66cadc59adc22d`  
		Last Modified: Tue, 04 Nov 2025 10:34:56 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; riscv64

```console
$ docker pull memcached@sha256:56542c7304b39c7980a644419d2ab6f603477cc9e1cb9c575d45b8c4220e0c6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30630140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e279bc62f41c4006902271742290cdde9d77c2121c1b4db697d09d01c690860e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 03:30:39 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 03:31:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:44:44 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 03:44:44 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 03:44:44 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 03:44:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 03:44:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 03:44:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 03:44:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 03:44:45 GMT
USER memcache
# Tue, 04 Nov 2025 03:44:45 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 03:44:45 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b836efb62045adb472c559fe0a4cedfe183f60ae9e36defd9b46efc4886fff56`  
		Last Modified: Tue, 04 Nov 2025 03:45:39 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db437579ba55d9291ad05cd904e857adb520e8189f0cc2fb207b475c10a95ee`  
		Last Modified: Tue, 04 Nov 2025 03:45:39 GMT  
		Size: 133.0 KB (132994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ca1f664c3ee469c225e4241d90dabf5a36c9fd5282ec51011fe16b9fcd5882`  
		Last Modified: Tue, 04 Nov 2025 03:45:39 GMT  
		Size: 2.2 MB (2219849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f5b56363e737d5d4b276274dc82b3ae7d3772bb1d6cadc5fb0c117ad6d004e`  
		Last Modified: Tue, 04 Nov 2025 03:45:39 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92139c3e4198e9ce61d77b8a86d621938a3390898a4ac22ba81eefd286a78cc7`  
		Last Modified: Tue, 04 Nov 2025 03:45:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:a72757dfcc56cb3edf581d72aa35ca18e099d18284ccfaabc697a74b2d7c2399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40a19d13356829e752dd3f0c530a1f2ef0abfc0ca53d29d3d74e1840a1698892`

```dockerfile
```

-	Layers:
	-	`sha256:78add421d4e1ac7755ca522075904f0acd06a15e1c8b9ca1bb0047a7d3ebf187`  
		Last Modified: Tue, 04 Nov 2025 07:34:38 GMT  
		Size: 2.0 MB (2002198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f1fc3731e375af1e0712ec91b83487acb49e907a1168f593f251fe43cb51fb9`  
		Last Modified: Tue, 04 Nov 2025 07:34:39 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:3de73b4ecf32984b0c6603b973257071c81c94af8351b35aa4343407c7315726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32293163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e6900a4460f82b0703aed07dde3c1722bdb7919a582b6b1f22a9ca701cb510f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 06:58:32 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 06:58:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 07:02:23 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 07:02:23 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 07:02:23 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 07:02:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 07:02:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 07:02:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 07:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 07:02:23 GMT
USER memcache
# Tue, 04 Nov 2025 07:02:23 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 07:02:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17527924bc8c8387e810ff986ddbe9998a0b5d55a4850b90b4cea0a897c94a09`  
		Last Modified: Tue, 04 Nov 2025 07:02:40 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54fd3d90bab9e973d6a8c142df91794bdc213e5bafe8926a58809036e1ee1f5`  
		Last Modified: Tue, 04 Nov 2025 07:02:40 GMT  
		Size: 140.4 KB (140429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc993f31fbd52e75a8dfc710d94d4130a8c228be35b7737c5950a5f93a1125a`  
		Last Modified: Tue, 04 Nov 2025 07:02:40 GMT  
		Size: 2.3 MB (2313833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acaa055d548771aab19234adcaf5b3ed727ee85214c303e1035e3e464e0fbda0`  
		Last Modified: Tue, 04 Nov 2025 07:02:40 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c2e1b3aad04d0544265917caef9c91d5ed4496376262541974a707026847f4`  
		Last Modified: Tue, 04 Nov 2025 07:02:40 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:414b070c237a13d5dee83e1db26eb0f953dd5af0753013a8bbd988611aa90e89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5cc4920f789bfe656195ac67c3ddd1a00030591f92b5ac4dc2b0e9dcdd2a0b`

```dockerfile
```

-	Layers:
	-	`sha256:b242fd5db27262af27c5589b736a5ae9f234cb03765c59c73e64818c1cade0c8`  
		Last Modified: Tue, 04 Nov 2025 10:35:02 GMT  
		Size: 2.0 MB (2009671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e15d059f16d47b54c3d82bdf997670c62a062815b64d7e7b486d8de0060691b4`  
		Last Modified: Tue, 04 Nov 2025 10:35:03 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:7b45203a99eb1419c95b875c7e48c5a9eebc0a305eeb09eefc9f3a2cff758a46
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
$ docker pull memcached@sha256:e319c3f1f6623fb2caedb14c4a5c8594f88736d90dc89d19f1ec11c8533ee263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70bce40b6c41c7484f47d1d51e8be171c582e0b3e18f2379dd66e49e3178d86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c711f2e2fe464121135109729faa513b79413712df200207ef35dfb19e550ca`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0cba00095a1ab15ee2ec0bcefea9c1fe601b9533d47626ab2fb6b74bf8a770`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 104.7 KB (104727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9204d372b3172134a4f3bbcf654ab17d33079a3aff6930e16fa7262df7c9cdbe`  
		Last Modified: Wed, 08 Oct 2025 22:42:05 GMT  
		Size: 2.0 MB (2000281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa9dd6a61433e778f70df6cd37bc70c4dcbfa8e0b0e8b1f9a0fc2f993c78685`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5a283c3ec8e0142f3f4b0b17b2901ab6d7dbff9e3f62bf978a03e5d31833f5`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:1cb56f4b692737cc136d1ff3c5dc0ca16e6b7c3be7023b1a9214348578dc4536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 KB (116754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a7a80cd482b54ecad43450e81b2d6858d2397277cf2d8358315295ef8152dc5`

```dockerfile
```

-	Layers:
	-	`sha256:659cc6afa1cde9acfc6444a310575d263f25f2f83d4987d4fddf83e5bb0d3082`  
		Last Modified: Thu, 09 Oct 2025 00:34:37 GMT  
		Size: 96.2 KB (96180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e43c8201b9a29cba2a3392f6a10e9ee6f0d6295f0248c8d3e9a792871224ec10`  
		Last Modified: Thu, 09 Oct 2025 00:34:38 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:43072fb4c4cfd652bf1a32d617dd81060515017e52b14f35faeb2fe26d071dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5557528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87416926a00e28eb0313c62e942bea0ce0517d67c95df6258358f109a49d392c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd90c0f65a0d79d1685d8fefb0f95b02afd962d0b160a1274598cb584ec37d9`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920bb020947e8d1d3b077c6d9861f8953febeb54f94421c689d40240e56b7ff0`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 101.5 KB (101532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4dc3dc5cf827d37f28e2a9a6758089ff72bc10d1915dbb61cce8f30350de40`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 2.0 MB (1950567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b2afb9c93ba0497cadc25e69b15de772b64456929b70dbe23c7ef54faa3815`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d88088c7b652b283feabfeb2974fb4bd7140ebf7da94c5d502f22841f26eb4a`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:bd27295997fc0e77ad410a3e638c230d83e3d366906a449f5349d8311d72e657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a474656b8df51a30dcb397a44bcb48c6ba3cb76e49cc3a108a15a662cd64c4b`

```dockerfile
```

-	Layers:
	-	`sha256:9a80e6fbb7fc2254a12359760da6745c28fe1d3fa2367b1137aad71c6732a8bd`  
		Last Modified: Thu, 09 Oct 2025 00:34:41 GMT  
		Size: 20.5 KB (20510 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:2caa01f7607cf1d95b2e261de80716a27de4077bf25b9dc623688091b78bf4ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c1be64fe03e8832bc6208dfced118762e57dca6b55b4482140c8fc3b06dfb3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0a02f5bd6bf63e96f5b45eda4849003b01c41b23425e7ac5a77eb01b5391e0`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f277f740301c69a561a94545bc7f140ee2d5f4ea87f88c0c861eb7b4f7983b0`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 91.3 KB (91313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e9ebffe0c4c57cd5b7fd1da1fcc7f14e2e881a81673f81e8bde4bf662a45b3`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 1.9 MB (1909853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46526f6db8416530677567eac97b5cfc18e2b86ec5c930d06de26b62f0c7a5c6`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f19627fe74f6edf1d0aa4deb85d035125067fcd28b2ee240aeb110e48330f19`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:09108dd858c6aae1c834fd9c8a7f9f78e552673ee6296d9f5cf2d84c0c26c6fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 KB (116969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9755e3f89f06272910c7fcbcaf44a3cb373b551f73bc7c9dc6dbffe13aad48`

```dockerfile
```

-	Layers:
	-	`sha256:13ba800aa65c8f207645e4069de55b11ad0a2dc87b951414df4bd35ad3923afd`  
		Last Modified: Thu, 09 Oct 2025 00:34:45 GMT  
		Size: 96.2 KB (96248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:636139066de216a683805bafa6cd72b23f1754f8dd2b5854e61578a684260418`  
		Last Modified: Thu, 09 Oct 2025 00:34:46 GMT  
		Size: 20.7 KB (20721 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:03d8054231ea1bb1dbb54d7e8bb32449b95c35475fa280a9b12d78219822fa48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6251299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42028500064e9ca7d32291ca01c636547943d3a6e6f11b80e503166efcfa6149`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098f75f9dd9f7dbf0e5993587a5b4de796bc9c01f2e795b325f1e22fe66c6833`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4c130fe47b24dbff1989543c440e0d6635524f9bf84473a6dc37472ecacac0`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 120.8 KB (120823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a41614e1c7aff72360936c76c0218330a487dd6ff6779cd243ad1c60ab6634`  
		Last Modified: Wed, 08 Oct 2025 21:31:15 GMT  
		Size: 2.0 MB (1991055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8573d5df234537883a638f95501925286c3367fd1cc40a4c6a80b70ef59ffa16`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd6f77485828d14a277cde4d3649153b058047ad8477c919e974016eb3ef6f7`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b47c7c82754dea9552416b18a213b43d6824105eb9a0318e31789b64ebb4524a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 KB (117055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc0f98e226622d3dd6ab1b57679deaa27c10decc2a26c0d7c64feeeae3b6e18`

```dockerfile
```

-	Layers:
	-	`sha256:949b28585bcee0143420765476ff3f8231f4f8049c4d0b3136c102cc9a3b272f`  
		Last Modified: Thu, 09 Oct 2025 00:34:49 GMT  
		Size: 96.3 KB (96284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c10e36727f7634ae28cb6de04bff91b38d77420fce24cf9b31503d14aff0636`  
		Last Modified: Thu, 09 Oct 2025 00:34:50 GMT  
		Size: 20.8 KB (20771 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:3dbd66df3fa527ea9d5ef8e15484f90fd2bc4445e9d21ad40602c7d954a57c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5692091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa2b9eb15af4ed95101c0752bbde283e07e28adfed081d3a9a731aa82d1ab68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5efc90d716eb56816bbbf625c914fe13450e5c8059469e05eaef18ddf200fd`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795865ca1e6e3ac4e3ed32dabe363301a453512615868e180c6c23f28f711154`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 109.5 KB (109526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f93c274afbe9d7756256b49ac152cdbd8b21b7bf4c0e1a564bf36c6940e986e`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 2.0 MB (1962279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8db2caca7c819c90101fe1d4c62396dd78bf9677be35f005e0026d6b76c095`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d53143d130829def781c84b33cfc19fa4ac216deae7acd8c510186dd525afdb`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c7b1229c17eb2270b6a966423e63e1ad70b16a7c79c87d2ea9df82f9d733d383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 KB (116649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392076445efbd53c3eea2f14c49336ed1c8f521c209369edbb2e7686671c310a`

```dockerfile
```

-	Layers:
	-	`sha256:e91e563cbe752ee16efaa2007b7b0f49392b0f5326018a94f34a2e187c1cb743`  
		Last Modified: Wed, 08 Oct 2025 21:34:33 GMT  
		Size: 96.1 KB (96135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:207733714725a312d472d7f8657279033f48a213756c3f87714f3b4bd3e03195`  
		Last Modified: Wed, 08 Oct 2025 21:34:34 GMT  
		Size: 20.5 KB (20514 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:7e2b422eba145439e8c30b7e3191cc1f8498a721f4ca3d90c31fbc5ed80aee7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5951257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48257955bab73ec394b46e2350210da8ec488c125ff0c7cb4ce03893fff291d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8caf4ead4d89e7cb932248ec2c3e7ae5ee7efb8989eb2ab51d407f7094fe6bf`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff948909dcd7ac6c4301b934b30465617e899ca99e5cb6ac6e537be4e6f6144`  
		Last Modified: Thu, 09 Oct 2025 01:11:40 GMT  
		Size: 124.3 KB (124318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f700c3c0f9d01825484f8ddf4ea689855d4c1ed78848558c4c2bf8bf817caed0`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 2.1 MB (2093342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ee4b65e8fe80e2ad3919c8c15d8855829430a43445decbd73237095a9771a9`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06240440b6e443402b0a5ca4dc97a2225661f3da03b4c6bc67c2e9443ba95ce4`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ea61cc67a9e9ffc7a8aaf326e701ea53f5d074dc907d4ad89b4274c4cb8ce804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213afd703e8e97590346c2a301a08bd84f590c17e18aefcbcdefc4d93622c57b`

```dockerfile
```

-	Layers:
	-	`sha256:d3b5325b8aa7c43ef1c7b6f6f4a09cbcfd07d64d439c41a950bc41da09e060ff`  
		Last Modified: Thu, 09 Oct 2025 03:34:33 GMT  
		Size: 94.3 KB (94287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dd52654f2c500e460030d1f9328acbf6d095a5e2d004a4f6417b79522c7fddf`  
		Last Modified: Thu, 09 Oct 2025 03:34:34 GMT  
		Size: 20.6 KB (20647 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:588117152fae8688e5cee8aa65963a1adb1e3851845da5da3e18c80099cdb1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5559076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c983e214f48d62c0be8ffbceb2a86b504aa71c02ac195047119fe264f612c35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ec1911f91425f5b1fc00d35f661d0dcb2691cdbff9a0ea4a65789eb8dd9b89`  
		Last Modified: Thu, 09 Oct 2025 04:54:06 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb577a02d7726836381f3dfcda7cb11472d8e99ef2feb088a9570bc2c0203f15`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 107.9 KB (107909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d6a77fdbd897c87616b71f12d107a1db186b3944ccdad6b89e33186d2645bf`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 1.9 MB (1934579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2879148828c59fde0e744fb56e2490c68a2e98902f3c6a0d01bb8381588a58ba`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00990bf09cdd6c9e756438f8b076739cea749be4889b317c88bf5d06c908e9d8`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:da1dc0b73e866df98aacb962264ed5b50bf3f61862f76c42828b9a179c32e455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b8b102978a5d01b2e4ec0cf55dd00df9776a17f5f31b8bae680908b73d2e1de`

```dockerfile
```

-	Layers:
	-	`sha256:2de1c9249a94130556f0db88a655ed432c15ad40e151579870de604725fbc086`  
		Last Modified: Thu, 09 Oct 2025 06:34:34 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0262f9b3a73d1455147e4436e4bf7da9aa19a7d385d28a807688e23d6a1f1d05`  
		Last Modified: Thu, 09 Oct 2025 06:34:34 GMT  
		Size: 20.6 KB (20648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:ed5969236f4728c97696471e08c88864c21019ea227118b3336d6484ed3e5b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5804524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c049e21de6c2be2f58a69ee9eb633a51a0491febb4b48fa476556586ac0fbd96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d91bfc8fa88993cee87c33ea18494c5e9f0ad8e5b6f644411e9cd648982653`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a682e0d523bab9ef58be0ad290abcee8563e45ceccc9d04fc9b47308aeb709b`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 113.5 KB (113502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9fe3585b1938fd376ffbce3ef824ed7bc20ed49039f98e279ff5ab6159b81e`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 2.0 MB (2040430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9870bcfd315f7fc77b2fb8e80646695f277bc2e7689cf73b395e230aa6fe327c`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20f8ef4bac131999b759bd8b49d1474c540fb1874c8db4e3f4b21a7262b6903`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2d42234a0a18e44870f34c7796f717e9d61b56556ba027f9fae085adfbeeb7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd89a980babfe6204633d40fbc2b82da6c42a3c42f43f980c4d29d3015fd40b`

```dockerfile
```

-	Layers:
	-	`sha256:70fb18f0cec1c9db308335dffc76a505d0855256e74dd6cd73079481cccac057`  
		Last Modified: Thu, 09 Oct 2025 03:34:39 GMT  
		Size: 94.2 KB (94229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02c95a382d7ff8c2fab05ba8609f8b69576ec785d085ed04e606445051336db9`  
		Last Modified: Thu, 09 Oct 2025 03:34:40 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine3.22`

```console
$ docker pull memcached@sha256:7b45203a99eb1419c95b875c7e48c5a9eebc0a305eeb09eefc9f3a2cff758a46
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
$ docker pull memcached@sha256:e319c3f1f6623fb2caedb14c4a5c8594f88736d90dc89d19f1ec11c8533ee263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70bce40b6c41c7484f47d1d51e8be171c582e0b3e18f2379dd66e49e3178d86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c711f2e2fe464121135109729faa513b79413712df200207ef35dfb19e550ca`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0cba00095a1ab15ee2ec0bcefea9c1fe601b9533d47626ab2fb6b74bf8a770`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 104.7 KB (104727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9204d372b3172134a4f3bbcf654ab17d33079a3aff6930e16fa7262df7c9cdbe`  
		Last Modified: Wed, 08 Oct 2025 22:42:05 GMT  
		Size: 2.0 MB (2000281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa9dd6a61433e778f70df6cd37bc70c4dcbfa8e0b0e8b1f9a0fc2f993c78685`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5a283c3ec8e0142f3f4b0b17b2901ab6d7dbff9e3f62bf978a03e5d31833f5`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:1cb56f4b692737cc136d1ff3c5dc0ca16e6b7c3be7023b1a9214348578dc4536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 KB (116754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a7a80cd482b54ecad43450e81b2d6858d2397277cf2d8358315295ef8152dc5`

```dockerfile
```

-	Layers:
	-	`sha256:659cc6afa1cde9acfc6444a310575d263f25f2f83d4987d4fddf83e5bb0d3082`  
		Last Modified: Thu, 09 Oct 2025 00:34:37 GMT  
		Size: 96.2 KB (96180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e43c8201b9a29cba2a3392f6a10e9ee6f0d6295f0248c8d3e9a792871224ec10`  
		Last Modified: Thu, 09 Oct 2025 00:34:38 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.22` - linux; arm variant v6

```console
$ docker pull memcached@sha256:43072fb4c4cfd652bf1a32d617dd81060515017e52b14f35faeb2fe26d071dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5557528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87416926a00e28eb0313c62e942bea0ce0517d67c95df6258358f109a49d392c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd90c0f65a0d79d1685d8fefb0f95b02afd962d0b160a1274598cb584ec37d9`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920bb020947e8d1d3b077c6d9861f8953febeb54f94421c689d40240e56b7ff0`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 101.5 KB (101532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4dc3dc5cf827d37f28e2a9a6758089ff72bc10d1915dbb61cce8f30350de40`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 2.0 MB (1950567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b2afb9c93ba0497cadc25e69b15de772b64456929b70dbe23c7ef54faa3815`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d88088c7b652b283feabfeb2974fb4bd7140ebf7da94c5d502f22841f26eb4a`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:bd27295997fc0e77ad410a3e638c230d83e3d366906a449f5349d8311d72e657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a474656b8df51a30dcb397a44bcb48c6ba3cb76e49cc3a108a15a662cd64c4b`

```dockerfile
```

-	Layers:
	-	`sha256:9a80e6fbb7fc2254a12359760da6745c28fe1d3fa2367b1137aad71c6732a8bd`  
		Last Modified: Thu, 09 Oct 2025 00:34:41 GMT  
		Size: 20.5 KB (20510 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.22` - linux; arm variant v7

```console
$ docker pull memcached@sha256:2caa01f7607cf1d95b2e261de80716a27de4077bf25b9dc623688091b78bf4ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c1be64fe03e8832bc6208dfced118762e57dca6b55b4482140c8fc3b06dfb3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0a02f5bd6bf63e96f5b45eda4849003b01c41b23425e7ac5a77eb01b5391e0`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f277f740301c69a561a94545bc7f140ee2d5f4ea87f88c0c861eb7b4f7983b0`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 91.3 KB (91313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e9ebffe0c4c57cd5b7fd1da1fcc7f14e2e881a81673f81e8bde4bf662a45b3`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 1.9 MB (1909853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46526f6db8416530677567eac97b5cfc18e2b86ec5c930d06de26b62f0c7a5c6`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f19627fe74f6edf1d0aa4deb85d035125067fcd28b2ee240aeb110e48330f19`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:09108dd858c6aae1c834fd9c8a7f9f78e552673ee6296d9f5cf2d84c0c26c6fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 KB (116969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9755e3f89f06272910c7fcbcaf44a3cb373b551f73bc7c9dc6dbffe13aad48`

```dockerfile
```

-	Layers:
	-	`sha256:13ba800aa65c8f207645e4069de55b11ad0a2dc87b951414df4bd35ad3923afd`  
		Last Modified: Thu, 09 Oct 2025 00:34:45 GMT  
		Size: 96.2 KB (96248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:636139066de216a683805bafa6cd72b23f1754f8dd2b5854e61578a684260418`  
		Last Modified: Thu, 09 Oct 2025 00:34:46 GMT  
		Size: 20.7 KB (20721 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:03d8054231ea1bb1dbb54d7e8bb32449b95c35475fa280a9b12d78219822fa48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6251299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42028500064e9ca7d32291ca01c636547943d3a6e6f11b80e503166efcfa6149`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098f75f9dd9f7dbf0e5993587a5b4de796bc9c01f2e795b325f1e22fe66c6833`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4c130fe47b24dbff1989543c440e0d6635524f9bf84473a6dc37472ecacac0`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 120.8 KB (120823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a41614e1c7aff72360936c76c0218330a487dd6ff6779cd243ad1c60ab6634`  
		Last Modified: Wed, 08 Oct 2025 21:31:15 GMT  
		Size: 2.0 MB (1991055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8573d5df234537883a638f95501925286c3367fd1cc40a4c6a80b70ef59ffa16`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd6f77485828d14a277cde4d3649153b058047ad8477c919e974016eb3ef6f7`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:b47c7c82754dea9552416b18a213b43d6824105eb9a0318e31789b64ebb4524a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 KB (117055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc0f98e226622d3dd6ab1b57679deaa27c10decc2a26c0d7c64feeeae3b6e18`

```dockerfile
```

-	Layers:
	-	`sha256:949b28585bcee0143420765476ff3f8231f4f8049c4d0b3136c102cc9a3b272f`  
		Last Modified: Thu, 09 Oct 2025 00:34:49 GMT  
		Size: 96.3 KB (96284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c10e36727f7634ae28cb6de04bff91b38d77420fce24cf9b31503d14aff0636`  
		Last Modified: Thu, 09 Oct 2025 00:34:50 GMT  
		Size: 20.8 KB (20771 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.22` - linux; 386

```console
$ docker pull memcached@sha256:3dbd66df3fa527ea9d5ef8e15484f90fd2bc4445e9d21ad40602c7d954a57c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5692091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa2b9eb15af4ed95101c0752bbde283e07e28adfed081d3a9a731aa82d1ab68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5efc90d716eb56816bbbf625c914fe13450e5c8059469e05eaef18ddf200fd`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795865ca1e6e3ac4e3ed32dabe363301a453512615868e180c6c23f28f711154`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 109.5 KB (109526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f93c274afbe9d7756256b49ac152cdbd8b21b7bf4c0e1a564bf36c6940e986e`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 2.0 MB (1962279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8db2caca7c819c90101fe1d4c62396dd78bf9677be35f005e0026d6b76c095`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d53143d130829def781c84b33cfc19fa4ac216deae7acd8c510186dd525afdb`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:c7b1229c17eb2270b6a966423e63e1ad70b16a7c79c87d2ea9df82f9d733d383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 KB (116649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392076445efbd53c3eea2f14c49336ed1c8f521c209369edbb2e7686671c310a`

```dockerfile
```

-	Layers:
	-	`sha256:e91e563cbe752ee16efaa2007b7b0f49392b0f5326018a94f34a2e187c1cb743`  
		Last Modified: Wed, 08 Oct 2025 21:34:33 GMT  
		Size: 96.1 KB (96135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:207733714725a312d472d7f8657279033f48a213756c3f87714f3b4bd3e03195`  
		Last Modified: Wed, 08 Oct 2025 21:34:34 GMT  
		Size: 20.5 KB (20514 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.22` - linux; ppc64le

```console
$ docker pull memcached@sha256:7e2b422eba145439e8c30b7e3191cc1f8498a721f4ca3d90c31fbc5ed80aee7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5951257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48257955bab73ec394b46e2350210da8ec488c125ff0c7cb4ce03893fff291d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8caf4ead4d89e7cb932248ec2c3e7ae5ee7efb8989eb2ab51d407f7094fe6bf`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff948909dcd7ac6c4301b934b30465617e899ca99e5cb6ac6e537be4e6f6144`  
		Last Modified: Thu, 09 Oct 2025 01:11:40 GMT  
		Size: 124.3 KB (124318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f700c3c0f9d01825484f8ddf4ea689855d4c1ed78848558c4c2bf8bf817caed0`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 2.1 MB (2093342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ee4b65e8fe80e2ad3919c8c15d8855829430a43445decbd73237095a9771a9`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06240440b6e443402b0a5ca4dc97a2225661f3da03b4c6bc67c2e9443ba95ce4`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:ea61cc67a9e9ffc7a8aaf326e701ea53f5d074dc907d4ad89b4274c4cb8ce804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213afd703e8e97590346c2a301a08bd84f590c17e18aefcbcdefc4d93622c57b`

```dockerfile
```

-	Layers:
	-	`sha256:d3b5325b8aa7c43ef1c7b6f6f4a09cbcfd07d64d439c41a950bc41da09e060ff`  
		Last Modified: Thu, 09 Oct 2025 03:34:33 GMT  
		Size: 94.3 KB (94287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dd52654f2c500e460030d1f9328acbf6d095a5e2d004a4f6417b79522c7fddf`  
		Last Modified: Thu, 09 Oct 2025 03:34:34 GMT  
		Size: 20.6 KB (20647 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.22` - linux; riscv64

```console
$ docker pull memcached@sha256:588117152fae8688e5cee8aa65963a1adb1e3851845da5da3e18c80099cdb1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5559076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c983e214f48d62c0be8ffbceb2a86b504aa71c02ac195047119fe264f612c35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ec1911f91425f5b1fc00d35f661d0dcb2691cdbff9a0ea4a65789eb8dd9b89`  
		Last Modified: Thu, 09 Oct 2025 04:54:06 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb577a02d7726836381f3dfcda7cb11472d8e99ef2feb088a9570bc2c0203f15`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 107.9 KB (107909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d6a77fdbd897c87616b71f12d107a1db186b3944ccdad6b89e33186d2645bf`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 1.9 MB (1934579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2879148828c59fde0e744fb56e2490c68a2e98902f3c6a0d01bb8381588a58ba`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00990bf09cdd6c9e756438f8b076739cea749be4889b317c88bf5d06c908e9d8`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:da1dc0b73e866df98aacb962264ed5b50bf3f61862f76c42828b9a179c32e455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b8b102978a5d01b2e4ec0cf55dd00df9776a17f5f31b8bae680908b73d2e1de`

```dockerfile
```

-	Layers:
	-	`sha256:2de1c9249a94130556f0db88a655ed432c15ad40e151579870de604725fbc086`  
		Last Modified: Thu, 09 Oct 2025 06:34:34 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0262f9b3a73d1455147e4436e4bf7da9aa19a7d385d28a807688e23d6a1f1d05`  
		Last Modified: Thu, 09 Oct 2025 06:34:34 GMT  
		Size: 20.6 KB (20648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.22` - linux; s390x

```console
$ docker pull memcached@sha256:ed5969236f4728c97696471e08c88864c21019ea227118b3336d6484ed3e5b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5804524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c049e21de6c2be2f58a69ee9eb633a51a0491febb4b48fa476556586ac0fbd96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d91bfc8fa88993cee87c33ea18494c5e9f0ad8e5b6f644411e9cd648982653`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a682e0d523bab9ef58be0ad290abcee8563e45ceccc9d04fc9b47308aeb709b`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 113.5 KB (113502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9fe3585b1938fd376ffbce3ef824ed7bc20ed49039f98e279ff5ab6159b81e`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 2.0 MB (2040430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9870bcfd315f7fc77b2fb8e80646695f277bc2e7689cf73b395e230aa6fe327c`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20f8ef4bac131999b759bd8b49d1474c540fb1874c8db4e3f4b21a7262b6903`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:2d42234a0a18e44870f34c7796f717e9d61b56556ba027f9fae085adfbeeb7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd89a980babfe6204633d40fbc2b82da6c42a3c42f43f980c4d29d3015fd40b`

```dockerfile
```

-	Layers:
	-	`sha256:70fb18f0cec1c9db308335dffc76a505d0855256e74dd6cd73079481cccac057`  
		Last Modified: Thu, 09 Oct 2025 03:34:39 GMT  
		Size: 94.2 KB (94229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02c95a382d7ff8c2fab05ba8609f8b69576ec785d085ed04e606445051336db9`  
		Last Modified: Thu, 09 Oct 2025 03:34:40 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-trixie`

```console
$ docker pull memcached@sha256:050de63e6c082df85f93ffed9c388004b3c6257a06f1904e8628a6f87658eb99
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
$ docker pull memcached@sha256:04cfb7a52848a5ddab7b57674b37c9b7b392d93ec11f0c9a4c300a9bbd1c19a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32209888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0b3dcfe086b67312e8b165a92d8e71b517bf64b356c0c804270d2330e2577c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:05:54 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 04:05:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:08:37 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 04:08:37 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 04:08:37 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 04:08:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 04:08:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:08:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 04:08:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 04:08:38 GMT
USER memcache
# Tue, 04 Nov 2025 04:08:38 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 04:08:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95dd2497c5fb854f1d1cb6790613048eae391c70dd7fe1d2c54ea024889782ad`  
		Last Modified: Tue, 04 Nov 2025 04:08:50 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5e80885bbbbd2ccaf87a97c9f6da9eb3a9b7395ce5e2b73a110224cfbcfb1e`  
		Last Modified: Tue, 04 Nov 2025 04:08:50 GMT  
		Size: 136.6 KB (136597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be7e82464812bb6ab2d37c74a6636ec8d73ec4154a192a75342dfa2f64cc8da`  
		Last Modified: Tue, 04 Nov 2025 04:08:50 GMT  
		Size: 2.3 MB (2293674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18ba826b4b67fa295ff82d2b102a5f2db243fabcb7cc2acac6cc3c33a1cbf4a`  
		Last Modified: Tue, 04 Nov 2025 04:08:50 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654bd5f6e9c2c18716bbdc27ac8f5eab96044427da57f1cb8ee268d2cd3b5f03`  
		Last Modified: Tue, 04 Nov 2025 04:08:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:b78568d9b4a4cd24bae6187909a2a4a808abc29638602ee6aac1885173203e35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b08f68a528f6821adc34258cb89e510c9bf97f5596cf2e47ce7b30ba202cea`

```dockerfile
```

-	Layers:
	-	`sha256:549c9101b19d3697bed0386c9c6378a334bce6d392f694130d47f2033273b571`  
		Last Modified: Tue, 04 Nov 2025 10:34:35 GMT  
		Size: 2.0 MB (2008234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26c87354a983796083082c9e84ccf372217e5a602e78aefdec01fc26eae125ce`  
		Last Modified: Tue, 04 Nov 2025 10:34:36 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:cfd8f3dc480855d184b335ea9b7c334731ce495de10ef2f2f17b4f82bedf1965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30319386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4fa3d1c819bb913d28b672eedf487f5165ff2dc4e5968326e550efb418196ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 00:24:40 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 00:24:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:28:01 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 00:28:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 00:28:01 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 00:28:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 00:28:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:28:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 00:28:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:28:01 GMT
USER memcache
# Tue, 04 Nov 2025 00:28:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 00:28:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:453afc2258d7bc5729fed5672fb95bafa092e30a933b4377a12034be940a671b`  
		Last Modified: Tue, 04 Nov 2025 00:13:12 GMT  
		Size: 27.9 MB (27946438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3da1461ffd1574069e2ddea407a8d31a9f215a260352498c03bb19d38c7d7ca`  
		Last Modified: Tue, 04 Nov 2025 00:28:13 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4066eb4ba0932fcecba129384e7059abaee0e303654cc15d444f8c6aa11e69bf`  
		Last Modified: Tue, 04 Nov 2025 00:28:13 GMT  
		Size: 144.0 KB (144040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f429e8aa4399dcb073c93dceeb4c04af1a46da5d750c71a36dcff1a94ab840`  
		Last Modified: Tue, 04 Nov 2025 00:28:13 GMT  
		Size: 2.2 MB (2227397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100f4b89d2a8997d39ef62d45e5590e944f3120ba301e303025c7ccaac6da369`  
		Last Modified: Tue, 04 Nov 2025 00:28:13 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334cb0302a41a8c70f7874d7de08c32eb550581a5fc8b17c9b565b9cecdb8149`  
		Last Modified: Tue, 04 Nov 2025 00:28:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:281d772292417096430072e287dae06f36229ebd35a2c308d81eccc1862e99bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956875d70010cc91e002ae89b4a07ce9edfc12bc2a743b377162df7dd92e6f05`

```dockerfile
```

-	Layers:
	-	`sha256:c19709d33e93cfcba6b59a36ac6efba06597c00114be0ab5c2aaddf33ee8ba33`  
		Last Modified: Tue, 04 Nov 2025 07:34:24 GMT  
		Size: 2.0 MB (2011237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a60d569262f9d2f585a47be2ccf35c498002df82c55fd19ebcbaea6f9cd101f9`  
		Last Modified: Tue, 04 Nov 2025 07:34:25 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:fb4a02a784ff9c44adb4a72aa161b935ed3bd148e49b37fc5e68a1f3aa30a87d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28532441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e70b324b1a195c841f52ba1facea8f75482e1bb049f38d17f8a8b69185f65166`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:06:51 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 02:06:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:09:59 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 02:09:59 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 02:09:59 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 02:09:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 02:09:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 02:09:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 02:09:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 02:09:59 GMT
USER memcache
# Tue, 04 Nov 2025 02:09:59 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 02:09:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f9bebc6d7be8fb19e90bd816cf5ea46e325d9d8d019345bd7e83bb27165e1c`  
		Last Modified: Tue, 04 Nov 2025 02:10:11 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d87b4f74b7b681280e1de65d55c7fef9af3294203ca9753541c48a7dbd67ac`  
		Last Modified: Tue, 04 Nov 2025 02:10:11 GMT  
		Size: 135.3 KB (135301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012aaeffd16b06fc90dbc9cf1682d2a8cb96482af9e0582ebc1dc6881617ba3d`  
		Last Modified: Tue, 04 Nov 2025 02:10:11 GMT  
		Size: 2.2 MB (2182590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30071a0aa370d64f866b34ab3ab9ed0d6e2f30dee5e631bc9b787ff5a9f4fdc0`  
		Last Modified: Tue, 04 Nov 2025 02:10:11 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18d6989abdf4813c6c982f04f7bc42405ebe217f82671824a3bd75a1f923f9c`  
		Last Modified: Tue, 04 Nov 2025 02:10:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:672ae9e81bd13a12a5ae6790d4619294b51a1cfd04a6af50c523797512fc75f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95641a91a03ab503b7750055d3fe6cf1474b1c75ce6288b8966a514375dddb1a`

```dockerfile
```

-	Layers:
	-	`sha256:f13ec9279ccf6461d334439358fdee3b542d225588c6a3857991636d57ce10ee`  
		Last Modified: Tue, 04 Nov 2025 10:34:42 GMT  
		Size: 2.0 MB (2009694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37374c73a31babc67e99ab9936b2166b55c09c55f1bc4cfff80e65a3c40d5425`  
		Last Modified: Tue, 04 Nov 2025 10:34:43 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:bc5ac38c2657d7c6d375374985e9293fb3744a75edbd96cb7a7524cc14c95d08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32572446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1f397ae776296a0fd6edeebc664c5cc9fbc3f08556289a5a1fe41c75626d379`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:17:41 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 01:17:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:20:41 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 01:20:41 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 01:20:41 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 01:20:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 01:20:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:20:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 01:20:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:20:41 GMT
USER memcache
# Tue, 04 Nov 2025 01:20:41 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 01:20:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db64d9b58942143a8d96f7823245feb1d4bf27c04222e71dbe7cedfce33d7e7f`  
		Last Modified: Tue, 04 Nov 2025 01:20:54 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e45c84ea5c10a0167bca67aede44a66fd08b708143ccb896170e30885ea50f1`  
		Last Modified: Tue, 04 Nov 2025 01:20:54 GMT  
		Size: 153.4 KB (153400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317fc2721e7de3ecc81d907c076c0de0aa0c4a80a7810a77e53335eab94adedc`  
		Last Modified: Tue, 04 Nov 2025 01:20:54 GMT  
		Size: 2.3 MB (2275238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a6f24d2569f3c38db7873c0a8f3942c5c7b876fa9eff4eaeca997bc6dc28df`  
		Last Modified: Tue, 04 Nov 2025 01:20:54 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d9e0c677fc63b66e178f9171abc553450378c9046b77cbcc52126068101766c`  
		Last Modified: Tue, 04 Nov 2025 01:20:54 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:8d2e6520d11120bd0b01076b34657bd1b1a785b38c6f7048bc58db91821f584f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97a00b54cc845295e717a2bf8ba5f7b91d5fb25acd85c6c399b94596dd67465`

```dockerfile
```

-	Layers:
	-	`sha256:7061efa09aee437d8b815835ea3f0afa471b9f76cb95323b8260dc846c1f49f1`  
		Last Modified: Tue, 04 Nov 2025 10:34:47 GMT  
		Size: 2.0 MB (2008550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0254e16c47bdde3eb7e8d57383df36625fad7398861b5aca562e447505806a8`  
		Last Modified: Tue, 04 Nov 2025 10:34:47 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; 386

```console
$ docker pull memcached@sha256:e950b4f76df4b7ad0e9dcc9f2357df6ae35314e232ad23b0ec4fb3c3beb2b84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33688177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9910abbdac4661a59a1d8fe6b43f96cd0abdde92371f8c995e7216d706f375bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:19:48 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 01:19:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:22:46 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 01:22:46 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 01:22:46 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 01:22:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 01:22:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:22:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 01:22:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:22:46 GMT
USER memcache
# Tue, 04 Nov 2025 01:22:46 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 01:22:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7f24a3a0c200106d0d9ab7b6264e50c689910154fb57bf08185b9eaf995db758`  
		Last Modified: Tue, 04 Nov 2025 00:13:54 GMT  
		Size: 31.3 MB (31294783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6840654bcf5429c7954c0483368ccd033e4222b3098ca64904c590f04dd07624`  
		Last Modified: Tue, 04 Nov 2025 01:22:59 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66205a10db2dcede178afb15530db6f282ec7194f11ffe734d9496d8b30e35a2`  
		Last Modified: Tue, 04 Nov 2025 01:22:59 GMT  
		Size: 147.4 KB (147440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b63b70a9c43a2f37c5f37f50e2aaf507c970f0133b7aaaea29fdb4e826c18b1`  
		Last Modified: Tue, 04 Nov 2025 01:23:00 GMT  
		Size: 2.2 MB (2244441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a3c1d29eba0037255cb4c7903d5de630770804520cfdb28ce05b112d526ed3`  
		Last Modified: Tue, 04 Nov 2025 01:22:59 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8da84bbfbc97884490625408deb986e43d5843e48291516064a41ab6d5963e`  
		Last Modified: Tue, 04 Nov 2025 01:22:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:51b41d632670fe8c786707c7977f9136c593c137bcde08516527421769778ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7473e22367c8e8c736bb1ce76169b1b4abf93fa0b057dec9103c4dccf90efc2`

```dockerfile
```

-	Layers:
	-	`sha256:f90631de8235b43d3b44250b8606b5783cd39dc12e9810fb5993f82a19dfe2ee`  
		Last Modified: Tue, 04 Nov 2025 10:34:51 GMT  
		Size: 2.0 MB (2005391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29d51086244a15fe10ebfe78e299fc7a89dd09601c8753741004d27949898c16`  
		Last Modified: Tue, 04 Nov 2025 10:34:52 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:ead041ea0e5c06d481ac304f7b4076a3339d849fcdffa3d25603418dc2fe82e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36187425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b0128aff763178ac8bb867e486c2450bacad45f79a5ff629194be435141070`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:52:27 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 01:52:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:55:40 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 01:55:40 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 01:55:40 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 01:55:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 01:55:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:55:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 01:55:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:55:41 GMT
USER memcache
# Tue, 04 Nov 2025 01:55:41 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 01:55:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126ce0c080daa81edc8784c59f60350b32083b3201304709775cf554155f80af`  
		Last Modified: Tue, 04 Nov 2025 01:56:04 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4c9857fe1f3ded2ba6c29c2f9591c7f5b2bfc46517527fac13f4c2b539a9a4`  
		Last Modified: Tue, 04 Nov 2025 01:56:04 GMT  
		Size: 170.2 KB (170244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e15beeee778428c51e89d0b8c3d6ca7931f0324e0a66f6b2bf85b101e9674a`  
		Last Modified: Tue, 04 Nov 2025 01:56:04 GMT  
		Size: 2.4 MB (2417022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d427e3c140105cfdb1a22a00010621a5a0834ce00ba3ea1059f8a63d8b0f5ee5`  
		Last Modified: Tue, 04 Nov 2025 01:56:04 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dfc7efa96996e95dcf030731f854bc07f2c7aa3349e75c4e74c04d924b3c62`  
		Last Modified: Tue, 04 Nov 2025 01:56:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:ad9b48a87b820bbf6c20cb57cd2247fa75ca6de00df26576f784a8f51703c571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1582395261fcee60bb7362c6cff0abd1d7325b4fde3cd609ac637f76aaa7ea5`

```dockerfile
```

-	Layers:
	-	`sha256:f5e9fbdfb8deeebb9142cd4facdedb0629028f8343a64b1e13d26ecb035f3c84`  
		Last Modified: Tue, 04 Nov 2025 10:34:55 GMT  
		Size: 2.0 MB (2011835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3dd30af34832aa3d277b4b6882a9786e4225d5a7387d5af5a66cadc59adc22d`  
		Last Modified: Tue, 04 Nov 2025 10:34:56 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:56542c7304b39c7980a644419d2ab6f603477cc9e1cb9c575d45b8c4220e0c6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30630140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e279bc62f41c4006902271742290cdde9d77c2121c1b4db697d09d01c690860e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 03:30:39 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 03:31:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:44:44 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 03:44:44 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 03:44:44 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 03:44:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 03:44:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 03:44:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 03:44:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 03:44:45 GMT
USER memcache
# Tue, 04 Nov 2025 03:44:45 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 03:44:45 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b836efb62045adb472c559fe0a4cedfe183f60ae9e36defd9b46efc4886fff56`  
		Last Modified: Tue, 04 Nov 2025 03:45:39 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db437579ba55d9291ad05cd904e857adb520e8189f0cc2fb207b475c10a95ee`  
		Last Modified: Tue, 04 Nov 2025 03:45:39 GMT  
		Size: 133.0 KB (132994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ca1f664c3ee469c225e4241d90dabf5a36c9fd5282ec51011fe16b9fcd5882`  
		Last Modified: Tue, 04 Nov 2025 03:45:39 GMT  
		Size: 2.2 MB (2219849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f5b56363e737d5d4b276274dc82b3ae7d3772bb1d6cadc5fb0c117ad6d004e`  
		Last Modified: Tue, 04 Nov 2025 03:45:39 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92139c3e4198e9ce61d77b8a86d621938a3390898a4ac22ba81eefd286a78cc7`  
		Last Modified: Tue, 04 Nov 2025 03:45:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:a72757dfcc56cb3edf581d72aa35ca18e099d18284ccfaabc697a74b2d7c2399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40a19d13356829e752dd3f0c530a1f2ef0abfc0ca53d29d3d74e1840a1698892`

```dockerfile
```

-	Layers:
	-	`sha256:78add421d4e1ac7755ca522075904f0acd06a15e1c8b9ca1bb0047a7d3ebf187`  
		Last Modified: Tue, 04 Nov 2025 07:34:38 GMT  
		Size: 2.0 MB (2002198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f1fc3731e375af1e0712ec91b83487acb49e907a1168f593f251fe43cb51fb9`  
		Last Modified: Tue, 04 Nov 2025 07:34:39 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:3de73b4ecf32984b0c6603b973257071c81c94af8351b35aa4343407c7315726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32293163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e6900a4460f82b0703aed07dde3c1722bdb7919a582b6b1f22a9ca701cb510f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 06:58:32 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 06:58:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 07:02:23 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 07:02:23 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 07:02:23 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 07:02:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 07:02:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 07:02:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 07:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 07:02:23 GMT
USER memcache
# Tue, 04 Nov 2025 07:02:23 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 07:02:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17527924bc8c8387e810ff986ddbe9998a0b5d55a4850b90b4cea0a897c94a09`  
		Last Modified: Tue, 04 Nov 2025 07:02:40 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54fd3d90bab9e973d6a8c142df91794bdc213e5bafe8926a58809036e1ee1f5`  
		Last Modified: Tue, 04 Nov 2025 07:02:40 GMT  
		Size: 140.4 KB (140429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc993f31fbd52e75a8dfc710d94d4130a8c228be35b7737c5950a5f93a1125a`  
		Last Modified: Tue, 04 Nov 2025 07:02:40 GMT  
		Size: 2.3 MB (2313833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acaa055d548771aab19234adcaf5b3ed727ee85214c303e1035e3e464e0fbda0`  
		Last Modified: Tue, 04 Nov 2025 07:02:40 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c2e1b3aad04d0544265917caef9c91d5ed4496376262541974a707026847f4`  
		Last Modified: Tue, 04 Nov 2025 07:02:40 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:414b070c237a13d5dee83e1db26eb0f953dd5af0753013a8bbd988611aa90e89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5cc4920f789bfe656195ac67c3ddd1a00030591f92b5ac4dc2b0e9dcdd2a0b`

```dockerfile
```

-	Layers:
	-	`sha256:b242fd5db27262af27c5589b736a5ae9f234cb03765c59c73e64818c1cade0c8`  
		Last Modified: Tue, 04 Nov 2025 10:35:02 GMT  
		Size: 2.0 MB (2009671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e15d059f16d47b54c3d82bdf997670c62a062815b64d7e7b486d8de0060691b4`  
		Last Modified: Tue, 04 Nov 2025 10:35:03 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6`

```console
$ docker pull memcached@sha256:050de63e6c082df85f93ffed9c388004b3c6257a06f1904e8628a6f87658eb99
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
$ docker pull memcached@sha256:04cfb7a52848a5ddab7b57674b37c9b7b392d93ec11f0c9a4c300a9bbd1c19a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32209888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0b3dcfe086b67312e8b165a92d8e71b517bf64b356c0c804270d2330e2577c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:05:54 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 04:05:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:08:37 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 04:08:37 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 04:08:37 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 04:08:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 04:08:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:08:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 04:08:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 04:08:38 GMT
USER memcache
# Tue, 04 Nov 2025 04:08:38 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 04:08:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95dd2497c5fb854f1d1cb6790613048eae391c70dd7fe1d2c54ea024889782ad`  
		Last Modified: Tue, 04 Nov 2025 04:08:50 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5e80885bbbbd2ccaf87a97c9f6da9eb3a9b7395ce5e2b73a110224cfbcfb1e`  
		Last Modified: Tue, 04 Nov 2025 04:08:50 GMT  
		Size: 136.6 KB (136597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be7e82464812bb6ab2d37c74a6636ec8d73ec4154a192a75342dfa2f64cc8da`  
		Last Modified: Tue, 04 Nov 2025 04:08:50 GMT  
		Size: 2.3 MB (2293674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18ba826b4b67fa295ff82d2b102a5f2db243fabcb7cc2acac6cc3c33a1cbf4a`  
		Last Modified: Tue, 04 Nov 2025 04:08:50 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654bd5f6e9c2c18716bbdc27ac8f5eab96044427da57f1cb8ee268d2cd3b5f03`  
		Last Modified: Tue, 04 Nov 2025 04:08:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:b78568d9b4a4cd24bae6187909a2a4a808abc29638602ee6aac1885173203e35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b08f68a528f6821adc34258cb89e510c9bf97f5596cf2e47ce7b30ba202cea`

```dockerfile
```

-	Layers:
	-	`sha256:549c9101b19d3697bed0386c9c6378a334bce6d392f694130d47f2033273b571`  
		Last Modified: Tue, 04 Nov 2025 10:34:35 GMT  
		Size: 2.0 MB (2008234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26c87354a983796083082c9e84ccf372217e5a602e78aefdec01fc26eae125ce`  
		Last Modified: Tue, 04 Nov 2025 10:34:36 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:cfd8f3dc480855d184b335ea9b7c334731ce495de10ef2f2f17b4f82bedf1965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30319386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4fa3d1c819bb913d28b672eedf487f5165ff2dc4e5968326e550efb418196ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 00:24:40 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 00:24:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:28:01 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 00:28:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 00:28:01 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 00:28:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 00:28:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:28:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 00:28:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:28:01 GMT
USER memcache
# Tue, 04 Nov 2025 00:28:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 00:28:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:453afc2258d7bc5729fed5672fb95bafa092e30a933b4377a12034be940a671b`  
		Last Modified: Tue, 04 Nov 2025 00:13:12 GMT  
		Size: 27.9 MB (27946438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3da1461ffd1574069e2ddea407a8d31a9f215a260352498c03bb19d38c7d7ca`  
		Last Modified: Tue, 04 Nov 2025 00:28:13 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4066eb4ba0932fcecba129384e7059abaee0e303654cc15d444f8c6aa11e69bf`  
		Last Modified: Tue, 04 Nov 2025 00:28:13 GMT  
		Size: 144.0 KB (144040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f429e8aa4399dcb073c93dceeb4c04af1a46da5d750c71a36dcff1a94ab840`  
		Last Modified: Tue, 04 Nov 2025 00:28:13 GMT  
		Size: 2.2 MB (2227397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100f4b89d2a8997d39ef62d45e5590e944f3120ba301e303025c7ccaac6da369`  
		Last Modified: Tue, 04 Nov 2025 00:28:13 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334cb0302a41a8c70f7874d7de08c32eb550581a5fc8b17c9b565b9cecdb8149`  
		Last Modified: Tue, 04 Nov 2025 00:28:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:281d772292417096430072e287dae06f36229ebd35a2c308d81eccc1862e99bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956875d70010cc91e002ae89b4a07ce9edfc12bc2a743b377162df7dd92e6f05`

```dockerfile
```

-	Layers:
	-	`sha256:c19709d33e93cfcba6b59a36ac6efba06597c00114be0ab5c2aaddf33ee8ba33`  
		Last Modified: Tue, 04 Nov 2025 07:34:24 GMT  
		Size: 2.0 MB (2011237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a60d569262f9d2f585a47be2ccf35c498002df82c55fd19ebcbaea6f9cd101f9`  
		Last Modified: Tue, 04 Nov 2025 07:34:25 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v7

```console
$ docker pull memcached@sha256:fb4a02a784ff9c44adb4a72aa161b935ed3bd148e49b37fc5e68a1f3aa30a87d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28532441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e70b324b1a195c841f52ba1facea8f75482e1bb049f38d17f8a8b69185f65166`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:06:51 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 02:06:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:09:59 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 02:09:59 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 02:09:59 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 02:09:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 02:09:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 02:09:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 02:09:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 02:09:59 GMT
USER memcache
# Tue, 04 Nov 2025 02:09:59 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 02:09:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f9bebc6d7be8fb19e90bd816cf5ea46e325d9d8d019345bd7e83bb27165e1c`  
		Last Modified: Tue, 04 Nov 2025 02:10:11 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d87b4f74b7b681280e1de65d55c7fef9af3294203ca9753541c48a7dbd67ac`  
		Last Modified: Tue, 04 Nov 2025 02:10:11 GMT  
		Size: 135.3 KB (135301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012aaeffd16b06fc90dbc9cf1682d2a8cb96482af9e0582ebc1dc6881617ba3d`  
		Last Modified: Tue, 04 Nov 2025 02:10:11 GMT  
		Size: 2.2 MB (2182590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30071a0aa370d64f866b34ab3ab9ed0d6e2f30dee5e631bc9b787ff5a9f4fdc0`  
		Last Modified: Tue, 04 Nov 2025 02:10:11 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18d6989abdf4813c6c982f04f7bc42405ebe217f82671824a3bd75a1f923f9c`  
		Last Modified: Tue, 04 Nov 2025 02:10:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:672ae9e81bd13a12a5ae6790d4619294b51a1cfd04a6af50c523797512fc75f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95641a91a03ab503b7750055d3fe6cf1474b1c75ce6288b8966a514375dddb1a`

```dockerfile
```

-	Layers:
	-	`sha256:f13ec9279ccf6461d334439358fdee3b542d225588c6a3857991636d57ce10ee`  
		Last Modified: Tue, 04 Nov 2025 10:34:42 GMT  
		Size: 2.0 MB (2009694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37374c73a31babc67e99ab9936b2166b55c09c55f1bc4cfff80e65a3c40d5425`  
		Last Modified: Tue, 04 Nov 2025 10:34:43 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:bc5ac38c2657d7c6d375374985e9293fb3744a75edbd96cb7a7524cc14c95d08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32572446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1f397ae776296a0fd6edeebc664c5cc9fbc3f08556289a5a1fe41c75626d379`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:17:41 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 01:17:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:20:41 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 01:20:41 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 01:20:41 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 01:20:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 01:20:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:20:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 01:20:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:20:41 GMT
USER memcache
# Tue, 04 Nov 2025 01:20:41 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 01:20:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db64d9b58942143a8d96f7823245feb1d4bf27c04222e71dbe7cedfce33d7e7f`  
		Last Modified: Tue, 04 Nov 2025 01:20:54 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e45c84ea5c10a0167bca67aede44a66fd08b708143ccb896170e30885ea50f1`  
		Last Modified: Tue, 04 Nov 2025 01:20:54 GMT  
		Size: 153.4 KB (153400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317fc2721e7de3ecc81d907c076c0de0aa0c4a80a7810a77e53335eab94adedc`  
		Last Modified: Tue, 04 Nov 2025 01:20:54 GMT  
		Size: 2.3 MB (2275238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a6f24d2569f3c38db7873c0a8f3942c5c7b876fa9eff4eaeca997bc6dc28df`  
		Last Modified: Tue, 04 Nov 2025 01:20:54 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d9e0c677fc63b66e178f9171abc553450378c9046b77cbcc52126068101766c`  
		Last Modified: Tue, 04 Nov 2025 01:20:54 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:8d2e6520d11120bd0b01076b34657bd1b1a785b38c6f7048bc58db91821f584f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97a00b54cc845295e717a2bf8ba5f7b91d5fb25acd85c6c399b94596dd67465`

```dockerfile
```

-	Layers:
	-	`sha256:7061efa09aee437d8b815835ea3f0afa471b9f76cb95323b8260dc846c1f49f1`  
		Last Modified: Tue, 04 Nov 2025 10:34:47 GMT  
		Size: 2.0 MB (2008550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0254e16c47bdde3eb7e8d57383df36625fad7398861b5aca562e447505806a8`  
		Last Modified: Tue, 04 Nov 2025 10:34:47 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; 386

```console
$ docker pull memcached@sha256:e950b4f76df4b7ad0e9dcc9f2357df6ae35314e232ad23b0ec4fb3c3beb2b84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33688177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9910abbdac4661a59a1d8fe6b43f96cd0abdde92371f8c995e7216d706f375bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:19:48 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 01:19:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:22:46 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 01:22:46 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 01:22:46 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 01:22:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 01:22:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:22:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 01:22:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:22:46 GMT
USER memcache
# Tue, 04 Nov 2025 01:22:46 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 01:22:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7f24a3a0c200106d0d9ab7b6264e50c689910154fb57bf08185b9eaf995db758`  
		Last Modified: Tue, 04 Nov 2025 00:13:54 GMT  
		Size: 31.3 MB (31294783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6840654bcf5429c7954c0483368ccd033e4222b3098ca64904c590f04dd07624`  
		Last Modified: Tue, 04 Nov 2025 01:22:59 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66205a10db2dcede178afb15530db6f282ec7194f11ffe734d9496d8b30e35a2`  
		Last Modified: Tue, 04 Nov 2025 01:22:59 GMT  
		Size: 147.4 KB (147440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b63b70a9c43a2f37c5f37f50e2aaf507c970f0133b7aaaea29fdb4e826c18b1`  
		Last Modified: Tue, 04 Nov 2025 01:23:00 GMT  
		Size: 2.2 MB (2244441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a3c1d29eba0037255cb4c7903d5de630770804520cfdb28ce05b112d526ed3`  
		Last Modified: Tue, 04 Nov 2025 01:22:59 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8da84bbfbc97884490625408deb986e43d5843e48291516064a41ab6d5963e`  
		Last Modified: Tue, 04 Nov 2025 01:22:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:51b41d632670fe8c786707c7977f9136c593c137bcde08516527421769778ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7473e22367c8e8c736bb1ce76169b1b4abf93fa0b057dec9103c4dccf90efc2`

```dockerfile
```

-	Layers:
	-	`sha256:f90631de8235b43d3b44250b8606b5783cd39dc12e9810fb5993f82a19dfe2ee`  
		Last Modified: Tue, 04 Nov 2025 10:34:51 GMT  
		Size: 2.0 MB (2005391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29d51086244a15fe10ebfe78e299fc7a89dd09601c8753741004d27949898c16`  
		Last Modified: Tue, 04 Nov 2025 10:34:52 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:ead041ea0e5c06d481ac304f7b4076a3339d849fcdffa3d25603418dc2fe82e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36187425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b0128aff763178ac8bb867e486c2450bacad45f79a5ff629194be435141070`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:52:27 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 01:52:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:55:40 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 01:55:40 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 01:55:40 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 01:55:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 01:55:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:55:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 01:55:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:55:41 GMT
USER memcache
# Tue, 04 Nov 2025 01:55:41 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 01:55:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126ce0c080daa81edc8784c59f60350b32083b3201304709775cf554155f80af`  
		Last Modified: Tue, 04 Nov 2025 01:56:04 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4c9857fe1f3ded2ba6c29c2f9591c7f5b2bfc46517527fac13f4c2b539a9a4`  
		Last Modified: Tue, 04 Nov 2025 01:56:04 GMT  
		Size: 170.2 KB (170244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e15beeee778428c51e89d0b8c3d6ca7931f0324e0a66f6b2bf85b101e9674a`  
		Last Modified: Tue, 04 Nov 2025 01:56:04 GMT  
		Size: 2.4 MB (2417022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d427e3c140105cfdb1a22a00010621a5a0834ce00ba3ea1059f8a63d8b0f5ee5`  
		Last Modified: Tue, 04 Nov 2025 01:56:04 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dfc7efa96996e95dcf030731f854bc07f2c7aa3349e75c4e74c04d924b3c62`  
		Last Modified: Tue, 04 Nov 2025 01:56:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:ad9b48a87b820bbf6c20cb57cd2247fa75ca6de00df26576f784a8f51703c571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1582395261fcee60bb7362c6cff0abd1d7325b4fde3cd609ac637f76aaa7ea5`

```dockerfile
```

-	Layers:
	-	`sha256:f5e9fbdfb8deeebb9142cd4facdedb0629028f8343a64b1e13d26ecb035f3c84`  
		Last Modified: Tue, 04 Nov 2025 10:34:55 GMT  
		Size: 2.0 MB (2011835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3dd30af34832aa3d277b4b6882a9786e4225d5a7387d5af5a66cadc59adc22d`  
		Last Modified: Tue, 04 Nov 2025 10:34:56 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; riscv64

```console
$ docker pull memcached@sha256:56542c7304b39c7980a644419d2ab6f603477cc9e1cb9c575d45b8c4220e0c6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30630140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e279bc62f41c4006902271742290cdde9d77c2121c1b4db697d09d01c690860e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 03:30:39 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 03:31:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:44:44 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 03:44:44 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 03:44:44 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 03:44:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 03:44:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 03:44:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 03:44:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 03:44:45 GMT
USER memcache
# Tue, 04 Nov 2025 03:44:45 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 03:44:45 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b836efb62045adb472c559fe0a4cedfe183f60ae9e36defd9b46efc4886fff56`  
		Last Modified: Tue, 04 Nov 2025 03:45:39 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db437579ba55d9291ad05cd904e857adb520e8189f0cc2fb207b475c10a95ee`  
		Last Modified: Tue, 04 Nov 2025 03:45:39 GMT  
		Size: 133.0 KB (132994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ca1f664c3ee469c225e4241d90dabf5a36c9fd5282ec51011fe16b9fcd5882`  
		Last Modified: Tue, 04 Nov 2025 03:45:39 GMT  
		Size: 2.2 MB (2219849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f5b56363e737d5d4b276274dc82b3ae7d3772bb1d6cadc5fb0c117ad6d004e`  
		Last Modified: Tue, 04 Nov 2025 03:45:39 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92139c3e4198e9ce61d77b8a86d621938a3390898a4ac22ba81eefd286a78cc7`  
		Last Modified: Tue, 04 Nov 2025 03:45:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:a72757dfcc56cb3edf581d72aa35ca18e099d18284ccfaabc697a74b2d7c2399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40a19d13356829e752dd3f0c530a1f2ef0abfc0ca53d29d3d74e1840a1698892`

```dockerfile
```

-	Layers:
	-	`sha256:78add421d4e1ac7755ca522075904f0acd06a15e1c8b9ca1bb0047a7d3ebf187`  
		Last Modified: Tue, 04 Nov 2025 07:34:38 GMT  
		Size: 2.0 MB (2002198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f1fc3731e375af1e0712ec91b83487acb49e907a1168f593f251fe43cb51fb9`  
		Last Modified: Tue, 04 Nov 2025 07:34:39 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; s390x

```console
$ docker pull memcached@sha256:3de73b4ecf32984b0c6603b973257071c81c94af8351b35aa4343407c7315726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32293163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e6900a4460f82b0703aed07dde3c1722bdb7919a582b6b1f22a9ca701cb510f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 06:58:32 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 06:58:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 07:02:23 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 07:02:23 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 07:02:23 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 07:02:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 07:02:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 07:02:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 07:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 07:02:23 GMT
USER memcache
# Tue, 04 Nov 2025 07:02:23 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 07:02:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17527924bc8c8387e810ff986ddbe9998a0b5d55a4850b90b4cea0a897c94a09`  
		Last Modified: Tue, 04 Nov 2025 07:02:40 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54fd3d90bab9e973d6a8c142df91794bdc213e5bafe8926a58809036e1ee1f5`  
		Last Modified: Tue, 04 Nov 2025 07:02:40 GMT  
		Size: 140.4 KB (140429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc993f31fbd52e75a8dfc710d94d4130a8c228be35b7737c5950a5f93a1125a`  
		Last Modified: Tue, 04 Nov 2025 07:02:40 GMT  
		Size: 2.3 MB (2313833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acaa055d548771aab19234adcaf5b3ed727ee85214c303e1035e3e464e0fbda0`  
		Last Modified: Tue, 04 Nov 2025 07:02:40 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c2e1b3aad04d0544265917caef9c91d5ed4496376262541974a707026847f4`  
		Last Modified: Tue, 04 Nov 2025 07:02:40 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:414b070c237a13d5dee83e1db26eb0f953dd5af0753013a8bbd988611aa90e89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5cc4920f789bfe656195ac67c3ddd1a00030591f92b5ac4dc2b0e9dcdd2a0b`

```dockerfile
```

-	Layers:
	-	`sha256:b242fd5db27262af27c5589b736a5ae9f234cb03765c59c73e64818c1cade0c8`  
		Last Modified: Tue, 04 Nov 2025 10:35:02 GMT  
		Size: 2.0 MB (2009671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e15d059f16d47b54c3d82bdf997670c62a062815b64d7e7b486d8de0060691b4`  
		Last Modified: Tue, 04 Nov 2025 10:35:03 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine`

```console
$ docker pull memcached@sha256:7b45203a99eb1419c95b875c7e48c5a9eebc0a305eeb09eefc9f3a2cff758a46
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
$ docker pull memcached@sha256:e319c3f1f6623fb2caedb14c4a5c8594f88736d90dc89d19f1ec11c8533ee263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70bce40b6c41c7484f47d1d51e8be171c582e0b3e18f2379dd66e49e3178d86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c711f2e2fe464121135109729faa513b79413712df200207ef35dfb19e550ca`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0cba00095a1ab15ee2ec0bcefea9c1fe601b9533d47626ab2fb6b74bf8a770`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 104.7 KB (104727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9204d372b3172134a4f3bbcf654ab17d33079a3aff6930e16fa7262df7c9cdbe`  
		Last Modified: Wed, 08 Oct 2025 22:42:05 GMT  
		Size: 2.0 MB (2000281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa9dd6a61433e778f70df6cd37bc70c4dcbfa8e0b0e8b1f9a0fc2f993c78685`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5a283c3ec8e0142f3f4b0b17b2901ab6d7dbff9e3f62bf978a03e5d31833f5`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:1cb56f4b692737cc136d1ff3c5dc0ca16e6b7c3be7023b1a9214348578dc4536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 KB (116754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a7a80cd482b54ecad43450e81b2d6858d2397277cf2d8358315295ef8152dc5`

```dockerfile
```

-	Layers:
	-	`sha256:659cc6afa1cde9acfc6444a310575d263f25f2f83d4987d4fddf83e5bb0d3082`  
		Last Modified: Thu, 09 Oct 2025 00:34:37 GMT  
		Size: 96.2 KB (96180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e43c8201b9a29cba2a3392f6a10e9ee6f0d6295f0248c8d3e9a792871224ec10`  
		Last Modified: Thu, 09 Oct 2025 00:34:38 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:43072fb4c4cfd652bf1a32d617dd81060515017e52b14f35faeb2fe26d071dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5557528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87416926a00e28eb0313c62e942bea0ce0517d67c95df6258358f109a49d392c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd90c0f65a0d79d1685d8fefb0f95b02afd962d0b160a1274598cb584ec37d9`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920bb020947e8d1d3b077c6d9861f8953febeb54f94421c689d40240e56b7ff0`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 101.5 KB (101532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4dc3dc5cf827d37f28e2a9a6758089ff72bc10d1915dbb61cce8f30350de40`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 2.0 MB (1950567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b2afb9c93ba0497cadc25e69b15de772b64456929b70dbe23c7ef54faa3815`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d88088c7b652b283feabfeb2974fb4bd7140ebf7da94c5d502f22841f26eb4a`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:bd27295997fc0e77ad410a3e638c230d83e3d366906a449f5349d8311d72e657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a474656b8df51a30dcb397a44bcb48c6ba3cb76e49cc3a108a15a662cd64c4b`

```dockerfile
```

-	Layers:
	-	`sha256:9a80e6fbb7fc2254a12359760da6745c28fe1d3fa2367b1137aad71c6732a8bd`  
		Last Modified: Thu, 09 Oct 2025 00:34:41 GMT  
		Size: 20.5 KB (20510 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:2caa01f7607cf1d95b2e261de80716a27de4077bf25b9dc623688091b78bf4ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c1be64fe03e8832bc6208dfced118762e57dca6b55b4482140c8fc3b06dfb3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0a02f5bd6bf63e96f5b45eda4849003b01c41b23425e7ac5a77eb01b5391e0`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f277f740301c69a561a94545bc7f140ee2d5f4ea87f88c0c861eb7b4f7983b0`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 91.3 KB (91313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e9ebffe0c4c57cd5b7fd1da1fcc7f14e2e881a81673f81e8bde4bf662a45b3`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 1.9 MB (1909853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46526f6db8416530677567eac97b5cfc18e2b86ec5c930d06de26b62f0c7a5c6`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f19627fe74f6edf1d0aa4deb85d035125067fcd28b2ee240aeb110e48330f19`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:09108dd858c6aae1c834fd9c8a7f9f78e552673ee6296d9f5cf2d84c0c26c6fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 KB (116969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9755e3f89f06272910c7fcbcaf44a3cb373b551f73bc7c9dc6dbffe13aad48`

```dockerfile
```

-	Layers:
	-	`sha256:13ba800aa65c8f207645e4069de55b11ad0a2dc87b951414df4bd35ad3923afd`  
		Last Modified: Thu, 09 Oct 2025 00:34:45 GMT  
		Size: 96.2 KB (96248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:636139066de216a683805bafa6cd72b23f1754f8dd2b5854e61578a684260418`  
		Last Modified: Thu, 09 Oct 2025 00:34:46 GMT  
		Size: 20.7 KB (20721 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:03d8054231ea1bb1dbb54d7e8bb32449b95c35475fa280a9b12d78219822fa48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6251299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42028500064e9ca7d32291ca01c636547943d3a6e6f11b80e503166efcfa6149`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098f75f9dd9f7dbf0e5993587a5b4de796bc9c01f2e795b325f1e22fe66c6833`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4c130fe47b24dbff1989543c440e0d6635524f9bf84473a6dc37472ecacac0`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 120.8 KB (120823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a41614e1c7aff72360936c76c0218330a487dd6ff6779cd243ad1c60ab6634`  
		Last Modified: Wed, 08 Oct 2025 21:31:15 GMT  
		Size: 2.0 MB (1991055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8573d5df234537883a638f95501925286c3367fd1cc40a4c6a80b70ef59ffa16`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd6f77485828d14a277cde4d3649153b058047ad8477c919e974016eb3ef6f7`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b47c7c82754dea9552416b18a213b43d6824105eb9a0318e31789b64ebb4524a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 KB (117055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc0f98e226622d3dd6ab1b57679deaa27c10decc2a26c0d7c64feeeae3b6e18`

```dockerfile
```

-	Layers:
	-	`sha256:949b28585bcee0143420765476ff3f8231f4f8049c4d0b3136c102cc9a3b272f`  
		Last Modified: Thu, 09 Oct 2025 00:34:49 GMT  
		Size: 96.3 KB (96284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c10e36727f7634ae28cb6de04bff91b38d77420fce24cf9b31503d14aff0636`  
		Last Modified: Thu, 09 Oct 2025 00:34:50 GMT  
		Size: 20.8 KB (20771 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:3dbd66df3fa527ea9d5ef8e15484f90fd2bc4445e9d21ad40602c7d954a57c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5692091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa2b9eb15af4ed95101c0752bbde283e07e28adfed081d3a9a731aa82d1ab68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5efc90d716eb56816bbbf625c914fe13450e5c8059469e05eaef18ddf200fd`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795865ca1e6e3ac4e3ed32dabe363301a453512615868e180c6c23f28f711154`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 109.5 KB (109526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f93c274afbe9d7756256b49ac152cdbd8b21b7bf4c0e1a564bf36c6940e986e`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 2.0 MB (1962279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8db2caca7c819c90101fe1d4c62396dd78bf9677be35f005e0026d6b76c095`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d53143d130829def781c84b33cfc19fa4ac216deae7acd8c510186dd525afdb`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c7b1229c17eb2270b6a966423e63e1ad70b16a7c79c87d2ea9df82f9d733d383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 KB (116649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392076445efbd53c3eea2f14c49336ed1c8f521c209369edbb2e7686671c310a`

```dockerfile
```

-	Layers:
	-	`sha256:e91e563cbe752ee16efaa2007b7b0f49392b0f5326018a94f34a2e187c1cb743`  
		Last Modified: Wed, 08 Oct 2025 21:34:33 GMT  
		Size: 96.1 KB (96135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:207733714725a312d472d7f8657279033f48a213756c3f87714f3b4bd3e03195`  
		Last Modified: Wed, 08 Oct 2025 21:34:34 GMT  
		Size: 20.5 KB (20514 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:7e2b422eba145439e8c30b7e3191cc1f8498a721f4ca3d90c31fbc5ed80aee7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5951257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48257955bab73ec394b46e2350210da8ec488c125ff0c7cb4ce03893fff291d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8caf4ead4d89e7cb932248ec2c3e7ae5ee7efb8989eb2ab51d407f7094fe6bf`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff948909dcd7ac6c4301b934b30465617e899ca99e5cb6ac6e537be4e6f6144`  
		Last Modified: Thu, 09 Oct 2025 01:11:40 GMT  
		Size: 124.3 KB (124318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f700c3c0f9d01825484f8ddf4ea689855d4c1ed78848558c4c2bf8bf817caed0`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 2.1 MB (2093342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ee4b65e8fe80e2ad3919c8c15d8855829430a43445decbd73237095a9771a9`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06240440b6e443402b0a5ca4dc97a2225661f3da03b4c6bc67c2e9443ba95ce4`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ea61cc67a9e9ffc7a8aaf326e701ea53f5d074dc907d4ad89b4274c4cb8ce804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213afd703e8e97590346c2a301a08bd84f590c17e18aefcbcdefc4d93622c57b`

```dockerfile
```

-	Layers:
	-	`sha256:d3b5325b8aa7c43ef1c7b6f6f4a09cbcfd07d64d439c41a950bc41da09e060ff`  
		Last Modified: Thu, 09 Oct 2025 03:34:33 GMT  
		Size: 94.3 KB (94287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dd52654f2c500e460030d1f9328acbf6d095a5e2d004a4f6417b79522c7fddf`  
		Last Modified: Thu, 09 Oct 2025 03:34:34 GMT  
		Size: 20.6 KB (20647 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:588117152fae8688e5cee8aa65963a1adb1e3851845da5da3e18c80099cdb1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5559076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c983e214f48d62c0be8ffbceb2a86b504aa71c02ac195047119fe264f612c35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ec1911f91425f5b1fc00d35f661d0dcb2691cdbff9a0ea4a65789eb8dd9b89`  
		Last Modified: Thu, 09 Oct 2025 04:54:06 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb577a02d7726836381f3dfcda7cb11472d8e99ef2feb088a9570bc2c0203f15`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 107.9 KB (107909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d6a77fdbd897c87616b71f12d107a1db186b3944ccdad6b89e33186d2645bf`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 1.9 MB (1934579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2879148828c59fde0e744fb56e2490c68a2e98902f3c6a0d01bb8381588a58ba`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00990bf09cdd6c9e756438f8b076739cea749be4889b317c88bf5d06c908e9d8`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:da1dc0b73e866df98aacb962264ed5b50bf3f61862f76c42828b9a179c32e455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b8b102978a5d01b2e4ec0cf55dd00df9776a17f5f31b8bae680908b73d2e1de`

```dockerfile
```

-	Layers:
	-	`sha256:2de1c9249a94130556f0db88a655ed432c15ad40e151579870de604725fbc086`  
		Last Modified: Thu, 09 Oct 2025 06:34:34 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0262f9b3a73d1455147e4436e4bf7da9aa19a7d385d28a807688e23d6a1f1d05`  
		Last Modified: Thu, 09 Oct 2025 06:34:34 GMT  
		Size: 20.6 KB (20648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:ed5969236f4728c97696471e08c88864c21019ea227118b3336d6484ed3e5b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5804524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c049e21de6c2be2f58a69ee9eb633a51a0491febb4b48fa476556586ac0fbd96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d91bfc8fa88993cee87c33ea18494c5e9f0ad8e5b6f644411e9cd648982653`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a682e0d523bab9ef58be0ad290abcee8563e45ceccc9d04fc9b47308aeb709b`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 113.5 KB (113502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9fe3585b1938fd376ffbce3ef824ed7bc20ed49039f98e279ff5ab6159b81e`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 2.0 MB (2040430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9870bcfd315f7fc77b2fb8e80646695f277bc2e7689cf73b395e230aa6fe327c`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20f8ef4bac131999b759bd8b49d1474c540fb1874c8db4e3f4b21a7262b6903`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2d42234a0a18e44870f34c7796f717e9d61b56556ba027f9fae085adfbeeb7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd89a980babfe6204633d40fbc2b82da6c42a3c42f43f980c4d29d3015fd40b`

```dockerfile
```

-	Layers:
	-	`sha256:70fb18f0cec1c9db308335dffc76a505d0855256e74dd6cd73079481cccac057`  
		Last Modified: Thu, 09 Oct 2025 03:34:39 GMT  
		Size: 94.2 KB (94229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02c95a382d7ff8c2fab05ba8609f8b69576ec785d085ed04e606445051336db9`  
		Last Modified: Thu, 09 Oct 2025 03:34:40 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine3.22`

```console
$ docker pull memcached@sha256:7b45203a99eb1419c95b875c7e48c5a9eebc0a305eeb09eefc9f3a2cff758a46
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
$ docker pull memcached@sha256:e319c3f1f6623fb2caedb14c4a5c8594f88736d90dc89d19f1ec11c8533ee263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70bce40b6c41c7484f47d1d51e8be171c582e0b3e18f2379dd66e49e3178d86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c711f2e2fe464121135109729faa513b79413712df200207ef35dfb19e550ca`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0cba00095a1ab15ee2ec0bcefea9c1fe601b9533d47626ab2fb6b74bf8a770`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 104.7 KB (104727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9204d372b3172134a4f3bbcf654ab17d33079a3aff6930e16fa7262df7c9cdbe`  
		Last Modified: Wed, 08 Oct 2025 22:42:05 GMT  
		Size: 2.0 MB (2000281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa9dd6a61433e778f70df6cd37bc70c4dcbfa8e0b0e8b1f9a0fc2f993c78685`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5a283c3ec8e0142f3f4b0b17b2901ab6d7dbff9e3f62bf978a03e5d31833f5`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:1cb56f4b692737cc136d1ff3c5dc0ca16e6b7c3be7023b1a9214348578dc4536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 KB (116754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a7a80cd482b54ecad43450e81b2d6858d2397277cf2d8358315295ef8152dc5`

```dockerfile
```

-	Layers:
	-	`sha256:659cc6afa1cde9acfc6444a310575d263f25f2f83d4987d4fddf83e5bb0d3082`  
		Last Modified: Thu, 09 Oct 2025 00:34:37 GMT  
		Size: 96.2 KB (96180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e43c8201b9a29cba2a3392f6a10e9ee6f0d6295f0248c8d3e9a792871224ec10`  
		Last Modified: Thu, 09 Oct 2025 00:34:38 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.22` - linux; arm variant v6

```console
$ docker pull memcached@sha256:43072fb4c4cfd652bf1a32d617dd81060515017e52b14f35faeb2fe26d071dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5557528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87416926a00e28eb0313c62e942bea0ce0517d67c95df6258358f109a49d392c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd90c0f65a0d79d1685d8fefb0f95b02afd962d0b160a1274598cb584ec37d9`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920bb020947e8d1d3b077c6d9861f8953febeb54f94421c689d40240e56b7ff0`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 101.5 KB (101532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4dc3dc5cf827d37f28e2a9a6758089ff72bc10d1915dbb61cce8f30350de40`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 2.0 MB (1950567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b2afb9c93ba0497cadc25e69b15de772b64456929b70dbe23c7ef54faa3815`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d88088c7b652b283feabfeb2974fb4bd7140ebf7da94c5d502f22841f26eb4a`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:bd27295997fc0e77ad410a3e638c230d83e3d366906a449f5349d8311d72e657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a474656b8df51a30dcb397a44bcb48c6ba3cb76e49cc3a108a15a662cd64c4b`

```dockerfile
```

-	Layers:
	-	`sha256:9a80e6fbb7fc2254a12359760da6745c28fe1d3fa2367b1137aad71c6732a8bd`  
		Last Modified: Thu, 09 Oct 2025 00:34:41 GMT  
		Size: 20.5 KB (20510 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.22` - linux; arm variant v7

```console
$ docker pull memcached@sha256:2caa01f7607cf1d95b2e261de80716a27de4077bf25b9dc623688091b78bf4ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c1be64fe03e8832bc6208dfced118762e57dca6b55b4482140c8fc3b06dfb3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0a02f5bd6bf63e96f5b45eda4849003b01c41b23425e7ac5a77eb01b5391e0`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f277f740301c69a561a94545bc7f140ee2d5f4ea87f88c0c861eb7b4f7983b0`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 91.3 KB (91313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e9ebffe0c4c57cd5b7fd1da1fcc7f14e2e881a81673f81e8bde4bf662a45b3`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 1.9 MB (1909853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46526f6db8416530677567eac97b5cfc18e2b86ec5c930d06de26b62f0c7a5c6`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f19627fe74f6edf1d0aa4deb85d035125067fcd28b2ee240aeb110e48330f19`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:09108dd858c6aae1c834fd9c8a7f9f78e552673ee6296d9f5cf2d84c0c26c6fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 KB (116969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9755e3f89f06272910c7fcbcaf44a3cb373b551f73bc7c9dc6dbffe13aad48`

```dockerfile
```

-	Layers:
	-	`sha256:13ba800aa65c8f207645e4069de55b11ad0a2dc87b951414df4bd35ad3923afd`  
		Last Modified: Thu, 09 Oct 2025 00:34:45 GMT  
		Size: 96.2 KB (96248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:636139066de216a683805bafa6cd72b23f1754f8dd2b5854e61578a684260418`  
		Last Modified: Thu, 09 Oct 2025 00:34:46 GMT  
		Size: 20.7 KB (20721 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:03d8054231ea1bb1dbb54d7e8bb32449b95c35475fa280a9b12d78219822fa48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6251299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42028500064e9ca7d32291ca01c636547943d3a6e6f11b80e503166efcfa6149`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098f75f9dd9f7dbf0e5993587a5b4de796bc9c01f2e795b325f1e22fe66c6833`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4c130fe47b24dbff1989543c440e0d6635524f9bf84473a6dc37472ecacac0`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 120.8 KB (120823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a41614e1c7aff72360936c76c0218330a487dd6ff6779cd243ad1c60ab6634`  
		Last Modified: Wed, 08 Oct 2025 21:31:15 GMT  
		Size: 2.0 MB (1991055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8573d5df234537883a638f95501925286c3367fd1cc40a4c6a80b70ef59ffa16`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd6f77485828d14a277cde4d3649153b058047ad8477c919e974016eb3ef6f7`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:b47c7c82754dea9552416b18a213b43d6824105eb9a0318e31789b64ebb4524a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 KB (117055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc0f98e226622d3dd6ab1b57679deaa27c10decc2a26c0d7c64feeeae3b6e18`

```dockerfile
```

-	Layers:
	-	`sha256:949b28585bcee0143420765476ff3f8231f4f8049c4d0b3136c102cc9a3b272f`  
		Last Modified: Thu, 09 Oct 2025 00:34:49 GMT  
		Size: 96.3 KB (96284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c10e36727f7634ae28cb6de04bff91b38d77420fce24cf9b31503d14aff0636`  
		Last Modified: Thu, 09 Oct 2025 00:34:50 GMT  
		Size: 20.8 KB (20771 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.22` - linux; 386

```console
$ docker pull memcached@sha256:3dbd66df3fa527ea9d5ef8e15484f90fd2bc4445e9d21ad40602c7d954a57c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5692091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa2b9eb15af4ed95101c0752bbde283e07e28adfed081d3a9a731aa82d1ab68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5efc90d716eb56816bbbf625c914fe13450e5c8059469e05eaef18ddf200fd`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795865ca1e6e3ac4e3ed32dabe363301a453512615868e180c6c23f28f711154`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 109.5 KB (109526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f93c274afbe9d7756256b49ac152cdbd8b21b7bf4c0e1a564bf36c6940e986e`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 2.0 MB (1962279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8db2caca7c819c90101fe1d4c62396dd78bf9677be35f005e0026d6b76c095`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d53143d130829def781c84b33cfc19fa4ac216deae7acd8c510186dd525afdb`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:c7b1229c17eb2270b6a966423e63e1ad70b16a7c79c87d2ea9df82f9d733d383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 KB (116649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392076445efbd53c3eea2f14c49336ed1c8f521c209369edbb2e7686671c310a`

```dockerfile
```

-	Layers:
	-	`sha256:e91e563cbe752ee16efaa2007b7b0f49392b0f5326018a94f34a2e187c1cb743`  
		Last Modified: Wed, 08 Oct 2025 21:34:33 GMT  
		Size: 96.1 KB (96135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:207733714725a312d472d7f8657279033f48a213756c3f87714f3b4bd3e03195`  
		Last Modified: Wed, 08 Oct 2025 21:34:34 GMT  
		Size: 20.5 KB (20514 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.22` - linux; ppc64le

```console
$ docker pull memcached@sha256:7e2b422eba145439e8c30b7e3191cc1f8498a721f4ca3d90c31fbc5ed80aee7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5951257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48257955bab73ec394b46e2350210da8ec488c125ff0c7cb4ce03893fff291d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8caf4ead4d89e7cb932248ec2c3e7ae5ee7efb8989eb2ab51d407f7094fe6bf`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff948909dcd7ac6c4301b934b30465617e899ca99e5cb6ac6e537be4e6f6144`  
		Last Modified: Thu, 09 Oct 2025 01:11:40 GMT  
		Size: 124.3 KB (124318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f700c3c0f9d01825484f8ddf4ea689855d4c1ed78848558c4c2bf8bf817caed0`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 2.1 MB (2093342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ee4b65e8fe80e2ad3919c8c15d8855829430a43445decbd73237095a9771a9`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06240440b6e443402b0a5ca4dc97a2225661f3da03b4c6bc67c2e9443ba95ce4`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:ea61cc67a9e9ffc7a8aaf326e701ea53f5d074dc907d4ad89b4274c4cb8ce804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213afd703e8e97590346c2a301a08bd84f590c17e18aefcbcdefc4d93622c57b`

```dockerfile
```

-	Layers:
	-	`sha256:d3b5325b8aa7c43ef1c7b6f6f4a09cbcfd07d64d439c41a950bc41da09e060ff`  
		Last Modified: Thu, 09 Oct 2025 03:34:33 GMT  
		Size: 94.3 KB (94287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dd52654f2c500e460030d1f9328acbf6d095a5e2d004a4f6417b79522c7fddf`  
		Last Modified: Thu, 09 Oct 2025 03:34:34 GMT  
		Size: 20.6 KB (20647 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.22` - linux; riscv64

```console
$ docker pull memcached@sha256:588117152fae8688e5cee8aa65963a1adb1e3851845da5da3e18c80099cdb1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5559076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c983e214f48d62c0be8ffbceb2a86b504aa71c02ac195047119fe264f612c35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ec1911f91425f5b1fc00d35f661d0dcb2691cdbff9a0ea4a65789eb8dd9b89`  
		Last Modified: Thu, 09 Oct 2025 04:54:06 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb577a02d7726836381f3dfcda7cb11472d8e99ef2feb088a9570bc2c0203f15`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 107.9 KB (107909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d6a77fdbd897c87616b71f12d107a1db186b3944ccdad6b89e33186d2645bf`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 1.9 MB (1934579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2879148828c59fde0e744fb56e2490c68a2e98902f3c6a0d01bb8381588a58ba`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00990bf09cdd6c9e756438f8b076739cea749be4889b317c88bf5d06c908e9d8`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:da1dc0b73e866df98aacb962264ed5b50bf3f61862f76c42828b9a179c32e455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b8b102978a5d01b2e4ec0cf55dd00df9776a17f5f31b8bae680908b73d2e1de`

```dockerfile
```

-	Layers:
	-	`sha256:2de1c9249a94130556f0db88a655ed432c15ad40e151579870de604725fbc086`  
		Last Modified: Thu, 09 Oct 2025 06:34:34 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0262f9b3a73d1455147e4436e4bf7da9aa19a7d385d28a807688e23d6a1f1d05`  
		Last Modified: Thu, 09 Oct 2025 06:34:34 GMT  
		Size: 20.6 KB (20648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.22` - linux; s390x

```console
$ docker pull memcached@sha256:ed5969236f4728c97696471e08c88864c21019ea227118b3336d6484ed3e5b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5804524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c049e21de6c2be2f58a69ee9eb633a51a0491febb4b48fa476556586ac0fbd96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d91bfc8fa88993cee87c33ea18494c5e9f0ad8e5b6f644411e9cd648982653`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a682e0d523bab9ef58be0ad290abcee8563e45ceccc9d04fc9b47308aeb709b`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 113.5 KB (113502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9fe3585b1938fd376ffbce3ef824ed7bc20ed49039f98e279ff5ab6159b81e`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 2.0 MB (2040430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9870bcfd315f7fc77b2fb8e80646695f277bc2e7689cf73b395e230aa6fe327c`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20f8ef4bac131999b759bd8b49d1474c540fb1874c8db4e3f4b21a7262b6903`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:2d42234a0a18e44870f34c7796f717e9d61b56556ba027f9fae085adfbeeb7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd89a980babfe6204633d40fbc2b82da6c42a3c42f43f980c4d29d3015fd40b`

```dockerfile
```

-	Layers:
	-	`sha256:70fb18f0cec1c9db308335dffc76a505d0855256e74dd6cd73079481cccac057`  
		Last Modified: Thu, 09 Oct 2025 03:34:39 GMT  
		Size: 94.2 KB (94229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02c95a382d7ff8c2fab05ba8609f8b69576ec785d085ed04e606445051336db9`  
		Last Modified: Thu, 09 Oct 2025 03:34:40 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-trixie`

```console
$ docker pull memcached@sha256:050de63e6c082df85f93ffed9c388004b3c6257a06f1904e8628a6f87658eb99
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
$ docker pull memcached@sha256:04cfb7a52848a5ddab7b57674b37c9b7b392d93ec11f0c9a4c300a9bbd1c19a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32209888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0b3dcfe086b67312e8b165a92d8e71b517bf64b356c0c804270d2330e2577c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:05:54 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 04:05:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:08:37 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 04:08:37 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 04:08:37 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 04:08:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 04:08:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:08:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 04:08:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 04:08:38 GMT
USER memcache
# Tue, 04 Nov 2025 04:08:38 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 04:08:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95dd2497c5fb854f1d1cb6790613048eae391c70dd7fe1d2c54ea024889782ad`  
		Last Modified: Tue, 04 Nov 2025 04:08:50 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5e80885bbbbd2ccaf87a97c9f6da9eb3a9b7395ce5e2b73a110224cfbcfb1e`  
		Last Modified: Tue, 04 Nov 2025 04:08:50 GMT  
		Size: 136.6 KB (136597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be7e82464812bb6ab2d37c74a6636ec8d73ec4154a192a75342dfa2f64cc8da`  
		Last Modified: Tue, 04 Nov 2025 04:08:50 GMT  
		Size: 2.3 MB (2293674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18ba826b4b67fa295ff82d2b102a5f2db243fabcb7cc2acac6cc3c33a1cbf4a`  
		Last Modified: Tue, 04 Nov 2025 04:08:50 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654bd5f6e9c2c18716bbdc27ac8f5eab96044427da57f1cb8ee268d2cd3b5f03`  
		Last Modified: Tue, 04 Nov 2025 04:08:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:b78568d9b4a4cd24bae6187909a2a4a808abc29638602ee6aac1885173203e35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b08f68a528f6821adc34258cb89e510c9bf97f5596cf2e47ce7b30ba202cea`

```dockerfile
```

-	Layers:
	-	`sha256:549c9101b19d3697bed0386c9c6378a334bce6d392f694130d47f2033273b571`  
		Last Modified: Tue, 04 Nov 2025 10:34:35 GMT  
		Size: 2.0 MB (2008234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26c87354a983796083082c9e84ccf372217e5a602e78aefdec01fc26eae125ce`  
		Last Modified: Tue, 04 Nov 2025 10:34:36 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:cfd8f3dc480855d184b335ea9b7c334731ce495de10ef2f2f17b4f82bedf1965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30319386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4fa3d1c819bb913d28b672eedf487f5165ff2dc4e5968326e550efb418196ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 00:24:40 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 00:24:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:28:01 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 00:28:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 00:28:01 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 00:28:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 00:28:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:28:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 00:28:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:28:01 GMT
USER memcache
# Tue, 04 Nov 2025 00:28:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 00:28:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:453afc2258d7bc5729fed5672fb95bafa092e30a933b4377a12034be940a671b`  
		Last Modified: Tue, 04 Nov 2025 00:13:12 GMT  
		Size: 27.9 MB (27946438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3da1461ffd1574069e2ddea407a8d31a9f215a260352498c03bb19d38c7d7ca`  
		Last Modified: Tue, 04 Nov 2025 00:28:13 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4066eb4ba0932fcecba129384e7059abaee0e303654cc15d444f8c6aa11e69bf`  
		Last Modified: Tue, 04 Nov 2025 00:28:13 GMT  
		Size: 144.0 KB (144040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f429e8aa4399dcb073c93dceeb4c04af1a46da5d750c71a36dcff1a94ab840`  
		Last Modified: Tue, 04 Nov 2025 00:28:13 GMT  
		Size: 2.2 MB (2227397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100f4b89d2a8997d39ef62d45e5590e944f3120ba301e303025c7ccaac6da369`  
		Last Modified: Tue, 04 Nov 2025 00:28:13 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334cb0302a41a8c70f7874d7de08c32eb550581a5fc8b17c9b565b9cecdb8149`  
		Last Modified: Tue, 04 Nov 2025 00:28:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:281d772292417096430072e287dae06f36229ebd35a2c308d81eccc1862e99bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956875d70010cc91e002ae89b4a07ce9edfc12bc2a743b377162df7dd92e6f05`

```dockerfile
```

-	Layers:
	-	`sha256:c19709d33e93cfcba6b59a36ac6efba06597c00114be0ab5c2aaddf33ee8ba33`  
		Last Modified: Tue, 04 Nov 2025 07:34:24 GMT  
		Size: 2.0 MB (2011237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a60d569262f9d2f585a47be2ccf35c498002df82c55fd19ebcbaea6f9cd101f9`  
		Last Modified: Tue, 04 Nov 2025 07:34:25 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:fb4a02a784ff9c44adb4a72aa161b935ed3bd148e49b37fc5e68a1f3aa30a87d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28532441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e70b324b1a195c841f52ba1facea8f75482e1bb049f38d17f8a8b69185f65166`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:06:51 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 02:06:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:09:59 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 02:09:59 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 02:09:59 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 02:09:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 02:09:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 02:09:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 02:09:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 02:09:59 GMT
USER memcache
# Tue, 04 Nov 2025 02:09:59 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 02:09:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f9bebc6d7be8fb19e90bd816cf5ea46e325d9d8d019345bd7e83bb27165e1c`  
		Last Modified: Tue, 04 Nov 2025 02:10:11 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d87b4f74b7b681280e1de65d55c7fef9af3294203ca9753541c48a7dbd67ac`  
		Last Modified: Tue, 04 Nov 2025 02:10:11 GMT  
		Size: 135.3 KB (135301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012aaeffd16b06fc90dbc9cf1682d2a8cb96482af9e0582ebc1dc6881617ba3d`  
		Last Modified: Tue, 04 Nov 2025 02:10:11 GMT  
		Size: 2.2 MB (2182590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30071a0aa370d64f866b34ab3ab9ed0d6e2f30dee5e631bc9b787ff5a9f4fdc0`  
		Last Modified: Tue, 04 Nov 2025 02:10:11 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18d6989abdf4813c6c982f04f7bc42405ebe217f82671824a3bd75a1f923f9c`  
		Last Modified: Tue, 04 Nov 2025 02:10:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:672ae9e81bd13a12a5ae6790d4619294b51a1cfd04a6af50c523797512fc75f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95641a91a03ab503b7750055d3fe6cf1474b1c75ce6288b8966a514375dddb1a`

```dockerfile
```

-	Layers:
	-	`sha256:f13ec9279ccf6461d334439358fdee3b542d225588c6a3857991636d57ce10ee`  
		Last Modified: Tue, 04 Nov 2025 10:34:42 GMT  
		Size: 2.0 MB (2009694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37374c73a31babc67e99ab9936b2166b55c09c55f1bc4cfff80e65a3c40d5425`  
		Last Modified: Tue, 04 Nov 2025 10:34:43 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:bc5ac38c2657d7c6d375374985e9293fb3744a75edbd96cb7a7524cc14c95d08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32572446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1f397ae776296a0fd6edeebc664c5cc9fbc3f08556289a5a1fe41c75626d379`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:17:41 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 01:17:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:20:41 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 01:20:41 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 01:20:41 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 01:20:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 01:20:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:20:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 01:20:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:20:41 GMT
USER memcache
# Tue, 04 Nov 2025 01:20:41 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 01:20:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db64d9b58942143a8d96f7823245feb1d4bf27c04222e71dbe7cedfce33d7e7f`  
		Last Modified: Tue, 04 Nov 2025 01:20:54 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e45c84ea5c10a0167bca67aede44a66fd08b708143ccb896170e30885ea50f1`  
		Last Modified: Tue, 04 Nov 2025 01:20:54 GMT  
		Size: 153.4 KB (153400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317fc2721e7de3ecc81d907c076c0de0aa0c4a80a7810a77e53335eab94adedc`  
		Last Modified: Tue, 04 Nov 2025 01:20:54 GMT  
		Size: 2.3 MB (2275238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a6f24d2569f3c38db7873c0a8f3942c5c7b876fa9eff4eaeca997bc6dc28df`  
		Last Modified: Tue, 04 Nov 2025 01:20:54 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d9e0c677fc63b66e178f9171abc553450378c9046b77cbcc52126068101766c`  
		Last Modified: Tue, 04 Nov 2025 01:20:54 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:8d2e6520d11120bd0b01076b34657bd1b1a785b38c6f7048bc58db91821f584f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97a00b54cc845295e717a2bf8ba5f7b91d5fb25acd85c6c399b94596dd67465`

```dockerfile
```

-	Layers:
	-	`sha256:7061efa09aee437d8b815835ea3f0afa471b9f76cb95323b8260dc846c1f49f1`  
		Last Modified: Tue, 04 Nov 2025 10:34:47 GMT  
		Size: 2.0 MB (2008550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0254e16c47bdde3eb7e8d57383df36625fad7398861b5aca562e447505806a8`  
		Last Modified: Tue, 04 Nov 2025 10:34:47 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; 386

```console
$ docker pull memcached@sha256:e950b4f76df4b7ad0e9dcc9f2357df6ae35314e232ad23b0ec4fb3c3beb2b84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33688177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9910abbdac4661a59a1d8fe6b43f96cd0abdde92371f8c995e7216d706f375bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:19:48 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 01:19:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:22:46 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 01:22:46 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 01:22:46 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 01:22:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 01:22:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:22:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 01:22:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:22:46 GMT
USER memcache
# Tue, 04 Nov 2025 01:22:46 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 01:22:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7f24a3a0c200106d0d9ab7b6264e50c689910154fb57bf08185b9eaf995db758`  
		Last Modified: Tue, 04 Nov 2025 00:13:54 GMT  
		Size: 31.3 MB (31294783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6840654bcf5429c7954c0483368ccd033e4222b3098ca64904c590f04dd07624`  
		Last Modified: Tue, 04 Nov 2025 01:22:59 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66205a10db2dcede178afb15530db6f282ec7194f11ffe734d9496d8b30e35a2`  
		Last Modified: Tue, 04 Nov 2025 01:22:59 GMT  
		Size: 147.4 KB (147440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b63b70a9c43a2f37c5f37f50e2aaf507c970f0133b7aaaea29fdb4e826c18b1`  
		Last Modified: Tue, 04 Nov 2025 01:23:00 GMT  
		Size: 2.2 MB (2244441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a3c1d29eba0037255cb4c7903d5de630770804520cfdb28ce05b112d526ed3`  
		Last Modified: Tue, 04 Nov 2025 01:22:59 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8da84bbfbc97884490625408deb986e43d5843e48291516064a41ab6d5963e`  
		Last Modified: Tue, 04 Nov 2025 01:22:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:51b41d632670fe8c786707c7977f9136c593c137bcde08516527421769778ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7473e22367c8e8c736bb1ce76169b1b4abf93fa0b057dec9103c4dccf90efc2`

```dockerfile
```

-	Layers:
	-	`sha256:f90631de8235b43d3b44250b8606b5783cd39dc12e9810fb5993f82a19dfe2ee`  
		Last Modified: Tue, 04 Nov 2025 10:34:51 GMT  
		Size: 2.0 MB (2005391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29d51086244a15fe10ebfe78e299fc7a89dd09601c8753741004d27949898c16`  
		Last Modified: Tue, 04 Nov 2025 10:34:52 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:ead041ea0e5c06d481ac304f7b4076a3339d849fcdffa3d25603418dc2fe82e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36187425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b0128aff763178ac8bb867e486c2450bacad45f79a5ff629194be435141070`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:52:27 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 01:52:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:55:40 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 01:55:40 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 01:55:40 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 01:55:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 01:55:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:55:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 01:55:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:55:41 GMT
USER memcache
# Tue, 04 Nov 2025 01:55:41 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 01:55:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126ce0c080daa81edc8784c59f60350b32083b3201304709775cf554155f80af`  
		Last Modified: Tue, 04 Nov 2025 01:56:04 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4c9857fe1f3ded2ba6c29c2f9591c7f5b2bfc46517527fac13f4c2b539a9a4`  
		Last Modified: Tue, 04 Nov 2025 01:56:04 GMT  
		Size: 170.2 KB (170244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e15beeee778428c51e89d0b8c3d6ca7931f0324e0a66f6b2bf85b101e9674a`  
		Last Modified: Tue, 04 Nov 2025 01:56:04 GMT  
		Size: 2.4 MB (2417022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d427e3c140105cfdb1a22a00010621a5a0834ce00ba3ea1059f8a63d8b0f5ee5`  
		Last Modified: Tue, 04 Nov 2025 01:56:04 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dfc7efa96996e95dcf030731f854bc07f2c7aa3349e75c4e74c04d924b3c62`  
		Last Modified: Tue, 04 Nov 2025 01:56:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:ad9b48a87b820bbf6c20cb57cd2247fa75ca6de00df26576f784a8f51703c571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1582395261fcee60bb7362c6cff0abd1d7325b4fde3cd609ac637f76aaa7ea5`

```dockerfile
```

-	Layers:
	-	`sha256:f5e9fbdfb8deeebb9142cd4facdedb0629028f8343a64b1e13d26ecb035f3c84`  
		Last Modified: Tue, 04 Nov 2025 10:34:55 GMT  
		Size: 2.0 MB (2011835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3dd30af34832aa3d277b4b6882a9786e4225d5a7387d5af5a66cadc59adc22d`  
		Last Modified: Tue, 04 Nov 2025 10:34:56 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:56542c7304b39c7980a644419d2ab6f603477cc9e1cb9c575d45b8c4220e0c6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30630140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e279bc62f41c4006902271742290cdde9d77c2121c1b4db697d09d01c690860e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 03:30:39 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 03:31:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:44:44 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 03:44:44 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 03:44:44 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 03:44:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 03:44:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 03:44:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 03:44:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 03:44:45 GMT
USER memcache
# Tue, 04 Nov 2025 03:44:45 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 03:44:45 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b836efb62045adb472c559fe0a4cedfe183f60ae9e36defd9b46efc4886fff56`  
		Last Modified: Tue, 04 Nov 2025 03:45:39 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db437579ba55d9291ad05cd904e857adb520e8189f0cc2fb207b475c10a95ee`  
		Last Modified: Tue, 04 Nov 2025 03:45:39 GMT  
		Size: 133.0 KB (132994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ca1f664c3ee469c225e4241d90dabf5a36c9fd5282ec51011fe16b9fcd5882`  
		Last Modified: Tue, 04 Nov 2025 03:45:39 GMT  
		Size: 2.2 MB (2219849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f5b56363e737d5d4b276274dc82b3ae7d3772bb1d6cadc5fb0c117ad6d004e`  
		Last Modified: Tue, 04 Nov 2025 03:45:39 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92139c3e4198e9ce61d77b8a86d621938a3390898a4ac22ba81eefd286a78cc7`  
		Last Modified: Tue, 04 Nov 2025 03:45:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:a72757dfcc56cb3edf581d72aa35ca18e099d18284ccfaabc697a74b2d7c2399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40a19d13356829e752dd3f0c530a1f2ef0abfc0ca53d29d3d74e1840a1698892`

```dockerfile
```

-	Layers:
	-	`sha256:78add421d4e1ac7755ca522075904f0acd06a15e1c8b9ca1bb0047a7d3ebf187`  
		Last Modified: Tue, 04 Nov 2025 07:34:38 GMT  
		Size: 2.0 MB (2002198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f1fc3731e375af1e0712ec91b83487acb49e907a1168f593f251fe43cb51fb9`  
		Last Modified: Tue, 04 Nov 2025 07:34:39 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:3de73b4ecf32984b0c6603b973257071c81c94af8351b35aa4343407c7315726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32293163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e6900a4460f82b0703aed07dde3c1722bdb7919a582b6b1f22a9ca701cb510f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 06:58:32 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 06:58:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 07:02:23 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 07:02:23 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 07:02:23 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 07:02:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 07:02:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 07:02:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 07:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 07:02:23 GMT
USER memcache
# Tue, 04 Nov 2025 07:02:23 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 07:02:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17527924bc8c8387e810ff986ddbe9998a0b5d55a4850b90b4cea0a897c94a09`  
		Last Modified: Tue, 04 Nov 2025 07:02:40 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54fd3d90bab9e973d6a8c142df91794bdc213e5bafe8926a58809036e1ee1f5`  
		Last Modified: Tue, 04 Nov 2025 07:02:40 GMT  
		Size: 140.4 KB (140429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc993f31fbd52e75a8dfc710d94d4130a8c228be35b7737c5950a5f93a1125a`  
		Last Modified: Tue, 04 Nov 2025 07:02:40 GMT  
		Size: 2.3 MB (2313833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acaa055d548771aab19234adcaf5b3ed727ee85214c303e1035e3e464e0fbda0`  
		Last Modified: Tue, 04 Nov 2025 07:02:40 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c2e1b3aad04d0544265917caef9c91d5ed4496376262541974a707026847f4`  
		Last Modified: Tue, 04 Nov 2025 07:02:40 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:414b070c237a13d5dee83e1db26eb0f953dd5af0753013a8bbd988611aa90e89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5cc4920f789bfe656195ac67c3ddd1a00030591f92b5ac4dc2b0e9dcdd2a0b`

```dockerfile
```

-	Layers:
	-	`sha256:b242fd5db27262af27c5589b736a5ae9f234cb03765c59c73e64818c1cade0c8`  
		Last Modified: Tue, 04 Nov 2025 10:35:02 GMT  
		Size: 2.0 MB (2009671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e15d059f16d47b54c3d82bdf997670c62a062815b64d7e7b486d8de0060691b4`  
		Last Modified: Tue, 04 Nov 2025 10:35:03 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.39`

```console
$ docker pull memcached@sha256:050de63e6c082df85f93ffed9c388004b3c6257a06f1904e8628a6f87658eb99
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
$ docker pull memcached@sha256:04cfb7a52848a5ddab7b57674b37c9b7b392d93ec11f0c9a4c300a9bbd1c19a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32209888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0b3dcfe086b67312e8b165a92d8e71b517bf64b356c0c804270d2330e2577c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:05:54 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 04:05:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:08:37 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 04:08:37 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 04:08:37 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 04:08:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 04:08:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:08:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 04:08:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 04:08:38 GMT
USER memcache
# Tue, 04 Nov 2025 04:08:38 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 04:08:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95dd2497c5fb854f1d1cb6790613048eae391c70dd7fe1d2c54ea024889782ad`  
		Last Modified: Tue, 04 Nov 2025 04:08:50 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5e80885bbbbd2ccaf87a97c9f6da9eb3a9b7395ce5e2b73a110224cfbcfb1e`  
		Last Modified: Tue, 04 Nov 2025 04:08:50 GMT  
		Size: 136.6 KB (136597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be7e82464812bb6ab2d37c74a6636ec8d73ec4154a192a75342dfa2f64cc8da`  
		Last Modified: Tue, 04 Nov 2025 04:08:50 GMT  
		Size: 2.3 MB (2293674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18ba826b4b67fa295ff82d2b102a5f2db243fabcb7cc2acac6cc3c33a1cbf4a`  
		Last Modified: Tue, 04 Nov 2025 04:08:50 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654bd5f6e9c2c18716bbdc27ac8f5eab96044427da57f1cb8ee268d2cd3b5f03`  
		Last Modified: Tue, 04 Nov 2025 04:08:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39` - unknown; unknown

```console
$ docker pull memcached@sha256:b78568d9b4a4cd24bae6187909a2a4a808abc29638602ee6aac1885173203e35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b08f68a528f6821adc34258cb89e510c9bf97f5596cf2e47ce7b30ba202cea`

```dockerfile
```

-	Layers:
	-	`sha256:549c9101b19d3697bed0386c9c6378a334bce6d392f694130d47f2033273b571`  
		Last Modified: Tue, 04 Nov 2025 10:34:35 GMT  
		Size: 2.0 MB (2008234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26c87354a983796083082c9e84ccf372217e5a602e78aefdec01fc26eae125ce`  
		Last Modified: Tue, 04 Nov 2025 10:34:36 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39` - linux; arm variant v5

```console
$ docker pull memcached@sha256:cfd8f3dc480855d184b335ea9b7c334731ce495de10ef2f2f17b4f82bedf1965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30319386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4fa3d1c819bb913d28b672eedf487f5165ff2dc4e5968326e550efb418196ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 00:24:40 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 00:24:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:28:01 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 00:28:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 00:28:01 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 00:28:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 00:28:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:28:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 00:28:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:28:01 GMT
USER memcache
# Tue, 04 Nov 2025 00:28:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 00:28:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:453afc2258d7bc5729fed5672fb95bafa092e30a933b4377a12034be940a671b`  
		Last Modified: Tue, 04 Nov 2025 00:13:12 GMT  
		Size: 27.9 MB (27946438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3da1461ffd1574069e2ddea407a8d31a9f215a260352498c03bb19d38c7d7ca`  
		Last Modified: Tue, 04 Nov 2025 00:28:13 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4066eb4ba0932fcecba129384e7059abaee0e303654cc15d444f8c6aa11e69bf`  
		Last Modified: Tue, 04 Nov 2025 00:28:13 GMT  
		Size: 144.0 KB (144040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f429e8aa4399dcb073c93dceeb4c04af1a46da5d750c71a36dcff1a94ab840`  
		Last Modified: Tue, 04 Nov 2025 00:28:13 GMT  
		Size: 2.2 MB (2227397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100f4b89d2a8997d39ef62d45e5590e944f3120ba301e303025c7ccaac6da369`  
		Last Modified: Tue, 04 Nov 2025 00:28:13 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334cb0302a41a8c70f7874d7de08c32eb550581a5fc8b17c9b565b9cecdb8149`  
		Last Modified: Tue, 04 Nov 2025 00:28:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39` - unknown; unknown

```console
$ docker pull memcached@sha256:281d772292417096430072e287dae06f36229ebd35a2c308d81eccc1862e99bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956875d70010cc91e002ae89b4a07ce9edfc12bc2a743b377162df7dd92e6f05`

```dockerfile
```

-	Layers:
	-	`sha256:c19709d33e93cfcba6b59a36ac6efba06597c00114be0ab5c2aaddf33ee8ba33`  
		Last Modified: Tue, 04 Nov 2025 07:34:24 GMT  
		Size: 2.0 MB (2011237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a60d569262f9d2f585a47be2ccf35c498002df82c55fd19ebcbaea6f9cd101f9`  
		Last Modified: Tue, 04 Nov 2025 07:34:25 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39` - linux; arm variant v7

```console
$ docker pull memcached@sha256:fb4a02a784ff9c44adb4a72aa161b935ed3bd148e49b37fc5e68a1f3aa30a87d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28532441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e70b324b1a195c841f52ba1facea8f75482e1bb049f38d17f8a8b69185f65166`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:06:51 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 02:06:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:09:59 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 02:09:59 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 02:09:59 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 02:09:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 02:09:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 02:09:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 02:09:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 02:09:59 GMT
USER memcache
# Tue, 04 Nov 2025 02:09:59 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 02:09:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f9bebc6d7be8fb19e90bd816cf5ea46e325d9d8d019345bd7e83bb27165e1c`  
		Last Modified: Tue, 04 Nov 2025 02:10:11 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d87b4f74b7b681280e1de65d55c7fef9af3294203ca9753541c48a7dbd67ac`  
		Last Modified: Tue, 04 Nov 2025 02:10:11 GMT  
		Size: 135.3 KB (135301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012aaeffd16b06fc90dbc9cf1682d2a8cb96482af9e0582ebc1dc6881617ba3d`  
		Last Modified: Tue, 04 Nov 2025 02:10:11 GMT  
		Size: 2.2 MB (2182590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30071a0aa370d64f866b34ab3ab9ed0d6e2f30dee5e631bc9b787ff5a9f4fdc0`  
		Last Modified: Tue, 04 Nov 2025 02:10:11 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18d6989abdf4813c6c982f04f7bc42405ebe217f82671824a3bd75a1f923f9c`  
		Last Modified: Tue, 04 Nov 2025 02:10:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39` - unknown; unknown

```console
$ docker pull memcached@sha256:672ae9e81bd13a12a5ae6790d4619294b51a1cfd04a6af50c523797512fc75f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95641a91a03ab503b7750055d3fe6cf1474b1c75ce6288b8966a514375dddb1a`

```dockerfile
```

-	Layers:
	-	`sha256:f13ec9279ccf6461d334439358fdee3b542d225588c6a3857991636d57ce10ee`  
		Last Modified: Tue, 04 Nov 2025 10:34:42 GMT  
		Size: 2.0 MB (2009694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37374c73a31babc67e99ab9936b2166b55c09c55f1bc4cfff80e65a3c40d5425`  
		Last Modified: Tue, 04 Nov 2025 10:34:43 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:bc5ac38c2657d7c6d375374985e9293fb3744a75edbd96cb7a7524cc14c95d08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32572446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1f397ae776296a0fd6edeebc664c5cc9fbc3f08556289a5a1fe41c75626d379`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:17:41 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 01:17:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:20:41 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 01:20:41 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 01:20:41 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 01:20:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 01:20:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:20:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 01:20:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:20:41 GMT
USER memcache
# Tue, 04 Nov 2025 01:20:41 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 01:20:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db64d9b58942143a8d96f7823245feb1d4bf27c04222e71dbe7cedfce33d7e7f`  
		Last Modified: Tue, 04 Nov 2025 01:20:54 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e45c84ea5c10a0167bca67aede44a66fd08b708143ccb896170e30885ea50f1`  
		Last Modified: Tue, 04 Nov 2025 01:20:54 GMT  
		Size: 153.4 KB (153400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317fc2721e7de3ecc81d907c076c0de0aa0c4a80a7810a77e53335eab94adedc`  
		Last Modified: Tue, 04 Nov 2025 01:20:54 GMT  
		Size: 2.3 MB (2275238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a6f24d2569f3c38db7873c0a8f3942c5c7b876fa9eff4eaeca997bc6dc28df`  
		Last Modified: Tue, 04 Nov 2025 01:20:54 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d9e0c677fc63b66e178f9171abc553450378c9046b77cbcc52126068101766c`  
		Last Modified: Tue, 04 Nov 2025 01:20:54 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39` - unknown; unknown

```console
$ docker pull memcached@sha256:8d2e6520d11120bd0b01076b34657bd1b1a785b38c6f7048bc58db91821f584f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97a00b54cc845295e717a2bf8ba5f7b91d5fb25acd85c6c399b94596dd67465`

```dockerfile
```

-	Layers:
	-	`sha256:7061efa09aee437d8b815835ea3f0afa471b9f76cb95323b8260dc846c1f49f1`  
		Last Modified: Tue, 04 Nov 2025 10:34:47 GMT  
		Size: 2.0 MB (2008550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0254e16c47bdde3eb7e8d57383df36625fad7398861b5aca562e447505806a8`  
		Last Modified: Tue, 04 Nov 2025 10:34:47 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39` - linux; 386

```console
$ docker pull memcached@sha256:e950b4f76df4b7ad0e9dcc9f2357df6ae35314e232ad23b0ec4fb3c3beb2b84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33688177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9910abbdac4661a59a1d8fe6b43f96cd0abdde92371f8c995e7216d706f375bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:19:48 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 01:19:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:22:46 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 01:22:46 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 01:22:46 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 01:22:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 01:22:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:22:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 01:22:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:22:46 GMT
USER memcache
# Tue, 04 Nov 2025 01:22:46 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 01:22:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7f24a3a0c200106d0d9ab7b6264e50c689910154fb57bf08185b9eaf995db758`  
		Last Modified: Tue, 04 Nov 2025 00:13:54 GMT  
		Size: 31.3 MB (31294783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6840654bcf5429c7954c0483368ccd033e4222b3098ca64904c590f04dd07624`  
		Last Modified: Tue, 04 Nov 2025 01:22:59 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66205a10db2dcede178afb15530db6f282ec7194f11ffe734d9496d8b30e35a2`  
		Last Modified: Tue, 04 Nov 2025 01:22:59 GMT  
		Size: 147.4 KB (147440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b63b70a9c43a2f37c5f37f50e2aaf507c970f0133b7aaaea29fdb4e826c18b1`  
		Last Modified: Tue, 04 Nov 2025 01:23:00 GMT  
		Size: 2.2 MB (2244441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a3c1d29eba0037255cb4c7903d5de630770804520cfdb28ce05b112d526ed3`  
		Last Modified: Tue, 04 Nov 2025 01:22:59 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8da84bbfbc97884490625408deb986e43d5843e48291516064a41ab6d5963e`  
		Last Modified: Tue, 04 Nov 2025 01:22:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39` - unknown; unknown

```console
$ docker pull memcached@sha256:51b41d632670fe8c786707c7977f9136c593c137bcde08516527421769778ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7473e22367c8e8c736bb1ce76169b1b4abf93fa0b057dec9103c4dccf90efc2`

```dockerfile
```

-	Layers:
	-	`sha256:f90631de8235b43d3b44250b8606b5783cd39dc12e9810fb5993f82a19dfe2ee`  
		Last Modified: Tue, 04 Nov 2025 10:34:51 GMT  
		Size: 2.0 MB (2005391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29d51086244a15fe10ebfe78e299fc7a89dd09601c8753741004d27949898c16`  
		Last Modified: Tue, 04 Nov 2025 10:34:52 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39` - linux; ppc64le

```console
$ docker pull memcached@sha256:ead041ea0e5c06d481ac304f7b4076a3339d849fcdffa3d25603418dc2fe82e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36187425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b0128aff763178ac8bb867e486c2450bacad45f79a5ff629194be435141070`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:52:27 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 01:52:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:55:40 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 01:55:40 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 01:55:40 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 01:55:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 01:55:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:55:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 01:55:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:55:41 GMT
USER memcache
# Tue, 04 Nov 2025 01:55:41 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 01:55:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126ce0c080daa81edc8784c59f60350b32083b3201304709775cf554155f80af`  
		Last Modified: Tue, 04 Nov 2025 01:56:04 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4c9857fe1f3ded2ba6c29c2f9591c7f5b2bfc46517527fac13f4c2b539a9a4`  
		Last Modified: Tue, 04 Nov 2025 01:56:04 GMT  
		Size: 170.2 KB (170244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e15beeee778428c51e89d0b8c3d6ca7931f0324e0a66f6b2bf85b101e9674a`  
		Last Modified: Tue, 04 Nov 2025 01:56:04 GMT  
		Size: 2.4 MB (2417022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d427e3c140105cfdb1a22a00010621a5a0834ce00ba3ea1059f8a63d8b0f5ee5`  
		Last Modified: Tue, 04 Nov 2025 01:56:04 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dfc7efa96996e95dcf030731f854bc07f2c7aa3349e75c4e74c04d924b3c62`  
		Last Modified: Tue, 04 Nov 2025 01:56:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39` - unknown; unknown

```console
$ docker pull memcached@sha256:ad9b48a87b820bbf6c20cb57cd2247fa75ca6de00df26576f784a8f51703c571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1582395261fcee60bb7362c6cff0abd1d7325b4fde3cd609ac637f76aaa7ea5`

```dockerfile
```

-	Layers:
	-	`sha256:f5e9fbdfb8deeebb9142cd4facdedb0629028f8343a64b1e13d26ecb035f3c84`  
		Last Modified: Tue, 04 Nov 2025 10:34:55 GMT  
		Size: 2.0 MB (2011835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3dd30af34832aa3d277b4b6882a9786e4225d5a7387d5af5a66cadc59adc22d`  
		Last Modified: Tue, 04 Nov 2025 10:34:56 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39` - linux; riscv64

```console
$ docker pull memcached@sha256:56542c7304b39c7980a644419d2ab6f603477cc9e1cb9c575d45b8c4220e0c6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30630140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e279bc62f41c4006902271742290cdde9d77c2121c1b4db697d09d01c690860e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 03:30:39 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 03:31:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:44:44 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 03:44:44 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 03:44:44 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 03:44:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 03:44:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 03:44:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 03:44:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 03:44:45 GMT
USER memcache
# Tue, 04 Nov 2025 03:44:45 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 03:44:45 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b836efb62045adb472c559fe0a4cedfe183f60ae9e36defd9b46efc4886fff56`  
		Last Modified: Tue, 04 Nov 2025 03:45:39 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db437579ba55d9291ad05cd904e857adb520e8189f0cc2fb207b475c10a95ee`  
		Last Modified: Tue, 04 Nov 2025 03:45:39 GMT  
		Size: 133.0 KB (132994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ca1f664c3ee469c225e4241d90dabf5a36c9fd5282ec51011fe16b9fcd5882`  
		Last Modified: Tue, 04 Nov 2025 03:45:39 GMT  
		Size: 2.2 MB (2219849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f5b56363e737d5d4b276274dc82b3ae7d3772bb1d6cadc5fb0c117ad6d004e`  
		Last Modified: Tue, 04 Nov 2025 03:45:39 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92139c3e4198e9ce61d77b8a86d621938a3390898a4ac22ba81eefd286a78cc7`  
		Last Modified: Tue, 04 Nov 2025 03:45:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39` - unknown; unknown

```console
$ docker pull memcached@sha256:a72757dfcc56cb3edf581d72aa35ca18e099d18284ccfaabc697a74b2d7c2399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40a19d13356829e752dd3f0c530a1f2ef0abfc0ca53d29d3d74e1840a1698892`

```dockerfile
```

-	Layers:
	-	`sha256:78add421d4e1ac7755ca522075904f0acd06a15e1c8b9ca1bb0047a7d3ebf187`  
		Last Modified: Tue, 04 Nov 2025 07:34:38 GMT  
		Size: 2.0 MB (2002198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f1fc3731e375af1e0712ec91b83487acb49e907a1168f593f251fe43cb51fb9`  
		Last Modified: Tue, 04 Nov 2025 07:34:39 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39` - linux; s390x

```console
$ docker pull memcached@sha256:3de73b4ecf32984b0c6603b973257071c81c94af8351b35aa4343407c7315726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32293163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e6900a4460f82b0703aed07dde3c1722bdb7919a582b6b1f22a9ca701cb510f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 06:58:32 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 06:58:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 07:02:23 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 07:02:23 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 07:02:23 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 07:02:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 07:02:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 07:02:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 07:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 07:02:23 GMT
USER memcache
# Tue, 04 Nov 2025 07:02:23 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 07:02:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17527924bc8c8387e810ff986ddbe9998a0b5d55a4850b90b4cea0a897c94a09`  
		Last Modified: Tue, 04 Nov 2025 07:02:40 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54fd3d90bab9e973d6a8c142df91794bdc213e5bafe8926a58809036e1ee1f5`  
		Last Modified: Tue, 04 Nov 2025 07:02:40 GMT  
		Size: 140.4 KB (140429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc993f31fbd52e75a8dfc710d94d4130a8c228be35b7737c5950a5f93a1125a`  
		Last Modified: Tue, 04 Nov 2025 07:02:40 GMT  
		Size: 2.3 MB (2313833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acaa055d548771aab19234adcaf5b3ed727ee85214c303e1035e3e464e0fbda0`  
		Last Modified: Tue, 04 Nov 2025 07:02:40 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c2e1b3aad04d0544265917caef9c91d5ed4496376262541974a707026847f4`  
		Last Modified: Tue, 04 Nov 2025 07:02:40 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39` - unknown; unknown

```console
$ docker pull memcached@sha256:414b070c237a13d5dee83e1db26eb0f953dd5af0753013a8bbd988611aa90e89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5cc4920f789bfe656195ac67c3ddd1a00030591f92b5ac4dc2b0e9dcdd2a0b`

```dockerfile
```

-	Layers:
	-	`sha256:b242fd5db27262af27c5589b736a5ae9f234cb03765c59c73e64818c1cade0c8`  
		Last Modified: Tue, 04 Nov 2025 10:35:02 GMT  
		Size: 2.0 MB (2009671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e15d059f16d47b54c3d82bdf997670c62a062815b64d7e7b486d8de0060691b4`  
		Last Modified: Tue, 04 Nov 2025 10:35:03 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.39-alpine`

```console
$ docker pull memcached@sha256:7b45203a99eb1419c95b875c7e48c5a9eebc0a305eeb09eefc9f3a2cff758a46
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
$ docker pull memcached@sha256:e319c3f1f6623fb2caedb14c4a5c8594f88736d90dc89d19f1ec11c8533ee263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70bce40b6c41c7484f47d1d51e8be171c582e0b3e18f2379dd66e49e3178d86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c711f2e2fe464121135109729faa513b79413712df200207ef35dfb19e550ca`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0cba00095a1ab15ee2ec0bcefea9c1fe601b9533d47626ab2fb6b74bf8a770`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 104.7 KB (104727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9204d372b3172134a4f3bbcf654ab17d33079a3aff6930e16fa7262df7c9cdbe`  
		Last Modified: Wed, 08 Oct 2025 22:42:05 GMT  
		Size: 2.0 MB (2000281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa9dd6a61433e778f70df6cd37bc70c4dcbfa8e0b0e8b1f9a0fc2f993c78685`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5a283c3ec8e0142f3f4b0b17b2901ab6d7dbff9e3f62bf978a03e5d31833f5`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:1cb56f4b692737cc136d1ff3c5dc0ca16e6b7c3be7023b1a9214348578dc4536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 KB (116754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a7a80cd482b54ecad43450e81b2d6858d2397277cf2d8358315295ef8152dc5`

```dockerfile
```

-	Layers:
	-	`sha256:659cc6afa1cde9acfc6444a310575d263f25f2f83d4987d4fddf83e5bb0d3082`  
		Last Modified: Thu, 09 Oct 2025 00:34:37 GMT  
		Size: 96.2 KB (96180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e43c8201b9a29cba2a3392f6a10e9ee6f0d6295f0248c8d3e9a792871224ec10`  
		Last Modified: Thu, 09 Oct 2025 00:34:38 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:43072fb4c4cfd652bf1a32d617dd81060515017e52b14f35faeb2fe26d071dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5557528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87416926a00e28eb0313c62e942bea0ce0517d67c95df6258358f109a49d392c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd90c0f65a0d79d1685d8fefb0f95b02afd962d0b160a1274598cb584ec37d9`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920bb020947e8d1d3b077c6d9861f8953febeb54f94421c689d40240e56b7ff0`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 101.5 KB (101532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4dc3dc5cf827d37f28e2a9a6758089ff72bc10d1915dbb61cce8f30350de40`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 2.0 MB (1950567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b2afb9c93ba0497cadc25e69b15de772b64456929b70dbe23c7ef54faa3815`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d88088c7b652b283feabfeb2974fb4bd7140ebf7da94c5d502f22841f26eb4a`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:bd27295997fc0e77ad410a3e638c230d83e3d366906a449f5349d8311d72e657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a474656b8df51a30dcb397a44bcb48c6ba3cb76e49cc3a108a15a662cd64c4b`

```dockerfile
```

-	Layers:
	-	`sha256:9a80e6fbb7fc2254a12359760da6745c28fe1d3fa2367b1137aad71c6732a8bd`  
		Last Modified: Thu, 09 Oct 2025 00:34:41 GMT  
		Size: 20.5 KB (20510 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:2caa01f7607cf1d95b2e261de80716a27de4077bf25b9dc623688091b78bf4ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c1be64fe03e8832bc6208dfced118762e57dca6b55b4482140c8fc3b06dfb3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0a02f5bd6bf63e96f5b45eda4849003b01c41b23425e7ac5a77eb01b5391e0`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f277f740301c69a561a94545bc7f140ee2d5f4ea87f88c0c861eb7b4f7983b0`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 91.3 KB (91313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e9ebffe0c4c57cd5b7fd1da1fcc7f14e2e881a81673f81e8bde4bf662a45b3`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 1.9 MB (1909853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46526f6db8416530677567eac97b5cfc18e2b86ec5c930d06de26b62f0c7a5c6`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f19627fe74f6edf1d0aa4deb85d035125067fcd28b2ee240aeb110e48330f19`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:09108dd858c6aae1c834fd9c8a7f9f78e552673ee6296d9f5cf2d84c0c26c6fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 KB (116969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9755e3f89f06272910c7fcbcaf44a3cb373b551f73bc7c9dc6dbffe13aad48`

```dockerfile
```

-	Layers:
	-	`sha256:13ba800aa65c8f207645e4069de55b11ad0a2dc87b951414df4bd35ad3923afd`  
		Last Modified: Thu, 09 Oct 2025 00:34:45 GMT  
		Size: 96.2 KB (96248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:636139066de216a683805bafa6cd72b23f1754f8dd2b5854e61578a684260418`  
		Last Modified: Thu, 09 Oct 2025 00:34:46 GMT  
		Size: 20.7 KB (20721 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:03d8054231ea1bb1dbb54d7e8bb32449b95c35475fa280a9b12d78219822fa48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6251299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42028500064e9ca7d32291ca01c636547943d3a6e6f11b80e503166efcfa6149`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098f75f9dd9f7dbf0e5993587a5b4de796bc9c01f2e795b325f1e22fe66c6833`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4c130fe47b24dbff1989543c440e0d6635524f9bf84473a6dc37472ecacac0`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 120.8 KB (120823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a41614e1c7aff72360936c76c0218330a487dd6ff6779cd243ad1c60ab6634`  
		Last Modified: Wed, 08 Oct 2025 21:31:15 GMT  
		Size: 2.0 MB (1991055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8573d5df234537883a638f95501925286c3367fd1cc40a4c6a80b70ef59ffa16`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd6f77485828d14a277cde4d3649153b058047ad8477c919e974016eb3ef6f7`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b47c7c82754dea9552416b18a213b43d6824105eb9a0318e31789b64ebb4524a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 KB (117055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc0f98e226622d3dd6ab1b57679deaa27c10decc2a26c0d7c64feeeae3b6e18`

```dockerfile
```

-	Layers:
	-	`sha256:949b28585bcee0143420765476ff3f8231f4f8049c4d0b3136c102cc9a3b272f`  
		Last Modified: Thu, 09 Oct 2025 00:34:49 GMT  
		Size: 96.3 KB (96284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c10e36727f7634ae28cb6de04bff91b38d77420fce24cf9b31503d14aff0636`  
		Last Modified: Thu, 09 Oct 2025 00:34:50 GMT  
		Size: 20.8 KB (20771 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine` - linux; 386

```console
$ docker pull memcached@sha256:3dbd66df3fa527ea9d5ef8e15484f90fd2bc4445e9d21ad40602c7d954a57c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5692091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa2b9eb15af4ed95101c0752bbde283e07e28adfed081d3a9a731aa82d1ab68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5efc90d716eb56816bbbf625c914fe13450e5c8059469e05eaef18ddf200fd`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795865ca1e6e3ac4e3ed32dabe363301a453512615868e180c6c23f28f711154`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 109.5 KB (109526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f93c274afbe9d7756256b49ac152cdbd8b21b7bf4c0e1a564bf36c6940e986e`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 2.0 MB (1962279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8db2caca7c819c90101fe1d4c62396dd78bf9677be35f005e0026d6b76c095`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d53143d130829def781c84b33cfc19fa4ac216deae7acd8c510186dd525afdb`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c7b1229c17eb2270b6a966423e63e1ad70b16a7c79c87d2ea9df82f9d733d383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 KB (116649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392076445efbd53c3eea2f14c49336ed1c8f521c209369edbb2e7686671c310a`

```dockerfile
```

-	Layers:
	-	`sha256:e91e563cbe752ee16efaa2007b7b0f49392b0f5326018a94f34a2e187c1cb743`  
		Last Modified: Wed, 08 Oct 2025 21:34:33 GMT  
		Size: 96.1 KB (96135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:207733714725a312d472d7f8657279033f48a213756c3f87714f3b4bd3e03195`  
		Last Modified: Wed, 08 Oct 2025 21:34:34 GMT  
		Size: 20.5 KB (20514 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:7e2b422eba145439e8c30b7e3191cc1f8498a721f4ca3d90c31fbc5ed80aee7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5951257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48257955bab73ec394b46e2350210da8ec488c125ff0c7cb4ce03893fff291d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8caf4ead4d89e7cb932248ec2c3e7ae5ee7efb8989eb2ab51d407f7094fe6bf`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff948909dcd7ac6c4301b934b30465617e899ca99e5cb6ac6e537be4e6f6144`  
		Last Modified: Thu, 09 Oct 2025 01:11:40 GMT  
		Size: 124.3 KB (124318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f700c3c0f9d01825484f8ddf4ea689855d4c1ed78848558c4c2bf8bf817caed0`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 2.1 MB (2093342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ee4b65e8fe80e2ad3919c8c15d8855829430a43445decbd73237095a9771a9`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06240440b6e443402b0a5ca4dc97a2225661f3da03b4c6bc67c2e9443ba95ce4`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ea61cc67a9e9ffc7a8aaf326e701ea53f5d074dc907d4ad89b4274c4cb8ce804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213afd703e8e97590346c2a301a08bd84f590c17e18aefcbcdefc4d93622c57b`

```dockerfile
```

-	Layers:
	-	`sha256:d3b5325b8aa7c43ef1c7b6f6f4a09cbcfd07d64d439c41a950bc41da09e060ff`  
		Last Modified: Thu, 09 Oct 2025 03:34:33 GMT  
		Size: 94.3 KB (94287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dd52654f2c500e460030d1f9328acbf6d095a5e2d004a4f6417b79522c7fddf`  
		Last Modified: Thu, 09 Oct 2025 03:34:34 GMT  
		Size: 20.6 KB (20647 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:588117152fae8688e5cee8aa65963a1adb1e3851845da5da3e18c80099cdb1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5559076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c983e214f48d62c0be8ffbceb2a86b504aa71c02ac195047119fe264f612c35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ec1911f91425f5b1fc00d35f661d0dcb2691cdbff9a0ea4a65789eb8dd9b89`  
		Last Modified: Thu, 09 Oct 2025 04:54:06 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb577a02d7726836381f3dfcda7cb11472d8e99ef2feb088a9570bc2c0203f15`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 107.9 KB (107909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d6a77fdbd897c87616b71f12d107a1db186b3944ccdad6b89e33186d2645bf`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 1.9 MB (1934579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2879148828c59fde0e744fb56e2490c68a2e98902f3c6a0d01bb8381588a58ba`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00990bf09cdd6c9e756438f8b076739cea749be4889b317c88bf5d06c908e9d8`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:da1dc0b73e866df98aacb962264ed5b50bf3f61862f76c42828b9a179c32e455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b8b102978a5d01b2e4ec0cf55dd00df9776a17f5f31b8bae680908b73d2e1de`

```dockerfile
```

-	Layers:
	-	`sha256:2de1c9249a94130556f0db88a655ed432c15ad40e151579870de604725fbc086`  
		Last Modified: Thu, 09 Oct 2025 06:34:34 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0262f9b3a73d1455147e4436e4bf7da9aa19a7d385d28a807688e23d6a1f1d05`  
		Last Modified: Thu, 09 Oct 2025 06:34:34 GMT  
		Size: 20.6 KB (20648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:ed5969236f4728c97696471e08c88864c21019ea227118b3336d6484ed3e5b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5804524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c049e21de6c2be2f58a69ee9eb633a51a0491febb4b48fa476556586ac0fbd96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d91bfc8fa88993cee87c33ea18494c5e9f0ad8e5b6f644411e9cd648982653`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a682e0d523bab9ef58be0ad290abcee8563e45ceccc9d04fc9b47308aeb709b`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 113.5 KB (113502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9fe3585b1938fd376ffbce3ef824ed7bc20ed49039f98e279ff5ab6159b81e`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 2.0 MB (2040430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9870bcfd315f7fc77b2fb8e80646695f277bc2e7689cf73b395e230aa6fe327c`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20f8ef4bac131999b759bd8b49d1474c540fb1874c8db4e3f4b21a7262b6903`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2d42234a0a18e44870f34c7796f717e9d61b56556ba027f9fae085adfbeeb7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd89a980babfe6204633d40fbc2b82da6c42a3c42f43f980c4d29d3015fd40b`

```dockerfile
```

-	Layers:
	-	`sha256:70fb18f0cec1c9db308335dffc76a505d0855256e74dd6cd73079481cccac057`  
		Last Modified: Thu, 09 Oct 2025 03:34:39 GMT  
		Size: 94.2 KB (94229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02c95a382d7ff8c2fab05ba8609f8b69576ec785d085ed04e606445051336db9`  
		Last Modified: Thu, 09 Oct 2025 03:34:40 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.39-alpine3.22`

```console
$ docker pull memcached@sha256:7b45203a99eb1419c95b875c7e48c5a9eebc0a305eeb09eefc9f3a2cff758a46
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
$ docker pull memcached@sha256:e319c3f1f6623fb2caedb14c4a5c8594f88736d90dc89d19f1ec11c8533ee263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70bce40b6c41c7484f47d1d51e8be171c582e0b3e18f2379dd66e49e3178d86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c711f2e2fe464121135109729faa513b79413712df200207ef35dfb19e550ca`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0cba00095a1ab15ee2ec0bcefea9c1fe601b9533d47626ab2fb6b74bf8a770`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 104.7 KB (104727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9204d372b3172134a4f3bbcf654ab17d33079a3aff6930e16fa7262df7c9cdbe`  
		Last Modified: Wed, 08 Oct 2025 22:42:05 GMT  
		Size: 2.0 MB (2000281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa9dd6a61433e778f70df6cd37bc70c4dcbfa8e0b0e8b1f9a0fc2f993c78685`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5a283c3ec8e0142f3f4b0b17b2901ab6d7dbff9e3f62bf978a03e5d31833f5`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:1cb56f4b692737cc136d1ff3c5dc0ca16e6b7c3be7023b1a9214348578dc4536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 KB (116754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a7a80cd482b54ecad43450e81b2d6858d2397277cf2d8358315295ef8152dc5`

```dockerfile
```

-	Layers:
	-	`sha256:659cc6afa1cde9acfc6444a310575d263f25f2f83d4987d4fddf83e5bb0d3082`  
		Last Modified: Thu, 09 Oct 2025 00:34:37 GMT  
		Size: 96.2 KB (96180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e43c8201b9a29cba2a3392f6a10e9ee6f0d6295f0248c8d3e9a792871224ec10`  
		Last Modified: Thu, 09 Oct 2025 00:34:38 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine3.22` - linux; arm variant v6

```console
$ docker pull memcached@sha256:43072fb4c4cfd652bf1a32d617dd81060515017e52b14f35faeb2fe26d071dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5557528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87416926a00e28eb0313c62e942bea0ce0517d67c95df6258358f109a49d392c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd90c0f65a0d79d1685d8fefb0f95b02afd962d0b160a1274598cb584ec37d9`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920bb020947e8d1d3b077c6d9861f8953febeb54f94421c689d40240e56b7ff0`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 101.5 KB (101532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4dc3dc5cf827d37f28e2a9a6758089ff72bc10d1915dbb61cce8f30350de40`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 2.0 MB (1950567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b2afb9c93ba0497cadc25e69b15de772b64456929b70dbe23c7ef54faa3815`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d88088c7b652b283feabfeb2974fb4bd7140ebf7da94c5d502f22841f26eb4a`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:bd27295997fc0e77ad410a3e638c230d83e3d366906a449f5349d8311d72e657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a474656b8df51a30dcb397a44bcb48c6ba3cb76e49cc3a108a15a662cd64c4b`

```dockerfile
```

-	Layers:
	-	`sha256:9a80e6fbb7fc2254a12359760da6745c28fe1d3fa2367b1137aad71c6732a8bd`  
		Last Modified: Thu, 09 Oct 2025 00:34:41 GMT  
		Size: 20.5 KB (20510 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine3.22` - linux; arm variant v7

```console
$ docker pull memcached@sha256:2caa01f7607cf1d95b2e261de80716a27de4077bf25b9dc623688091b78bf4ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c1be64fe03e8832bc6208dfced118762e57dca6b55b4482140c8fc3b06dfb3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0a02f5bd6bf63e96f5b45eda4849003b01c41b23425e7ac5a77eb01b5391e0`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f277f740301c69a561a94545bc7f140ee2d5f4ea87f88c0c861eb7b4f7983b0`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 91.3 KB (91313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e9ebffe0c4c57cd5b7fd1da1fcc7f14e2e881a81673f81e8bde4bf662a45b3`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 1.9 MB (1909853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46526f6db8416530677567eac97b5cfc18e2b86ec5c930d06de26b62f0c7a5c6`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f19627fe74f6edf1d0aa4deb85d035125067fcd28b2ee240aeb110e48330f19`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:09108dd858c6aae1c834fd9c8a7f9f78e552673ee6296d9f5cf2d84c0c26c6fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 KB (116969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9755e3f89f06272910c7fcbcaf44a3cb373b551f73bc7c9dc6dbffe13aad48`

```dockerfile
```

-	Layers:
	-	`sha256:13ba800aa65c8f207645e4069de55b11ad0a2dc87b951414df4bd35ad3923afd`  
		Last Modified: Thu, 09 Oct 2025 00:34:45 GMT  
		Size: 96.2 KB (96248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:636139066de216a683805bafa6cd72b23f1754f8dd2b5854e61578a684260418`  
		Last Modified: Thu, 09 Oct 2025 00:34:46 GMT  
		Size: 20.7 KB (20721 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:03d8054231ea1bb1dbb54d7e8bb32449b95c35475fa280a9b12d78219822fa48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6251299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42028500064e9ca7d32291ca01c636547943d3a6e6f11b80e503166efcfa6149`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098f75f9dd9f7dbf0e5993587a5b4de796bc9c01f2e795b325f1e22fe66c6833`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4c130fe47b24dbff1989543c440e0d6635524f9bf84473a6dc37472ecacac0`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 120.8 KB (120823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a41614e1c7aff72360936c76c0218330a487dd6ff6779cd243ad1c60ab6634`  
		Last Modified: Wed, 08 Oct 2025 21:31:15 GMT  
		Size: 2.0 MB (1991055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8573d5df234537883a638f95501925286c3367fd1cc40a4c6a80b70ef59ffa16`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd6f77485828d14a277cde4d3649153b058047ad8477c919e974016eb3ef6f7`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:b47c7c82754dea9552416b18a213b43d6824105eb9a0318e31789b64ebb4524a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 KB (117055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc0f98e226622d3dd6ab1b57679deaa27c10decc2a26c0d7c64feeeae3b6e18`

```dockerfile
```

-	Layers:
	-	`sha256:949b28585bcee0143420765476ff3f8231f4f8049c4d0b3136c102cc9a3b272f`  
		Last Modified: Thu, 09 Oct 2025 00:34:49 GMT  
		Size: 96.3 KB (96284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c10e36727f7634ae28cb6de04bff91b38d77420fce24cf9b31503d14aff0636`  
		Last Modified: Thu, 09 Oct 2025 00:34:50 GMT  
		Size: 20.8 KB (20771 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine3.22` - linux; 386

```console
$ docker pull memcached@sha256:3dbd66df3fa527ea9d5ef8e15484f90fd2bc4445e9d21ad40602c7d954a57c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5692091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa2b9eb15af4ed95101c0752bbde283e07e28adfed081d3a9a731aa82d1ab68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5efc90d716eb56816bbbf625c914fe13450e5c8059469e05eaef18ddf200fd`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795865ca1e6e3ac4e3ed32dabe363301a453512615868e180c6c23f28f711154`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 109.5 KB (109526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f93c274afbe9d7756256b49ac152cdbd8b21b7bf4c0e1a564bf36c6940e986e`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 2.0 MB (1962279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8db2caca7c819c90101fe1d4c62396dd78bf9677be35f005e0026d6b76c095`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d53143d130829def781c84b33cfc19fa4ac216deae7acd8c510186dd525afdb`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:c7b1229c17eb2270b6a966423e63e1ad70b16a7c79c87d2ea9df82f9d733d383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 KB (116649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392076445efbd53c3eea2f14c49336ed1c8f521c209369edbb2e7686671c310a`

```dockerfile
```

-	Layers:
	-	`sha256:e91e563cbe752ee16efaa2007b7b0f49392b0f5326018a94f34a2e187c1cb743`  
		Last Modified: Wed, 08 Oct 2025 21:34:33 GMT  
		Size: 96.1 KB (96135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:207733714725a312d472d7f8657279033f48a213756c3f87714f3b4bd3e03195`  
		Last Modified: Wed, 08 Oct 2025 21:34:34 GMT  
		Size: 20.5 KB (20514 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine3.22` - linux; ppc64le

```console
$ docker pull memcached@sha256:7e2b422eba145439e8c30b7e3191cc1f8498a721f4ca3d90c31fbc5ed80aee7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5951257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48257955bab73ec394b46e2350210da8ec488c125ff0c7cb4ce03893fff291d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8caf4ead4d89e7cb932248ec2c3e7ae5ee7efb8989eb2ab51d407f7094fe6bf`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff948909dcd7ac6c4301b934b30465617e899ca99e5cb6ac6e537be4e6f6144`  
		Last Modified: Thu, 09 Oct 2025 01:11:40 GMT  
		Size: 124.3 KB (124318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f700c3c0f9d01825484f8ddf4ea689855d4c1ed78848558c4c2bf8bf817caed0`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 2.1 MB (2093342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ee4b65e8fe80e2ad3919c8c15d8855829430a43445decbd73237095a9771a9`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06240440b6e443402b0a5ca4dc97a2225661f3da03b4c6bc67c2e9443ba95ce4`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:ea61cc67a9e9ffc7a8aaf326e701ea53f5d074dc907d4ad89b4274c4cb8ce804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213afd703e8e97590346c2a301a08bd84f590c17e18aefcbcdefc4d93622c57b`

```dockerfile
```

-	Layers:
	-	`sha256:d3b5325b8aa7c43ef1c7b6f6f4a09cbcfd07d64d439c41a950bc41da09e060ff`  
		Last Modified: Thu, 09 Oct 2025 03:34:33 GMT  
		Size: 94.3 KB (94287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dd52654f2c500e460030d1f9328acbf6d095a5e2d004a4f6417b79522c7fddf`  
		Last Modified: Thu, 09 Oct 2025 03:34:34 GMT  
		Size: 20.6 KB (20647 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine3.22` - linux; riscv64

```console
$ docker pull memcached@sha256:588117152fae8688e5cee8aa65963a1adb1e3851845da5da3e18c80099cdb1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5559076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c983e214f48d62c0be8ffbceb2a86b504aa71c02ac195047119fe264f612c35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ec1911f91425f5b1fc00d35f661d0dcb2691cdbff9a0ea4a65789eb8dd9b89`  
		Last Modified: Thu, 09 Oct 2025 04:54:06 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb577a02d7726836381f3dfcda7cb11472d8e99ef2feb088a9570bc2c0203f15`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 107.9 KB (107909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d6a77fdbd897c87616b71f12d107a1db186b3944ccdad6b89e33186d2645bf`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 1.9 MB (1934579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2879148828c59fde0e744fb56e2490c68a2e98902f3c6a0d01bb8381588a58ba`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00990bf09cdd6c9e756438f8b076739cea749be4889b317c88bf5d06c908e9d8`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:da1dc0b73e866df98aacb962264ed5b50bf3f61862f76c42828b9a179c32e455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b8b102978a5d01b2e4ec0cf55dd00df9776a17f5f31b8bae680908b73d2e1de`

```dockerfile
```

-	Layers:
	-	`sha256:2de1c9249a94130556f0db88a655ed432c15ad40e151579870de604725fbc086`  
		Last Modified: Thu, 09 Oct 2025 06:34:34 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0262f9b3a73d1455147e4436e4bf7da9aa19a7d385d28a807688e23d6a1f1d05`  
		Last Modified: Thu, 09 Oct 2025 06:34:34 GMT  
		Size: 20.6 KB (20648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine3.22` - linux; s390x

```console
$ docker pull memcached@sha256:ed5969236f4728c97696471e08c88864c21019ea227118b3336d6484ed3e5b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5804524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c049e21de6c2be2f58a69ee9eb633a51a0491febb4b48fa476556586ac0fbd96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d91bfc8fa88993cee87c33ea18494c5e9f0ad8e5b6f644411e9cd648982653`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a682e0d523bab9ef58be0ad290abcee8563e45ceccc9d04fc9b47308aeb709b`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 113.5 KB (113502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9fe3585b1938fd376ffbce3ef824ed7bc20ed49039f98e279ff5ab6159b81e`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 2.0 MB (2040430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9870bcfd315f7fc77b2fb8e80646695f277bc2e7689cf73b395e230aa6fe327c`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20f8ef4bac131999b759bd8b49d1474c540fb1874c8db4e3f4b21a7262b6903`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:2d42234a0a18e44870f34c7796f717e9d61b56556ba027f9fae085adfbeeb7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd89a980babfe6204633d40fbc2b82da6c42a3c42f43f980c4d29d3015fd40b`

```dockerfile
```

-	Layers:
	-	`sha256:70fb18f0cec1c9db308335dffc76a505d0855256e74dd6cd73079481cccac057`  
		Last Modified: Thu, 09 Oct 2025 03:34:39 GMT  
		Size: 94.2 KB (94229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02c95a382d7ff8c2fab05ba8609f8b69576ec785d085ed04e606445051336db9`  
		Last Modified: Thu, 09 Oct 2025 03:34:40 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.39-trixie`

```console
$ docker pull memcached@sha256:050de63e6c082df85f93ffed9c388004b3c6257a06f1904e8628a6f87658eb99
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
$ docker pull memcached@sha256:04cfb7a52848a5ddab7b57674b37c9b7b392d93ec11f0c9a4c300a9bbd1c19a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32209888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0b3dcfe086b67312e8b165a92d8e71b517bf64b356c0c804270d2330e2577c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:05:54 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 04:05:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:08:37 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 04:08:37 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 04:08:37 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 04:08:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 04:08:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:08:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 04:08:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 04:08:38 GMT
USER memcache
# Tue, 04 Nov 2025 04:08:38 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 04:08:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95dd2497c5fb854f1d1cb6790613048eae391c70dd7fe1d2c54ea024889782ad`  
		Last Modified: Tue, 04 Nov 2025 04:08:50 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5e80885bbbbd2ccaf87a97c9f6da9eb3a9b7395ce5e2b73a110224cfbcfb1e`  
		Last Modified: Tue, 04 Nov 2025 04:08:50 GMT  
		Size: 136.6 KB (136597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be7e82464812bb6ab2d37c74a6636ec8d73ec4154a192a75342dfa2f64cc8da`  
		Last Modified: Tue, 04 Nov 2025 04:08:50 GMT  
		Size: 2.3 MB (2293674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18ba826b4b67fa295ff82d2b102a5f2db243fabcb7cc2acac6cc3c33a1cbf4a`  
		Last Modified: Tue, 04 Nov 2025 04:08:50 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654bd5f6e9c2c18716bbdc27ac8f5eab96044427da57f1cb8ee268d2cd3b5f03`  
		Last Modified: Tue, 04 Nov 2025 04:08:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:b78568d9b4a4cd24bae6187909a2a4a808abc29638602ee6aac1885173203e35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b08f68a528f6821adc34258cb89e510c9bf97f5596cf2e47ce7b30ba202cea`

```dockerfile
```

-	Layers:
	-	`sha256:549c9101b19d3697bed0386c9c6378a334bce6d392f694130d47f2033273b571`  
		Last Modified: Tue, 04 Nov 2025 10:34:35 GMT  
		Size: 2.0 MB (2008234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26c87354a983796083082c9e84ccf372217e5a602e78aefdec01fc26eae125ce`  
		Last Modified: Tue, 04 Nov 2025 10:34:36 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:cfd8f3dc480855d184b335ea9b7c334731ce495de10ef2f2f17b4f82bedf1965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30319386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4fa3d1c819bb913d28b672eedf487f5165ff2dc4e5968326e550efb418196ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 00:24:40 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 00:24:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:28:01 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 00:28:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 00:28:01 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 00:28:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 00:28:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:28:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 00:28:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:28:01 GMT
USER memcache
# Tue, 04 Nov 2025 00:28:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 00:28:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:453afc2258d7bc5729fed5672fb95bafa092e30a933b4377a12034be940a671b`  
		Last Modified: Tue, 04 Nov 2025 00:13:12 GMT  
		Size: 27.9 MB (27946438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3da1461ffd1574069e2ddea407a8d31a9f215a260352498c03bb19d38c7d7ca`  
		Last Modified: Tue, 04 Nov 2025 00:28:13 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4066eb4ba0932fcecba129384e7059abaee0e303654cc15d444f8c6aa11e69bf`  
		Last Modified: Tue, 04 Nov 2025 00:28:13 GMT  
		Size: 144.0 KB (144040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f429e8aa4399dcb073c93dceeb4c04af1a46da5d750c71a36dcff1a94ab840`  
		Last Modified: Tue, 04 Nov 2025 00:28:13 GMT  
		Size: 2.2 MB (2227397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100f4b89d2a8997d39ef62d45e5590e944f3120ba301e303025c7ccaac6da369`  
		Last Modified: Tue, 04 Nov 2025 00:28:13 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334cb0302a41a8c70f7874d7de08c32eb550581a5fc8b17c9b565b9cecdb8149`  
		Last Modified: Tue, 04 Nov 2025 00:28:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:281d772292417096430072e287dae06f36229ebd35a2c308d81eccc1862e99bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956875d70010cc91e002ae89b4a07ce9edfc12bc2a743b377162df7dd92e6f05`

```dockerfile
```

-	Layers:
	-	`sha256:c19709d33e93cfcba6b59a36ac6efba06597c00114be0ab5c2aaddf33ee8ba33`  
		Last Modified: Tue, 04 Nov 2025 07:34:24 GMT  
		Size: 2.0 MB (2011237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a60d569262f9d2f585a47be2ccf35c498002df82c55fd19ebcbaea6f9cd101f9`  
		Last Modified: Tue, 04 Nov 2025 07:34:25 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:fb4a02a784ff9c44adb4a72aa161b935ed3bd148e49b37fc5e68a1f3aa30a87d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28532441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e70b324b1a195c841f52ba1facea8f75482e1bb049f38d17f8a8b69185f65166`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:06:51 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 02:06:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:09:59 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 02:09:59 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 02:09:59 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 02:09:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 02:09:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 02:09:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 02:09:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 02:09:59 GMT
USER memcache
# Tue, 04 Nov 2025 02:09:59 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 02:09:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f9bebc6d7be8fb19e90bd816cf5ea46e325d9d8d019345bd7e83bb27165e1c`  
		Last Modified: Tue, 04 Nov 2025 02:10:11 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d87b4f74b7b681280e1de65d55c7fef9af3294203ca9753541c48a7dbd67ac`  
		Last Modified: Tue, 04 Nov 2025 02:10:11 GMT  
		Size: 135.3 KB (135301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012aaeffd16b06fc90dbc9cf1682d2a8cb96482af9e0582ebc1dc6881617ba3d`  
		Last Modified: Tue, 04 Nov 2025 02:10:11 GMT  
		Size: 2.2 MB (2182590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30071a0aa370d64f866b34ab3ab9ed0d6e2f30dee5e631bc9b787ff5a9f4fdc0`  
		Last Modified: Tue, 04 Nov 2025 02:10:11 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18d6989abdf4813c6c982f04f7bc42405ebe217f82671824a3bd75a1f923f9c`  
		Last Modified: Tue, 04 Nov 2025 02:10:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:672ae9e81bd13a12a5ae6790d4619294b51a1cfd04a6af50c523797512fc75f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95641a91a03ab503b7750055d3fe6cf1474b1c75ce6288b8966a514375dddb1a`

```dockerfile
```

-	Layers:
	-	`sha256:f13ec9279ccf6461d334439358fdee3b542d225588c6a3857991636d57ce10ee`  
		Last Modified: Tue, 04 Nov 2025 10:34:42 GMT  
		Size: 2.0 MB (2009694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37374c73a31babc67e99ab9936b2166b55c09c55f1bc4cfff80e65a3c40d5425`  
		Last Modified: Tue, 04 Nov 2025 10:34:43 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:bc5ac38c2657d7c6d375374985e9293fb3744a75edbd96cb7a7524cc14c95d08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32572446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1f397ae776296a0fd6edeebc664c5cc9fbc3f08556289a5a1fe41c75626d379`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:17:41 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 01:17:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:20:41 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 01:20:41 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 01:20:41 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 01:20:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 01:20:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:20:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 01:20:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:20:41 GMT
USER memcache
# Tue, 04 Nov 2025 01:20:41 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 01:20:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db64d9b58942143a8d96f7823245feb1d4bf27c04222e71dbe7cedfce33d7e7f`  
		Last Modified: Tue, 04 Nov 2025 01:20:54 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e45c84ea5c10a0167bca67aede44a66fd08b708143ccb896170e30885ea50f1`  
		Last Modified: Tue, 04 Nov 2025 01:20:54 GMT  
		Size: 153.4 KB (153400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317fc2721e7de3ecc81d907c076c0de0aa0c4a80a7810a77e53335eab94adedc`  
		Last Modified: Tue, 04 Nov 2025 01:20:54 GMT  
		Size: 2.3 MB (2275238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a6f24d2569f3c38db7873c0a8f3942c5c7b876fa9eff4eaeca997bc6dc28df`  
		Last Modified: Tue, 04 Nov 2025 01:20:54 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d9e0c677fc63b66e178f9171abc553450378c9046b77cbcc52126068101766c`  
		Last Modified: Tue, 04 Nov 2025 01:20:54 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:8d2e6520d11120bd0b01076b34657bd1b1a785b38c6f7048bc58db91821f584f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97a00b54cc845295e717a2bf8ba5f7b91d5fb25acd85c6c399b94596dd67465`

```dockerfile
```

-	Layers:
	-	`sha256:7061efa09aee437d8b815835ea3f0afa471b9f76cb95323b8260dc846c1f49f1`  
		Last Modified: Tue, 04 Nov 2025 10:34:47 GMT  
		Size: 2.0 MB (2008550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0254e16c47bdde3eb7e8d57383df36625fad7398861b5aca562e447505806a8`  
		Last Modified: Tue, 04 Nov 2025 10:34:47 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-trixie` - linux; 386

```console
$ docker pull memcached@sha256:e950b4f76df4b7ad0e9dcc9f2357df6ae35314e232ad23b0ec4fb3c3beb2b84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33688177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9910abbdac4661a59a1d8fe6b43f96cd0abdde92371f8c995e7216d706f375bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:19:48 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 01:19:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:22:46 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 01:22:46 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 01:22:46 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 01:22:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 01:22:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:22:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 01:22:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:22:46 GMT
USER memcache
# Tue, 04 Nov 2025 01:22:46 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 01:22:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7f24a3a0c200106d0d9ab7b6264e50c689910154fb57bf08185b9eaf995db758`  
		Last Modified: Tue, 04 Nov 2025 00:13:54 GMT  
		Size: 31.3 MB (31294783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6840654bcf5429c7954c0483368ccd033e4222b3098ca64904c590f04dd07624`  
		Last Modified: Tue, 04 Nov 2025 01:22:59 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66205a10db2dcede178afb15530db6f282ec7194f11ffe734d9496d8b30e35a2`  
		Last Modified: Tue, 04 Nov 2025 01:22:59 GMT  
		Size: 147.4 KB (147440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b63b70a9c43a2f37c5f37f50e2aaf507c970f0133b7aaaea29fdb4e826c18b1`  
		Last Modified: Tue, 04 Nov 2025 01:23:00 GMT  
		Size: 2.2 MB (2244441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a3c1d29eba0037255cb4c7903d5de630770804520cfdb28ce05b112d526ed3`  
		Last Modified: Tue, 04 Nov 2025 01:22:59 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8da84bbfbc97884490625408deb986e43d5843e48291516064a41ab6d5963e`  
		Last Modified: Tue, 04 Nov 2025 01:22:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:51b41d632670fe8c786707c7977f9136c593c137bcde08516527421769778ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7473e22367c8e8c736bb1ce76169b1b4abf93fa0b057dec9103c4dccf90efc2`

```dockerfile
```

-	Layers:
	-	`sha256:f90631de8235b43d3b44250b8606b5783cd39dc12e9810fb5993f82a19dfe2ee`  
		Last Modified: Tue, 04 Nov 2025 10:34:51 GMT  
		Size: 2.0 MB (2005391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29d51086244a15fe10ebfe78e299fc7a89dd09601c8753741004d27949898c16`  
		Last Modified: Tue, 04 Nov 2025 10:34:52 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:ead041ea0e5c06d481ac304f7b4076a3339d849fcdffa3d25603418dc2fe82e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36187425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b0128aff763178ac8bb867e486c2450bacad45f79a5ff629194be435141070`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:52:27 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 01:52:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:55:40 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 01:55:40 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 01:55:40 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 01:55:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 01:55:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:55:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 01:55:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:55:41 GMT
USER memcache
# Tue, 04 Nov 2025 01:55:41 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 01:55:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126ce0c080daa81edc8784c59f60350b32083b3201304709775cf554155f80af`  
		Last Modified: Tue, 04 Nov 2025 01:56:04 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4c9857fe1f3ded2ba6c29c2f9591c7f5b2bfc46517527fac13f4c2b539a9a4`  
		Last Modified: Tue, 04 Nov 2025 01:56:04 GMT  
		Size: 170.2 KB (170244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e15beeee778428c51e89d0b8c3d6ca7931f0324e0a66f6b2bf85b101e9674a`  
		Last Modified: Tue, 04 Nov 2025 01:56:04 GMT  
		Size: 2.4 MB (2417022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d427e3c140105cfdb1a22a00010621a5a0834ce00ba3ea1059f8a63d8b0f5ee5`  
		Last Modified: Tue, 04 Nov 2025 01:56:04 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dfc7efa96996e95dcf030731f854bc07f2c7aa3349e75c4e74c04d924b3c62`  
		Last Modified: Tue, 04 Nov 2025 01:56:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:ad9b48a87b820bbf6c20cb57cd2247fa75ca6de00df26576f784a8f51703c571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1582395261fcee60bb7362c6cff0abd1d7325b4fde3cd609ac637f76aaa7ea5`

```dockerfile
```

-	Layers:
	-	`sha256:f5e9fbdfb8deeebb9142cd4facdedb0629028f8343a64b1e13d26ecb035f3c84`  
		Last Modified: Tue, 04 Nov 2025 10:34:55 GMT  
		Size: 2.0 MB (2011835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3dd30af34832aa3d277b4b6882a9786e4225d5a7387d5af5a66cadc59adc22d`  
		Last Modified: Tue, 04 Nov 2025 10:34:56 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:56542c7304b39c7980a644419d2ab6f603477cc9e1cb9c575d45b8c4220e0c6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30630140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e279bc62f41c4006902271742290cdde9d77c2121c1b4db697d09d01c690860e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 03:30:39 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 03:31:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:44:44 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 03:44:44 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 03:44:44 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 03:44:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 03:44:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 03:44:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 03:44:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 03:44:45 GMT
USER memcache
# Tue, 04 Nov 2025 03:44:45 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 03:44:45 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b836efb62045adb472c559fe0a4cedfe183f60ae9e36defd9b46efc4886fff56`  
		Last Modified: Tue, 04 Nov 2025 03:45:39 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db437579ba55d9291ad05cd904e857adb520e8189f0cc2fb207b475c10a95ee`  
		Last Modified: Tue, 04 Nov 2025 03:45:39 GMT  
		Size: 133.0 KB (132994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ca1f664c3ee469c225e4241d90dabf5a36c9fd5282ec51011fe16b9fcd5882`  
		Last Modified: Tue, 04 Nov 2025 03:45:39 GMT  
		Size: 2.2 MB (2219849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f5b56363e737d5d4b276274dc82b3ae7d3772bb1d6cadc5fb0c117ad6d004e`  
		Last Modified: Tue, 04 Nov 2025 03:45:39 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92139c3e4198e9ce61d77b8a86d621938a3390898a4ac22ba81eefd286a78cc7`  
		Last Modified: Tue, 04 Nov 2025 03:45:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:a72757dfcc56cb3edf581d72aa35ca18e099d18284ccfaabc697a74b2d7c2399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40a19d13356829e752dd3f0c530a1f2ef0abfc0ca53d29d3d74e1840a1698892`

```dockerfile
```

-	Layers:
	-	`sha256:78add421d4e1ac7755ca522075904f0acd06a15e1c8b9ca1bb0047a7d3ebf187`  
		Last Modified: Tue, 04 Nov 2025 07:34:38 GMT  
		Size: 2.0 MB (2002198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f1fc3731e375af1e0712ec91b83487acb49e907a1168f593f251fe43cb51fb9`  
		Last Modified: Tue, 04 Nov 2025 07:34:39 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:3de73b4ecf32984b0c6603b973257071c81c94af8351b35aa4343407c7315726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32293163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e6900a4460f82b0703aed07dde3c1722bdb7919a582b6b1f22a9ca701cb510f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 06:58:32 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 06:58:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 07:02:23 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 07:02:23 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 07:02:23 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 07:02:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 07:02:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 07:02:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 07:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 07:02:23 GMT
USER memcache
# Tue, 04 Nov 2025 07:02:23 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 07:02:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17527924bc8c8387e810ff986ddbe9998a0b5d55a4850b90b4cea0a897c94a09`  
		Last Modified: Tue, 04 Nov 2025 07:02:40 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54fd3d90bab9e973d6a8c142df91794bdc213e5bafe8926a58809036e1ee1f5`  
		Last Modified: Tue, 04 Nov 2025 07:02:40 GMT  
		Size: 140.4 KB (140429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc993f31fbd52e75a8dfc710d94d4130a8c228be35b7737c5950a5f93a1125a`  
		Last Modified: Tue, 04 Nov 2025 07:02:40 GMT  
		Size: 2.3 MB (2313833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acaa055d548771aab19234adcaf5b3ed727ee85214c303e1035e3e464e0fbda0`  
		Last Modified: Tue, 04 Nov 2025 07:02:40 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c2e1b3aad04d0544265917caef9c91d5ed4496376262541974a707026847f4`  
		Last Modified: Tue, 04 Nov 2025 07:02:40 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:414b070c237a13d5dee83e1db26eb0f953dd5af0753013a8bbd988611aa90e89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5cc4920f789bfe656195ac67c3ddd1a00030591f92b5ac4dc2b0e9dcdd2a0b`

```dockerfile
```

-	Layers:
	-	`sha256:b242fd5db27262af27c5589b736a5ae9f234cb03765c59c73e64818c1cade0c8`  
		Last Modified: Tue, 04 Nov 2025 10:35:02 GMT  
		Size: 2.0 MB (2009671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e15d059f16d47b54c3d82bdf997670c62a062815b64d7e7b486d8de0060691b4`  
		Last Modified: Tue, 04 Nov 2025 10:35:03 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine`

```console
$ docker pull memcached@sha256:7b45203a99eb1419c95b875c7e48c5a9eebc0a305eeb09eefc9f3a2cff758a46
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
$ docker pull memcached@sha256:e319c3f1f6623fb2caedb14c4a5c8594f88736d90dc89d19f1ec11c8533ee263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70bce40b6c41c7484f47d1d51e8be171c582e0b3e18f2379dd66e49e3178d86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c711f2e2fe464121135109729faa513b79413712df200207ef35dfb19e550ca`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0cba00095a1ab15ee2ec0bcefea9c1fe601b9533d47626ab2fb6b74bf8a770`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 104.7 KB (104727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9204d372b3172134a4f3bbcf654ab17d33079a3aff6930e16fa7262df7c9cdbe`  
		Last Modified: Wed, 08 Oct 2025 22:42:05 GMT  
		Size: 2.0 MB (2000281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa9dd6a61433e778f70df6cd37bc70c4dcbfa8e0b0e8b1f9a0fc2f993c78685`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5a283c3ec8e0142f3f4b0b17b2901ab6d7dbff9e3f62bf978a03e5d31833f5`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:1cb56f4b692737cc136d1ff3c5dc0ca16e6b7c3be7023b1a9214348578dc4536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 KB (116754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a7a80cd482b54ecad43450e81b2d6858d2397277cf2d8358315295ef8152dc5`

```dockerfile
```

-	Layers:
	-	`sha256:659cc6afa1cde9acfc6444a310575d263f25f2f83d4987d4fddf83e5bb0d3082`  
		Last Modified: Thu, 09 Oct 2025 00:34:37 GMT  
		Size: 96.2 KB (96180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e43c8201b9a29cba2a3392f6a10e9ee6f0d6295f0248c8d3e9a792871224ec10`  
		Last Modified: Thu, 09 Oct 2025 00:34:38 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:43072fb4c4cfd652bf1a32d617dd81060515017e52b14f35faeb2fe26d071dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5557528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87416926a00e28eb0313c62e942bea0ce0517d67c95df6258358f109a49d392c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd90c0f65a0d79d1685d8fefb0f95b02afd962d0b160a1274598cb584ec37d9`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920bb020947e8d1d3b077c6d9861f8953febeb54f94421c689d40240e56b7ff0`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 101.5 KB (101532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4dc3dc5cf827d37f28e2a9a6758089ff72bc10d1915dbb61cce8f30350de40`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 2.0 MB (1950567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b2afb9c93ba0497cadc25e69b15de772b64456929b70dbe23c7ef54faa3815`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d88088c7b652b283feabfeb2974fb4bd7140ebf7da94c5d502f22841f26eb4a`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:bd27295997fc0e77ad410a3e638c230d83e3d366906a449f5349d8311d72e657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a474656b8df51a30dcb397a44bcb48c6ba3cb76e49cc3a108a15a662cd64c4b`

```dockerfile
```

-	Layers:
	-	`sha256:9a80e6fbb7fc2254a12359760da6745c28fe1d3fa2367b1137aad71c6732a8bd`  
		Last Modified: Thu, 09 Oct 2025 00:34:41 GMT  
		Size: 20.5 KB (20510 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:2caa01f7607cf1d95b2e261de80716a27de4077bf25b9dc623688091b78bf4ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c1be64fe03e8832bc6208dfced118762e57dca6b55b4482140c8fc3b06dfb3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0a02f5bd6bf63e96f5b45eda4849003b01c41b23425e7ac5a77eb01b5391e0`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f277f740301c69a561a94545bc7f140ee2d5f4ea87f88c0c861eb7b4f7983b0`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 91.3 KB (91313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e9ebffe0c4c57cd5b7fd1da1fcc7f14e2e881a81673f81e8bde4bf662a45b3`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 1.9 MB (1909853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46526f6db8416530677567eac97b5cfc18e2b86ec5c930d06de26b62f0c7a5c6`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f19627fe74f6edf1d0aa4deb85d035125067fcd28b2ee240aeb110e48330f19`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:09108dd858c6aae1c834fd9c8a7f9f78e552673ee6296d9f5cf2d84c0c26c6fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 KB (116969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9755e3f89f06272910c7fcbcaf44a3cb373b551f73bc7c9dc6dbffe13aad48`

```dockerfile
```

-	Layers:
	-	`sha256:13ba800aa65c8f207645e4069de55b11ad0a2dc87b951414df4bd35ad3923afd`  
		Last Modified: Thu, 09 Oct 2025 00:34:45 GMT  
		Size: 96.2 KB (96248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:636139066de216a683805bafa6cd72b23f1754f8dd2b5854e61578a684260418`  
		Last Modified: Thu, 09 Oct 2025 00:34:46 GMT  
		Size: 20.7 KB (20721 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:03d8054231ea1bb1dbb54d7e8bb32449b95c35475fa280a9b12d78219822fa48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6251299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42028500064e9ca7d32291ca01c636547943d3a6e6f11b80e503166efcfa6149`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098f75f9dd9f7dbf0e5993587a5b4de796bc9c01f2e795b325f1e22fe66c6833`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4c130fe47b24dbff1989543c440e0d6635524f9bf84473a6dc37472ecacac0`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 120.8 KB (120823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a41614e1c7aff72360936c76c0218330a487dd6ff6779cd243ad1c60ab6634`  
		Last Modified: Wed, 08 Oct 2025 21:31:15 GMT  
		Size: 2.0 MB (1991055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8573d5df234537883a638f95501925286c3367fd1cc40a4c6a80b70ef59ffa16`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd6f77485828d14a277cde4d3649153b058047ad8477c919e974016eb3ef6f7`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b47c7c82754dea9552416b18a213b43d6824105eb9a0318e31789b64ebb4524a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 KB (117055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc0f98e226622d3dd6ab1b57679deaa27c10decc2a26c0d7c64feeeae3b6e18`

```dockerfile
```

-	Layers:
	-	`sha256:949b28585bcee0143420765476ff3f8231f4f8049c4d0b3136c102cc9a3b272f`  
		Last Modified: Thu, 09 Oct 2025 00:34:49 GMT  
		Size: 96.3 KB (96284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c10e36727f7634ae28cb6de04bff91b38d77420fce24cf9b31503d14aff0636`  
		Last Modified: Thu, 09 Oct 2025 00:34:50 GMT  
		Size: 20.8 KB (20771 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:3dbd66df3fa527ea9d5ef8e15484f90fd2bc4445e9d21ad40602c7d954a57c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5692091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa2b9eb15af4ed95101c0752bbde283e07e28adfed081d3a9a731aa82d1ab68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5efc90d716eb56816bbbf625c914fe13450e5c8059469e05eaef18ddf200fd`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795865ca1e6e3ac4e3ed32dabe363301a453512615868e180c6c23f28f711154`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 109.5 KB (109526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f93c274afbe9d7756256b49ac152cdbd8b21b7bf4c0e1a564bf36c6940e986e`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 2.0 MB (1962279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8db2caca7c819c90101fe1d4c62396dd78bf9677be35f005e0026d6b76c095`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d53143d130829def781c84b33cfc19fa4ac216deae7acd8c510186dd525afdb`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c7b1229c17eb2270b6a966423e63e1ad70b16a7c79c87d2ea9df82f9d733d383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 KB (116649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392076445efbd53c3eea2f14c49336ed1c8f521c209369edbb2e7686671c310a`

```dockerfile
```

-	Layers:
	-	`sha256:e91e563cbe752ee16efaa2007b7b0f49392b0f5326018a94f34a2e187c1cb743`  
		Last Modified: Wed, 08 Oct 2025 21:34:33 GMT  
		Size: 96.1 KB (96135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:207733714725a312d472d7f8657279033f48a213756c3f87714f3b4bd3e03195`  
		Last Modified: Wed, 08 Oct 2025 21:34:34 GMT  
		Size: 20.5 KB (20514 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:7e2b422eba145439e8c30b7e3191cc1f8498a721f4ca3d90c31fbc5ed80aee7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5951257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48257955bab73ec394b46e2350210da8ec488c125ff0c7cb4ce03893fff291d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8caf4ead4d89e7cb932248ec2c3e7ae5ee7efb8989eb2ab51d407f7094fe6bf`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff948909dcd7ac6c4301b934b30465617e899ca99e5cb6ac6e537be4e6f6144`  
		Last Modified: Thu, 09 Oct 2025 01:11:40 GMT  
		Size: 124.3 KB (124318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f700c3c0f9d01825484f8ddf4ea689855d4c1ed78848558c4c2bf8bf817caed0`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 2.1 MB (2093342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ee4b65e8fe80e2ad3919c8c15d8855829430a43445decbd73237095a9771a9`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06240440b6e443402b0a5ca4dc97a2225661f3da03b4c6bc67c2e9443ba95ce4`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ea61cc67a9e9ffc7a8aaf326e701ea53f5d074dc907d4ad89b4274c4cb8ce804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213afd703e8e97590346c2a301a08bd84f590c17e18aefcbcdefc4d93622c57b`

```dockerfile
```

-	Layers:
	-	`sha256:d3b5325b8aa7c43ef1c7b6f6f4a09cbcfd07d64d439c41a950bc41da09e060ff`  
		Last Modified: Thu, 09 Oct 2025 03:34:33 GMT  
		Size: 94.3 KB (94287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dd52654f2c500e460030d1f9328acbf6d095a5e2d004a4f6417b79522c7fddf`  
		Last Modified: Thu, 09 Oct 2025 03:34:34 GMT  
		Size: 20.6 KB (20647 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:588117152fae8688e5cee8aa65963a1adb1e3851845da5da3e18c80099cdb1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5559076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c983e214f48d62c0be8ffbceb2a86b504aa71c02ac195047119fe264f612c35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ec1911f91425f5b1fc00d35f661d0dcb2691cdbff9a0ea4a65789eb8dd9b89`  
		Last Modified: Thu, 09 Oct 2025 04:54:06 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb577a02d7726836381f3dfcda7cb11472d8e99ef2feb088a9570bc2c0203f15`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 107.9 KB (107909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d6a77fdbd897c87616b71f12d107a1db186b3944ccdad6b89e33186d2645bf`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 1.9 MB (1934579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2879148828c59fde0e744fb56e2490c68a2e98902f3c6a0d01bb8381588a58ba`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00990bf09cdd6c9e756438f8b076739cea749be4889b317c88bf5d06c908e9d8`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:da1dc0b73e866df98aacb962264ed5b50bf3f61862f76c42828b9a179c32e455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b8b102978a5d01b2e4ec0cf55dd00df9776a17f5f31b8bae680908b73d2e1de`

```dockerfile
```

-	Layers:
	-	`sha256:2de1c9249a94130556f0db88a655ed432c15ad40e151579870de604725fbc086`  
		Last Modified: Thu, 09 Oct 2025 06:34:34 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0262f9b3a73d1455147e4436e4bf7da9aa19a7d385d28a807688e23d6a1f1d05`  
		Last Modified: Thu, 09 Oct 2025 06:34:34 GMT  
		Size: 20.6 KB (20648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; s390x

```console
$ docker pull memcached@sha256:ed5969236f4728c97696471e08c88864c21019ea227118b3336d6484ed3e5b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5804524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c049e21de6c2be2f58a69ee9eb633a51a0491febb4b48fa476556586ac0fbd96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d91bfc8fa88993cee87c33ea18494c5e9f0ad8e5b6f644411e9cd648982653`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a682e0d523bab9ef58be0ad290abcee8563e45ceccc9d04fc9b47308aeb709b`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 113.5 KB (113502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9fe3585b1938fd376ffbce3ef824ed7bc20ed49039f98e279ff5ab6159b81e`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 2.0 MB (2040430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9870bcfd315f7fc77b2fb8e80646695f277bc2e7689cf73b395e230aa6fe327c`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20f8ef4bac131999b759bd8b49d1474c540fb1874c8db4e3f4b21a7262b6903`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2d42234a0a18e44870f34c7796f717e9d61b56556ba027f9fae085adfbeeb7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd89a980babfe6204633d40fbc2b82da6c42a3c42f43f980c4d29d3015fd40b`

```dockerfile
```

-	Layers:
	-	`sha256:70fb18f0cec1c9db308335dffc76a505d0855256e74dd6cd73079481cccac057`  
		Last Modified: Thu, 09 Oct 2025 03:34:39 GMT  
		Size: 94.2 KB (94229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02c95a382d7ff8c2fab05ba8609f8b69576ec785d085ed04e606445051336db9`  
		Last Modified: Thu, 09 Oct 2025 03:34:40 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine3.22`

```console
$ docker pull memcached@sha256:7b45203a99eb1419c95b875c7e48c5a9eebc0a305eeb09eefc9f3a2cff758a46
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
$ docker pull memcached@sha256:e319c3f1f6623fb2caedb14c4a5c8594f88736d90dc89d19f1ec11c8533ee263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70bce40b6c41c7484f47d1d51e8be171c582e0b3e18f2379dd66e49e3178d86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c711f2e2fe464121135109729faa513b79413712df200207ef35dfb19e550ca`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0cba00095a1ab15ee2ec0bcefea9c1fe601b9533d47626ab2fb6b74bf8a770`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 104.7 KB (104727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9204d372b3172134a4f3bbcf654ab17d33079a3aff6930e16fa7262df7c9cdbe`  
		Last Modified: Wed, 08 Oct 2025 22:42:05 GMT  
		Size: 2.0 MB (2000281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa9dd6a61433e778f70df6cd37bc70c4dcbfa8e0b0e8b1f9a0fc2f993c78685`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5a283c3ec8e0142f3f4b0b17b2901ab6d7dbff9e3f62bf978a03e5d31833f5`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:1cb56f4b692737cc136d1ff3c5dc0ca16e6b7c3be7023b1a9214348578dc4536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 KB (116754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a7a80cd482b54ecad43450e81b2d6858d2397277cf2d8358315295ef8152dc5`

```dockerfile
```

-	Layers:
	-	`sha256:659cc6afa1cde9acfc6444a310575d263f25f2f83d4987d4fddf83e5bb0d3082`  
		Last Modified: Thu, 09 Oct 2025 00:34:37 GMT  
		Size: 96.2 KB (96180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e43c8201b9a29cba2a3392f6a10e9ee6f0d6295f0248c8d3e9a792871224ec10`  
		Last Modified: Thu, 09 Oct 2025 00:34:38 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.22` - linux; arm variant v6

```console
$ docker pull memcached@sha256:43072fb4c4cfd652bf1a32d617dd81060515017e52b14f35faeb2fe26d071dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5557528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87416926a00e28eb0313c62e942bea0ce0517d67c95df6258358f109a49d392c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd90c0f65a0d79d1685d8fefb0f95b02afd962d0b160a1274598cb584ec37d9`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920bb020947e8d1d3b077c6d9861f8953febeb54f94421c689d40240e56b7ff0`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 101.5 KB (101532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4dc3dc5cf827d37f28e2a9a6758089ff72bc10d1915dbb61cce8f30350de40`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 2.0 MB (1950567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b2afb9c93ba0497cadc25e69b15de772b64456929b70dbe23c7ef54faa3815`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d88088c7b652b283feabfeb2974fb4bd7140ebf7da94c5d502f22841f26eb4a`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:bd27295997fc0e77ad410a3e638c230d83e3d366906a449f5349d8311d72e657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a474656b8df51a30dcb397a44bcb48c6ba3cb76e49cc3a108a15a662cd64c4b`

```dockerfile
```

-	Layers:
	-	`sha256:9a80e6fbb7fc2254a12359760da6745c28fe1d3fa2367b1137aad71c6732a8bd`  
		Last Modified: Thu, 09 Oct 2025 00:34:41 GMT  
		Size: 20.5 KB (20510 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.22` - linux; arm variant v7

```console
$ docker pull memcached@sha256:2caa01f7607cf1d95b2e261de80716a27de4077bf25b9dc623688091b78bf4ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c1be64fe03e8832bc6208dfced118762e57dca6b55b4482140c8fc3b06dfb3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0a02f5bd6bf63e96f5b45eda4849003b01c41b23425e7ac5a77eb01b5391e0`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f277f740301c69a561a94545bc7f140ee2d5f4ea87f88c0c861eb7b4f7983b0`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 91.3 KB (91313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e9ebffe0c4c57cd5b7fd1da1fcc7f14e2e881a81673f81e8bde4bf662a45b3`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 1.9 MB (1909853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46526f6db8416530677567eac97b5cfc18e2b86ec5c930d06de26b62f0c7a5c6`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f19627fe74f6edf1d0aa4deb85d035125067fcd28b2ee240aeb110e48330f19`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:09108dd858c6aae1c834fd9c8a7f9f78e552673ee6296d9f5cf2d84c0c26c6fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 KB (116969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9755e3f89f06272910c7fcbcaf44a3cb373b551f73bc7c9dc6dbffe13aad48`

```dockerfile
```

-	Layers:
	-	`sha256:13ba800aa65c8f207645e4069de55b11ad0a2dc87b951414df4bd35ad3923afd`  
		Last Modified: Thu, 09 Oct 2025 00:34:45 GMT  
		Size: 96.2 KB (96248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:636139066de216a683805bafa6cd72b23f1754f8dd2b5854e61578a684260418`  
		Last Modified: Thu, 09 Oct 2025 00:34:46 GMT  
		Size: 20.7 KB (20721 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:03d8054231ea1bb1dbb54d7e8bb32449b95c35475fa280a9b12d78219822fa48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6251299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42028500064e9ca7d32291ca01c636547943d3a6e6f11b80e503166efcfa6149`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098f75f9dd9f7dbf0e5993587a5b4de796bc9c01f2e795b325f1e22fe66c6833`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4c130fe47b24dbff1989543c440e0d6635524f9bf84473a6dc37472ecacac0`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 120.8 KB (120823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a41614e1c7aff72360936c76c0218330a487dd6ff6779cd243ad1c60ab6634`  
		Last Modified: Wed, 08 Oct 2025 21:31:15 GMT  
		Size: 2.0 MB (1991055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8573d5df234537883a638f95501925286c3367fd1cc40a4c6a80b70ef59ffa16`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd6f77485828d14a277cde4d3649153b058047ad8477c919e974016eb3ef6f7`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:b47c7c82754dea9552416b18a213b43d6824105eb9a0318e31789b64ebb4524a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 KB (117055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc0f98e226622d3dd6ab1b57679deaa27c10decc2a26c0d7c64feeeae3b6e18`

```dockerfile
```

-	Layers:
	-	`sha256:949b28585bcee0143420765476ff3f8231f4f8049c4d0b3136c102cc9a3b272f`  
		Last Modified: Thu, 09 Oct 2025 00:34:49 GMT  
		Size: 96.3 KB (96284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c10e36727f7634ae28cb6de04bff91b38d77420fce24cf9b31503d14aff0636`  
		Last Modified: Thu, 09 Oct 2025 00:34:50 GMT  
		Size: 20.8 KB (20771 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.22` - linux; 386

```console
$ docker pull memcached@sha256:3dbd66df3fa527ea9d5ef8e15484f90fd2bc4445e9d21ad40602c7d954a57c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5692091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa2b9eb15af4ed95101c0752bbde283e07e28adfed081d3a9a731aa82d1ab68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5efc90d716eb56816bbbf625c914fe13450e5c8059469e05eaef18ddf200fd`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795865ca1e6e3ac4e3ed32dabe363301a453512615868e180c6c23f28f711154`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 109.5 KB (109526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f93c274afbe9d7756256b49ac152cdbd8b21b7bf4c0e1a564bf36c6940e986e`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 2.0 MB (1962279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8db2caca7c819c90101fe1d4c62396dd78bf9677be35f005e0026d6b76c095`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d53143d130829def781c84b33cfc19fa4ac216deae7acd8c510186dd525afdb`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:c7b1229c17eb2270b6a966423e63e1ad70b16a7c79c87d2ea9df82f9d733d383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 KB (116649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392076445efbd53c3eea2f14c49336ed1c8f521c209369edbb2e7686671c310a`

```dockerfile
```

-	Layers:
	-	`sha256:e91e563cbe752ee16efaa2007b7b0f49392b0f5326018a94f34a2e187c1cb743`  
		Last Modified: Wed, 08 Oct 2025 21:34:33 GMT  
		Size: 96.1 KB (96135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:207733714725a312d472d7f8657279033f48a213756c3f87714f3b4bd3e03195`  
		Last Modified: Wed, 08 Oct 2025 21:34:34 GMT  
		Size: 20.5 KB (20514 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.22` - linux; ppc64le

```console
$ docker pull memcached@sha256:7e2b422eba145439e8c30b7e3191cc1f8498a721f4ca3d90c31fbc5ed80aee7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5951257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48257955bab73ec394b46e2350210da8ec488c125ff0c7cb4ce03893fff291d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8caf4ead4d89e7cb932248ec2c3e7ae5ee7efb8989eb2ab51d407f7094fe6bf`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff948909dcd7ac6c4301b934b30465617e899ca99e5cb6ac6e537be4e6f6144`  
		Last Modified: Thu, 09 Oct 2025 01:11:40 GMT  
		Size: 124.3 KB (124318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f700c3c0f9d01825484f8ddf4ea689855d4c1ed78848558c4c2bf8bf817caed0`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 2.1 MB (2093342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ee4b65e8fe80e2ad3919c8c15d8855829430a43445decbd73237095a9771a9`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06240440b6e443402b0a5ca4dc97a2225661f3da03b4c6bc67c2e9443ba95ce4`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:ea61cc67a9e9ffc7a8aaf326e701ea53f5d074dc907d4ad89b4274c4cb8ce804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213afd703e8e97590346c2a301a08bd84f590c17e18aefcbcdefc4d93622c57b`

```dockerfile
```

-	Layers:
	-	`sha256:d3b5325b8aa7c43ef1c7b6f6f4a09cbcfd07d64d439c41a950bc41da09e060ff`  
		Last Modified: Thu, 09 Oct 2025 03:34:33 GMT  
		Size: 94.3 KB (94287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dd52654f2c500e460030d1f9328acbf6d095a5e2d004a4f6417b79522c7fddf`  
		Last Modified: Thu, 09 Oct 2025 03:34:34 GMT  
		Size: 20.6 KB (20647 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.22` - linux; riscv64

```console
$ docker pull memcached@sha256:588117152fae8688e5cee8aa65963a1adb1e3851845da5da3e18c80099cdb1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5559076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c983e214f48d62c0be8ffbceb2a86b504aa71c02ac195047119fe264f612c35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ec1911f91425f5b1fc00d35f661d0dcb2691cdbff9a0ea4a65789eb8dd9b89`  
		Last Modified: Thu, 09 Oct 2025 04:54:06 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb577a02d7726836381f3dfcda7cb11472d8e99ef2feb088a9570bc2c0203f15`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 107.9 KB (107909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d6a77fdbd897c87616b71f12d107a1db186b3944ccdad6b89e33186d2645bf`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 1.9 MB (1934579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2879148828c59fde0e744fb56e2490c68a2e98902f3c6a0d01bb8381588a58ba`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00990bf09cdd6c9e756438f8b076739cea749be4889b317c88bf5d06c908e9d8`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:da1dc0b73e866df98aacb962264ed5b50bf3f61862f76c42828b9a179c32e455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b8b102978a5d01b2e4ec0cf55dd00df9776a17f5f31b8bae680908b73d2e1de`

```dockerfile
```

-	Layers:
	-	`sha256:2de1c9249a94130556f0db88a655ed432c15ad40e151579870de604725fbc086`  
		Last Modified: Thu, 09 Oct 2025 06:34:34 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0262f9b3a73d1455147e4436e4bf7da9aa19a7d385d28a807688e23d6a1f1d05`  
		Last Modified: Thu, 09 Oct 2025 06:34:34 GMT  
		Size: 20.6 KB (20648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.22` - linux; s390x

```console
$ docker pull memcached@sha256:ed5969236f4728c97696471e08c88864c21019ea227118b3336d6484ed3e5b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5804524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c049e21de6c2be2f58a69ee9eb633a51a0491febb4b48fa476556586ac0fbd96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
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
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d91bfc8fa88993cee87c33ea18494c5e9f0ad8e5b6f644411e9cd648982653`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a682e0d523bab9ef58be0ad290abcee8563e45ceccc9d04fc9b47308aeb709b`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 113.5 KB (113502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9fe3585b1938fd376ffbce3ef824ed7bc20ed49039f98e279ff5ab6159b81e`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 2.0 MB (2040430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9870bcfd315f7fc77b2fb8e80646695f277bc2e7689cf73b395e230aa6fe327c`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20f8ef4bac131999b759bd8b49d1474c540fb1874c8db4e3f4b21a7262b6903`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:2d42234a0a18e44870f34c7796f717e9d61b56556ba027f9fae085adfbeeb7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd89a980babfe6204633d40fbc2b82da6c42a3c42f43f980c4d29d3015fd40b`

```dockerfile
```

-	Layers:
	-	`sha256:70fb18f0cec1c9db308335dffc76a505d0855256e74dd6cd73079481cccac057`  
		Last Modified: Thu, 09 Oct 2025 03:34:39 GMT  
		Size: 94.2 KB (94229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02c95a382d7ff8c2fab05ba8609f8b69576ec785d085ed04e606445051336db9`  
		Last Modified: Thu, 09 Oct 2025 03:34:40 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:latest`

```console
$ docker pull memcached@sha256:050de63e6c082df85f93ffed9c388004b3c6257a06f1904e8628a6f87658eb99
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
$ docker pull memcached@sha256:04cfb7a52848a5ddab7b57674b37c9b7b392d93ec11f0c9a4c300a9bbd1c19a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32209888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0b3dcfe086b67312e8b165a92d8e71b517bf64b356c0c804270d2330e2577c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:05:54 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 04:05:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:08:37 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 04:08:37 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 04:08:37 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 04:08:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 04:08:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:08:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 04:08:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 04:08:38 GMT
USER memcache
# Tue, 04 Nov 2025 04:08:38 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 04:08:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95dd2497c5fb854f1d1cb6790613048eae391c70dd7fe1d2c54ea024889782ad`  
		Last Modified: Tue, 04 Nov 2025 04:08:50 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5e80885bbbbd2ccaf87a97c9f6da9eb3a9b7395ce5e2b73a110224cfbcfb1e`  
		Last Modified: Tue, 04 Nov 2025 04:08:50 GMT  
		Size: 136.6 KB (136597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be7e82464812bb6ab2d37c74a6636ec8d73ec4154a192a75342dfa2f64cc8da`  
		Last Modified: Tue, 04 Nov 2025 04:08:50 GMT  
		Size: 2.3 MB (2293674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18ba826b4b67fa295ff82d2b102a5f2db243fabcb7cc2acac6cc3c33a1cbf4a`  
		Last Modified: Tue, 04 Nov 2025 04:08:50 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654bd5f6e9c2c18716bbdc27ac8f5eab96044427da57f1cb8ee268d2cd3b5f03`  
		Last Modified: Tue, 04 Nov 2025 04:08:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:b78568d9b4a4cd24bae6187909a2a4a808abc29638602ee6aac1885173203e35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b08f68a528f6821adc34258cb89e510c9bf97f5596cf2e47ce7b30ba202cea`

```dockerfile
```

-	Layers:
	-	`sha256:549c9101b19d3697bed0386c9c6378a334bce6d392f694130d47f2033273b571`  
		Last Modified: Tue, 04 Nov 2025 10:34:35 GMT  
		Size: 2.0 MB (2008234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26c87354a983796083082c9e84ccf372217e5a602e78aefdec01fc26eae125ce`  
		Last Modified: Tue, 04 Nov 2025 10:34:36 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:cfd8f3dc480855d184b335ea9b7c334731ce495de10ef2f2f17b4f82bedf1965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30319386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4fa3d1c819bb913d28b672eedf487f5165ff2dc4e5968326e550efb418196ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 00:24:40 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 00:24:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:28:01 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 00:28:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 00:28:01 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 00:28:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 00:28:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:28:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 00:28:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:28:01 GMT
USER memcache
# Tue, 04 Nov 2025 00:28:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 00:28:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:453afc2258d7bc5729fed5672fb95bafa092e30a933b4377a12034be940a671b`  
		Last Modified: Tue, 04 Nov 2025 00:13:12 GMT  
		Size: 27.9 MB (27946438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3da1461ffd1574069e2ddea407a8d31a9f215a260352498c03bb19d38c7d7ca`  
		Last Modified: Tue, 04 Nov 2025 00:28:13 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4066eb4ba0932fcecba129384e7059abaee0e303654cc15d444f8c6aa11e69bf`  
		Last Modified: Tue, 04 Nov 2025 00:28:13 GMT  
		Size: 144.0 KB (144040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f429e8aa4399dcb073c93dceeb4c04af1a46da5d750c71a36dcff1a94ab840`  
		Last Modified: Tue, 04 Nov 2025 00:28:13 GMT  
		Size: 2.2 MB (2227397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100f4b89d2a8997d39ef62d45e5590e944f3120ba301e303025c7ccaac6da369`  
		Last Modified: Tue, 04 Nov 2025 00:28:13 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334cb0302a41a8c70f7874d7de08c32eb550581a5fc8b17c9b565b9cecdb8149`  
		Last Modified: Tue, 04 Nov 2025 00:28:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:281d772292417096430072e287dae06f36229ebd35a2c308d81eccc1862e99bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956875d70010cc91e002ae89b4a07ce9edfc12bc2a743b377162df7dd92e6f05`

```dockerfile
```

-	Layers:
	-	`sha256:c19709d33e93cfcba6b59a36ac6efba06597c00114be0ab5c2aaddf33ee8ba33`  
		Last Modified: Tue, 04 Nov 2025 07:34:24 GMT  
		Size: 2.0 MB (2011237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a60d569262f9d2f585a47be2ccf35c498002df82c55fd19ebcbaea6f9cd101f9`  
		Last Modified: Tue, 04 Nov 2025 07:34:25 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v7

```console
$ docker pull memcached@sha256:fb4a02a784ff9c44adb4a72aa161b935ed3bd148e49b37fc5e68a1f3aa30a87d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28532441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e70b324b1a195c841f52ba1facea8f75482e1bb049f38d17f8a8b69185f65166`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:06:51 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 02:06:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:09:59 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 02:09:59 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 02:09:59 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 02:09:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 02:09:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 02:09:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 02:09:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 02:09:59 GMT
USER memcache
# Tue, 04 Nov 2025 02:09:59 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 02:09:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f9bebc6d7be8fb19e90bd816cf5ea46e325d9d8d019345bd7e83bb27165e1c`  
		Last Modified: Tue, 04 Nov 2025 02:10:11 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d87b4f74b7b681280e1de65d55c7fef9af3294203ca9753541c48a7dbd67ac`  
		Last Modified: Tue, 04 Nov 2025 02:10:11 GMT  
		Size: 135.3 KB (135301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012aaeffd16b06fc90dbc9cf1682d2a8cb96482af9e0582ebc1dc6881617ba3d`  
		Last Modified: Tue, 04 Nov 2025 02:10:11 GMT  
		Size: 2.2 MB (2182590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30071a0aa370d64f866b34ab3ab9ed0d6e2f30dee5e631bc9b787ff5a9f4fdc0`  
		Last Modified: Tue, 04 Nov 2025 02:10:11 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18d6989abdf4813c6c982f04f7bc42405ebe217f82671824a3bd75a1f923f9c`  
		Last Modified: Tue, 04 Nov 2025 02:10:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:672ae9e81bd13a12a5ae6790d4619294b51a1cfd04a6af50c523797512fc75f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95641a91a03ab503b7750055d3fe6cf1474b1c75ce6288b8966a514375dddb1a`

```dockerfile
```

-	Layers:
	-	`sha256:f13ec9279ccf6461d334439358fdee3b542d225588c6a3857991636d57ce10ee`  
		Last Modified: Tue, 04 Nov 2025 10:34:42 GMT  
		Size: 2.0 MB (2009694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37374c73a31babc67e99ab9936b2166b55c09c55f1bc4cfff80e65a3c40d5425`  
		Last Modified: Tue, 04 Nov 2025 10:34:43 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:bc5ac38c2657d7c6d375374985e9293fb3744a75edbd96cb7a7524cc14c95d08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32572446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1f397ae776296a0fd6edeebc664c5cc9fbc3f08556289a5a1fe41c75626d379`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:17:41 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 01:17:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:20:41 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 01:20:41 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 01:20:41 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 01:20:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 01:20:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:20:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 01:20:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:20:41 GMT
USER memcache
# Tue, 04 Nov 2025 01:20:41 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 01:20:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db64d9b58942143a8d96f7823245feb1d4bf27c04222e71dbe7cedfce33d7e7f`  
		Last Modified: Tue, 04 Nov 2025 01:20:54 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e45c84ea5c10a0167bca67aede44a66fd08b708143ccb896170e30885ea50f1`  
		Last Modified: Tue, 04 Nov 2025 01:20:54 GMT  
		Size: 153.4 KB (153400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317fc2721e7de3ecc81d907c076c0de0aa0c4a80a7810a77e53335eab94adedc`  
		Last Modified: Tue, 04 Nov 2025 01:20:54 GMT  
		Size: 2.3 MB (2275238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a6f24d2569f3c38db7873c0a8f3942c5c7b876fa9eff4eaeca997bc6dc28df`  
		Last Modified: Tue, 04 Nov 2025 01:20:54 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d9e0c677fc63b66e178f9171abc553450378c9046b77cbcc52126068101766c`  
		Last Modified: Tue, 04 Nov 2025 01:20:54 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:8d2e6520d11120bd0b01076b34657bd1b1a785b38c6f7048bc58db91821f584f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97a00b54cc845295e717a2bf8ba5f7b91d5fb25acd85c6c399b94596dd67465`

```dockerfile
```

-	Layers:
	-	`sha256:7061efa09aee437d8b815835ea3f0afa471b9f76cb95323b8260dc846c1f49f1`  
		Last Modified: Tue, 04 Nov 2025 10:34:47 GMT  
		Size: 2.0 MB (2008550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0254e16c47bdde3eb7e8d57383df36625fad7398861b5aca562e447505806a8`  
		Last Modified: Tue, 04 Nov 2025 10:34:47 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:e950b4f76df4b7ad0e9dcc9f2357df6ae35314e232ad23b0ec4fb3c3beb2b84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33688177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9910abbdac4661a59a1d8fe6b43f96cd0abdde92371f8c995e7216d706f375bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:19:48 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 01:19:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:22:46 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 01:22:46 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 01:22:46 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 01:22:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 01:22:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:22:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 01:22:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:22:46 GMT
USER memcache
# Tue, 04 Nov 2025 01:22:46 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 01:22:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7f24a3a0c200106d0d9ab7b6264e50c689910154fb57bf08185b9eaf995db758`  
		Last Modified: Tue, 04 Nov 2025 00:13:54 GMT  
		Size: 31.3 MB (31294783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6840654bcf5429c7954c0483368ccd033e4222b3098ca64904c590f04dd07624`  
		Last Modified: Tue, 04 Nov 2025 01:22:59 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66205a10db2dcede178afb15530db6f282ec7194f11ffe734d9496d8b30e35a2`  
		Last Modified: Tue, 04 Nov 2025 01:22:59 GMT  
		Size: 147.4 KB (147440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b63b70a9c43a2f37c5f37f50e2aaf507c970f0133b7aaaea29fdb4e826c18b1`  
		Last Modified: Tue, 04 Nov 2025 01:23:00 GMT  
		Size: 2.2 MB (2244441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a3c1d29eba0037255cb4c7903d5de630770804520cfdb28ce05b112d526ed3`  
		Last Modified: Tue, 04 Nov 2025 01:22:59 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8da84bbfbc97884490625408deb986e43d5843e48291516064a41ab6d5963e`  
		Last Modified: Tue, 04 Nov 2025 01:22:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:51b41d632670fe8c786707c7977f9136c593c137bcde08516527421769778ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7473e22367c8e8c736bb1ce76169b1b4abf93fa0b057dec9103c4dccf90efc2`

```dockerfile
```

-	Layers:
	-	`sha256:f90631de8235b43d3b44250b8606b5783cd39dc12e9810fb5993f82a19dfe2ee`  
		Last Modified: Tue, 04 Nov 2025 10:34:51 GMT  
		Size: 2.0 MB (2005391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29d51086244a15fe10ebfe78e299fc7a89dd09601c8753741004d27949898c16`  
		Last Modified: Tue, 04 Nov 2025 10:34:52 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:ead041ea0e5c06d481ac304f7b4076a3339d849fcdffa3d25603418dc2fe82e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36187425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b0128aff763178ac8bb867e486c2450bacad45f79a5ff629194be435141070`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:52:27 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 01:52:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:55:40 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 01:55:40 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 01:55:40 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 01:55:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 01:55:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:55:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 01:55:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:55:41 GMT
USER memcache
# Tue, 04 Nov 2025 01:55:41 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 01:55:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126ce0c080daa81edc8784c59f60350b32083b3201304709775cf554155f80af`  
		Last Modified: Tue, 04 Nov 2025 01:56:04 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4c9857fe1f3ded2ba6c29c2f9591c7f5b2bfc46517527fac13f4c2b539a9a4`  
		Last Modified: Tue, 04 Nov 2025 01:56:04 GMT  
		Size: 170.2 KB (170244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e15beeee778428c51e89d0b8c3d6ca7931f0324e0a66f6b2bf85b101e9674a`  
		Last Modified: Tue, 04 Nov 2025 01:56:04 GMT  
		Size: 2.4 MB (2417022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d427e3c140105cfdb1a22a00010621a5a0834ce00ba3ea1059f8a63d8b0f5ee5`  
		Last Modified: Tue, 04 Nov 2025 01:56:04 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dfc7efa96996e95dcf030731f854bc07f2c7aa3349e75c4e74c04d924b3c62`  
		Last Modified: Tue, 04 Nov 2025 01:56:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:ad9b48a87b820bbf6c20cb57cd2247fa75ca6de00df26576f784a8f51703c571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1582395261fcee60bb7362c6cff0abd1d7325b4fde3cd609ac637f76aaa7ea5`

```dockerfile
```

-	Layers:
	-	`sha256:f5e9fbdfb8deeebb9142cd4facdedb0629028f8343a64b1e13d26ecb035f3c84`  
		Last Modified: Tue, 04 Nov 2025 10:34:55 GMT  
		Size: 2.0 MB (2011835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3dd30af34832aa3d277b4b6882a9786e4225d5a7387d5af5a66cadc59adc22d`  
		Last Modified: Tue, 04 Nov 2025 10:34:56 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; riscv64

```console
$ docker pull memcached@sha256:56542c7304b39c7980a644419d2ab6f603477cc9e1cb9c575d45b8c4220e0c6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30630140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e279bc62f41c4006902271742290cdde9d77c2121c1b4db697d09d01c690860e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 03:30:39 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 03:31:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:44:44 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 03:44:44 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 03:44:44 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 03:44:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 03:44:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 03:44:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 03:44:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 03:44:45 GMT
USER memcache
# Tue, 04 Nov 2025 03:44:45 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 03:44:45 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b836efb62045adb472c559fe0a4cedfe183f60ae9e36defd9b46efc4886fff56`  
		Last Modified: Tue, 04 Nov 2025 03:45:39 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db437579ba55d9291ad05cd904e857adb520e8189f0cc2fb207b475c10a95ee`  
		Last Modified: Tue, 04 Nov 2025 03:45:39 GMT  
		Size: 133.0 KB (132994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ca1f664c3ee469c225e4241d90dabf5a36c9fd5282ec51011fe16b9fcd5882`  
		Last Modified: Tue, 04 Nov 2025 03:45:39 GMT  
		Size: 2.2 MB (2219849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f5b56363e737d5d4b276274dc82b3ae7d3772bb1d6cadc5fb0c117ad6d004e`  
		Last Modified: Tue, 04 Nov 2025 03:45:39 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92139c3e4198e9ce61d77b8a86d621938a3390898a4ac22ba81eefd286a78cc7`  
		Last Modified: Tue, 04 Nov 2025 03:45:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:a72757dfcc56cb3edf581d72aa35ca18e099d18284ccfaabc697a74b2d7c2399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40a19d13356829e752dd3f0c530a1f2ef0abfc0ca53d29d3d74e1840a1698892`

```dockerfile
```

-	Layers:
	-	`sha256:78add421d4e1ac7755ca522075904f0acd06a15e1c8b9ca1bb0047a7d3ebf187`  
		Last Modified: Tue, 04 Nov 2025 07:34:38 GMT  
		Size: 2.0 MB (2002198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f1fc3731e375af1e0712ec91b83487acb49e907a1168f593f251fe43cb51fb9`  
		Last Modified: Tue, 04 Nov 2025 07:34:39 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:3de73b4ecf32984b0c6603b973257071c81c94af8351b35aa4343407c7315726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32293163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e6900a4460f82b0703aed07dde3c1722bdb7919a582b6b1f22a9ca701cb510f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 06:58:32 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 06:58:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 07:02:23 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 07:02:23 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 07:02:23 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 07:02:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 07:02:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 07:02:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 07:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 07:02:23 GMT
USER memcache
# Tue, 04 Nov 2025 07:02:23 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 07:02:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17527924bc8c8387e810ff986ddbe9998a0b5d55a4850b90b4cea0a897c94a09`  
		Last Modified: Tue, 04 Nov 2025 07:02:40 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54fd3d90bab9e973d6a8c142df91794bdc213e5bafe8926a58809036e1ee1f5`  
		Last Modified: Tue, 04 Nov 2025 07:02:40 GMT  
		Size: 140.4 KB (140429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc993f31fbd52e75a8dfc710d94d4130a8c228be35b7737c5950a5f93a1125a`  
		Last Modified: Tue, 04 Nov 2025 07:02:40 GMT  
		Size: 2.3 MB (2313833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acaa055d548771aab19234adcaf5b3ed727ee85214c303e1035e3e464e0fbda0`  
		Last Modified: Tue, 04 Nov 2025 07:02:40 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c2e1b3aad04d0544265917caef9c91d5ed4496376262541974a707026847f4`  
		Last Modified: Tue, 04 Nov 2025 07:02:40 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:414b070c237a13d5dee83e1db26eb0f953dd5af0753013a8bbd988611aa90e89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5cc4920f789bfe656195ac67c3ddd1a00030591f92b5ac4dc2b0e9dcdd2a0b`

```dockerfile
```

-	Layers:
	-	`sha256:b242fd5db27262af27c5589b736a5ae9f234cb03765c59c73e64818c1cade0c8`  
		Last Modified: Tue, 04 Nov 2025 10:35:02 GMT  
		Size: 2.0 MB (2009671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e15d059f16d47b54c3d82bdf997670c62a062815b64d7e7b486d8de0060691b4`  
		Last Modified: Tue, 04 Nov 2025 10:35:03 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:trixie`

```console
$ docker pull memcached@sha256:050de63e6c082df85f93ffed9c388004b3c6257a06f1904e8628a6f87658eb99
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
$ docker pull memcached@sha256:04cfb7a52848a5ddab7b57674b37c9b7b392d93ec11f0c9a4c300a9bbd1c19a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32209888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0b3dcfe086b67312e8b165a92d8e71b517bf64b356c0c804270d2330e2577c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:05:54 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 04:05:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:08:37 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 04:08:37 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 04:08:37 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 04:08:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 04:08:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:08:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 04:08:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 04:08:38 GMT
USER memcache
# Tue, 04 Nov 2025 04:08:38 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 04:08:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95dd2497c5fb854f1d1cb6790613048eae391c70dd7fe1d2c54ea024889782ad`  
		Last Modified: Tue, 04 Nov 2025 04:08:50 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5e80885bbbbd2ccaf87a97c9f6da9eb3a9b7395ce5e2b73a110224cfbcfb1e`  
		Last Modified: Tue, 04 Nov 2025 04:08:50 GMT  
		Size: 136.6 KB (136597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be7e82464812bb6ab2d37c74a6636ec8d73ec4154a192a75342dfa2f64cc8da`  
		Last Modified: Tue, 04 Nov 2025 04:08:50 GMT  
		Size: 2.3 MB (2293674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18ba826b4b67fa295ff82d2b102a5f2db243fabcb7cc2acac6cc3c33a1cbf4a`  
		Last Modified: Tue, 04 Nov 2025 04:08:50 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654bd5f6e9c2c18716bbdc27ac8f5eab96044427da57f1cb8ee268d2cd3b5f03`  
		Last Modified: Tue, 04 Nov 2025 04:08:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:b78568d9b4a4cd24bae6187909a2a4a808abc29638602ee6aac1885173203e35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b08f68a528f6821adc34258cb89e510c9bf97f5596cf2e47ce7b30ba202cea`

```dockerfile
```

-	Layers:
	-	`sha256:549c9101b19d3697bed0386c9c6378a334bce6d392f694130d47f2033273b571`  
		Last Modified: Tue, 04 Nov 2025 10:34:35 GMT  
		Size: 2.0 MB (2008234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26c87354a983796083082c9e84ccf372217e5a602e78aefdec01fc26eae125ce`  
		Last Modified: Tue, 04 Nov 2025 10:34:36 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:cfd8f3dc480855d184b335ea9b7c334731ce495de10ef2f2f17b4f82bedf1965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30319386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4fa3d1c819bb913d28b672eedf487f5165ff2dc4e5968326e550efb418196ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 00:24:40 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 00:24:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:28:01 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 00:28:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 00:28:01 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 00:28:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 00:28:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:28:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 00:28:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:28:01 GMT
USER memcache
# Tue, 04 Nov 2025 00:28:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 00:28:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:453afc2258d7bc5729fed5672fb95bafa092e30a933b4377a12034be940a671b`  
		Last Modified: Tue, 04 Nov 2025 00:13:12 GMT  
		Size: 27.9 MB (27946438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3da1461ffd1574069e2ddea407a8d31a9f215a260352498c03bb19d38c7d7ca`  
		Last Modified: Tue, 04 Nov 2025 00:28:13 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4066eb4ba0932fcecba129384e7059abaee0e303654cc15d444f8c6aa11e69bf`  
		Last Modified: Tue, 04 Nov 2025 00:28:13 GMT  
		Size: 144.0 KB (144040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f429e8aa4399dcb073c93dceeb4c04af1a46da5d750c71a36dcff1a94ab840`  
		Last Modified: Tue, 04 Nov 2025 00:28:13 GMT  
		Size: 2.2 MB (2227397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100f4b89d2a8997d39ef62d45e5590e944f3120ba301e303025c7ccaac6da369`  
		Last Modified: Tue, 04 Nov 2025 00:28:13 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334cb0302a41a8c70f7874d7de08c32eb550581a5fc8b17c9b565b9cecdb8149`  
		Last Modified: Tue, 04 Nov 2025 00:28:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:281d772292417096430072e287dae06f36229ebd35a2c308d81eccc1862e99bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956875d70010cc91e002ae89b4a07ce9edfc12bc2a743b377162df7dd92e6f05`

```dockerfile
```

-	Layers:
	-	`sha256:c19709d33e93cfcba6b59a36ac6efba06597c00114be0ab5c2aaddf33ee8ba33`  
		Last Modified: Tue, 04 Nov 2025 07:34:24 GMT  
		Size: 2.0 MB (2011237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a60d569262f9d2f585a47be2ccf35c498002df82c55fd19ebcbaea6f9cd101f9`  
		Last Modified: Tue, 04 Nov 2025 07:34:25 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:fb4a02a784ff9c44adb4a72aa161b935ed3bd148e49b37fc5e68a1f3aa30a87d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28532441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e70b324b1a195c841f52ba1facea8f75482e1bb049f38d17f8a8b69185f65166`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:06:51 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 02:06:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:09:59 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 02:09:59 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 02:09:59 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 02:09:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 02:09:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 02:09:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 02:09:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 02:09:59 GMT
USER memcache
# Tue, 04 Nov 2025 02:09:59 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 02:09:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f9bebc6d7be8fb19e90bd816cf5ea46e325d9d8d019345bd7e83bb27165e1c`  
		Last Modified: Tue, 04 Nov 2025 02:10:11 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d87b4f74b7b681280e1de65d55c7fef9af3294203ca9753541c48a7dbd67ac`  
		Last Modified: Tue, 04 Nov 2025 02:10:11 GMT  
		Size: 135.3 KB (135301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012aaeffd16b06fc90dbc9cf1682d2a8cb96482af9e0582ebc1dc6881617ba3d`  
		Last Modified: Tue, 04 Nov 2025 02:10:11 GMT  
		Size: 2.2 MB (2182590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30071a0aa370d64f866b34ab3ab9ed0d6e2f30dee5e631bc9b787ff5a9f4fdc0`  
		Last Modified: Tue, 04 Nov 2025 02:10:11 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18d6989abdf4813c6c982f04f7bc42405ebe217f82671824a3bd75a1f923f9c`  
		Last Modified: Tue, 04 Nov 2025 02:10:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:672ae9e81bd13a12a5ae6790d4619294b51a1cfd04a6af50c523797512fc75f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95641a91a03ab503b7750055d3fe6cf1474b1c75ce6288b8966a514375dddb1a`

```dockerfile
```

-	Layers:
	-	`sha256:f13ec9279ccf6461d334439358fdee3b542d225588c6a3857991636d57ce10ee`  
		Last Modified: Tue, 04 Nov 2025 10:34:42 GMT  
		Size: 2.0 MB (2009694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37374c73a31babc67e99ab9936b2166b55c09c55f1bc4cfff80e65a3c40d5425`  
		Last Modified: Tue, 04 Nov 2025 10:34:43 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:bc5ac38c2657d7c6d375374985e9293fb3744a75edbd96cb7a7524cc14c95d08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32572446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1f397ae776296a0fd6edeebc664c5cc9fbc3f08556289a5a1fe41c75626d379`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:17:41 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 01:17:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:20:41 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 01:20:41 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 01:20:41 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 01:20:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 01:20:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:20:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 01:20:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:20:41 GMT
USER memcache
# Tue, 04 Nov 2025 01:20:41 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 01:20:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db64d9b58942143a8d96f7823245feb1d4bf27c04222e71dbe7cedfce33d7e7f`  
		Last Modified: Tue, 04 Nov 2025 01:20:54 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e45c84ea5c10a0167bca67aede44a66fd08b708143ccb896170e30885ea50f1`  
		Last Modified: Tue, 04 Nov 2025 01:20:54 GMT  
		Size: 153.4 KB (153400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317fc2721e7de3ecc81d907c076c0de0aa0c4a80a7810a77e53335eab94adedc`  
		Last Modified: Tue, 04 Nov 2025 01:20:54 GMT  
		Size: 2.3 MB (2275238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a6f24d2569f3c38db7873c0a8f3942c5c7b876fa9eff4eaeca997bc6dc28df`  
		Last Modified: Tue, 04 Nov 2025 01:20:54 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d9e0c677fc63b66e178f9171abc553450378c9046b77cbcc52126068101766c`  
		Last Modified: Tue, 04 Nov 2025 01:20:54 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:8d2e6520d11120bd0b01076b34657bd1b1a785b38c6f7048bc58db91821f584f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97a00b54cc845295e717a2bf8ba5f7b91d5fb25acd85c6c399b94596dd67465`

```dockerfile
```

-	Layers:
	-	`sha256:7061efa09aee437d8b815835ea3f0afa471b9f76cb95323b8260dc846c1f49f1`  
		Last Modified: Tue, 04 Nov 2025 10:34:47 GMT  
		Size: 2.0 MB (2008550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0254e16c47bdde3eb7e8d57383df36625fad7398861b5aca562e447505806a8`  
		Last Modified: Tue, 04 Nov 2025 10:34:47 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; 386

```console
$ docker pull memcached@sha256:e950b4f76df4b7ad0e9dcc9f2357df6ae35314e232ad23b0ec4fb3c3beb2b84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33688177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9910abbdac4661a59a1d8fe6b43f96cd0abdde92371f8c995e7216d706f375bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:19:48 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 01:19:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:22:46 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 01:22:46 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 01:22:46 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 01:22:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 01:22:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:22:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 01:22:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:22:46 GMT
USER memcache
# Tue, 04 Nov 2025 01:22:46 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 01:22:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7f24a3a0c200106d0d9ab7b6264e50c689910154fb57bf08185b9eaf995db758`  
		Last Modified: Tue, 04 Nov 2025 00:13:54 GMT  
		Size: 31.3 MB (31294783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6840654bcf5429c7954c0483368ccd033e4222b3098ca64904c590f04dd07624`  
		Last Modified: Tue, 04 Nov 2025 01:22:59 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66205a10db2dcede178afb15530db6f282ec7194f11ffe734d9496d8b30e35a2`  
		Last Modified: Tue, 04 Nov 2025 01:22:59 GMT  
		Size: 147.4 KB (147440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b63b70a9c43a2f37c5f37f50e2aaf507c970f0133b7aaaea29fdb4e826c18b1`  
		Last Modified: Tue, 04 Nov 2025 01:23:00 GMT  
		Size: 2.2 MB (2244441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a3c1d29eba0037255cb4c7903d5de630770804520cfdb28ce05b112d526ed3`  
		Last Modified: Tue, 04 Nov 2025 01:22:59 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8da84bbfbc97884490625408deb986e43d5843e48291516064a41ab6d5963e`  
		Last Modified: Tue, 04 Nov 2025 01:22:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:51b41d632670fe8c786707c7977f9136c593c137bcde08516527421769778ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7473e22367c8e8c736bb1ce76169b1b4abf93fa0b057dec9103c4dccf90efc2`

```dockerfile
```

-	Layers:
	-	`sha256:f90631de8235b43d3b44250b8606b5783cd39dc12e9810fb5993f82a19dfe2ee`  
		Last Modified: Tue, 04 Nov 2025 10:34:51 GMT  
		Size: 2.0 MB (2005391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29d51086244a15fe10ebfe78e299fc7a89dd09601c8753741004d27949898c16`  
		Last Modified: Tue, 04 Nov 2025 10:34:52 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:ead041ea0e5c06d481ac304f7b4076a3339d849fcdffa3d25603418dc2fe82e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36187425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b0128aff763178ac8bb867e486c2450bacad45f79a5ff629194be435141070`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:52:27 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 01:52:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:55:40 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 01:55:40 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 01:55:40 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 01:55:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 01:55:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:55:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 01:55:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:55:41 GMT
USER memcache
# Tue, 04 Nov 2025 01:55:41 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 01:55:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126ce0c080daa81edc8784c59f60350b32083b3201304709775cf554155f80af`  
		Last Modified: Tue, 04 Nov 2025 01:56:04 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4c9857fe1f3ded2ba6c29c2f9591c7f5b2bfc46517527fac13f4c2b539a9a4`  
		Last Modified: Tue, 04 Nov 2025 01:56:04 GMT  
		Size: 170.2 KB (170244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e15beeee778428c51e89d0b8c3d6ca7931f0324e0a66f6b2bf85b101e9674a`  
		Last Modified: Tue, 04 Nov 2025 01:56:04 GMT  
		Size: 2.4 MB (2417022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d427e3c140105cfdb1a22a00010621a5a0834ce00ba3ea1059f8a63d8b0f5ee5`  
		Last Modified: Tue, 04 Nov 2025 01:56:04 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dfc7efa96996e95dcf030731f854bc07f2c7aa3349e75c4e74c04d924b3c62`  
		Last Modified: Tue, 04 Nov 2025 01:56:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:ad9b48a87b820bbf6c20cb57cd2247fa75ca6de00df26576f784a8f51703c571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1582395261fcee60bb7362c6cff0abd1d7325b4fde3cd609ac637f76aaa7ea5`

```dockerfile
```

-	Layers:
	-	`sha256:f5e9fbdfb8deeebb9142cd4facdedb0629028f8343a64b1e13d26ecb035f3c84`  
		Last Modified: Tue, 04 Nov 2025 10:34:55 GMT  
		Size: 2.0 MB (2011835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3dd30af34832aa3d277b4b6882a9786e4225d5a7387d5af5a66cadc59adc22d`  
		Last Modified: Tue, 04 Nov 2025 10:34:56 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:56542c7304b39c7980a644419d2ab6f603477cc9e1cb9c575d45b8c4220e0c6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30630140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e279bc62f41c4006902271742290cdde9d77c2121c1b4db697d09d01c690860e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 03:30:39 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 03:31:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:44:44 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 03:44:44 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 03:44:44 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 03:44:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 03:44:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 03:44:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 03:44:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 03:44:45 GMT
USER memcache
# Tue, 04 Nov 2025 03:44:45 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 03:44:45 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b836efb62045adb472c559fe0a4cedfe183f60ae9e36defd9b46efc4886fff56`  
		Last Modified: Tue, 04 Nov 2025 03:45:39 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db437579ba55d9291ad05cd904e857adb520e8189f0cc2fb207b475c10a95ee`  
		Last Modified: Tue, 04 Nov 2025 03:45:39 GMT  
		Size: 133.0 KB (132994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ca1f664c3ee469c225e4241d90dabf5a36c9fd5282ec51011fe16b9fcd5882`  
		Last Modified: Tue, 04 Nov 2025 03:45:39 GMT  
		Size: 2.2 MB (2219849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f5b56363e737d5d4b276274dc82b3ae7d3772bb1d6cadc5fb0c117ad6d004e`  
		Last Modified: Tue, 04 Nov 2025 03:45:39 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92139c3e4198e9ce61d77b8a86d621938a3390898a4ac22ba81eefd286a78cc7`  
		Last Modified: Tue, 04 Nov 2025 03:45:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:a72757dfcc56cb3edf581d72aa35ca18e099d18284ccfaabc697a74b2d7c2399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40a19d13356829e752dd3f0c530a1f2ef0abfc0ca53d29d3d74e1840a1698892`

```dockerfile
```

-	Layers:
	-	`sha256:78add421d4e1ac7755ca522075904f0acd06a15e1c8b9ca1bb0047a7d3ebf187`  
		Last Modified: Tue, 04 Nov 2025 07:34:38 GMT  
		Size: 2.0 MB (2002198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f1fc3731e375af1e0712ec91b83487acb49e907a1168f593f251fe43cb51fb9`  
		Last Modified: Tue, 04 Nov 2025 07:34:39 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; s390x

```console
$ docker pull memcached@sha256:3de73b4ecf32984b0c6603b973257071c81c94af8351b35aa4343407c7315726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32293163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e6900a4460f82b0703aed07dde3c1722bdb7919a582b6b1f22a9ca701cb510f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 06:58:32 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 06:58:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 07:02:23 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 07:02:23 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 07:02:23 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 07:02:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 07:02:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 07:02:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 07:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 07:02:23 GMT
USER memcache
# Tue, 04 Nov 2025 07:02:23 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 07:02:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17527924bc8c8387e810ff986ddbe9998a0b5d55a4850b90b4cea0a897c94a09`  
		Last Modified: Tue, 04 Nov 2025 07:02:40 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54fd3d90bab9e973d6a8c142df91794bdc213e5bafe8926a58809036e1ee1f5`  
		Last Modified: Tue, 04 Nov 2025 07:02:40 GMT  
		Size: 140.4 KB (140429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc993f31fbd52e75a8dfc710d94d4130a8c228be35b7737c5950a5f93a1125a`  
		Last Modified: Tue, 04 Nov 2025 07:02:40 GMT  
		Size: 2.3 MB (2313833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acaa055d548771aab19234adcaf5b3ed727ee85214c303e1035e3e464e0fbda0`  
		Last Modified: Tue, 04 Nov 2025 07:02:40 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c2e1b3aad04d0544265917caef9c91d5ed4496376262541974a707026847f4`  
		Last Modified: Tue, 04 Nov 2025 07:02:40 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:414b070c237a13d5dee83e1db26eb0f953dd5af0753013a8bbd988611aa90e89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5cc4920f789bfe656195ac67c3ddd1a00030591f92b5ac4dc2b0e9dcdd2a0b`

```dockerfile
```

-	Layers:
	-	`sha256:b242fd5db27262af27c5589b736a5ae9f234cb03765c59c73e64818c1cade0c8`  
		Last Modified: Tue, 04 Nov 2025 10:35:02 GMT  
		Size: 2.0 MB (2009671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e15d059f16d47b54c3d82bdf997670c62a062815b64d7e7b486d8de0060691b4`  
		Last Modified: Tue, 04 Nov 2025 10:35:03 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json
