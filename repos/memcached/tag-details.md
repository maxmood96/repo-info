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
-	[`memcached:1.6.37`](#memcached1637)
-	[`memcached:1.6.37-alpine`](#memcached1637-alpine)
-	[`memcached:1.6.37-alpine3.21`](#memcached1637-alpine321)
-	[`memcached:1.6.37-bookworm`](#memcached1637-bookworm)
-	[`memcached:alpine`](#memcachedalpine)
-	[`memcached:alpine3.21`](#memcachedalpine321)
-	[`memcached:bookworm`](#memcachedbookworm)
-	[`memcached:latest`](#memcachedlatest)

## `memcached:1`

```console
$ docker pull memcached@sha256:685ba31ae4994ff6daf16d21142346dbd828d0dfbeff3cbc7a7f9b4f5f93b2dd
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
$ docker pull memcached@sha256:bfe5fd0aac5c89b8022c2620abc0a1118cb84d68a74a437ac1fef55be567a23f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31972590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a69266e53d188956df96699ee7bd22b00986730a190789881f82a593361bfc16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d569cc07bddca59980d45ae28a8bfede7584cdca655fad52796e829ac8b7fee`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c58bc9b838a5c291945e3cd889cc93151a03fc70e079914ba998f26239ef2e`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 2.5 MB (2491762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67c97f377dc045ebb683ab2bf6d771520192351043ab7fc20c63ed1a997f84b`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 1.3 MB (1267012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8282d3a602638805126b2e682263fb38ca402e3beaa3a047ed0add1bf754fdb8`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cd8dd518d1c91daec2bae1887feb80b6473e0fe5e6846ddb613387e8311c64`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:ffc24940329fbd38d3efa10fbceb92bc75b8c8e3861170180d934c88ad8659b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a2b67f33d20bb90a8a9305d3ef143d1332d728823aeba14947ec779d5da211`

```dockerfile
```

-	Layers:
	-	`sha256:6ff1804b1ee0e0da242ef1ef47226adb9ac0a4172528e4ac5501443a5e6f3487`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 2.3 MB (2289307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6460f3cc3f151e357a1fa273d42ff4f884c9d2b093c4763cb3c73595fb554fa5`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v5

```console
$ docker pull memcached@sha256:abee184952eb3cfc02bd6555047901e0e27fe9379eaddc25acb7805ac3c01e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29079400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c55ad492b5523a9106a2cef2d811d102d5d88a74110653f3187894c060ae61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aa8576c673e5a651f7450bee7603a12ac6168051fdd5b2411678987e180cad6e`  
		Last Modified: Tue, 04 Feb 2025 01:38:28 GMT  
		Size: 25.7 MB (25736549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d03c1f12f429fcd661498f32bc4e1c1e6a1e4189bd6014e71da057147e2286`  
		Last Modified: Tue, 04 Feb 2025 04:58:18 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7e25c626324a280a0e7be83a5642bb48a551515d4c38cb544c66904fcf10bb`  
		Last Modified: Tue, 04 Feb 2025 04:58:19 GMT  
		Size: 2.1 MB (2096073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b068d3f71231f010921a5b6713e177cb20b1838ecd63d09bbfa1cf87d64a1108`  
		Last Modified: Sat, 22 Feb 2025 00:32:42 GMT  
		Size: 1.2 MB (1245268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b49e89cf77efc47a7250f3af153069fc9a2d7696d280b7f9b2ef3ef434a4e1b`  
		Last Modified: Sat, 22 Feb 2025 00:32:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615b1475c4f9cc790d1525380d666d53c7507c87e777e647ed0287598efa3d48`  
		Last Modified: Sat, 22 Feb 2025 00:32:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:b668a646c910c9b5f5c8f752e53b49deb2a1ad6e7ebdc0526adbcf9d299b4ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49e0834cecf5abf237b771c3850e94ba86e05385ccbab4b91cb3d9f063af010c`

```dockerfile
```

-	Layers:
	-	`sha256:cb0b22895c3619cafd6dca713774db852bfe31b3adb4ba3ec6a66838eac945e3`  
		Last Modified: Sat, 22 Feb 2025 00:32:42 GMT  
		Size: 2.3 MB (2292845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d7f06daebcc005d1c5979488409050e03ba04720bf9c424588de02b684b8c03`  
		Last Modified: Sat, 22 Feb 2025 00:32:42 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ecdac108a456c82920f95b934edd7b2c3abf62adf96adac7b99767591b6fecf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31658335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c4d6a0c65f7a9206b9660b5d79d29c8183bb45cef6fa838bbc17493f7085b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85c190a9b2b110c5e0805ab31e5792459e717a286856047e10f45423d8231dd`  
		Last Modified: Wed, 05 Feb 2025 20:31:30 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d150df6d26f3098fb2b4554249a49c854dd5acf5f8255fcf725a970fdbcccbe`  
		Last Modified: Wed, 05 Feb 2025 20:31:31 GMT  
		Size: 2.4 MB (2355307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d34310d49ce6a8c13f0814ea92dbb59638c73a98d899a8f489b4cdba59cf1a4`  
		Last Modified: Sat, 22 Feb 2025 00:31:38 GMT  
		Size: 1.3 MB (1260635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d933eb164ac02e89a9ec663d27d218ab0e489db96ca622ac5023f149bb767f2`  
		Last Modified: Sat, 22 Feb 2025 00:31:38 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3955731998caab6a7273ad7e2b63e663ae711d2f45416977f29c9df6c3a5771`  
		Last Modified: Sat, 22 Feb 2025 00:31:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:b0998d3901cbf4dc98a6f5d0254d7f2115d3d110c1de81a5ec4cc6b56c1afe39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:351b12242d29e072aaf887e69b6b36f8b86fb05d09e37cd2a338014241525536`

```dockerfile
```

-	Layers:
	-	`sha256:c6ec4332029f56a214be68a1da8a91d6170bcc2d2d243daae2353e3cb0baeaae`  
		Last Modified: Sat, 22 Feb 2025 00:31:38 GMT  
		Size: 2.3 MB (2289622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c51e1294036728fb8cdc19970c532c2ced14c50e64984ed76d91eda1e1a61c92`  
		Last Modified: Sat, 22 Feb 2025 00:31:38 GMT  
		Size: 21.4 KB (21419 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:ef53c35087afb0499842bedf1fbfa79d5b842f19779b63afa6f1f025a9d5a6ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32956089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e8028b418ebc438bf613b1826c1c627b9c70d0ceba487e067f06ce1140efa93`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a2635855d79b555abffa55c629412da2c4134f2a8ccd4a315c0b6f92b579ae`  
		Last Modified: Sat, 22 Feb 2025 00:31:19 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b44d66689e77fbfe0bc0a0c7e8a45833882611191361e49b6a48030dfbda7bb`  
		Last Modified: Sat, 22 Feb 2025 00:31:20 GMT  
		Size: 2.5 MB (2500720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22086dfd31db842102b740e2bc68682931021ff3fb6491253f9087ca1df6f3cd`  
		Last Modified: Sat, 22 Feb 2025 00:31:19 GMT  
		Size: 1.3 MB (1266399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0d2b64685890c225d3c813b7c867d2d96fb3719d43d4edb206375e55ee6a32`  
		Last Modified: Sat, 22 Feb 2025 00:31:19 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365bc8ba2a50069e758df20bd1b42ff192846fbb115b9edb0cda2fc43fdb2600`  
		Last Modified: Sat, 22 Feb 2025 00:31:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:26ed9f96a812fb5af80816d45e029522166082e249f638019205191bb5b02cb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb94ae18d76a538788c16c601bc76b3509862697a1367bd2fa42cfd5ab18e5b9`

```dockerfile
```

-	Layers:
	-	`sha256:ece746d0e00e98b51635c1914e1aeab67cf6208f531559f2af8346d9e8f40606`  
		Last Modified: Sat, 22 Feb 2025 00:31:20 GMT  
		Size: 2.3 MB (2286406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31ecb87a15a354348411689e2d7bf34846d275e3db9f99b9d2fd53c5d931d382`  
		Last Modified: Sat, 22 Feb 2025 00:31:19 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; mips64le

```console
$ docker pull memcached@sha256:61282eccad654d1d03273cc2fb02a4db982d36e9e0ff866eab773795e106ec8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31692298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c72f2790d1441f439ca292b3f0077287e8f93af8f30b6ae44f467f4728aecf0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:60fe4951c23056512065fcf1948d3167c5aa5d83d4bfd2829494b7d09b4fe661`  
		Last Modified: Tue, 04 Feb 2025 01:38:47 GMT  
		Size: 28.5 MB (28486581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006e6bf1f5c579c425dd6a7045b45795f463f886bf4ee3532c5964da484e77c4`  
		Last Modified: Tue, 04 Feb 2025 05:36:04 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa88afbdcfa1d52adc83e6c274708611503deecc6240cf640db7eb23e1999a30`  
		Last Modified: Sat, 22 Feb 2025 00:36:16 GMT  
		Size: 1.9 MB (1943183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dcb0fa418dcf8d7cccdc41a73ad2063c2ae4bf810f2b8a7c67a8ead47c9d684`  
		Last Modified: Sat, 22 Feb 2025 00:36:16 GMT  
		Size: 1.3 MB (1261025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f222082e64a60018ba8bea35cd86f7254591435953a40e022541df5dd42e64`  
		Last Modified: Sat, 22 Feb 2025 00:36:16 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f367b09aa255318629e01e577d62f20d50bcc2cb49cd5519a9c1b68c0829b4e`  
		Last Modified: Sat, 22 Feb 2025 00:36:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:c3872907481511259937b839ceb7f595c2edbf6f47b17ae6cd4e1a10c2456f41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48598526c0aff23b0715615e1f0cd1c35b57f4de0e9b13447903c812540b5683`

```dockerfile
```

-	Layers:
	-	`sha256:308d9f10522a8efc39d94eb5a4f47a8b547bdf8ef47d53a710264ade572dc85b`  
		Last Modified: Sat, 22 Feb 2025 00:36:16 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:10e27fa85f13d51af4a481e4778b04b3b80d506a129aab984fc5d5dab919a8e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36085879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac4b53721162a6ae89b5b0e96dfb4e7ba41127c795c3b9689c36040284ea691`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 01:38:01 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2deccedfff592cdf0e60a1a0f23cfa011cc09854b3b8fd5979a2215801fe859a`  
		Last Modified: Wed, 05 Feb 2025 20:30:01 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f77d137ef9ee5f1f27684f14e816a1f088dfffc4476ab6d02ffa5d251db059`  
		Last Modified: Wed, 05 Feb 2025 20:30:01 GMT  
		Size: 2.7 MB (2708582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163ac5a13dc4a349552e8a728dbfe7a6747c6c194c8f3af433fa8f89ca89614e`  
		Last Modified: Sat, 22 Feb 2025 00:31:22 GMT  
		Size: 1.3 MB (1331006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52cbf6e5ffb6677cc60835d4722667a4e9ac72b9ede1a0a9f282e56abf5dc63`  
		Last Modified: Sat, 22 Feb 2025 00:31:22 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7111ad13f64383b6c5b3388ba5cd00d3804080114fc716c24ebe318a0b45d350`  
		Last Modified: Sat, 22 Feb 2025 00:31:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:8ec0ef0ee501fe9bf349dbf63dce11035a606876a565ee69fd5055418b09d08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8468c14d9febe1b645497e9293a93d6b378bbdb3147a6c0bb18f23a907241bda`

```dockerfile
```

-	Layers:
	-	`sha256:ebd1905c7f20a0d3d102c7b17f531860a3ac45d105b42f0669754a3230ae5fe2`  
		Last Modified: Sat, 22 Feb 2025 00:31:22 GMT  
		Size: 2.3 MB (2293679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b94eff9fb2c5e828a7e6a3ec42729e322d3cc31372e12a5ad1b7eb9761e30a8`  
		Last Modified: Sat, 22 Feb 2025 00:31:21 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:10f8a97eb4da432625002966d78d3993a95f073fb5077a1a4f3cc5a76cd6bab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30261694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a090e8956a7fcbb8b2f590626585d48385828d83d3925e0f8127f400e7c074`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85c3e9bcd86da2086f455efe77a700fe40645a11782885cb35509ae6da968af`  
		Last Modified: Wed, 05 Feb 2025 20:31:33 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25653c174b0d3f4223a55d32a6e019a0a071b0f939c2043a5f3ca38897b6a47`  
		Last Modified: Wed, 05 Feb 2025 20:31:33 GMT  
		Size: 2.2 MB (2156373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86dc255a71b2a050391adb8d18b925df4b93b704a5d38583f893d4c1e1babe1`  
		Last Modified: Sat, 22 Feb 2025 00:31:32 GMT  
		Size: 1.2 MB (1245183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848092fc56244055b7ee89f53de1c07230b0bd2651e37dea23770fc8089383db`  
		Last Modified: Sat, 22 Feb 2025 00:31:33 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab89cd679a4ffa81bbb3cbb213b25b557649024534fef1f253bdaf6f65799c05`  
		Last Modified: Sat, 22 Feb 2025 00:31:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:b70e906e72967b0e6ed1c8be6d754bf62e2ee68350435a171d182ba6efc9dd70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f906cfd918535c7f2f1b3af08ff4c29ffce9b1c176c8ca28e5f3333bd612aaa3`

```dockerfile
```

-	Layers:
	-	`sha256:0fcec7672387ec22fd81d2b2a8c5de99e7aae50b53faf5bf629ded84a19776d1`  
		Last Modified: Sat, 22 Feb 2025 00:31:32 GMT  
		Size: 2.3 MB (2289021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5d0bd85e2270f2d197500c26d3f1fdc8af08248f560b4dfcee81130a4a3748f`  
		Last Modified: Sat, 22 Feb 2025 00:31:32 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:c2efa3700db8d6768b4fc98e064843aa0c98705e9bb3e63a70768d7a6a5b6a02
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
$ docker pull memcached@sha256:787e9120e36559c9aba4cce621188072d00e159bc596fe803c00037f3702c22f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4716929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21a7aa256b160c9c42cce498615225db46d75b42d27b180c3879e9e7d1fbd92`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3e9f8182c72be0cf629032be09e1b5da2b94a8a03a202110036eae2fa538b9`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc58417b03bbd338e8fab898ba984cef01fdb2b2960ae862ecc89bc258a0b981`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 104.7 KB (104690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82369477a539cf4bc0cfd0063cb20ce85cf36442b532dbde15f71a6061abc106`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 968.6 KB (968644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0261a578c93ccd99ba866def61b28a43cc2938598cbc307011db812c246ee206`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cd8dd518d1c91daec2bae1887feb80b6473e0fe5e6846ddb613387e8311c64`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:abae77e9a8d50f01601a4188494f6d7a2e3442e7258fa213a581d2e281fc02c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c452640b5e4fe4e1b31941228c0615b396ec62a56794e1c63e1b9326c5cbf60a`

```dockerfile
```

-	Layers:
	-	`sha256:297387df1b0d33fd74438a8273ab5e20a2a8193785491bcc9b6ad3e03d9c1aa6`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 93.6 KB (93633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0d579b1ca91bec4046749a5bf7a3549239008c1a1083ec2213a3c6004a5725b`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 19.6 KB (19570 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:22169a1786f676798782408232c35b71e12bd32b10164e81c0b32da6143641c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5083533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add144e03275b9c89bb582ad307446fa229055731caf45650896ed6d340a839a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b3b947aa71cef021cd9306b1f24a44554e8d663c8530dd36d42b94a883f4c9`  
		Last Modified: Fri, 14 Feb 2025 19:50:13 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6014feb1c2bb2b6c63e9a7b16a3850c447422bdad6e65b302925b8547b23c192`  
		Last Modified: Fri, 14 Feb 2025 19:50:13 GMT  
		Size: 120.8 KB (120780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b307ec9e1116f91be05519ed18f8206fb49e72d80c7a04638004cf9a82ac2a77`  
		Last Modified: Sat, 22 Feb 2025 00:34:08 GMT  
		Size: 968.4 KB (968374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b643c0752d8cb8b54b8a8d095693feba316ac84b1fd17048fc0189599bc5e1d`  
		Last Modified: Sat, 22 Feb 2025 00:34:08 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38c21d127cb51320d77ca177167435601efbd6ddc02a49c2876aac2884a0109`  
		Last Modified: Sat, 22 Feb 2025 00:34:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:bef45ca6f335dcb09118c5ee88802a722f482af24a9afa8974e7b4800b0fd39f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b1eae2531d72df59778c8c8ac7fecb6d4b6b408b9192cc6ac7d77a5e98128d7`

```dockerfile
```

-	Layers:
	-	`sha256:f675a5a746afeb63892d91271eccac08f3a01bbf6dae0926114e83673197e1be`  
		Last Modified: Sat, 22 Feb 2025 00:34:08 GMT  
		Size: 93.7 KB (93737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74fc4c03468266c50ce86e1314f4c6f45903d6c98465180f75f826dfb54cfcfd`  
		Last Modified: Sat, 22 Feb 2025 00:34:07 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:46aa92b9d94ea6493f4f5f098e6b1de64f3e8c450eb6440d5bf59f4e1f2ead69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4534801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac2f67d3ec71890e3d6bd391e98b4da571242348ac135e99bcef39979486b34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0216147e703738541dd8987b9b2bc147da47c311b00a06feb265c9f0abf707`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab4b25598c42e6f016cb0a26803d39acd19d7871e0b092cbefd2f8856b0a112`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 109.5 KB (109489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5589cc68943165ccc1b90f645ea08e4c8bb401c6ea2db3506bd1309fd04158`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 960.3 KB (960336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f9697b895d35627f393cf365d336aad6ff6d5d9d767f2ab73d2696751527c1`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a049f6eb832cc266adfa607fe5c42c0710850885d375ee2fd2b22a9add7d29b7`  
		Last Modified: Sat, 22 Feb 2025 00:31:07 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:f9710d1f921ddd802f69f2eb77ae2baa0a046307d13215474dd3f369124034e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de341f780812144f1c4528778277abc1e0f979937153200813e3e66b11d01d02`

```dockerfile
```

-	Layers:
	-	`sha256:4bd1b00215d14ae69987d6066982bb958dbe599471eebf5233fbc9512b4a5fcd`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 93.6 KB (93588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1126652f997b244e12c038e90d03bc059f60adbf626ea9d38c90259a5920775c`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 19.5 KB (19512 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:e3fbb21940e6ecf6e09878be1fdb50cfe7d0ca132112d7439d1c3f266f6b8b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4706934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ab0bd6e09f5b37468b8ae688526c599c21045baf0b0b8bc98ec097e5267b28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deee0b86774e394f5e07eff435a072bdde8922ec1757ef689265af3e1864d632`  
		Last Modified: Fri, 14 Feb 2025 19:42:34 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbafd6c675f155044ba3e5ef96996313b9f05064b966848001c7ea04a9c6048`  
		Last Modified: Fri, 14 Feb 2025 19:42:34 GMT  
		Size: 124.3 KB (124276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56400c974ec4a72a96f97ce1a5828e0ebcb6df76fe5c2f7d8dae29c07223abbf`  
		Last Modified: Sat, 22 Feb 2025 00:34:12 GMT  
		Size: 1.0 MB (1006957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0b9347f26655d1e450da08a0e5a23d5cc368bbfad35a84c643be25c87b2726`  
		Last Modified: Sat, 22 Feb 2025 00:34:11 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5064388d99c64e09f330fcec8ffba565524c380566e6a70fb34aedbf84880f8`  
		Last Modified: Sat, 22 Feb 2025 00:34:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:94cd05711888081e81791841a80e96d16b22ba21e835ba80d125ed65d295b947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84057bf494e545f78faa4d02b570fd42a27b6c3a616d2e07c06013f7125b0ec2`

```dockerfile
```

-	Layers:
	-	`sha256:f969bce286e2478dcbbe6690408d5b20920506d09783024c5e824272ee16cc9e`  
		Last Modified: Sat, 22 Feb 2025 00:34:11 GMT  
		Size: 91.7 KB (91740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93bbfb8bcbd31cfc88a941030e8e18f43fdb73c07293481a932203cb3a25e504`  
		Last Modified: Sat, 22 Feb 2025 00:34:11 GMT  
		Size: 19.6 KB (19648 bytes)  
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
$ docker pull memcached@sha256:0087cdeb03b579438e5e722b991d7e3ee891e4770b26ceeff27c4401cf654657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4571101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2bc2ef8da87893bf85939bd479692ebd280f9d840686e5fdc00089b536aad65`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d658470bb26df23b8a940bc8e53f6c8b685a81ce47a086f683e29b63a6bac496`  
		Last Modified: Fri, 14 Feb 2025 19:44:23 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a07c51d6bc9e389360e3ccba6d95f5697fdd3366a1ac093d59ce54e0da2550`  
		Last Modified: Fri, 14 Feb 2025 19:44:23 GMT  
		Size: 113.5 KB (113462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91fbcb7a7ec7da4c7e8e462c545d152b5a079ef1360a1d05df018c7f78da31e7`  
		Last Modified: Sat, 22 Feb 2025 00:35:17 GMT  
		Size: 988.7 KB (988725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539207d8d3aff51a577331b44e1e08e93ad1330f182ca154c800fa3cc40b77bd`  
		Last Modified: Sat, 22 Feb 2025 00:35:17 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236b320beb51084e2e1b6b838aa193caf573a4292b1353bba1a0cdf076b82db6`  
		Last Modified: Sat, 22 Feb 2025 00:35:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9bd727783dc634399ded38736a232ba7801976d1b0096e07194f53a8f82de528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 KB (111252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7030d08f1e1857ea22b2d774577cb0cb56dd6eb8f7b7ff94fb262e44551c1c`

```dockerfile
```

-	Layers:
	-	`sha256:b7ec10e807d6f8925ef59303e53fc02069fd4a687b1baa66cf3164590cb29d4b`  
		Last Modified: Sat, 22 Feb 2025 00:35:17 GMT  
		Size: 91.7 KB (91682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25a3bb1b2ff42fd2d2a4c3e88ec8af248b5df8c2a42a871dcec17d8a1deb6dbb`  
		Last Modified: Sat, 22 Feb 2025 00:35:17 GMT  
		Size: 19.6 KB (19570 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine3.21`

```console
$ docker pull memcached@sha256:4fb13e4757387000230be124c5a74f107abfd1f65e2526f4c627110d666bf5a3
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
$ docker pull memcached@sha256:787e9120e36559c9aba4cce621188072d00e159bc596fe803c00037f3702c22f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4716929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21a7aa256b160c9c42cce498615225db46d75b42d27b180c3879e9e7d1fbd92`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3e9f8182c72be0cf629032be09e1b5da2b94a8a03a202110036eae2fa538b9`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc58417b03bbd338e8fab898ba984cef01fdb2b2960ae862ecc89bc258a0b981`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 104.7 KB (104690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82369477a539cf4bc0cfd0063cb20ce85cf36442b532dbde15f71a6061abc106`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 968.6 KB (968644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0261a578c93ccd99ba866def61b28a43cc2938598cbc307011db812c246ee206`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cd8dd518d1c91daec2bae1887feb80b6473e0fe5e6846ddb613387e8311c64`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:abae77e9a8d50f01601a4188494f6d7a2e3442e7258fa213a581d2e281fc02c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c452640b5e4fe4e1b31941228c0615b396ec62a56794e1c63e1b9326c5cbf60a`

```dockerfile
```

-	Layers:
	-	`sha256:297387df1b0d33fd74438a8273ab5e20a2a8193785491bcc9b6ad3e03d9c1aa6`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 93.6 KB (93633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0d579b1ca91bec4046749a5bf7a3549239008c1a1083ec2213a3c6004a5725b`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 19.6 KB (19570 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:22169a1786f676798782408232c35b71e12bd32b10164e81c0b32da6143641c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5083533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add144e03275b9c89bb582ad307446fa229055731caf45650896ed6d340a839a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b3b947aa71cef021cd9306b1f24a44554e8d663c8530dd36d42b94a883f4c9`  
		Last Modified: Fri, 14 Feb 2025 19:50:13 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6014feb1c2bb2b6c63e9a7b16a3850c447422bdad6e65b302925b8547b23c192`  
		Last Modified: Fri, 14 Feb 2025 19:50:13 GMT  
		Size: 120.8 KB (120780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b307ec9e1116f91be05519ed18f8206fb49e72d80c7a04638004cf9a82ac2a77`  
		Last Modified: Sat, 22 Feb 2025 00:34:08 GMT  
		Size: 968.4 KB (968374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b643c0752d8cb8b54b8a8d095693feba316ac84b1fd17048fc0189599bc5e1d`  
		Last Modified: Sat, 22 Feb 2025 00:34:08 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38c21d127cb51320d77ca177167435601efbd6ddc02a49c2876aac2884a0109`  
		Last Modified: Sat, 22 Feb 2025 00:34:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:bef45ca6f335dcb09118c5ee88802a722f482af24a9afa8974e7b4800b0fd39f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b1eae2531d72df59778c8c8ac7fecb6d4b6b408b9192cc6ac7d77a5e98128d7`

```dockerfile
```

-	Layers:
	-	`sha256:f675a5a746afeb63892d91271eccac08f3a01bbf6dae0926114e83673197e1be`  
		Last Modified: Sat, 22 Feb 2025 00:34:08 GMT  
		Size: 93.7 KB (93737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74fc4c03468266c50ce86e1314f4c6f45903d6c98465180f75f826dfb54cfcfd`  
		Last Modified: Sat, 22 Feb 2025 00:34:07 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; 386

```console
$ docker pull memcached@sha256:46aa92b9d94ea6493f4f5f098e6b1de64f3e8c450eb6440d5bf59f4e1f2ead69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4534801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac2f67d3ec71890e3d6bd391e98b4da571242348ac135e99bcef39979486b34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0216147e703738541dd8987b9b2bc147da47c311b00a06feb265c9f0abf707`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab4b25598c42e6f016cb0a26803d39acd19d7871e0b092cbefd2f8856b0a112`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 109.5 KB (109489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5589cc68943165ccc1b90f645ea08e4c8bb401c6ea2db3506bd1309fd04158`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 960.3 KB (960336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f9697b895d35627f393cf365d336aad6ff6d5d9d767f2ab73d2696751527c1`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a049f6eb832cc266adfa607fe5c42c0710850885d375ee2fd2b22a9add7d29b7`  
		Last Modified: Sat, 22 Feb 2025 00:31:07 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:f9710d1f921ddd802f69f2eb77ae2baa0a046307d13215474dd3f369124034e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de341f780812144f1c4528778277abc1e0f979937153200813e3e66b11d01d02`

```dockerfile
```

-	Layers:
	-	`sha256:4bd1b00215d14ae69987d6066982bb958dbe599471eebf5233fbc9512b4a5fcd`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 93.6 KB (93588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1126652f997b244e12c038e90d03bc059f60adbf626ea9d38c90259a5920775c`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 19.5 KB (19512 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; ppc64le

```console
$ docker pull memcached@sha256:e3fbb21940e6ecf6e09878be1fdb50cfe7d0ca132112d7439d1c3f266f6b8b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4706934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ab0bd6e09f5b37468b8ae688526c599c21045baf0b0b8bc98ec097e5267b28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deee0b86774e394f5e07eff435a072bdde8922ec1757ef689265af3e1864d632`  
		Last Modified: Fri, 14 Feb 2025 19:42:34 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbafd6c675f155044ba3e5ef96996313b9f05064b966848001c7ea04a9c6048`  
		Last Modified: Fri, 14 Feb 2025 19:42:34 GMT  
		Size: 124.3 KB (124276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56400c974ec4a72a96f97ce1a5828e0ebcb6df76fe5c2f7d8dae29c07223abbf`  
		Last Modified: Sat, 22 Feb 2025 00:34:12 GMT  
		Size: 1.0 MB (1006957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0b9347f26655d1e450da08a0e5a23d5cc368bbfad35a84c643be25c87b2726`  
		Last Modified: Sat, 22 Feb 2025 00:34:11 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5064388d99c64e09f330fcec8ffba565524c380566e6a70fb34aedbf84880f8`  
		Last Modified: Sat, 22 Feb 2025 00:34:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:94cd05711888081e81791841a80e96d16b22ba21e835ba80d125ed65d295b947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84057bf494e545f78faa4d02b570fd42a27b6c3a616d2e07c06013f7125b0ec2`

```dockerfile
```

-	Layers:
	-	`sha256:f969bce286e2478dcbbe6690408d5b20920506d09783024c5e824272ee16cc9e`  
		Last Modified: Sat, 22 Feb 2025 00:34:11 GMT  
		Size: 91.7 KB (91740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93bbfb8bcbd31cfc88a941030e8e18f43fdb73c07293481a932203cb3a25e504`  
		Last Modified: Sat, 22 Feb 2025 00:34:11 GMT  
		Size: 19.6 KB (19648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; s390x

```console
$ docker pull memcached@sha256:0087cdeb03b579438e5e722b991d7e3ee891e4770b26ceeff27c4401cf654657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4571101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2bc2ef8da87893bf85939bd479692ebd280f9d840686e5fdc00089b536aad65`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d658470bb26df23b8a940bc8e53f6c8b685a81ce47a086f683e29b63a6bac496`  
		Last Modified: Fri, 14 Feb 2025 19:44:23 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a07c51d6bc9e389360e3ccba6d95f5697fdd3366a1ac093d59ce54e0da2550`  
		Last Modified: Fri, 14 Feb 2025 19:44:23 GMT  
		Size: 113.5 KB (113462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91fbcb7a7ec7da4c7e8e462c545d152b5a079ef1360a1d05df018c7f78da31e7`  
		Last Modified: Sat, 22 Feb 2025 00:35:17 GMT  
		Size: 988.7 KB (988725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539207d8d3aff51a577331b44e1e08e93ad1330f182ca154c800fa3cc40b77bd`  
		Last Modified: Sat, 22 Feb 2025 00:35:17 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236b320beb51084e2e1b6b838aa193caf573a4292b1353bba1a0cdf076b82db6`  
		Last Modified: Sat, 22 Feb 2025 00:35:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:9bd727783dc634399ded38736a232ba7801976d1b0096e07194f53a8f82de528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 KB (111252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7030d08f1e1857ea22b2d774577cb0cb56dd6eb8f7b7ff94fb262e44551c1c`

```dockerfile
```

-	Layers:
	-	`sha256:b7ec10e807d6f8925ef59303e53fc02069fd4a687b1baa66cf3164590cb29d4b`  
		Last Modified: Sat, 22 Feb 2025 00:35:17 GMT  
		Size: 91.7 KB (91682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25a3bb1b2ff42fd2d2a4c3e88ec8af248b5df8c2a42a871dcec17d8a1deb6dbb`  
		Last Modified: Sat, 22 Feb 2025 00:35:17 GMT  
		Size: 19.6 KB (19570 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-bookworm`

```console
$ docker pull memcached@sha256:685ba31ae4994ff6daf16d21142346dbd828d0dfbeff3cbc7a7f9b4f5f93b2dd
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
$ docker pull memcached@sha256:bfe5fd0aac5c89b8022c2620abc0a1118cb84d68a74a437ac1fef55be567a23f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31972590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a69266e53d188956df96699ee7bd22b00986730a190789881f82a593361bfc16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d569cc07bddca59980d45ae28a8bfede7584cdca655fad52796e829ac8b7fee`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c58bc9b838a5c291945e3cd889cc93151a03fc70e079914ba998f26239ef2e`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 2.5 MB (2491762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67c97f377dc045ebb683ab2bf6d771520192351043ab7fc20c63ed1a997f84b`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 1.3 MB (1267012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8282d3a602638805126b2e682263fb38ca402e3beaa3a047ed0add1bf754fdb8`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cd8dd518d1c91daec2bae1887feb80b6473e0fe5e6846ddb613387e8311c64`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:ffc24940329fbd38d3efa10fbceb92bc75b8c8e3861170180d934c88ad8659b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a2b67f33d20bb90a8a9305d3ef143d1332d728823aeba14947ec779d5da211`

```dockerfile
```

-	Layers:
	-	`sha256:6ff1804b1ee0e0da242ef1ef47226adb9ac0a4172528e4ac5501443a5e6f3487`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 2.3 MB (2289307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6460f3cc3f151e357a1fa273d42ff4f884c9d2b093c4763cb3c73595fb554fa5`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:abee184952eb3cfc02bd6555047901e0e27fe9379eaddc25acb7805ac3c01e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29079400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c55ad492b5523a9106a2cef2d811d102d5d88a74110653f3187894c060ae61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aa8576c673e5a651f7450bee7603a12ac6168051fdd5b2411678987e180cad6e`  
		Last Modified: Tue, 04 Feb 2025 01:38:28 GMT  
		Size: 25.7 MB (25736549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d03c1f12f429fcd661498f32bc4e1c1e6a1e4189bd6014e71da057147e2286`  
		Last Modified: Tue, 04 Feb 2025 04:58:18 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7e25c626324a280a0e7be83a5642bb48a551515d4c38cb544c66904fcf10bb`  
		Last Modified: Tue, 04 Feb 2025 04:58:19 GMT  
		Size: 2.1 MB (2096073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b068d3f71231f010921a5b6713e177cb20b1838ecd63d09bbfa1cf87d64a1108`  
		Last Modified: Sat, 22 Feb 2025 00:32:42 GMT  
		Size: 1.2 MB (1245268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b49e89cf77efc47a7250f3af153069fc9a2d7696d280b7f9b2ef3ef434a4e1b`  
		Last Modified: Sat, 22 Feb 2025 00:32:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615b1475c4f9cc790d1525380d666d53c7507c87e777e647ed0287598efa3d48`  
		Last Modified: Sat, 22 Feb 2025 00:32:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:b668a646c910c9b5f5c8f752e53b49deb2a1ad6e7ebdc0526adbcf9d299b4ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49e0834cecf5abf237b771c3850e94ba86e05385ccbab4b91cb3d9f063af010c`

```dockerfile
```

-	Layers:
	-	`sha256:cb0b22895c3619cafd6dca713774db852bfe31b3adb4ba3ec6a66838eac945e3`  
		Last Modified: Sat, 22 Feb 2025 00:32:42 GMT  
		Size: 2.3 MB (2292845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d7f06daebcc005d1c5979488409050e03ba04720bf9c424588de02b684b8c03`  
		Last Modified: Sat, 22 Feb 2025 00:32:42 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ecdac108a456c82920f95b934edd7b2c3abf62adf96adac7b99767591b6fecf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31658335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c4d6a0c65f7a9206b9660b5d79d29c8183bb45cef6fa838bbc17493f7085b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85c190a9b2b110c5e0805ab31e5792459e717a286856047e10f45423d8231dd`  
		Last Modified: Wed, 05 Feb 2025 20:31:30 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d150df6d26f3098fb2b4554249a49c854dd5acf5f8255fcf725a970fdbcccbe`  
		Last Modified: Wed, 05 Feb 2025 20:31:31 GMT  
		Size: 2.4 MB (2355307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d34310d49ce6a8c13f0814ea92dbb59638c73a98d899a8f489b4cdba59cf1a4`  
		Last Modified: Sat, 22 Feb 2025 00:31:38 GMT  
		Size: 1.3 MB (1260635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d933eb164ac02e89a9ec663d27d218ab0e489db96ca622ac5023f149bb767f2`  
		Last Modified: Sat, 22 Feb 2025 00:31:38 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3955731998caab6a7273ad7e2b63e663ae711d2f45416977f29c9df6c3a5771`  
		Last Modified: Sat, 22 Feb 2025 00:31:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:b0998d3901cbf4dc98a6f5d0254d7f2115d3d110c1de81a5ec4cc6b56c1afe39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:351b12242d29e072aaf887e69b6b36f8b86fb05d09e37cd2a338014241525536`

```dockerfile
```

-	Layers:
	-	`sha256:c6ec4332029f56a214be68a1da8a91d6170bcc2d2d243daae2353e3cb0baeaae`  
		Last Modified: Sat, 22 Feb 2025 00:31:38 GMT  
		Size: 2.3 MB (2289622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c51e1294036728fb8cdc19970c532c2ced14c50e64984ed76d91eda1e1a61c92`  
		Last Modified: Sat, 22 Feb 2025 00:31:38 GMT  
		Size: 21.4 KB (21419 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:ef53c35087afb0499842bedf1fbfa79d5b842f19779b63afa6f1f025a9d5a6ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32956089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e8028b418ebc438bf613b1826c1c627b9c70d0ceba487e067f06ce1140efa93`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a2635855d79b555abffa55c629412da2c4134f2a8ccd4a315c0b6f92b579ae`  
		Last Modified: Sat, 22 Feb 2025 00:31:19 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b44d66689e77fbfe0bc0a0c7e8a45833882611191361e49b6a48030dfbda7bb`  
		Last Modified: Sat, 22 Feb 2025 00:31:20 GMT  
		Size: 2.5 MB (2500720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22086dfd31db842102b740e2bc68682931021ff3fb6491253f9087ca1df6f3cd`  
		Last Modified: Sat, 22 Feb 2025 00:31:19 GMT  
		Size: 1.3 MB (1266399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0d2b64685890c225d3c813b7c867d2d96fb3719d43d4edb206375e55ee6a32`  
		Last Modified: Sat, 22 Feb 2025 00:31:19 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365bc8ba2a50069e758df20bd1b42ff192846fbb115b9edb0cda2fc43fdb2600`  
		Last Modified: Sat, 22 Feb 2025 00:31:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:26ed9f96a812fb5af80816d45e029522166082e249f638019205191bb5b02cb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb94ae18d76a538788c16c601bc76b3509862697a1367bd2fa42cfd5ab18e5b9`

```dockerfile
```

-	Layers:
	-	`sha256:ece746d0e00e98b51635c1914e1aeab67cf6208f531559f2af8346d9e8f40606`  
		Last Modified: Sat, 22 Feb 2025 00:31:20 GMT  
		Size: 2.3 MB (2286406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31ecb87a15a354348411689e2d7bf34846d275e3db9f99b9d2fd53c5d931d382`  
		Last Modified: Sat, 22 Feb 2025 00:31:19 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:61282eccad654d1d03273cc2fb02a4db982d36e9e0ff866eab773795e106ec8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31692298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c72f2790d1441f439ca292b3f0077287e8f93af8f30b6ae44f467f4728aecf0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:60fe4951c23056512065fcf1948d3167c5aa5d83d4bfd2829494b7d09b4fe661`  
		Last Modified: Tue, 04 Feb 2025 01:38:47 GMT  
		Size: 28.5 MB (28486581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006e6bf1f5c579c425dd6a7045b45795f463f886bf4ee3532c5964da484e77c4`  
		Last Modified: Tue, 04 Feb 2025 05:36:04 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa88afbdcfa1d52adc83e6c274708611503deecc6240cf640db7eb23e1999a30`  
		Last Modified: Sat, 22 Feb 2025 00:36:16 GMT  
		Size: 1.9 MB (1943183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dcb0fa418dcf8d7cccdc41a73ad2063c2ae4bf810f2b8a7c67a8ead47c9d684`  
		Last Modified: Sat, 22 Feb 2025 00:36:16 GMT  
		Size: 1.3 MB (1261025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f222082e64a60018ba8bea35cd86f7254591435953a40e022541df5dd42e64`  
		Last Modified: Sat, 22 Feb 2025 00:36:16 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f367b09aa255318629e01e577d62f20d50bcc2cb49cd5519a9c1b68c0829b4e`  
		Last Modified: Sat, 22 Feb 2025 00:36:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:c3872907481511259937b839ceb7f595c2edbf6f47b17ae6cd4e1a10c2456f41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48598526c0aff23b0715615e1f0cd1c35b57f4de0e9b13447903c812540b5683`

```dockerfile
```

-	Layers:
	-	`sha256:308d9f10522a8efc39d94eb5a4f47a8b547bdf8ef47d53a710264ade572dc85b`  
		Last Modified: Sat, 22 Feb 2025 00:36:16 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:10e27fa85f13d51af4a481e4778b04b3b80d506a129aab984fc5d5dab919a8e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36085879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac4b53721162a6ae89b5b0e96dfb4e7ba41127c795c3b9689c36040284ea691`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 01:38:01 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2deccedfff592cdf0e60a1a0f23cfa011cc09854b3b8fd5979a2215801fe859a`  
		Last Modified: Wed, 05 Feb 2025 20:30:01 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f77d137ef9ee5f1f27684f14e816a1f088dfffc4476ab6d02ffa5d251db059`  
		Last Modified: Wed, 05 Feb 2025 20:30:01 GMT  
		Size: 2.7 MB (2708582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163ac5a13dc4a349552e8a728dbfe7a6747c6c194c8f3af433fa8f89ca89614e`  
		Last Modified: Sat, 22 Feb 2025 00:31:22 GMT  
		Size: 1.3 MB (1331006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52cbf6e5ffb6677cc60835d4722667a4e9ac72b9ede1a0a9f282e56abf5dc63`  
		Last Modified: Sat, 22 Feb 2025 00:31:22 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7111ad13f64383b6c5b3388ba5cd00d3804080114fc716c24ebe318a0b45d350`  
		Last Modified: Sat, 22 Feb 2025 00:31:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:8ec0ef0ee501fe9bf349dbf63dce11035a606876a565ee69fd5055418b09d08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8468c14d9febe1b645497e9293a93d6b378bbdb3147a6c0bb18f23a907241bda`

```dockerfile
```

-	Layers:
	-	`sha256:ebd1905c7f20a0d3d102c7b17f531860a3ac45d105b42f0669754a3230ae5fe2`  
		Last Modified: Sat, 22 Feb 2025 00:31:22 GMT  
		Size: 2.3 MB (2293679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b94eff9fb2c5e828a7e6a3ec42729e322d3cc31372e12a5ad1b7eb9761e30a8`  
		Last Modified: Sat, 22 Feb 2025 00:31:21 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:10f8a97eb4da432625002966d78d3993a95f073fb5077a1a4f3cc5a76cd6bab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30261694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a090e8956a7fcbb8b2f590626585d48385828d83d3925e0f8127f400e7c074`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85c3e9bcd86da2086f455efe77a700fe40645a11782885cb35509ae6da968af`  
		Last Modified: Wed, 05 Feb 2025 20:31:33 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25653c174b0d3f4223a55d32a6e019a0a071b0f939c2043a5f3ca38897b6a47`  
		Last Modified: Wed, 05 Feb 2025 20:31:33 GMT  
		Size: 2.2 MB (2156373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86dc255a71b2a050391adb8d18b925df4b93b704a5d38583f893d4c1e1babe1`  
		Last Modified: Sat, 22 Feb 2025 00:31:32 GMT  
		Size: 1.2 MB (1245183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848092fc56244055b7ee89f53de1c07230b0bd2651e37dea23770fc8089383db`  
		Last Modified: Sat, 22 Feb 2025 00:31:33 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab89cd679a4ffa81bbb3cbb213b25b557649024534fef1f253bdaf6f65799c05`  
		Last Modified: Sat, 22 Feb 2025 00:31:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:b70e906e72967b0e6ed1c8be6d754bf62e2ee68350435a171d182ba6efc9dd70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f906cfd918535c7f2f1b3af08ff4c29ffce9b1c176c8ca28e5f3333bd612aaa3`

```dockerfile
```

-	Layers:
	-	`sha256:0fcec7672387ec22fd81d2b2a8c5de99e7aae50b53faf5bf629ded84a19776d1`  
		Last Modified: Sat, 22 Feb 2025 00:31:32 GMT  
		Size: 2.3 MB (2289021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5d0bd85e2270f2d197500c26d3f1fdc8af08248f560b4dfcee81130a4a3748f`  
		Last Modified: Sat, 22 Feb 2025 00:31:32 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6`

```console
$ docker pull memcached@sha256:685ba31ae4994ff6daf16d21142346dbd828d0dfbeff3cbc7a7f9b4f5f93b2dd
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
$ docker pull memcached@sha256:bfe5fd0aac5c89b8022c2620abc0a1118cb84d68a74a437ac1fef55be567a23f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31972590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a69266e53d188956df96699ee7bd22b00986730a190789881f82a593361bfc16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d569cc07bddca59980d45ae28a8bfede7584cdca655fad52796e829ac8b7fee`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c58bc9b838a5c291945e3cd889cc93151a03fc70e079914ba998f26239ef2e`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 2.5 MB (2491762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67c97f377dc045ebb683ab2bf6d771520192351043ab7fc20c63ed1a997f84b`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 1.3 MB (1267012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8282d3a602638805126b2e682263fb38ca402e3beaa3a047ed0add1bf754fdb8`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cd8dd518d1c91daec2bae1887feb80b6473e0fe5e6846ddb613387e8311c64`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:ffc24940329fbd38d3efa10fbceb92bc75b8c8e3861170180d934c88ad8659b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a2b67f33d20bb90a8a9305d3ef143d1332d728823aeba14947ec779d5da211`

```dockerfile
```

-	Layers:
	-	`sha256:6ff1804b1ee0e0da242ef1ef47226adb9ac0a4172528e4ac5501443a5e6f3487`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 2.3 MB (2289307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6460f3cc3f151e357a1fa273d42ff4f884c9d2b093c4763cb3c73595fb554fa5`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:abee184952eb3cfc02bd6555047901e0e27fe9379eaddc25acb7805ac3c01e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29079400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c55ad492b5523a9106a2cef2d811d102d5d88a74110653f3187894c060ae61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aa8576c673e5a651f7450bee7603a12ac6168051fdd5b2411678987e180cad6e`  
		Last Modified: Tue, 04 Feb 2025 01:38:28 GMT  
		Size: 25.7 MB (25736549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d03c1f12f429fcd661498f32bc4e1c1e6a1e4189bd6014e71da057147e2286`  
		Last Modified: Tue, 04 Feb 2025 04:58:18 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7e25c626324a280a0e7be83a5642bb48a551515d4c38cb544c66904fcf10bb`  
		Last Modified: Tue, 04 Feb 2025 04:58:19 GMT  
		Size: 2.1 MB (2096073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b068d3f71231f010921a5b6713e177cb20b1838ecd63d09bbfa1cf87d64a1108`  
		Last Modified: Sat, 22 Feb 2025 00:32:42 GMT  
		Size: 1.2 MB (1245268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b49e89cf77efc47a7250f3af153069fc9a2d7696d280b7f9b2ef3ef434a4e1b`  
		Last Modified: Sat, 22 Feb 2025 00:32:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615b1475c4f9cc790d1525380d666d53c7507c87e777e647ed0287598efa3d48`  
		Last Modified: Sat, 22 Feb 2025 00:32:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:b668a646c910c9b5f5c8f752e53b49deb2a1ad6e7ebdc0526adbcf9d299b4ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49e0834cecf5abf237b771c3850e94ba86e05385ccbab4b91cb3d9f063af010c`

```dockerfile
```

-	Layers:
	-	`sha256:cb0b22895c3619cafd6dca713774db852bfe31b3adb4ba3ec6a66838eac945e3`  
		Last Modified: Sat, 22 Feb 2025 00:32:42 GMT  
		Size: 2.3 MB (2292845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d7f06daebcc005d1c5979488409050e03ba04720bf9c424588de02b684b8c03`  
		Last Modified: Sat, 22 Feb 2025 00:32:42 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ecdac108a456c82920f95b934edd7b2c3abf62adf96adac7b99767591b6fecf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31658335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c4d6a0c65f7a9206b9660b5d79d29c8183bb45cef6fa838bbc17493f7085b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85c190a9b2b110c5e0805ab31e5792459e717a286856047e10f45423d8231dd`  
		Last Modified: Wed, 05 Feb 2025 20:31:30 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d150df6d26f3098fb2b4554249a49c854dd5acf5f8255fcf725a970fdbcccbe`  
		Last Modified: Wed, 05 Feb 2025 20:31:31 GMT  
		Size: 2.4 MB (2355307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d34310d49ce6a8c13f0814ea92dbb59638c73a98d899a8f489b4cdba59cf1a4`  
		Last Modified: Sat, 22 Feb 2025 00:31:38 GMT  
		Size: 1.3 MB (1260635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d933eb164ac02e89a9ec663d27d218ab0e489db96ca622ac5023f149bb767f2`  
		Last Modified: Sat, 22 Feb 2025 00:31:38 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3955731998caab6a7273ad7e2b63e663ae711d2f45416977f29c9df6c3a5771`  
		Last Modified: Sat, 22 Feb 2025 00:31:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:b0998d3901cbf4dc98a6f5d0254d7f2115d3d110c1de81a5ec4cc6b56c1afe39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:351b12242d29e072aaf887e69b6b36f8b86fb05d09e37cd2a338014241525536`

```dockerfile
```

-	Layers:
	-	`sha256:c6ec4332029f56a214be68a1da8a91d6170bcc2d2d243daae2353e3cb0baeaae`  
		Last Modified: Sat, 22 Feb 2025 00:31:38 GMT  
		Size: 2.3 MB (2289622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c51e1294036728fb8cdc19970c532c2ced14c50e64984ed76d91eda1e1a61c92`  
		Last Modified: Sat, 22 Feb 2025 00:31:38 GMT  
		Size: 21.4 KB (21419 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; 386

```console
$ docker pull memcached@sha256:ef53c35087afb0499842bedf1fbfa79d5b842f19779b63afa6f1f025a9d5a6ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32956089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e8028b418ebc438bf613b1826c1c627b9c70d0ceba487e067f06ce1140efa93`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a2635855d79b555abffa55c629412da2c4134f2a8ccd4a315c0b6f92b579ae`  
		Last Modified: Sat, 22 Feb 2025 00:31:19 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b44d66689e77fbfe0bc0a0c7e8a45833882611191361e49b6a48030dfbda7bb`  
		Last Modified: Sat, 22 Feb 2025 00:31:20 GMT  
		Size: 2.5 MB (2500720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22086dfd31db842102b740e2bc68682931021ff3fb6491253f9087ca1df6f3cd`  
		Last Modified: Sat, 22 Feb 2025 00:31:19 GMT  
		Size: 1.3 MB (1266399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0d2b64685890c225d3c813b7c867d2d96fb3719d43d4edb206375e55ee6a32`  
		Last Modified: Sat, 22 Feb 2025 00:31:19 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365bc8ba2a50069e758df20bd1b42ff192846fbb115b9edb0cda2fc43fdb2600`  
		Last Modified: Sat, 22 Feb 2025 00:31:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:26ed9f96a812fb5af80816d45e029522166082e249f638019205191bb5b02cb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb94ae18d76a538788c16c601bc76b3509862697a1367bd2fa42cfd5ab18e5b9`

```dockerfile
```

-	Layers:
	-	`sha256:ece746d0e00e98b51635c1914e1aeab67cf6208f531559f2af8346d9e8f40606`  
		Last Modified: Sat, 22 Feb 2025 00:31:20 GMT  
		Size: 2.3 MB (2286406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31ecb87a15a354348411689e2d7bf34846d275e3db9f99b9d2fd53c5d931d382`  
		Last Modified: Sat, 22 Feb 2025 00:31:19 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; mips64le

```console
$ docker pull memcached@sha256:61282eccad654d1d03273cc2fb02a4db982d36e9e0ff866eab773795e106ec8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31692298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c72f2790d1441f439ca292b3f0077287e8f93af8f30b6ae44f467f4728aecf0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:60fe4951c23056512065fcf1948d3167c5aa5d83d4bfd2829494b7d09b4fe661`  
		Last Modified: Tue, 04 Feb 2025 01:38:47 GMT  
		Size: 28.5 MB (28486581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006e6bf1f5c579c425dd6a7045b45795f463f886bf4ee3532c5964da484e77c4`  
		Last Modified: Tue, 04 Feb 2025 05:36:04 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa88afbdcfa1d52adc83e6c274708611503deecc6240cf640db7eb23e1999a30`  
		Last Modified: Sat, 22 Feb 2025 00:36:16 GMT  
		Size: 1.9 MB (1943183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dcb0fa418dcf8d7cccdc41a73ad2063c2ae4bf810f2b8a7c67a8ead47c9d684`  
		Last Modified: Sat, 22 Feb 2025 00:36:16 GMT  
		Size: 1.3 MB (1261025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f222082e64a60018ba8bea35cd86f7254591435953a40e022541df5dd42e64`  
		Last Modified: Sat, 22 Feb 2025 00:36:16 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f367b09aa255318629e01e577d62f20d50bcc2cb49cd5519a9c1b68c0829b4e`  
		Last Modified: Sat, 22 Feb 2025 00:36:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:c3872907481511259937b839ceb7f595c2edbf6f47b17ae6cd4e1a10c2456f41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48598526c0aff23b0715615e1f0cd1c35b57f4de0e9b13447903c812540b5683`

```dockerfile
```

-	Layers:
	-	`sha256:308d9f10522a8efc39d94eb5a4f47a8b547bdf8ef47d53a710264ade572dc85b`  
		Last Modified: Sat, 22 Feb 2025 00:36:16 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:10e27fa85f13d51af4a481e4778b04b3b80d506a129aab984fc5d5dab919a8e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36085879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac4b53721162a6ae89b5b0e96dfb4e7ba41127c795c3b9689c36040284ea691`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 01:38:01 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2deccedfff592cdf0e60a1a0f23cfa011cc09854b3b8fd5979a2215801fe859a`  
		Last Modified: Wed, 05 Feb 2025 20:30:01 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f77d137ef9ee5f1f27684f14e816a1f088dfffc4476ab6d02ffa5d251db059`  
		Last Modified: Wed, 05 Feb 2025 20:30:01 GMT  
		Size: 2.7 MB (2708582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163ac5a13dc4a349552e8a728dbfe7a6747c6c194c8f3af433fa8f89ca89614e`  
		Last Modified: Sat, 22 Feb 2025 00:31:22 GMT  
		Size: 1.3 MB (1331006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52cbf6e5ffb6677cc60835d4722667a4e9ac72b9ede1a0a9f282e56abf5dc63`  
		Last Modified: Sat, 22 Feb 2025 00:31:22 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7111ad13f64383b6c5b3388ba5cd00d3804080114fc716c24ebe318a0b45d350`  
		Last Modified: Sat, 22 Feb 2025 00:31:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:8ec0ef0ee501fe9bf349dbf63dce11035a606876a565ee69fd5055418b09d08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8468c14d9febe1b645497e9293a93d6b378bbdb3147a6c0bb18f23a907241bda`

```dockerfile
```

-	Layers:
	-	`sha256:ebd1905c7f20a0d3d102c7b17f531860a3ac45d105b42f0669754a3230ae5fe2`  
		Last Modified: Sat, 22 Feb 2025 00:31:22 GMT  
		Size: 2.3 MB (2293679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b94eff9fb2c5e828a7e6a3ec42729e322d3cc31372e12a5ad1b7eb9761e30a8`  
		Last Modified: Sat, 22 Feb 2025 00:31:21 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; s390x

```console
$ docker pull memcached@sha256:10f8a97eb4da432625002966d78d3993a95f073fb5077a1a4f3cc5a76cd6bab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30261694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a090e8956a7fcbb8b2f590626585d48385828d83d3925e0f8127f400e7c074`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85c3e9bcd86da2086f455efe77a700fe40645a11782885cb35509ae6da968af`  
		Last Modified: Wed, 05 Feb 2025 20:31:33 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25653c174b0d3f4223a55d32a6e019a0a071b0f939c2043a5f3ca38897b6a47`  
		Last Modified: Wed, 05 Feb 2025 20:31:33 GMT  
		Size: 2.2 MB (2156373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86dc255a71b2a050391adb8d18b925df4b93b704a5d38583f893d4c1e1babe1`  
		Last Modified: Sat, 22 Feb 2025 00:31:32 GMT  
		Size: 1.2 MB (1245183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848092fc56244055b7ee89f53de1c07230b0bd2651e37dea23770fc8089383db`  
		Last Modified: Sat, 22 Feb 2025 00:31:33 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab89cd679a4ffa81bbb3cbb213b25b557649024534fef1f253bdaf6f65799c05`  
		Last Modified: Sat, 22 Feb 2025 00:31:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:b70e906e72967b0e6ed1c8be6d754bf62e2ee68350435a171d182ba6efc9dd70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f906cfd918535c7f2f1b3af08ff4c29ffce9b1c176c8ca28e5f3333bd612aaa3`

```dockerfile
```

-	Layers:
	-	`sha256:0fcec7672387ec22fd81d2b2a8c5de99e7aae50b53faf5bf629ded84a19776d1`  
		Last Modified: Sat, 22 Feb 2025 00:31:32 GMT  
		Size: 2.3 MB (2289021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5d0bd85e2270f2d197500c26d3f1fdc8af08248f560b4dfcee81130a4a3748f`  
		Last Modified: Sat, 22 Feb 2025 00:31:32 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine`

```console
$ docker pull memcached@sha256:c2efa3700db8d6768b4fc98e064843aa0c98705e9bb3e63a70768d7a6a5b6a02
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
$ docker pull memcached@sha256:787e9120e36559c9aba4cce621188072d00e159bc596fe803c00037f3702c22f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4716929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21a7aa256b160c9c42cce498615225db46d75b42d27b180c3879e9e7d1fbd92`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3e9f8182c72be0cf629032be09e1b5da2b94a8a03a202110036eae2fa538b9`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc58417b03bbd338e8fab898ba984cef01fdb2b2960ae862ecc89bc258a0b981`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 104.7 KB (104690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82369477a539cf4bc0cfd0063cb20ce85cf36442b532dbde15f71a6061abc106`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 968.6 KB (968644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0261a578c93ccd99ba866def61b28a43cc2938598cbc307011db812c246ee206`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cd8dd518d1c91daec2bae1887feb80b6473e0fe5e6846ddb613387e8311c64`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:abae77e9a8d50f01601a4188494f6d7a2e3442e7258fa213a581d2e281fc02c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c452640b5e4fe4e1b31941228c0615b396ec62a56794e1c63e1b9326c5cbf60a`

```dockerfile
```

-	Layers:
	-	`sha256:297387df1b0d33fd74438a8273ab5e20a2a8193785491bcc9b6ad3e03d9c1aa6`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 93.6 KB (93633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0d579b1ca91bec4046749a5bf7a3549239008c1a1083ec2213a3c6004a5725b`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 19.6 KB (19570 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:22169a1786f676798782408232c35b71e12bd32b10164e81c0b32da6143641c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5083533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add144e03275b9c89bb582ad307446fa229055731caf45650896ed6d340a839a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b3b947aa71cef021cd9306b1f24a44554e8d663c8530dd36d42b94a883f4c9`  
		Last Modified: Fri, 14 Feb 2025 19:50:13 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6014feb1c2bb2b6c63e9a7b16a3850c447422bdad6e65b302925b8547b23c192`  
		Last Modified: Fri, 14 Feb 2025 19:50:13 GMT  
		Size: 120.8 KB (120780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b307ec9e1116f91be05519ed18f8206fb49e72d80c7a04638004cf9a82ac2a77`  
		Last Modified: Sat, 22 Feb 2025 00:34:08 GMT  
		Size: 968.4 KB (968374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b643c0752d8cb8b54b8a8d095693feba316ac84b1fd17048fc0189599bc5e1d`  
		Last Modified: Sat, 22 Feb 2025 00:34:08 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38c21d127cb51320d77ca177167435601efbd6ddc02a49c2876aac2884a0109`  
		Last Modified: Sat, 22 Feb 2025 00:34:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:bef45ca6f335dcb09118c5ee88802a722f482af24a9afa8974e7b4800b0fd39f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b1eae2531d72df59778c8c8ac7fecb6d4b6b408b9192cc6ac7d77a5e98128d7`

```dockerfile
```

-	Layers:
	-	`sha256:f675a5a746afeb63892d91271eccac08f3a01bbf6dae0926114e83673197e1be`  
		Last Modified: Sat, 22 Feb 2025 00:34:08 GMT  
		Size: 93.7 KB (93737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74fc4c03468266c50ce86e1314f4c6f45903d6c98465180f75f826dfb54cfcfd`  
		Last Modified: Sat, 22 Feb 2025 00:34:07 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:46aa92b9d94ea6493f4f5f098e6b1de64f3e8c450eb6440d5bf59f4e1f2ead69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4534801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac2f67d3ec71890e3d6bd391e98b4da571242348ac135e99bcef39979486b34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0216147e703738541dd8987b9b2bc147da47c311b00a06feb265c9f0abf707`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab4b25598c42e6f016cb0a26803d39acd19d7871e0b092cbefd2f8856b0a112`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 109.5 KB (109489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5589cc68943165ccc1b90f645ea08e4c8bb401c6ea2db3506bd1309fd04158`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 960.3 KB (960336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f9697b895d35627f393cf365d336aad6ff6d5d9d767f2ab73d2696751527c1`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a049f6eb832cc266adfa607fe5c42c0710850885d375ee2fd2b22a9add7d29b7`  
		Last Modified: Sat, 22 Feb 2025 00:31:07 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:f9710d1f921ddd802f69f2eb77ae2baa0a046307d13215474dd3f369124034e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de341f780812144f1c4528778277abc1e0f979937153200813e3e66b11d01d02`

```dockerfile
```

-	Layers:
	-	`sha256:4bd1b00215d14ae69987d6066982bb958dbe599471eebf5233fbc9512b4a5fcd`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 93.6 KB (93588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1126652f997b244e12c038e90d03bc059f60adbf626ea9d38c90259a5920775c`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 19.5 KB (19512 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:e3fbb21940e6ecf6e09878be1fdb50cfe7d0ca132112d7439d1c3f266f6b8b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4706934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ab0bd6e09f5b37468b8ae688526c599c21045baf0b0b8bc98ec097e5267b28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deee0b86774e394f5e07eff435a072bdde8922ec1757ef689265af3e1864d632`  
		Last Modified: Fri, 14 Feb 2025 19:42:34 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbafd6c675f155044ba3e5ef96996313b9f05064b966848001c7ea04a9c6048`  
		Last Modified: Fri, 14 Feb 2025 19:42:34 GMT  
		Size: 124.3 KB (124276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56400c974ec4a72a96f97ce1a5828e0ebcb6df76fe5c2f7d8dae29c07223abbf`  
		Last Modified: Sat, 22 Feb 2025 00:34:12 GMT  
		Size: 1.0 MB (1006957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0b9347f26655d1e450da08a0e5a23d5cc368bbfad35a84c643be25c87b2726`  
		Last Modified: Sat, 22 Feb 2025 00:34:11 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5064388d99c64e09f330fcec8ffba565524c380566e6a70fb34aedbf84880f8`  
		Last Modified: Sat, 22 Feb 2025 00:34:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:94cd05711888081e81791841a80e96d16b22ba21e835ba80d125ed65d295b947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84057bf494e545f78faa4d02b570fd42a27b6c3a616d2e07c06013f7125b0ec2`

```dockerfile
```

-	Layers:
	-	`sha256:f969bce286e2478dcbbe6690408d5b20920506d09783024c5e824272ee16cc9e`  
		Last Modified: Sat, 22 Feb 2025 00:34:11 GMT  
		Size: 91.7 KB (91740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93bbfb8bcbd31cfc88a941030e8e18f43fdb73c07293481a932203cb3a25e504`  
		Last Modified: Sat, 22 Feb 2025 00:34:11 GMT  
		Size: 19.6 KB (19648 bytes)  
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
$ docker pull memcached@sha256:0087cdeb03b579438e5e722b991d7e3ee891e4770b26ceeff27c4401cf654657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4571101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2bc2ef8da87893bf85939bd479692ebd280f9d840686e5fdc00089b536aad65`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d658470bb26df23b8a940bc8e53f6c8b685a81ce47a086f683e29b63a6bac496`  
		Last Modified: Fri, 14 Feb 2025 19:44:23 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a07c51d6bc9e389360e3ccba6d95f5697fdd3366a1ac093d59ce54e0da2550`  
		Last Modified: Fri, 14 Feb 2025 19:44:23 GMT  
		Size: 113.5 KB (113462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91fbcb7a7ec7da4c7e8e462c545d152b5a079ef1360a1d05df018c7f78da31e7`  
		Last Modified: Sat, 22 Feb 2025 00:35:17 GMT  
		Size: 988.7 KB (988725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539207d8d3aff51a577331b44e1e08e93ad1330f182ca154c800fa3cc40b77bd`  
		Last Modified: Sat, 22 Feb 2025 00:35:17 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236b320beb51084e2e1b6b838aa193caf573a4292b1353bba1a0cdf076b82db6`  
		Last Modified: Sat, 22 Feb 2025 00:35:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9bd727783dc634399ded38736a232ba7801976d1b0096e07194f53a8f82de528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 KB (111252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7030d08f1e1857ea22b2d774577cb0cb56dd6eb8f7b7ff94fb262e44551c1c`

```dockerfile
```

-	Layers:
	-	`sha256:b7ec10e807d6f8925ef59303e53fc02069fd4a687b1baa66cf3164590cb29d4b`  
		Last Modified: Sat, 22 Feb 2025 00:35:17 GMT  
		Size: 91.7 KB (91682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25a3bb1b2ff42fd2d2a4c3e88ec8af248b5df8c2a42a871dcec17d8a1deb6dbb`  
		Last Modified: Sat, 22 Feb 2025 00:35:17 GMT  
		Size: 19.6 KB (19570 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine3.21`

```console
$ docker pull memcached@sha256:4fb13e4757387000230be124c5a74f107abfd1f65e2526f4c627110d666bf5a3
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
$ docker pull memcached@sha256:787e9120e36559c9aba4cce621188072d00e159bc596fe803c00037f3702c22f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4716929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21a7aa256b160c9c42cce498615225db46d75b42d27b180c3879e9e7d1fbd92`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3e9f8182c72be0cf629032be09e1b5da2b94a8a03a202110036eae2fa538b9`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc58417b03bbd338e8fab898ba984cef01fdb2b2960ae862ecc89bc258a0b981`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 104.7 KB (104690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82369477a539cf4bc0cfd0063cb20ce85cf36442b532dbde15f71a6061abc106`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 968.6 KB (968644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0261a578c93ccd99ba866def61b28a43cc2938598cbc307011db812c246ee206`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cd8dd518d1c91daec2bae1887feb80b6473e0fe5e6846ddb613387e8311c64`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:abae77e9a8d50f01601a4188494f6d7a2e3442e7258fa213a581d2e281fc02c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c452640b5e4fe4e1b31941228c0615b396ec62a56794e1c63e1b9326c5cbf60a`

```dockerfile
```

-	Layers:
	-	`sha256:297387df1b0d33fd74438a8273ab5e20a2a8193785491bcc9b6ad3e03d9c1aa6`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 93.6 KB (93633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0d579b1ca91bec4046749a5bf7a3549239008c1a1083ec2213a3c6004a5725b`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 19.6 KB (19570 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:22169a1786f676798782408232c35b71e12bd32b10164e81c0b32da6143641c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5083533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add144e03275b9c89bb582ad307446fa229055731caf45650896ed6d340a839a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b3b947aa71cef021cd9306b1f24a44554e8d663c8530dd36d42b94a883f4c9`  
		Last Modified: Fri, 14 Feb 2025 19:50:13 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6014feb1c2bb2b6c63e9a7b16a3850c447422bdad6e65b302925b8547b23c192`  
		Last Modified: Fri, 14 Feb 2025 19:50:13 GMT  
		Size: 120.8 KB (120780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b307ec9e1116f91be05519ed18f8206fb49e72d80c7a04638004cf9a82ac2a77`  
		Last Modified: Sat, 22 Feb 2025 00:34:08 GMT  
		Size: 968.4 KB (968374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b643c0752d8cb8b54b8a8d095693feba316ac84b1fd17048fc0189599bc5e1d`  
		Last Modified: Sat, 22 Feb 2025 00:34:08 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38c21d127cb51320d77ca177167435601efbd6ddc02a49c2876aac2884a0109`  
		Last Modified: Sat, 22 Feb 2025 00:34:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:bef45ca6f335dcb09118c5ee88802a722f482af24a9afa8974e7b4800b0fd39f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b1eae2531d72df59778c8c8ac7fecb6d4b6b408b9192cc6ac7d77a5e98128d7`

```dockerfile
```

-	Layers:
	-	`sha256:f675a5a746afeb63892d91271eccac08f3a01bbf6dae0926114e83673197e1be`  
		Last Modified: Sat, 22 Feb 2025 00:34:08 GMT  
		Size: 93.7 KB (93737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74fc4c03468266c50ce86e1314f4c6f45903d6c98465180f75f826dfb54cfcfd`  
		Last Modified: Sat, 22 Feb 2025 00:34:07 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.21` - linux; 386

```console
$ docker pull memcached@sha256:46aa92b9d94ea6493f4f5f098e6b1de64f3e8c450eb6440d5bf59f4e1f2ead69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4534801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac2f67d3ec71890e3d6bd391e98b4da571242348ac135e99bcef39979486b34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0216147e703738541dd8987b9b2bc147da47c311b00a06feb265c9f0abf707`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab4b25598c42e6f016cb0a26803d39acd19d7871e0b092cbefd2f8856b0a112`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 109.5 KB (109489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5589cc68943165ccc1b90f645ea08e4c8bb401c6ea2db3506bd1309fd04158`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 960.3 KB (960336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f9697b895d35627f393cf365d336aad6ff6d5d9d767f2ab73d2696751527c1`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a049f6eb832cc266adfa607fe5c42c0710850885d375ee2fd2b22a9add7d29b7`  
		Last Modified: Sat, 22 Feb 2025 00:31:07 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:f9710d1f921ddd802f69f2eb77ae2baa0a046307d13215474dd3f369124034e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de341f780812144f1c4528778277abc1e0f979937153200813e3e66b11d01d02`

```dockerfile
```

-	Layers:
	-	`sha256:4bd1b00215d14ae69987d6066982bb958dbe599471eebf5233fbc9512b4a5fcd`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 93.6 KB (93588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1126652f997b244e12c038e90d03bc059f60adbf626ea9d38c90259a5920775c`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 19.5 KB (19512 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.21` - linux; ppc64le

```console
$ docker pull memcached@sha256:e3fbb21940e6ecf6e09878be1fdb50cfe7d0ca132112d7439d1c3f266f6b8b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4706934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ab0bd6e09f5b37468b8ae688526c599c21045baf0b0b8bc98ec097e5267b28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deee0b86774e394f5e07eff435a072bdde8922ec1757ef689265af3e1864d632`  
		Last Modified: Fri, 14 Feb 2025 19:42:34 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbafd6c675f155044ba3e5ef96996313b9f05064b966848001c7ea04a9c6048`  
		Last Modified: Fri, 14 Feb 2025 19:42:34 GMT  
		Size: 124.3 KB (124276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56400c974ec4a72a96f97ce1a5828e0ebcb6df76fe5c2f7d8dae29c07223abbf`  
		Last Modified: Sat, 22 Feb 2025 00:34:12 GMT  
		Size: 1.0 MB (1006957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0b9347f26655d1e450da08a0e5a23d5cc368bbfad35a84c643be25c87b2726`  
		Last Modified: Sat, 22 Feb 2025 00:34:11 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5064388d99c64e09f330fcec8ffba565524c380566e6a70fb34aedbf84880f8`  
		Last Modified: Sat, 22 Feb 2025 00:34:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:94cd05711888081e81791841a80e96d16b22ba21e835ba80d125ed65d295b947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84057bf494e545f78faa4d02b570fd42a27b6c3a616d2e07c06013f7125b0ec2`

```dockerfile
```

-	Layers:
	-	`sha256:f969bce286e2478dcbbe6690408d5b20920506d09783024c5e824272ee16cc9e`  
		Last Modified: Sat, 22 Feb 2025 00:34:11 GMT  
		Size: 91.7 KB (91740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93bbfb8bcbd31cfc88a941030e8e18f43fdb73c07293481a932203cb3a25e504`  
		Last Modified: Sat, 22 Feb 2025 00:34:11 GMT  
		Size: 19.6 KB (19648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.21` - linux; s390x

```console
$ docker pull memcached@sha256:0087cdeb03b579438e5e722b991d7e3ee891e4770b26ceeff27c4401cf654657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4571101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2bc2ef8da87893bf85939bd479692ebd280f9d840686e5fdc00089b536aad65`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d658470bb26df23b8a940bc8e53f6c8b685a81ce47a086f683e29b63a6bac496`  
		Last Modified: Fri, 14 Feb 2025 19:44:23 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a07c51d6bc9e389360e3ccba6d95f5697fdd3366a1ac093d59ce54e0da2550`  
		Last Modified: Fri, 14 Feb 2025 19:44:23 GMT  
		Size: 113.5 KB (113462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91fbcb7a7ec7da4c7e8e462c545d152b5a079ef1360a1d05df018c7f78da31e7`  
		Last Modified: Sat, 22 Feb 2025 00:35:17 GMT  
		Size: 988.7 KB (988725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539207d8d3aff51a577331b44e1e08e93ad1330f182ca154c800fa3cc40b77bd`  
		Last Modified: Sat, 22 Feb 2025 00:35:17 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236b320beb51084e2e1b6b838aa193caf573a4292b1353bba1a0cdf076b82db6`  
		Last Modified: Sat, 22 Feb 2025 00:35:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:9bd727783dc634399ded38736a232ba7801976d1b0096e07194f53a8f82de528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 KB (111252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7030d08f1e1857ea22b2d774577cb0cb56dd6eb8f7b7ff94fb262e44551c1c`

```dockerfile
```

-	Layers:
	-	`sha256:b7ec10e807d6f8925ef59303e53fc02069fd4a687b1baa66cf3164590cb29d4b`  
		Last Modified: Sat, 22 Feb 2025 00:35:17 GMT  
		Size: 91.7 KB (91682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25a3bb1b2ff42fd2d2a4c3e88ec8af248b5df8c2a42a871dcec17d8a1deb6dbb`  
		Last Modified: Sat, 22 Feb 2025 00:35:17 GMT  
		Size: 19.6 KB (19570 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-bookworm`

```console
$ docker pull memcached@sha256:685ba31ae4994ff6daf16d21142346dbd828d0dfbeff3cbc7a7f9b4f5f93b2dd
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
$ docker pull memcached@sha256:bfe5fd0aac5c89b8022c2620abc0a1118cb84d68a74a437ac1fef55be567a23f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31972590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a69266e53d188956df96699ee7bd22b00986730a190789881f82a593361bfc16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d569cc07bddca59980d45ae28a8bfede7584cdca655fad52796e829ac8b7fee`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c58bc9b838a5c291945e3cd889cc93151a03fc70e079914ba998f26239ef2e`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 2.5 MB (2491762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67c97f377dc045ebb683ab2bf6d771520192351043ab7fc20c63ed1a997f84b`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 1.3 MB (1267012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8282d3a602638805126b2e682263fb38ca402e3beaa3a047ed0add1bf754fdb8`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cd8dd518d1c91daec2bae1887feb80b6473e0fe5e6846ddb613387e8311c64`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:ffc24940329fbd38d3efa10fbceb92bc75b8c8e3861170180d934c88ad8659b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a2b67f33d20bb90a8a9305d3ef143d1332d728823aeba14947ec779d5da211`

```dockerfile
```

-	Layers:
	-	`sha256:6ff1804b1ee0e0da242ef1ef47226adb9ac0a4172528e4ac5501443a5e6f3487`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 2.3 MB (2289307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6460f3cc3f151e357a1fa273d42ff4f884c9d2b093c4763cb3c73595fb554fa5`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:abee184952eb3cfc02bd6555047901e0e27fe9379eaddc25acb7805ac3c01e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29079400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c55ad492b5523a9106a2cef2d811d102d5d88a74110653f3187894c060ae61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aa8576c673e5a651f7450bee7603a12ac6168051fdd5b2411678987e180cad6e`  
		Last Modified: Tue, 04 Feb 2025 01:38:28 GMT  
		Size: 25.7 MB (25736549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d03c1f12f429fcd661498f32bc4e1c1e6a1e4189bd6014e71da057147e2286`  
		Last Modified: Tue, 04 Feb 2025 04:58:18 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7e25c626324a280a0e7be83a5642bb48a551515d4c38cb544c66904fcf10bb`  
		Last Modified: Tue, 04 Feb 2025 04:58:19 GMT  
		Size: 2.1 MB (2096073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b068d3f71231f010921a5b6713e177cb20b1838ecd63d09bbfa1cf87d64a1108`  
		Last Modified: Sat, 22 Feb 2025 00:32:42 GMT  
		Size: 1.2 MB (1245268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b49e89cf77efc47a7250f3af153069fc9a2d7696d280b7f9b2ef3ef434a4e1b`  
		Last Modified: Sat, 22 Feb 2025 00:32:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615b1475c4f9cc790d1525380d666d53c7507c87e777e647ed0287598efa3d48`  
		Last Modified: Sat, 22 Feb 2025 00:32:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:b668a646c910c9b5f5c8f752e53b49deb2a1ad6e7ebdc0526adbcf9d299b4ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49e0834cecf5abf237b771c3850e94ba86e05385ccbab4b91cb3d9f063af010c`

```dockerfile
```

-	Layers:
	-	`sha256:cb0b22895c3619cafd6dca713774db852bfe31b3adb4ba3ec6a66838eac945e3`  
		Last Modified: Sat, 22 Feb 2025 00:32:42 GMT  
		Size: 2.3 MB (2292845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d7f06daebcc005d1c5979488409050e03ba04720bf9c424588de02b684b8c03`  
		Last Modified: Sat, 22 Feb 2025 00:32:42 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ecdac108a456c82920f95b934edd7b2c3abf62adf96adac7b99767591b6fecf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31658335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c4d6a0c65f7a9206b9660b5d79d29c8183bb45cef6fa838bbc17493f7085b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85c190a9b2b110c5e0805ab31e5792459e717a286856047e10f45423d8231dd`  
		Last Modified: Wed, 05 Feb 2025 20:31:30 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d150df6d26f3098fb2b4554249a49c854dd5acf5f8255fcf725a970fdbcccbe`  
		Last Modified: Wed, 05 Feb 2025 20:31:31 GMT  
		Size: 2.4 MB (2355307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d34310d49ce6a8c13f0814ea92dbb59638c73a98d899a8f489b4cdba59cf1a4`  
		Last Modified: Sat, 22 Feb 2025 00:31:38 GMT  
		Size: 1.3 MB (1260635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d933eb164ac02e89a9ec663d27d218ab0e489db96ca622ac5023f149bb767f2`  
		Last Modified: Sat, 22 Feb 2025 00:31:38 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3955731998caab6a7273ad7e2b63e663ae711d2f45416977f29c9df6c3a5771`  
		Last Modified: Sat, 22 Feb 2025 00:31:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:b0998d3901cbf4dc98a6f5d0254d7f2115d3d110c1de81a5ec4cc6b56c1afe39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:351b12242d29e072aaf887e69b6b36f8b86fb05d09e37cd2a338014241525536`

```dockerfile
```

-	Layers:
	-	`sha256:c6ec4332029f56a214be68a1da8a91d6170bcc2d2d243daae2353e3cb0baeaae`  
		Last Modified: Sat, 22 Feb 2025 00:31:38 GMT  
		Size: 2.3 MB (2289622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c51e1294036728fb8cdc19970c532c2ced14c50e64984ed76d91eda1e1a61c92`  
		Last Modified: Sat, 22 Feb 2025 00:31:38 GMT  
		Size: 21.4 KB (21419 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:ef53c35087afb0499842bedf1fbfa79d5b842f19779b63afa6f1f025a9d5a6ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32956089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e8028b418ebc438bf613b1826c1c627b9c70d0ceba487e067f06ce1140efa93`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a2635855d79b555abffa55c629412da2c4134f2a8ccd4a315c0b6f92b579ae`  
		Last Modified: Sat, 22 Feb 2025 00:31:19 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b44d66689e77fbfe0bc0a0c7e8a45833882611191361e49b6a48030dfbda7bb`  
		Last Modified: Sat, 22 Feb 2025 00:31:20 GMT  
		Size: 2.5 MB (2500720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22086dfd31db842102b740e2bc68682931021ff3fb6491253f9087ca1df6f3cd`  
		Last Modified: Sat, 22 Feb 2025 00:31:19 GMT  
		Size: 1.3 MB (1266399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0d2b64685890c225d3c813b7c867d2d96fb3719d43d4edb206375e55ee6a32`  
		Last Modified: Sat, 22 Feb 2025 00:31:19 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365bc8ba2a50069e758df20bd1b42ff192846fbb115b9edb0cda2fc43fdb2600`  
		Last Modified: Sat, 22 Feb 2025 00:31:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:26ed9f96a812fb5af80816d45e029522166082e249f638019205191bb5b02cb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb94ae18d76a538788c16c601bc76b3509862697a1367bd2fa42cfd5ab18e5b9`

```dockerfile
```

-	Layers:
	-	`sha256:ece746d0e00e98b51635c1914e1aeab67cf6208f531559f2af8346d9e8f40606`  
		Last Modified: Sat, 22 Feb 2025 00:31:20 GMT  
		Size: 2.3 MB (2286406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31ecb87a15a354348411689e2d7bf34846d275e3db9f99b9d2fd53c5d931d382`  
		Last Modified: Sat, 22 Feb 2025 00:31:19 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:61282eccad654d1d03273cc2fb02a4db982d36e9e0ff866eab773795e106ec8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31692298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c72f2790d1441f439ca292b3f0077287e8f93af8f30b6ae44f467f4728aecf0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:60fe4951c23056512065fcf1948d3167c5aa5d83d4bfd2829494b7d09b4fe661`  
		Last Modified: Tue, 04 Feb 2025 01:38:47 GMT  
		Size: 28.5 MB (28486581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006e6bf1f5c579c425dd6a7045b45795f463f886bf4ee3532c5964da484e77c4`  
		Last Modified: Tue, 04 Feb 2025 05:36:04 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa88afbdcfa1d52adc83e6c274708611503deecc6240cf640db7eb23e1999a30`  
		Last Modified: Sat, 22 Feb 2025 00:36:16 GMT  
		Size: 1.9 MB (1943183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dcb0fa418dcf8d7cccdc41a73ad2063c2ae4bf810f2b8a7c67a8ead47c9d684`  
		Last Modified: Sat, 22 Feb 2025 00:36:16 GMT  
		Size: 1.3 MB (1261025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f222082e64a60018ba8bea35cd86f7254591435953a40e022541df5dd42e64`  
		Last Modified: Sat, 22 Feb 2025 00:36:16 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f367b09aa255318629e01e577d62f20d50bcc2cb49cd5519a9c1b68c0829b4e`  
		Last Modified: Sat, 22 Feb 2025 00:36:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:c3872907481511259937b839ceb7f595c2edbf6f47b17ae6cd4e1a10c2456f41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48598526c0aff23b0715615e1f0cd1c35b57f4de0e9b13447903c812540b5683`

```dockerfile
```

-	Layers:
	-	`sha256:308d9f10522a8efc39d94eb5a4f47a8b547bdf8ef47d53a710264ade572dc85b`  
		Last Modified: Sat, 22 Feb 2025 00:36:16 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:10e27fa85f13d51af4a481e4778b04b3b80d506a129aab984fc5d5dab919a8e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36085879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac4b53721162a6ae89b5b0e96dfb4e7ba41127c795c3b9689c36040284ea691`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 01:38:01 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2deccedfff592cdf0e60a1a0f23cfa011cc09854b3b8fd5979a2215801fe859a`  
		Last Modified: Wed, 05 Feb 2025 20:30:01 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f77d137ef9ee5f1f27684f14e816a1f088dfffc4476ab6d02ffa5d251db059`  
		Last Modified: Wed, 05 Feb 2025 20:30:01 GMT  
		Size: 2.7 MB (2708582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163ac5a13dc4a349552e8a728dbfe7a6747c6c194c8f3af433fa8f89ca89614e`  
		Last Modified: Sat, 22 Feb 2025 00:31:22 GMT  
		Size: 1.3 MB (1331006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52cbf6e5ffb6677cc60835d4722667a4e9ac72b9ede1a0a9f282e56abf5dc63`  
		Last Modified: Sat, 22 Feb 2025 00:31:22 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7111ad13f64383b6c5b3388ba5cd00d3804080114fc716c24ebe318a0b45d350`  
		Last Modified: Sat, 22 Feb 2025 00:31:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:8ec0ef0ee501fe9bf349dbf63dce11035a606876a565ee69fd5055418b09d08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8468c14d9febe1b645497e9293a93d6b378bbdb3147a6c0bb18f23a907241bda`

```dockerfile
```

-	Layers:
	-	`sha256:ebd1905c7f20a0d3d102c7b17f531860a3ac45d105b42f0669754a3230ae5fe2`  
		Last Modified: Sat, 22 Feb 2025 00:31:22 GMT  
		Size: 2.3 MB (2293679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b94eff9fb2c5e828a7e6a3ec42729e322d3cc31372e12a5ad1b7eb9761e30a8`  
		Last Modified: Sat, 22 Feb 2025 00:31:21 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:10f8a97eb4da432625002966d78d3993a95f073fb5077a1a4f3cc5a76cd6bab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30261694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a090e8956a7fcbb8b2f590626585d48385828d83d3925e0f8127f400e7c074`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85c3e9bcd86da2086f455efe77a700fe40645a11782885cb35509ae6da968af`  
		Last Modified: Wed, 05 Feb 2025 20:31:33 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25653c174b0d3f4223a55d32a6e019a0a071b0f939c2043a5f3ca38897b6a47`  
		Last Modified: Wed, 05 Feb 2025 20:31:33 GMT  
		Size: 2.2 MB (2156373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86dc255a71b2a050391adb8d18b925df4b93b704a5d38583f893d4c1e1babe1`  
		Last Modified: Sat, 22 Feb 2025 00:31:32 GMT  
		Size: 1.2 MB (1245183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848092fc56244055b7ee89f53de1c07230b0bd2651e37dea23770fc8089383db`  
		Last Modified: Sat, 22 Feb 2025 00:31:33 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab89cd679a4ffa81bbb3cbb213b25b557649024534fef1f253bdaf6f65799c05`  
		Last Modified: Sat, 22 Feb 2025 00:31:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:b70e906e72967b0e6ed1c8be6d754bf62e2ee68350435a171d182ba6efc9dd70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f906cfd918535c7f2f1b3af08ff4c29ffce9b1c176c8ca28e5f3333bd612aaa3`

```dockerfile
```

-	Layers:
	-	`sha256:0fcec7672387ec22fd81d2b2a8c5de99e7aae50b53faf5bf629ded84a19776d1`  
		Last Modified: Sat, 22 Feb 2025 00:31:32 GMT  
		Size: 2.3 MB (2289021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5d0bd85e2270f2d197500c26d3f1fdc8af08248f560b4dfcee81130a4a3748f`  
		Last Modified: Sat, 22 Feb 2025 00:31:32 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.37`

```console
$ docker pull memcached@sha256:685ba31ae4994ff6daf16d21142346dbd828d0dfbeff3cbc7a7f9b4f5f93b2dd
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

### `memcached:1.6.37` - linux; amd64

```console
$ docker pull memcached@sha256:bfe5fd0aac5c89b8022c2620abc0a1118cb84d68a74a437ac1fef55be567a23f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31972590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a69266e53d188956df96699ee7bd22b00986730a190789881f82a593361bfc16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d569cc07bddca59980d45ae28a8bfede7584cdca655fad52796e829ac8b7fee`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c58bc9b838a5c291945e3cd889cc93151a03fc70e079914ba998f26239ef2e`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 2.5 MB (2491762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67c97f377dc045ebb683ab2bf6d771520192351043ab7fc20c63ed1a997f84b`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 1.3 MB (1267012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8282d3a602638805126b2e682263fb38ca402e3beaa3a047ed0add1bf754fdb8`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cd8dd518d1c91daec2bae1887feb80b6473e0fe5e6846ddb613387e8311c64`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.37` - unknown; unknown

```console
$ docker pull memcached@sha256:ffc24940329fbd38d3efa10fbceb92bc75b8c8e3861170180d934c88ad8659b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a2b67f33d20bb90a8a9305d3ef143d1332d728823aeba14947ec779d5da211`

```dockerfile
```

-	Layers:
	-	`sha256:6ff1804b1ee0e0da242ef1ef47226adb9ac0a4172528e4ac5501443a5e6f3487`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 2.3 MB (2289307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6460f3cc3f151e357a1fa273d42ff4f884c9d2b093c4763cb3c73595fb554fa5`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.37` - linux; arm variant v5

```console
$ docker pull memcached@sha256:abee184952eb3cfc02bd6555047901e0e27fe9379eaddc25acb7805ac3c01e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29079400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c55ad492b5523a9106a2cef2d811d102d5d88a74110653f3187894c060ae61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aa8576c673e5a651f7450bee7603a12ac6168051fdd5b2411678987e180cad6e`  
		Last Modified: Tue, 04 Feb 2025 01:38:28 GMT  
		Size: 25.7 MB (25736549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d03c1f12f429fcd661498f32bc4e1c1e6a1e4189bd6014e71da057147e2286`  
		Last Modified: Tue, 04 Feb 2025 04:58:18 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7e25c626324a280a0e7be83a5642bb48a551515d4c38cb544c66904fcf10bb`  
		Last Modified: Tue, 04 Feb 2025 04:58:19 GMT  
		Size: 2.1 MB (2096073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b068d3f71231f010921a5b6713e177cb20b1838ecd63d09bbfa1cf87d64a1108`  
		Last Modified: Sat, 22 Feb 2025 00:32:42 GMT  
		Size: 1.2 MB (1245268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b49e89cf77efc47a7250f3af153069fc9a2d7696d280b7f9b2ef3ef434a4e1b`  
		Last Modified: Sat, 22 Feb 2025 00:32:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615b1475c4f9cc790d1525380d666d53c7507c87e777e647ed0287598efa3d48`  
		Last Modified: Sat, 22 Feb 2025 00:32:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.37` - unknown; unknown

```console
$ docker pull memcached@sha256:b668a646c910c9b5f5c8f752e53b49deb2a1ad6e7ebdc0526adbcf9d299b4ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49e0834cecf5abf237b771c3850e94ba86e05385ccbab4b91cb3d9f063af010c`

```dockerfile
```

-	Layers:
	-	`sha256:cb0b22895c3619cafd6dca713774db852bfe31b3adb4ba3ec6a66838eac945e3`  
		Last Modified: Sat, 22 Feb 2025 00:32:42 GMT  
		Size: 2.3 MB (2292845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d7f06daebcc005d1c5979488409050e03ba04720bf9c424588de02b684b8c03`  
		Last Modified: Sat, 22 Feb 2025 00:32:42 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.37` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ecdac108a456c82920f95b934edd7b2c3abf62adf96adac7b99767591b6fecf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31658335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c4d6a0c65f7a9206b9660b5d79d29c8183bb45cef6fa838bbc17493f7085b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85c190a9b2b110c5e0805ab31e5792459e717a286856047e10f45423d8231dd`  
		Last Modified: Wed, 05 Feb 2025 20:31:30 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d150df6d26f3098fb2b4554249a49c854dd5acf5f8255fcf725a970fdbcccbe`  
		Last Modified: Wed, 05 Feb 2025 20:31:31 GMT  
		Size: 2.4 MB (2355307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d34310d49ce6a8c13f0814ea92dbb59638c73a98d899a8f489b4cdba59cf1a4`  
		Last Modified: Sat, 22 Feb 2025 00:31:38 GMT  
		Size: 1.3 MB (1260635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d933eb164ac02e89a9ec663d27d218ab0e489db96ca622ac5023f149bb767f2`  
		Last Modified: Sat, 22 Feb 2025 00:31:38 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3955731998caab6a7273ad7e2b63e663ae711d2f45416977f29c9df6c3a5771`  
		Last Modified: Sat, 22 Feb 2025 00:31:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.37` - unknown; unknown

```console
$ docker pull memcached@sha256:b0998d3901cbf4dc98a6f5d0254d7f2115d3d110c1de81a5ec4cc6b56c1afe39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:351b12242d29e072aaf887e69b6b36f8b86fb05d09e37cd2a338014241525536`

```dockerfile
```

-	Layers:
	-	`sha256:c6ec4332029f56a214be68a1da8a91d6170bcc2d2d243daae2353e3cb0baeaae`  
		Last Modified: Sat, 22 Feb 2025 00:31:38 GMT  
		Size: 2.3 MB (2289622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c51e1294036728fb8cdc19970c532c2ced14c50e64984ed76d91eda1e1a61c92`  
		Last Modified: Sat, 22 Feb 2025 00:31:38 GMT  
		Size: 21.4 KB (21419 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.37` - linux; 386

```console
$ docker pull memcached@sha256:ef53c35087afb0499842bedf1fbfa79d5b842f19779b63afa6f1f025a9d5a6ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32956089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e8028b418ebc438bf613b1826c1c627b9c70d0ceba487e067f06ce1140efa93`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a2635855d79b555abffa55c629412da2c4134f2a8ccd4a315c0b6f92b579ae`  
		Last Modified: Sat, 22 Feb 2025 00:31:19 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b44d66689e77fbfe0bc0a0c7e8a45833882611191361e49b6a48030dfbda7bb`  
		Last Modified: Sat, 22 Feb 2025 00:31:20 GMT  
		Size: 2.5 MB (2500720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22086dfd31db842102b740e2bc68682931021ff3fb6491253f9087ca1df6f3cd`  
		Last Modified: Sat, 22 Feb 2025 00:31:19 GMT  
		Size: 1.3 MB (1266399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0d2b64685890c225d3c813b7c867d2d96fb3719d43d4edb206375e55ee6a32`  
		Last Modified: Sat, 22 Feb 2025 00:31:19 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365bc8ba2a50069e758df20bd1b42ff192846fbb115b9edb0cda2fc43fdb2600`  
		Last Modified: Sat, 22 Feb 2025 00:31:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.37` - unknown; unknown

```console
$ docker pull memcached@sha256:26ed9f96a812fb5af80816d45e029522166082e249f638019205191bb5b02cb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb94ae18d76a538788c16c601bc76b3509862697a1367bd2fa42cfd5ab18e5b9`

```dockerfile
```

-	Layers:
	-	`sha256:ece746d0e00e98b51635c1914e1aeab67cf6208f531559f2af8346d9e8f40606`  
		Last Modified: Sat, 22 Feb 2025 00:31:20 GMT  
		Size: 2.3 MB (2286406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31ecb87a15a354348411689e2d7bf34846d275e3db9f99b9d2fd53c5d931d382`  
		Last Modified: Sat, 22 Feb 2025 00:31:19 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.37` - linux; mips64le

```console
$ docker pull memcached@sha256:61282eccad654d1d03273cc2fb02a4db982d36e9e0ff866eab773795e106ec8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31692298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c72f2790d1441f439ca292b3f0077287e8f93af8f30b6ae44f467f4728aecf0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:60fe4951c23056512065fcf1948d3167c5aa5d83d4bfd2829494b7d09b4fe661`  
		Last Modified: Tue, 04 Feb 2025 01:38:47 GMT  
		Size: 28.5 MB (28486581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006e6bf1f5c579c425dd6a7045b45795f463f886bf4ee3532c5964da484e77c4`  
		Last Modified: Tue, 04 Feb 2025 05:36:04 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa88afbdcfa1d52adc83e6c274708611503deecc6240cf640db7eb23e1999a30`  
		Last Modified: Sat, 22 Feb 2025 00:36:16 GMT  
		Size: 1.9 MB (1943183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dcb0fa418dcf8d7cccdc41a73ad2063c2ae4bf810f2b8a7c67a8ead47c9d684`  
		Last Modified: Sat, 22 Feb 2025 00:36:16 GMT  
		Size: 1.3 MB (1261025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f222082e64a60018ba8bea35cd86f7254591435953a40e022541df5dd42e64`  
		Last Modified: Sat, 22 Feb 2025 00:36:16 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f367b09aa255318629e01e577d62f20d50bcc2cb49cd5519a9c1b68c0829b4e`  
		Last Modified: Sat, 22 Feb 2025 00:36:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.37` - unknown; unknown

```console
$ docker pull memcached@sha256:c3872907481511259937b839ceb7f595c2edbf6f47b17ae6cd4e1a10c2456f41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48598526c0aff23b0715615e1f0cd1c35b57f4de0e9b13447903c812540b5683`

```dockerfile
```

-	Layers:
	-	`sha256:308d9f10522a8efc39d94eb5a4f47a8b547bdf8ef47d53a710264ade572dc85b`  
		Last Modified: Sat, 22 Feb 2025 00:36:16 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.37` - linux; ppc64le

```console
$ docker pull memcached@sha256:10e27fa85f13d51af4a481e4778b04b3b80d506a129aab984fc5d5dab919a8e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36085879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac4b53721162a6ae89b5b0e96dfb4e7ba41127c795c3b9689c36040284ea691`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 01:38:01 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2deccedfff592cdf0e60a1a0f23cfa011cc09854b3b8fd5979a2215801fe859a`  
		Last Modified: Wed, 05 Feb 2025 20:30:01 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f77d137ef9ee5f1f27684f14e816a1f088dfffc4476ab6d02ffa5d251db059`  
		Last Modified: Wed, 05 Feb 2025 20:30:01 GMT  
		Size: 2.7 MB (2708582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163ac5a13dc4a349552e8a728dbfe7a6747c6c194c8f3af433fa8f89ca89614e`  
		Last Modified: Sat, 22 Feb 2025 00:31:22 GMT  
		Size: 1.3 MB (1331006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52cbf6e5ffb6677cc60835d4722667a4e9ac72b9ede1a0a9f282e56abf5dc63`  
		Last Modified: Sat, 22 Feb 2025 00:31:22 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7111ad13f64383b6c5b3388ba5cd00d3804080114fc716c24ebe318a0b45d350`  
		Last Modified: Sat, 22 Feb 2025 00:31:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.37` - unknown; unknown

```console
$ docker pull memcached@sha256:8ec0ef0ee501fe9bf349dbf63dce11035a606876a565ee69fd5055418b09d08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8468c14d9febe1b645497e9293a93d6b378bbdb3147a6c0bb18f23a907241bda`

```dockerfile
```

-	Layers:
	-	`sha256:ebd1905c7f20a0d3d102c7b17f531860a3ac45d105b42f0669754a3230ae5fe2`  
		Last Modified: Sat, 22 Feb 2025 00:31:22 GMT  
		Size: 2.3 MB (2293679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b94eff9fb2c5e828a7e6a3ec42729e322d3cc31372e12a5ad1b7eb9761e30a8`  
		Last Modified: Sat, 22 Feb 2025 00:31:21 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.37` - linux; s390x

```console
$ docker pull memcached@sha256:10f8a97eb4da432625002966d78d3993a95f073fb5077a1a4f3cc5a76cd6bab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30261694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a090e8956a7fcbb8b2f590626585d48385828d83d3925e0f8127f400e7c074`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85c3e9bcd86da2086f455efe77a700fe40645a11782885cb35509ae6da968af`  
		Last Modified: Wed, 05 Feb 2025 20:31:33 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25653c174b0d3f4223a55d32a6e019a0a071b0f939c2043a5f3ca38897b6a47`  
		Last Modified: Wed, 05 Feb 2025 20:31:33 GMT  
		Size: 2.2 MB (2156373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86dc255a71b2a050391adb8d18b925df4b93b704a5d38583f893d4c1e1babe1`  
		Last Modified: Sat, 22 Feb 2025 00:31:32 GMT  
		Size: 1.2 MB (1245183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848092fc56244055b7ee89f53de1c07230b0bd2651e37dea23770fc8089383db`  
		Last Modified: Sat, 22 Feb 2025 00:31:33 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab89cd679a4ffa81bbb3cbb213b25b557649024534fef1f253bdaf6f65799c05`  
		Last Modified: Sat, 22 Feb 2025 00:31:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.37` - unknown; unknown

```console
$ docker pull memcached@sha256:b70e906e72967b0e6ed1c8be6d754bf62e2ee68350435a171d182ba6efc9dd70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f906cfd918535c7f2f1b3af08ff4c29ffce9b1c176c8ca28e5f3333bd612aaa3`

```dockerfile
```

-	Layers:
	-	`sha256:0fcec7672387ec22fd81d2b2a8c5de99e7aae50b53faf5bf629ded84a19776d1`  
		Last Modified: Sat, 22 Feb 2025 00:31:32 GMT  
		Size: 2.3 MB (2289021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5d0bd85e2270f2d197500c26d3f1fdc8af08248f560b4dfcee81130a4a3748f`  
		Last Modified: Sat, 22 Feb 2025 00:31:32 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.37-alpine`

```console
$ docker pull memcached@sha256:4fb13e4757387000230be124c5a74f107abfd1f65e2526f4c627110d666bf5a3
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

### `memcached:1.6.37-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:787e9120e36559c9aba4cce621188072d00e159bc596fe803c00037f3702c22f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4716929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21a7aa256b160c9c42cce498615225db46d75b42d27b180c3879e9e7d1fbd92`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3e9f8182c72be0cf629032be09e1b5da2b94a8a03a202110036eae2fa538b9`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc58417b03bbd338e8fab898ba984cef01fdb2b2960ae862ecc89bc258a0b981`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 104.7 KB (104690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82369477a539cf4bc0cfd0063cb20ce85cf36442b532dbde15f71a6061abc106`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 968.6 KB (968644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0261a578c93ccd99ba866def61b28a43cc2938598cbc307011db812c246ee206`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cd8dd518d1c91daec2bae1887feb80b6473e0fe5e6846ddb613387e8311c64`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.37-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:abae77e9a8d50f01601a4188494f6d7a2e3442e7258fa213a581d2e281fc02c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c452640b5e4fe4e1b31941228c0615b396ec62a56794e1c63e1b9326c5cbf60a`

```dockerfile
```

-	Layers:
	-	`sha256:297387df1b0d33fd74438a8273ab5e20a2a8193785491bcc9b6ad3e03d9c1aa6`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 93.6 KB (93633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0d579b1ca91bec4046749a5bf7a3549239008c1a1083ec2213a3c6004a5725b`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 19.6 KB (19570 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.37-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:22169a1786f676798782408232c35b71e12bd32b10164e81c0b32da6143641c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5083533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add144e03275b9c89bb582ad307446fa229055731caf45650896ed6d340a839a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b3b947aa71cef021cd9306b1f24a44554e8d663c8530dd36d42b94a883f4c9`  
		Last Modified: Fri, 14 Feb 2025 19:50:13 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6014feb1c2bb2b6c63e9a7b16a3850c447422bdad6e65b302925b8547b23c192`  
		Last Modified: Fri, 14 Feb 2025 19:50:13 GMT  
		Size: 120.8 KB (120780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b307ec9e1116f91be05519ed18f8206fb49e72d80c7a04638004cf9a82ac2a77`  
		Last Modified: Sat, 22 Feb 2025 00:34:08 GMT  
		Size: 968.4 KB (968374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b643c0752d8cb8b54b8a8d095693feba316ac84b1fd17048fc0189599bc5e1d`  
		Last Modified: Sat, 22 Feb 2025 00:34:08 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38c21d127cb51320d77ca177167435601efbd6ddc02a49c2876aac2884a0109`  
		Last Modified: Sat, 22 Feb 2025 00:34:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.37-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:bef45ca6f335dcb09118c5ee88802a722f482af24a9afa8974e7b4800b0fd39f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b1eae2531d72df59778c8c8ac7fecb6d4b6b408b9192cc6ac7d77a5e98128d7`

```dockerfile
```

-	Layers:
	-	`sha256:f675a5a746afeb63892d91271eccac08f3a01bbf6dae0926114e83673197e1be`  
		Last Modified: Sat, 22 Feb 2025 00:34:08 GMT  
		Size: 93.7 KB (93737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74fc4c03468266c50ce86e1314f4c6f45903d6c98465180f75f826dfb54cfcfd`  
		Last Modified: Sat, 22 Feb 2025 00:34:07 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.37-alpine` - linux; 386

```console
$ docker pull memcached@sha256:46aa92b9d94ea6493f4f5f098e6b1de64f3e8c450eb6440d5bf59f4e1f2ead69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4534801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac2f67d3ec71890e3d6bd391e98b4da571242348ac135e99bcef39979486b34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0216147e703738541dd8987b9b2bc147da47c311b00a06feb265c9f0abf707`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab4b25598c42e6f016cb0a26803d39acd19d7871e0b092cbefd2f8856b0a112`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 109.5 KB (109489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5589cc68943165ccc1b90f645ea08e4c8bb401c6ea2db3506bd1309fd04158`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 960.3 KB (960336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f9697b895d35627f393cf365d336aad6ff6d5d9d767f2ab73d2696751527c1`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a049f6eb832cc266adfa607fe5c42c0710850885d375ee2fd2b22a9add7d29b7`  
		Last Modified: Sat, 22 Feb 2025 00:31:07 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.37-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:f9710d1f921ddd802f69f2eb77ae2baa0a046307d13215474dd3f369124034e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de341f780812144f1c4528778277abc1e0f979937153200813e3e66b11d01d02`

```dockerfile
```

-	Layers:
	-	`sha256:4bd1b00215d14ae69987d6066982bb958dbe599471eebf5233fbc9512b4a5fcd`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 93.6 KB (93588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1126652f997b244e12c038e90d03bc059f60adbf626ea9d38c90259a5920775c`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 19.5 KB (19512 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.37-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:e3fbb21940e6ecf6e09878be1fdb50cfe7d0ca132112d7439d1c3f266f6b8b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4706934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ab0bd6e09f5b37468b8ae688526c599c21045baf0b0b8bc98ec097e5267b28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deee0b86774e394f5e07eff435a072bdde8922ec1757ef689265af3e1864d632`  
		Last Modified: Fri, 14 Feb 2025 19:42:34 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbafd6c675f155044ba3e5ef96996313b9f05064b966848001c7ea04a9c6048`  
		Last Modified: Fri, 14 Feb 2025 19:42:34 GMT  
		Size: 124.3 KB (124276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56400c974ec4a72a96f97ce1a5828e0ebcb6df76fe5c2f7d8dae29c07223abbf`  
		Last Modified: Sat, 22 Feb 2025 00:34:12 GMT  
		Size: 1.0 MB (1006957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0b9347f26655d1e450da08a0e5a23d5cc368bbfad35a84c643be25c87b2726`  
		Last Modified: Sat, 22 Feb 2025 00:34:11 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5064388d99c64e09f330fcec8ffba565524c380566e6a70fb34aedbf84880f8`  
		Last Modified: Sat, 22 Feb 2025 00:34:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.37-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:94cd05711888081e81791841a80e96d16b22ba21e835ba80d125ed65d295b947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84057bf494e545f78faa4d02b570fd42a27b6c3a616d2e07c06013f7125b0ec2`

```dockerfile
```

-	Layers:
	-	`sha256:f969bce286e2478dcbbe6690408d5b20920506d09783024c5e824272ee16cc9e`  
		Last Modified: Sat, 22 Feb 2025 00:34:11 GMT  
		Size: 91.7 KB (91740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93bbfb8bcbd31cfc88a941030e8e18f43fdb73c07293481a932203cb3a25e504`  
		Last Modified: Sat, 22 Feb 2025 00:34:11 GMT  
		Size: 19.6 KB (19648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.37-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:0087cdeb03b579438e5e722b991d7e3ee891e4770b26ceeff27c4401cf654657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4571101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2bc2ef8da87893bf85939bd479692ebd280f9d840686e5fdc00089b536aad65`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d658470bb26df23b8a940bc8e53f6c8b685a81ce47a086f683e29b63a6bac496`  
		Last Modified: Fri, 14 Feb 2025 19:44:23 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a07c51d6bc9e389360e3ccba6d95f5697fdd3366a1ac093d59ce54e0da2550`  
		Last Modified: Fri, 14 Feb 2025 19:44:23 GMT  
		Size: 113.5 KB (113462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91fbcb7a7ec7da4c7e8e462c545d152b5a079ef1360a1d05df018c7f78da31e7`  
		Last Modified: Sat, 22 Feb 2025 00:35:17 GMT  
		Size: 988.7 KB (988725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539207d8d3aff51a577331b44e1e08e93ad1330f182ca154c800fa3cc40b77bd`  
		Last Modified: Sat, 22 Feb 2025 00:35:17 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236b320beb51084e2e1b6b838aa193caf573a4292b1353bba1a0cdf076b82db6`  
		Last Modified: Sat, 22 Feb 2025 00:35:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.37-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9bd727783dc634399ded38736a232ba7801976d1b0096e07194f53a8f82de528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 KB (111252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7030d08f1e1857ea22b2d774577cb0cb56dd6eb8f7b7ff94fb262e44551c1c`

```dockerfile
```

-	Layers:
	-	`sha256:b7ec10e807d6f8925ef59303e53fc02069fd4a687b1baa66cf3164590cb29d4b`  
		Last Modified: Sat, 22 Feb 2025 00:35:17 GMT  
		Size: 91.7 KB (91682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25a3bb1b2ff42fd2d2a4c3e88ec8af248b5df8c2a42a871dcec17d8a1deb6dbb`  
		Last Modified: Sat, 22 Feb 2025 00:35:17 GMT  
		Size: 19.6 KB (19570 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.37-alpine3.21`

```console
$ docker pull memcached@sha256:4fb13e4757387000230be124c5a74f107abfd1f65e2526f4c627110d666bf5a3
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

### `memcached:1.6.37-alpine3.21` - linux; amd64

```console
$ docker pull memcached@sha256:787e9120e36559c9aba4cce621188072d00e159bc596fe803c00037f3702c22f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4716929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21a7aa256b160c9c42cce498615225db46d75b42d27b180c3879e9e7d1fbd92`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3e9f8182c72be0cf629032be09e1b5da2b94a8a03a202110036eae2fa538b9`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc58417b03bbd338e8fab898ba984cef01fdb2b2960ae862ecc89bc258a0b981`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 104.7 KB (104690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82369477a539cf4bc0cfd0063cb20ce85cf36442b532dbde15f71a6061abc106`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 968.6 KB (968644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0261a578c93ccd99ba866def61b28a43cc2938598cbc307011db812c246ee206`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cd8dd518d1c91daec2bae1887feb80b6473e0fe5e6846ddb613387e8311c64`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.37-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:abae77e9a8d50f01601a4188494f6d7a2e3442e7258fa213a581d2e281fc02c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c452640b5e4fe4e1b31941228c0615b396ec62a56794e1c63e1b9326c5cbf60a`

```dockerfile
```

-	Layers:
	-	`sha256:297387df1b0d33fd74438a8273ab5e20a2a8193785491bcc9b6ad3e03d9c1aa6`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 93.6 KB (93633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0d579b1ca91bec4046749a5bf7a3549239008c1a1083ec2213a3c6004a5725b`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 19.6 KB (19570 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.37-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:22169a1786f676798782408232c35b71e12bd32b10164e81c0b32da6143641c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5083533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add144e03275b9c89bb582ad307446fa229055731caf45650896ed6d340a839a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b3b947aa71cef021cd9306b1f24a44554e8d663c8530dd36d42b94a883f4c9`  
		Last Modified: Fri, 14 Feb 2025 19:50:13 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6014feb1c2bb2b6c63e9a7b16a3850c447422bdad6e65b302925b8547b23c192`  
		Last Modified: Fri, 14 Feb 2025 19:50:13 GMT  
		Size: 120.8 KB (120780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b307ec9e1116f91be05519ed18f8206fb49e72d80c7a04638004cf9a82ac2a77`  
		Last Modified: Sat, 22 Feb 2025 00:34:08 GMT  
		Size: 968.4 KB (968374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b643c0752d8cb8b54b8a8d095693feba316ac84b1fd17048fc0189599bc5e1d`  
		Last Modified: Sat, 22 Feb 2025 00:34:08 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38c21d127cb51320d77ca177167435601efbd6ddc02a49c2876aac2884a0109`  
		Last Modified: Sat, 22 Feb 2025 00:34:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.37-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:bef45ca6f335dcb09118c5ee88802a722f482af24a9afa8974e7b4800b0fd39f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b1eae2531d72df59778c8c8ac7fecb6d4b6b408b9192cc6ac7d77a5e98128d7`

```dockerfile
```

-	Layers:
	-	`sha256:f675a5a746afeb63892d91271eccac08f3a01bbf6dae0926114e83673197e1be`  
		Last Modified: Sat, 22 Feb 2025 00:34:08 GMT  
		Size: 93.7 KB (93737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74fc4c03468266c50ce86e1314f4c6f45903d6c98465180f75f826dfb54cfcfd`  
		Last Modified: Sat, 22 Feb 2025 00:34:07 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.37-alpine3.21` - linux; 386

```console
$ docker pull memcached@sha256:46aa92b9d94ea6493f4f5f098e6b1de64f3e8c450eb6440d5bf59f4e1f2ead69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4534801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac2f67d3ec71890e3d6bd391e98b4da571242348ac135e99bcef39979486b34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0216147e703738541dd8987b9b2bc147da47c311b00a06feb265c9f0abf707`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab4b25598c42e6f016cb0a26803d39acd19d7871e0b092cbefd2f8856b0a112`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 109.5 KB (109489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5589cc68943165ccc1b90f645ea08e4c8bb401c6ea2db3506bd1309fd04158`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 960.3 KB (960336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f9697b895d35627f393cf365d336aad6ff6d5d9d767f2ab73d2696751527c1`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a049f6eb832cc266adfa607fe5c42c0710850885d375ee2fd2b22a9add7d29b7`  
		Last Modified: Sat, 22 Feb 2025 00:31:07 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.37-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:f9710d1f921ddd802f69f2eb77ae2baa0a046307d13215474dd3f369124034e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de341f780812144f1c4528778277abc1e0f979937153200813e3e66b11d01d02`

```dockerfile
```

-	Layers:
	-	`sha256:4bd1b00215d14ae69987d6066982bb958dbe599471eebf5233fbc9512b4a5fcd`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 93.6 KB (93588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1126652f997b244e12c038e90d03bc059f60adbf626ea9d38c90259a5920775c`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 19.5 KB (19512 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.37-alpine3.21` - linux; ppc64le

```console
$ docker pull memcached@sha256:e3fbb21940e6ecf6e09878be1fdb50cfe7d0ca132112d7439d1c3f266f6b8b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4706934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ab0bd6e09f5b37468b8ae688526c599c21045baf0b0b8bc98ec097e5267b28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deee0b86774e394f5e07eff435a072bdde8922ec1757ef689265af3e1864d632`  
		Last Modified: Fri, 14 Feb 2025 19:42:34 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbafd6c675f155044ba3e5ef96996313b9f05064b966848001c7ea04a9c6048`  
		Last Modified: Fri, 14 Feb 2025 19:42:34 GMT  
		Size: 124.3 KB (124276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56400c974ec4a72a96f97ce1a5828e0ebcb6df76fe5c2f7d8dae29c07223abbf`  
		Last Modified: Sat, 22 Feb 2025 00:34:12 GMT  
		Size: 1.0 MB (1006957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0b9347f26655d1e450da08a0e5a23d5cc368bbfad35a84c643be25c87b2726`  
		Last Modified: Sat, 22 Feb 2025 00:34:11 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5064388d99c64e09f330fcec8ffba565524c380566e6a70fb34aedbf84880f8`  
		Last Modified: Sat, 22 Feb 2025 00:34:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.37-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:94cd05711888081e81791841a80e96d16b22ba21e835ba80d125ed65d295b947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84057bf494e545f78faa4d02b570fd42a27b6c3a616d2e07c06013f7125b0ec2`

```dockerfile
```

-	Layers:
	-	`sha256:f969bce286e2478dcbbe6690408d5b20920506d09783024c5e824272ee16cc9e`  
		Last Modified: Sat, 22 Feb 2025 00:34:11 GMT  
		Size: 91.7 KB (91740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93bbfb8bcbd31cfc88a941030e8e18f43fdb73c07293481a932203cb3a25e504`  
		Last Modified: Sat, 22 Feb 2025 00:34:11 GMT  
		Size: 19.6 KB (19648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.37-alpine3.21` - linux; s390x

```console
$ docker pull memcached@sha256:0087cdeb03b579438e5e722b991d7e3ee891e4770b26ceeff27c4401cf654657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4571101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2bc2ef8da87893bf85939bd479692ebd280f9d840686e5fdc00089b536aad65`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d658470bb26df23b8a940bc8e53f6c8b685a81ce47a086f683e29b63a6bac496`  
		Last Modified: Fri, 14 Feb 2025 19:44:23 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a07c51d6bc9e389360e3ccba6d95f5697fdd3366a1ac093d59ce54e0da2550`  
		Last Modified: Fri, 14 Feb 2025 19:44:23 GMT  
		Size: 113.5 KB (113462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91fbcb7a7ec7da4c7e8e462c545d152b5a079ef1360a1d05df018c7f78da31e7`  
		Last Modified: Sat, 22 Feb 2025 00:35:17 GMT  
		Size: 988.7 KB (988725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539207d8d3aff51a577331b44e1e08e93ad1330f182ca154c800fa3cc40b77bd`  
		Last Modified: Sat, 22 Feb 2025 00:35:17 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236b320beb51084e2e1b6b838aa193caf573a4292b1353bba1a0cdf076b82db6`  
		Last Modified: Sat, 22 Feb 2025 00:35:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.37-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:9bd727783dc634399ded38736a232ba7801976d1b0096e07194f53a8f82de528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 KB (111252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7030d08f1e1857ea22b2d774577cb0cb56dd6eb8f7b7ff94fb262e44551c1c`

```dockerfile
```

-	Layers:
	-	`sha256:b7ec10e807d6f8925ef59303e53fc02069fd4a687b1baa66cf3164590cb29d4b`  
		Last Modified: Sat, 22 Feb 2025 00:35:17 GMT  
		Size: 91.7 KB (91682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25a3bb1b2ff42fd2d2a4c3e88ec8af248b5df8c2a42a871dcec17d8a1deb6dbb`  
		Last Modified: Sat, 22 Feb 2025 00:35:17 GMT  
		Size: 19.6 KB (19570 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.37-bookworm`

```console
$ docker pull memcached@sha256:685ba31ae4994ff6daf16d21142346dbd828d0dfbeff3cbc7a7f9b4f5f93b2dd
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

### `memcached:1.6.37-bookworm` - linux; amd64

```console
$ docker pull memcached@sha256:bfe5fd0aac5c89b8022c2620abc0a1118cb84d68a74a437ac1fef55be567a23f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31972590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a69266e53d188956df96699ee7bd22b00986730a190789881f82a593361bfc16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d569cc07bddca59980d45ae28a8bfede7584cdca655fad52796e829ac8b7fee`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c58bc9b838a5c291945e3cd889cc93151a03fc70e079914ba998f26239ef2e`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 2.5 MB (2491762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67c97f377dc045ebb683ab2bf6d771520192351043ab7fc20c63ed1a997f84b`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 1.3 MB (1267012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8282d3a602638805126b2e682263fb38ca402e3beaa3a047ed0add1bf754fdb8`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cd8dd518d1c91daec2bae1887feb80b6473e0fe5e6846ddb613387e8311c64`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.37-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:ffc24940329fbd38d3efa10fbceb92bc75b8c8e3861170180d934c88ad8659b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a2b67f33d20bb90a8a9305d3ef143d1332d728823aeba14947ec779d5da211`

```dockerfile
```

-	Layers:
	-	`sha256:6ff1804b1ee0e0da242ef1ef47226adb9ac0a4172528e4ac5501443a5e6f3487`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 2.3 MB (2289307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6460f3cc3f151e357a1fa273d42ff4f884c9d2b093c4763cb3c73595fb554fa5`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.37-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:abee184952eb3cfc02bd6555047901e0e27fe9379eaddc25acb7805ac3c01e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29079400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c55ad492b5523a9106a2cef2d811d102d5d88a74110653f3187894c060ae61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aa8576c673e5a651f7450bee7603a12ac6168051fdd5b2411678987e180cad6e`  
		Last Modified: Tue, 04 Feb 2025 01:38:28 GMT  
		Size: 25.7 MB (25736549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d03c1f12f429fcd661498f32bc4e1c1e6a1e4189bd6014e71da057147e2286`  
		Last Modified: Tue, 04 Feb 2025 04:58:18 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7e25c626324a280a0e7be83a5642bb48a551515d4c38cb544c66904fcf10bb`  
		Last Modified: Tue, 04 Feb 2025 04:58:19 GMT  
		Size: 2.1 MB (2096073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b068d3f71231f010921a5b6713e177cb20b1838ecd63d09bbfa1cf87d64a1108`  
		Last Modified: Sat, 22 Feb 2025 00:32:42 GMT  
		Size: 1.2 MB (1245268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b49e89cf77efc47a7250f3af153069fc9a2d7696d280b7f9b2ef3ef434a4e1b`  
		Last Modified: Sat, 22 Feb 2025 00:32:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615b1475c4f9cc790d1525380d666d53c7507c87e777e647ed0287598efa3d48`  
		Last Modified: Sat, 22 Feb 2025 00:32:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.37-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:b668a646c910c9b5f5c8f752e53b49deb2a1ad6e7ebdc0526adbcf9d299b4ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49e0834cecf5abf237b771c3850e94ba86e05385ccbab4b91cb3d9f063af010c`

```dockerfile
```

-	Layers:
	-	`sha256:cb0b22895c3619cafd6dca713774db852bfe31b3adb4ba3ec6a66838eac945e3`  
		Last Modified: Sat, 22 Feb 2025 00:32:42 GMT  
		Size: 2.3 MB (2292845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d7f06daebcc005d1c5979488409050e03ba04720bf9c424588de02b684b8c03`  
		Last Modified: Sat, 22 Feb 2025 00:32:42 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.37-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ecdac108a456c82920f95b934edd7b2c3abf62adf96adac7b99767591b6fecf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31658335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c4d6a0c65f7a9206b9660b5d79d29c8183bb45cef6fa838bbc17493f7085b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85c190a9b2b110c5e0805ab31e5792459e717a286856047e10f45423d8231dd`  
		Last Modified: Wed, 05 Feb 2025 20:31:30 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d150df6d26f3098fb2b4554249a49c854dd5acf5f8255fcf725a970fdbcccbe`  
		Last Modified: Wed, 05 Feb 2025 20:31:31 GMT  
		Size: 2.4 MB (2355307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d34310d49ce6a8c13f0814ea92dbb59638c73a98d899a8f489b4cdba59cf1a4`  
		Last Modified: Sat, 22 Feb 2025 00:31:38 GMT  
		Size: 1.3 MB (1260635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d933eb164ac02e89a9ec663d27d218ab0e489db96ca622ac5023f149bb767f2`  
		Last Modified: Sat, 22 Feb 2025 00:31:38 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3955731998caab6a7273ad7e2b63e663ae711d2f45416977f29c9df6c3a5771`  
		Last Modified: Sat, 22 Feb 2025 00:31:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.37-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:b0998d3901cbf4dc98a6f5d0254d7f2115d3d110c1de81a5ec4cc6b56c1afe39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:351b12242d29e072aaf887e69b6b36f8b86fb05d09e37cd2a338014241525536`

```dockerfile
```

-	Layers:
	-	`sha256:c6ec4332029f56a214be68a1da8a91d6170bcc2d2d243daae2353e3cb0baeaae`  
		Last Modified: Sat, 22 Feb 2025 00:31:38 GMT  
		Size: 2.3 MB (2289622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c51e1294036728fb8cdc19970c532c2ced14c50e64984ed76d91eda1e1a61c92`  
		Last Modified: Sat, 22 Feb 2025 00:31:38 GMT  
		Size: 21.4 KB (21419 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.37-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:ef53c35087afb0499842bedf1fbfa79d5b842f19779b63afa6f1f025a9d5a6ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32956089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e8028b418ebc438bf613b1826c1c627b9c70d0ceba487e067f06ce1140efa93`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a2635855d79b555abffa55c629412da2c4134f2a8ccd4a315c0b6f92b579ae`  
		Last Modified: Sat, 22 Feb 2025 00:31:19 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b44d66689e77fbfe0bc0a0c7e8a45833882611191361e49b6a48030dfbda7bb`  
		Last Modified: Sat, 22 Feb 2025 00:31:20 GMT  
		Size: 2.5 MB (2500720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22086dfd31db842102b740e2bc68682931021ff3fb6491253f9087ca1df6f3cd`  
		Last Modified: Sat, 22 Feb 2025 00:31:19 GMT  
		Size: 1.3 MB (1266399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0d2b64685890c225d3c813b7c867d2d96fb3719d43d4edb206375e55ee6a32`  
		Last Modified: Sat, 22 Feb 2025 00:31:19 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365bc8ba2a50069e758df20bd1b42ff192846fbb115b9edb0cda2fc43fdb2600`  
		Last Modified: Sat, 22 Feb 2025 00:31:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.37-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:26ed9f96a812fb5af80816d45e029522166082e249f638019205191bb5b02cb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb94ae18d76a538788c16c601bc76b3509862697a1367bd2fa42cfd5ab18e5b9`

```dockerfile
```

-	Layers:
	-	`sha256:ece746d0e00e98b51635c1914e1aeab67cf6208f531559f2af8346d9e8f40606`  
		Last Modified: Sat, 22 Feb 2025 00:31:20 GMT  
		Size: 2.3 MB (2286406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31ecb87a15a354348411689e2d7bf34846d275e3db9f99b9d2fd53c5d931d382`  
		Last Modified: Sat, 22 Feb 2025 00:31:19 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.37-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:61282eccad654d1d03273cc2fb02a4db982d36e9e0ff866eab773795e106ec8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31692298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c72f2790d1441f439ca292b3f0077287e8f93af8f30b6ae44f467f4728aecf0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:60fe4951c23056512065fcf1948d3167c5aa5d83d4bfd2829494b7d09b4fe661`  
		Last Modified: Tue, 04 Feb 2025 01:38:47 GMT  
		Size: 28.5 MB (28486581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006e6bf1f5c579c425dd6a7045b45795f463f886bf4ee3532c5964da484e77c4`  
		Last Modified: Tue, 04 Feb 2025 05:36:04 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa88afbdcfa1d52adc83e6c274708611503deecc6240cf640db7eb23e1999a30`  
		Last Modified: Sat, 22 Feb 2025 00:36:16 GMT  
		Size: 1.9 MB (1943183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dcb0fa418dcf8d7cccdc41a73ad2063c2ae4bf810f2b8a7c67a8ead47c9d684`  
		Last Modified: Sat, 22 Feb 2025 00:36:16 GMT  
		Size: 1.3 MB (1261025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f222082e64a60018ba8bea35cd86f7254591435953a40e022541df5dd42e64`  
		Last Modified: Sat, 22 Feb 2025 00:36:16 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f367b09aa255318629e01e577d62f20d50bcc2cb49cd5519a9c1b68c0829b4e`  
		Last Modified: Sat, 22 Feb 2025 00:36:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.37-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:c3872907481511259937b839ceb7f595c2edbf6f47b17ae6cd4e1a10c2456f41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48598526c0aff23b0715615e1f0cd1c35b57f4de0e9b13447903c812540b5683`

```dockerfile
```

-	Layers:
	-	`sha256:308d9f10522a8efc39d94eb5a4f47a8b547bdf8ef47d53a710264ade572dc85b`  
		Last Modified: Sat, 22 Feb 2025 00:36:16 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.37-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:10e27fa85f13d51af4a481e4778b04b3b80d506a129aab984fc5d5dab919a8e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36085879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac4b53721162a6ae89b5b0e96dfb4e7ba41127c795c3b9689c36040284ea691`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 01:38:01 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2deccedfff592cdf0e60a1a0f23cfa011cc09854b3b8fd5979a2215801fe859a`  
		Last Modified: Wed, 05 Feb 2025 20:30:01 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f77d137ef9ee5f1f27684f14e816a1f088dfffc4476ab6d02ffa5d251db059`  
		Last Modified: Wed, 05 Feb 2025 20:30:01 GMT  
		Size: 2.7 MB (2708582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163ac5a13dc4a349552e8a728dbfe7a6747c6c194c8f3af433fa8f89ca89614e`  
		Last Modified: Sat, 22 Feb 2025 00:31:22 GMT  
		Size: 1.3 MB (1331006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52cbf6e5ffb6677cc60835d4722667a4e9ac72b9ede1a0a9f282e56abf5dc63`  
		Last Modified: Sat, 22 Feb 2025 00:31:22 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7111ad13f64383b6c5b3388ba5cd00d3804080114fc716c24ebe318a0b45d350`  
		Last Modified: Sat, 22 Feb 2025 00:31:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.37-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:8ec0ef0ee501fe9bf349dbf63dce11035a606876a565ee69fd5055418b09d08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8468c14d9febe1b645497e9293a93d6b378bbdb3147a6c0bb18f23a907241bda`

```dockerfile
```

-	Layers:
	-	`sha256:ebd1905c7f20a0d3d102c7b17f531860a3ac45d105b42f0669754a3230ae5fe2`  
		Last Modified: Sat, 22 Feb 2025 00:31:22 GMT  
		Size: 2.3 MB (2293679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b94eff9fb2c5e828a7e6a3ec42729e322d3cc31372e12a5ad1b7eb9761e30a8`  
		Last Modified: Sat, 22 Feb 2025 00:31:21 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.37-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:10f8a97eb4da432625002966d78d3993a95f073fb5077a1a4f3cc5a76cd6bab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30261694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a090e8956a7fcbb8b2f590626585d48385828d83d3925e0f8127f400e7c074`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85c3e9bcd86da2086f455efe77a700fe40645a11782885cb35509ae6da968af`  
		Last Modified: Wed, 05 Feb 2025 20:31:33 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25653c174b0d3f4223a55d32a6e019a0a071b0f939c2043a5f3ca38897b6a47`  
		Last Modified: Wed, 05 Feb 2025 20:31:33 GMT  
		Size: 2.2 MB (2156373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86dc255a71b2a050391adb8d18b925df4b93b704a5d38583f893d4c1e1babe1`  
		Last Modified: Sat, 22 Feb 2025 00:31:32 GMT  
		Size: 1.2 MB (1245183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848092fc56244055b7ee89f53de1c07230b0bd2651e37dea23770fc8089383db`  
		Last Modified: Sat, 22 Feb 2025 00:31:33 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab89cd679a4ffa81bbb3cbb213b25b557649024534fef1f253bdaf6f65799c05`  
		Last Modified: Sat, 22 Feb 2025 00:31:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.37-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:b70e906e72967b0e6ed1c8be6d754bf62e2ee68350435a171d182ba6efc9dd70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f906cfd918535c7f2f1b3af08ff4c29ffce9b1c176c8ca28e5f3333bd612aaa3`

```dockerfile
```

-	Layers:
	-	`sha256:0fcec7672387ec22fd81d2b2a8c5de99e7aae50b53faf5bf629ded84a19776d1`  
		Last Modified: Sat, 22 Feb 2025 00:31:32 GMT  
		Size: 2.3 MB (2289021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5d0bd85e2270f2d197500c26d3f1fdc8af08248f560b4dfcee81130a4a3748f`  
		Last Modified: Sat, 22 Feb 2025 00:31:32 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine`

```console
$ docker pull memcached@sha256:c091f8b1a110063b2634d853f3ecda3b873ce70afedc292584f82a5bff7e3446
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
$ docker pull memcached@sha256:787e9120e36559c9aba4cce621188072d00e159bc596fe803c00037f3702c22f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4716929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21a7aa256b160c9c42cce498615225db46d75b42d27b180c3879e9e7d1fbd92`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3e9f8182c72be0cf629032be09e1b5da2b94a8a03a202110036eae2fa538b9`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc58417b03bbd338e8fab898ba984cef01fdb2b2960ae862ecc89bc258a0b981`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 104.7 KB (104690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82369477a539cf4bc0cfd0063cb20ce85cf36442b532dbde15f71a6061abc106`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 968.6 KB (968644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0261a578c93ccd99ba866def61b28a43cc2938598cbc307011db812c246ee206`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cd8dd518d1c91daec2bae1887feb80b6473e0fe5e6846ddb613387e8311c64`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:abae77e9a8d50f01601a4188494f6d7a2e3442e7258fa213a581d2e281fc02c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c452640b5e4fe4e1b31941228c0615b396ec62a56794e1c63e1b9326c5cbf60a`

```dockerfile
```

-	Layers:
	-	`sha256:297387df1b0d33fd74438a8273ab5e20a2a8193785491bcc9b6ad3e03d9c1aa6`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 93.6 KB (93633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0d579b1ca91bec4046749a5bf7a3549239008c1a1083ec2213a3c6004a5725b`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 19.6 KB (19570 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ce3f51d366c64cac4eea49764d62e7fe28b0eaae043336343478a7c929efc8dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5083461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d090618520b70a81c9d35e5a83322a2f92816f0d6925aef9df09030de0d08311`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 05 Feb 2025 01:54:12 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_VERSION=1.6.36
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.36.tar.gz
# Wed, 05 Feb 2025 01:54:12 GMT
ENV MEMCACHED_SHA1=af9696ef8a96f059f643453c299e6acce7f0305c
# Wed, 05 Feb 2025 01:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 05 Feb 2025 01:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 01:54:12 GMT
USER memcache
# Wed, 05 Feb 2025 01:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 05 Feb 2025 01:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b3b947aa71cef021cd9306b1f24a44554e8d663c8530dd36d42b94a883f4c9`  
		Last Modified: Fri, 14 Feb 2025 19:50:13 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6014feb1c2bb2b6c63e9a7b16a3850c447422bdad6e65b302925b8547b23c192`  
		Last Modified: Fri, 14 Feb 2025 19:50:13 GMT  
		Size: 120.8 KB (120780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99010112552ee673d6d495966aaad6261f60804f647797f7c1f469b5a8e1a2e6`  
		Last Modified: Fri, 14 Feb 2025 19:50:13 GMT  
		Size: 968.3 KB (968303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8f67a403c1e521ec7b5f40e063bdd09ef23a311f24f22be50353c692255c5e`  
		Last Modified: Fri, 14 Feb 2025 19:50:13 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503bebaa39aabb9ec92d968d6a001616c3e99d004f2914c79b634a3f86667868`  
		Last Modified: Fri, 14 Feb 2025 19:50:14 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:45d315779fe0ba26e70739761364d7d3d169c66787aa9e695fda292eb2d68c55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae2a22245b82b8df228a72e4532f8dba52f6011a534c034d56e41f3fa17498dc`

```dockerfile
```

-	Layers:
	-	`sha256:3a55f6a29ef4de7c7c715aac043860bba4401f65bacf316fd0c630f98e06f148`  
		Last Modified: Fri, 14 Feb 2025 19:50:13 GMT  
		Size: 93.7 KB (93737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37bd60fea29ca2e6cc7707238eae48e5c684568f11bec6344fa2173fa3880f4e`  
		Last Modified: Fri, 14 Feb 2025 19:50:13 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:46aa92b9d94ea6493f4f5f098e6b1de64f3e8c450eb6440d5bf59f4e1f2ead69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4534801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac2f67d3ec71890e3d6bd391e98b4da571242348ac135e99bcef39979486b34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0216147e703738541dd8987b9b2bc147da47c311b00a06feb265c9f0abf707`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab4b25598c42e6f016cb0a26803d39acd19d7871e0b092cbefd2f8856b0a112`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 109.5 KB (109489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5589cc68943165ccc1b90f645ea08e4c8bb401c6ea2db3506bd1309fd04158`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 960.3 KB (960336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f9697b895d35627f393cf365d336aad6ff6d5d9d767f2ab73d2696751527c1`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a049f6eb832cc266adfa607fe5c42c0710850885d375ee2fd2b22a9add7d29b7`  
		Last Modified: Sat, 22 Feb 2025 00:31:07 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:f9710d1f921ddd802f69f2eb77ae2baa0a046307d13215474dd3f369124034e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de341f780812144f1c4528778277abc1e0f979937153200813e3e66b11d01d02`

```dockerfile
```

-	Layers:
	-	`sha256:4bd1b00215d14ae69987d6066982bb958dbe599471eebf5233fbc9512b4a5fcd`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 93.6 KB (93588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1126652f997b244e12c038e90d03bc059f60adbf626ea9d38c90259a5920775c`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 19.5 KB (19512 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:e3fbb21940e6ecf6e09878be1fdb50cfe7d0ca132112d7439d1c3f266f6b8b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4706934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ab0bd6e09f5b37468b8ae688526c599c21045baf0b0b8bc98ec097e5267b28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deee0b86774e394f5e07eff435a072bdde8922ec1757ef689265af3e1864d632`  
		Last Modified: Fri, 14 Feb 2025 19:42:34 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbafd6c675f155044ba3e5ef96996313b9f05064b966848001c7ea04a9c6048`  
		Last Modified: Fri, 14 Feb 2025 19:42:34 GMT  
		Size: 124.3 KB (124276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56400c974ec4a72a96f97ce1a5828e0ebcb6df76fe5c2f7d8dae29c07223abbf`  
		Last Modified: Sat, 22 Feb 2025 00:34:12 GMT  
		Size: 1.0 MB (1006957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0b9347f26655d1e450da08a0e5a23d5cc368bbfad35a84c643be25c87b2726`  
		Last Modified: Sat, 22 Feb 2025 00:34:11 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5064388d99c64e09f330fcec8ffba565524c380566e6a70fb34aedbf84880f8`  
		Last Modified: Sat, 22 Feb 2025 00:34:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:94cd05711888081e81791841a80e96d16b22ba21e835ba80d125ed65d295b947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84057bf494e545f78faa4d02b570fd42a27b6c3a616d2e07c06013f7125b0ec2`

```dockerfile
```

-	Layers:
	-	`sha256:f969bce286e2478dcbbe6690408d5b20920506d09783024c5e824272ee16cc9e`  
		Last Modified: Sat, 22 Feb 2025 00:34:11 GMT  
		Size: 91.7 KB (91740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93bbfb8bcbd31cfc88a941030e8e18f43fdb73c07293481a932203cb3a25e504`  
		Last Modified: Sat, 22 Feb 2025 00:34:11 GMT  
		Size: 19.6 KB (19648 bytes)  
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
$ docker pull memcached@sha256:0087cdeb03b579438e5e722b991d7e3ee891e4770b26ceeff27c4401cf654657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4571101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2bc2ef8da87893bf85939bd479692ebd280f9d840686e5fdc00089b536aad65`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d658470bb26df23b8a940bc8e53f6c8b685a81ce47a086f683e29b63a6bac496`  
		Last Modified: Fri, 14 Feb 2025 19:44:23 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a07c51d6bc9e389360e3ccba6d95f5697fdd3366a1ac093d59ce54e0da2550`  
		Last Modified: Fri, 14 Feb 2025 19:44:23 GMT  
		Size: 113.5 KB (113462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91fbcb7a7ec7da4c7e8e462c545d152b5a079ef1360a1d05df018c7f78da31e7`  
		Last Modified: Sat, 22 Feb 2025 00:35:17 GMT  
		Size: 988.7 KB (988725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539207d8d3aff51a577331b44e1e08e93ad1330f182ca154c800fa3cc40b77bd`  
		Last Modified: Sat, 22 Feb 2025 00:35:17 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236b320beb51084e2e1b6b838aa193caf573a4292b1353bba1a0cdf076b82db6`  
		Last Modified: Sat, 22 Feb 2025 00:35:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9bd727783dc634399ded38736a232ba7801976d1b0096e07194f53a8f82de528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 KB (111252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7030d08f1e1857ea22b2d774577cb0cb56dd6eb8f7b7ff94fb262e44551c1c`

```dockerfile
```

-	Layers:
	-	`sha256:b7ec10e807d6f8925ef59303e53fc02069fd4a687b1baa66cf3164590cb29d4b`  
		Last Modified: Sat, 22 Feb 2025 00:35:17 GMT  
		Size: 91.7 KB (91682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25a3bb1b2ff42fd2d2a4c3e88ec8af248b5df8c2a42a871dcec17d8a1deb6dbb`  
		Last Modified: Sat, 22 Feb 2025 00:35:17 GMT  
		Size: 19.6 KB (19570 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine3.21`

```console
$ docker pull memcached@sha256:4fb13e4757387000230be124c5a74f107abfd1f65e2526f4c627110d666bf5a3
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
$ docker pull memcached@sha256:787e9120e36559c9aba4cce621188072d00e159bc596fe803c00037f3702c22f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4716929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21a7aa256b160c9c42cce498615225db46d75b42d27b180c3879e9e7d1fbd92`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3e9f8182c72be0cf629032be09e1b5da2b94a8a03a202110036eae2fa538b9`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc58417b03bbd338e8fab898ba984cef01fdb2b2960ae862ecc89bc258a0b981`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 104.7 KB (104690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82369477a539cf4bc0cfd0063cb20ce85cf36442b532dbde15f71a6061abc106`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 968.6 KB (968644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0261a578c93ccd99ba866def61b28a43cc2938598cbc307011db812c246ee206`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cd8dd518d1c91daec2bae1887feb80b6473e0fe5e6846ddb613387e8311c64`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:abae77e9a8d50f01601a4188494f6d7a2e3442e7258fa213a581d2e281fc02c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c452640b5e4fe4e1b31941228c0615b396ec62a56794e1c63e1b9326c5cbf60a`

```dockerfile
```

-	Layers:
	-	`sha256:297387df1b0d33fd74438a8273ab5e20a2a8193785491bcc9b6ad3e03d9c1aa6`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 93.6 KB (93633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0d579b1ca91bec4046749a5bf7a3549239008c1a1083ec2213a3c6004a5725b`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 19.6 KB (19570 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:22169a1786f676798782408232c35b71e12bd32b10164e81c0b32da6143641c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5083533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add144e03275b9c89bb582ad307446fa229055731caf45650896ed6d340a839a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b3b947aa71cef021cd9306b1f24a44554e8d663c8530dd36d42b94a883f4c9`  
		Last Modified: Fri, 14 Feb 2025 19:50:13 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6014feb1c2bb2b6c63e9a7b16a3850c447422bdad6e65b302925b8547b23c192`  
		Last Modified: Fri, 14 Feb 2025 19:50:13 GMT  
		Size: 120.8 KB (120780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b307ec9e1116f91be05519ed18f8206fb49e72d80c7a04638004cf9a82ac2a77`  
		Last Modified: Sat, 22 Feb 2025 00:34:08 GMT  
		Size: 968.4 KB (968374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b643c0752d8cb8b54b8a8d095693feba316ac84b1fd17048fc0189599bc5e1d`  
		Last Modified: Sat, 22 Feb 2025 00:34:08 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38c21d127cb51320d77ca177167435601efbd6ddc02a49c2876aac2884a0109`  
		Last Modified: Sat, 22 Feb 2025 00:34:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:bef45ca6f335dcb09118c5ee88802a722f482af24a9afa8974e7b4800b0fd39f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b1eae2531d72df59778c8c8ac7fecb6d4b6b408b9192cc6ac7d77a5e98128d7`

```dockerfile
```

-	Layers:
	-	`sha256:f675a5a746afeb63892d91271eccac08f3a01bbf6dae0926114e83673197e1be`  
		Last Modified: Sat, 22 Feb 2025 00:34:08 GMT  
		Size: 93.7 KB (93737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74fc4c03468266c50ce86e1314f4c6f45903d6c98465180f75f826dfb54cfcfd`  
		Last Modified: Sat, 22 Feb 2025 00:34:07 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.21` - linux; 386

```console
$ docker pull memcached@sha256:46aa92b9d94ea6493f4f5f098e6b1de64f3e8c450eb6440d5bf59f4e1f2ead69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4534801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac2f67d3ec71890e3d6bd391e98b4da571242348ac135e99bcef39979486b34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0216147e703738541dd8987b9b2bc147da47c311b00a06feb265c9f0abf707`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab4b25598c42e6f016cb0a26803d39acd19d7871e0b092cbefd2f8856b0a112`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 109.5 KB (109489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5589cc68943165ccc1b90f645ea08e4c8bb401c6ea2db3506bd1309fd04158`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 960.3 KB (960336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f9697b895d35627f393cf365d336aad6ff6d5d9d767f2ab73d2696751527c1`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a049f6eb832cc266adfa607fe5c42c0710850885d375ee2fd2b22a9add7d29b7`  
		Last Modified: Sat, 22 Feb 2025 00:31:07 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:f9710d1f921ddd802f69f2eb77ae2baa0a046307d13215474dd3f369124034e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de341f780812144f1c4528778277abc1e0f979937153200813e3e66b11d01d02`

```dockerfile
```

-	Layers:
	-	`sha256:4bd1b00215d14ae69987d6066982bb958dbe599471eebf5233fbc9512b4a5fcd`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 93.6 KB (93588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1126652f997b244e12c038e90d03bc059f60adbf626ea9d38c90259a5920775c`  
		Last Modified: Sat, 22 Feb 2025 00:31:06 GMT  
		Size: 19.5 KB (19512 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.21` - linux; ppc64le

```console
$ docker pull memcached@sha256:e3fbb21940e6ecf6e09878be1fdb50cfe7d0ca132112d7439d1c3f266f6b8b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4706934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ab0bd6e09f5b37468b8ae688526c599c21045baf0b0b8bc98ec097e5267b28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deee0b86774e394f5e07eff435a072bdde8922ec1757ef689265af3e1864d632`  
		Last Modified: Fri, 14 Feb 2025 19:42:34 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbafd6c675f155044ba3e5ef96996313b9f05064b966848001c7ea04a9c6048`  
		Last Modified: Fri, 14 Feb 2025 19:42:34 GMT  
		Size: 124.3 KB (124276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56400c974ec4a72a96f97ce1a5828e0ebcb6df76fe5c2f7d8dae29c07223abbf`  
		Last Modified: Sat, 22 Feb 2025 00:34:12 GMT  
		Size: 1.0 MB (1006957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0b9347f26655d1e450da08a0e5a23d5cc368bbfad35a84c643be25c87b2726`  
		Last Modified: Sat, 22 Feb 2025 00:34:11 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5064388d99c64e09f330fcec8ffba565524c380566e6a70fb34aedbf84880f8`  
		Last Modified: Sat, 22 Feb 2025 00:34:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:94cd05711888081e81791841a80e96d16b22ba21e835ba80d125ed65d295b947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84057bf494e545f78faa4d02b570fd42a27b6c3a616d2e07c06013f7125b0ec2`

```dockerfile
```

-	Layers:
	-	`sha256:f969bce286e2478dcbbe6690408d5b20920506d09783024c5e824272ee16cc9e`  
		Last Modified: Sat, 22 Feb 2025 00:34:11 GMT  
		Size: 91.7 KB (91740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93bbfb8bcbd31cfc88a941030e8e18f43fdb73c07293481a932203cb3a25e504`  
		Last Modified: Sat, 22 Feb 2025 00:34:11 GMT  
		Size: 19.6 KB (19648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.21` - linux; s390x

```console
$ docker pull memcached@sha256:0087cdeb03b579438e5e722b991d7e3ee891e4770b26ceeff27c4401cf654657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4571101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2bc2ef8da87893bf85939bd479692ebd280f9d840686e5fdc00089b536aad65`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d658470bb26df23b8a940bc8e53f6c8b685a81ce47a086f683e29b63a6bac496`  
		Last Modified: Fri, 14 Feb 2025 19:44:23 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a07c51d6bc9e389360e3ccba6d95f5697fdd3366a1ac093d59ce54e0da2550`  
		Last Modified: Fri, 14 Feb 2025 19:44:23 GMT  
		Size: 113.5 KB (113462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91fbcb7a7ec7da4c7e8e462c545d152b5a079ef1360a1d05df018c7f78da31e7`  
		Last Modified: Sat, 22 Feb 2025 00:35:17 GMT  
		Size: 988.7 KB (988725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539207d8d3aff51a577331b44e1e08e93ad1330f182ca154c800fa3cc40b77bd`  
		Last Modified: Sat, 22 Feb 2025 00:35:17 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236b320beb51084e2e1b6b838aa193caf573a4292b1353bba1a0cdf076b82db6`  
		Last Modified: Sat, 22 Feb 2025 00:35:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:9bd727783dc634399ded38736a232ba7801976d1b0096e07194f53a8f82de528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 KB (111252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7030d08f1e1857ea22b2d774577cb0cb56dd6eb8f7b7ff94fb262e44551c1c`

```dockerfile
```

-	Layers:
	-	`sha256:b7ec10e807d6f8925ef59303e53fc02069fd4a687b1baa66cf3164590cb29d4b`  
		Last Modified: Sat, 22 Feb 2025 00:35:17 GMT  
		Size: 91.7 KB (91682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25a3bb1b2ff42fd2d2a4c3e88ec8af248b5df8c2a42a871dcec17d8a1deb6dbb`  
		Last Modified: Sat, 22 Feb 2025 00:35:17 GMT  
		Size: 19.6 KB (19570 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:bookworm`

```console
$ docker pull memcached@sha256:685ba31ae4994ff6daf16d21142346dbd828d0dfbeff3cbc7a7f9b4f5f93b2dd
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
$ docker pull memcached@sha256:bfe5fd0aac5c89b8022c2620abc0a1118cb84d68a74a437ac1fef55be567a23f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31972590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a69266e53d188956df96699ee7bd22b00986730a190789881f82a593361bfc16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d569cc07bddca59980d45ae28a8bfede7584cdca655fad52796e829ac8b7fee`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c58bc9b838a5c291945e3cd889cc93151a03fc70e079914ba998f26239ef2e`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 2.5 MB (2491762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67c97f377dc045ebb683ab2bf6d771520192351043ab7fc20c63ed1a997f84b`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 1.3 MB (1267012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8282d3a602638805126b2e682263fb38ca402e3beaa3a047ed0add1bf754fdb8`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cd8dd518d1c91daec2bae1887feb80b6473e0fe5e6846ddb613387e8311c64`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:ffc24940329fbd38d3efa10fbceb92bc75b8c8e3861170180d934c88ad8659b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a2b67f33d20bb90a8a9305d3ef143d1332d728823aeba14947ec779d5da211`

```dockerfile
```

-	Layers:
	-	`sha256:6ff1804b1ee0e0da242ef1ef47226adb9ac0a4172528e4ac5501443a5e6f3487`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 2.3 MB (2289307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6460f3cc3f151e357a1fa273d42ff4f884c9d2b093c4763cb3c73595fb554fa5`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:abee184952eb3cfc02bd6555047901e0e27fe9379eaddc25acb7805ac3c01e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29079400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c55ad492b5523a9106a2cef2d811d102d5d88a74110653f3187894c060ae61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aa8576c673e5a651f7450bee7603a12ac6168051fdd5b2411678987e180cad6e`  
		Last Modified: Tue, 04 Feb 2025 01:38:28 GMT  
		Size: 25.7 MB (25736549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d03c1f12f429fcd661498f32bc4e1c1e6a1e4189bd6014e71da057147e2286`  
		Last Modified: Tue, 04 Feb 2025 04:58:18 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7e25c626324a280a0e7be83a5642bb48a551515d4c38cb544c66904fcf10bb`  
		Last Modified: Tue, 04 Feb 2025 04:58:19 GMT  
		Size: 2.1 MB (2096073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b068d3f71231f010921a5b6713e177cb20b1838ecd63d09bbfa1cf87d64a1108`  
		Last Modified: Sat, 22 Feb 2025 00:32:42 GMT  
		Size: 1.2 MB (1245268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b49e89cf77efc47a7250f3af153069fc9a2d7696d280b7f9b2ef3ef434a4e1b`  
		Last Modified: Sat, 22 Feb 2025 00:32:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615b1475c4f9cc790d1525380d666d53c7507c87e777e647ed0287598efa3d48`  
		Last Modified: Sat, 22 Feb 2025 00:32:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:b668a646c910c9b5f5c8f752e53b49deb2a1ad6e7ebdc0526adbcf9d299b4ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49e0834cecf5abf237b771c3850e94ba86e05385ccbab4b91cb3d9f063af010c`

```dockerfile
```

-	Layers:
	-	`sha256:cb0b22895c3619cafd6dca713774db852bfe31b3adb4ba3ec6a66838eac945e3`  
		Last Modified: Sat, 22 Feb 2025 00:32:42 GMT  
		Size: 2.3 MB (2292845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d7f06daebcc005d1c5979488409050e03ba04720bf9c424588de02b684b8c03`  
		Last Modified: Sat, 22 Feb 2025 00:32:42 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ecdac108a456c82920f95b934edd7b2c3abf62adf96adac7b99767591b6fecf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31658335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c4d6a0c65f7a9206b9660b5d79d29c8183bb45cef6fa838bbc17493f7085b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85c190a9b2b110c5e0805ab31e5792459e717a286856047e10f45423d8231dd`  
		Last Modified: Wed, 05 Feb 2025 20:31:30 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d150df6d26f3098fb2b4554249a49c854dd5acf5f8255fcf725a970fdbcccbe`  
		Last Modified: Wed, 05 Feb 2025 20:31:31 GMT  
		Size: 2.4 MB (2355307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d34310d49ce6a8c13f0814ea92dbb59638c73a98d899a8f489b4cdba59cf1a4`  
		Last Modified: Sat, 22 Feb 2025 00:31:38 GMT  
		Size: 1.3 MB (1260635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d933eb164ac02e89a9ec663d27d218ab0e489db96ca622ac5023f149bb767f2`  
		Last Modified: Sat, 22 Feb 2025 00:31:38 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3955731998caab6a7273ad7e2b63e663ae711d2f45416977f29c9df6c3a5771`  
		Last Modified: Sat, 22 Feb 2025 00:31:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:b0998d3901cbf4dc98a6f5d0254d7f2115d3d110c1de81a5ec4cc6b56c1afe39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:351b12242d29e072aaf887e69b6b36f8b86fb05d09e37cd2a338014241525536`

```dockerfile
```

-	Layers:
	-	`sha256:c6ec4332029f56a214be68a1da8a91d6170bcc2d2d243daae2353e3cb0baeaae`  
		Last Modified: Sat, 22 Feb 2025 00:31:38 GMT  
		Size: 2.3 MB (2289622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c51e1294036728fb8cdc19970c532c2ced14c50e64984ed76d91eda1e1a61c92`  
		Last Modified: Sat, 22 Feb 2025 00:31:38 GMT  
		Size: 21.4 KB (21419 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; 386

```console
$ docker pull memcached@sha256:ef53c35087afb0499842bedf1fbfa79d5b842f19779b63afa6f1f025a9d5a6ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32956089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e8028b418ebc438bf613b1826c1c627b9c70d0ceba487e067f06ce1140efa93`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a2635855d79b555abffa55c629412da2c4134f2a8ccd4a315c0b6f92b579ae`  
		Last Modified: Sat, 22 Feb 2025 00:31:19 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b44d66689e77fbfe0bc0a0c7e8a45833882611191361e49b6a48030dfbda7bb`  
		Last Modified: Sat, 22 Feb 2025 00:31:20 GMT  
		Size: 2.5 MB (2500720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22086dfd31db842102b740e2bc68682931021ff3fb6491253f9087ca1df6f3cd`  
		Last Modified: Sat, 22 Feb 2025 00:31:19 GMT  
		Size: 1.3 MB (1266399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0d2b64685890c225d3c813b7c867d2d96fb3719d43d4edb206375e55ee6a32`  
		Last Modified: Sat, 22 Feb 2025 00:31:19 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365bc8ba2a50069e758df20bd1b42ff192846fbb115b9edb0cda2fc43fdb2600`  
		Last Modified: Sat, 22 Feb 2025 00:31:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:26ed9f96a812fb5af80816d45e029522166082e249f638019205191bb5b02cb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb94ae18d76a538788c16c601bc76b3509862697a1367bd2fa42cfd5ab18e5b9`

```dockerfile
```

-	Layers:
	-	`sha256:ece746d0e00e98b51635c1914e1aeab67cf6208f531559f2af8346d9e8f40606`  
		Last Modified: Sat, 22 Feb 2025 00:31:20 GMT  
		Size: 2.3 MB (2286406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31ecb87a15a354348411689e2d7bf34846d275e3db9f99b9d2fd53c5d931d382`  
		Last Modified: Sat, 22 Feb 2025 00:31:19 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:61282eccad654d1d03273cc2fb02a4db982d36e9e0ff866eab773795e106ec8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31692298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c72f2790d1441f439ca292b3f0077287e8f93af8f30b6ae44f467f4728aecf0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:60fe4951c23056512065fcf1948d3167c5aa5d83d4bfd2829494b7d09b4fe661`  
		Last Modified: Tue, 04 Feb 2025 01:38:47 GMT  
		Size: 28.5 MB (28486581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006e6bf1f5c579c425dd6a7045b45795f463f886bf4ee3532c5964da484e77c4`  
		Last Modified: Tue, 04 Feb 2025 05:36:04 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa88afbdcfa1d52adc83e6c274708611503deecc6240cf640db7eb23e1999a30`  
		Last Modified: Sat, 22 Feb 2025 00:36:16 GMT  
		Size: 1.9 MB (1943183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dcb0fa418dcf8d7cccdc41a73ad2063c2ae4bf810f2b8a7c67a8ead47c9d684`  
		Last Modified: Sat, 22 Feb 2025 00:36:16 GMT  
		Size: 1.3 MB (1261025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f222082e64a60018ba8bea35cd86f7254591435953a40e022541df5dd42e64`  
		Last Modified: Sat, 22 Feb 2025 00:36:16 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f367b09aa255318629e01e577d62f20d50bcc2cb49cd5519a9c1b68c0829b4e`  
		Last Modified: Sat, 22 Feb 2025 00:36:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:c3872907481511259937b839ceb7f595c2edbf6f47b17ae6cd4e1a10c2456f41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48598526c0aff23b0715615e1f0cd1c35b57f4de0e9b13447903c812540b5683`

```dockerfile
```

-	Layers:
	-	`sha256:308d9f10522a8efc39d94eb5a4f47a8b547bdf8ef47d53a710264ade572dc85b`  
		Last Modified: Sat, 22 Feb 2025 00:36:16 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:10e27fa85f13d51af4a481e4778b04b3b80d506a129aab984fc5d5dab919a8e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36085879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac4b53721162a6ae89b5b0e96dfb4e7ba41127c795c3b9689c36040284ea691`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 01:38:01 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2deccedfff592cdf0e60a1a0f23cfa011cc09854b3b8fd5979a2215801fe859a`  
		Last Modified: Wed, 05 Feb 2025 20:30:01 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f77d137ef9ee5f1f27684f14e816a1f088dfffc4476ab6d02ffa5d251db059`  
		Last Modified: Wed, 05 Feb 2025 20:30:01 GMT  
		Size: 2.7 MB (2708582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163ac5a13dc4a349552e8a728dbfe7a6747c6c194c8f3af433fa8f89ca89614e`  
		Last Modified: Sat, 22 Feb 2025 00:31:22 GMT  
		Size: 1.3 MB (1331006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52cbf6e5ffb6677cc60835d4722667a4e9ac72b9ede1a0a9f282e56abf5dc63`  
		Last Modified: Sat, 22 Feb 2025 00:31:22 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7111ad13f64383b6c5b3388ba5cd00d3804080114fc716c24ebe318a0b45d350`  
		Last Modified: Sat, 22 Feb 2025 00:31:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:8ec0ef0ee501fe9bf349dbf63dce11035a606876a565ee69fd5055418b09d08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8468c14d9febe1b645497e9293a93d6b378bbdb3147a6c0bb18f23a907241bda`

```dockerfile
```

-	Layers:
	-	`sha256:ebd1905c7f20a0d3d102c7b17f531860a3ac45d105b42f0669754a3230ae5fe2`  
		Last Modified: Sat, 22 Feb 2025 00:31:22 GMT  
		Size: 2.3 MB (2293679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b94eff9fb2c5e828a7e6a3ec42729e322d3cc31372e12a5ad1b7eb9761e30a8`  
		Last Modified: Sat, 22 Feb 2025 00:31:21 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:10f8a97eb4da432625002966d78d3993a95f073fb5077a1a4f3cc5a76cd6bab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30261694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a090e8956a7fcbb8b2f590626585d48385828d83d3925e0f8127f400e7c074`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85c3e9bcd86da2086f455efe77a700fe40645a11782885cb35509ae6da968af`  
		Last Modified: Wed, 05 Feb 2025 20:31:33 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25653c174b0d3f4223a55d32a6e019a0a071b0f939c2043a5f3ca38897b6a47`  
		Last Modified: Wed, 05 Feb 2025 20:31:33 GMT  
		Size: 2.2 MB (2156373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86dc255a71b2a050391adb8d18b925df4b93b704a5d38583f893d4c1e1babe1`  
		Last Modified: Sat, 22 Feb 2025 00:31:32 GMT  
		Size: 1.2 MB (1245183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848092fc56244055b7ee89f53de1c07230b0bd2651e37dea23770fc8089383db`  
		Last Modified: Sat, 22 Feb 2025 00:31:33 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab89cd679a4ffa81bbb3cbb213b25b557649024534fef1f253bdaf6f65799c05`  
		Last Modified: Sat, 22 Feb 2025 00:31:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:b70e906e72967b0e6ed1c8be6d754bf62e2ee68350435a171d182ba6efc9dd70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f906cfd918535c7f2f1b3af08ff4c29ffce9b1c176c8ca28e5f3333bd612aaa3`

```dockerfile
```

-	Layers:
	-	`sha256:0fcec7672387ec22fd81d2b2a8c5de99e7aae50b53faf5bf629ded84a19776d1`  
		Last Modified: Sat, 22 Feb 2025 00:31:32 GMT  
		Size: 2.3 MB (2289021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5d0bd85e2270f2d197500c26d3f1fdc8af08248f560b4dfcee81130a4a3748f`  
		Last Modified: Sat, 22 Feb 2025 00:31:32 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:latest`

```console
$ docker pull memcached@sha256:685ba31ae4994ff6daf16d21142346dbd828d0dfbeff3cbc7a7f9b4f5f93b2dd
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
$ docker pull memcached@sha256:bfe5fd0aac5c89b8022c2620abc0a1118cb84d68a74a437ac1fef55be567a23f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31972590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a69266e53d188956df96699ee7bd22b00986730a190789881f82a593361bfc16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d569cc07bddca59980d45ae28a8bfede7584cdca655fad52796e829ac8b7fee`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c58bc9b838a5c291945e3cd889cc93151a03fc70e079914ba998f26239ef2e`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 2.5 MB (2491762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67c97f377dc045ebb683ab2bf6d771520192351043ab7fc20c63ed1a997f84b`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 1.3 MB (1267012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8282d3a602638805126b2e682263fb38ca402e3beaa3a047ed0add1bf754fdb8`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cd8dd518d1c91daec2bae1887feb80b6473e0fe5e6846ddb613387e8311c64`  
		Last Modified: Sat, 22 Feb 2025 00:30:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:ffc24940329fbd38d3efa10fbceb92bc75b8c8e3861170180d934c88ad8659b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a2b67f33d20bb90a8a9305d3ef143d1332d728823aeba14947ec779d5da211`

```dockerfile
```

-	Layers:
	-	`sha256:6ff1804b1ee0e0da242ef1ef47226adb9ac0a4172528e4ac5501443a5e6f3487`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 2.3 MB (2289307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6460f3cc3f151e357a1fa273d42ff4f884c9d2b093c4763cb3c73595fb554fa5`  
		Last Modified: Sat, 22 Feb 2025 00:30:48 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:abee184952eb3cfc02bd6555047901e0e27fe9379eaddc25acb7805ac3c01e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29079400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c55ad492b5523a9106a2cef2d811d102d5d88a74110653f3187894c060ae61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aa8576c673e5a651f7450bee7603a12ac6168051fdd5b2411678987e180cad6e`  
		Last Modified: Tue, 04 Feb 2025 01:38:28 GMT  
		Size: 25.7 MB (25736549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d03c1f12f429fcd661498f32bc4e1c1e6a1e4189bd6014e71da057147e2286`  
		Last Modified: Tue, 04 Feb 2025 04:58:18 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7e25c626324a280a0e7be83a5642bb48a551515d4c38cb544c66904fcf10bb`  
		Last Modified: Tue, 04 Feb 2025 04:58:19 GMT  
		Size: 2.1 MB (2096073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b068d3f71231f010921a5b6713e177cb20b1838ecd63d09bbfa1cf87d64a1108`  
		Last Modified: Sat, 22 Feb 2025 00:32:42 GMT  
		Size: 1.2 MB (1245268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b49e89cf77efc47a7250f3af153069fc9a2d7696d280b7f9b2ef3ef434a4e1b`  
		Last Modified: Sat, 22 Feb 2025 00:32:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615b1475c4f9cc790d1525380d666d53c7507c87e777e647ed0287598efa3d48`  
		Last Modified: Sat, 22 Feb 2025 00:32:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:b668a646c910c9b5f5c8f752e53b49deb2a1ad6e7ebdc0526adbcf9d299b4ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49e0834cecf5abf237b771c3850e94ba86e05385ccbab4b91cb3d9f063af010c`

```dockerfile
```

-	Layers:
	-	`sha256:cb0b22895c3619cafd6dca713774db852bfe31b3adb4ba3ec6a66838eac945e3`  
		Last Modified: Sat, 22 Feb 2025 00:32:42 GMT  
		Size: 2.3 MB (2292845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d7f06daebcc005d1c5979488409050e03ba04720bf9c424588de02b684b8c03`  
		Last Modified: Sat, 22 Feb 2025 00:32:42 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ecdac108a456c82920f95b934edd7b2c3abf62adf96adac7b99767591b6fecf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31658335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c4d6a0c65f7a9206b9660b5d79d29c8183bb45cef6fa838bbc17493f7085b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85c190a9b2b110c5e0805ab31e5792459e717a286856047e10f45423d8231dd`  
		Last Modified: Wed, 05 Feb 2025 20:31:30 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d150df6d26f3098fb2b4554249a49c854dd5acf5f8255fcf725a970fdbcccbe`  
		Last Modified: Wed, 05 Feb 2025 20:31:31 GMT  
		Size: 2.4 MB (2355307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d34310d49ce6a8c13f0814ea92dbb59638c73a98d899a8f489b4cdba59cf1a4`  
		Last Modified: Sat, 22 Feb 2025 00:31:38 GMT  
		Size: 1.3 MB (1260635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d933eb164ac02e89a9ec663d27d218ab0e489db96ca622ac5023f149bb767f2`  
		Last Modified: Sat, 22 Feb 2025 00:31:38 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3955731998caab6a7273ad7e2b63e663ae711d2f45416977f29c9df6c3a5771`  
		Last Modified: Sat, 22 Feb 2025 00:31:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:b0998d3901cbf4dc98a6f5d0254d7f2115d3d110c1de81a5ec4cc6b56c1afe39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:351b12242d29e072aaf887e69b6b36f8b86fb05d09e37cd2a338014241525536`

```dockerfile
```

-	Layers:
	-	`sha256:c6ec4332029f56a214be68a1da8a91d6170bcc2d2d243daae2353e3cb0baeaae`  
		Last Modified: Sat, 22 Feb 2025 00:31:38 GMT  
		Size: 2.3 MB (2289622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c51e1294036728fb8cdc19970c532c2ced14c50e64984ed76d91eda1e1a61c92`  
		Last Modified: Sat, 22 Feb 2025 00:31:38 GMT  
		Size: 21.4 KB (21419 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:ef53c35087afb0499842bedf1fbfa79d5b842f19779b63afa6f1f025a9d5a6ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32956089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e8028b418ebc438bf613b1826c1c627b9c70d0ceba487e067f06ce1140efa93`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a2635855d79b555abffa55c629412da2c4134f2a8ccd4a315c0b6f92b579ae`  
		Last Modified: Sat, 22 Feb 2025 00:31:19 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b44d66689e77fbfe0bc0a0c7e8a45833882611191361e49b6a48030dfbda7bb`  
		Last Modified: Sat, 22 Feb 2025 00:31:20 GMT  
		Size: 2.5 MB (2500720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22086dfd31db842102b740e2bc68682931021ff3fb6491253f9087ca1df6f3cd`  
		Last Modified: Sat, 22 Feb 2025 00:31:19 GMT  
		Size: 1.3 MB (1266399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0d2b64685890c225d3c813b7c867d2d96fb3719d43d4edb206375e55ee6a32`  
		Last Modified: Sat, 22 Feb 2025 00:31:19 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365bc8ba2a50069e758df20bd1b42ff192846fbb115b9edb0cda2fc43fdb2600`  
		Last Modified: Sat, 22 Feb 2025 00:31:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:26ed9f96a812fb5af80816d45e029522166082e249f638019205191bb5b02cb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb94ae18d76a538788c16c601bc76b3509862697a1367bd2fa42cfd5ab18e5b9`

```dockerfile
```

-	Layers:
	-	`sha256:ece746d0e00e98b51635c1914e1aeab67cf6208f531559f2af8346d9e8f40606`  
		Last Modified: Sat, 22 Feb 2025 00:31:20 GMT  
		Size: 2.3 MB (2286406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31ecb87a15a354348411689e2d7bf34846d275e3db9f99b9d2fd53c5d931d382`  
		Last Modified: Sat, 22 Feb 2025 00:31:19 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; mips64le

```console
$ docker pull memcached@sha256:61282eccad654d1d03273cc2fb02a4db982d36e9e0ff866eab773795e106ec8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31692298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c72f2790d1441f439ca292b3f0077287e8f93af8f30b6ae44f467f4728aecf0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:60fe4951c23056512065fcf1948d3167c5aa5d83d4bfd2829494b7d09b4fe661`  
		Last Modified: Tue, 04 Feb 2025 01:38:47 GMT  
		Size: 28.5 MB (28486581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006e6bf1f5c579c425dd6a7045b45795f463f886bf4ee3532c5964da484e77c4`  
		Last Modified: Tue, 04 Feb 2025 05:36:04 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa88afbdcfa1d52adc83e6c274708611503deecc6240cf640db7eb23e1999a30`  
		Last Modified: Sat, 22 Feb 2025 00:36:16 GMT  
		Size: 1.9 MB (1943183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dcb0fa418dcf8d7cccdc41a73ad2063c2ae4bf810f2b8a7c67a8ead47c9d684`  
		Last Modified: Sat, 22 Feb 2025 00:36:16 GMT  
		Size: 1.3 MB (1261025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f222082e64a60018ba8bea35cd86f7254591435953a40e022541df5dd42e64`  
		Last Modified: Sat, 22 Feb 2025 00:36:16 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f367b09aa255318629e01e577d62f20d50bcc2cb49cd5519a9c1b68c0829b4e`  
		Last Modified: Sat, 22 Feb 2025 00:36:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:c3872907481511259937b839ceb7f595c2edbf6f47b17ae6cd4e1a10c2456f41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48598526c0aff23b0715615e1f0cd1c35b57f4de0e9b13447903c812540b5683`

```dockerfile
```

-	Layers:
	-	`sha256:308d9f10522a8efc39d94eb5a4f47a8b547bdf8ef47d53a710264ade572dc85b`  
		Last Modified: Sat, 22 Feb 2025 00:36:16 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:10e27fa85f13d51af4a481e4778b04b3b80d506a129aab984fc5d5dab919a8e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36085879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac4b53721162a6ae89b5b0e96dfb4e7ba41127c795c3b9689c36040284ea691`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 01:38:01 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2deccedfff592cdf0e60a1a0f23cfa011cc09854b3b8fd5979a2215801fe859a`  
		Last Modified: Wed, 05 Feb 2025 20:30:01 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f77d137ef9ee5f1f27684f14e816a1f088dfffc4476ab6d02ffa5d251db059`  
		Last Modified: Wed, 05 Feb 2025 20:30:01 GMT  
		Size: 2.7 MB (2708582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163ac5a13dc4a349552e8a728dbfe7a6747c6c194c8f3af433fa8f89ca89614e`  
		Last Modified: Sat, 22 Feb 2025 00:31:22 GMT  
		Size: 1.3 MB (1331006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52cbf6e5ffb6677cc60835d4722667a4e9ac72b9ede1a0a9f282e56abf5dc63`  
		Last Modified: Sat, 22 Feb 2025 00:31:22 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7111ad13f64383b6c5b3388ba5cd00d3804080114fc716c24ebe318a0b45d350`  
		Last Modified: Sat, 22 Feb 2025 00:31:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:8ec0ef0ee501fe9bf349dbf63dce11035a606876a565ee69fd5055418b09d08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8468c14d9febe1b645497e9293a93d6b378bbdb3147a6c0bb18f23a907241bda`

```dockerfile
```

-	Layers:
	-	`sha256:ebd1905c7f20a0d3d102c7b17f531860a3ac45d105b42f0669754a3230ae5fe2`  
		Last Modified: Sat, 22 Feb 2025 00:31:22 GMT  
		Size: 2.3 MB (2293679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b94eff9fb2c5e828a7e6a3ec42729e322d3cc31372e12a5ad1b7eb9761e30a8`  
		Last Modified: Sat, 22 Feb 2025 00:31:21 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:10f8a97eb4da432625002966d78d3993a95f073fb5077a1a4f3cc5a76cd6bab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30261694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a090e8956a7fcbb8b2f590626585d48385828d83d3925e0f8127f400e7c074`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85c3e9bcd86da2086f455efe77a700fe40645a11782885cb35509ae6da968af`  
		Last Modified: Wed, 05 Feb 2025 20:31:33 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25653c174b0d3f4223a55d32a6e019a0a071b0f939c2043a5f3ca38897b6a47`  
		Last Modified: Wed, 05 Feb 2025 20:31:33 GMT  
		Size: 2.2 MB (2156373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86dc255a71b2a050391adb8d18b925df4b93b704a5d38583f893d4c1e1babe1`  
		Last Modified: Sat, 22 Feb 2025 00:31:32 GMT  
		Size: 1.2 MB (1245183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848092fc56244055b7ee89f53de1c07230b0bd2651e37dea23770fc8089383db`  
		Last Modified: Sat, 22 Feb 2025 00:31:33 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab89cd679a4ffa81bbb3cbb213b25b557649024534fef1f253bdaf6f65799c05`  
		Last Modified: Sat, 22 Feb 2025 00:31:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:b70e906e72967b0e6ed1c8be6d754bf62e2ee68350435a171d182ba6efc9dd70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f906cfd918535c7f2f1b3af08ff4c29ffce9b1c176c8ca28e5f3333bd612aaa3`

```dockerfile
```

-	Layers:
	-	`sha256:0fcec7672387ec22fd81d2b2a8c5de99e7aae50b53faf5bf629ded84a19776d1`  
		Last Modified: Sat, 22 Feb 2025 00:31:32 GMT  
		Size: 2.3 MB (2289021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5d0bd85e2270f2d197500c26d3f1fdc8af08248f560b4dfcee81130a4a3748f`  
		Last Modified: Sat, 22 Feb 2025 00:31:32 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json
