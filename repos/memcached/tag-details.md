<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `memcached`

-	[`memcached:1`](#memcached1)
-	[`memcached:1-alpine`](#memcached1-alpine)
-	[`memcached:1-alpine3.20`](#memcached1-alpine320)
-	[`memcached:1-bookworm`](#memcached1-bookworm)
-	[`memcached:1.6`](#memcached16)
-	[`memcached:1.6-alpine`](#memcached16-alpine)
-	[`memcached:1.6-alpine3.20`](#memcached16-alpine320)
-	[`memcached:1.6-bookworm`](#memcached16-bookworm)
-	[`memcached:1.6.28`](#memcached1628)
-	[`memcached:1.6.28-alpine`](#memcached1628-alpine)
-	[`memcached:1.6.28-alpine3.20`](#memcached1628-alpine320)
-	[`memcached:1.6.28-bookworm`](#memcached1628-bookworm)
-	[`memcached:alpine`](#memcachedalpine)
-	[`memcached:alpine3.20`](#memcachedalpine320)
-	[`memcached:bookworm`](#memcachedbookworm)
-	[`memcached:latest`](#memcachedlatest)

## `memcached:1`

```console
$ docker pull memcached@sha256:6bc6193233fb86bb8deaf6706445bd3e55b1e786bbea8c642bb42462e0d5fa9b
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
$ docker pull memcached@sha256:9147945260ea3aae4982858f21c236318a3f6e714e3247c5baf29a5a72e0f541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32898057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23286975f91428ab86b108f596c0340aed9fc99015d547119acc7f7aaf10007e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc543897dce5b0ec373146149c07d4d311f530d35fd5660eacf896059d19c1f9`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67696248863aa6bf5473db03626425b13368fab900b2145458a0aadf3ec50685`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 2.5 MB (2488532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1225c54544336958562027d237b24c6e6fdf0242b27fedb8de59463271161a`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 1.3 MB (1257596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c8c669390569241c531942ed6c73e9ed972acd0d553620dc73b27efd017da4`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750d4cc56720b2b3726c433153484ee8befc8ef867db54c4ea893932042208b4`  
		Last Modified: Mon, 03 Jun 2024 19:03:49 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:16ed0d681048581dce561ae4090acbdcf920ce1f2ddce248215521ed4fd9decd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d6ffeaf490e2efb6c46e0c490e1c11020fcf721e84a6b2d8edef168a450b00`

```dockerfile
```

-	Layers:
	-	`sha256:7055f894d5826460bb2eb3ea9b0ef5d51df1ce6b1c073f786f5d1cf92573a368`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 2.3 MB (2261260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1e66ce28cc0bd263cb0b4aa93ffcc60f78c1c750f403cbd3ab265a6794fc167`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 21.0 KB (20979 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v5

```console
$ docker pull memcached@sha256:14753c4e01088e08a436d89d02a2a78902028bf49d6db1569f475092fd460bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30237639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c21e319ac699c14e10d279852e999e826acf2731ee4b72c4c10a33bb47692f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 00:48:34 GMT
ADD file:ee9f1914c7fc370bdb089c9e2fcfa15477f7091fc5437cb780232afdf6297586 in / 
# Tue, 14 May 2024 00:48:34 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:169fcae2368e5a601c42972560f091e123648fa0e741975d1b35900c61b9ff71`  
		Last Modified: Tue, 14 May 2024 00:51:36 GMT  
		Size: 26.9 MB (26909921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6135c82883bf5f0df15a6d3d42e97b6013681d12f1f0d535ccb0c1cacf6676b`  
		Last Modified: Mon, 03 Jun 2024 19:08:33 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51f9357aee8294bc0ab883e4493123d2a4dabd21e30ab2900da6cfe6fce5b20`  
		Last Modified: Mon, 03 Jun 2024 19:08:34 GMT  
		Size: 2.1 MB (2089512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32e18a9983de65ed92d9394655a09d3d69089e493a069562641ea42c679e1a4`  
		Last Modified: Mon, 03 Jun 2024 19:08:34 GMT  
		Size: 1.2 MB (1236688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc76114b0bb29114c4b5ff03c2b92a6a317377e26442ec0b79e0016bdc73147d`  
		Last Modified: Mon, 03 Jun 2024 19:08:33 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c636887432e5986c55e92368eef61a43bd3e05cd00609197541f460647ef8208`  
		Last Modified: Mon, 03 Jun 2024 19:08:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:3db3baea327d4e01491ca8527e9a966a8bc9c6fb518a0f2850e7418c158eb8f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84af36590abfbf847e39461d5668a9b85b5846ab2c1705bdf2e8858807e9d86c`

```dockerfile
```

-	Layers:
	-	`sha256:aaab43908073c0eddfc13729d70514a3426255ff8d31aa19aa39108390f5c65d`  
		Last Modified: Mon, 03 Jun 2024 19:08:34 GMT  
		Size: 2.3 MB (2264548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6af6c6fa69438301c0c320846677e25900a5aa269506c074071536e7fdc092ff`  
		Last Modified: Mon, 03 Jun 2024 19:08:33 GMT  
		Size: 21.1 KB (21120 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b953ca66ecee777524a0f33f0adefbe99183367e180f4b2ed82d1e525f57d208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32780663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a9c7e97a66ca554c0cfc88de871b1c7dfad7637ffcbd6a79b5c75b3954bb583`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
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
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994933505bafbbaba95cef494f2dfb3e85f2bfde1ea5c4a6dae5a179e39e7b5c`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9488359f89f8c6691f1737ce76ce6b7520511a8246658953dae9429090e88746`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 2.3 MB (2346183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fa925bb96d2305b22651dc4d10899309c212aef95cb13afbdeb2ba5436cb0b`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 1.3 MB (1253469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5284a06f3ca2503602cf214d936daf8aedee3d442d7aa66a5b67874c8f156685`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a475f5b1bcd9a980f0e2923bf1af87002c6468529583ce41a151599d11b2cc`  
		Last Modified: Tue, 14 May 2024 17:41:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:303a74af5e224338560198dc50e2c9cb2a7b4a46b01d39144559de1dd7788518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e79fb901bf217f30113856b6b39e296324993066435904abd2a2152baae6156`

```dockerfile
```

-	Layers:
	-	`sha256:a35747f1af90484d4a9021de5c31be89cb3117cb5f56f499d3cebe78562716cf`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 2.3 MB (2261490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48c7060af35b31db7e804b3ce19451726c3fb6b956edad221ee58000cf04a91`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 21.0 KB (20997 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:36e236fc6b16e7e3170743b8c6a4fbaa296f4d7804c6c2b2106171eac49c9e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33915077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46c7f4bc09921dd239f3c7eb02f4989d48a1df441f3bc33fa1eac70860b0ae6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 00:47:12 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Tue, 14 May 2024 00:47:12 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb23370f3994993b447e434bb257c1618064ae75acb7e15d1fb88d95c481416`  
		Last Modified: Mon, 03 Jun 2024 19:03:52 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43508bc095d4cad435f08c64c32dd8056399b25cddfeca86964d15f117cbd0c`  
		Last Modified: Mon, 03 Jun 2024 19:03:52 GMT  
		Size: 2.5 MB (2492668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2870f8c3ee5b47d7a6a8e194db84b04de521e6a228093ad33b4252661ee3d0d0`  
		Last Modified: Mon, 03 Jun 2024 19:03:52 GMT  
		Size: 1.3 MB (1258253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c83af100d615d1363ef33866755b85f6153e23f56a4e9c1a6cba13d0463082d`  
		Last Modified: Mon, 03 Jun 2024 19:03:53 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ec3bf8bf691991f57de6b00811ed6d06fe0417f1955d1d7b6cd33ecf81b406`  
		Last Modified: Mon, 03 Jun 2024 19:03:53 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:443d7accdadab953db276145a1ab012f3232c120ea362461be5a22531600dca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da086c82559c925e7fcc2b0c79e47076545d92a837f0e4d1b8f49b66cfb55fc0`

```dockerfile
```

-	Layers:
	-	`sha256:829f8d9a7d33b902a3c59de1e19bd0291df3704cf233de30580da78a72c5220f`  
		Last Modified: Mon, 03 Jun 2024 19:03:52 GMT  
		Size: 2.3 MB (2258358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffb9dd39ce17614aed4cd4f0bac42e7b8bb49b726b85d39d48b1700119a54cf0`  
		Last Modified: Mon, 03 Jun 2024 19:03:52 GMT  
		Size: 20.9 KB (20924 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; mips64le

```console
$ docker pull memcached@sha256:129ad612a59e558c3da7dfa1a1958d7b374599149ad2ac085bfd539341b0e76d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32335816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4ee8bdf9b447076bff1edf5bfe8aafd428b9e3a1c11745e3eac190a7957b50d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 01:11:07 GMT
ADD file:a92da94a28279478b2eae11dcdcd2913fc06af02498a5515cc3f288668d74e43 in / 
# Tue, 14 May 2024 01:11:12 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6ccc6628d3cdcda935b3b60cb54fa578d669965454d9cf39de3df9c1276132b7`  
		Last Modified: Tue, 14 May 2024 01:22:19 GMT  
		Size: 29.1 MB (29143688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2c2342dfc8d9203635e3e3bc46109d12ef7ef9940adb0794934bca415e4d79`  
		Last Modified: Mon, 03 Jun 2024 19:52:36 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba60c707dc72485dffcb0f586703d60083e3a99568905fc77c61a927aa023133`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 1.9 MB (1937709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5d0dde6405cfccdcc1ece97791b0c134d743d3dbbb4648cfd8ffa51f7fa7fa`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 1.3 MB (1252902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c5806cc8f133288ec076e5d9a6d04f2f7528380144d22892c7b84314c99a8c`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198d6a5f4cd3ba446c2120eb2826773388a541360046c35203d6024dce60a143`  
		Last Modified: Mon, 03 Jun 2024 19:52:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:bf5993b43a4118f01f52ac8a194cb102c52ee5b81fe6f6217d77ca4afaef2a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295c96051f2df83e45a2fe340023dd1e664fdec31e7ef871ca8d797cbc594205`

```dockerfile
```

-	Layers:
	-	`sha256:396ed31b018a1dc19cc7f9fcd8bc9c31f7d68c64735199594c25d0801926c1b7`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:63978abc93d511e5c74a4cc84e7b57a1d767833ba0c69e02c29365668c96bf86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37163958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9054e0ed4fdeb443fcae69bad304d1e19e2434684bbca08c83f5ef5897d1e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 01:20:02 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Tue, 14 May 2024 01:20:04 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:11ee2a6dbc4a6a6b182097f6023f775e595488a6bcc424e9b58001659deb7fa1`  
		Last Modified: Tue, 14 May 2024 01:24:06 GMT  
		Size: 33.1 MB (33141160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d531128e0fac13a6c4e8656afa2e85afbd55db7a786a38bf715c14f4e05a5d94`  
		Last Modified: Mon, 03 Jun 2024 19:50:52 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037940292acc903c706efafe81e090f3eca4683a90304378efe5f4b2cd3cbd47`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 2.7 MB (2698394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d2e0144b8349ea33bdc906d060868aa61958e0c45ac421dcf26a5fc15eb677`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 1.3 MB (1322885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02930e85eb728b1b92f67233fa0c4ff46787e43e4c5f78933df1a64f4c1f7ad0`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cb49628af48f1c1c75566128625afdacca39df7ea0a7c2762ff858d5a3c3e9`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:eae1092d4dd48c0f18e3eda2c5440fe8988dc3823060e738b93a20fba09baf54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea636723fe65c22cb491ee51203b6349d5302ba3288e8ebf7395457c83a78a3`

```dockerfile
```

-	Layers:
	-	`sha256:0c88ae099fbb77c9cefb907169eb358536ff37e4c35140a81c2cb67411da7a9f`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 2.3 MB (2265631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba09bde198a5df307f36fa75f66fe410b324cf250153ce67c8d2f7e9def7d0e5`  
		Last Modified: Mon, 03 Jun 2024 19:50:52 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:da94175eec280d37f0dfd2d8acdc57bd8b4607f66f738dd796b0719c28737986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30903401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf7fe752edb4161d9cd43825ddd58ceff332eb34c41dcc9623255e4cc9bf376`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 00:42:38 GMT
ADD file:55fef93bbad6701fe968a070a0c72b3a0bd3df408dd79c9a616a43dea0de11d0 in / 
# Tue, 14 May 2024 00:42:40 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d7365433874e83ccc92aa5d768989641a64e23c3247409161401a09b4895c406`  
		Last Modified: Tue, 14 May 2024 00:47:35 GMT  
		Size: 27.5 MB (27512398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422d2a0f87a8b8c2712bf0d473e4f936bcbad2af462760d8ae88a25a4ddcbabe`  
		Last Modified: Mon, 03 Jun 2024 19:40:44 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dac9575eb2b0b2d47b6c792dddf0edd2afdeaad0f5dc8a1572996977ceb0fa6`  
		Last Modified: Mon, 03 Jun 2024 19:40:44 GMT  
		Size: 2.2 MB (2152694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e3eb594a178112f9ea3d30d498b8b619b5165ff992e96e66a2cb723b708eea`  
		Last Modified: Mon, 03 Jun 2024 19:40:44 GMT  
		Size: 1.2 MB (1236790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f6ebc8f32f01f7f87e92d446e389a62516dcde1dd8b66b0ed80618c1279d7f`  
		Last Modified: Mon, 03 Jun 2024 19:40:45 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b1370c7b0f96a4cb325b9cd27e7cc508def3a755eaf10f7f2893a6d721d6b6`  
		Last Modified: Mon, 03 Jun 2024 19:40:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:b7e29c218845ad20177e6072bafe8ceb34957f028c9ab5dc784bf0d8abb3266b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:801c05520a31b4c181fcea7491e35a45441ce8b7d97f9f1133ce0da9982b9f65`

```dockerfile
```

-	Layers:
	-	`sha256:7059681ccb9077ae5d5d066a76afbdf315e577e6f6185513b43dc17567fd6a41`  
		Last Modified: Mon, 03 Jun 2024 19:40:44 GMT  
		Size: 2.3 MB (2261081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d33b5d8c8737f3f638401087329e3541977c1b45f846a92a33f44bc802633636`  
		Last Modified: Mon, 03 Jun 2024 19:40:44 GMT  
		Size: 21.0 KB (20979 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:dcdfc647eaab83cce1e15874888f7e28bdae4b1b947f637e45fec64db1d1a3e3
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
$ docker pull memcached@sha256:7e7f1b92cbd46c4b5f60777f034debc77c1b66bd5b66b732e424d47bc9fbeed0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4681905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae47e754356b145ac3883025be70df81397e012b7b9deea79c6e1549cebb820`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723fe97584e549852ab448538bb35f45d46da4b09c52e18fa4eeec5352c47a42`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5f2dacb5179622644f1e47531960f1fa5aef816fb60aad38a20349103c7191`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 103.8 KB (103828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef494bb92067167934aab739f7d1f023f4e34ef112f973afc201b98e54fa5d50`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 954.6 KB (954617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd803b6c0eb021a0b33649dd96256f867eac7aa91b9255624ed7f239c9475ff`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1c222c9d9e5ee0e2e34c4386e9c09b7ebf79a12072e245332f295c63bddf3e`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2dd815e2d1643bcba94e92c59e4c260f02bf06b0ff954840272439de861358f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 KB (103568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0885c1305da890646b6ad6dbcd2ae57932bcd2d1b804dc7404de2cd8713cc284`

```dockerfile
```

-	Layers:
	-	`sha256:6e6853da7f25eec4b641df434dccd72f8d65a0a540787c715049bd366d0f787b`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 84.3 KB (84267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b7bd473fc9187722cabb9a96acad9c5a1dbb88c26431928b2166223fb0dee7c`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 19.3 KB (19301 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:e0688d9873a4cf749f89b43548d03f7d6c873596b1495b6da6943d4a3e767df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5166898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6a1a46a5867d6ecd3c9bf99a695a89cc1f746f59d3a9a140b85a42b99a2e26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_VERSION=1.6.27
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 22 May 2024 18:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:54:12 GMT
USER memcache
# Wed, 22 May 2024 18:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 May 2024 18:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024a9ccd1af8ffcfe453e22adead9362703e916c9dec4f1d4e94b597e660f23e`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab592fa6ce63bf6772b1c208275d773ef6e671af73b2bd119e98de86dce4fc1`  
		Last Modified: Thu, 23 May 2024 06:29:58 GMT  
		Size: 121.0 KB (121017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd20d288c43aabf4d5e06a885b2e2f24583aae8e102eca2bf9257ce5e307a2cd`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 957.7 KB (957743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d039a0fcb8c2c4f062cb3fb5c2b20ae16915479721254aadfc68d0319c84ee25`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cf5bc5246a4e40149d2a6b161c9fbce8354373e305c03088715546070c2742`  
		Last Modified: Thu, 23 May 2024 06:29:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ec1932014529a81f308cae2db47073ddf344ef48cbc77766d95510cb7385b2af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 KB (103606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0d85c8cad5520d9245c1563457fcf55da9b744f736c305ad21fad10027e013`

```dockerfile
```

-	Layers:
	-	`sha256:f77bdac9710cd22ef4eb7ba293b1b4fe4736e109a3767950432991fe0237fa54`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 84.3 KB (84287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12016cd6764c2821a23d0e8fb3c182eda4d12d096e83cf52f57eb0103616d5e8`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 19.3 KB (19319 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:d021aa4701a1cbf3afb535aa82cd88bc0f7c5d51c05c34d5160fabd876a5bce7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d85661f9f9c582ffadd4540ae1b2fb7bf653da454d36eab21d69ed0aa33ddb7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:05:50 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 18:05:51 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77c9b09b82af8bb67811ab3d796c64874348624abc7cf7658894f3042e3fdda`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61451eaaecf42ca95101dad4ed37d00cf792b8afae1d5eeab46e43e258b3ef4`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 109.0 KB (108954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1cfe9a7dc0eb6422fdd3e24036097ac92ebb3781776994ac1a1985641b7746a`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 947.9 KB (947940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffa1b620c706dc7fccfe69ac07a840b285472eebf3a5b12f4627f73b14a8262`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3107d914479457d4f68098546010a68c957c8958f8617fe612a4de36890751d`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:f7757ea9df5138c45bdbcd9e258bd5f8d3b847272ba419799988079f669fbe74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 KB (103468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f14b161d58134f0ae5adc6bf8b94c753848d136ed143b505c68fd6d0083ef5e`

```dockerfile
```

-	Layers:
	-	`sha256:977ffaf9dabb1b3eba7edd08c3c73174de9a29484b0f80d86a81072bb317517f`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 84.2 KB (84222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d4314a7e1c917ad745b623d3c1ea185133876babcee74b1048a636196ae0e48`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 19.2 KB (19246 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:0b9a2b083716079e6c1da7a9eef4cda25b8d81f3e16840ca6b2b12e9d90e00b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c5555e7ff1014a88296e46cd6d51b379698f7678f76fcd835e8c9f30d647d79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f168e15e72e8585ac6cf20d04f29cfeea15135f34178693fec86adfd88204d`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e2f6d65a966b68fa13bdc24e920a1a1fa7b86b2e000d17eff60efbfdd38993`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 123.0 KB (123004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5864e6eb973cda0b80fc0b600b8fdc61cab246b23ff08158ec77e3c819aacb99`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 992.9 KB (992907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af9bfa929a4b7886285f34b50a2506270b5db318f414db5cfa7c505e069495e`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf6c5b09507827cb18669a5979a2e3e258baa20df3c7d3b1790c8e47c4da755`  
		Last Modified: Mon, 03 Jun 2024 19:53:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:47e12d8b1103b819e814e52b644a34f6fd25e9b3c301cf64bd3a5aed59882a32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 KB (101740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac2cf30c8b57070d3d517da1a03e3bf9241f943b85fa56a7a7cafcec23db720f`

```dockerfile
```

-	Layers:
	-	`sha256:bf26f6e69d9a08fc6932c97112ad23a6a9b487855c46d9d7e0c8bddd8b5292f2`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 82.4 KB (82371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:018afee57a818e12505b2c4851b768103c8b30b0796588e3def21bb1bb3e7d24`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 19.4 KB (19369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:c9d716888f3de4b62fcb97a29f86e58ace3ecd27d3e140bf093a91a55b457895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4551732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98e758f93cfeb8699e726a62495bbcb588c84eb23144c8f4fef5e84556142be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b951b4f532c41c7412daf128075fc9cd89c182acbc79418cb89d9bdcca3f7f5`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ace4ff1604d5e2114f279c4a7dbd9c7255f5c22442459e1dde1e1dba3c3662`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 112.7 KB (112734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3635c0cf5ff89eaa5a72c24ee555909e50ee12d3629572ef94a113391f5b0e92`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 977.3 KB (977292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e93a0ef4a20f636cd8f486379f0e8926c809875d1be02f187e1d9beb0155870`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2e88b16dd19768ead777afafdc9ec27072ab209e2f240c51dce37ce1590302`  
		Last Modified: Mon, 03 Jun 2024 19:44:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7e094c1f57f2f2a6a9f5e6290afe42f796d0444a80835660c23f0880808b9fac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 KB (101612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22673137bae204447eabe141346d72e57cec6908c114a55f94494e572a484849`

```dockerfile
```

-	Layers:
	-	`sha256:245be0555de7893afdeab5ba2e974bc77e29549c40a4bdb62d8b49cdd98938c8`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 82.3 KB (82313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41c84b152f2dcb64eb163c14efbbe0d430a1cd597e9fe2a74c52c447568f2d9f`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 19.3 KB (19299 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine3.20`

```console
$ docker pull memcached@sha256:dcdfc647eaab83cce1e15874888f7e28bdae4b1b947f637e45fec64db1d1a3e3
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

### `memcached:1-alpine3.20` - linux; amd64

```console
$ docker pull memcached@sha256:7e7f1b92cbd46c4b5f60777f034debc77c1b66bd5b66b732e424d47bc9fbeed0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4681905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae47e754356b145ac3883025be70df81397e012b7b9deea79c6e1549cebb820`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723fe97584e549852ab448538bb35f45d46da4b09c52e18fa4eeec5352c47a42`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5f2dacb5179622644f1e47531960f1fa5aef816fb60aad38a20349103c7191`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 103.8 KB (103828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef494bb92067167934aab739f7d1f023f4e34ef112f973afc201b98e54fa5d50`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 954.6 KB (954617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd803b6c0eb021a0b33649dd96256f867eac7aa91b9255624ed7f239c9475ff`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1c222c9d9e5ee0e2e34c4386e9c09b7ebf79a12072e245332f295c63bddf3e`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:2dd815e2d1643bcba94e92c59e4c260f02bf06b0ff954840272439de861358f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 KB (103568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0885c1305da890646b6ad6dbcd2ae57932bcd2d1b804dc7404de2cd8713cc284`

```dockerfile
```

-	Layers:
	-	`sha256:6e6853da7f25eec4b641df434dccd72f8d65a0a540787c715049bd366d0f787b`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 84.3 KB (84267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b7bd473fc9187722cabb9a96acad9c5a1dbb88c26431928b2166223fb0dee7c`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 19.3 KB (19301 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:e0688d9873a4cf749f89b43548d03f7d6c873596b1495b6da6943d4a3e767df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5166898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6a1a46a5867d6ecd3c9bf99a695a89cc1f746f59d3a9a140b85a42b99a2e26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_VERSION=1.6.27
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 22 May 2024 18:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:54:12 GMT
USER memcache
# Wed, 22 May 2024 18:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 May 2024 18:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024a9ccd1af8ffcfe453e22adead9362703e916c9dec4f1d4e94b597e660f23e`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab592fa6ce63bf6772b1c208275d773ef6e671af73b2bd119e98de86dce4fc1`  
		Last Modified: Thu, 23 May 2024 06:29:58 GMT  
		Size: 121.0 KB (121017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd20d288c43aabf4d5e06a885b2e2f24583aae8e102eca2bf9257ce5e307a2cd`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 957.7 KB (957743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d039a0fcb8c2c4f062cb3fb5c2b20ae16915479721254aadfc68d0319c84ee25`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cf5bc5246a4e40149d2a6b161c9fbce8354373e305c03088715546070c2742`  
		Last Modified: Thu, 23 May 2024 06:29:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:ec1932014529a81f308cae2db47073ddf344ef48cbc77766d95510cb7385b2af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 KB (103606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0d85c8cad5520d9245c1563457fcf55da9b744f736c305ad21fad10027e013`

```dockerfile
```

-	Layers:
	-	`sha256:f77bdac9710cd22ef4eb7ba293b1b4fe4736e109a3767950432991fe0237fa54`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 84.3 KB (84287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12016cd6764c2821a23d0e8fb3c182eda4d12d096e83cf52f57eb0103616d5e8`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 19.3 KB (19319 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; 386

```console
$ docker pull memcached@sha256:d021aa4701a1cbf3afb535aa82cd88bc0f7c5d51c05c34d5160fabd876a5bce7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d85661f9f9c582ffadd4540ae1b2fb7bf653da454d36eab21d69ed0aa33ddb7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:05:50 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 18:05:51 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77c9b09b82af8bb67811ab3d796c64874348624abc7cf7658894f3042e3fdda`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61451eaaecf42ca95101dad4ed37d00cf792b8afae1d5eeab46e43e258b3ef4`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 109.0 KB (108954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1cfe9a7dc0eb6422fdd3e24036097ac92ebb3781776994ac1a1985641b7746a`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 947.9 KB (947940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffa1b620c706dc7fccfe69ac07a840b285472eebf3a5b12f4627f73b14a8262`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3107d914479457d4f68098546010a68c957c8958f8617fe612a4de36890751d`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:f7757ea9df5138c45bdbcd9e258bd5f8d3b847272ba419799988079f669fbe74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 KB (103468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f14b161d58134f0ae5adc6bf8b94c753848d136ed143b505c68fd6d0083ef5e`

```dockerfile
```

-	Layers:
	-	`sha256:977ffaf9dabb1b3eba7edd08c3c73174de9a29484b0f80d86a81072bb317517f`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 84.2 KB (84222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d4314a7e1c917ad745b623d3c1ea185133876babcee74b1048a636196ae0e48`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 19.2 KB (19246 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; ppc64le

```console
$ docker pull memcached@sha256:0b9a2b083716079e6c1da7a9eef4cda25b8d81f3e16840ca6b2b12e9d90e00b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c5555e7ff1014a88296e46cd6d51b379698f7678f76fcd835e8c9f30d647d79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f168e15e72e8585ac6cf20d04f29cfeea15135f34178693fec86adfd88204d`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e2f6d65a966b68fa13bdc24e920a1a1fa7b86b2e000d17eff60efbfdd38993`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 123.0 KB (123004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5864e6eb973cda0b80fc0b600b8fdc61cab246b23ff08158ec77e3c819aacb99`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 992.9 KB (992907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af9bfa929a4b7886285f34b50a2506270b5db318f414db5cfa7c505e069495e`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf6c5b09507827cb18669a5979a2e3e258baa20df3c7d3b1790c8e47c4da755`  
		Last Modified: Mon, 03 Jun 2024 19:53:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:47e12d8b1103b819e814e52b644a34f6fd25e9b3c301cf64bd3a5aed59882a32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 KB (101740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac2cf30c8b57070d3d517da1a03e3bf9241f943b85fa56a7a7cafcec23db720f`

```dockerfile
```

-	Layers:
	-	`sha256:bf26f6e69d9a08fc6932c97112ad23a6a9b487855c46d9d7e0c8bddd8b5292f2`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 82.4 KB (82371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:018afee57a818e12505b2c4851b768103c8b30b0796588e3def21bb1bb3e7d24`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 19.4 KB (19369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; s390x

```console
$ docker pull memcached@sha256:c9d716888f3de4b62fcb97a29f86e58ace3ecd27d3e140bf093a91a55b457895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4551732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98e758f93cfeb8699e726a62495bbcb588c84eb23144c8f4fef5e84556142be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b951b4f532c41c7412daf128075fc9cd89c182acbc79418cb89d9bdcca3f7f5`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ace4ff1604d5e2114f279c4a7dbd9c7255f5c22442459e1dde1e1dba3c3662`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 112.7 KB (112734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3635c0cf5ff89eaa5a72c24ee555909e50ee12d3629572ef94a113391f5b0e92`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 977.3 KB (977292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e93a0ef4a20f636cd8f486379f0e8926c809875d1be02f187e1d9beb0155870`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2e88b16dd19768ead777afafdc9ec27072ab209e2f240c51dce37ce1590302`  
		Last Modified: Mon, 03 Jun 2024 19:44:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:7e094c1f57f2f2a6a9f5e6290afe42f796d0444a80835660c23f0880808b9fac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 KB (101612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22673137bae204447eabe141346d72e57cec6908c114a55f94494e572a484849`

```dockerfile
```

-	Layers:
	-	`sha256:245be0555de7893afdeab5ba2e974bc77e29549c40a4bdb62d8b49cdd98938c8`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 82.3 KB (82313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41c84b152f2dcb64eb163c14efbbe0d430a1cd597e9fe2a74c52c447568f2d9f`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 19.3 KB (19299 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-bookworm`

```console
$ docker pull memcached@sha256:6bc6193233fb86bb8deaf6706445bd3e55b1e786bbea8c642bb42462e0d5fa9b
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
$ docker pull memcached@sha256:9147945260ea3aae4982858f21c236318a3f6e714e3247c5baf29a5a72e0f541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32898057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23286975f91428ab86b108f596c0340aed9fc99015d547119acc7f7aaf10007e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc543897dce5b0ec373146149c07d4d311f530d35fd5660eacf896059d19c1f9`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67696248863aa6bf5473db03626425b13368fab900b2145458a0aadf3ec50685`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 2.5 MB (2488532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1225c54544336958562027d237b24c6e6fdf0242b27fedb8de59463271161a`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 1.3 MB (1257596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c8c669390569241c531942ed6c73e9ed972acd0d553620dc73b27efd017da4`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750d4cc56720b2b3726c433153484ee8befc8ef867db54c4ea893932042208b4`  
		Last Modified: Mon, 03 Jun 2024 19:03:49 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:16ed0d681048581dce561ae4090acbdcf920ce1f2ddce248215521ed4fd9decd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d6ffeaf490e2efb6c46e0c490e1c11020fcf721e84a6b2d8edef168a450b00`

```dockerfile
```

-	Layers:
	-	`sha256:7055f894d5826460bb2eb3ea9b0ef5d51df1ce6b1c073f786f5d1cf92573a368`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 2.3 MB (2261260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1e66ce28cc0bd263cb0b4aa93ffcc60f78c1c750f403cbd3ab265a6794fc167`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 21.0 KB (20979 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:14753c4e01088e08a436d89d02a2a78902028bf49d6db1569f475092fd460bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30237639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c21e319ac699c14e10d279852e999e826acf2731ee4b72c4c10a33bb47692f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 00:48:34 GMT
ADD file:ee9f1914c7fc370bdb089c9e2fcfa15477f7091fc5437cb780232afdf6297586 in / 
# Tue, 14 May 2024 00:48:34 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:169fcae2368e5a601c42972560f091e123648fa0e741975d1b35900c61b9ff71`  
		Last Modified: Tue, 14 May 2024 00:51:36 GMT  
		Size: 26.9 MB (26909921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6135c82883bf5f0df15a6d3d42e97b6013681d12f1f0d535ccb0c1cacf6676b`  
		Last Modified: Mon, 03 Jun 2024 19:08:33 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51f9357aee8294bc0ab883e4493123d2a4dabd21e30ab2900da6cfe6fce5b20`  
		Last Modified: Mon, 03 Jun 2024 19:08:34 GMT  
		Size: 2.1 MB (2089512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32e18a9983de65ed92d9394655a09d3d69089e493a069562641ea42c679e1a4`  
		Last Modified: Mon, 03 Jun 2024 19:08:34 GMT  
		Size: 1.2 MB (1236688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc76114b0bb29114c4b5ff03c2b92a6a317377e26442ec0b79e0016bdc73147d`  
		Last Modified: Mon, 03 Jun 2024 19:08:33 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c636887432e5986c55e92368eef61a43bd3e05cd00609197541f460647ef8208`  
		Last Modified: Mon, 03 Jun 2024 19:08:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:3db3baea327d4e01491ca8527e9a966a8bc9c6fb518a0f2850e7418c158eb8f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84af36590abfbf847e39461d5668a9b85b5846ab2c1705bdf2e8858807e9d86c`

```dockerfile
```

-	Layers:
	-	`sha256:aaab43908073c0eddfc13729d70514a3426255ff8d31aa19aa39108390f5c65d`  
		Last Modified: Mon, 03 Jun 2024 19:08:34 GMT  
		Size: 2.3 MB (2264548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6af6c6fa69438301c0c320846677e25900a5aa269506c074071536e7fdc092ff`  
		Last Modified: Mon, 03 Jun 2024 19:08:33 GMT  
		Size: 21.1 KB (21120 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b953ca66ecee777524a0f33f0adefbe99183367e180f4b2ed82d1e525f57d208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32780663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a9c7e97a66ca554c0cfc88de871b1c7dfad7637ffcbd6a79b5c75b3954bb583`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
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
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994933505bafbbaba95cef494f2dfb3e85f2bfde1ea5c4a6dae5a179e39e7b5c`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9488359f89f8c6691f1737ce76ce6b7520511a8246658953dae9429090e88746`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 2.3 MB (2346183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fa925bb96d2305b22651dc4d10899309c212aef95cb13afbdeb2ba5436cb0b`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 1.3 MB (1253469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5284a06f3ca2503602cf214d936daf8aedee3d442d7aa66a5b67874c8f156685`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a475f5b1bcd9a980f0e2923bf1af87002c6468529583ce41a151599d11b2cc`  
		Last Modified: Tue, 14 May 2024 17:41:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:303a74af5e224338560198dc50e2c9cb2a7b4a46b01d39144559de1dd7788518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e79fb901bf217f30113856b6b39e296324993066435904abd2a2152baae6156`

```dockerfile
```

-	Layers:
	-	`sha256:a35747f1af90484d4a9021de5c31be89cb3117cb5f56f499d3cebe78562716cf`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 2.3 MB (2261490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48c7060af35b31db7e804b3ce19451726c3fb6b956edad221ee58000cf04a91`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 21.0 KB (20997 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:36e236fc6b16e7e3170743b8c6a4fbaa296f4d7804c6c2b2106171eac49c9e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33915077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46c7f4bc09921dd239f3c7eb02f4989d48a1df441f3bc33fa1eac70860b0ae6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 00:47:12 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Tue, 14 May 2024 00:47:12 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb23370f3994993b447e434bb257c1618064ae75acb7e15d1fb88d95c481416`  
		Last Modified: Mon, 03 Jun 2024 19:03:52 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43508bc095d4cad435f08c64c32dd8056399b25cddfeca86964d15f117cbd0c`  
		Last Modified: Mon, 03 Jun 2024 19:03:52 GMT  
		Size: 2.5 MB (2492668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2870f8c3ee5b47d7a6a8e194db84b04de521e6a228093ad33b4252661ee3d0d0`  
		Last Modified: Mon, 03 Jun 2024 19:03:52 GMT  
		Size: 1.3 MB (1258253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c83af100d615d1363ef33866755b85f6153e23f56a4e9c1a6cba13d0463082d`  
		Last Modified: Mon, 03 Jun 2024 19:03:53 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ec3bf8bf691991f57de6b00811ed6d06fe0417f1955d1d7b6cd33ecf81b406`  
		Last Modified: Mon, 03 Jun 2024 19:03:53 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:443d7accdadab953db276145a1ab012f3232c120ea362461be5a22531600dca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da086c82559c925e7fcc2b0c79e47076545d92a837f0e4d1b8f49b66cfb55fc0`

```dockerfile
```

-	Layers:
	-	`sha256:829f8d9a7d33b902a3c59de1e19bd0291df3704cf233de30580da78a72c5220f`  
		Last Modified: Mon, 03 Jun 2024 19:03:52 GMT  
		Size: 2.3 MB (2258358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffb9dd39ce17614aed4cd4f0bac42e7b8bb49b726b85d39d48b1700119a54cf0`  
		Last Modified: Mon, 03 Jun 2024 19:03:52 GMT  
		Size: 20.9 KB (20924 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:129ad612a59e558c3da7dfa1a1958d7b374599149ad2ac085bfd539341b0e76d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32335816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4ee8bdf9b447076bff1edf5bfe8aafd428b9e3a1c11745e3eac190a7957b50d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 01:11:07 GMT
ADD file:a92da94a28279478b2eae11dcdcd2913fc06af02498a5515cc3f288668d74e43 in / 
# Tue, 14 May 2024 01:11:12 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6ccc6628d3cdcda935b3b60cb54fa578d669965454d9cf39de3df9c1276132b7`  
		Last Modified: Tue, 14 May 2024 01:22:19 GMT  
		Size: 29.1 MB (29143688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2c2342dfc8d9203635e3e3bc46109d12ef7ef9940adb0794934bca415e4d79`  
		Last Modified: Mon, 03 Jun 2024 19:52:36 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba60c707dc72485dffcb0f586703d60083e3a99568905fc77c61a927aa023133`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 1.9 MB (1937709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5d0dde6405cfccdcc1ece97791b0c134d743d3dbbb4648cfd8ffa51f7fa7fa`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 1.3 MB (1252902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c5806cc8f133288ec076e5d9a6d04f2f7528380144d22892c7b84314c99a8c`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198d6a5f4cd3ba446c2120eb2826773388a541360046c35203d6024dce60a143`  
		Last Modified: Mon, 03 Jun 2024 19:52:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:bf5993b43a4118f01f52ac8a194cb102c52ee5b81fe6f6217d77ca4afaef2a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295c96051f2df83e45a2fe340023dd1e664fdec31e7ef871ca8d797cbc594205`

```dockerfile
```

-	Layers:
	-	`sha256:396ed31b018a1dc19cc7f9fcd8bc9c31f7d68c64735199594c25d0801926c1b7`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:63978abc93d511e5c74a4cc84e7b57a1d767833ba0c69e02c29365668c96bf86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37163958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9054e0ed4fdeb443fcae69bad304d1e19e2434684bbca08c83f5ef5897d1e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 01:20:02 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Tue, 14 May 2024 01:20:04 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:11ee2a6dbc4a6a6b182097f6023f775e595488a6bcc424e9b58001659deb7fa1`  
		Last Modified: Tue, 14 May 2024 01:24:06 GMT  
		Size: 33.1 MB (33141160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d531128e0fac13a6c4e8656afa2e85afbd55db7a786a38bf715c14f4e05a5d94`  
		Last Modified: Mon, 03 Jun 2024 19:50:52 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037940292acc903c706efafe81e090f3eca4683a90304378efe5f4b2cd3cbd47`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 2.7 MB (2698394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d2e0144b8349ea33bdc906d060868aa61958e0c45ac421dcf26a5fc15eb677`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 1.3 MB (1322885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02930e85eb728b1b92f67233fa0c4ff46787e43e4c5f78933df1a64f4c1f7ad0`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cb49628af48f1c1c75566128625afdacca39df7ea0a7c2762ff858d5a3c3e9`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:eae1092d4dd48c0f18e3eda2c5440fe8988dc3823060e738b93a20fba09baf54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea636723fe65c22cb491ee51203b6349d5302ba3288e8ebf7395457c83a78a3`

```dockerfile
```

-	Layers:
	-	`sha256:0c88ae099fbb77c9cefb907169eb358536ff37e4c35140a81c2cb67411da7a9f`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 2.3 MB (2265631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba09bde198a5df307f36fa75f66fe410b324cf250153ce67c8d2f7e9def7d0e5`  
		Last Modified: Mon, 03 Jun 2024 19:50:52 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:da94175eec280d37f0dfd2d8acdc57bd8b4607f66f738dd796b0719c28737986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30903401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf7fe752edb4161d9cd43825ddd58ceff332eb34c41dcc9623255e4cc9bf376`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 00:42:38 GMT
ADD file:55fef93bbad6701fe968a070a0c72b3a0bd3df408dd79c9a616a43dea0de11d0 in / 
# Tue, 14 May 2024 00:42:40 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d7365433874e83ccc92aa5d768989641a64e23c3247409161401a09b4895c406`  
		Last Modified: Tue, 14 May 2024 00:47:35 GMT  
		Size: 27.5 MB (27512398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422d2a0f87a8b8c2712bf0d473e4f936bcbad2af462760d8ae88a25a4ddcbabe`  
		Last Modified: Mon, 03 Jun 2024 19:40:44 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dac9575eb2b0b2d47b6c792dddf0edd2afdeaad0f5dc8a1572996977ceb0fa6`  
		Last Modified: Mon, 03 Jun 2024 19:40:44 GMT  
		Size: 2.2 MB (2152694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e3eb594a178112f9ea3d30d498b8b619b5165ff992e96e66a2cb723b708eea`  
		Last Modified: Mon, 03 Jun 2024 19:40:44 GMT  
		Size: 1.2 MB (1236790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f6ebc8f32f01f7f87e92d446e389a62516dcde1dd8b66b0ed80618c1279d7f`  
		Last Modified: Mon, 03 Jun 2024 19:40:45 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b1370c7b0f96a4cb325b9cd27e7cc508def3a755eaf10f7f2893a6d721d6b6`  
		Last Modified: Mon, 03 Jun 2024 19:40:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:b7e29c218845ad20177e6072bafe8ceb34957f028c9ab5dc784bf0d8abb3266b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:801c05520a31b4c181fcea7491e35a45441ce8b7d97f9f1133ce0da9982b9f65`

```dockerfile
```

-	Layers:
	-	`sha256:7059681ccb9077ae5d5d066a76afbdf315e577e6f6185513b43dc17567fd6a41`  
		Last Modified: Mon, 03 Jun 2024 19:40:44 GMT  
		Size: 2.3 MB (2261081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d33b5d8c8737f3f638401087329e3541977c1b45f846a92a33f44bc802633636`  
		Last Modified: Mon, 03 Jun 2024 19:40:44 GMT  
		Size: 21.0 KB (20979 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6`

```console
$ docker pull memcached@sha256:6bc6193233fb86bb8deaf6706445bd3e55b1e786bbea8c642bb42462e0d5fa9b
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
$ docker pull memcached@sha256:9147945260ea3aae4982858f21c236318a3f6e714e3247c5baf29a5a72e0f541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32898057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23286975f91428ab86b108f596c0340aed9fc99015d547119acc7f7aaf10007e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc543897dce5b0ec373146149c07d4d311f530d35fd5660eacf896059d19c1f9`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67696248863aa6bf5473db03626425b13368fab900b2145458a0aadf3ec50685`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 2.5 MB (2488532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1225c54544336958562027d237b24c6e6fdf0242b27fedb8de59463271161a`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 1.3 MB (1257596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c8c669390569241c531942ed6c73e9ed972acd0d553620dc73b27efd017da4`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750d4cc56720b2b3726c433153484ee8befc8ef867db54c4ea893932042208b4`  
		Last Modified: Mon, 03 Jun 2024 19:03:49 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:16ed0d681048581dce561ae4090acbdcf920ce1f2ddce248215521ed4fd9decd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d6ffeaf490e2efb6c46e0c490e1c11020fcf721e84a6b2d8edef168a450b00`

```dockerfile
```

-	Layers:
	-	`sha256:7055f894d5826460bb2eb3ea9b0ef5d51df1ce6b1c073f786f5d1cf92573a368`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 2.3 MB (2261260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1e66ce28cc0bd263cb0b4aa93ffcc60f78c1c750f403cbd3ab265a6794fc167`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 21.0 KB (20979 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:14753c4e01088e08a436d89d02a2a78902028bf49d6db1569f475092fd460bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30237639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c21e319ac699c14e10d279852e999e826acf2731ee4b72c4c10a33bb47692f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 00:48:34 GMT
ADD file:ee9f1914c7fc370bdb089c9e2fcfa15477f7091fc5437cb780232afdf6297586 in / 
# Tue, 14 May 2024 00:48:34 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:169fcae2368e5a601c42972560f091e123648fa0e741975d1b35900c61b9ff71`  
		Last Modified: Tue, 14 May 2024 00:51:36 GMT  
		Size: 26.9 MB (26909921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6135c82883bf5f0df15a6d3d42e97b6013681d12f1f0d535ccb0c1cacf6676b`  
		Last Modified: Mon, 03 Jun 2024 19:08:33 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51f9357aee8294bc0ab883e4493123d2a4dabd21e30ab2900da6cfe6fce5b20`  
		Last Modified: Mon, 03 Jun 2024 19:08:34 GMT  
		Size: 2.1 MB (2089512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32e18a9983de65ed92d9394655a09d3d69089e493a069562641ea42c679e1a4`  
		Last Modified: Mon, 03 Jun 2024 19:08:34 GMT  
		Size: 1.2 MB (1236688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc76114b0bb29114c4b5ff03c2b92a6a317377e26442ec0b79e0016bdc73147d`  
		Last Modified: Mon, 03 Jun 2024 19:08:33 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c636887432e5986c55e92368eef61a43bd3e05cd00609197541f460647ef8208`  
		Last Modified: Mon, 03 Jun 2024 19:08:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:3db3baea327d4e01491ca8527e9a966a8bc9c6fb518a0f2850e7418c158eb8f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84af36590abfbf847e39461d5668a9b85b5846ab2c1705bdf2e8858807e9d86c`

```dockerfile
```

-	Layers:
	-	`sha256:aaab43908073c0eddfc13729d70514a3426255ff8d31aa19aa39108390f5c65d`  
		Last Modified: Mon, 03 Jun 2024 19:08:34 GMT  
		Size: 2.3 MB (2264548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6af6c6fa69438301c0c320846677e25900a5aa269506c074071536e7fdc092ff`  
		Last Modified: Mon, 03 Jun 2024 19:08:33 GMT  
		Size: 21.1 KB (21120 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b953ca66ecee777524a0f33f0adefbe99183367e180f4b2ed82d1e525f57d208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32780663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a9c7e97a66ca554c0cfc88de871b1c7dfad7637ffcbd6a79b5c75b3954bb583`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
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
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994933505bafbbaba95cef494f2dfb3e85f2bfde1ea5c4a6dae5a179e39e7b5c`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9488359f89f8c6691f1737ce76ce6b7520511a8246658953dae9429090e88746`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 2.3 MB (2346183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fa925bb96d2305b22651dc4d10899309c212aef95cb13afbdeb2ba5436cb0b`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 1.3 MB (1253469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5284a06f3ca2503602cf214d936daf8aedee3d442d7aa66a5b67874c8f156685`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a475f5b1bcd9a980f0e2923bf1af87002c6468529583ce41a151599d11b2cc`  
		Last Modified: Tue, 14 May 2024 17:41:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:303a74af5e224338560198dc50e2c9cb2a7b4a46b01d39144559de1dd7788518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e79fb901bf217f30113856b6b39e296324993066435904abd2a2152baae6156`

```dockerfile
```

-	Layers:
	-	`sha256:a35747f1af90484d4a9021de5c31be89cb3117cb5f56f499d3cebe78562716cf`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 2.3 MB (2261490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48c7060af35b31db7e804b3ce19451726c3fb6b956edad221ee58000cf04a91`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 21.0 KB (20997 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; 386

```console
$ docker pull memcached@sha256:36e236fc6b16e7e3170743b8c6a4fbaa296f4d7804c6c2b2106171eac49c9e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33915077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46c7f4bc09921dd239f3c7eb02f4989d48a1df441f3bc33fa1eac70860b0ae6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 00:47:12 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Tue, 14 May 2024 00:47:12 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb23370f3994993b447e434bb257c1618064ae75acb7e15d1fb88d95c481416`  
		Last Modified: Mon, 03 Jun 2024 19:03:52 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43508bc095d4cad435f08c64c32dd8056399b25cddfeca86964d15f117cbd0c`  
		Last Modified: Mon, 03 Jun 2024 19:03:52 GMT  
		Size: 2.5 MB (2492668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2870f8c3ee5b47d7a6a8e194db84b04de521e6a228093ad33b4252661ee3d0d0`  
		Last Modified: Mon, 03 Jun 2024 19:03:52 GMT  
		Size: 1.3 MB (1258253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c83af100d615d1363ef33866755b85f6153e23f56a4e9c1a6cba13d0463082d`  
		Last Modified: Mon, 03 Jun 2024 19:03:53 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ec3bf8bf691991f57de6b00811ed6d06fe0417f1955d1d7b6cd33ecf81b406`  
		Last Modified: Mon, 03 Jun 2024 19:03:53 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:443d7accdadab953db276145a1ab012f3232c120ea362461be5a22531600dca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da086c82559c925e7fcc2b0c79e47076545d92a837f0e4d1b8f49b66cfb55fc0`

```dockerfile
```

-	Layers:
	-	`sha256:829f8d9a7d33b902a3c59de1e19bd0291df3704cf233de30580da78a72c5220f`  
		Last Modified: Mon, 03 Jun 2024 19:03:52 GMT  
		Size: 2.3 MB (2258358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffb9dd39ce17614aed4cd4f0bac42e7b8bb49b726b85d39d48b1700119a54cf0`  
		Last Modified: Mon, 03 Jun 2024 19:03:52 GMT  
		Size: 20.9 KB (20924 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; mips64le

```console
$ docker pull memcached@sha256:129ad612a59e558c3da7dfa1a1958d7b374599149ad2ac085bfd539341b0e76d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32335816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4ee8bdf9b447076bff1edf5bfe8aafd428b9e3a1c11745e3eac190a7957b50d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 01:11:07 GMT
ADD file:a92da94a28279478b2eae11dcdcd2913fc06af02498a5515cc3f288668d74e43 in / 
# Tue, 14 May 2024 01:11:12 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6ccc6628d3cdcda935b3b60cb54fa578d669965454d9cf39de3df9c1276132b7`  
		Last Modified: Tue, 14 May 2024 01:22:19 GMT  
		Size: 29.1 MB (29143688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2c2342dfc8d9203635e3e3bc46109d12ef7ef9940adb0794934bca415e4d79`  
		Last Modified: Mon, 03 Jun 2024 19:52:36 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba60c707dc72485dffcb0f586703d60083e3a99568905fc77c61a927aa023133`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 1.9 MB (1937709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5d0dde6405cfccdcc1ece97791b0c134d743d3dbbb4648cfd8ffa51f7fa7fa`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 1.3 MB (1252902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c5806cc8f133288ec076e5d9a6d04f2f7528380144d22892c7b84314c99a8c`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198d6a5f4cd3ba446c2120eb2826773388a541360046c35203d6024dce60a143`  
		Last Modified: Mon, 03 Jun 2024 19:52:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:bf5993b43a4118f01f52ac8a194cb102c52ee5b81fe6f6217d77ca4afaef2a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295c96051f2df83e45a2fe340023dd1e664fdec31e7ef871ca8d797cbc594205`

```dockerfile
```

-	Layers:
	-	`sha256:396ed31b018a1dc19cc7f9fcd8bc9c31f7d68c64735199594c25d0801926c1b7`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:63978abc93d511e5c74a4cc84e7b57a1d767833ba0c69e02c29365668c96bf86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37163958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9054e0ed4fdeb443fcae69bad304d1e19e2434684bbca08c83f5ef5897d1e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 01:20:02 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Tue, 14 May 2024 01:20:04 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:11ee2a6dbc4a6a6b182097f6023f775e595488a6bcc424e9b58001659deb7fa1`  
		Last Modified: Tue, 14 May 2024 01:24:06 GMT  
		Size: 33.1 MB (33141160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d531128e0fac13a6c4e8656afa2e85afbd55db7a786a38bf715c14f4e05a5d94`  
		Last Modified: Mon, 03 Jun 2024 19:50:52 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037940292acc903c706efafe81e090f3eca4683a90304378efe5f4b2cd3cbd47`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 2.7 MB (2698394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d2e0144b8349ea33bdc906d060868aa61958e0c45ac421dcf26a5fc15eb677`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 1.3 MB (1322885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02930e85eb728b1b92f67233fa0c4ff46787e43e4c5f78933df1a64f4c1f7ad0`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cb49628af48f1c1c75566128625afdacca39df7ea0a7c2762ff858d5a3c3e9`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:eae1092d4dd48c0f18e3eda2c5440fe8988dc3823060e738b93a20fba09baf54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea636723fe65c22cb491ee51203b6349d5302ba3288e8ebf7395457c83a78a3`

```dockerfile
```

-	Layers:
	-	`sha256:0c88ae099fbb77c9cefb907169eb358536ff37e4c35140a81c2cb67411da7a9f`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 2.3 MB (2265631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba09bde198a5df307f36fa75f66fe410b324cf250153ce67c8d2f7e9def7d0e5`  
		Last Modified: Mon, 03 Jun 2024 19:50:52 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; s390x

```console
$ docker pull memcached@sha256:da94175eec280d37f0dfd2d8acdc57bd8b4607f66f738dd796b0719c28737986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30903401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf7fe752edb4161d9cd43825ddd58ceff332eb34c41dcc9623255e4cc9bf376`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 00:42:38 GMT
ADD file:55fef93bbad6701fe968a070a0c72b3a0bd3df408dd79c9a616a43dea0de11d0 in / 
# Tue, 14 May 2024 00:42:40 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d7365433874e83ccc92aa5d768989641a64e23c3247409161401a09b4895c406`  
		Last Modified: Tue, 14 May 2024 00:47:35 GMT  
		Size: 27.5 MB (27512398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422d2a0f87a8b8c2712bf0d473e4f936bcbad2af462760d8ae88a25a4ddcbabe`  
		Last Modified: Mon, 03 Jun 2024 19:40:44 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dac9575eb2b0b2d47b6c792dddf0edd2afdeaad0f5dc8a1572996977ceb0fa6`  
		Last Modified: Mon, 03 Jun 2024 19:40:44 GMT  
		Size: 2.2 MB (2152694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e3eb594a178112f9ea3d30d498b8b619b5165ff992e96e66a2cb723b708eea`  
		Last Modified: Mon, 03 Jun 2024 19:40:44 GMT  
		Size: 1.2 MB (1236790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f6ebc8f32f01f7f87e92d446e389a62516dcde1dd8b66b0ed80618c1279d7f`  
		Last Modified: Mon, 03 Jun 2024 19:40:45 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b1370c7b0f96a4cb325b9cd27e7cc508def3a755eaf10f7f2893a6d721d6b6`  
		Last Modified: Mon, 03 Jun 2024 19:40:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:b7e29c218845ad20177e6072bafe8ceb34957f028c9ab5dc784bf0d8abb3266b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:801c05520a31b4c181fcea7491e35a45441ce8b7d97f9f1133ce0da9982b9f65`

```dockerfile
```

-	Layers:
	-	`sha256:7059681ccb9077ae5d5d066a76afbdf315e577e6f6185513b43dc17567fd6a41`  
		Last Modified: Mon, 03 Jun 2024 19:40:44 GMT  
		Size: 2.3 MB (2261081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d33b5d8c8737f3f638401087329e3541977c1b45f846a92a33f44bc802633636`  
		Last Modified: Mon, 03 Jun 2024 19:40:44 GMT  
		Size: 21.0 KB (20979 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine`

```console
$ docker pull memcached@sha256:dcdfc647eaab83cce1e15874888f7e28bdae4b1b947f637e45fec64db1d1a3e3
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
$ docker pull memcached@sha256:7e7f1b92cbd46c4b5f60777f034debc77c1b66bd5b66b732e424d47bc9fbeed0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4681905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae47e754356b145ac3883025be70df81397e012b7b9deea79c6e1549cebb820`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723fe97584e549852ab448538bb35f45d46da4b09c52e18fa4eeec5352c47a42`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5f2dacb5179622644f1e47531960f1fa5aef816fb60aad38a20349103c7191`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 103.8 KB (103828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef494bb92067167934aab739f7d1f023f4e34ef112f973afc201b98e54fa5d50`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 954.6 KB (954617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd803b6c0eb021a0b33649dd96256f867eac7aa91b9255624ed7f239c9475ff`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1c222c9d9e5ee0e2e34c4386e9c09b7ebf79a12072e245332f295c63bddf3e`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2dd815e2d1643bcba94e92c59e4c260f02bf06b0ff954840272439de861358f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 KB (103568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0885c1305da890646b6ad6dbcd2ae57932bcd2d1b804dc7404de2cd8713cc284`

```dockerfile
```

-	Layers:
	-	`sha256:6e6853da7f25eec4b641df434dccd72f8d65a0a540787c715049bd366d0f787b`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 84.3 KB (84267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b7bd473fc9187722cabb9a96acad9c5a1dbb88c26431928b2166223fb0dee7c`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 19.3 KB (19301 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:e0688d9873a4cf749f89b43548d03f7d6c873596b1495b6da6943d4a3e767df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5166898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6a1a46a5867d6ecd3c9bf99a695a89cc1f746f59d3a9a140b85a42b99a2e26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_VERSION=1.6.27
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 22 May 2024 18:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:54:12 GMT
USER memcache
# Wed, 22 May 2024 18:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 May 2024 18:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024a9ccd1af8ffcfe453e22adead9362703e916c9dec4f1d4e94b597e660f23e`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab592fa6ce63bf6772b1c208275d773ef6e671af73b2bd119e98de86dce4fc1`  
		Last Modified: Thu, 23 May 2024 06:29:58 GMT  
		Size: 121.0 KB (121017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd20d288c43aabf4d5e06a885b2e2f24583aae8e102eca2bf9257ce5e307a2cd`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 957.7 KB (957743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d039a0fcb8c2c4f062cb3fb5c2b20ae16915479721254aadfc68d0319c84ee25`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cf5bc5246a4e40149d2a6b161c9fbce8354373e305c03088715546070c2742`  
		Last Modified: Thu, 23 May 2024 06:29:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ec1932014529a81f308cae2db47073ddf344ef48cbc77766d95510cb7385b2af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 KB (103606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0d85c8cad5520d9245c1563457fcf55da9b744f736c305ad21fad10027e013`

```dockerfile
```

-	Layers:
	-	`sha256:f77bdac9710cd22ef4eb7ba293b1b4fe4736e109a3767950432991fe0237fa54`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 84.3 KB (84287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12016cd6764c2821a23d0e8fb3c182eda4d12d096e83cf52f57eb0103616d5e8`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 19.3 KB (19319 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:d021aa4701a1cbf3afb535aa82cd88bc0f7c5d51c05c34d5160fabd876a5bce7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d85661f9f9c582ffadd4540ae1b2fb7bf653da454d36eab21d69ed0aa33ddb7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:05:50 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 18:05:51 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77c9b09b82af8bb67811ab3d796c64874348624abc7cf7658894f3042e3fdda`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61451eaaecf42ca95101dad4ed37d00cf792b8afae1d5eeab46e43e258b3ef4`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 109.0 KB (108954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1cfe9a7dc0eb6422fdd3e24036097ac92ebb3781776994ac1a1985641b7746a`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 947.9 KB (947940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffa1b620c706dc7fccfe69ac07a840b285472eebf3a5b12f4627f73b14a8262`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3107d914479457d4f68098546010a68c957c8958f8617fe612a4de36890751d`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:f7757ea9df5138c45bdbcd9e258bd5f8d3b847272ba419799988079f669fbe74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 KB (103468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f14b161d58134f0ae5adc6bf8b94c753848d136ed143b505c68fd6d0083ef5e`

```dockerfile
```

-	Layers:
	-	`sha256:977ffaf9dabb1b3eba7edd08c3c73174de9a29484b0f80d86a81072bb317517f`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 84.2 KB (84222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d4314a7e1c917ad745b623d3c1ea185133876babcee74b1048a636196ae0e48`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 19.2 KB (19246 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:0b9a2b083716079e6c1da7a9eef4cda25b8d81f3e16840ca6b2b12e9d90e00b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c5555e7ff1014a88296e46cd6d51b379698f7678f76fcd835e8c9f30d647d79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f168e15e72e8585ac6cf20d04f29cfeea15135f34178693fec86adfd88204d`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e2f6d65a966b68fa13bdc24e920a1a1fa7b86b2e000d17eff60efbfdd38993`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 123.0 KB (123004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5864e6eb973cda0b80fc0b600b8fdc61cab246b23ff08158ec77e3c819aacb99`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 992.9 KB (992907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af9bfa929a4b7886285f34b50a2506270b5db318f414db5cfa7c505e069495e`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf6c5b09507827cb18669a5979a2e3e258baa20df3c7d3b1790c8e47c4da755`  
		Last Modified: Mon, 03 Jun 2024 19:53:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:47e12d8b1103b819e814e52b644a34f6fd25e9b3c301cf64bd3a5aed59882a32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 KB (101740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac2cf30c8b57070d3d517da1a03e3bf9241f943b85fa56a7a7cafcec23db720f`

```dockerfile
```

-	Layers:
	-	`sha256:bf26f6e69d9a08fc6932c97112ad23a6a9b487855c46d9d7e0c8bddd8b5292f2`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 82.4 KB (82371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:018afee57a818e12505b2c4851b768103c8b30b0796588e3def21bb1bb3e7d24`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 19.4 KB (19369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:c9d716888f3de4b62fcb97a29f86e58ace3ecd27d3e140bf093a91a55b457895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4551732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98e758f93cfeb8699e726a62495bbcb588c84eb23144c8f4fef5e84556142be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b951b4f532c41c7412daf128075fc9cd89c182acbc79418cb89d9bdcca3f7f5`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ace4ff1604d5e2114f279c4a7dbd9c7255f5c22442459e1dde1e1dba3c3662`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 112.7 KB (112734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3635c0cf5ff89eaa5a72c24ee555909e50ee12d3629572ef94a113391f5b0e92`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 977.3 KB (977292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e93a0ef4a20f636cd8f486379f0e8926c809875d1be02f187e1d9beb0155870`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2e88b16dd19768ead777afafdc9ec27072ab209e2f240c51dce37ce1590302`  
		Last Modified: Mon, 03 Jun 2024 19:44:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7e094c1f57f2f2a6a9f5e6290afe42f796d0444a80835660c23f0880808b9fac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 KB (101612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22673137bae204447eabe141346d72e57cec6908c114a55f94494e572a484849`

```dockerfile
```

-	Layers:
	-	`sha256:245be0555de7893afdeab5ba2e974bc77e29549c40a4bdb62d8b49cdd98938c8`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 82.3 KB (82313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41c84b152f2dcb64eb163c14efbbe0d430a1cd597e9fe2a74c52c447568f2d9f`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 19.3 KB (19299 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine3.20`

```console
$ docker pull memcached@sha256:dcdfc647eaab83cce1e15874888f7e28bdae4b1b947f637e45fec64db1d1a3e3
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

### `memcached:1.6-alpine3.20` - linux; amd64

```console
$ docker pull memcached@sha256:7e7f1b92cbd46c4b5f60777f034debc77c1b66bd5b66b732e424d47bc9fbeed0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4681905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae47e754356b145ac3883025be70df81397e012b7b9deea79c6e1549cebb820`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723fe97584e549852ab448538bb35f45d46da4b09c52e18fa4eeec5352c47a42`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5f2dacb5179622644f1e47531960f1fa5aef816fb60aad38a20349103c7191`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 103.8 KB (103828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef494bb92067167934aab739f7d1f023f4e34ef112f973afc201b98e54fa5d50`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 954.6 KB (954617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd803b6c0eb021a0b33649dd96256f867eac7aa91b9255624ed7f239c9475ff`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1c222c9d9e5ee0e2e34c4386e9c09b7ebf79a12072e245332f295c63bddf3e`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:2dd815e2d1643bcba94e92c59e4c260f02bf06b0ff954840272439de861358f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 KB (103568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0885c1305da890646b6ad6dbcd2ae57932bcd2d1b804dc7404de2cd8713cc284`

```dockerfile
```

-	Layers:
	-	`sha256:6e6853da7f25eec4b641df434dccd72f8d65a0a540787c715049bd366d0f787b`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 84.3 KB (84267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b7bd473fc9187722cabb9a96acad9c5a1dbb88c26431928b2166223fb0dee7c`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 19.3 KB (19301 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:e0688d9873a4cf749f89b43548d03f7d6c873596b1495b6da6943d4a3e767df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5166898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6a1a46a5867d6ecd3c9bf99a695a89cc1f746f59d3a9a140b85a42b99a2e26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_VERSION=1.6.27
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 22 May 2024 18:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:54:12 GMT
USER memcache
# Wed, 22 May 2024 18:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 May 2024 18:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024a9ccd1af8ffcfe453e22adead9362703e916c9dec4f1d4e94b597e660f23e`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab592fa6ce63bf6772b1c208275d773ef6e671af73b2bd119e98de86dce4fc1`  
		Last Modified: Thu, 23 May 2024 06:29:58 GMT  
		Size: 121.0 KB (121017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd20d288c43aabf4d5e06a885b2e2f24583aae8e102eca2bf9257ce5e307a2cd`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 957.7 KB (957743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d039a0fcb8c2c4f062cb3fb5c2b20ae16915479721254aadfc68d0319c84ee25`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cf5bc5246a4e40149d2a6b161c9fbce8354373e305c03088715546070c2742`  
		Last Modified: Thu, 23 May 2024 06:29:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:ec1932014529a81f308cae2db47073ddf344ef48cbc77766d95510cb7385b2af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 KB (103606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0d85c8cad5520d9245c1563457fcf55da9b744f736c305ad21fad10027e013`

```dockerfile
```

-	Layers:
	-	`sha256:f77bdac9710cd22ef4eb7ba293b1b4fe4736e109a3767950432991fe0237fa54`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 84.3 KB (84287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12016cd6764c2821a23d0e8fb3c182eda4d12d096e83cf52f57eb0103616d5e8`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 19.3 KB (19319 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.20` - linux; 386

```console
$ docker pull memcached@sha256:d021aa4701a1cbf3afb535aa82cd88bc0f7c5d51c05c34d5160fabd876a5bce7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d85661f9f9c582ffadd4540ae1b2fb7bf653da454d36eab21d69ed0aa33ddb7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:05:50 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 18:05:51 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77c9b09b82af8bb67811ab3d796c64874348624abc7cf7658894f3042e3fdda`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61451eaaecf42ca95101dad4ed37d00cf792b8afae1d5eeab46e43e258b3ef4`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 109.0 KB (108954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1cfe9a7dc0eb6422fdd3e24036097ac92ebb3781776994ac1a1985641b7746a`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 947.9 KB (947940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffa1b620c706dc7fccfe69ac07a840b285472eebf3a5b12f4627f73b14a8262`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3107d914479457d4f68098546010a68c957c8958f8617fe612a4de36890751d`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:f7757ea9df5138c45bdbcd9e258bd5f8d3b847272ba419799988079f669fbe74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 KB (103468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f14b161d58134f0ae5adc6bf8b94c753848d136ed143b505c68fd6d0083ef5e`

```dockerfile
```

-	Layers:
	-	`sha256:977ffaf9dabb1b3eba7edd08c3c73174de9a29484b0f80d86a81072bb317517f`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 84.2 KB (84222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d4314a7e1c917ad745b623d3c1ea185133876babcee74b1048a636196ae0e48`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 19.2 KB (19246 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.20` - linux; ppc64le

```console
$ docker pull memcached@sha256:0b9a2b083716079e6c1da7a9eef4cda25b8d81f3e16840ca6b2b12e9d90e00b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c5555e7ff1014a88296e46cd6d51b379698f7678f76fcd835e8c9f30d647d79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f168e15e72e8585ac6cf20d04f29cfeea15135f34178693fec86adfd88204d`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e2f6d65a966b68fa13bdc24e920a1a1fa7b86b2e000d17eff60efbfdd38993`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 123.0 KB (123004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5864e6eb973cda0b80fc0b600b8fdc61cab246b23ff08158ec77e3c819aacb99`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 992.9 KB (992907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af9bfa929a4b7886285f34b50a2506270b5db318f414db5cfa7c505e069495e`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf6c5b09507827cb18669a5979a2e3e258baa20df3c7d3b1790c8e47c4da755`  
		Last Modified: Mon, 03 Jun 2024 19:53:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:47e12d8b1103b819e814e52b644a34f6fd25e9b3c301cf64bd3a5aed59882a32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 KB (101740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac2cf30c8b57070d3d517da1a03e3bf9241f943b85fa56a7a7cafcec23db720f`

```dockerfile
```

-	Layers:
	-	`sha256:bf26f6e69d9a08fc6932c97112ad23a6a9b487855c46d9d7e0c8bddd8b5292f2`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 82.4 KB (82371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:018afee57a818e12505b2c4851b768103c8b30b0796588e3def21bb1bb3e7d24`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 19.4 KB (19369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.20` - linux; s390x

```console
$ docker pull memcached@sha256:c9d716888f3de4b62fcb97a29f86e58ace3ecd27d3e140bf093a91a55b457895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4551732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98e758f93cfeb8699e726a62495bbcb588c84eb23144c8f4fef5e84556142be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b951b4f532c41c7412daf128075fc9cd89c182acbc79418cb89d9bdcca3f7f5`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ace4ff1604d5e2114f279c4a7dbd9c7255f5c22442459e1dde1e1dba3c3662`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 112.7 KB (112734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3635c0cf5ff89eaa5a72c24ee555909e50ee12d3629572ef94a113391f5b0e92`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 977.3 KB (977292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e93a0ef4a20f636cd8f486379f0e8926c809875d1be02f187e1d9beb0155870`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2e88b16dd19768ead777afafdc9ec27072ab209e2f240c51dce37ce1590302`  
		Last Modified: Mon, 03 Jun 2024 19:44:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:7e094c1f57f2f2a6a9f5e6290afe42f796d0444a80835660c23f0880808b9fac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 KB (101612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22673137bae204447eabe141346d72e57cec6908c114a55f94494e572a484849`

```dockerfile
```

-	Layers:
	-	`sha256:245be0555de7893afdeab5ba2e974bc77e29549c40a4bdb62d8b49cdd98938c8`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 82.3 KB (82313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41c84b152f2dcb64eb163c14efbbe0d430a1cd597e9fe2a74c52c447568f2d9f`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 19.3 KB (19299 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-bookworm`

```console
$ docker pull memcached@sha256:6bc6193233fb86bb8deaf6706445bd3e55b1e786bbea8c642bb42462e0d5fa9b
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
$ docker pull memcached@sha256:9147945260ea3aae4982858f21c236318a3f6e714e3247c5baf29a5a72e0f541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32898057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23286975f91428ab86b108f596c0340aed9fc99015d547119acc7f7aaf10007e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc543897dce5b0ec373146149c07d4d311f530d35fd5660eacf896059d19c1f9`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67696248863aa6bf5473db03626425b13368fab900b2145458a0aadf3ec50685`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 2.5 MB (2488532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1225c54544336958562027d237b24c6e6fdf0242b27fedb8de59463271161a`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 1.3 MB (1257596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c8c669390569241c531942ed6c73e9ed972acd0d553620dc73b27efd017da4`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750d4cc56720b2b3726c433153484ee8befc8ef867db54c4ea893932042208b4`  
		Last Modified: Mon, 03 Jun 2024 19:03:49 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:16ed0d681048581dce561ae4090acbdcf920ce1f2ddce248215521ed4fd9decd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d6ffeaf490e2efb6c46e0c490e1c11020fcf721e84a6b2d8edef168a450b00`

```dockerfile
```

-	Layers:
	-	`sha256:7055f894d5826460bb2eb3ea9b0ef5d51df1ce6b1c073f786f5d1cf92573a368`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 2.3 MB (2261260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1e66ce28cc0bd263cb0b4aa93ffcc60f78c1c750f403cbd3ab265a6794fc167`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 21.0 KB (20979 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:14753c4e01088e08a436d89d02a2a78902028bf49d6db1569f475092fd460bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30237639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c21e319ac699c14e10d279852e999e826acf2731ee4b72c4c10a33bb47692f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 00:48:34 GMT
ADD file:ee9f1914c7fc370bdb089c9e2fcfa15477f7091fc5437cb780232afdf6297586 in / 
# Tue, 14 May 2024 00:48:34 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:169fcae2368e5a601c42972560f091e123648fa0e741975d1b35900c61b9ff71`  
		Last Modified: Tue, 14 May 2024 00:51:36 GMT  
		Size: 26.9 MB (26909921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6135c82883bf5f0df15a6d3d42e97b6013681d12f1f0d535ccb0c1cacf6676b`  
		Last Modified: Mon, 03 Jun 2024 19:08:33 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51f9357aee8294bc0ab883e4493123d2a4dabd21e30ab2900da6cfe6fce5b20`  
		Last Modified: Mon, 03 Jun 2024 19:08:34 GMT  
		Size: 2.1 MB (2089512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32e18a9983de65ed92d9394655a09d3d69089e493a069562641ea42c679e1a4`  
		Last Modified: Mon, 03 Jun 2024 19:08:34 GMT  
		Size: 1.2 MB (1236688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc76114b0bb29114c4b5ff03c2b92a6a317377e26442ec0b79e0016bdc73147d`  
		Last Modified: Mon, 03 Jun 2024 19:08:33 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c636887432e5986c55e92368eef61a43bd3e05cd00609197541f460647ef8208`  
		Last Modified: Mon, 03 Jun 2024 19:08:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:3db3baea327d4e01491ca8527e9a966a8bc9c6fb518a0f2850e7418c158eb8f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84af36590abfbf847e39461d5668a9b85b5846ab2c1705bdf2e8858807e9d86c`

```dockerfile
```

-	Layers:
	-	`sha256:aaab43908073c0eddfc13729d70514a3426255ff8d31aa19aa39108390f5c65d`  
		Last Modified: Mon, 03 Jun 2024 19:08:34 GMT  
		Size: 2.3 MB (2264548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6af6c6fa69438301c0c320846677e25900a5aa269506c074071536e7fdc092ff`  
		Last Modified: Mon, 03 Jun 2024 19:08:33 GMT  
		Size: 21.1 KB (21120 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b953ca66ecee777524a0f33f0adefbe99183367e180f4b2ed82d1e525f57d208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32780663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a9c7e97a66ca554c0cfc88de871b1c7dfad7637ffcbd6a79b5c75b3954bb583`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
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
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994933505bafbbaba95cef494f2dfb3e85f2bfde1ea5c4a6dae5a179e39e7b5c`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9488359f89f8c6691f1737ce76ce6b7520511a8246658953dae9429090e88746`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 2.3 MB (2346183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fa925bb96d2305b22651dc4d10899309c212aef95cb13afbdeb2ba5436cb0b`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 1.3 MB (1253469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5284a06f3ca2503602cf214d936daf8aedee3d442d7aa66a5b67874c8f156685`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a475f5b1bcd9a980f0e2923bf1af87002c6468529583ce41a151599d11b2cc`  
		Last Modified: Tue, 14 May 2024 17:41:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:303a74af5e224338560198dc50e2c9cb2a7b4a46b01d39144559de1dd7788518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e79fb901bf217f30113856b6b39e296324993066435904abd2a2152baae6156`

```dockerfile
```

-	Layers:
	-	`sha256:a35747f1af90484d4a9021de5c31be89cb3117cb5f56f499d3cebe78562716cf`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 2.3 MB (2261490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48c7060af35b31db7e804b3ce19451726c3fb6b956edad221ee58000cf04a91`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 21.0 KB (20997 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:36e236fc6b16e7e3170743b8c6a4fbaa296f4d7804c6c2b2106171eac49c9e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33915077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46c7f4bc09921dd239f3c7eb02f4989d48a1df441f3bc33fa1eac70860b0ae6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 00:47:12 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Tue, 14 May 2024 00:47:12 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb23370f3994993b447e434bb257c1618064ae75acb7e15d1fb88d95c481416`  
		Last Modified: Mon, 03 Jun 2024 19:03:52 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43508bc095d4cad435f08c64c32dd8056399b25cddfeca86964d15f117cbd0c`  
		Last Modified: Mon, 03 Jun 2024 19:03:52 GMT  
		Size: 2.5 MB (2492668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2870f8c3ee5b47d7a6a8e194db84b04de521e6a228093ad33b4252661ee3d0d0`  
		Last Modified: Mon, 03 Jun 2024 19:03:52 GMT  
		Size: 1.3 MB (1258253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c83af100d615d1363ef33866755b85f6153e23f56a4e9c1a6cba13d0463082d`  
		Last Modified: Mon, 03 Jun 2024 19:03:53 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ec3bf8bf691991f57de6b00811ed6d06fe0417f1955d1d7b6cd33ecf81b406`  
		Last Modified: Mon, 03 Jun 2024 19:03:53 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:443d7accdadab953db276145a1ab012f3232c120ea362461be5a22531600dca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da086c82559c925e7fcc2b0c79e47076545d92a837f0e4d1b8f49b66cfb55fc0`

```dockerfile
```

-	Layers:
	-	`sha256:829f8d9a7d33b902a3c59de1e19bd0291df3704cf233de30580da78a72c5220f`  
		Last Modified: Mon, 03 Jun 2024 19:03:52 GMT  
		Size: 2.3 MB (2258358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffb9dd39ce17614aed4cd4f0bac42e7b8bb49b726b85d39d48b1700119a54cf0`  
		Last Modified: Mon, 03 Jun 2024 19:03:52 GMT  
		Size: 20.9 KB (20924 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:129ad612a59e558c3da7dfa1a1958d7b374599149ad2ac085bfd539341b0e76d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32335816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4ee8bdf9b447076bff1edf5bfe8aafd428b9e3a1c11745e3eac190a7957b50d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 01:11:07 GMT
ADD file:a92da94a28279478b2eae11dcdcd2913fc06af02498a5515cc3f288668d74e43 in / 
# Tue, 14 May 2024 01:11:12 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6ccc6628d3cdcda935b3b60cb54fa578d669965454d9cf39de3df9c1276132b7`  
		Last Modified: Tue, 14 May 2024 01:22:19 GMT  
		Size: 29.1 MB (29143688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2c2342dfc8d9203635e3e3bc46109d12ef7ef9940adb0794934bca415e4d79`  
		Last Modified: Mon, 03 Jun 2024 19:52:36 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba60c707dc72485dffcb0f586703d60083e3a99568905fc77c61a927aa023133`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 1.9 MB (1937709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5d0dde6405cfccdcc1ece97791b0c134d743d3dbbb4648cfd8ffa51f7fa7fa`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 1.3 MB (1252902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c5806cc8f133288ec076e5d9a6d04f2f7528380144d22892c7b84314c99a8c`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198d6a5f4cd3ba446c2120eb2826773388a541360046c35203d6024dce60a143`  
		Last Modified: Mon, 03 Jun 2024 19:52:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:bf5993b43a4118f01f52ac8a194cb102c52ee5b81fe6f6217d77ca4afaef2a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295c96051f2df83e45a2fe340023dd1e664fdec31e7ef871ca8d797cbc594205`

```dockerfile
```

-	Layers:
	-	`sha256:396ed31b018a1dc19cc7f9fcd8bc9c31f7d68c64735199594c25d0801926c1b7`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:63978abc93d511e5c74a4cc84e7b57a1d767833ba0c69e02c29365668c96bf86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37163958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9054e0ed4fdeb443fcae69bad304d1e19e2434684bbca08c83f5ef5897d1e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 01:20:02 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Tue, 14 May 2024 01:20:04 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:11ee2a6dbc4a6a6b182097f6023f775e595488a6bcc424e9b58001659deb7fa1`  
		Last Modified: Tue, 14 May 2024 01:24:06 GMT  
		Size: 33.1 MB (33141160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d531128e0fac13a6c4e8656afa2e85afbd55db7a786a38bf715c14f4e05a5d94`  
		Last Modified: Mon, 03 Jun 2024 19:50:52 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037940292acc903c706efafe81e090f3eca4683a90304378efe5f4b2cd3cbd47`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 2.7 MB (2698394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d2e0144b8349ea33bdc906d060868aa61958e0c45ac421dcf26a5fc15eb677`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 1.3 MB (1322885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02930e85eb728b1b92f67233fa0c4ff46787e43e4c5f78933df1a64f4c1f7ad0`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cb49628af48f1c1c75566128625afdacca39df7ea0a7c2762ff858d5a3c3e9`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:eae1092d4dd48c0f18e3eda2c5440fe8988dc3823060e738b93a20fba09baf54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea636723fe65c22cb491ee51203b6349d5302ba3288e8ebf7395457c83a78a3`

```dockerfile
```

-	Layers:
	-	`sha256:0c88ae099fbb77c9cefb907169eb358536ff37e4c35140a81c2cb67411da7a9f`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 2.3 MB (2265631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba09bde198a5df307f36fa75f66fe410b324cf250153ce67c8d2f7e9def7d0e5`  
		Last Modified: Mon, 03 Jun 2024 19:50:52 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:da94175eec280d37f0dfd2d8acdc57bd8b4607f66f738dd796b0719c28737986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30903401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf7fe752edb4161d9cd43825ddd58ceff332eb34c41dcc9623255e4cc9bf376`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 00:42:38 GMT
ADD file:55fef93bbad6701fe968a070a0c72b3a0bd3df408dd79c9a616a43dea0de11d0 in / 
# Tue, 14 May 2024 00:42:40 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d7365433874e83ccc92aa5d768989641a64e23c3247409161401a09b4895c406`  
		Last Modified: Tue, 14 May 2024 00:47:35 GMT  
		Size: 27.5 MB (27512398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422d2a0f87a8b8c2712bf0d473e4f936bcbad2af462760d8ae88a25a4ddcbabe`  
		Last Modified: Mon, 03 Jun 2024 19:40:44 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dac9575eb2b0b2d47b6c792dddf0edd2afdeaad0f5dc8a1572996977ceb0fa6`  
		Last Modified: Mon, 03 Jun 2024 19:40:44 GMT  
		Size: 2.2 MB (2152694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e3eb594a178112f9ea3d30d498b8b619b5165ff992e96e66a2cb723b708eea`  
		Last Modified: Mon, 03 Jun 2024 19:40:44 GMT  
		Size: 1.2 MB (1236790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f6ebc8f32f01f7f87e92d446e389a62516dcde1dd8b66b0ed80618c1279d7f`  
		Last Modified: Mon, 03 Jun 2024 19:40:45 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b1370c7b0f96a4cb325b9cd27e7cc508def3a755eaf10f7f2893a6d721d6b6`  
		Last Modified: Mon, 03 Jun 2024 19:40:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:b7e29c218845ad20177e6072bafe8ceb34957f028c9ab5dc784bf0d8abb3266b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:801c05520a31b4c181fcea7491e35a45441ce8b7d97f9f1133ce0da9982b9f65`

```dockerfile
```

-	Layers:
	-	`sha256:7059681ccb9077ae5d5d066a76afbdf315e577e6f6185513b43dc17567fd6a41`  
		Last Modified: Mon, 03 Jun 2024 19:40:44 GMT  
		Size: 2.3 MB (2261081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d33b5d8c8737f3f638401087329e3541977c1b45f846a92a33f44bc802633636`  
		Last Modified: Mon, 03 Jun 2024 19:40:44 GMT  
		Size: 21.0 KB (20979 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.28`

```console
$ docker pull memcached@sha256:fb81bfa7ea3af0a26cdf3598a67327c45cb525eedf6f0ec3b48667127cd8fc42
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:1.6.28` - linux; amd64

```console
$ docker pull memcached@sha256:9147945260ea3aae4982858f21c236318a3f6e714e3247c5baf29a5a72e0f541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32898057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23286975f91428ab86b108f596c0340aed9fc99015d547119acc7f7aaf10007e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc543897dce5b0ec373146149c07d4d311f530d35fd5660eacf896059d19c1f9`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67696248863aa6bf5473db03626425b13368fab900b2145458a0aadf3ec50685`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 2.5 MB (2488532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1225c54544336958562027d237b24c6e6fdf0242b27fedb8de59463271161a`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 1.3 MB (1257596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c8c669390569241c531942ed6c73e9ed972acd0d553620dc73b27efd017da4`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750d4cc56720b2b3726c433153484ee8befc8ef867db54c4ea893932042208b4`  
		Last Modified: Mon, 03 Jun 2024 19:03:49 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.28` - unknown; unknown

```console
$ docker pull memcached@sha256:16ed0d681048581dce561ae4090acbdcf920ce1f2ddce248215521ed4fd9decd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d6ffeaf490e2efb6c46e0c490e1c11020fcf721e84a6b2d8edef168a450b00`

```dockerfile
```

-	Layers:
	-	`sha256:7055f894d5826460bb2eb3ea9b0ef5d51df1ce6b1c073f786f5d1cf92573a368`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 2.3 MB (2261260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1e66ce28cc0bd263cb0b4aa93ffcc60f78c1c750f403cbd3ab265a6794fc167`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 21.0 KB (20979 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.28` - linux; arm variant v5

```console
$ docker pull memcached@sha256:14753c4e01088e08a436d89d02a2a78902028bf49d6db1569f475092fd460bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30237639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c21e319ac699c14e10d279852e999e826acf2731ee4b72c4c10a33bb47692f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 00:48:34 GMT
ADD file:ee9f1914c7fc370bdb089c9e2fcfa15477f7091fc5437cb780232afdf6297586 in / 
# Tue, 14 May 2024 00:48:34 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:169fcae2368e5a601c42972560f091e123648fa0e741975d1b35900c61b9ff71`  
		Last Modified: Tue, 14 May 2024 00:51:36 GMT  
		Size: 26.9 MB (26909921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6135c82883bf5f0df15a6d3d42e97b6013681d12f1f0d535ccb0c1cacf6676b`  
		Last Modified: Mon, 03 Jun 2024 19:08:33 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51f9357aee8294bc0ab883e4493123d2a4dabd21e30ab2900da6cfe6fce5b20`  
		Last Modified: Mon, 03 Jun 2024 19:08:34 GMT  
		Size: 2.1 MB (2089512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32e18a9983de65ed92d9394655a09d3d69089e493a069562641ea42c679e1a4`  
		Last Modified: Mon, 03 Jun 2024 19:08:34 GMT  
		Size: 1.2 MB (1236688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc76114b0bb29114c4b5ff03c2b92a6a317377e26442ec0b79e0016bdc73147d`  
		Last Modified: Mon, 03 Jun 2024 19:08:33 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c636887432e5986c55e92368eef61a43bd3e05cd00609197541f460647ef8208`  
		Last Modified: Mon, 03 Jun 2024 19:08:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.28` - unknown; unknown

```console
$ docker pull memcached@sha256:3db3baea327d4e01491ca8527e9a966a8bc9c6fb518a0f2850e7418c158eb8f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84af36590abfbf847e39461d5668a9b85b5846ab2c1705bdf2e8858807e9d86c`

```dockerfile
```

-	Layers:
	-	`sha256:aaab43908073c0eddfc13729d70514a3426255ff8d31aa19aa39108390f5c65d`  
		Last Modified: Mon, 03 Jun 2024 19:08:34 GMT  
		Size: 2.3 MB (2264548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6af6c6fa69438301c0c320846677e25900a5aa269506c074071536e7fdc092ff`  
		Last Modified: Mon, 03 Jun 2024 19:08:33 GMT  
		Size: 21.1 KB (21120 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.28` - linux; 386

```console
$ docker pull memcached@sha256:36e236fc6b16e7e3170743b8c6a4fbaa296f4d7804c6c2b2106171eac49c9e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33915077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46c7f4bc09921dd239f3c7eb02f4989d48a1df441f3bc33fa1eac70860b0ae6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 00:47:12 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Tue, 14 May 2024 00:47:12 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb23370f3994993b447e434bb257c1618064ae75acb7e15d1fb88d95c481416`  
		Last Modified: Mon, 03 Jun 2024 19:03:52 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43508bc095d4cad435f08c64c32dd8056399b25cddfeca86964d15f117cbd0c`  
		Last Modified: Mon, 03 Jun 2024 19:03:52 GMT  
		Size: 2.5 MB (2492668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2870f8c3ee5b47d7a6a8e194db84b04de521e6a228093ad33b4252661ee3d0d0`  
		Last Modified: Mon, 03 Jun 2024 19:03:52 GMT  
		Size: 1.3 MB (1258253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c83af100d615d1363ef33866755b85f6153e23f56a4e9c1a6cba13d0463082d`  
		Last Modified: Mon, 03 Jun 2024 19:03:53 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ec3bf8bf691991f57de6b00811ed6d06fe0417f1955d1d7b6cd33ecf81b406`  
		Last Modified: Mon, 03 Jun 2024 19:03:53 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.28` - unknown; unknown

```console
$ docker pull memcached@sha256:443d7accdadab953db276145a1ab012f3232c120ea362461be5a22531600dca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da086c82559c925e7fcc2b0c79e47076545d92a837f0e4d1b8f49b66cfb55fc0`

```dockerfile
```

-	Layers:
	-	`sha256:829f8d9a7d33b902a3c59de1e19bd0291df3704cf233de30580da78a72c5220f`  
		Last Modified: Mon, 03 Jun 2024 19:03:52 GMT  
		Size: 2.3 MB (2258358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffb9dd39ce17614aed4cd4f0bac42e7b8bb49b726b85d39d48b1700119a54cf0`  
		Last Modified: Mon, 03 Jun 2024 19:03:52 GMT  
		Size: 20.9 KB (20924 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.28` - linux; mips64le

```console
$ docker pull memcached@sha256:129ad612a59e558c3da7dfa1a1958d7b374599149ad2ac085bfd539341b0e76d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32335816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4ee8bdf9b447076bff1edf5bfe8aafd428b9e3a1c11745e3eac190a7957b50d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 01:11:07 GMT
ADD file:a92da94a28279478b2eae11dcdcd2913fc06af02498a5515cc3f288668d74e43 in / 
# Tue, 14 May 2024 01:11:12 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6ccc6628d3cdcda935b3b60cb54fa578d669965454d9cf39de3df9c1276132b7`  
		Last Modified: Tue, 14 May 2024 01:22:19 GMT  
		Size: 29.1 MB (29143688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2c2342dfc8d9203635e3e3bc46109d12ef7ef9940adb0794934bca415e4d79`  
		Last Modified: Mon, 03 Jun 2024 19:52:36 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba60c707dc72485dffcb0f586703d60083e3a99568905fc77c61a927aa023133`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 1.9 MB (1937709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5d0dde6405cfccdcc1ece97791b0c134d743d3dbbb4648cfd8ffa51f7fa7fa`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 1.3 MB (1252902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c5806cc8f133288ec076e5d9a6d04f2f7528380144d22892c7b84314c99a8c`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198d6a5f4cd3ba446c2120eb2826773388a541360046c35203d6024dce60a143`  
		Last Modified: Mon, 03 Jun 2024 19:52:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.28` - unknown; unknown

```console
$ docker pull memcached@sha256:bf5993b43a4118f01f52ac8a194cb102c52ee5b81fe6f6217d77ca4afaef2a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295c96051f2df83e45a2fe340023dd1e664fdec31e7ef871ca8d797cbc594205`

```dockerfile
```

-	Layers:
	-	`sha256:396ed31b018a1dc19cc7f9fcd8bc9c31f7d68c64735199594c25d0801926c1b7`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.28` - linux; ppc64le

```console
$ docker pull memcached@sha256:63978abc93d511e5c74a4cc84e7b57a1d767833ba0c69e02c29365668c96bf86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37163958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9054e0ed4fdeb443fcae69bad304d1e19e2434684bbca08c83f5ef5897d1e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 01:20:02 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Tue, 14 May 2024 01:20:04 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:11ee2a6dbc4a6a6b182097f6023f775e595488a6bcc424e9b58001659deb7fa1`  
		Last Modified: Tue, 14 May 2024 01:24:06 GMT  
		Size: 33.1 MB (33141160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d531128e0fac13a6c4e8656afa2e85afbd55db7a786a38bf715c14f4e05a5d94`  
		Last Modified: Mon, 03 Jun 2024 19:50:52 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037940292acc903c706efafe81e090f3eca4683a90304378efe5f4b2cd3cbd47`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 2.7 MB (2698394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d2e0144b8349ea33bdc906d060868aa61958e0c45ac421dcf26a5fc15eb677`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 1.3 MB (1322885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02930e85eb728b1b92f67233fa0c4ff46787e43e4c5f78933df1a64f4c1f7ad0`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cb49628af48f1c1c75566128625afdacca39df7ea0a7c2762ff858d5a3c3e9`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.28` - unknown; unknown

```console
$ docker pull memcached@sha256:eae1092d4dd48c0f18e3eda2c5440fe8988dc3823060e738b93a20fba09baf54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea636723fe65c22cb491ee51203b6349d5302ba3288e8ebf7395457c83a78a3`

```dockerfile
```

-	Layers:
	-	`sha256:0c88ae099fbb77c9cefb907169eb358536ff37e4c35140a81c2cb67411da7a9f`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 2.3 MB (2265631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba09bde198a5df307f36fa75f66fe410b324cf250153ce67c8d2f7e9def7d0e5`  
		Last Modified: Mon, 03 Jun 2024 19:50:52 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.28` - linux; s390x

```console
$ docker pull memcached@sha256:da94175eec280d37f0dfd2d8acdc57bd8b4607f66f738dd796b0719c28737986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30903401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf7fe752edb4161d9cd43825ddd58ceff332eb34c41dcc9623255e4cc9bf376`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 00:42:38 GMT
ADD file:55fef93bbad6701fe968a070a0c72b3a0bd3df408dd79c9a616a43dea0de11d0 in / 
# Tue, 14 May 2024 00:42:40 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d7365433874e83ccc92aa5d768989641a64e23c3247409161401a09b4895c406`  
		Last Modified: Tue, 14 May 2024 00:47:35 GMT  
		Size: 27.5 MB (27512398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422d2a0f87a8b8c2712bf0d473e4f936bcbad2af462760d8ae88a25a4ddcbabe`  
		Last Modified: Mon, 03 Jun 2024 19:40:44 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dac9575eb2b0b2d47b6c792dddf0edd2afdeaad0f5dc8a1572996977ceb0fa6`  
		Last Modified: Mon, 03 Jun 2024 19:40:44 GMT  
		Size: 2.2 MB (2152694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e3eb594a178112f9ea3d30d498b8b619b5165ff992e96e66a2cb723b708eea`  
		Last Modified: Mon, 03 Jun 2024 19:40:44 GMT  
		Size: 1.2 MB (1236790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f6ebc8f32f01f7f87e92d446e389a62516dcde1dd8b66b0ed80618c1279d7f`  
		Last Modified: Mon, 03 Jun 2024 19:40:45 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b1370c7b0f96a4cb325b9cd27e7cc508def3a755eaf10f7f2893a6d721d6b6`  
		Last Modified: Mon, 03 Jun 2024 19:40:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.28` - unknown; unknown

```console
$ docker pull memcached@sha256:b7e29c218845ad20177e6072bafe8ceb34957f028c9ab5dc784bf0d8abb3266b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:801c05520a31b4c181fcea7491e35a45441ce8b7d97f9f1133ce0da9982b9f65`

```dockerfile
```

-	Layers:
	-	`sha256:7059681ccb9077ae5d5d066a76afbdf315e577e6f6185513b43dc17567fd6a41`  
		Last Modified: Mon, 03 Jun 2024 19:40:44 GMT  
		Size: 2.3 MB (2261081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d33b5d8c8737f3f638401087329e3541977c1b45f846a92a33f44bc802633636`  
		Last Modified: Mon, 03 Jun 2024 19:40:44 GMT  
		Size: 21.0 KB (20979 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.28-alpine`

```console
$ docker pull memcached@sha256:6c5c70454314cec1db57010b2ddc4e5e7412244c15833bb789b4cae046ecfb43
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:1.6.28-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:7e7f1b92cbd46c4b5f60777f034debc77c1b66bd5b66b732e424d47bc9fbeed0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4681905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae47e754356b145ac3883025be70df81397e012b7b9deea79c6e1549cebb820`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723fe97584e549852ab448538bb35f45d46da4b09c52e18fa4eeec5352c47a42`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5f2dacb5179622644f1e47531960f1fa5aef816fb60aad38a20349103c7191`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 103.8 KB (103828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef494bb92067167934aab739f7d1f023f4e34ef112f973afc201b98e54fa5d50`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 954.6 KB (954617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd803b6c0eb021a0b33649dd96256f867eac7aa91b9255624ed7f239c9475ff`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1c222c9d9e5ee0e2e34c4386e9c09b7ebf79a12072e245332f295c63bddf3e`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.28-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2dd815e2d1643bcba94e92c59e4c260f02bf06b0ff954840272439de861358f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 KB (103568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0885c1305da890646b6ad6dbcd2ae57932bcd2d1b804dc7404de2cd8713cc284`

```dockerfile
```

-	Layers:
	-	`sha256:6e6853da7f25eec4b641df434dccd72f8d65a0a540787c715049bd366d0f787b`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 84.3 KB (84267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b7bd473fc9187722cabb9a96acad9c5a1dbb88c26431928b2166223fb0dee7c`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 19.3 KB (19301 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.28-alpine` - linux; 386

```console
$ docker pull memcached@sha256:d021aa4701a1cbf3afb535aa82cd88bc0f7c5d51c05c34d5160fabd876a5bce7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d85661f9f9c582ffadd4540ae1b2fb7bf653da454d36eab21d69ed0aa33ddb7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:05:50 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 18:05:51 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77c9b09b82af8bb67811ab3d796c64874348624abc7cf7658894f3042e3fdda`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61451eaaecf42ca95101dad4ed37d00cf792b8afae1d5eeab46e43e258b3ef4`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 109.0 KB (108954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1cfe9a7dc0eb6422fdd3e24036097ac92ebb3781776994ac1a1985641b7746a`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 947.9 KB (947940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffa1b620c706dc7fccfe69ac07a840b285472eebf3a5b12f4627f73b14a8262`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3107d914479457d4f68098546010a68c957c8958f8617fe612a4de36890751d`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.28-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:f7757ea9df5138c45bdbcd9e258bd5f8d3b847272ba419799988079f669fbe74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 KB (103468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f14b161d58134f0ae5adc6bf8b94c753848d136ed143b505c68fd6d0083ef5e`

```dockerfile
```

-	Layers:
	-	`sha256:977ffaf9dabb1b3eba7edd08c3c73174de9a29484b0f80d86a81072bb317517f`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 84.2 KB (84222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d4314a7e1c917ad745b623d3c1ea185133876babcee74b1048a636196ae0e48`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 19.2 KB (19246 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.28-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:0b9a2b083716079e6c1da7a9eef4cda25b8d81f3e16840ca6b2b12e9d90e00b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c5555e7ff1014a88296e46cd6d51b379698f7678f76fcd835e8c9f30d647d79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f168e15e72e8585ac6cf20d04f29cfeea15135f34178693fec86adfd88204d`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e2f6d65a966b68fa13bdc24e920a1a1fa7b86b2e000d17eff60efbfdd38993`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 123.0 KB (123004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5864e6eb973cda0b80fc0b600b8fdc61cab246b23ff08158ec77e3c819aacb99`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 992.9 KB (992907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af9bfa929a4b7886285f34b50a2506270b5db318f414db5cfa7c505e069495e`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf6c5b09507827cb18669a5979a2e3e258baa20df3c7d3b1790c8e47c4da755`  
		Last Modified: Mon, 03 Jun 2024 19:53:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.28-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:47e12d8b1103b819e814e52b644a34f6fd25e9b3c301cf64bd3a5aed59882a32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 KB (101740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac2cf30c8b57070d3d517da1a03e3bf9241f943b85fa56a7a7cafcec23db720f`

```dockerfile
```

-	Layers:
	-	`sha256:bf26f6e69d9a08fc6932c97112ad23a6a9b487855c46d9d7e0c8bddd8b5292f2`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 82.4 KB (82371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:018afee57a818e12505b2c4851b768103c8b30b0796588e3def21bb1bb3e7d24`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 19.4 KB (19369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.28-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:c9d716888f3de4b62fcb97a29f86e58ace3ecd27d3e140bf093a91a55b457895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4551732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98e758f93cfeb8699e726a62495bbcb588c84eb23144c8f4fef5e84556142be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b951b4f532c41c7412daf128075fc9cd89c182acbc79418cb89d9bdcca3f7f5`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ace4ff1604d5e2114f279c4a7dbd9c7255f5c22442459e1dde1e1dba3c3662`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 112.7 KB (112734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3635c0cf5ff89eaa5a72c24ee555909e50ee12d3629572ef94a113391f5b0e92`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 977.3 KB (977292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e93a0ef4a20f636cd8f486379f0e8926c809875d1be02f187e1d9beb0155870`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2e88b16dd19768ead777afafdc9ec27072ab209e2f240c51dce37ce1590302`  
		Last Modified: Mon, 03 Jun 2024 19:44:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.28-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7e094c1f57f2f2a6a9f5e6290afe42f796d0444a80835660c23f0880808b9fac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 KB (101612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22673137bae204447eabe141346d72e57cec6908c114a55f94494e572a484849`

```dockerfile
```

-	Layers:
	-	`sha256:245be0555de7893afdeab5ba2e974bc77e29549c40a4bdb62d8b49cdd98938c8`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 82.3 KB (82313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41c84b152f2dcb64eb163c14efbbe0d430a1cd597e9fe2a74c52c447568f2d9f`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 19.3 KB (19299 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.28-alpine3.20`

```console
$ docker pull memcached@sha256:6c5c70454314cec1db57010b2ddc4e5e7412244c15833bb789b4cae046ecfb43
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:1.6.28-alpine3.20` - linux; amd64

```console
$ docker pull memcached@sha256:7e7f1b92cbd46c4b5f60777f034debc77c1b66bd5b66b732e424d47bc9fbeed0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4681905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae47e754356b145ac3883025be70df81397e012b7b9deea79c6e1549cebb820`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723fe97584e549852ab448538bb35f45d46da4b09c52e18fa4eeec5352c47a42`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5f2dacb5179622644f1e47531960f1fa5aef816fb60aad38a20349103c7191`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 103.8 KB (103828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef494bb92067167934aab739f7d1f023f4e34ef112f973afc201b98e54fa5d50`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 954.6 KB (954617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd803b6c0eb021a0b33649dd96256f867eac7aa91b9255624ed7f239c9475ff`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1c222c9d9e5ee0e2e34c4386e9c09b7ebf79a12072e245332f295c63bddf3e`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.28-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:2dd815e2d1643bcba94e92c59e4c260f02bf06b0ff954840272439de861358f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 KB (103568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0885c1305da890646b6ad6dbcd2ae57932bcd2d1b804dc7404de2cd8713cc284`

```dockerfile
```

-	Layers:
	-	`sha256:6e6853da7f25eec4b641df434dccd72f8d65a0a540787c715049bd366d0f787b`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 84.3 KB (84267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b7bd473fc9187722cabb9a96acad9c5a1dbb88c26431928b2166223fb0dee7c`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 19.3 KB (19301 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.28-alpine3.20` - linux; 386

```console
$ docker pull memcached@sha256:d021aa4701a1cbf3afb535aa82cd88bc0f7c5d51c05c34d5160fabd876a5bce7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d85661f9f9c582ffadd4540ae1b2fb7bf653da454d36eab21d69ed0aa33ddb7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:05:50 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 18:05:51 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77c9b09b82af8bb67811ab3d796c64874348624abc7cf7658894f3042e3fdda`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61451eaaecf42ca95101dad4ed37d00cf792b8afae1d5eeab46e43e258b3ef4`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 109.0 KB (108954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1cfe9a7dc0eb6422fdd3e24036097ac92ebb3781776994ac1a1985641b7746a`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 947.9 KB (947940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffa1b620c706dc7fccfe69ac07a840b285472eebf3a5b12f4627f73b14a8262`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3107d914479457d4f68098546010a68c957c8958f8617fe612a4de36890751d`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.28-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:f7757ea9df5138c45bdbcd9e258bd5f8d3b847272ba419799988079f669fbe74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 KB (103468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f14b161d58134f0ae5adc6bf8b94c753848d136ed143b505c68fd6d0083ef5e`

```dockerfile
```

-	Layers:
	-	`sha256:977ffaf9dabb1b3eba7edd08c3c73174de9a29484b0f80d86a81072bb317517f`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 84.2 KB (84222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d4314a7e1c917ad745b623d3c1ea185133876babcee74b1048a636196ae0e48`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 19.2 KB (19246 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.28-alpine3.20` - linux; ppc64le

```console
$ docker pull memcached@sha256:0b9a2b083716079e6c1da7a9eef4cda25b8d81f3e16840ca6b2b12e9d90e00b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c5555e7ff1014a88296e46cd6d51b379698f7678f76fcd835e8c9f30d647d79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f168e15e72e8585ac6cf20d04f29cfeea15135f34178693fec86adfd88204d`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e2f6d65a966b68fa13bdc24e920a1a1fa7b86b2e000d17eff60efbfdd38993`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 123.0 KB (123004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5864e6eb973cda0b80fc0b600b8fdc61cab246b23ff08158ec77e3c819aacb99`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 992.9 KB (992907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af9bfa929a4b7886285f34b50a2506270b5db318f414db5cfa7c505e069495e`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf6c5b09507827cb18669a5979a2e3e258baa20df3c7d3b1790c8e47c4da755`  
		Last Modified: Mon, 03 Jun 2024 19:53:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.28-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:47e12d8b1103b819e814e52b644a34f6fd25e9b3c301cf64bd3a5aed59882a32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 KB (101740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac2cf30c8b57070d3d517da1a03e3bf9241f943b85fa56a7a7cafcec23db720f`

```dockerfile
```

-	Layers:
	-	`sha256:bf26f6e69d9a08fc6932c97112ad23a6a9b487855c46d9d7e0c8bddd8b5292f2`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 82.4 KB (82371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:018afee57a818e12505b2c4851b768103c8b30b0796588e3def21bb1bb3e7d24`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 19.4 KB (19369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.28-alpine3.20` - linux; s390x

```console
$ docker pull memcached@sha256:c9d716888f3de4b62fcb97a29f86e58ace3ecd27d3e140bf093a91a55b457895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4551732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98e758f93cfeb8699e726a62495bbcb588c84eb23144c8f4fef5e84556142be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b951b4f532c41c7412daf128075fc9cd89c182acbc79418cb89d9bdcca3f7f5`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ace4ff1604d5e2114f279c4a7dbd9c7255f5c22442459e1dde1e1dba3c3662`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 112.7 KB (112734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3635c0cf5ff89eaa5a72c24ee555909e50ee12d3629572ef94a113391f5b0e92`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 977.3 KB (977292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e93a0ef4a20f636cd8f486379f0e8926c809875d1be02f187e1d9beb0155870`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2e88b16dd19768ead777afafdc9ec27072ab209e2f240c51dce37ce1590302`  
		Last Modified: Mon, 03 Jun 2024 19:44:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.28-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:7e094c1f57f2f2a6a9f5e6290afe42f796d0444a80835660c23f0880808b9fac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 KB (101612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22673137bae204447eabe141346d72e57cec6908c114a55f94494e572a484849`

```dockerfile
```

-	Layers:
	-	`sha256:245be0555de7893afdeab5ba2e974bc77e29549c40a4bdb62d8b49cdd98938c8`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 82.3 KB (82313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41c84b152f2dcb64eb163c14efbbe0d430a1cd597e9fe2a74c52c447568f2d9f`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 19.3 KB (19299 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.28-bookworm`

```console
$ docker pull memcached@sha256:fb81bfa7ea3af0a26cdf3598a67327c45cb525eedf6f0ec3b48667127cd8fc42
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:1.6.28-bookworm` - linux; amd64

```console
$ docker pull memcached@sha256:9147945260ea3aae4982858f21c236318a3f6e714e3247c5baf29a5a72e0f541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32898057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23286975f91428ab86b108f596c0340aed9fc99015d547119acc7f7aaf10007e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc543897dce5b0ec373146149c07d4d311f530d35fd5660eacf896059d19c1f9`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67696248863aa6bf5473db03626425b13368fab900b2145458a0aadf3ec50685`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 2.5 MB (2488532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1225c54544336958562027d237b24c6e6fdf0242b27fedb8de59463271161a`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 1.3 MB (1257596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c8c669390569241c531942ed6c73e9ed972acd0d553620dc73b27efd017da4`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750d4cc56720b2b3726c433153484ee8befc8ef867db54c4ea893932042208b4`  
		Last Modified: Mon, 03 Jun 2024 19:03:49 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.28-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:16ed0d681048581dce561ae4090acbdcf920ce1f2ddce248215521ed4fd9decd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d6ffeaf490e2efb6c46e0c490e1c11020fcf721e84a6b2d8edef168a450b00`

```dockerfile
```

-	Layers:
	-	`sha256:7055f894d5826460bb2eb3ea9b0ef5d51df1ce6b1c073f786f5d1cf92573a368`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 2.3 MB (2261260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1e66ce28cc0bd263cb0b4aa93ffcc60f78c1c750f403cbd3ab265a6794fc167`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 21.0 KB (20979 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.28-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:14753c4e01088e08a436d89d02a2a78902028bf49d6db1569f475092fd460bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30237639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c21e319ac699c14e10d279852e999e826acf2731ee4b72c4c10a33bb47692f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 00:48:34 GMT
ADD file:ee9f1914c7fc370bdb089c9e2fcfa15477f7091fc5437cb780232afdf6297586 in / 
# Tue, 14 May 2024 00:48:34 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:169fcae2368e5a601c42972560f091e123648fa0e741975d1b35900c61b9ff71`  
		Last Modified: Tue, 14 May 2024 00:51:36 GMT  
		Size: 26.9 MB (26909921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6135c82883bf5f0df15a6d3d42e97b6013681d12f1f0d535ccb0c1cacf6676b`  
		Last Modified: Mon, 03 Jun 2024 19:08:33 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51f9357aee8294bc0ab883e4493123d2a4dabd21e30ab2900da6cfe6fce5b20`  
		Last Modified: Mon, 03 Jun 2024 19:08:34 GMT  
		Size: 2.1 MB (2089512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32e18a9983de65ed92d9394655a09d3d69089e493a069562641ea42c679e1a4`  
		Last Modified: Mon, 03 Jun 2024 19:08:34 GMT  
		Size: 1.2 MB (1236688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc76114b0bb29114c4b5ff03c2b92a6a317377e26442ec0b79e0016bdc73147d`  
		Last Modified: Mon, 03 Jun 2024 19:08:33 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c636887432e5986c55e92368eef61a43bd3e05cd00609197541f460647ef8208`  
		Last Modified: Mon, 03 Jun 2024 19:08:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.28-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:3db3baea327d4e01491ca8527e9a966a8bc9c6fb518a0f2850e7418c158eb8f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84af36590abfbf847e39461d5668a9b85b5846ab2c1705bdf2e8858807e9d86c`

```dockerfile
```

-	Layers:
	-	`sha256:aaab43908073c0eddfc13729d70514a3426255ff8d31aa19aa39108390f5c65d`  
		Last Modified: Mon, 03 Jun 2024 19:08:34 GMT  
		Size: 2.3 MB (2264548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6af6c6fa69438301c0c320846677e25900a5aa269506c074071536e7fdc092ff`  
		Last Modified: Mon, 03 Jun 2024 19:08:33 GMT  
		Size: 21.1 KB (21120 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.28-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:36e236fc6b16e7e3170743b8c6a4fbaa296f4d7804c6c2b2106171eac49c9e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33915077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46c7f4bc09921dd239f3c7eb02f4989d48a1df441f3bc33fa1eac70860b0ae6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 00:47:12 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Tue, 14 May 2024 00:47:12 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb23370f3994993b447e434bb257c1618064ae75acb7e15d1fb88d95c481416`  
		Last Modified: Mon, 03 Jun 2024 19:03:52 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43508bc095d4cad435f08c64c32dd8056399b25cddfeca86964d15f117cbd0c`  
		Last Modified: Mon, 03 Jun 2024 19:03:52 GMT  
		Size: 2.5 MB (2492668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2870f8c3ee5b47d7a6a8e194db84b04de521e6a228093ad33b4252661ee3d0d0`  
		Last Modified: Mon, 03 Jun 2024 19:03:52 GMT  
		Size: 1.3 MB (1258253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c83af100d615d1363ef33866755b85f6153e23f56a4e9c1a6cba13d0463082d`  
		Last Modified: Mon, 03 Jun 2024 19:03:53 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ec3bf8bf691991f57de6b00811ed6d06fe0417f1955d1d7b6cd33ecf81b406`  
		Last Modified: Mon, 03 Jun 2024 19:03:53 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.28-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:443d7accdadab953db276145a1ab012f3232c120ea362461be5a22531600dca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da086c82559c925e7fcc2b0c79e47076545d92a837f0e4d1b8f49b66cfb55fc0`

```dockerfile
```

-	Layers:
	-	`sha256:829f8d9a7d33b902a3c59de1e19bd0291df3704cf233de30580da78a72c5220f`  
		Last Modified: Mon, 03 Jun 2024 19:03:52 GMT  
		Size: 2.3 MB (2258358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffb9dd39ce17614aed4cd4f0bac42e7b8bb49b726b85d39d48b1700119a54cf0`  
		Last Modified: Mon, 03 Jun 2024 19:03:52 GMT  
		Size: 20.9 KB (20924 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.28-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:129ad612a59e558c3da7dfa1a1958d7b374599149ad2ac085bfd539341b0e76d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32335816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4ee8bdf9b447076bff1edf5bfe8aafd428b9e3a1c11745e3eac190a7957b50d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 01:11:07 GMT
ADD file:a92da94a28279478b2eae11dcdcd2913fc06af02498a5515cc3f288668d74e43 in / 
# Tue, 14 May 2024 01:11:12 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6ccc6628d3cdcda935b3b60cb54fa578d669965454d9cf39de3df9c1276132b7`  
		Last Modified: Tue, 14 May 2024 01:22:19 GMT  
		Size: 29.1 MB (29143688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2c2342dfc8d9203635e3e3bc46109d12ef7ef9940adb0794934bca415e4d79`  
		Last Modified: Mon, 03 Jun 2024 19:52:36 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba60c707dc72485dffcb0f586703d60083e3a99568905fc77c61a927aa023133`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 1.9 MB (1937709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5d0dde6405cfccdcc1ece97791b0c134d743d3dbbb4648cfd8ffa51f7fa7fa`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 1.3 MB (1252902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c5806cc8f133288ec076e5d9a6d04f2f7528380144d22892c7b84314c99a8c`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198d6a5f4cd3ba446c2120eb2826773388a541360046c35203d6024dce60a143`  
		Last Modified: Mon, 03 Jun 2024 19:52:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.28-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:bf5993b43a4118f01f52ac8a194cb102c52ee5b81fe6f6217d77ca4afaef2a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295c96051f2df83e45a2fe340023dd1e664fdec31e7ef871ca8d797cbc594205`

```dockerfile
```

-	Layers:
	-	`sha256:396ed31b018a1dc19cc7f9fcd8bc9c31f7d68c64735199594c25d0801926c1b7`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.28-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:63978abc93d511e5c74a4cc84e7b57a1d767833ba0c69e02c29365668c96bf86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37163958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9054e0ed4fdeb443fcae69bad304d1e19e2434684bbca08c83f5ef5897d1e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 01:20:02 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Tue, 14 May 2024 01:20:04 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:11ee2a6dbc4a6a6b182097f6023f775e595488a6bcc424e9b58001659deb7fa1`  
		Last Modified: Tue, 14 May 2024 01:24:06 GMT  
		Size: 33.1 MB (33141160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d531128e0fac13a6c4e8656afa2e85afbd55db7a786a38bf715c14f4e05a5d94`  
		Last Modified: Mon, 03 Jun 2024 19:50:52 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037940292acc903c706efafe81e090f3eca4683a90304378efe5f4b2cd3cbd47`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 2.7 MB (2698394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d2e0144b8349ea33bdc906d060868aa61958e0c45ac421dcf26a5fc15eb677`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 1.3 MB (1322885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02930e85eb728b1b92f67233fa0c4ff46787e43e4c5f78933df1a64f4c1f7ad0`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cb49628af48f1c1c75566128625afdacca39df7ea0a7c2762ff858d5a3c3e9`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.28-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:eae1092d4dd48c0f18e3eda2c5440fe8988dc3823060e738b93a20fba09baf54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea636723fe65c22cb491ee51203b6349d5302ba3288e8ebf7395457c83a78a3`

```dockerfile
```

-	Layers:
	-	`sha256:0c88ae099fbb77c9cefb907169eb358536ff37e4c35140a81c2cb67411da7a9f`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 2.3 MB (2265631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba09bde198a5df307f36fa75f66fe410b324cf250153ce67c8d2f7e9def7d0e5`  
		Last Modified: Mon, 03 Jun 2024 19:50:52 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.28-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:da94175eec280d37f0dfd2d8acdc57bd8b4607f66f738dd796b0719c28737986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30903401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf7fe752edb4161d9cd43825ddd58ceff332eb34c41dcc9623255e4cc9bf376`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 00:42:38 GMT
ADD file:55fef93bbad6701fe968a070a0c72b3a0bd3df408dd79c9a616a43dea0de11d0 in / 
# Tue, 14 May 2024 00:42:40 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d7365433874e83ccc92aa5d768989641a64e23c3247409161401a09b4895c406`  
		Last Modified: Tue, 14 May 2024 00:47:35 GMT  
		Size: 27.5 MB (27512398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422d2a0f87a8b8c2712bf0d473e4f936bcbad2af462760d8ae88a25a4ddcbabe`  
		Last Modified: Mon, 03 Jun 2024 19:40:44 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dac9575eb2b0b2d47b6c792dddf0edd2afdeaad0f5dc8a1572996977ceb0fa6`  
		Last Modified: Mon, 03 Jun 2024 19:40:44 GMT  
		Size: 2.2 MB (2152694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e3eb594a178112f9ea3d30d498b8b619b5165ff992e96e66a2cb723b708eea`  
		Last Modified: Mon, 03 Jun 2024 19:40:44 GMT  
		Size: 1.2 MB (1236790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f6ebc8f32f01f7f87e92d446e389a62516dcde1dd8b66b0ed80618c1279d7f`  
		Last Modified: Mon, 03 Jun 2024 19:40:45 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b1370c7b0f96a4cb325b9cd27e7cc508def3a755eaf10f7f2893a6d721d6b6`  
		Last Modified: Mon, 03 Jun 2024 19:40:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.28-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:b7e29c218845ad20177e6072bafe8ceb34957f028c9ab5dc784bf0d8abb3266b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:801c05520a31b4c181fcea7491e35a45441ce8b7d97f9f1133ce0da9982b9f65`

```dockerfile
```

-	Layers:
	-	`sha256:7059681ccb9077ae5d5d066a76afbdf315e577e6f6185513b43dc17567fd6a41`  
		Last Modified: Mon, 03 Jun 2024 19:40:44 GMT  
		Size: 2.3 MB (2261081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d33b5d8c8737f3f638401087329e3541977c1b45f846a92a33f44bc802633636`  
		Last Modified: Mon, 03 Jun 2024 19:40:44 GMT  
		Size: 21.0 KB (20979 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine`

```console
$ docker pull memcached@sha256:dcdfc647eaab83cce1e15874888f7e28bdae4b1b947f637e45fec64db1d1a3e3
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
$ docker pull memcached@sha256:7e7f1b92cbd46c4b5f60777f034debc77c1b66bd5b66b732e424d47bc9fbeed0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4681905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae47e754356b145ac3883025be70df81397e012b7b9deea79c6e1549cebb820`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723fe97584e549852ab448538bb35f45d46da4b09c52e18fa4eeec5352c47a42`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5f2dacb5179622644f1e47531960f1fa5aef816fb60aad38a20349103c7191`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 103.8 KB (103828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef494bb92067167934aab739f7d1f023f4e34ef112f973afc201b98e54fa5d50`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 954.6 KB (954617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd803b6c0eb021a0b33649dd96256f867eac7aa91b9255624ed7f239c9475ff`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1c222c9d9e5ee0e2e34c4386e9c09b7ebf79a12072e245332f295c63bddf3e`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2dd815e2d1643bcba94e92c59e4c260f02bf06b0ff954840272439de861358f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 KB (103568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0885c1305da890646b6ad6dbcd2ae57932bcd2d1b804dc7404de2cd8713cc284`

```dockerfile
```

-	Layers:
	-	`sha256:6e6853da7f25eec4b641df434dccd72f8d65a0a540787c715049bd366d0f787b`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 84.3 KB (84267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b7bd473fc9187722cabb9a96acad9c5a1dbb88c26431928b2166223fb0dee7c`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 19.3 KB (19301 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:e0688d9873a4cf749f89b43548d03f7d6c873596b1495b6da6943d4a3e767df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5166898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6a1a46a5867d6ecd3c9bf99a695a89cc1f746f59d3a9a140b85a42b99a2e26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_VERSION=1.6.27
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 22 May 2024 18:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:54:12 GMT
USER memcache
# Wed, 22 May 2024 18:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 May 2024 18:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024a9ccd1af8ffcfe453e22adead9362703e916c9dec4f1d4e94b597e660f23e`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab592fa6ce63bf6772b1c208275d773ef6e671af73b2bd119e98de86dce4fc1`  
		Last Modified: Thu, 23 May 2024 06:29:58 GMT  
		Size: 121.0 KB (121017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd20d288c43aabf4d5e06a885b2e2f24583aae8e102eca2bf9257ce5e307a2cd`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 957.7 KB (957743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d039a0fcb8c2c4f062cb3fb5c2b20ae16915479721254aadfc68d0319c84ee25`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cf5bc5246a4e40149d2a6b161c9fbce8354373e305c03088715546070c2742`  
		Last Modified: Thu, 23 May 2024 06:29:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ec1932014529a81f308cae2db47073ddf344ef48cbc77766d95510cb7385b2af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 KB (103606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0d85c8cad5520d9245c1563457fcf55da9b744f736c305ad21fad10027e013`

```dockerfile
```

-	Layers:
	-	`sha256:f77bdac9710cd22ef4eb7ba293b1b4fe4736e109a3767950432991fe0237fa54`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 84.3 KB (84287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12016cd6764c2821a23d0e8fb3c182eda4d12d096e83cf52f57eb0103616d5e8`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 19.3 KB (19319 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:d021aa4701a1cbf3afb535aa82cd88bc0f7c5d51c05c34d5160fabd876a5bce7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d85661f9f9c582ffadd4540ae1b2fb7bf653da454d36eab21d69ed0aa33ddb7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:05:50 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 18:05:51 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77c9b09b82af8bb67811ab3d796c64874348624abc7cf7658894f3042e3fdda`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61451eaaecf42ca95101dad4ed37d00cf792b8afae1d5eeab46e43e258b3ef4`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 109.0 KB (108954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1cfe9a7dc0eb6422fdd3e24036097ac92ebb3781776994ac1a1985641b7746a`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 947.9 KB (947940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffa1b620c706dc7fccfe69ac07a840b285472eebf3a5b12f4627f73b14a8262`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3107d914479457d4f68098546010a68c957c8958f8617fe612a4de36890751d`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:f7757ea9df5138c45bdbcd9e258bd5f8d3b847272ba419799988079f669fbe74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 KB (103468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f14b161d58134f0ae5adc6bf8b94c753848d136ed143b505c68fd6d0083ef5e`

```dockerfile
```

-	Layers:
	-	`sha256:977ffaf9dabb1b3eba7edd08c3c73174de9a29484b0f80d86a81072bb317517f`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 84.2 KB (84222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d4314a7e1c917ad745b623d3c1ea185133876babcee74b1048a636196ae0e48`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 19.2 KB (19246 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:0b9a2b083716079e6c1da7a9eef4cda25b8d81f3e16840ca6b2b12e9d90e00b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c5555e7ff1014a88296e46cd6d51b379698f7678f76fcd835e8c9f30d647d79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f168e15e72e8585ac6cf20d04f29cfeea15135f34178693fec86adfd88204d`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e2f6d65a966b68fa13bdc24e920a1a1fa7b86b2e000d17eff60efbfdd38993`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 123.0 KB (123004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5864e6eb973cda0b80fc0b600b8fdc61cab246b23ff08158ec77e3c819aacb99`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 992.9 KB (992907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af9bfa929a4b7886285f34b50a2506270b5db318f414db5cfa7c505e069495e`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf6c5b09507827cb18669a5979a2e3e258baa20df3c7d3b1790c8e47c4da755`  
		Last Modified: Mon, 03 Jun 2024 19:53:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:47e12d8b1103b819e814e52b644a34f6fd25e9b3c301cf64bd3a5aed59882a32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 KB (101740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac2cf30c8b57070d3d517da1a03e3bf9241f943b85fa56a7a7cafcec23db720f`

```dockerfile
```

-	Layers:
	-	`sha256:bf26f6e69d9a08fc6932c97112ad23a6a9b487855c46d9d7e0c8bddd8b5292f2`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 82.4 KB (82371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:018afee57a818e12505b2c4851b768103c8b30b0796588e3def21bb1bb3e7d24`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 19.4 KB (19369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; s390x

```console
$ docker pull memcached@sha256:c9d716888f3de4b62fcb97a29f86e58ace3ecd27d3e140bf093a91a55b457895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4551732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98e758f93cfeb8699e726a62495bbcb588c84eb23144c8f4fef5e84556142be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b951b4f532c41c7412daf128075fc9cd89c182acbc79418cb89d9bdcca3f7f5`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ace4ff1604d5e2114f279c4a7dbd9c7255f5c22442459e1dde1e1dba3c3662`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 112.7 KB (112734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3635c0cf5ff89eaa5a72c24ee555909e50ee12d3629572ef94a113391f5b0e92`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 977.3 KB (977292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e93a0ef4a20f636cd8f486379f0e8926c809875d1be02f187e1d9beb0155870`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2e88b16dd19768ead777afafdc9ec27072ab209e2f240c51dce37ce1590302`  
		Last Modified: Mon, 03 Jun 2024 19:44:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7e094c1f57f2f2a6a9f5e6290afe42f796d0444a80835660c23f0880808b9fac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 KB (101612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22673137bae204447eabe141346d72e57cec6908c114a55f94494e572a484849`

```dockerfile
```

-	Layers:
	-	`sha256:245be0555de7893afdeab5ba2e974bc77e29549c40a4bdb62d8b49cdd98938c8`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 82.3 KB (82313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41c84b152f2dcb64eb163c14efbbe0d430a1cd597e9fe2a74c52c447568f2d9f`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 19.3 KB (19299 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine3.20`

```console
$ docker pull memcached@sha256:dcdfc647eaab83cce1e15874888f7e28bdae4b1b947f637e45fec64db1d1a3e3
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

### `memcached:alpine3.20` - linux; amd64

```console
$ docker pull memcached@sha256:7e7f1b92cbd46c4b5f60777f034debc77c1b66bd5b66b732e424d47bc9fbeed0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4681905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae47e754356b145ac3883025be70df81397e012b7b9deea79c6e1549cebb820`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723fe97584e549852ab448538bb35f45d46da4b09c52e18fa4eeec5352c47a42`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5f2dacb5179622644f1e47531960f1fa5aef816fb60aad38a20349103c7191`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 103.8 KB (103828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef494bb92067167934aab739f7d1f023f4e34ef112f973afc201b98e54fa5d50`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 954.6 KB (954617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd803b6c0eb021a0b33649dd96256f867eac7aa91b9255624ed7f239c9475ff`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1c222c9d9e5ee0e2e34c4386e9c09b7ebf79a12072e245332f295c63bddf3e`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:2dd815e2d1643bcba94e92c59e4c260f02bf06b0ff954840272439de861358f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 KB (103568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0885c1305da890646b6ad6dbcd2ae57932bcd2d1b804dc7404de2cd8713cc284`

```dockerfile
```

-	Layers:
	-	`sha256:6e6853da7f25eec4b641df434dccd72f8d65a0a540787c715049bd366d0f787b`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 84.3 KB (84267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b7bd473fc9187722cabb9a96acad9c5a1dbb88c26431928b2166223fb0dee7c`  
		Last Modified: Mon, 03 Jun 2024 19:03:38 GMT  
		Size: 19.3 KB (19301 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:e0688d9873a4cf749f89b43548d03f7d6c873596b1495b6da6943d4a3e767df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5166898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6a1a46a5867d6ecd3c9bf99a695a89cc1f746f59d3a9a140b85a42b99a2e26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_VERSION=1.6.27
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 22 May 2024 18:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:54:12 GMT
USER memcache
# Wed, 22 May 2024 18:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 May 2024 18:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024a9ccd1af8ffcfe453e22adead9362703e916c9dec4f1d4e94b597e660f23e`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab592fa6ce63bf6772b1c208275d773ef6e671af73b2bd119e98de86dce4fc1`  
		Last Modified: Thu, 23 May 2024 06:29:58 GMT  
		Size: 121.0 KB (121017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd20d288c43aabf4d5e06a885b2e2f24583aae8e102eca2bf9257ce5e307a2cd`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 957.7 KB (957743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d039a0fcb8c2c4f062cb3fb5c2b20ae16915479721254aadfc68d0319c84ee25`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cf5bc5246a4e40149d2a6b161c9fbce8354373e305c03088715546070c2742`  
		Last Modified: Thu, 23 May 2024 06:29:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:ec1932014529a81f308cae2db47073ddf344ef48cbc77766d95510cb7385b2af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 KB (103606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0d85c8cad5520d9245c1563457fcf55da9b744f736c305ad21fad10027e013`

```dockerfile
```

-	Layers:
	-	`sha256:f77bdac9710cd22ef4eb7ba293b1b4fe4736e109a3767950432991fe0237fa54`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 84.3 KB (84287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12016cd6764c2821a23d0e8fb3c182eda4d12d096e83cf52f57eb0103616d5e8`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 19.3 KB (19319 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.20` - linux; 386

```console
$ docker pull memcached@sha256:d021aa4701a1cbf3afb535aa82cd88bc0f7c5d51c05c34d5160fabd876a5bce7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d85661f9f9c582ffadd4540ae1b2fb7bf653da454d36eab21d69ed0aa33ddb7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:05:50 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 18:05:51 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77c9b09b82af8bb67811ab3d796c64874348624abc7cf7658894f3042e3fdda`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61451eaaecf42ca95101dad4ed37d00cf792b8afae1d5eeab46e43e258b3ef4`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 109.0 KB (108954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1cfe9a7dc0eb6422fdd3e24036097ac92ebb3781776994ac1a1985641b7746a`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 947.9 KB (947940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffa1b620c706dc7fccfe69ac07a840b285472eebf3a5b12f4627f73b14a8262`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3107d914479457d4f68098546010a68c957c8958f8617fe612a4de36890751d`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:f7757ea9df5138c45bdbcd9e258bd5f8d3b847272ba419799988079f669fbe74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 KB (103468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f14b161d58134f0ae5adc6bf8b94c753848d136ed143b505c68fd6d0083ef5e`

```dockerfile
```

-	Layers:
	-	`sha256:977ffaf9dabb1b3eba7edd08c3c73174de9a29484b0f80d86a81072bb317517f`  
		Last Modified: Mon, 03 Jun 2024 19:03:51 GMT  
		Size: 84.2 KB (84222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d4314a7e1c917ad745b623d3c1ea185133876babcee74b1048a636196ae0e48`  
		Last Modified: Mon, 03 Jun 2024 19:03:50 GMT  
		Size: 19.2 KB (19246 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.20` - linux; ppc64le

```console
$ docker pull memcached@sha256:0b9a2b083716079e6c1da7a9eef4cda25b8d81f3e16840ca6b2b12e9d90e00b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c5555e7ff1014a88296e46cd6d51b379698f7678f76fcd835e8c9f30d647d79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f168e15e72e8585ac6cf20d04f29cfeea15135f34178693fec86adfd88204d`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e2f6d65a966b68fa13bdc24e920a1a1fa7b86b2e000d17eff60efbfdd38993`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 123.0 KB (123004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5864e6eb973cda0b80fc0b600b8fdc61cab246b23ff08158ec77e3c819aacb99`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 992.9 KB (992907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af9bfa929a4b7886285f34b50a2506270b5db318f414db5cfa7c505e069495e`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf6c5b09507827cb18669a5979a2e3e258baa20df3c7d3b1790c8e47c4da755`  
		Last Modified: Mon, 03 Jun 2024 19:53:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:47e12d8b1103b819e814e52b644a34f6fd25e9b3c301cf64bd3a5aed59882a32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 KB (101740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac2cf30c8b57070d3d517da1a03e3bf9241f943b85fa56a7a7cafcec23db720f`

```dockerfile
```

-	Layers:
	-	`sha256:bf26f6e69d9a08fc6932c97112ad23a6a9b487855c46d9d7e0c8bddd8b5292f2`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 82.4 KB (82371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:018afee57a818e12505b2c4851b768103c8b30b0796588e3def21bb1bb3e7d24`  
		Last Modified: Mon, 03 Jun 2024 19:53:40 GMT  
		Size: 19.4 KB (19369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.20` - linux; s390x

```console
$ docker pull memcached@sha256:c9d716888f3de4b62fcb97a29f86e58ace3ecd27d3e140bf093a91a55b457895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4551732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98e758f93cfeb8699e726a62495bbcb588c84eb23144c8f4fef5e84556142be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b951b4f532c41c7412daf128075fc9cd89c182acbc79418cb89d9bdcca3f7f5`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ace4ff1604d5e2114f279c4a7dbd9c7255f5c22442459e1dde1e1dba3c3662`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 112.7 KB (112734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3635c0cf5ff89eaa5a72c24ee555909e50ee12d3629572ef94a113391f5b0e92`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 977.3 KB (977292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e93a0ef4a20f636cd8f486379f0e8926c809875d1be02f187e1d9beb0155870`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2e88b16dd19768ead777afafdc9ec27072ab209e2f240c51dce37ce1590302`  
		Last Modified: Mon, 03 Jun 2024 19:44:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:7e094c1f57f2f2a6a9f5e6290afe42f796d0444a80835660c23f0880808b9fac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 KB (101612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22673137bae204447eabe141346d72e57cec6908c114a55f94494e572a484849`

```dockerfile
```

-	Layers:
	-	`sha256:245be0555de7893afdeab5ba2e974bc77e29549c40a4bdb62d8b49cdd98938c8`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 82.3 KB (82313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41c84b152f2dcb64eb163c14efbbe0d430a1cd597e9fe2a74c52c447568f2d9f`  
		Last Modified: Mon, 03 Jun 2024 19:44:21 GMT  
		Size: 19.3 KB (19299 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:bookworm`

```console
$ docker pull memcached@sha256:6bc6193233fb86bb8deaf6706445bd3e55b1e786bbea8c642bb42462e0d5fa9b
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
$ docker pull memcached@sha256:9147945260ea3aae4982858f21c236318a3f6e714e3247c5baf29a5a72e0f541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32898057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23286975f91428ab86b108f596c0340aed9fc99015d547119acc7f7aaf10007e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc543897dce5b0ec373146149c07d4d311f530d35fd5660eacf896059d19c1f9`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67696248863aa6bf5473db03626425b13368fab900b2145458a0aadf3ec50685`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 2.5 MB (2488532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1225c54544336958562027d237b24c6e6fdf0242b27fedb8de59463271161a`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 1.3 MB (1257596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c8c669390569241c531942ed6c73e9ed972acd0d553620dc73b27efd017da4`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750d4cc56720b2b3726c433153484ee8befc8ef867db54c4ea893932042208b4`  
		Last Modified: Mon, 03 Jun 2024 19:03:49 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:16ed0d681048581dce561ae4090acbdcf920ce1f2ddce248215521ed4fd9decd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d6ffeaf490e2efb6c46e0c490e1c11020fcf721e84a6b2d8edef168a450b00`

```dockerfile
```

-	Layers:
	-	`sha256:7055f894d5826460bb2eb3ea9b0ef5d51df1ce6b1c073f786f5d1cf92573a368`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 2.3 MB (2261260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1e66ce28cc0bd263cb0b4aa93ffcc60f78c1c750f403cbd3ab265a6794fc167`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 21.0 KB (20979 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:14753c4e01088e08a436d89d02a2a78902028bf49d6db1569f475092fd460bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30237639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c21e319ac699c14e10d279852e999e826acf2731ee4b72c4c10a33bb47692f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 00:48:34 GMT
ADD file:ee9f1914c7fc370bdb089c9e2fcfa15477f7091fc5437cb780232afdf6297586 in / 
# Tue, 14 May 2024 00:48:34 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:169fcae2368e5a601c42972560f091e123648fa0e741975d1b35900c61b9ff71`  
		Last Modified: Tue, 14 May 2024 00:51:36 GMT  
		Size: 26.9 MB (26909921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6135c82883bf5f0df15a6d3d42e97b6013681d12f1f0d535ccb0c1cacf6676b`  
		Last Modified: Mon, 03 Jun 2024 19:08:33 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51f9357aee8294bc0ab883e4493123d2a4dabd21e30ab2900da6cfe6fce5b20`  
		Last Modified: Mon, 03 Jun 2024 19:08:34 GMT  
		Size: 2.1 MB (2089512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32e18a9983de65ed92d9394655a09d3d69089e493a069562641ea42c679e1a4`  
		Last Modified: Mon, 03 Jun 2024 19:08:34 GMT  
		Size: 1.2 MB (1236688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc76114b0bb29114c4b5ff03c2b92a6a317377e26442ec0b79e0016bdc73147d`  
		Last Modified: Mon, 03 Jun 2024 19:08:33 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c636887432e5986c55e92368eef61a43bd3e05cd00609197541f460647ef8208`  
		Last Modified: Mon, 03 Jun 2024 19:08:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:3db3baea327d4e01491ca8527e9a966a8bc9c6fb518a0f2850e7418c158eb8f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84af36590abfbf847e39461d5668a9b85b5846ab2c1705bdf2e8858807e9d86c`

```dockerfile
```

-	Layers:
	-	`sha256:aaab43908073c0eddfc13729d70514a3426255ff8d31aa19aa39108390f5c65d`  
		Last Modified: Mon, 03 Jun 2024 19:08:34 GMT  
		Size: 2.3 MB (2264548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6af6c6fa69438301c0c320846677e25900a5aa269506c074071536e7fdc092ff`  
		Last Modified: Mon, 03 Jun 2024 19:08:33 GMT  
		Size: 21.1 KB (21120 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b953ca66ecee777524a0f33f0adefbe99183367e180f4b2ed82d1e525f57d208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32780663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a9c7e97a66ca554c0cfc88de871b1c7dfad7637ffcbd6a79b5c75b3954bb583`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
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
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994933505bafbbaba95cef494f2dfb3e85f2bfde1ea5c4a6dae5a179e39e7b5c`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9488359f89f8c6691f1737ce76ce6b7520511a8246658953dae9429090e88746`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 2.3 MB (2346183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fa925bb96d2305b22651dc4d10899309c212aef95cb13afbdeb2ba5436cb0b`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 1.3 MB (1253469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5284a06f3ca2503602cf214d936daf8aedee3d442d7aa66a5b67874c8f156685`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a475f5b1bcd9a980f0e2923bf1af87002c6468529583ce41a151599d11b2cc`  
		Last Modified: Tue, 14 May 2024 17:41:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:303a74af5e224338560198dc50e2c9cb2a7b4a46b01d39144559de1dd7788518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e79fb901bf217f30113856b6b39e296324993066435904abd2a2152baae6156`

```dockerfile
```

-	Layers:
	-	`sha256:a35747f1af90484d4a9021de5c31be89cb3117cb5f56f499d3cebe78562716cf`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 2.3 MB (2261490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48c7060af35b31db7e804b3ce19451726c3fb6b956edad221ee58000cf04a91`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 21.0 KB (20997 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; 386

```console
$ docker pull memcached@sha256:36e236fc6b16e7e3170743b8c6a4fbaa296f4d7804c6c2b2106171eac49c9e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33915077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46c7f4bc09921dd239f3c7eb02f4989d48a1df441f3bc33fa1eac70860b0ae6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 00:47:12 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Tue, 14 May 2024 00:47:12 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb23370f3994993b447e434bb257c1618064ae75acb7e15d1fb88d95c481416`  
		Last Modified: Mon, 03 Jun 2024 19:03:52 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43508bc095d4cad435f08c64c32dd8056399b25cddfeca86964d15f117cbd0c`  
		Last Modified: Mon, 03 Jun 2024 19:03:52 GMT  
		Size: 2.5 MB (2492668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2870f8c3ee5b47d7a6a8e194db84b04de521e6a228093ad33b4252661ee3d0d0`  
		Last Modified: Mon, 03 Jun 2024 19:03:52 GMT  
		Size: 1.3 MB (1258253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c83af100d615d1363ef33866755b85f6153e23f56a4e9c1a6cba13d0463082d`  
		Last Modified: Mon, 03 Jun 2024 19:03:53 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ec3bf8bf691991f57de6b00811ed6d06fe0417f1955d1d7b6cd33ecf81b406`  
		Last Modified: Mon, 03 Jun 2024 19:03:53 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:443d7accdadab953db276145a1ab012f3232c120ea362461be5a22531600dca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da086c82559c925e7fcc2b0c79e47076545d92a837f0e4d1b8f49b66cfb55fc0`

```dockerfile
```

-	Layers:
	-	`sha256:829f8d9a7d33b902a3c59de1e19bd0291df3704cf233de30580da78a72c5220f`  
		Last Modified: Mon, 03 Jun 2024 19:03:52 GMT  
		Size: 2.3 MB (2258358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffb9dd39ce17614aed4cd4f0bac42e7b8bb49b726b85d39d48b1700119a54cf0`  
		Last Modified: Mon, 03 Jun 2024 19:03:52 GMT  
		Size: 20.9 KB (20924 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:129ad612a59e558c3da7dfa1a1958d7b374599149ad2ac085bfd539341b0e76d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32335816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4ee8bdf9b447076bff1edf5bfe8aafd428b9e3a1c11745e3eac190a7957b50d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 01:11:07 GMT
ADD file:a92da94a28279478b2eae11dcdcd2913fc06af02498a5515cc3f288668d74e43 in / 
# Tue, 14 May 2024 01:11:12 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6ccc6628d3cdcda935b3b60cb54fa578d669965454d9cf39de3df9c1276132b7`  
		Last Modified: Tue, 14 May 2024 01:22:19 GMT  
		Size: 29.1 MB (29143688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2c2342dfc8d9203635e3e3bc46109d12ef7ef9940adb0794934bca415e4d79`  
		Last Modified: Mon, 03 Jun 2024 19:52:36 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba60c707dc72485dffcb0f586703d60083e3a99568905fc77c61a927aa023133`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 1.9 MB (1937709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5d0dde6405cfccdcc1ece97791b0c134d743d3dbbb4648cfd8ffa51f7fa7fa`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 1.3 MB (1252902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c5806cc8f133288ec076e5d9a6d04f2f7528380144d22892c7b84314c99a8c`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198d6a5f4cd3ba446c2120eb2826773388a541360046c35203d6024dce60a143`  
		Last Modified: Mon, 03 Jun 2024 19:52:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:bf5993b43a4118f01f52ac8a194cb102c52ee5b81fe6f6217d77ca4afaef2a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295c96051f2df83e45a2fe340023dd1e664fdec31e7ef871ca8d797cbc594205`

```dockerfile
```

-	Layers:
	-	`sha256:396ed31b018a1dc19cc7f9fcd8bc9c31f7d68c64735199594c25d0801926c1b7`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:63978abc93d511e5c74a4cc84e7b57a1d767833ba0c69e02c29365668c96bf86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37163958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9054e0ed4fdeb443fcae69bad304d1e19e2434684bbca08c83f5ef5897d1e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 01:20:02 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Tue, 14 May 2024 01:20:04 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:11ee2a6dbc4a6a6b182097f6023f775e595488a6bcc424e9b58001659deb7fa1`  
		Last Modified: Tue, 14 May 2024 01:24:06 GMT  
		Size: 33.1 MB (33141160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d531128e0fac13a6c4e8656afa2e85afbd55db7a786a38bf715c14f4e05a5d94`  
		Last Modified: Mon, 03 Jun 2024 19:50:52 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037940292acc903c706efafe81e090f3eca4683a90304378efe5f4b2cd3cbd47`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 2.7 MB (2698394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d2e0144b8349ea33bdc906d060868aa61958e0c45ac421dcf26a5fc15eb677`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 1.3 MB (1322885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02930e85eb728b1b92f67233fa0c4ff46787e43e4c5f78933df1a64f4c1f7ad0`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cb49628af48f1c1c75566128625afdacca39df7ea0a7c2762ff858d5a3c3e9`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:eae1092d4dd48c0f18e3eda2c5440fe8988dc3823060e738b93a20fba09baf54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea636723fe65c22cb491ee51203b6349d5302ba3288e8ebf7395457c83a78a3`

```dockerfile
```

-	Layers:
	-	`sha256:0c88ae099fbb77c9cefb907169eb358536ff37e4c35140a81c2cb67411da7a9f`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 2.3 MB (2265631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba09bde198a5df307f36fa75f66fe410b324cf250153ce67c8d2f7e9def7d0e5`  
		Last Modified: Mon, 03 Jun 2024 19:50:52 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:da94175eec280d37f0dfd2d8acdc57bd8b4607f66f738dd796b0719c28737986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30903401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf7fe752edb4161d9cd43825ddd58ceff332eb34c41dcc9623255e4cc9bf376`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 00:42:38 GMT
ADD file:55fef93bbad6701fe968a070a0c72b3a0bd3df408dd79c9a616a43dea0de11d0 in / 
# Tue, 14 May 2024 00:42:40 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d7365433874e83ccc92aa5d768989641a64e23c3247409161401a09b4895c406`  
		Last Modified: Tue, 14 May 2024 00:47:35 GMT  
		Size: 27.5 MB (27512398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422d2a0f87a8b8c2712bf0d473e4f936bcbad2af462760d8ae88a25a4ddcbabe`  
		Last Modified: Mon, 03 Jun 2024 19:40:44 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dac9575eb2b0b2d47b6c792dddf0edd2afdeaad0f5dc8a1572996977ceb0fa6`  
		Last Modified: Mon, 03 Jun 2024 19:40:44 GMT  
		Size: 2.2 MB (2152694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e3eb594a178112f9ea3d30d498b8b619b5165ff992e96e66a2cb723b708eea`  
		Last Modified: Mon, 03 Jun 2024 19:40:44 GMT  
		Size: 1.2 MB (1236790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f6ebc8f32f01f7f87e92d446e389a62516dcde1dd8b66b0ed80618c1279d7f`  
		Last Modified: Mon, 03 Jun 2024 19:40:45 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b1370c7b0f96a4cb325b9cd27e7cc508def3a755eaf10f7f2893a6d721d6b6`  
		Last Modified: Mon, 03 Jun 2024 19:40:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:b7e29c218845ad20177e6072bafe8ceb34957f028c9ab5dc784bf0d8abb3266b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:801c05520a31b4c181fcea7491e35a45441ce8b7d97f9f1133ce0da9982b9f65`

```dockerfile
```

-	Layers:
	-	`sha256:7059681ccb9077ae5d5d066a76afbdf315e577e6f6185513b43dc17567fd6a41`  
		Last Modified: Mon, 03 Jun 2024 19:40:44 GMT  
		Size: 2.3 MB (2261081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d33b5d8c8737f3f638401087329e3541977c1b45f846a92a33f44bc802633636`  
		Last Modified: Mon, 03 Jun 2024 19:40:44 GMT  
		Size: 21.0 KB (20979 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:latest`

```console
$ docker pull memcached@sha256:6bc6193233fb86bb8deaf6706445bd3e55b1e786bbea8c642bb42462e0d5fa9b
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
$ docker pull memcached@sha256:9147945260ea3aae4982858f21c236318a3f6e714e3247c5baf29a5a72e0f541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32898057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23286975f91428ab86b108f596c0340aed9fc99015d547119acc7f7aaf10007e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc543897dce5b0ec373146149c07d4d311f530d35fd5660eacf896059d19c1f9`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67696248863aa6bf5473db03626425b13368fab900b2145458a0aadf3ec50685`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 2.5 MB (2488532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1225c54544336958562027d237b24c6e6fdf0242b27fedb8de59463271161a`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 1.3 MB (1257596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c8c669390569241c531942ed6c73e9ed972acd0d553620dc73b27efd017da4`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750d4cc56720b2b3726c433153484ee8befc8ef867db54c4ea893932042208b4`  
		Last Modified: Mon, 03 Jun 2024 19:03:49 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:16ed0d681048581dce561ae4090acbdcf920ce1f2ddce248215521ed4fd9decd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d6ffeaf490e2efb6c46e0c490e1c11020fcf721e84a6b2d8edef168a450b00`

```dockerfile
```

-	Layers:
	-	`sha256:7055f894d5826460bb2eb3ea9b0ef5d51df1ce6b1c073f786f5d1cf92573a368`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 2.3 MB (2261260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1e66ce28cc0bd263cb0b4aa93ffcc60f78c1c750f403cbd3ab265a6794fc167`  
		Last Modified: Mon, 03 Jun 2024 19:03:48 GMT  
		Size: 21.0 KB (20979 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:14753c4e01088e08a436d89d02a2a78902028bf49d6db1569f475092fd460bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30237639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c21e319ac699c14e10d279852e999e826acf2731ee4b72c4c10a33bb47692f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 00:48:34 GMT
ADD file:ee9f1914c7fc370bdb089c9e2fcfa15477f7091fc5437cb780232afdf6297586 in / 
# Tue, 14 May 2024 00:48:34 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:169fcae2368e5a601c42972560f091e123648fa0e741975d1b35900c61b9ff71`  
		Last Modified: Tue, 14 May 2024 00:51:36 GMT  
		Size: 26.9 MB (26909921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6135c82883bf5f0df15a6d3d42e97b6013681d12f1f0d535ccb0c1cacf6676b`  
		Last Modified: Mon, 03 Jun 2024 19:08:33 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51f9357aee8294bc0ab883e4493123d2a4dabd21e30ab2900da6cfe6fce5b20`  
		Last Modified: Mon, 03 Jun 2024 19:08:34 GMT  
		Size: 2.1 MB (2089512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32e18a9983de65ed92d9394655a09d3d69089e493a069562641ea42c679e1a4`  
		Last Modified: Mon, 03 Jun 2024 19:08:34 GMT  
		Size: 1.2 MB (1236688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc76114b0bb29114c4b5ff03c2b92a6a317377e26442ec0b79e0016bdc73147d`  
		Last Modified: Mon, 03 Jun 2024 19:08:33 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c636887432e5986c55e92368eef61a43bd3e05cd00609197541f460647ef8208`  
		Last Modified: Mon, 03 Jun 2024 19:08:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:3db3baea327d4e01491ca8527e9a966a8bc9c6fb518a0f2850e7418c158eb8f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84af36590abfbf847e39461d5668a9b85b5846ab2c1705bdf2e8858807e9d86c`

```dockerfile
```

-	Layers:
	-	`sha256:aaab43908073c0eddfc13729d70514a3426255ff8d31aa19aa39108390f5c65d`  
		Last Modified: Mon, 03 Jun 2024 19:08:34 GMT  
		Size: 2.3 MB (2264548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6af6c6fa69438301c0c320846677e25900a5aa269506c074071536e7fdc092ff`  
		Last Modified: Mon, 03 Jun 2024 19:08:33 GMT  
		Size: 21.1 KB (21120 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b953ca66ecee777524a0f33f0adefbe99183367e180f4b2ed82d1e525f57d208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32780663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a9c7e97a66ca554c0cfc88de871b1c7dfad7637ffcbd6a79b5c75b3954bb583`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
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
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994933505bafbbaba95cef494f2dfb3e85f2bfde1ea5c4a6dae5a179e39e7b5c`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9488359f89f8c6691f1737ce76ce6b7520511a8246658953dae9429090e88746`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 2.3 MB (2346183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fa925bb96d2305b22651dc4d10899309c212aef95cb13afbdeb2ba5436cb0b`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 1.3 MB (1253469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5284a06f3ca2503602cf214d936daf8aedee3d442d7aa66a5b67874c8f156685`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a475f5b1bcd9a980f0e2923bf1af87002c6468529583ce41a151599d11b2cc`  
		Last Modified: Tue, 14 May 2024 17:41:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:303a74af5e224338560198dc50e2c9cb2a7b4a46b01d39144559de1dd7788518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e79fb901bf217f30113856b6b39e296324993066435904abd2a2152baae6156`

```dockerfile
```

-	Layers:
	-	`sha256:a35747f1af90484d4a9021de5c31be89cb3117cb5f56f499d3cebe78562716cf`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 2.3 MB (2261490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48c7060af35b31db7e804b3ce19451726c3fb6b956edad221ee58000cf04a91`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 21.0 KB (20997 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:36e236fc6b16e7e3170743b8c6a4fbaa296f4d7804c6c2b2106171eac49c9e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33915077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46c7f4bc09921dd239f3c7eb02f4989d48a1df441f3bc33fa1eac70860b0ae6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 00:47:12 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Tue, 14 May 2024 00:47:12 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb23370f3994993b447e434bb257c1618064ae75acb7e15d1fb88d95c481416`  
		Last Modified: Mon, 03 Jun 2024 19:03:52 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43508bc095d4cad435f08c64c32dd8056399b25cddfeca86964d15f117cbd0c`  
		Last Modified: Mon, 03 Jun 2024 19:03:52 GMT  
		Size: 2.5 MB (2492668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2870f8c3ee5b47d7a6a8e194db84b04de521e6a228093ad33b4252661ee3d0d0`  
		Last Modified: Mon, 03 Jun 2024 19:03:52 GMT  
		Size: 1.3 MB (1258253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c83af100d615d1363ef33866755b85f6153e23f56a4e9c1a6cba13d0463082d`  
		Last Modified: Mon, 03 Jun 2024 19:03:53 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ec3bf8bf691991f57de6b00811ed6d06fe0417f1955d1d7b6cd33ecf81b406`  
		Last Modified: Mon, 03 Jun 2024 19:03:53 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:443d7accdadab953db276145a1ab012f3232c120ea362461be5a22531600dca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da086c82559c925e7fcc2b0c79e47076545d92a837f0e4d1b8f49b66cfb55fc0`

```dockerfile
```

-	Layers:
	-	`sha256:829f8d9a7d33b902a3c59de1e19bd0291df3704cf233de30580da78a72c5220f`  
		Last Modified: Mon, 03 Jun 2024 19:03:52 GMT  
		Size: 2.3 MB (2258358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffb9dd39ce17614aed4cd4f0bac42e7b8bb49b726b85d39d48b1700119a54cf0`  
		Last Modified: Mon, 03 Jun 2024 19:03:52 GMT  
		Size: 20.9 KB (20924 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; mips64le

```console
$ docker pull memcached@sha256:129ad612a59e558c3da7dfa1a1958d7b374599149ad2ac085bfd539341b0e76d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32335816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4ee8bdf9b447076bff1edf5bfe8aafd428b9e3a1c11745e3eac190a7957b50d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 01:11:07 GMT
ADD file:a92da94a28279478b2eae11dcdcd2913fc06af02498a5515cc3f288668d74e43 in / 
# Tue, 14 May 2024 01:11:12 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6ccc6628d3cdcda935b3b60cb54fa578d669965454d9cf39de3df9c1276132b7`  
		Last Modified: Tue, 14 May 2024 01:22:19 GMT  
		Size: 29.1 MB (29143688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2c2342dfc8d9203635e3e3bc46109d12ef7ef9940adb0794934bca415e4d79`  
		Last Modified: Mon, 03 Jun 2024 19:52:36 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba60c707dc72485dffcb0f586703d60083e3a99568905fc77c61a927aa023133`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 1.9 MB (1937709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5d0dde6405cfccdcc1ece97791b0c134d743d3dbbb4648cfd8ffa51f7fa7fa`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 1.3 MB (1252902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c5806cc8f133288ec076e5d9a6d04f2f7528380144d22892c7b84314c99a8c`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198d6a5f4cd3ba446c2120eb2826773388a541360046c35203d6024dce60a143`  
		Last Modified: Mon, 03 Jun 2024 19:52:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:bf5993b43a4118f01f52ac8a194cb102c52ee5b81fe6f6217d77ca4afaef2a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295c96051f2df83e45a2fe340023dd1e664fdec31e7ef871ca8d797cbc594205`

```dockerfile
```

-	Layers:
	-	`sha256:396ed31b018a1dc19cc7f9fcd8bc9c31f7d68c64735199594c25d0801926c1b7`  
		Last Modified: Mon, 03 Jun 2024 19:52:37 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:63978abc93d511e5c74a4cc84e7b57a1d767833ba0c69e02c29365668c96bf86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37163958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9054e0ed4fdeb443fcae69bad304d1e19e2434684bbca08c83f5ef5897d1e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 01:20:02 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Tue, 14 May 2024 01:20:04 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:11ee2a6dbc4a6a6b182097f6023f775e595488a6bcc424e9b58001659deb7fa1`  
		Last Modified: Tue, 14 May 2024 01:24:06 GMT  
		Size: 33.1 MB (33141160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d531128e0fac13a6c4e8656afa2e85afbd55db7a786a38bf715c14f4e05a5d94`  
		Last Modified: Mon, 03 Jun 2024 19:50:52 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037940292acc903c706efafe81e090f3eca4683a90304378efe5f4b2cd3cbd47`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 2.7 MB (2698394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d2e0144b8349ea33bdc906d060868aa61958e0c45ac421dcf26a5fc15eb677`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 1.3 MB (1322885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02930e85eb728b1b92f67233fa0c4ff46787e43e4c5f78933df1a64f4c1f7ad0`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cb49628af48f1c1c75566128625afdacca39df7ea0a7c2762ff858d5a3c3e9`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:eae1092d4dd48c0f18e3eda2c5440fe8988dc3823060e738b93a20fba09baf54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea636723fe65c22cb491ee51203b6349d5302ba3288e8ebf7395457c83a78a3`

```dockerfile
```

-	Layers:
	-	`sha256:0c88ae099fbb77c9cefb907169eb358536ff37e4c35140a81c2cb67411da7a9f`  
		Last Modified: Mon, 03 Jun 2024 19:50:53 GMT  
		Size: 2.3 MB (2265631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba09bde198a5df307f36fa75f66fe410b324cf250153ce67c8d2f7e9def7d0e5`  
		Last Modified: Mon, 03 Jun 2024 19:50:52 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:da94175eec280d37f0dfd2d8acdc57bd8b4607f66f738dd796b0719c28737986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30903401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf7fe752edb4161d9cd43825ddd58ceff332eb34c41dcc9623255e4cc9bf376`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 14 May 2024 00:42:38 GMT
ADD file:55fef93bbad6701fe968a070a0c72b3a0bd3df408dd79c9a616a43dea0de11d0 in / 
# Tue, 14 May 2024 00:42:40 GMT
CMD ["bash"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d7365433874e83ccc92aa5d768989641a64e23c3247409161401a09b4895c406`  
		Last Modified: Tue, 14 May 2024 00:47:35 GMT  
		Size: 27.5 MB (27512398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422d2a0f87a8b8c2712bf0d473e4f936bcbad2af462760d8ae88a25a4ddcbabe`  
		Last Modified: Mon, 03 Jun 2024 19:40:44 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dac9575eb2b0b2d47b6c792dddf0edd2afdeaad0f5dc8a1572996977ceb0fa6`  
		Last Modified: Mon, 03 Jun 2024 19:40:44 GMT  
		Size: 2.2 MB (2152694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e3eb594a178112f9ea3d30d498b8b619b5165ff992e96e66a2cb723b708eea`  
		Last Modified: Mon, 03 Jun 2024 19:40:44 GMT  
		Size: 1.2 MB (1236790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f6ebc8f32f01f7f87e92d446e389a62516dcde1dd8b66b0ed80618c1279d7f`  
		Last Modified: Mon, 03 Jun 2024 19:40:45 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b1370c7b0f96a4cb325b9cd27e7cc508def3a755eaf10f7f2893a6d721d6b6`  
		Last Modified: Mon, 03 Jun 2024 19:40:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:b7e29c218845ad20177e6072bafe8ceb34957f028c9ab5dc784bf0d8abb3266b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:801c05520a31b4c181fcea7491e35a45441ce8b7d97f9f1133ce0da9982b9f65`

```dockerfile
```

-	Layers:
	-	`sha256:7059681ccb9077ae5d5d066a76afbdf315e577e6f6185513b43dc17567fd6a41`  
		Last Modified: Mon, 03 Jun 2024 19:40:44 GMT  
		Size: 2.3 MB (2261081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d33b5d8c8737f3f638401087329e3541977c1b45f846a92a33f44bc802633636`  
		Last Modified: Mon, 03 Jun 2024 19:40:44 GMT  
		Size: 21.0 KB (20979 bytes)  
		MIME: application/vnd.in-toto+json
