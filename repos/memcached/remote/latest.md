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
