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
-	[`memcached:1.6.33`](#memcached1633)
-	[`memcached:1.6.33-alpine`](#memcached1633-alpine)
-	[`memcached:1.6.33-alpine3.20`](#memcached1633-alpine320)
-	[`memcached:1.6.33-bookworm`](#memcached1633-bookworm)
-	[`memcached:alpine`](#memcachedalpine)
-	[`memcached:alpine3.20`](#memcachedalpine320)
-	[`memcached:bookworm`](#memcachedbookworm)
-	[`memcached:latest`](#memcachedlatest)

## `memcached:1`

```console
$ docker pull memcached@sha256:b8cb0ed0bf5d3d38f9606fc847c9a21baa68952472ea29a5a685f82a1efc2987
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
$ docker pull memcached@sha256:1e2854f49ddb3fc0103bf7b8fcd80ed47c6f72e2aa74ad0848acc1274e4f98f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31984433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04abd86d309da60dfe2b7f4f4e20226dd5f87fe17482740074bbc2c6865d6987`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977f47ceef0f8173cff02fe737b3fd37efab540ec727c2a20869e90ab8279920`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1599032aa7639a9095e216c0b122c7eb2cf54392a6e7bf2d191ff3e086bb478a`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 2.5 MB (2491759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:034904c659cc08a9f86d31858f173bfc3a20727cb5fb51319eb9478c29151562`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 1.3 MB (1259579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbc04f1662c41c4314f0f2a27cbf319464d441170360aee7702dd51be327e76`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4e9ce09f9de3f7835981235d8000bd031663f2328a8e4ffb2f6b6e9d1a1e0d`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:fb6b716e55ea5a7353f965101017052ad92d603abfbd05eb49dc5aeceea69dfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2312843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2806c278d65e027e6b4619f466776331a5efde1eb1992a4a013a5e85ae769111`

```dockerfile
```

-	Layers:
	-	`sha256:a489ae83eb749729e07a801603bdc10563b8508b7272d035a9f58304ea805e5c`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 2.3 MB (2291621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbb57e1ba346b719e10354837a9bef89546f505a248a0977af44ec554c92262a`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v5

```console
$ docker pull memcached@sha256:91ab868f687f5d84ed97501641c6276629ba558cf3b893411d4bff8ddf3b7a20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29090498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddac0a9030226a9353757b40367ccad4e58abf3df5f1cecab9445504a7141a50`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:25d432086d20067bebfff2b163f22d49e7da8528782652615fe170bf8c39194d`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 25.8 MB (25754926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29864ebc65411065e6cc80afcb839ecd53357c5d8accb084195a861ffe331f0c`  
		Last Modified: Tue, 03 Dec 2024 02:34:22 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17b8bb45df912fe349545bf67aeee395da8a6bbd8c9fd4b4bba4ab37d4c46e6`  
		Last Modified: Tue, 03 Dec 2024 02:34:23 GMT  
		Size: 2.1 MB (2096040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f971acf6335510d8cd95bbf08ed1b82d5ccdbb6a46d5cc4004f4d3f17f79ad22`  
		Last Modified: Fri, 06 Dec 2024 01:31:23 GMT  
		Size: 1.2 MB (1238020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d2f4b78825fe502c36e4f1340340617bc5d281e1a4d0bfd9c29b683505190d`  
		Last Modified: Fri, 06 Dec 2024 01:31:23 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0b278088431fe97844cee08594eb17b8a478179969a38c2138afcc8635209b`  
		Last Modified: Fri, 06 Dec 2024 01:31:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:33b0db124591dec0a6fd5c81068992c08e8cb9a2f4e0f7c8dd8474b34525c0f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2316527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59492fefec6386be99693d0d6d513a6c53fd5cc3e197beb39bcce988752d934b`

```dockerfile
```

-	Layers:
	-	`sha256:3183c33c304bb139731b8181094f3cedf637a75d2c2b46a39117b249bcbf9a94`  
		Last Modified: Fri, 06 Dec 2024 01:31:23 GMT  
		Size: 2.3 MB (2295158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe9afff481d34963c12864f80d0a8758b8462fbfbdf815070d7b572ba117476b`  
		Last Modified: Fri, 06 Dec 2024 01:31:23 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:4b50248c9ebc50990818eb60f6c506e07a29315de1cf92f8089ce198db55f78f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31670277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae090e1fc19e90d2a650cdd682ddd6cebff3ef4c472411c422c7b772f9c7844a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78a410ea91650a45f4516634a8253fbca2d2238ebd376ee434a91c97add0d41`  
		Last Modified: Tue, 03 Dec 2024 02:56:13 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3651f43c686dcae90b2bb5bfaafb1c1e92231bce87f7c2a4f7f92606b3f6048`  
		Last Modified: Tue, 03 Dec 2024 02:56:14 GMT  
		Size: 2.4 MB (2355349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1974b3b5f9215ed5e7c38499590f73f9d2cc9f0eab4b5bfc835e795f011b6ec`  
		Last Modified: Fri, 06 Dec 2024 01:31:13 GMT  
		Size: 1.3 MB (1254605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0d87f19f5dcc124861cef54d5060fdddf78285679e5e18c5c228a649873178`  
		Last Modified: Fri, 06 Dec 2024 01:31:12 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4e9ce09f9de3f7835981235d8000bd031663f2328a8e4ffb2f6b6e9d1a1e0d`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:65ec047e972b106c4dccd5e7db2375b427183eaa0a17d24a87733f0781a6f4cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2313354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6be2bd8ba74100235eb2a7790cd07be00c97e00f811e0074913d8ef6bce12587`

```dockerfile
```

-	Layers:
	-	`sha256:aea7e31a5ac097dbe2c1f459e15d324e0b4c270652bc090fc7bb75b32d29171f`  
		Last Modified: Fri, 06 Dec 2024 01:31:13 GMT  
		Size: 2.3 MB (2291935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72554d4560a983cd304f173578e432f68442018a3d2f900c20e8692c7507475d`  
		Last Modified: Fri, 06 Dec 2024 01:31:12 GMT  
		Size: 21.4 KB (21419 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:2ee1837e5180933d5ce36c27a48671480a1269845d9fe11427b429f7ddcb89e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32967293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa8709f96acad9a15c63279cf937b75d01dd91a1585ac5ca41256e80e432a0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ae6c80ee852fcccae85579165042a3767dcd1190112e87c9f22fa3e76a624c73`  
		Last Modified: Tue, 03 Dec 2024 01:27:10 GMT  
		Size: 29.2 MB (29205487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580dd662e45fd4b251d3406f5a1ea8962e3e4e1d2520efbb737df740b7e957f2`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3f1598f54c5456764cfdadbb7074ec777bd66ed0fab6c8fdfa5e8a435c5ae8`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 2.5 MB (2500687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd3aa7547e95a174e12f01b948f1c39aee54d184931a433b0ea5f3e180259de`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 1.3 MB (1259605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b9d8a09b833489a3bf75e47d6fc9c98a4f688e73ae311ff2277c461dc66a85`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6fe54f00cf7e2bebef13e9698cee799c63127f12560807f4bf87fda6395baf`  
		Last Modified: Fri, 06 Dec 2024 01:31:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:2029c4c3e23c8bfb7b5f3992ef8057fc969eca5273a1f436d6d8605b3ba6f081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2309883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025c0e1e5fec67ce720fae6f7e5aaaa9c8217653956e512bf60be97cb2294914`

```dockerfile
```

-	Layers:
	-	`sha256:3f7aef5b25a76a78ebdd73ae22cef84f68f0d0a920a1e0a89dab2aa1fa5accdd`  
		Last Modified: Fri, 06 Dec 2024 01:31:11 GMT  
		Size: 2.3 MB (2288719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:551482c681545d405b9f1d3139dcf0fb74b2fecfd0e7d9d54de6e57a981c3d71`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; mips64le

```console
$ docker pull memcached@sha256:b398c51c3b2d91d0274741650d383d12bb8dd65d4acdb202d0a7063d6e4b8b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31705243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4838f50554bb3277090b0aa55a3191c3489fc05113546999725b9c946e1a954e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:29ac4ae2849b0c84c0ef17659082268617abeb406402ef46b6fa9140e6d2064d`  
		Last Modified: Tue, 03 Dec 2024 01:28:15 GMT  
		Size: 28.5 MB (28505909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f398f0ee699c887dba3a51e3212be4320212ed287d33cdd1df41e7fd72240a7`  
		Last Modified: Fri, 06 Dec 2024 01:35:13 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7ddb249939dc734c215bc1be4a564dacdb2495a3ca51100084126ecd662f02`  
		Last Modified: Fri, 06 Dec 2024 01:35:14 GMT  
		Size: 1.9 MB (1943197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d087c96f4f05d81a987f0812e9c7c28cca806e5aa40786761696d7bd547b926a`  
		Last Modified: Fri, 06 Dec 2024 01:35:14 GMT  
		Size: 1.3 MB (1254620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec32257bb4a1a2d1b3c027ae74afbc31c03aec77c3aec28b9f546843aa638ab`  
		Last Modified: Fri, 06 Dec 2024 01:35:13 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4f728769ae3f10d5ef679ac778b45c6992248d4a8e853760525c3c24041f6f`  
		Last Modified: Fri, 06 Dec 2024 01:35:14 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:f528c619723b1b912a572178e808db3bf0968e4baf6ef920992198b60a50bd7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00565dc210c91f04967e0e4b932ca263ef440c9803d1fb47313d6524c29b26f3`

```dockerfile
```

-	Layers:
	-	`sha256:4fe7144715458a1e421c93fd64b7134c4f3738eb832551e549e822b1ba66523d`  
		Last Modified: Fri, 06 Dec 2024 01:35:13 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:01b87270745db075ed8b996a903bbb03e1ce8e91a1492c6763e8e0184098bf0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36096936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca502cddeb618d1bc49dc5bc8d6538584dd37bf9fdef22011502443d817f36aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e62b6946337cc6b72ec307008f1acc46e12a4f98e6f0e29c92b5538bbafd7ce6`  
		Last Modified: Tue, 03 Dec 2024 01:28:28 GMT  
		Size: 32.1 MB (32063265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8e81ffdbb3a1a0871b7d927a02d62e2ce4eb8b6f7bbc76e4bba93c799b9075`  
		Last Modified: Tue, 03 Dec 2024 02:42:07 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0276e7f6ce6bb384613f81bb9a596143583bdbf5cac2714170243761daa43b7`  
		Last Modified: Tue, 03 Dec 2024 02:42:08 GMT  
		Size: 2.7 MB (2708555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb84fa77333d98470bc633574f7b051132ca9675ff7d781c3cce4a079186907b`  
		Last Modified: Fri, 06 Dec 2024 01:30:50 GMT  
		Size: 1.3 MB (1323604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ecb320c4cc5c4e8e57c37ce8e39a4136d2ef053377f6bc3812880eeab6f20f`  
		Last Modified: Fri, 06 Dec 2024 01:30:50 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b9e76d0bac4875861b1d66e91f0dd7273347b172785e7659835a862b71c9e2`  
		Last Modified: Fri, 06 Dec 2024 01:30:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:2416ac25dc3bb76b01b44fb54d535ad95f9e7d3f8c5cc714c15e381a4d35d0ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2317287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48fe760f47f1bdadfdc6584c4f1802c30ff05ebb44d44b931211aac3a762993f`

```dockerfile
```

-	Layers:
	-	`sha256:5f182f9c7a52c9256109712b419bb1efe3847e993e342af008724d31754d7b58`  
		Last Modified: Fri, 06 Dec 2024 01:30:50 GMT  
		Size: 2.3 MB (2295992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:373a3417f812a3143655df1a9b4ee6893a0b627316005c587b3c5ddacd6cdd6d`  
		Last Modified: Fri, 06 Dec 2024 01:30:50 GMT  
		Size: 21.3 KB (21295 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:2a204d42b50b0598b0ce8900e8bde20bcbf35f9c5cd4bbb38186b48cdac2d4d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30274542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:154623d34f127ea2636384bc7205519ccf3b1aad97280ebcdb64b7662a374040`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9378ae44108012049addde60d193467e2b15a247b2f953ad5c27e073c4573d42`  
		Last Modified: Tue, 03 Dec 2024 01:28:18 GMT  
		Size: 26.9 MB (26878971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214d47b5512f1991eb09046f46526e464102115476ac71ca1c8e7bd9439c4a5b`  
		Last Modified: Tue, 03 Dec 2024 02:32:32 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc13e1c57cbb046f722e07c9a375af936eb9f47e47a86a2435b54dc393da6657`  
		Last Modified: Tue, 03 Dec 2024 02:32:32 GMT  
		Size: 2.2 MB (2156364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cecb2200496ee18d3c1d0287a623829849840935d625131d9dded26f2bd67478`  
		Last Modified: Fri, 06 Dec 2024 01:32:17 GMT  
		Size: 1.2 MB (1237695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06048c152c70476e77823ded2b6e26aaa36538ae99b655fed345f19eacdccb3`  
		Last Modified: Fri, 06 Dec 2024 01:32:17 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad2217a2f73e7c40ee3dda6f84683bbf529af0a6c88a2f8509a8c6236fab9b3`  
		Last Modified: Fri, 06 Dec 2024 01:32:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:9633d4f6d1ceb311422b86502f057cfd400959e6fa3f9fa28d6848bb6cdc9055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2312558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b9c4fe1473e54d45f0c30ca2bdaa8200d0f9e10d811703e74c27232d288313`

```dockerfile
```

-	Layers:
	-	`sha256:470d0c1e3b27df7cc86c281b0b437958b8b4742962b109311219d1d5c8d199e7`  
		Last Modified: Fri, 06 Dec 2024 01:32:17 GMT  
		Size: 2.3 MB (2291336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d21968c91e92936985a4af7a988f292a75a85b6f014bbb668a0e336ff3f0966`  
		Last Modified: Fri, 06 Dec 2024 01:32:17 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:e8f244572aec9f880cbccace3a05f97f24ff71b53d8d694814748eac12f427c2
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
$ docker pull memcached@sha256:e303bdddcf04ceba4983b9b8cf8b40f8fa41a3ba2d31f7214151d17a2a3076dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6964456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f99a3c16eb499f6cdf0c4680227af234f0e81b86cbb3e219dfd1cc4d331ed8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4191c73fdb45d23dac2c68d4abc8221e6406e9b5591365424302359c1717d44f`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc8b2c6385836cdfcf380e66751377fa23d31f333b616fdd8024545be6c0cc7`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 103.8 KB (103823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77829dd883bfed11037e738040ee96033efef20717be2a3ee174be7d444bd5e3`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 3.2 MB (3235366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfc1d638a936f750e8e87da5702f5b6b5ca51380fca27d33b2f2a75c14f22ba`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b374bd2d4e1ea47b597a16a9e9e56aba35aef6fc394904249a1f2e0f08618e`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c8915813030bfdc12790cdf965af8cfe77b77f8af9f51e92837f89f9eb87c296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05abf48b9dac7138d3a7fe7d19150a99ab63e08e30d39ba567ac00a81d2f1128`

```dockerfile
```

-	Layers:
	-	`sha256:4c8e4bfd8ce93a5fb987902f718ea9389273600f0d3e9d4787a4b63df46b890a`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 88.0 KB (87997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f08348125d8660725339fdc8fac6a613450c75e943e98dc3dde6ba8364bea2cf`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 19.6 KB (19574 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:070c242a1121df9eaa6bb4151dc7c67340b8f20ef0ad5d0e049de50dd7344396
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7862766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c37e99de69f18e54515a8d3071b8ea1fd0f2a4900297a8b2c1c386a6a24b78ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb9a0a7b9b4c9f5adc5080dca4ca693f553a370e9fa64affed9aac65b383dc5`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694142e1e3f17625e53d3827671e05224425e877a3e74761c94b54645204ded1`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 121.0 KB (121021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7796589e641878ee661afd57987309f860c136ca6f4413c7d84116bd64ecad12`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 3.7 MB (3652653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29e7393633dafdad3ecd5f2432e9c09c88ae197ae63ebc39cdd5d755efc1093`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7232ef393c6312a3d76029b6d56988d15a40f595f77e0537ee596b7caaca7132`  
		Last Modified: Fri, 06 Dec 2024 01:33:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:fe3c78175237195a75aca53378025420314ce4b8bd427652e821e9663becf695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.9 KB (107872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095cd6aa8766c7a849d35f1d8a015b4b7aec092919440079533223bcd2268290`

```dockerfile
```

-	Layers:
	-	`sha256:e9f4643bf814c73775db7c54c18dd433640b2a57bca6adaf08f427cfa1bc3de1`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 88.1 KB (88101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee64ac9068d8c28d1fbbd0690d6771ea5be16985b2b5dd0fdc3e6769ec1ee14b`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 19.8 KB (19771 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:492db91f15dbd3e9e9e33a1f7e2cc09b20fae42051a02e3f0de5acd8454a316c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6646126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3ad52f1373f146c439a3c8e68b2d6ed471a4db701c049fd0b5ffea34119f61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bfed8762acb5fad17a943b928db6acd316a3f41770d6ccb3ccde6c5058de8d6`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f39ea1560a9fce397084caa49fd70c40dc655e0857cec268d76a430c74e7b9`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 109.0 KB (108960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a781c1b2a58f8cf6bd9facbe1e1ad73be61573272f8914f2dd4bf85d4ff0baad`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 3.1 MB (3066579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b827afe494b121a7e333c94baa21f20421366c2bb0f1e0eeb73e437c52ff40`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9d6c0f8c12091da40ce7700dcb522ce3106703627f2a754241cdb1bbc845d1`  
		Last Modified: Fri, 06 Dec 2024 01:31:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c91fa3449f439c4e9c30c88fa79e5fe63d3bf8af8356defc87da1e56609349ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ee8dfa6edf9c1a3e3b579f7f9fce0a46eb85e82ae82e1e5364b961be5801ca`

```dockerfile
```

-	Layers:
	-	`sha256:a3eb59cf4c9b8cc00383cca89ed90cd3e204f3e898b960d8fb6aea259589e2f3`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 88.0 KB (87952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3242abd4e76a0a4671ab58ff40ccc25a63d6e796bdf01ab8238cd61b52844e92`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 19.5 KB (19516 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:9ed77a1e3df85d41958cfab6678f84b7a0c5478c3ee4031bb4ef7009ae148a8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6838378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7debc910ab631f46ff86577268f8190435a1a1cad3c4f28c2a14839844c89ec6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac7c2caa12b9b7c688356275a58d0faa1e26ca96ea89c8041aca795343d90fb`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0955050f3ec94864d6e58cb0e77be49260e6358a11bcfe4f18fcd7a16ef98bd`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 123.0 KB (123004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1076a55e57cd99a295a1a9b0943a35ef12c0cbefcee0f539ebc0f9d767f09ac7`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 3.1 MB (3141546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd0157cad0ccfad57f8818a6674665d46df00b03abce2b8b0a4b2b55bc097af`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200b295ab1fad685ec6581c5220bd29b35b4de15dd7b79b1670cc8c3a5318ff1`  
		Last Modified: Fri, 06 Dec 2024 01:33:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:44ef397246da32f636714921281ea510a545706dff7755d39ed522fd34ef818c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.7 KB (105748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27dd5988cf9c77426d5d3ce108181cfde561e89d21a1e57c46b06a24494bc24`

```dockerfile
```

-	Layers:
	-	`sha256:9dd942067c2d5eec8c44d618b60a4fb2d533da4aaa9e59aa658035bae7864153`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 86.1 KB (86101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7ae50a8f9772a347faf3150966eb0a294bad1037dcd82a6b7ca6e7085def4b0`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 19.6 KB (19647 bytes)  
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
$ docker pull memcached@sha256:2f9e35d548959a8ea66fbb14b4e45db6201bd399fbce7aa6a91ced6724529015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6590517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e59cf784613df48eaa8bb5d47ccb40bb41263090034725c38a1d343c40fdc98b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd586bc77f5fb181172c996290db7374e9c10d57409c2b44fd564414325e007`  
		Last Modified: Fri, 06 Dec 2024 01:36:13 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0fcd80ecbef8175a68d824552ed0f114429b0267802305d4c7d844c3577627e`  
		Last Modified: Fri, 06 Dec 2024 01:36:13 GMT  
		Size: 112.8 KB (112750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec43a227c373cac7def72eaec9a32204740c8000aa305974e2bdb1684ee66532`  
		Last Modified: Fri, 06 Dec 2024 01:36:13 GMT  
		Size: 3.0 MB (3014795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c4d2f183090b5a127cca23a337b895f3cf87bf67d4f7753457dda9b9e71179`  
		Last Modified: Fri, 06 Dec 2024 01:36:14 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e27bc505bddda3fa278b4085496625d324fb6e550b22e4eed35b931033473d7`  
		Last Modified: Fri, 06 Dec 2024 01:36:14 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:19d143dfb5e455c347101473ad04cdac2e988e4db9be4af04174526f0d488453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185266b3e1c500c32f3ce16d81debe696e90be32f272cd58900e7e79549f53f4`

```dockerfile
```

-	Layers:
	-	`sha256:cb583c39b213e1d44b5dc21216421e4b8ff1f212376d783788f7ecec530ffbdd`  
		Last Modified: Fri, 06 Dec 2024 01:36:13 GMT  
		Size: 86.0 KB (86043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d788cea57935c2cb3c0e8b4293caec6b1447956196a6739ddf9264bcb76563a9`  
		Last Modified: Fri, 06 Dec 2024 01:36:13 GMT  
		Size: 19.6 KB (19574 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine3.20`

```console
$ docker pull memcached@sha256:e8f244572aec9f880cbccace3a05f97f24ff71b53d8d694814748eac12f427c2
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

### `memcached:1-alpine3.20` - linux; amd64

```console
$ docker pull memcached@sha256:e303bdddcf04ceba4983b9b8cf8b40f8fa41a3ba2d31f7214151d17a2a3076dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6964456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f99a3c16eb499f6cdf0c4680227af234f0e81b86cbb3e219dfd1cc4d331ed8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4191c73fdb45d23dac2c68d4abc8221e6406e9b5591365424302359c1717d44f`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc8b2c6385836cdfcf380e66751377fa23d31f333b616fdd8024545be6c0cc7`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 103.8 KB (103823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77829dd883bfed11037e738040ee96033efef20717be2a3ee174be7d444bd5e3`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 3.2 MB (3235366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfc1d638a936f750e8e87da5702f5b6b5ca51380fca27d33b2f2a75c14f22ba`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b374bd2d4e1ea47b597a16a9e9e56aba35aef6fc394904249a1f2e0f08618e`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:c8915813030bfdc12790cdf965af8cfe77b77f8af9f51e92837f89f9eb87c296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05abf48b9dac7138d3a7fe7d19150a99ab63e08e30d39ba567ac00a81d2f1128`

```dockerfile
```

-	Layers:
	-	`sha256:4c8e4bfd8ce93a5fb987902f718ea9389273600f0d3e9d4787a4b63df46b890a`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 88.0 KB (87997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f08348125d8660725339fdc8fac6a613450c75e943e98dc3dde6ba8364bea2cf`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 19.6 KB (19574 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:070c242a1121df9eaa6bb4151dc7c67340b8f20ef0ad5d0e049de50dd7344396
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7862766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c37e99de69f18e54515a8d3071b8ea1fd0f2a4900297a8b2c1c386a6a24b78ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb9a0a7b9b4c9f5adc5080dca4ca693f553a370e9fa64affed9aac65b383dc5`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694142e1e3f17625e53d3827671e05224425e877a3e74761c94b54645204ded1`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 121.0 KB (121021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7796589e641878ee661afd57987309f860c136ca6f4413c7d84116bd64ecad12`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 3.7 MB (3652653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29e7393633dafdad3ecd5f2432e9c09c88ae197ae63ebc39cdd5d755efc1093`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7232ef393c6312a3d76029b6d56988d15a40f595f77e0537ee596b7caaca7132`  
		Last Modified: Fri, 06 Dec 2024 01:33:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:fe3c78175237195a75aca53378025420314ce4b8bd427652e821e9663becf695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.9 KB (107872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095cd6aa8766c7a849d35f1d8a015b4b7aec092919440079533223bcd2268290`

```dockerfile
```

-	Layers:
	-	`sha256:e9f4643bf814c73775db7c54c18dd433640b2a57bca6adaf08f427cfa1bc3de1`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 88.1 KB (88101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee64ac9068d8c28d1fbbd0690d6771ea5be16985b2b5dd0fdc3e6769ec1ee14b`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 19.8 KB (19771 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; 386

```console
$ docker pull memcached@sha256:492db91f15dbd3e9e9e33a1f7e2cc09b20fae42051a02e3f0de5acd8454a316c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6646126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3ad52f1373f146c439a3c8e68b2d6ed471a4db701c049fd0b5ffea34119f61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bfed8762acb5fad17a943b928db6acd316a3f41770d6ccb3ccde6c5058de8d6`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f39ea1560a9fce397084caa49fd70c40dc655e0857cec268d76a430c74e7b9`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 109.0 KB (108960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a781c1b2a58f8cf6bd9facbe1e1ad73be61573272f8914f2dd4bf85d4ff0baad`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 3.1 MB (3066579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b827afe494b121a7e333c94baa21f20421366c2bb0f1e0eeb73e437c52ff40`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9d6c0f8c12091da40ce7700dcb522ce3106703627f2a754241cdb1bbc845d1`  
		Last Modified: Fri, 06 Dec 2024 01:31:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:c91fa3449f439c4e9c30c88fa79e5fe63d3bf8af8356defc87da1e56609349ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ee8dfa6edf9c1a3e3b579f7f9fce0a46eb85e82ae82e1e5364b961be5801ca`

```dockerfile
```

-	Layers:
	-	`sha256:a3eb59cf4c9b8cc00383cca89ed90cd3e204f3e898b960d8fb6aea259589e2f3`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 88.0 KB (87952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3242abd4e76a0a4671ab58ff40ccc25a63d6e796bdf01ab8238cd61b52844e92`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 19.5 KB (19516 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; ppc64le

```console
$ docker pull memcached@sha256:9ed77a1e3df85d41958cfab6678f84b7a0c5478c3ee4031bb4ef7009ae148a8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6838378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7debc910ab631f46ff86577268f8190435a1a1cad3c4f28c2a14839844c89ec6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac7c2caa12b9b7c688356275a58d0faa1e26ca96ea89c8041aca795343d90fb`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0955050f3ec94864d6e58cb0e77be49260e6358a11bcfe4f18fcd7a16ef98bd`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 123.0 KB (123004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1076a55e57cd99a295a1a9b0943a35ef12c0cbefcee0f539ebc0f9d767f09ac7`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 3.1 MB (3141546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd0157cad0ccfad57f8818a6674665d46df00b03abce2b8b0a4b2b55bc097af`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200b295ab1fad685ec6581c5220bd29b35b4de15dd7b79b1670cc8c3a5318ff1`  
		Last Modified: Fri, 06 Dec 2024 01:33:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:44ef397246da32f636714921281ea510a545706dff7755d39ed522fd34ef818c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.7 KB (105748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27dd5988cf9c77426d5d3ce108181cfde561e89d21a1e57c46b06a24494bc24`

```dockerfile
```

-	Layers:
	-	`sha256:9dd942067c2d5eec8c44d618b60a4fb2d533da4aaa9e59aa658035bae7864153`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 86.1 KB (86101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7ae50a8f9772a347faf3150966eb0a294bad1037dcd82a6b7ca6e7085def4b0`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 19.6 KB (19647 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; riscv64

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

### `memcached:1-alpine3.20` - unknown; unknown

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

### `memcached:1-alpine3.20` - linux; s390x

```console
$ docker pull memcached@sha256:2f9e35d548959a8ea66fbb14b4e45db6201bd399fbce7aa6a91ced6724529015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6590517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e59cf784613df48eaa8bb5d47ccb40bb41263090034725c38a1d343c40fdc98b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd586bc77f5fb181172c996290db7374e9c10d57409c2b44fd564414325e007`  
		Last Modified: Fri, 06 Dec 2024 01:36:13 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0fcd80ecbef8175a68d824552ed0f114429b0267802305d4c7d844c3577627e`  
		Last Modified: Fri, 06 Dec 2024 01:36:13 GMT  
		Size: 112.8 KB (112750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec43a227c373cac7def72eaec9a32204740c8000aa305974e2bdb1684ee66532`  
		Last Modified: Fri, 06 Dec 2024 01:36:13 GMT  
		Size: 3.0 MB (3014795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c4d2f183090b5a127cca23a337b895f3cf87bf67d4f7753457dda9b9e71179`  
		Last Modified: Fri, 06 Dec 2024 01:36:14 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e27bc505bddda3fa278b4085496625d324fb6e550b22e4eed35b931033473d7`  
		Last Modified: Fri, 06 Dec 2024 01:36:14 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:19d143dfb5e455c347101473ad04cdac2e988e4db9be4af04174526f0d488453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185266b3e1c500c32f3ce16d81debe696e90be32f272cd58900e7e79549f53f4`

```dockerfile
```

-	Layers:
	-	`sha256:cb583c39b213e1d44b5dc21216421e4b8ff1f212376d783788f7ecec530ffbdd`  
		Last Modified: Fri, 06 Dec 2024 01:36:13 GMT  
		Size: 86.0 KB (86043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d788cea57935c2cb3c0e8b4293caec6b1447956196a6739ddf9264bcb76563a9`  
		Last Modified: Fri, 06 Dec 2024 01:36:13 GMT  
		Size: 19.6 KB (19574 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-bookworm`

```console
$ docker pull memcached@sha256:b8cb0ed0bf5d3d38f9606fc847c9a21baa68952472ea29a5a685f82a1efc2987
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
$ docker pull memcached@sha256:1e2854f49ddb3fc0103bf7b8fcd80ed47c6f72e2aa74ad0848acc1274e4f98f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31984433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04abd86d309da60dfe2b7f4f4e20226dd5f87fe17482740074bbc2c6865d6987`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977f47ceef0f8173cff02fe737b3fd37efab540ec727c2a20869e90ab8279920`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1599032aa7639a9095e216c0b122c7eb2cf54392a6e7bf2d191ff3e086bb478a`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 2.5 MB (2491759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:034904c659cc08a9f86d31858f173bfc3a20727cb5fb51319eb9478c29151562`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 1.3 MB (1259579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbc04f1662c41c4314f0f2a27cbf319464d441170360aee7702dd51be327e76`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4e9ce09f9de3f7835981235d8000bd031663f2328a8e4ffb2f6b6e9d1a1e0d`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:fb6b716e55ea5a7353f965101017052ad92d603abfbd05eb49dc5aeceea69dfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2312843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2806c278d65e027e6b4619f466776331a5efde1eb1992a4a013a5e85ae769111`

```dockerfile
```

-	Layers:
	-	`sha256:a489ae83eb749729e07a801603bdc10563b8508b7272d035a9f58304ea805e5c`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 2.3 MB (2291621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbb57e1ba346b719e10354837a9bef89546f505a248a0977af44ec554c92262a`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:91ab868f687f5d84ed97501641c6276629ba558cf3b893411d4bff8ddf3b7a20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29090498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddac0a9030226a9353757b40367ccad4e58abf3df5f1cecab9445504a7141a50`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:25d432086d20067bebfff2b163f22d49e7da8528782652615fe170bf8c39194d`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 25.8 MB (25754926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29864ebc65411065e6cc80afcb839ecd53357c5d8accb084195a861ffe331f0c`  
		Last Modified: Tue, 03 Dec 2024 02:34:22 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17b8bb45df912fe349545bf67aeee395da8a6bbd8c9fd4b4bba4ab37d4c46e6`  
		Last Modified: Tue, 03 Dec 2024 02:34:23 GMT  
		Size: 2.1 MB (2096040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f971acf6335510d8cd95bbf08ed1b82d5ccdbb6a46d5cc4004f4d3f17f79ad22`  
		Last Modified: Fri, 06 Dec 2024 01:31:23 GMT  
		Size: 1.2 MB (1238020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d2f4b78825fe502c36e4f1340340617bc5d281e1a4d0bfd9c29b683505190d`  
		Last Modified: Fri, 06 Dec 2024 01:31:23 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0b278088431fe97844cee08594eb17b8a478179969a38c2138afcc8635209b`  
		Last Modified: Fri, 06 Dec 2024 01:31:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:33b0db124591dec0a6fd5c81068992c08e8cb9a2f4e0f7c8dd8474b34525c0f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2316527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59492fefec6386be99693d0d6d513a6c53fd5cc3e197beb39bcce988752d934b`

```dockerfile
```

-	Layers:
	-	`sha256:3183c33c304bb139731b8181094f3cedf637a75d2c2b46a39117b249bcbf9a94`  
		Last Modified: Fri, 06 Dec 2024 01:31:23 GMT  
		Size: 2.3 MB (2295158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe9afff481d34963c12864f80d0a8758b8462fbfbdf815070d7b572ba117476b`  
		Last Modified: Fri, 06 Dec 2024 01:31:23 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:4b50248c9ebc50990818eb60f6c506e07a29315de1cf92f8089ce198db55f78f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31670277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae090e1fc19e90d2a650cdd682ddd6cebff3ef4c472411c422c7b772f9c7844a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78a410ea91650a45f4516634a8253fbca2d2238ebd376ee434a91c97add0d41`  
		Last Modified: Tue, 03 Dec 2024 02:56:13 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3651f43c686dcae90b2bb5bfaafb1c1e92231bce87f7c2a4f7f92606b3f6048`  
		Last Modified: Tue, 03 Dec 2024 02:56:14 GMT  
		Size: 2.4 MB (2355349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1974b3b5f9215ed5e7c38499590f73f9d2cc9f0eab4b5bfc835e795f011b6ec`  
		Last Modified: Fri, 06 Dec 2024 01:31:13 GMT  
		Size: 1.3 MB (1254605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0d87f19f5dcc124861cef54d5060fdddf78285679e5e18c5c228a649873178`  
		Last Modified: Fri, 06 Dec 2024 01:31:12 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4e9ce09f9de3f7835981235d8000bd031663f2328a8e4ffb2f6b6e9d1a1e0d`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:65ec047e972b106c4dccd5e7db2375b427183eaa0a17d24a87733f0781a6f4cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2313354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6be2bd8ba74100235eb2a7790cd07be00c97e00f811e0074913d8ef6bce12587`

```dockerfile
```

-	Layers:
	-	`sha256:aea7e31a5ac097dbe2c1f459e15d324e0b4c270652bc090fc7bb75b32d29171f`  
		Last Modified: Fri, 06 Dec 2024 01:31:13 GMT  
		Size: 2.3 MB (2291935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72554d4560a983cd304f173578e432f68442018a3d2f900c20e8692c7507475d`  
		Last Modified: Fri, 06 Dec 2024 01:31:12 GMT  
		Size: 21.4 KB (21419 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:2ee1837e5180933d5ce36c27a48671480a1269845d9fe11427b429f7ddcb89e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32967293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa8709f96acad9a15c63279cf937b75d01dd91a1585ac5ca41256e80e432a0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ae6c80ee852fcccae85579165042a3767dcd1190112e87c9f22fa3e76a624c73`  
		Last Modified: Tue, 03 Dec 2024 01:27:10 GMT  
		Size: 29.2 MB (29205487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580dd662e45fd4b251d3406f5a1ea8962e3e4e1d2520efbb737df740b7e957f2`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3f1598f54c5456764cfdadbb7074ec777bd66ed0fab6c8fdfa5e8a435c5ae8`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 2.5 MB (2500687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd3aa7547e95a174e12f01b948f1c39aee54d184931a433b0ea5f3e180259de`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 1.3 MB (1259605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b9d8a09b833489a3bf75e47d6fc9c98a4f688e73ae311ff2277c461dc66a85`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6fe54f00cf7e2bebef13e9698cee799c63127f12560807f4bf87fda6395baf`  
		Last Modified: Fri, 06 Dec 2024 01:31:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:2029c4c3e23c8bfb7b5f3992ef8057fc969eca5273a1f436d6d8605b3ba6f081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2309883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025c0e1e5fec67ce720fae6f7e5aaaa9c8217653956e512bf60be97cb2294914`

```dockerfile
```

-	Layers:
	-	`sha256:3f7aef5b25a76a78ebdd73ae22cef84f68f0d0a920a1e0a89dab2aa1fa5accdd`  
		Last Modified: Fri, 06 Dec 2024 01:31:11 GMT  
		Size: 2.3 MB (2288719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:551482c681545d405b9f1d3139dcf0fb74b2fecfd0e7d9d54de6e57a981c3d71`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:b398c51c3b2d91d0274741650d383d12bb8dd65d4acdb202d0a7063d6e4b8b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31705243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4838f50554bb3277090b0aa55a3191c3489fc05113546999725b9c946e1a954e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:29ac4ae2849b0c84c0ef17659082268617abeb406402ef46b6fa9140e6d2064d`  
		Last Modified: Tue, 03 Dec 2024 01:28:15 GMT  
		Size: 28.5 MB (28505909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f398f0ee699c887dba3a51e3212be4320212ed287d33cdd1df41e7fd72240a7`  
		Last Modified: Fri, 06 Dec 2024 01:35:13 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7ddb249939dc734c215bc1be4a564dacdb2495a3ca51100084126ecd662f02`  
		Last Modified: Fri, 06 Dec 2024 01:35:14 GMT  
		Size: 1.9 MB (1943197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d087c96f4f05d81a987f0812e9c7c28cca806e5aa40786761696d7bd547b926a`  
		Last Modified: Fri, 06 Dec 2024 01:35:14 GMT  
		Size: 1.3 MB (1254620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec32257bb4a1a2d1b3c027ae74afbc31c03aec77c3aec28b9f546843aa638ab`  
		Last Modified: Fri, 06 Dec 2024 01:35:13 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4f728769ae3f10d5ef679ac778b45c6992248d4a8e853760525c3c24041f6f`  
		Last Modified: Fri, 06 Dec 2024 01:35:14 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f528c619723b1b912a572178e808db3bf0968e4baf6ef920992198b60a50bd7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00565dc210c91f04967e0e4b932ca263ef440c9803d1fb47313d6524c29b26f3`

```dockerfile
```

-	Layers:
	-	`sha256:4fe7144715458a1e421c93fd64b7134c4f3738eb832551e549e822b1ba66523d`  
		Last Modified: Fri, 06 Dec 2024 01:35:13 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:01b87270745db075ed8b996a903bbb03e1ce8e91a1492c6763e8e0184098bf0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36096936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca502cddeb618d1bc49dc5bc8d6538584dd37bf9fdef22011502443d817f36aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e62b6946337cc6b72ec307008f1acc46e12a4f98e6f0e29c92b5538bbafd7ce6`  
		Last Modified: Tue, 03 Dec 2024 01:28:28 GMT  
		Size: 32.1 MB (32063265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8e81ffdbb3a1a0871b7d927a02d62e2ce4eb8b6f7bbc76e4bba93c799b9075`  
		Last Modified: Tue, 03 Dec 2024 02:42:07 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0276e7f6ce6bb384613f81bb9a596143583bdbf5cac2714170243761daa43b7`  
		Last Modified: Tue, 03 Dec 2024 02:42:08 GMT  
		Size: 2.7 MB (2708555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb84fa77333d98470bc633574f7b051132ca9675ff7d781c3cce4a079186907b`  
		Last Modified: Fri, 06 Dec 2024 01:30:50 GMT  
		Size: 1.3 MB (1323604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ecb320c4cc5c4e8e57c37ce8e39a4136d2ef053377f6bc3812880eeab6f20f`  
		Last Modified: Fri, 06 Dec 2024 01:30:50 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b9e76d0bac4875861b1d66e91f0dd7273347b172785e7659835a862b71c9e2`  
		Last Modified: Fri, 06 Dec 2024 01:30:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:2416ac25dc3bb76b01b44fb54d535ad95f9e7d3f8c5cc714c15e381a4d35d0ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2317287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48fe760f47f1bdadfdc6584c4f1802c30ff05ebb44d44b931211aac3a762993f`

```dockerfile
```

-	Layers:
	-	`sha256:5f182f9c7a52c9256109712b419bb1efe3847e993e342af008724d31754d7b58`  
		Last Modified: Fri, 06 Dec 2024 01:30:50 GMT  
		Size: 2.3 MB (2295992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:373a3417f812a3143655df1a9b4ee6893a0b627316005c587b3c5ddacd6cdd6d`  
		Last Modified: Fri, 06 Dec 2024 01:30:50 GMT  
		Size: 21.3 KB (21295 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:2a204d42b50b0598b0ce8900e8bde20bcbf35f9c5cd4bbb38186b48cdac2d4d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30274542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:154623d34f127ea2636384bc7205519ccf3b1aad97280ebcdb64b7662a374040`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9378ae44108012049addde60d193467e2b15a247b2f953ad5c27e073c4573d42`  
		Last Modified: Tue, 03 Dec 2024 01:28:18 GMT  
		Size: 26.9 MB (26878971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214d47b5512f1991eb09046f46526e464102115476ac71ca1c8e7bd9439c4a5b`  
		Last Modified: Tue, 03 Dec 2024 02:32:32 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc13e1c57cbb046f722e07c9a375af936eb9f47e47a86a2435b54dc393da6657`  
		Last Modified: Tue, 03 Dec 2024 02:32:32 GMT  
		Size: 2.2 MB (2156364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cecb2200496ee18d3c1d0287a623829849840935d625131d9dded26f2bd67478`  
		Last Modified: Fri, 06 Dec 2024 01:32:17 GMT  
		Size: 1.2 MB (1237695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06048c152c70476e77823ded2b6e26aaa36538ae99b655fed345f19eacdccb3`  
		Last Modified: Fri, 06 Dec 2024 01:32:17 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad2217a2f73e7c40ee3dda6f84683bbf529af0a6c88a2f8509a8c6236fab9b3`  
		Last Modified: Fri, 06 Dec 2024 01:32:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:9633d4f6d1ceb311422b86502f057cfd400959e6fa3f9fa28d6848bb6cdc9055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2312558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b9c4fe1473e54d45f0c30ca2bdaa8200d0f9e10d811703e74c27232d288313`

```dockerfile
```

-	Layers:
	-	`sha256:470d0c1e3b27df7cc86c281b0b437958b8b4742962b109311219d1d5c8d199e7`  
		Last Modified: Fri, 06 Dec 2024 01:32:17 GMT  
		Size: 2.3 MB (2291336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d21968c91e92936985a4af7a988f292a75a85b6f014bbb668a0e336ff3f0966`  
		Last Modified: Fri, 06 Dec 2024 01:32:17 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6`

```console
$ docker pull memcached@sha256:b8cb0ed0bf5d3d38f9606fc847c9a21baa68952472ea29a5a685f82a1efc2987
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
$ docker pull memcached@sha256:1e2854f49ddb3fc0103bf7b8fcd80ed47c6f72e2aa74ad0848acc1274e4f98f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31984433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04abd86d309da60dfe2b7f4f4e20226dd5f87fe17482740074bbc2c6865d6987`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977f47ceef0f8173cff02fe737b3fd37efab540ec727c2a20869e90ab8279920`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1599032aa7639a9095e216c0b122c7eb2cf54392a6e7bf2d191ff3e086bb478a`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 2.5 MB (2491759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:034904c659cc08a9f86d31858f173bfc3a20727cb5fb51319eb9478c29151562`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 1.3 MB (1259579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbc04f1662c41c4314f0f2a27cbf319464d441170360aee7702dd51be327e76`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4e9ce09f9de3f7835981235d8000bd031663f2328a8e4ffb2f6b6e9d1a1e0d`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:fb6b716e55ea5a7353f965101017052ad92d603abfbd05eb49dc5aeceea69dfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2312843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2806c278d65e027e6b4619f466776331a5efde1eb1992a4a013a5e85ae769111`

```dockerfile
```

-	Layers:
	-	`sha256:a489ae83eb749729e07a801603bdc10563b8508b7272d035a9f58304ea805e5c`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 2.3 MB (2291621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbb57e1ba346b719e10354837a9bef89546f505a248a0977af44ec554c92262a`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:91ab868f687f5d84ed97501641c6276629ba558cf3b893411d4bff8ddf3b7a20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29090498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddac0a9030226a9353757b40367ccad4e58abf3df5f1cecab9445504a7141a50`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:25d432086d20067bebfff2b163f22d49e7da8528782652615fe170bf8c39194d`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 25.8 MB (25754926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29864ebc65411065e6cc80afcb839ecd53357c5d8accb084195a861ffe331f0c`  
		Last Modified: Tue, 03 Dec 2024 02:34:22 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17b8bb45df912fe349545bf67aeee395da8a6bbd8c9fd4b4bba4ab37d4c46e6`  
		Last Modified: Tue, 03 Dec 2024 02:34:23 GMT  
		Size: 2.1 MB (2096040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f971acf6335510d8cd95bbf08ed1b82d5ccdbb6a46d5cc4004f4d3f17f79ad22`  
		Last Modified: Fri, 06 Dec 2024 01:31:23 GMT  
		Size: 1.2 MB (1238020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d2f4b78825fe502c36e4f1340340617bc5d281e1a4d0bfd9c29b683505190d`  
		Last Modified: Fri, 06 Dec 2024 01:31:23 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0b278088431fe97844cee08594eb17b8a478179969a38c2138afcc8635209b`  
		Last Modified: Fri, 06 Dec 2024 01:31:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:33b0db124591dec0a6fd5c81068992c08e8cb9a2f4e0f7c8dd8474b34525c0f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2316527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59492fefec6386be99693d0d6d513a6c53fd5cc3e197beb39bcce988752d934b`

```dockerfile
```

-	Layers:
	-	`sha256:3183c33c304bb139731b8181094f3cedf637a75d2c2b46a39117b249bcbf9a94`  
		Last Modified: Fri, 06 Dec 2024 01:31:23 GMT  
		Size: 2.3 MB (2295158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe9afff481d34963c12864f80d0a8758b8462fbfbdf815070d7b572ba117476b`  
		Last Modified: Fri, 06 Dec 2024 01:31:23 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:4b50248c9ebc50990818eb60f6c506e07a29315de1cf92f8089ce198db55f78f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31670277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae090e1fc19e90d2a650cdd682ddd6cebff3ef4c472411c422c7b772f9c7844a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78a410ea91650a45f4516634a8253fbca2d2238ebd376ee434a91c97add0d41`  
		Last Modified: Tue, 03 Dec 2024 02:56:13 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3651f43c686dcae90b2bb5bfaafb1c1e92231bce87f7c2a4f7f92606b3f6048`  
		Last Modified: Tue, 03 Dec 2024 02:56:14 GMT  
		Size: 2.4 MB (2355349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1974b3b5f9215ed5e7c38499590f73f9d2cc9f0eab4b5bfc835e795f011b6ec`  
		Last Modified: Fri, 06 Dec 2024 01:31:13 GMT  
		Size: 1.3 MB (1254605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0d87f19f5dcc124861cef54d5060fdddf78285679e5e18c5c228a649873178`  
		Last Modified: Fri, 06 Dec 2024 01:31:12 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4e9ce09f9de3f7835981235d8000bd031663f2328a8e4ffb2f6b6e9d1a1e0d`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:65ec047e972b106c4dccd5e7db2375b427183eaa0a17d24a87733f0781a6f4cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2313354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6be2bd8ba74100235eb2a7790cd07be00c97e00f811e0074913d8ef6bce12587`

```dockerfile
```

-	Layers:
	-	`sha256:aea7e31a5ac097dbe2c1f459e15d324e0b4c270652bc090fc7bb75b32d29171f`  
		Last Modified: Fri, 06 Dec 2024 01:31:13 GMT  
		Size: 2.3 MB (2291935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72554d4560a983cd304f173578e432f68442018a3d2f900c20e8692c7507475d`  
		Last Modified: Fri, 06 Dec 2024 01:31:12 GMT  
		Size: 21.4 KB (21419 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; 386

```console
$ docker pull memcached@sha256:2ee1837e5180933d5ce36c27a48671480a1269845d9fe11427b429f7ddcb89e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32967293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa8709f96acad9a15c63279cf937b75d01dd91a1585ac5ca41256e80e432a0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ae6c80ee852fcccae85579165042a3767dcd1190112e87c9f22fa3e76a624c73`  
		Last Modified: Tue, 03 Dec 2024 01:27:10 GMT  
		Size: 29.2 MB (29205487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580dd662e45fd4b251d3406f5a1ea8962e3e4e1d2520efbb737df740b7e957f2`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3f1598f54c5456764cfdadbb7074ec777bd66ed0fab6c8fdfa5e8a435c5ae8`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 2.5 MB (2500687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd3aa7547e95a174e12f01b948f1c39aee54d184931a433b0ea5f3e180259de`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 1.3 MB (1259605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b9d8a09b833489a3bf75e47d6fc9c98a4f688e73ae311ff2277c461dc66a85`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6fe54f00cf7e2bebef13e9698cee799c63127f12560807f4bf87fda6395baf`  
		Last Modified: Fri, 06 Dec 2024 01:31:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:2029c4c3e23c8bfb7b5f3992ef8057fc969eca5273a1f436d6d8605b3ba6f081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2309883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025c0e1e5fec67ce720fae6f7e5aaaa9c8217653956e512bf60be97cb2294914`

```dockerfile
```

-	Layers:
	-	`sha256:3f7aef5b25a76a78ebdd73ae22cef84f68f0d0a920a1e0a89dab2aa1fa5accdd`  
		Last Modified: Fri, 06 Dec 2024 01:31:11 GMT  
		Size: 2.3 MB (2288719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:551482c681545d405b9f1d3139dcf0fb74b2fecfd0e7d9d54de6e57a981c3d71`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; mips64le

```console
$ docker pull memcached@sha256:b398c51c3b2d91d0274741650d383d12bb8dd65d4acdb202d0a7063d6e4b8b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31705243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4838f50554bb3277090b0aa55a3191c3489fc05113546999725b9c946e1a954e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:29ac4ae2849b0c84c0ef17659082268617abeb406402ef46b6fa9140e6d2064d`  
		Last Modified: Tue, 03 Dec 2024 01:28:15 GMT  
		Size: 28.5 MB (28505909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f398f0ee699c887dba3a51e3212be4320212ed287d33cdd1df41e7fd72240a7`  
		Last Modified: Fri, 06 Dec 2024 01:35:13 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7ddb249939dc734c215bc1be4a564dacdb2495a3ca51100084126ecd662f02`  
		Last Modified: Fri, 06 Dec 2024 01:35:14 GMT  
		Size: 1.9 MB (1943197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d087c96f4f05d81a987f0812e9c7c28cca806e5aa40786761696d7bd547b926a`  
		Last Modified: Fri, 06 Dec 2024 01:35:14 GMT  
		Size: 1.3 MB (1254620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec32257bb4a1a2d1b3c027ae74afbc31c03aec77c3aec28b9f546843aa638ab`  
		Last Modified: Fri, 06 Dec 2024 01:35:13 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4f728769ae3f10d5ef679ac778b45c6992248d4a8e853760525c3c24041f6f`  
		Last Modified: Fri, 06 Dec 2024 01:35:14 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:f528c619723b1b912a572178e808db3bf0968e4baf6ef920992198b60a50bd7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00565dc210c91f04967e0e4b932ca263ef440c9803d1fb47313d6524c29b26f3`

```dockerfile
```

-	Layers:
	-	`sha256:4fe7144715458a1e421c93fd64b7134c4f3738eb832551e549e822b1ba66523d`  
		Last Modified: Fri, 06 Dec 2024 01:35:13 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:01b87270745db075ed8b996a903bbb03e1ce8e91a1492c6763e8e0184098bf0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36096936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca502cddeb618d1bc49dc5bc8d6538584dd37bf9fdef22011502443d817f36aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e62b6946337cc6b72ec307008f1acc46e12a4f98e6f0e29c92b5538bbafd7ce6`  
		Last Modified: Tue, 03 Dec 2024 01:28:28 GMT  
		Size: 32.1 MB (32063265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8e81ffdbb3a1a0871b7d927a02d62e2ce4eb8b6f7bbc76e4bba93c799b9075`  
		Last Modified: Tue, 03 Dec 2024 02:42:07 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0276e7f6ce6bb384613f81bb9a596143583bdbf5cac2714170243761daa43b7`  
		Last Modified: Tue, 03 Dec 2024 02:42:08 GMT  
		Size: 2.7 MB (2708555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb84fa77333d98470bc633574f7b051132ca9675ff7d781c3cce4a079186907b`  
		Last Modified: Fri, 06 Dec 2024 01:30:50 GMT  
		Size: 1.3 MB (1323604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ecb320c4cc5c4e8e57c37ce8e39a4136d2ef053377f6bc3812880eeab6f20f`  
		Last Modified: Fri, 06 Dec 2024 01:30:50 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b9e76d0bac4875861b1d66e91f0dd7273347b172785e7659835a862b71c9e2`  
		Last Modified: Fri, 06 Dec 2024 01:30:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:2416ac25dc3bb76b01b44fb54d535ad95f9e7d3f8c5cc714c15e381a4d35d0ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2317287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48fe760f47f1bdadfdc6584c4f1802c30ff05ebb44d44b931211aac3a762993f`

```dockerfile
```

-	Layers:
	-	`sha256:5f182f9c7a52c9256109712b419bb1efe3847e993e342af008724d31754d7b58`  
		Last Modified: Fri, 06 Dec 2024 01:30:50 GMT  
		Size: 2.3 MB (2295992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:373a3417f812a3143655df1a9b4ee6893a0b627316005c587b3c5ddacd6cdd6d`  
		Last Modified: Fri, 06 Dec 2024 01:30:50 GMT  
		Size: 21.3 KB (21295 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; s390x

```console
$ docker pull memcached@sha256:2a204d42b50b0598b0ce8900e8bde20bcbf35f9c5cd4bbb38186b48cdac2d4d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30274542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:154623d34f127ea2636384bc7205519ccf3b1aad97280ebcdb64b7662a374040`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9378ae44108012049addde60d193467e2b15a247b2f953ad5c27e073c4573d42`  
		Last Modified: Tue, 03 Dec 2024 01:28:18 GMT  
		Size: 26.9 MB (26878971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214d47b5512f1991eb09046f46526e464102115476ac71ca1c8e7bd9439c4a5b`  
		Last Modified: Tue, 03 Dec 2024 02:32:32 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc13e1c57cbb046f722e07c9a375af936eb9f47e47a86a2435b54dc393da6657`  
		Last Modified: Tue, 03 Dec 2024 02:32:32 GMT  
		Size: 2.2 MB (2156364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cecb2200496ee18d3c1d0287a623829849840935d625131d9dded26f2bd67478`  
		Last Modified: Fri, 06 Dec 2024 01:32:17 GMT  
		Size: 1.2 MB (1237695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06048c152c70476e77823ded2b6e26aaa36538ae99b655fed345f19eacdccb3`  
		Last Modified: Fri, 06 Dec 2024 01:32:17 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad2217a2f73e7c40ee3dda6f84683bbf529af0a6c88a2f8509a8c6236fab9b3`  
		Last Modified: Fri, 06 Dec 2024 01:32:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:9633d4f6d1ceb311422b86502f057cfd400959e6fa3f9fa28d6848bb6cdc9055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2312558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b9c4fe1473e54d45f0c30ca2bdaa8200d0f9e10d811703e74c27232d288313`

```dockerfile
```

-	Layers:
	-	`sha256:470d0c1e3b27df7cc86c281b0b437958b8b4742962b109311219d1d5c8d199e7`  
		Last Modified: Fri, 06 Dec 2024 01:32:17 GMT  
		Size: 2.3 MB (2291336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d21968c91e92936985a4af7a988f292a75a85b6f014bbb668a0e336ff3f0966`  
		Last Modified: Fri, 06 Dec 2024 01:32:17 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine`

```console
$ docker pull memcached@sha256:e8f244572aec9f880cbccace3a05f97f24ff71b53d8d694814748eac12f427c2
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
$ docker pull memcached@sha256:e303bdddcf04ceba4983b9b8cf8b40f8fa41a3ba2d31f7214151d17a2a3076dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6964456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f99a3c16eb499f6cdf0c4680227af234f0e81b86cbb3e219dfd1cc4d331ed8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4191c73fdb45d23dac2c68d4abc8221e6406e9b5591365424302359c1717d44f`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc8b2c6385836cdfcf380e66751377fa23d31f333b616fdd8024545be6c0cc7`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 103.8 KB (103823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77829dd883bfed11037e738040ee96033efef20717be2a3ee174be7d444bd5e3`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 3.2 MB (3235366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfc1d638a936f750e8e87da5702f5b6b5ca51380fca27d33b2f2a75c14f22ba`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b374bd2d4e1ea47b597a16a9e9e56aba35aef6fc394904249a1f2e0f08618e`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c8915813030bfdc12790cdf965af8cfe77b77f8af9f51e92837f89f9eb87c296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05abf48b9dac7138d3a7fe7d19150a99ab63e08e30d39ba567ac00a81d2f1128`

```dockerfile
```

-	Layers:
	-	`sha256:4c8e4bfd8ce93a5fb987902f718ea9389273600f0d3e9d4787a4b63df46b890a`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 88.0 KB (87997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f08348125d8660725339fdc8fac6a613450c75e943e98dc3dde6ba8364bea2cf`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 19.6 KB (19574 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:070c242a1121df9eaa6bb4151dc7c67340b8f20ef0ad5d0e049de50dd7344396
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7862766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c37e99de69f18e54515a8d3071b8ea1fd0f2a4900297a8b2c1c386a6a24b78ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb9a0a7b9b4c9f5adc5080dca4ca693f553a370e9fa64affed9aac65b383dc5`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694142e1e3f17625e53d3827671e05224425e877a3e74761c94b54645204ded1`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 121.0 KB (121021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7796589e641878ee661afd57987309f860c136ca6f4413c7d84116bd64ecad12`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 3.7 MB (3652653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29e7393633dafdad3ecd5f2432e9c09c88ae197ae63ebc39cdd5d755efc1093`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7232ef393c6312a3d76029b6d56988d15a40f595f77e0537ee596b7caaca7132`  
		Last Modified: Fri, 06 Dec 2024 01:33:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:fe3c78175237195a75aca53378025420314ce4b8bd427652e821e9663becf695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.9 KB (107872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095cd6aa8766c7a849d35f1d8a015b4b7aec092919440079533223bcd2268290`

```dockerfile
```

-	Layers:
	-	`sha256:e9f4643bf814c73775db7c54c18dd433640b2a57bca6adaf08f427cfa1bc3de1`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 88.1 KB (88101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee64ac9068d8c28d1fbbd0690d6771ea5be16985b2b5dd0fdc3e6769ec1ee14b`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 19.8 KB (19771 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:492db91f15dbd3e9e9e33a1f7e2cc09b20fae42051a02e3f0de5acd8454a316c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6646126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3ad52f1373f146c439a3c8e68b2d6ed471a4db701c049fd0b5ffea34119f61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bfed8762acb5fad17a943b928db6acd316a3f41770d6ccb3ccde6c5058de8d6`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f39ea1560a9fce397084caa49fd70c40dc655e0857cec268d76a430c74e7b9`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 109.0 KB (108960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a781c1b2a58f8cf6bd9facbe1e1ad73be61573272f8914f2dd4bf85d4ff0baad`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 3.1 MB (3066579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b827afe494b121a7e333c94baa21f20421366c2bb0f1e0eeb73e437c52ff40`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9d6c0f8c12091da40ce7700dcb522ce3106703627f2a754241cdb1bbc845d1`  
		Last Modified: Fri, 06 Dec 2024 01:31:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c91fa3449f439c4e9c30c88fa79e5fe63d3bf8af8356defc87da1e56609349ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ee8dfa6edf9c1a3e3b579f7f9fce0a46eb85e82ae82e1e5364b961be5801ca`

```dockerfile
```

-	Layers:
	-	`sha256:a3eb59cf4c9b8cc00383cca89ed90cd3e204f3e898b960d8fb6aea259589e2f3`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 88.0 KB (87952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3242abd4e76a0a4671ab58ff40ccc25a63d6e796bdf01ab8238cd61b52844e92`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 19.5 KB (19516 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:9ed77a1e3df85d41958cfab6678f84b7a0c5478c3ee4031bb4ef7009ae148a8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6838378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7debc910ab631f46ff86577268f8190435a1a1cad3c4f28c2a14839844c89ec6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac7c2caa12b9b7c688356275a58d0faa1e26ca96ea89c8041aca795343d90fb`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0955050f3ec94864d6e58cb0e77be49260e6358a11bcfe4f18fcd7a16ef98bd`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 123.0 KB (123004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1076a55e57cd99a295a1a9b0943a35ef12c0cbefcee0f539ebc0f9d767f09ac7`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 3.1 MB (3141546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd0157cad0ccfad57f8818a6674665d46df00b03abce2b8b0a4b2b55bc097af`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200b295ab1fad685ec6581c5220bd29b35b4de15dd7b79b1670cc8c3a5318ff1`  
		Last Modified: Fri, 06 Dec 2024 01:33:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:44ef397246da32f636714921281ea510a545706dff7755d39ed522fd34ef818c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.7 KB (105748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27dd5988cf9c77426d5d3ce108181cfde561e89d21a1e57c46b06a24494bc24`

```dockerfile
```

-	Layers:
	-	`sha256:9dd942067c2d5eec8c44d618b60a4fb2d533da4aaa9e59aa658035bae7864153`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 86.1 KB (86101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7ae50a8f9772a347faf3150966eb0a294bad1037dcd82a6b7ca6e7085def4b0`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 19.6 KB (19647 bytes)  
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
$ docker pull memcached@sha256:2f9e35d548959a8ea66fbb14b4e45db6201bd399fbce7aa6a91ced6724529015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6590517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e59cf784613df48eaa8bb5d47ccb40bb41263090034725c38a1d343c40fdc98b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd586bc77f5fb181172c996290db7374e9c10d57409c2b44fd564414325e007`  
		Last Modified: Fri, 06 Dec 2024 01:36:13 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0fcd80ecbef8175a68d824552ed0f114429b0267802305d4c7d844c3577627e`  
		Last Modified: Fri, 06 Dec 2024 01:36:13 GMT  
		Size: 112.8 KB (112750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec43a227c373cac7def72eaec9a32204740c8000aa305974e2bdb1684ee66532`  
		Last Modified: Fri, 06 Dec 2024 01:36:13 GMT  
		Size: 3.0 MB (3014795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c4d2f183090b5a127cca23a337b895f3cf87bf67d4f7753457dda9b9e71179`  
		Last Modified: Fri, 06 Dec 2024 01:36:14 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e27bc505bddda3fa278b4085496625d324fb6e550b22e4eed35b931033473d7`  
		Last Modified: Fri, 06 Dec 2024 01:36:14 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:19d143dfb5e455c347101473ad04cdac2e988e4db9be4af04174526f0d488453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185266b3e1c500c32f3ce16d81debe696e90be32f272cd58900e7e79549f53f4`

```dockerfile
```

-	Layers:
	-	`sha256:cb583c39b213e1d44b5dc21216421e4b8ff1f212376d783788f7ecec530ffbdd`  
		Last Modified: Fri, 06 Dec 2024 01:36:13 GMT  
		Size: 86.0 KB (86043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d788cea57935c2cb3c0e8b4293caec6b1447956196a6739ddf9264bcb76563a9`  
		Last Modified: Fri, 06 Dec 2024 01:36:13 GMT  
		Size: 19.6 KB (19574 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine3.20`

```console
$ docker pull memcached@sha256:e8f244572aec9f880cbccace3a05f97f24ff71b53d8d694814748eac12f427c2
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

### `memcached:1.6-alpine3.20` - linux; amd64

```console
$ docker pull memcached@sha256:e303bdddcf04ceba4983b9b8cf8b40f8fa41a3ba2d31f7214151d17a2a3076dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6964456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f99a3c16eb499f6cdf0c4680227af234f0e81b86cbb3e219dfd1cc4d331ed8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4191c73fdb45d23dac2c68d4abc8221e6406e9b5591365424302359c1717d44f`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc8b2c6385836cdfcf380e66751377fa23d31f333b616fdd8024545be6c0cc7`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 103.8 KB (103823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77829dd883bfed11037e738040ee96033efef20717be2a3ee174be7d444bd5e3`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 3.2 MB (3235366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfc1d638a936f750e8e87da5702f5b6b5ca51380fca27d33b2f2a75c14f22ba`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b374bd2d4e1ea47b597a16a9e9e56aba35aef6fc394904249a1f2e0f08618e`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:c8915813030bfdc12790cdf965af8cfe77b77f8af9f51e92837f89f9eb87c296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05abf48b9dac7138d3a7fe7d19150a99ab63e08e30d39ba567ac00a81d2f1128`

```dockerfile
```

-	Layers:
	-	`sha256:4c8e4bfd8ce93a5fb987902f718ea9389273600f0d3e9d4787a4b63df46b890a`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 88.0 KB (87997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f08348125d8660725339fdc8fac6a613450c75e943e98dc3dde6ba8364bea2cf`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 19.6 KB (19574 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:070c242a1121df9eaa6bb4151dc7c67340b8f20ef0ad5d0e049de50dd7344396
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7862766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c37e99de69f18e54515a8d3071b8ea1fd0f2a4900297a8b2c1c386a6a24b78ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb9a0a7b9b4c9f5adc5080dca4ca693f553a370e9fa64affed9aac65b383dc5`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694142e1e3f17625e53d3827671e05224425e877a3e74761c94b54645204ded1`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 121.0 KB (121021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7796589e641878ee661afd57987309f860c136ca6f4413c7d84116bd64ecad12`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 3.7 MB (3652653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29e7393633dafdad3ecd5f2432e9c09c88ae197ae63ebc39cdd5d755efc1093`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7232ef393c6312a3d76029b6d56988d15a40f595f77e0537ee596b7caaca7132`  
		Last Modified: Fri, 06 Dec 2024 01:33:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:fe3c78175237195a75aca53378025420314ce4b8bd427652e821e9663becf695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.9 KB (107872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095cd6aa8766c7a849d35f1d8a015b4b7aec092919440079533223bcd2268290`

```dockerfile
```

-	Layers:
	-	`sha256:e9f4643bf814c73775db7c54c18dd433640b2a57bca6adaf08f427cfa1bc3de1`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 88.1 KB (88101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee64ac9068d8c28d1fbbd0690d6771ea5be16985b2b5dd0fdc3e6769ec1ee14b`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 19.8 KB (19771 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.20` - linux; 386

```console
$ docker pull memcached@sha256:492db91f15dbd3e9e9e33a1f7e2cc09b20fae42051a02e3f0de5acd8454a316c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6646126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3ad52f1373f146c439a3c8e68b2d6ed471a4db701c049fd0b5ffea34119f61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bfed8762acb5fad17a943b928db6acd316a3f41770d6ccb3ccde6c5058de8d6`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f39ea1560a9fce397084caa49fd70c40dc655e0857cec268d76a430c74e7b9`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 109.0 KB (108960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a781c1b2a58f8cf6bd9facbe1e1ad73be61573272f8914f2dd4bf85d4ff0baad`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 3.1 MB (3066579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b827afe494b121a7e333c94baa21f20421366c2bb0f1e0eeb73e437c52ff40`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9d6c0f8c12091da40ce7700dcb522ce3106703627f2a754241cdb1bbc845d1`  
		Last Modified: Fri, 06 Dec 2024 01:31:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:c91fa3449f439c4e9c30c88fa79e5fe63d3bf8af8356defc87da1e56609349ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ee8dfa6edf9c1a3e3b579f7f9fce0a46eb85e82ae82e1e5364b961be5801ca`

```dockerfile
```

-	Layers:
	-	`sha256:a3eb59cf4c9b8cc00383cca89ed90cd3e204f3e898b960d8fb6aea259589e2f3`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 88.0 KB (87952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3242abd4e76a0a4671ab58ff40ccc25a63d6e796bdf01ab8238cd61b52844e92`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 19.5 KB (19516 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.20` - linux; ppc64le

```console
$ docker pull memcached@sha256:9ed77a1e3df85d41958cfab6678f84b7a0c5478c3ee4031bb4ef7009ae148a8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6838378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7debc910ab631f46ff86577268f8190435a1a1cad3c4f28c2a14839844c89ec6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac7c2caa12b9b7c688356275a58d0faa1e26ca96ea89c8041aca795343d90fb`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0955050f3ec94864d6e58cb0e77be49260e6358a11bcfe4f18fcd7a16ef98bd`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 123.0 KB (123004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1076a55e57cd99a295a1a9b0943a35ef12c0cbefcee0f539ebc0f9d767f09ac7`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 3.1 MB (3141546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd0157cad0ccfad57f8818a6674665d46df00b03abce2b8b0a4b2b55bc097af`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200b295ab1fad685ec6581c5220bd29b35b4de15dd7b79b1670cc8c3a5318ff1`  
		Last Modified: Fri, 06 Dec 2024 01:33:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:44ef397246da32f636714921281ea510a545706dff7755d39ed522fd34ef818c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.7 KB (105748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27dd5988cf9c77426d5d3ce108181cfde561e89d21a1e57c46b06a24494bc24`

```dockerfile
```

-	Layers:
	-	`sha256:9dd942067c2d5eec8c44d618b60a4fb2d533da4aaa9e59aa658035bae7864153`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 86.1 KB (86101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7ae50a8f9772a347faf3150966eb0a294bad1037dcd82a6b7ca6e7085def4b0`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 19.6 KB (19647 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.20` - linux; riscv64

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

### `memcached:1.6-alpine3.20` - unknown; unknown

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

### `memcached:1.6-alpine3.20` - linux; s390x

```console
$ docker pull memcached@sha256:2f9e35d548959a8ea66fbb14b4e45db6201bd399fbce7aa6a91ced6724529015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6590517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e59cf784613df48eaa8bb5d47ccb40bb41263090034725c38a1d343c40fdc98b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd586bc77f5fb181172c996290db7374e9c10d57409c2b44fd564414325e007`  
		Last Modified: Fri, 06 Dec 2024 01:36:13 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0fcd80ecbef8175a68d824552ed0f114429b0267802305d4c7d844c3577627e`  
		Last Modified: Fri, 06 Dec 2024 01:36:13 GMT  
		Size: 112.8 KB (112750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec43a227c373cac7def72eaec9a32204740c8000aa305974e2bdb1684ee66532`  
		Last Modified: Fri, 06 Dec 2024 01:36:13 GMT  
		Size: 3.0 MB (3014795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c4d2f183090b5a127cca23a337b895f3cf87bf67d4f7753457dda9b9e71179`  
		Last Modified: Fri, 06 Dec 2024 01:36:14 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e27bc505bddda3fa278b4085496625d324fb6e550b22e4eed35b931033473d7`  
		Last Modified: Fri, 06 Dec 2024 01:36:14 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:19d143dfb5e455c347101473ad04cdac2e988e4db9be4af04174526f0d488453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185266b3e1c500c32f3ce16d81debe696e90be32f272cd58900e7e79549f53f4`

```dockerfile
```

-	Layers:
	-	`sha256:cb583c39b213e1d44b5dc21216421e4b8ff1f212376d783788f7ecec530ffbdd`  
		Last Modified: Fri, 06 Dec 2024 01:36:13 GMT  
		Size: 86.0 KB (86043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d788cea57935c2cb3c0e8b4293caec6b1447956196a6739ddf9264bcb76563a9`  
		Last Modified: Fri, 06 Dec 2024 01:36:13 GMT  
		Size: 19.6 KB (19574 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-bookworm`

```console
$ docker pull memcached@sha256:b8cb0ed0bf5d3d38f9606fc847c9a21baa68952472ea29a5a685f82a1efc2987
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
$ docker pull memcached@sha256:1e2854f49ddb3fc0103bf7b8fcd80ed47c6f72e2aa74ad0848acc1274e4f98f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31984433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04abd86d309da60dfe2b7f4f4e20226dd5f87fe17482740074bbc2c6865d6987`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977f47ceef0f8173cff02fe737b3fd37efab540ec727c2a20869e90ab8279920`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1599032aa7639a9095e216c0b122c7eb2cf54392a6e7bf2d191ff3e086bb478a`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 2.5 MB (2491759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:034904c659cc08a9f86d31858f173bfc3a20727cb5fb51319eb9478c29151562`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 1.3 MB (1259579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbc04f1662c41c4314f0f2a27cbf319464d441170360aee7702dd51be327e76`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4e9ce09f9de3f7835981235d8000bd031663f2328a8e4ffb2f6b6e9d1a1e0d`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:fb6b716e55ea5a7353f965101017052ad92d603abfbd05eb49dc5aeceea69dfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2312843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2806c278d65e027e6b4619f466776331a5efde1eb1992a4a013a5e85ae769111`

```dockerfile
```

-	Layers:
	-	`sha256:a489ae83eb749729e07a801603bdc10563b8508b7272d035a9f58304ea805e5c`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 2.3 MB (2291621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbb57e1ba346b719e10354837a9bef89546f505a248a0977af44ec554c92262a`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:91ab868f687f5d84ed97501641c6276629ba558cf3b893411d4bff8ddf3b7a20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29090498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddac0a9030226a9353757b40367ccad4e58abf3df5f1cecab9445504a7141a50`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:25d432086d20067bebfff2b163f22d49e7da8528782652615fe170bf8c39194d`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 25.8 MB (25754926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29864ebc65411065e6cc80afcb839ecd53357c5d8accb084195a861ffe331f0c`  
		Last Modified: Tue, 03 Dec 2024 02:34:22 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17b8bb45df912fe349545bf67aeee395da8a6bbd8c9fd4b4bba4ab37d4c46e6`  
		Last Modified: Tue, 03 Dec 2024 02:34:23 GMT  
		Size: 2.1 MB (2096040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f971acf6335510d8cd95bbf08ed1b82d5ccdbb6a46d5cc4004f4d3f17f79ad22`  
		Last Modified: Fri, 06 Dec 2024 01:31:23 GMT  
		Size: 1.2 MB (1238020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d2f4b78825fe502c36e4f1340340617bc5d281e1a4d0bfd9c29b683505190d`  
		Last Modified: Fri, 06 Dec 2024 01:31:23 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0b278088431fe97844cee08594eb17b8a478179969a38c2138afcc8635209b`  
		Last Modified: Fri, 06 Dec 2024 01:31:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:33b0db124591dec0a6fd5c81068992c08e8cb9a2f4e0f7c8dd8474b34525c0f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2316527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59492fefec6386be99693d0d6d513a6c53fd5cc3e197beb39bcce988752d934b`

```dockerfile
```

-	Layers:
	-	`sha256:3183c33c304bb139731b8181094f3cedf637a75d2c2b46a39117b249bcbf9a94`  
		Last Modified: Fri, 06 Dec 2024 01:31:23 GMT  
		Size: 2.3 MB (2295158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe9afff481d34963c12864f80d0a8758b8462fbfbdf815070d7b572ba117476b`  
		Last Modified: Fri, 06 Dec 2024 01:31:23 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:4b50248c9ebc50990818eb60f6c506e07a29315de1cf92f8089ce198db55f78f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31670277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae090e1fc19e90d2a650cdd682ddd6cebff3ef4c472411c422c7b772f9c7844a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78a410ea91650a45f4516634a8253fbca2d2238ebd376ee434a91c97add0d41`  
		Last Modified: Tue, 03 Dec 2024 02:56:13 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3651f43c686dcae90b2bb5bfaafb1c1e92231bce87f7c2a4f7f92606b3f6048`  
		Last Modified: Tue, 03 Dec 2024 02:56:14 GMT  
		Size: 2.4 MB (2355349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1974b3b5f9215ed5e7c38499590f73f9d2cc9f0eab4b5bfc835e795f011b6ec`  
		Last Modified: Fri, 06 Dec 2024 01:31:13 GMT  
		Size: 1.3 MB (1254605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0d87f19f5dcc124861cef54d5060fdddf78285679e5e18c5c228a649873178`  
		Last Modified: Fri, 06 Dec 2024 01:31:12 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4e9ce09f9de3f7835981235d8000bd031663f2328a8e4ffb2f6b6e9d1a1e0d`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:65ec047e972b106c4dccd5e7db2375b427183eaa0a17d24a87733f0781a6f4cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2313354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6be2bd8ba74100235eb2a7790cd07be00c97e00f811e0074913d8ef6bce12587`

```dockerfile
```

-	Layers:
	-	`sha256:aea7e31a5ac097dbe2c1f459e15d324e0b4c270652bc090fc7bb75b32d29171f`  
		Last Modified: Fri, 06 Dec 2024 01:31:13 GMT  
		Size: 2.3 MB (2291935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72554d4560a983cd304f173578e432f68442018a3d2f900c20e8692c7507475d`  
		Last Modified: Fri, 06 Dec 2024 01:31:12 GMT  
		Size: 21.4 KB (21419 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:2ee1837e5180933d5ce36c27a48671480a1269845d9fe11427b429f7ddcb89e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32967293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa8709f96acad9a15c63279cf937b75d01dd91a1585ac5ca41256e80e432a0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ae6c80ee852fcccae85579165042a3767dcd1190112e87c9f22fa3e76a624c73`  
		Last Modified: Tue, 03 Dec 2024 01:27:10 GMT  
		Size: 29.2 MB (29205487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580dd662e45fd4b251d3406f5a1ea8962e3e4e1d2520efbb737df740b7e957f2`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3f1598f54c5456764cfdadbb7074ec777bd66ed0fab6c8fdfa5e8a435c5ae8`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 2.5 MB (2500687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd3aa7547e95a174e12f01b948f1c39aee54d184931a433b0ea5f3e180259de`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 1.3 MB (1259605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b9d8a09b833489a3bf75e47d6fc9c98a4f688e73ae311ff2277c461dc66a85`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6fe54f00cf7e2bebef13e9698cee799c63127f12560807f4bf87fda6395baf`  
		Last Modified: Fri, 06 Dec 2024 01:31:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:2029c4c3e23c8bfb7b5f3992ef8057fc969eca5273a1f436d6d8605b3ba6f081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2309883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025c0e1e5fec67ce720fae6f7e5aaaa9c8217653956e512bf60be97cb2294914`

```dockerfile
```

-	Layers:
	-	`sha256:3f7aef5b25a76a78ebdd73ae22cef84f68f0d0a920a1e0a89dab2aa1fa5accdd`  
		Last Modified: Fri, 06 Dec 2024 01:31:11 GMT  
		Size: 2.3 MB (2288719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:551482c681545d405b9f1d3139dcf0fb74b2fecfd0e7d9d54de6e57a981c3d71`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:b398c51c3b2d91d0274741650d383d12bb8dd65d4acdb202d0a7063d6e4b8b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31705243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4838f50554bb3277090b0aa55a3191c3489fc05113546999725b9c946e1a954e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:29ac4ae2849b0c84c0ef17659082268617abeb406402ef46b6fa9140e6d2064d`  
		Last Modified: Tue, 03 Dec 2024 01:28:15 GMT  
		Size: 28.5 MB (28505909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f398f0ee699c887dba3a51e3212be4320212ed287d33cdd1df41e7fd72240a7`  
		Last Modified: Fri, 06 Dec 2024 01:35:13 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7ddb249939dc734c215bc1be4a564dacdb2495a3ca51100084126ecd662f02`  
		Last Modified: Fri, 06 Dec 2024 01:35:14 GMT  
		Size: 1.9 MB (1943197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d087c96f4f05d81a987f0812e9c7c28cca806e5aa40786761696d7bd547b926a`  
		Last Modified: Fri, 06 Dec 2024 01:35:14 GMT  
		Size: 1.3 MB (1254620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec32257bb4a1a2d1b3c027ae74afbc31c03aec77c3aec28b9f546843aa638ab`  
		Last Modified: Fri, 06 Dec 2024 01:35:13 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4f728769ae3f10d5ef679ac778b45c6992248d4a8e853760525c3c24041f6f`  
		Last Modified: Fri, 06 Dec 2024 01:35:14 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f528c619723b1b912a572178e808db3bf0968e4baf6ef920992198b60a50bd7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00565dc210c91f04967e0e4b932ca263ef440c9803d1fb47313d6524c29b26f3`

```dockerfile
```

-	Layers:
	-	`sha256:4fe7144715458a1e421c93fd64b7134c4f3738eb832551e549e822b1ba66523d`  
		Last Modified: Fri, 06 Dec 2024 01:35:13 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:01b87270745db075ed8b996a903bbb03e1ce8e91a1492c6763e8e0184098bf0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36096936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca502cddeb618d1bc49dc5bc8d6538584dd37bf9fdef22011502443d817f36aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e62b6946337cc6b72ec307008f1acc46e12a4f98e6f0e29c92b5538bbafd7ce6`  
		Last Modified: Tue, 03 Dec 2024 01:28:28 GMT  
		Size: 32.1 MB (32063265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8e81ffdbb3a1a0871b7d927a02d62e2ce4eb8b6f7bbc76e4bba93c799b9075`  
		Last Modified: Tue, 03 Dec 2024 02:42:07 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0276e7f6ce6bb384613f81bb9a596143583bdbf5cac2714170243761daa43b7`  
		Last Modified: Tue, 03 Dec 2024 02:42:08 GMT  
		Size: 2.7 MB (2708555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb84fa77333d98470bc633574f7b051132ca9675ff7d781c3cce4a079186907b`  
		Last Modified: Fri, 06 Dec 2024 01:30:50 GMT  
		Size: 1.3 MB (1323604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ecb320c4cc5c4e8e57c37ce8e39a4136d2ef053377f6bc3812880eeab6f20f`  
		Last Modified: Fri, 06 Dec 2024 01:30:50 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b9e76d0bac4875861b1d66e91f0dd7273347b172785e7659835a862b71c9e2`  
		Last Modified: Fri, 06 Dec 2024 01:30:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:2416ac25dc3bb76b01b44fb54d535ad95f9e7d3f8c5cc714c15e381a4d35d0ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2317287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48fe760f47f1bdadfdc6584c4f1802c30ff05ebb44d44b931211aac3a762993f`

```dockerfile
```

-	Layers:
	-	`sha256:5f182f9c7a52c9256109712b419bb1efe3847e993e342af008724d31754d7b58`  
		Last Modified: Fri, 06 Dec 2024 01:30:50 GMT  
		Size: 2.3 MB (2295992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:373a3417f812a3143655df1a9b4ee6893a0b627316005c587b3c5ddacd6cdd6d`  
		Last Modified: Fri, 06 Dec 2024 01:30:50 GMT  
		Size: 21.3 KB (21295 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:2a204d42b50b0598b0ce8900e8bde20bcbf35f9c5cd4bbb38186b48cdac2d4d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30274542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:154623d34f127ea2636384bc7205519ccf3b1aad97280ebcdb64b7662a374040`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9378ae44108012049addde60d193467e2b15a247b2f953ad5c27e073c4573d42`  
		Last Modified: Tue, 03 Dec 2024 01:28:18 GMT  
		Size: 26.9 MB (26878971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214d47b5512f1991eb09046f46526e464102115476ac71ca1c8e7bd9439c4a5b`  
		Last Modified: Tue, 03 Dec 2024 02:32:32 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc13e1c57cbb046f722e07c9a375af936eb9f47e47a86a2435b54dc393da6657`  
		Last Modified: Tue, 03 Dec 2024 02:32:32 GMT  
		Size: 2.2 MB (2156364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cecb2200496ee18d3c1d0287a623829849840935d625131d9dded26f2bd67478`  
		Last Modified: Fri, 06 Dec 2024 01:32:17 GMT  
		Size: 1.2 MB (1237695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06048c152c70476e77823ded2b6e26aaa36538ae99b655fed345f19eacdccb3`  
		Last Modified: Fri, 06 Dec 2024 01:32:17 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad2217a2f73e7c40ee3dda6f84683bbf529af0a6c88a2f8509a8c6236fab9b3`  
		Last Modified: Fri, 06 Dec 2024 01:32:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:9633d4f6d1ceb311422b86502f057cfd400959e6fa3f9fa28d6848bb6cdc9055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2312558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b9c4fe1473e54d45f0c30ca2bdaa8200d0f9e10d811703e74c27232d288313`

```dockerfile
```

-	Layers:
	-	`sha256:470d0c1e3b27df7cc86c281b0b437958b8b4742962b109311219d1d5c8d199e7`  
		Last Modified: Fri, 06 Dec 2024 01:32:17 GMT  
		Size: 2.3 MB (2291336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d21968c91e92936985a4af7a988f292a75a85b6f014bbb668a0e336ff3f0966`  
		Last Modified: Fri, 06 Dec 2024 01:32:17 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.33`

```console
$ docker pull memcached@sha256:b8cb0ed0bf5d3d38f9606fc847c9a21baa68952472ea29a5a685f82a1efc2987
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

### `memcached:1.6.33` - linux; amd64

```console
$ docker pull memcached@sha256:1e2854f49ddb3fc0103bf7b8fcd80ed47c6f72e2aa74ad0848acc1274e4f98f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31984433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04abd86d309da60dfe2b7f4f4e20226dd5f87fe17482740074bbc2c6865d6987`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977f47ceef0f8173cff02fe737b3fd37efab540ec727c2a20869e90ab8279920`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1599032aa7639a9095e216c0b122c7eb2cf54392a6e7bf2d191ff3e086bb478a`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 2.5 MB (2491759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:034904c659cc08a9f86d31858f173bfc3a20727cb5fb51319eb9478c29151562`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 1.3 MB (1259579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbc04f1662c41c4314f0f2a27cbf319464d441170360aee7702dd51be327e76`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4e9ce09f9de3f7835981235d8000bd031663f2328a8e4ffb2f6b6e9d1a1e0d`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.33` - unknown; unknown

```console
$ docker pull memcached@sha256:fb6b716e55ea5a7353f965101017052ad92d603abfbd05eb49dc5aeceea69dfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2312843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2806c278d65e027e6b4619f466776331a5efde1eb1992a4a013a5e85ae769111`

```dockerfile
```

-	Layers:
	-	`sha256:a489ae83eb749729e07a801603bdc10563b8508b7272d035a9f58304ea805e5c`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 2.3 MB (2291621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbb57e1ba346b719e10354837a9bef89546f505a248a0977af44ec554c92262a`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.33` - linux; arm variant v5

```console
$ docker pull memcached@sha256:91ab868f687f5d84ed97501641c6276629ba558cf3b893411d4bff8ddf3b7a20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29090498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddac0a9030226a9353757b40367ccad4e58abf3df5f1cecab9445504a7141a50`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:25d432086d20067bebfff2b163f22d49e7da8528782652615fe170bf8c39194d`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 25.8 MB (25754926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29864ebc65411065e6cc80afcb839ecd53357c5d8accb084195a861ffe331f0c`  
		Last Modified: Tue, 03 Dec 2024 02:34:22 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17b8bb45df912fe349545bf67aeee395da8a6bbd8c9fd4b4bba4ab37d4c46e6`  
		Last Modified: Tue, 03 Dec 2024 02:34:23 GMT  
		Size: 2.1 MB (2096040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f971acf6335510d8cd95bbf08ed1b82d5ccdbb6a46d5cc4004f4d3f17f79ad22`  
		Last Modified: Fri, 06 Dec 2024 01:31:23 GMT  
		Size: 1.2 MB (1238020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d2f4b78825fe502c36e4f1340340617bc5d281e1a4d0bfd9c29b683505190d`  
		Last Modified: Fri, 06 Dec 2024 01:31:23 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0b278088431fe97844cee08594eb17b8a478179969a38c2138afcc8635209b`  
		Last Modified: Fri, 06 Dec 2024 01:31:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.33` - unknown; unknown

```console
$ docker pull memcached@sha256:33b0db124591dec0a6fd5c81068992c08e8cb9a2f4e0f7c8dd8474b34525c0f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2316527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59492fefec6386be99693d0d6d513a6c53fd5cc3e197beb39bcce988752d934b`

```dockerfile
```

-	Layers:
	-	`sha256:3183c33c304bb139731b8181094f3cedf637a75d2c2b46a39117b249bcbf9a94`  
		Last Modified: Fri, 06 Dec 2024 01:31:23 GMT  
		Size: 2.3 MB (2295158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe9afff481d34963c12864f80d0a8758b8462fbfbdf815070d7b572ba117476b`  
		Last Modified: Fri, 06 Dec 2024 01:31:23 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.33` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:4b50248c9ebc50990818eb60f6c506e07a29315de1cf92f8089ce198db55f78f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31670277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae090e1fc19e90d2a650cdd682ddd6cebff3ef4c472411c422c7b772f9c7844a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78a410ea91650a45f4516634a8253fbca2d2238ebd376ee434a91c97add0d41`  
		Last Modified: Tue, 03 Dec 2024 02:56:13 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3651f43c686dcae90b2bb5bfaafb1c1e92231bce87f7c2a4f7f92606b3f6048`  
		Last Modified: Tue, 03 Dec 2024 02:56:14 GMT  
		Size: 2.4 MB (2355349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1974b3b5f9215ed5e7c38499590f73f9d2cc9f0eab4b5bfc835e795f011b6ec`  
		Last Modified: Fri, 06 Dec 2024 01:31:13 GMT  
		Size: 1.3 MB (1254605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0d87f19f5dcc124861cef54d5060fdddf78285679e5e18c5c228a649873178`  
		Last Modified: Fri, 06 Dec 2024 01:31:12 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4e9ce09f9de3f7835981235d8000bd031663f2328a8e4ffb2f6b6e9d1a1e0d`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.33` - unknown; unknown

```console
$ docker pull memcached@sha256:65ec047e972b106c4dccd5e7db2375b427183eaa0a17d24a87733f0781a6f4cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2313354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6be2bd8ba74100235eb2a7790cd07be00c97e00f811e0074913d8ef6bce12587`

```dockerfile
```

-	Layers:
	-	`sha256:aea7e31a5ac097dbe2c1f459e15d324e0b4c270652bc090fc7bb75b32d29171f`  
		Last Modified: Fri, 06 Dec 2024 01:31:13 GMT  
		Size: 2.3 MB (2291935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72554d4560a983cd304f173578e432f68442018a3d2f900c20e8692c7507475d`  
		Last Modified: Fri, 06 Dec 2024 01:31:12 GMT  
		Size: 21.4 KB (21419 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.33` - linux; 386

```console
$ docker pull memcached@sha256:2ee1837e5180933d5ce36c27a48671480a1269845d9fe11427b429f7ddcb89e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32967293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa8709f96acad9a15c63279cf937b75d01dd91a1585ac5ca41256e80e432a0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ae6c80ee852fcccae85579165042a3767dcd1190112e87c9f22fa3e76a624c73`  
		Last Modified: Tue, 03 Dec 2024 01:27:10 GMT  
		Size: 29.2 MB (29205487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580dd662e45fd4b251d3406f5a1ea8962e3e4e1d2520efbb737df740b7e957f2`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3f1598f54c5456764cfdadbb7074ec777bd66ed0fab6c8fdfa5e8a435c5ae8`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 2.5 MB (2500687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd3aa7547e95a174e12f01b948f1c39aee54d184931a433b0ea5f3e180259de`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 1.3 MB (1259605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b9d8a09b833489a3bf75e47d6fc9c98a4f688e73ae311ff2277c461dc66a85`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6fe54f00cf7e2bebef13e9698cee799c63127f12560807f4bf87fda6395baf`  
		Last Modified: Fri, 06 Dec 2024 01:31:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.33` - unknown; unknown

```console
$ docker pull memcached@sha256:2029c4c3e23c8bfb7b5f3992ef8057fc969eca5273a1f436d6d8605b3ba6f081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2309883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025c0e1e5fec67ce720fae6f7e5aaaa9c8217653956e512bf60be97cb2294914`

```dockerfile
```

-	Layers:
	-	`sha256:3f7aef5b25a76a78ebdd73ae22cef84f68f0d0a920a1e0a89dab2aa1fa5accdd`  
		Last Modified: Fri, 06 Dec 2024 01:31:11 GMT  
		Size: 2.3 MB (2288719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:551482c681545d405b9f1d3139dcf0fb74b2fecfd0e7d9d54de6e57a981c3d71`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.33` - linux; mips64le

```console
$ docker pull memcached@sha256:b398c51c3b2d91d0274741650d383d12bb8dd65d4acdb202d0a7063d6e4b8b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31705243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4838f50554bb3277090b0aa55a3191c3489fc05113546999725b9c946e1a954e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:29ac4ae2849b0c84c0ef17659082268617abeb406402ef46b6fa9140e6d2064d`  
		Last Modified: Tue, 03 Dec 2024 01:28:15 GMT  
		Size: 28.5 MB (28505909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f398f0ee699c887dba3a51e3212be4320212ed287d33cdd1df41e7fd72240a7`  
		Last Modified: Fri, 06 Dec 2024 01:35:13 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7ddb249939dc734c215bc1be4a564dacdb2495a3ca51100084126ecd662f02`  
		Last Modified: Fri, 06 Dec 2024 01:35:14 GMT  
		Size: 1.9 MB (1943197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d087c96f4f05d81a987f0812e9c7c28cca806e5aa40786761696d7bd547b926a`  
		Last Modified: Fri, 06 Dec 2024 01:35:14 GMT  
		Size: 1.3 MB (1254620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec32257bb4a1a2d1b3c027ae74afbc31c03aec77c3aec28b9f546843aa638ab`  
		Last Modified: Fri, 06 Dec 2024 01:35:13 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4f728769ae3f10d5ef679ac778b45c6992248d4a8e853760525c3c24041f6f`  
		Last Modified: Fri, 06 Dec 2024 01:35:14 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.33` - unknown; unknown

```console
$ docker pull memcached@sha256:f528c619723b1b912a572178e808db3bf0968e4baf6ef920992198b60a50bd7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00565dc210c91f04967e0e4b932ca263ef440c9803d1fb47313d6524c29b26f3`

```dockerfile
```

-	Layers:
	-	`sha256:4fe7144715458a1e421c93fd64b7134c4f3738eb832551e549e822b1ba66523d`  
		Last Modified: Fri, 06 Dec 2024 01:35:13 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.33` - linux; ppc64le

```console
$ docker pull memcached@sha256:01b87270745db075ed8b996a903bbb03e1ce8e91a1492c6763e8e0184098bf0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36096936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca502cddeb618d1bc49dc5bc8d6538584dd37bf9fdef22011502443d817f36aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e62b6946337cc6b72ec307008f1acc46e12a4f98e6f0e29c92b5538bbafd7ce6`  
		Last Modified: Tue, 03 Dec 2024 01:28:28 GMT  
		Size: 32.1 MB (32063265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8e81ffdbb3a1a0871b7d927a02d62e2ce4eb8b6f7bbc76e4bba93c799b9075`  
		Last Modified: Tue, 03 Dec 2024 02:42:07 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0276e7f6ce6bb384613f81bb9a596143583bdbf5cac2714170243761daa43b7`  
		Last Modified: Tue, 03 Dec 2024 02:42:08 GMT  
		Size: 2.7 MB (2708555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb84fa77333d98470bc633574f7b051132ca9675ff7d781c3cce4a079186907b`  
		Last Modified: Fri, 06 Dec 2024 01:30:50 GMT  
		Size: 1.3 MB (1323604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ecb320c4cc5c4e8e57c37ce8e39a4136d2ef053377f6bc3812880eeab6f20f`  
		Last Modified: Fri, 06 Dec 2024 01:30:50 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b9e76d0bac4875861b1d66e91f0dd7273347b172785e7659835a862b71c9e2`  
		Last Modified: Fri, 06 Dec 2024 01:30:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.33` - unknown; unknown

```console
$ docker pull memcached@sha256:2416ac25dc3bb76b01b44fb54d535ad95f9e7d3f8c5cc714c15e381a4d35d0ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2317287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48fe760f47f1bdadfdc6584c4f1802c30ff05ebb44d44b931211aac3a762993f`

```dockerfile
```

-	Layers:
	-	`sha256:5f182f9c7a52c9256109712b419bb1efe3847e993e342af008724d31754d7b58`  
		Last Modified: Fri, 06 Dec 2024 01:30:50 GMT  
		Size: 2.3 MB (2295992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:373a3417f812a3143655df1a9b4ee6893a0b627316005c587b3c5ddacd6cdd6d`  
		Last Modified: Fri, 06 Dec 2024 01:30:50 GMT  
		Size: 21.3 KB (21295 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.33` - linux; s390x

```console
$ docker pull memcached@sha256:2a204d42b50b0598b0ce8900e8bde20bcbf35f9c5cd4bbb38186b48cdac2d4d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30274542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:154623d34f127ea2636384bc7205519ccf3b1aad97280ebcdb64b7662a374040`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9378ae44108012049addde60d193467e2b15a247b2f953ad5c27e073c4573d42`  
		Last Modified: Tue, 03 Dec 2024 01:28:18 GMT  
		Size: 26.9 MB (26878971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214d47b5512f1991eb09046f46526e464102115476ac71ca1c8e7bd9439c4a5b`  
		Last Modified: Tue, 03 Dec 2024 02:32:32 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc13e1c57cbb046f722e07c9a375af936eb9f47e47a86a2435b54dc393da6657`  
		Last Modified: Tue, 03 Dec 2024 02:32:32 GMT  
		Size: 2.2 MB (2156364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cecb2200496ee18d3c1d0287a623829849840935d625131d9dded26f2bd67478`  
		Last Modified: Fri, 06 Dec 2024 01:32:17 GMT  
		Size: 1.2 MB (1237695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06048c152c70476e77823ded2b6e26aaa36538ae99b655fed345f19eacdccb3`  
		Last Modified: Fri, 06 Dec 2024 01:32:17 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad2217a2f73e7c40ee3dda6f84683bbf529af0a6c88a2f8509a8c6236fab9b3`  
		Last Modified: Fri, 06 Dec 2024 01:32:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.33` - unknown; unknown

```console
$ docker pull memcached@sha256:9633d4f6d1ceb311422b86502f057cfd400959e6fa3f9fa28d6848bb6cdc9055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2312558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b9c4fe1473e54d45f0c30ca2bdaa8200d0f9e10d811703e74c27232d288313`

```dockerfile
```

-	Layers:
	-	`sha256:470d0c1e3b27df7cc86c281b0b437958b8b4742962b109311219d1d5c8d199e7`  
		Last Modified: Fri, 06 Dec 2024 01:32:17 GMT  
		Size: 2.3 MB (2291336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d21968c91e92936985a4af7a988f292a75a85b6f014bbb668a0e336ff3f0966`  
		Last Modified: Fri, 06 Dec 2024 01:32:17 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.33-alpine`

```console
$ docker pull memcached@sha256:7e7f6f2a7fac3e41af0e1cd2d5ebb5c93fdc4a3c7fde9db44934aa7b5eea715a
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

### `memcached:1.6.33-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:e303bdddcf04ceba4983b9b8cf8b40f8fa41a3ba2d31f7214151d17a2a3076dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6964456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f99a3c16eb499f6cdf0c4680227af234f0e81b86cbb3e219dfd1cc4d331ed8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4191c73fdb45d23dac2c68d4abc8221e6406e9b5591365424302359c1717d44f`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc8b2c6385836cdfcf380e66751377fa23d31f333b616fdd8024545be6c0cc7`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 103.8 KB (103823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77829dd883bfed11037e738040ee96033efef20717be2a3ee174be7d444bd5e3`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 3.2 MB (3235366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfc1d638a936f750e8e87da5702f5b6b5ca51380fca27d33b2f2a75c14f22ba`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b374bd2d4e1ea47b597a16a9e9e56aba35aef6fc394904249a1f2e0f08618e`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.33-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c8915813030bfdc12790cdf965af8cfe77b77f8af9f51e92837f89f9eb87c296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05abf48b9dac7138d3a7fe7d19150a99ab63e08e30d39ba567ac00a81d2f1128`

```dockerfile
```

-	Layers:
	-	`sha256:4c8e4bfd8ce93a5fb987902f718ea9389273600f0d3e9d4787a4b63df46b890a`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 88.0 KB (87997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f08348125d8660725339fdc8fac6a613450c75e943e98dc3dde6ba8364bea2cf`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 19.6 KB (19574 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.33-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:070c242a1121df9eaa6bb4151dc7c67340b8f20ef0ad5d0e049de50dd7344396
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7862766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c37e99de69f18e54515a8d3071b8ea1fd0f2a4900297a8b2c1c386a6a24b78ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb9a0a7b9b4c9f5adc5080dca4ca693f553a370e9fa64affed9aac65b383dc5`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694142e1e3f17625e53d3827671e05224425e877a3e74761c94b54645204ded1`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 121.0 KB (121021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7796589e641878ee661afd57987309f860c136ca6f4413c7d84116bd64ecad12`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 3.7 MB (3652653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29e7393633dafdad3ecd5f2432e9c09c88ae197ae63ebc39cdd5d755efc1093`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7232ef393c6312a3d76029b6d56988d15a40f595f77e0537ee596b7caaca7132`  
		Last Modified: Fri, 06 Dec 2024 01:33:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.33-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:fe3c78175237195a75aca53378025420314ce4b8bd427652e821e9663becf695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.9 KB (107872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095cd6aa8766c7a849d35f1d8a015b4b7aec092919440079533223bcd2268290`

```dockerfile
```

-	Layers:
	-	`sha256:e9f4643bf814c73775db7c54c18dd433640b2a57bca6adaf08f427cfa1bc3de1`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 88.1 KB (88101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee64ac9068d8c28d1fbbd0690d6771ea5be16985b2b5dd0fdc3e6769ec1ee14b`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 19.8 KB (19771 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.33-alpine` - linux; 386

```console
$ docker pull memcached@sha256:492db91f15dbd3e9e9e33a1f7e2cc09b20fae42051a02e3f0de5acd8454a316c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6646126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3ad52f1373f146c439a3c8e68b2d6ed471a4db701c049fd0b5ffea34119f61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bfed8762acb5fad17a943b928db6acd316a3f41770d6ccb3ccde6c5058de8d6`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f39ea1560a9fce397084caa49fd70c40dc655e0857cec268d76a430c74e7b9`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 109.0 KB (108960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a781c1b2a58f8cf6bd9facbe1e1ad73be61573272f8914f2dd4bf85d4ff0baad`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 3.1 MB (3066579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b827afe494b121a7e333c94baa21f20421366c2bb0f1e0eeb73e437c52ff40`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9d6c0f8c12091da40ce7700dcb522ce3106703627f2a754241cdb1bbc845d1`  
		Last Modified: Fri, 06 Dec 2024 01:31:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.33-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c91fa3449f439c4e9c30c88fa79e5fe63d3bf8af8356defc87da1e56609349ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ee8dfa6edf9c1a3e3b579f7f9fce0a46eb85e82ae82e1e5364b961be5801ca`

```dockerfile
```

-	Layers:
	-	`sha256:a3eb59cf4c9b8cc00383cca89ed90cd3e204f3e898b960d8fb6aea259589e2f3`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 88.0 KB (87952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3242abd4e76a0a4671ab58ff40ccc25a63d6e796bdf01ab8238cd61b52844e92`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 19.5 KB (19516 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.33-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:9ed77a1e3df85d41958cfab6678f84b7a0c5478c3ee4031bb4ef7009ae148a8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6838378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7debc910ab631f46ff86577268f8190435a1a1cad3c4f28c2a14839844c89ec6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac7c2caa12b9b7c688356275a58d0faa1e26ca96ea89c8041aca795343d90fb`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0955050f3ec94864d6e58cb0e77be49260e6358a11bcfe4f18fcd7a16ef98bd`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 123.0 KB (123004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1076a55e57cd99a295a1a9b0943a35ef12c0cbefcee0f539ebc0f9d767f09ac7`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 3.1 MB (3141546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd0157cad0ccfad57f8818a6674665d46df00b03abce2b8b0a4b2b55bc097af`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200b295ab1fad685ec6581c5220bd29b35b4de15dd7b79b1670cc8c3a5318ff1`  
		Last Modified: Fri, 06 Dec 2024 01:33:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.33-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:44ef397246da32f636714921281ea510a545706dff7755d39ed522fd34ef818c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.7 KB (105748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27dd5988cf9c77426d5d3ce108181cfde561e89d21a1e57c46b06a24494bc24`

```dockerfile
```

-	Layers:
	-	`sha256:9dd942067c2d5eec8c44d618b60a4fb2d533da4aaa9e59aa658035bae7864153`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 86.1 KB (86101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7ae50a8f9772a347faf3150966eb0a294bad1037dcd82a6b7ca6e7085def4b0`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 19.6 KB (19647 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.33-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:2f9e35d548959a8ea66fbb14b4e45db6201bd399fbce7aa6a91ced6724529015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6590517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e59cf784613df48eaa8bb5d47ccb40bb41263090034725c38a1d343c40fdc98b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd586bc77f5fb181172c996290db7374e9c10d57409c2b44fd564414325e007`  
		Last Modified: Fri, 06 Dec 2024 01:36:13 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0fcd80ecbef8175a68d824552ed0f114429b0267802305d4c7d844c3577627e`  
		Last Modified: Fri, 06 Dec 2024 01:36:13 GMT  
		Size: 112.8 KB (112750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec43a227c373cac7def72eaec9a32204740c8000aa305974e2bdb1684ee66532`  
		Last Modified: Fri, 06 Dec 2024 01:36:13 GMT  
		Size: 3.0 MB (3014795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c4d2f183090b5a127cca23a337b895f3cf87bf67d4f7753457dda9b9e71179`  
		Last Modified: Fri, 06 Dec 2024 01:36:14 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e27bc505bddda3fa278b4085496625d324fb6e550b22e4eed35b931033473d7`  
		Last Modified: Fri, 06 Dec 2024 01:36:14 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.33-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:19d143dfb5e455c347101473ad04cdac2e988e4db9be4af04174526f0d488453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185266b3e1c500c32f3ce16d81debe696e90be32f272cd58900e7e79549f53f4`

```dockerfile
```

-	Layers:
	-	`sha256:cb583c39b213e1d44b5dc21216421e4b8ff1f212376d783788f7ecec530ffbdd`  
		Last Modified: Fri, 06 Dec 2024 01:36:13 GMT  
		Size: 86.0 KB (86043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d788cea57935c2cb3c0e8b4293caec6b1447956196a6739ddf9264bcb76563a9`  
		Last Modified: Fri, 06 Dec 2024 01:36:13 GMT  
		Size: 19.6 KB (19574 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.33-alpine3.20`

```console
$ docker pull memcached@sha256:7e7f6f2a7fac3e41af0e1cd2d5ebb5c93fdc4a3c7fde9db44934aa7b5eea715a
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

### `memcached:1.6.33-alpine3.20` - linux; amd64

```console
$ docker pull memcached@sha256:e303bdddcf04ceba4983b9b8cf8b40f8fa41a3ba2d31f7214151d17a2a3076dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6964456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f99a3c16eb499f6cdf0c4680227af234f0e81b86cbb3e219dfd1cc4d331ed8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4191c73fdb45d23dac2c68d4abc8221e6406e9b5591365424302359c1717d44f`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc8b2c6385836cdfcf380e66751377fa23d31f333b616fdd8024545be6c0cc7`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 103.8 KB (103823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77829dd883bfed11037e738040ee96033efef20717be2a3ee174be7d444bd5e3`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 3.2 MB (3235366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfc1d638a936f750e8e87da5702f5b6b5ca51380fca27d33b2f2a75c14f22ba`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b374bd2d4e1ea47b597a16a9e9e56aba35aef6fc394904249a1f2e0f08618e`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.33-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:c8915813030bfdc12790cdf965af8cfe77b77f8af9f51e92837f89f9eb87c296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05abf48b9dac7138d3a7fe7d19150a99ab63e08e30d39ba567ac00a81d2f1128`

```dockerfile
```

-	Layers:
	-	`sha256:4c8e4bfd8ce93a5fb987902f718ea9389273600f0d3e9d4787a4b63df46b890a`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 88.0 KB (87997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f08348125d8660725339fdc8fac6a613450c75e943e98dc3dde6ba8364bea2cf`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 19.6 KB (19574 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.33-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:070c242a1121df9eaa6bb4151dc7c67340b8f20ef0ad5d0e049de50dd7344396
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7862766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c37e99de69f18e54515a8d3071b8ea1fd0f2a4900297a8b2c1c386a6a24b78ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb9a0a7b9b4c9f5adc5080dca4ca693f553a370e9fa64affed9aac65b383dc5`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694142e1e3f17625e53d3827671e05224425e877a3e74761c94b54645204ded1`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 121.0 KB (121021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7796589e641878ee661afd57987309f860c136ca6f4413c7d84116bd64ecad12`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 3.7 MB (3652653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29e7393633dafdad3ecd5f2432e9c09c88ae197ae63ebc39cdd5d755efc1093`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7232ef393c6312a3d76029b6d56988d15a40f595f77e0537ee596b7caaca7132`  
		Last Modified: Fri, 06 Dec 2024 01:33:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.33-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:fe3c78175237195a75aca53378025420314ce4b8bd427652e821e9663becf695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.9 KB (107872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095cd6aa8766c7a849d35f1d8a015b4b7aec092919440079533223bcd2268290`

```dockerfile
```

-	Layers:
	-	`sha256:e9f4643bf814c73775db7c54c18dd433640b2a57bca6adaf08f427cfa1bc3de1`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 88.1 KB (88101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee64ac9068d8c28d1fbbd0690d6771ea5be16985b2b5dd0fdc3e6769ec1ee14b`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 19.8 KB (19771 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.33-alpine3.20` - linux; 386

```console
$ docker pull memcached@sha256:492db91f15dbd3e9e9e33a1f7e2cc09b20fae42051a02e3f0de5acd8454a316c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6646126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3ad52f1373f146c439a3c8e68b2d6ed471a4db701c049fd0b5ffea34119f61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bfed8762acb5fad17a943b928db6acd316a3f41770d6ccb3ccde6c5058de8d6`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f39ea1560a9fce397084caa49fd70c40dc655e0857cec268d76a430c74e7b9`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 109.0 KB (108960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a781c1b2a58f8cf6bd9facbe1e1ad73be61573272f8914f2dd4bf85d4ff0baad`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 3.1 MB (3066579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b827afe494b121a7e333c94baa21f20421366c2bb0f1e0eeb73e437c52ff40`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9d6c0f8c12091da40ce7700dcb522ce3106703627f2a754241cdb1bbc845d1`  
		Last Modified: Fri, 06 Dec 2024 01:31:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.33-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:c91fa3449f439c4e9c30c88fa79e5fe63d3bf8af8356defc87da1e56609349ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ee8dfa6edf9c1a3e3b579f7f9fce0a46eb85e82ae82e1e5364b961be5801ca`

```dockerfile
```

-	Layers:
	-	`sha256:a3eb59cf4c9b8cc00383cca89ed90cd3e204f3e898b960d8fb6aea259589e2f3`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 88.0 KB (87952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3242abd4e76a0a4671ab58ff40ccc25a63d6e796bdf01ab8238cd61b52844e92`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 19.5 KB (19516 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.33-alpine3.20` - linux; ppc64le

```console
$ docker pull memcached@sha256:9ed77a1e3df85d41958cfab6678f84b7a0c5478c3ee4031bb4ef7009ae148a8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6838378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7debc910ab631f46ff86577268f8190435a1a1cad3c4f28c2a14839844c89ec6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac7c2caa12b9b7c688356275a58d0faa1e26ca96ea89c8041aca795343d90fb`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0955050f3ec94864d6e58cb0e77be49260e6358a11bcfe4f18fcd7a16ef98bd`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 123.0 KB (123004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1076a55e57cd99a295a1a9b0943a35ef12c0cbefcee0f539ebc0f9d767f09ac7`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 3.1 MB (3141546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd0157cad0ccfad57f8818a6674665d46df00b03abce2b8b0a4b2b55bc097af`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200b295ab1fad685ec6581c5220bd29b35b4de15dd7b79b1670cc8c3a5318ff1`  
		Last Modified: Fri, 06 Dec 2024 01:33:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.33-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:44ef397246da32f636714921281ea510a545706dff7755d39ed522fd34ef818c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.7 KB (105748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27dd5988cf9c77426d5d3ce108181cfde561e89d21a1e57c46b06a24494bc24`

```dockerfile
```

-	Layers:
	-	`sha256:9dd942067c2d5eec8c44d618b60a4fb2d533da4aaa9e59aa658035bae7864153`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 86.1 KB (86101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7ae50a8f9772a347faf3150966eb0a294bad1037dcd82a6b7ca6e7085def4b0`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 19.6 KB (19647 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.33-alpine3.20` - linux; s390x

```console
$ docker pull memcached@sha256:2f9e35d548959a8ea66fbb14b4e45db6201bd399fbce7aa6a91ced6724529015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6590517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e59cf784613df48eaa8bb5d47ccb40bb41263090034725c38a1d343c40fdc98b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd586bc77f5fb181172c996290db7374e9c10d57409c2b44fd564414325e007`  
		Last Modified: Fri, 06 Dec 2024 01:36:13 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0fcd80ecbef8175a68d824552ed0f114429b0267802305d4c7d844c3577627e`  
		Last Modified: Fri, 06 Dec 2024 01:36:13 GMT  
		Size: 112.8 KB (112750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec43a227c373cac7def72eaec9a32204740c8000aa305974e2bdb1684ee66532`  
		Last Modified: Fri, 06 Dec 2024 01:36:13 GMT  
		Size: 3.0 MB (3014795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c4d2f183090b5a127cca23a337b895f3cf87bf67d4f7753457dda9b9e71179`  
		Last Modified: Fri, 06 Dec 2024 01:36:14 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e27bc505bddda3fa278b4085496625d324fb6e550b22e4eed35b931033473d7`  
		Last Modified: Fri, 06 Dec 2024 01:36:14 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.33-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:19d143dfb5e455c347101473ad04cdac2e988e4db9be4af04174526f0d488453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185266b3e1c500c32f3ce16d81debe696e90be32f272cd58900e7e79549f53f4`

```dockerfile
```

-	Layers:
	-	`sha256:cb583c39b213e1d44b5dc21216421e4b8ff1f212376d783788f7ecec530ffbdd`  
		Last Modified: Fri, 06 Dec 2024 01:36:13 GMT  
		Size: 86.0 KB (86043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d788cea57935c2cb3c0e8b4293caec6b1447956196a6739ddf9264bcb76563a9`  
		Last Modified: Fri, 06 Dec 2024 01:36:13 GMT  
		Size: 19.6 KB (19574 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.33-bookworm`

```console
$ docker pull memcached@sha256:b8cb0ed0bf5d3d38f9606fc847c9a21baa68952472ea29a5a685f82a1efc2987
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

### `memcached:1.6.33-bookworm` - linux; amd64

```console
$ docker pull memcached@sha256:1e2854f49ddb3fc0103bf7b8fcd80ed47c6f72e2aa74ad0848acc1274e4f98f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31984433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04abd86d309da60dfe2b7f4f4e20226dd5f87fe17482740074bbc2c6865d6987`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977f47ceef0f8173cff02fe737b3fd37efab540ec727c2a20869e90ab8279920`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1599032aa7639a9095e216c0b122c7eb2cf54392a6e7bf2d191ff3e086bb478a`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 2.5 MB (2491759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:034904c659cc08a9f86d31858f173bfc3a20727cb5fb51319eb9478c29151562`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 1.3 MB (1259579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbc04f1662c41c4314f0f2a27cbf319464d441170360aee7702dd51be327e76`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4e9ce09f9de3f7835981235d8000bd031663f2328a8e4ffb2f6b6e9d1a1e0d`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.33-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:fb6b716e55ea5a7353f965101017052ad92d603abfbd05eb49dc5aeceea69dfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2312843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2806c278d65e027e6b4619f466776331a5efde1eb1992a4a013a5e85ae769111`

```dockerfile
```

-	Layers:
	-	`sha256:a489ae83eb749729e07a801603bdc10563b8508b7272d035a9f58304ea805e5c`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 2.3 MB (2291621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbb57e1ba346b719e10354837a9bef89546f505a248a0977af44ec554c92262a`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.33-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:91ab868f687f5d84ed97501641c6276629ba558cf3b893411d4bff8ddf3b7a20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29090498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddac0a9030226a9353757b40367ccad4e58abf3df5f1cecab9445504a7141a50`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:25d432086d20067bebfff2b163f22d49e7da8528782652615fe170bf8c39194d`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 25.8 MB (25754926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29864ebc65411065e6cc80afcb839ecd53357c5d8accb084195a861ffe331f0c`  
		Last Modified: Tue, 03 Dec 2024 02:34:22 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17b8bb45df912fe349545bf67aeee395da8a6bbd8c9fd4b4bba4ab37d4c46e6`  
		Last Modified: Tue, 03 Dec 2024 02:34:23 GMT  
		Size: 2.1 MB (2096040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f971acf6335510d8cd95bbf08ed1b82d5ccdbb6a46d5cc4004f4d3f17f79ad22`  
		Last Modified: Fri, 06 Dec 2024 01:31:23 GMT  
		Size: 1.2 MB (1238020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d2f4b78825fe502c36e4f1340340617bc5d281e1a4d0bfd9c29b683505190d`  
		Last Modified: Fri, 06 Dec 2024 01:31:23 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0b278088431fe97844cee08594eb17b8a478179969a38c2138afcc8635209b`  
		Last Modified: Fri, 06 Dec 2024 01:31:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.33-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:33b0db124591dec0a6fd5c81068992c08e8cb9a2f4e0f7c8dd8474b34525c0f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2316527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59492fefec6386be99693d0d6d513a6c53fd5cc3e197beb39bcce988752d934b`

```dockerfile
```

-	Layers:
	-	`sha256:3183c33c304bb139731b8181094f3cedf637a75d2c2b46a39117b249bcbf9a94`  
		Last Modified: Fri, 06 Dec 2024 01:31:23 GMT  
		Size: 2.3 MB (2295158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe9afff481d34963c12864f80d0a8758b8462fbfbdf815070d7b572ba117476b`  
		Last Modified: Fri, 06 Dec 2024 01:31:23 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.33-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:4b50248c9ebc50990818eb60f6c506e07a29315de1cf92f8089ce198db55f78f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31670277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae090e1fc19e90d2a650cdd682ddd6cebff3ef4c472411c422c7b772f9c7844a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78a410ea91650a45f4516634a8253fbca2d2238ebd376ee434a91c97add0d41`  
		Last Modified: Tue, 03 Dec 2024 02:56:13 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3651f43c686dcae90b2bb5bfaafb1c1e92231bce87f7c2a4f7f92606b3f6048`  
		Last Modified: Tue, 03 Dec 2024 02:56:14 GMT  
		Size: 2.4 MB (2355349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1974b3b5f9215ed5e7c38499590f73f9d2cc9f0eab4b5bfc835e795f011b6ec`  
		Last Modified: Fri, 06 Dec 2024 01:31:13 GMT  
		Size: 1.3 MB (1254605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0d87f19f5dcc124861cef54d5060fdddf78285679e5e18c5c228a649873178`  
		Last Modified: Fri, 06 Dec 2024 01:31:12 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4e9ce09f9de3f7835981235d8000bd031663f2328a8e4ffb2f6b6e9d1a1e0d`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.33-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:65ec047e972b106c4dccd5e7db2375b427183eaa0a17d24a87733f0781a6f4cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2313354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6be2bd8ba74100235eb2a7790cd07be00c97e00f811e0074913d8ef6bce12587`

```dockerfile
```

-	Layers:
	-	`sha256:aea7e31a5ac097dbe2c1f459e15d324e0b4c270652bc090fc7bb75b32d29171f`  
		Last Modified: Fri, 06 Dec 2024 01:31:13 GMT  
		Size: 2.3 MB (2291935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72554d4560a983cd304f173578e432f68442018a3d2f900c20e8692c7507475d`  
		Last Modified: Fri, 06 Dec 2024 01:31:12 GMT  
		Size: 21.4 KB (21419 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.33-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:2ee1837e5180933d5ce36c27a48671480a1269845d9fe11427b429f7ddcb89e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32967293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa8709f96acad9a15c63279cf937b75d01dd91a1585ac5ca41256e80e432a0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ae6c80ee852fcccae85579165042a3767dcd1190112e87c9f22fa3e76a624c73`  
		Last Modified: Tue, 03 Dec 2024 01:27:10 GMT  
		Size: 29.2 MB (29205487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580dd662e45fd4b251d3406f5a1ea8962e3e4e1d2520efbb737df740b7e957f2`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3f1598f54c5456764cfdadbb7074ec777bd66ed0fab6c8fdfa5e8a435c5ae8`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 2.5 MB (2500687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd3aa7547e95a174e12f01b948f1c39aee54d184931a433b0ea5f3e180259de`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 1.3 MB (1259605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b9d8a09b833489a3bf75e47d6fc9c98a4f688e73ae311ff2277c461dc66a85`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6fe54f00cf7e2bebef13e9698cee799c63127f12560807f4bf87fda6395baf`  
		Last Modified: Fri, 06 Dec 2024 01:31:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.33-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:2029c4c3e23c8bfb7b5f3992ef8057fc969eca5273a1f436d6d8605b3ba6f081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2309883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025c0e1e5fec67ce720fae6f7e5aaaa9c8217653956e512bf60be97cb2294914`

```dockerfile
```

-	Layers:
	-	`sha256:3f7aef5b25a76a78ebdd73ae22cef84f68f0d0a920a1e0a89dab2aa1fa5accdd`  
		Last Modified: Fri, 06 Dec 2024 01:31:11 GMT  
		Size: 2.3 MB (2288719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:551482c681545d405b9f1d3139dcf0fb74b2fecfd0e7d9d54de6e57a981c3d71`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.33-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:b398c51c3b2d91d0274741650d383d12bb8dd65d4acdb202d0a7063d6e4b8b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31705243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4838f50554bb3277090b0aa55a3191c3489fc05113546999725b9c946e1a954e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:29ac4ae2849b0c84c0ef17659082268617abeb406402ef46b6fa9140e6d2064d`  
		Last Modified: Tue, 03 Dec 2024 01:28:15 GMT  
		Size: 28.5 MB (28505909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f398f0ee699c887dba3a51e3212be4320212ed287d33cdd1df41e7fd72240a7`  
		Last Modified: Fri, 06 Dec 2024 01:35:13 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7ddb249939dc734c215bc1be4a564dacdb2495a3ca51100084126ecd662f02`  
		Last Modified: Fri, 06 Dec 2024 01:35:14 GMT  
		Size: 1.9 MB (1943197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d087c96f4f05d81a987f0812e9c7c28cca806e5aa40786761696d7bd547b926a`  
		Last Modified: Fri, 06 Dec 2024 01:35:14 GMT  
		Size: 1.3 MB (1254620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec32257bb4a1a2d1b3c027ae74afbc31c03aec77c3aec28b9f546843aa638ab`  
		Last Modified: Fri, 06 Dec 2024 01:35:13 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4f728769ae3f10d5ef679ac778b45c6992248d4a8e853760525c3c24041f6f`  
		Last Modified: Fri, 06 Dec 2024 01:35:14 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.33-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f528c619723b1b912a572178e808db3bf0968e4baf6ef920992198b60a50bd7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00565dc210c91f04967e0e4b932ca263ef440c9803d1fb47313d6524c29b26f3`

```dockerfile
```

-	Layers:
	-	`sha256:4fe7144715458a1e421c93fd64b7134c4f3738eb832551e549e822b1ba66523d`  
		Last Modified: Fri, 06 Dec 2024 01:35:13 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.33-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:01b87270745db075ed8b996a903bbb03e1ce8e91a1492c6763e8e0184098bf0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36096936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca502cddeb618d1bc49dc5bc8d6538584dd37bf9fdef22011502443d817f36aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e62b6946337cc6b72ec307008f1acc46e12a4f98e6f0e29c92b5538bbafd7ce6`  
		Last Modified: Tue, 03 Dec 2024 01:28:28 GMT  
		Size: 32.1 MB (32063265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8e81ffdbb3a1a0871b7d927a02d62e2ce4eb8b6f7bbc76e4bba93c799b9075`  
		Last Modified: Tue, 03 Dec 2024 02:42:07 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0276e7f6ce6bb384613f81bb9a596143583bdbf5cac2714170243761daa43b7`  
		Last Modified: Tue, 03 Dec 2024 02:42:08 GMT  
		Size: 2.7 MB (2708555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb84fa77333d98470bc633574f7b051132ca9675ff7d781c3cce4a079186907b`  
		Last Modified: Fri, 06 Dec 2024 01:30:50 GMT  
		Size: 1.3 MB (1323604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ecb320c4cc5c4e8e57c37ce8e39a4136d2ef053377f6bc3812880eeab6f20f`  
		Last Modified: Fri, 06 Dec 2024 01:30:50 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b9e76d0bac4875861b1d66e91f0dd7273347b172785e7659835a862b71c9e2`  
		Last Modified: Fri, 06 Dec 2024 01:30:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.33-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:2416ac25dc3bb76b01b44fb54d535ad95f9e7d3f8c5cc714c15e381a4d35d0ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2317287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48fe760f47f1bdadfdc6584c4f1802c30ff05ebb44d44b931211aac3a762993f`

```dockerfile
```

-	Layers:
	-	`sha256:5f182f9c7a52c9256109712b419bb1efe3847e993e342af008724d31754d7b58`  
		Last Modified: Fri, 06 Dec 2024 01:30:50 GMT  
		Size: 2.3 MB (2295992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:373a3417f812a3143655df1a9b4ee6893a0b627316005c587b3c5ddacd6cdd6d`  
		Last Modified: Fri, 06 Dec 2024 01:30:50 GMT  
		Size: 21.3 KB (21295 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.33-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:2a204d42b50b0598b0ce8900e8bde20bcbf35f9c5cd4bbb38186b48cdac2d4d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30274542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:154623d34f127ea2636384bc7205519ccf3b1aad97280ebcdb64b7662a374040`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9378ae44108012049addde60d193467e2b15a247b2f953ad5c27e073c4573d42`  
		Last Modified: Tue, 03 Dec 2024 01:28:18 GMT  
		Size: 26.9 MB (26878971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214d47b5512f1991eb09046f46526e464102115476ac71ca1c8e7bd9439c4a5b`  
		Last Modified: Tue, 03 Dec 2024 02:32:32 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc13e1c57cbb046f722e07c9a375af936eb9f47e47a86a2435b54dc393da6657`  
		Last Modified: Tue, 03 Dec 2024 02:32:32 GMT  
		Size: 2.2 MB (2156364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cecb2200496ee18d3c1d0287a623829849840935d625131d9dded26f2bd67478`  
		Last Modified: Fri, 06 Dec 2024 01:32:17 GMT  
		Size: 1.2 MB (1237695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06048c152c70476e77823ded2b6e26aaa36538ae99b655fed345f19eacdccb3`  
		Last Modified: Fri, 06 Dec 2024 01:32:17 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad2217a2f73e7c40ee3dda6f84683bbf529af0a6c88a2f8509a8c6236fab9b3`  
		Last Modified: Fri, 06 Dec 2024 01:32:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.33-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:9633d4f6d1ceb311422b86502f057cfd400959e6fa3f9fa28d6848bb6cdc9055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2312558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b9c4fe1473e54d45f0c30ca2bdaa8200d0f9e10d811703e74c27232d288313`

```dockerfile
```

-	Layers:
	-	`sha256:470d0c1e3b27df7cc86c281b0b437958b8b4742962b109311219d1d5c8d199e7`  
		Last Modified: Fri, 06 Dec 2024 01:32:17 GMT  
		Size: 2.3 MB (2291336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d21968c91e92936985a4af7a988f292a75a85b6f014bbb668a0e336ff3f0966`  
		Last Modified: Fri, 06 Dec 2024 01:32:17 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine`

```console
$ docker pull memcached@sha256:e8f244572aec9f880cbccace3a05f97f24ff71b53d8d694814748eac12f427c2
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
$ docker pull memcached@sha256:e303bdddcf04ceba4983b9b8cf8b40f8fa41a3ba2d31f7214151d17a2a3076dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6964456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f99a3c16eb499f6cdf0c4680227af234f0e81b86cbb3e219dfd1cc4d331ed8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4191c73fdb45d23dac2c68d4abc8221e6406e9b5591365424302359c1717d44f`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc8b2c6385836cdfcf380e66751377fa23d31f333b616fdd8024545be6c0cc7`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 103.8 KB (103823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77829dd883bfed11037e738040ee96033efef20717be2a3ee174be7d444bd5e3`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 3.2 MB (3235366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfc1d638a936f750e8e87da5702f5b6b5ca51380fca27d33b2f2a75c14f22ba`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b374bd2d4e1ea47b597a16a9e9e56aba35aef6fc394904249a1f2e0f08618e`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c8915813030bfdc12790cdf965af8cfe77b77f8af9f51e92837f89f9eb87c296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05abf48b9dac7138d3a7fe7d19150a99ab63e08e30d39ba567ac00a81d2f1128`

```dockerfile
```

-	Layers:
	-	`sha256:4c8e4bfd8ce93a5fb987902f718ea9389273600f0d3e9d4787a4b63df46b890a`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 88.0 KB (87997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f08348125d8660725339fdc8fac6a613450c75e943e98dc3dde6ba8364bea2cf`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 19.6 KB (19574 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:070c242a1121df9eaa6bb4151dc7c67340b8f20ef0ad5d0e049de50dd7344396
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7862766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c37e99de69f18e54515a8d3071b8ea1fd0f2a4900297a8b2c1c386a6a24b78ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb9a0a7b9b4c9f5adc5080dca4ca693f553a370e9fa64affed9aac65b383dc5`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694142e1e3f17625e53d3827671e05224425e877a3e74761c94b54645204ded1`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 121.0 KB (121021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7796589e641878ee661afd57987309f860c136ca6f4413c7d84116bd64ecad12`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 3.7 MB (3652653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29e7393633dafdad3ecd5f2432e9c09c88ae197ae63ebc39cdd5d755efc1093`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7232ef393c6312a3d76029b6d56988d15a40f595f77e0537ee596b7caaca7132`  
		Last Modified: Fri, 06 Dec 2024 01:33:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:fe3c78175237195a75aca53378025420314ce4b8bd427652e821e9663becf695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.9 KB (107872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095cd6aa8766c7a849d35f1d8a015b4b7aec092919440079533223bcd2268290`

```dockerfile
```

-	Layers:
	-	`sha256:e9f4643bf814c73775db7c54c18dd433640b2a57bca6adaf08f427cfa1bc3de1`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 88.1 KB (88101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee64ac9068d8c28d1fbbd0690d6771ea5be16985b2b5dd0fdc3e6769ec1ee14b`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 19.8 KB (19771 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:492db91f15dbd3e9e9e33a1f7e2cc09b20fae42051a02e3f0de5acd8454a316c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6646126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3ad52f1373f146c439a3c8e68b2d6ed471a4db701c049fd0b5ffea34119f61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bfed8762acb5fad17a943b928db6acd316a3f41770d6ccb3ccde6c5058de8d6`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f39ea1560a9fce397084caa49fd70c40dc655e0857cec268d76a430c74e7b9`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 109.0 KB (108960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a781c1b2a58f8cf6bd9facbe1e1ad73be61573272f8914f2dd4bf85d4ff0baad`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 3.1 MB (3066579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b827afe494b121a7e333c94baa21f20421366c2bb0f1e0eeb73e437c52ff40`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9d6c0f8c12091da40ce7700dcb522ce3106703627f2a754241cdb1bbc845d1`  
		Last Modified: Fri, 06 Dec 2024 01:31:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c91fa3449f439c4e9c30c88fa79e5fe63d3bf8af8356defc87da1e56609349ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ee8dfa6edf9c1a3e3b579f7f9fce0a46eb85e82ae82e1e5364b961be5801ca`

```dockerfile
```

-	Layers:
	-	`sha256:a3eb59cf4c9b8cc00383cca89ed90cd3e204f3e898b960d8fb6aea259589e2f3`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 88.0 KB (87952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3242abd4e76a0a4671ab58ff40ccc25a63d6e796bdf01ab8238cd61b52844e92`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 19.5 KB (19516 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:9ed77a1e3df85d41958cfab6678f84b7a0c5478c3ee4031bb4ef7009ae148a8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6838378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7debc910ab631f46ff86577268f8190435a1a1cad3c4f28c2a14839844c89ec6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac7c2caa12b9b7c688356275a58d0faa1e26ca96ea89c8041aca795343d90fb`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0955050f3ec94864d6e58cb0e77be49260e6358a11bcfe4f18fcd7a16ef98bd`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 123.0 KB (123004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1076a55e57cd99a295a1a9b0943a35ef12c0cbefcee0f539ebc0f9d767f09ac7`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 3.1 MB (3141546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd0157cad0ccfad57f8818a6674665d46df00b03abce2b8b0a4b2b55bc097af`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200b295ab1fad685ec6581c5220bd29b35b4de15dd7b79b1670cc8c3a5318ff1`  
		Last Modified: Fri, 06 Dec 2024 01:33:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:44ef397246da32f636714921281ea510a545706dff7755d39ed522fd34ef818c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.7 KB (105748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27dd5988cf9c77426d5d3ce108181cfde561e89d21a1e57c46b06a24494bc24`

```dockerfile
```

-	Layers:
	-	`sha256:9dd942067c2d5eec8c44d618b60a4fb2d533da4aaa9e59aa658035bae7864153`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 86.1 KB (86101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7ae50a8f9772a347faf3150966eb0a294bad1037dcd82a6b7ca6e7085def4b0`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 19.6 KB (19647 bytes)  
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
$ docker pull memcached@sha256:2f9e35d548959a8ea66fbb14b4e45db6201bd399fbce7aa6a91ced6724529015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6590517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e59cf784613df48eaa8bb5d47ccb40bb41263090034725c38a1d343c40fdc98b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd586bc77f5fb181172c996290db7374e9c10d57409c2b44fd564414325e007`  
		Last Modified: Fri, 06 Dec 2024 01:36:13 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0fcd80ecbef8175a68d824552ed0f114429b0267802305d4c7d844c3577627e`  
		Last Modified: Fri, 06 Dec 2024 01:36:13 GMT  
		Size: 112.8 KB (112750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec43a227c373cac7def72eaec9a32204740c8000aa305974e2bdb1684ee66532`  
		Last Modified: Fri, 06 Dec 2024 01:36:13 GMT  
		Size: 3.0 MB (3014795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c4d2f183090b5a127cca23a337b895f3cf87bf67d4f7753457dda9b9e71179`  
		Last Modified: Fri, 06 Dec 2024 01:36:14 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e27bc505bddda3fa278b4085496625d324fb6e550b22e4eed35b931033473d7`  
		Last Modified: Fri, 06 Dec 2024 01:36:14 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:19d143dfb5e455c347101473ad04cdac2e988e4db9be4af04174526f0d488453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185266b3e1c500c32f3ce16d81debe696e90be32f272cd58900e7e79549f53f4`

```dockerfile
```

-	Layers:
	-	`sha256:cb583c39b213e1d44b5dc21216421e4b8ff1f212376d783788f7ecec530ffbdd`  
		Last Modified: Fri, 06 Dec 2024 01:36:13 GMT  
		Size: 86.0 KB (86043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d788cea57935c2cb3c0e8b4293caec6b1447956196a6739ddf9264bcb76563a9`  
		Last Modified: Fri, 06 Dec 2024 01:36:13 GMT  
		Size: 19.6 KB (19574 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine3.20`

```console
$ docker pull memcached@sha256:e8f244572aec9f880cbccace3a05f97f24ff71b53d8d694814748eac12f427c2
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

### `memcached:alpine3.20` - linux; amd64

```console
$ docker pull memcached@sha256:e303bdddcf04ceba4983b9b8cf8b40f8fa41a3ba2d31f7214151d17a2a3076dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6964456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f99a3c16eb499f6cdf0c4680227af234f0e81b86cbb3e219dfd1cc4d331ed8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4191c73fdb45d23dac2c68d4abc8221e6406e9b5591365424302359c1717d44f`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc8b2c6385836cdfcf380e66751377fa23d31f333b616fdd8024545be6c0cc7`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 103.8 KB (103823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77829dd883bfed11037e738040ee96033efef20717be2a3ee174be7d444bd5e3`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 3.2 MB (3235366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfc1d638a936f750e8e87da5702f5b6b5ca51380fca27d33b2f2a75c14f22ba`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b374bd2d4e1ea47b597a16a9e9e56aba35aef6fc394904249a1f2e0f08618e`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:c8915813030bfdc12790cdf965af8cfe77b77f8af9f51e92837f89f9eb87c296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05abf48b9dac7138d3a7fe7d19150a99ab63e08e30d39ba567ac00a81d2f1128`

```dockerfile
```

-	Layers:
	-	`sha256:4c8e4bfd8ce93a5fb987902f718ea9389273600f0d3e9d4787a4b63df46b890a`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 88.0 KB (87997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f08348125d8660725339fdc8fac6a613450c75e943e98dc3dde6ba8364bea2cf`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 19.6 KB (19574 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:070c242a1121df9eaa6bb4151dc7c67340b8f20ef0ad5d0e049de50dd7344396
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7862766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c37e99de69f18e54515a8d3071b8ea1fd0f2a4900297a8b2c1c386a6a24b78ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb9a0a7b9b4c9f5adc5080dca4ca693f553a370e9fa64affed9aac65b383dc5`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694142e1e3f17625e53d3827671e05224425e877a3e74761c94b54645204ded1`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 121.0 KB (121021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7796589e641878ee661afd57987309f860c136ca6f4413c7d84116bd64ecad12`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 3.7 MB (3652653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29e7393633dafdad3ecd5f2432e9c09c88ae197ae63ebc39cdd5d755efc1093`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7232ef393c6312a3d76029b6d56988d15a40f595f77e0537ee596b7caaca7132`  
		Last Modified: Fri, 06 Dec 2024 01:33:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:fe3c78175237195a75aca53378025420314ce4b8bd427652e821e9663becf695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.9 KB (107872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095cd6aa8766c7a849d35f1d8a015b4b7aec092919440079533223bcd2268290`

```dockerfile
```

-	Layers:
	-	`sha256:e9f4643bf814c73775db7c54c18dd433640b2a57bca6adaf08f427cfa1bc3de1`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 88.1 KB (88101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee64ac9068d8c28d1fbbd0690d6771ea5be16985b2b5dd0fdc3e6769ec1ee14b`  
		Last Modified: Fri, 06 Dec 2024 01:33:57 GMT  
		Size: 19.8 KB (19771 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.20` - linux; 386

```console
$ docker pull memcached@sha256:492db91f15dbd3e9e9e33a1f7e2cc09b20fae42051a02e3f0de5acd8454a316c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6646126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3ad52f1373f146c439a3c8e68b2d6ed471a4db701c049fd0b5ffea34119f61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bfed8762acb5fad17a943b928db6acd316a3f41770d6ccb3ccde6c5058de8d6`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f39ea1560a9fce397084caa49fd70c40dc655e0857cec268d76a430c74e7b9`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 109.0 KB (108960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a781c1b2a58f8cf6bd9facbe1e1ad73be61573272f8914f2dd4bf85d4ff0baad`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 3.1 MB (3066579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b827afe494b121a7e333c94baa21f20421366c2bb0f1e0eeb73e437c52ff40`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9d6c0f8c12091da40ce7700dcb522ce3106703627f2a754241cdb1bbc845d1`  
		Last Modified: Fri, 06 Dec 2024 01:31:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:c91fa3449f439c4e9c30c88fa79e5fe63d3bf8af8356defc87da1e56609349ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ee8dfa6edf9c1a3e3b579f7f9fce0a46eb85e82ae82e1e5364b961be5801ca`

```dockerfile
```

-	Layers:
	-	`sha256:a3eb59cf4c9b8cc00383cca89ed90cd3e204f3e898b960d8fb6aea259589e2f3`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 88.0 KB (87952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3242abd4e76a0a4671ab58ff40ccc25a63d6e796bdf01ab8238cd61b52844e92`  
		Last Modified: Fri, 06 Dec 2024 01:31:18 GMT  
		Size: 19.5 KB (19516 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.20` - linux; ppc64le

```console
$ docker pull memcached@sha256:9ed77a1e3df85d41958cfab6678f84b7a0c5478c3ee4031bb4ef7009ae148a8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6838378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7debc910ab631f46ff86577268f8190435a1a1cad3c4f28c2a14839844c89ec6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac7c2caa12b9b7c688356275a58d0faa1e26ca96ea89c8041aca795343d90fb`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0955050f3ec94864d6e58cb0e77be49260e6358a11bcfe4f18fcd7a16ef98bd`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 123.0 KB (123004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1076a55e57cd99a295a1a9b0943a35ef12c0cbefcee0f539ebc0f9d767f09ac7`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 3.1 MB (3141546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd0157cad0ccfad57f8818a6674665d46df00b03abce2b8b0a4b2b55bc097af`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200b295ab1fad685ec6581c5220bd29b35b4de15dd7b79b1670cc8c3a5318ff1`  
		Last Modified: Fri, 06 Dec 2024 01:33:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:44ef397246da32f636714921281ea510a545706dff7755d39ed522fd34ef818c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.7 KB (105748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27dd5988cf9c77426d5d3ce108181cfde561e89d21a1e57c46b06a24494bc24`

```dockerfile
```

-	Layers:
	-	`sha256:9dd942067c2d5eec8c44d618b60a4fb2d533da4aaa9e59aa658035bae7864153`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 86.1 KB (86101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7ae50a8f9772a347faf3150966eb0a294bad1037dcd82a6b7ca6e7085def4b0`  
		Last Modified: Fri, 06 Dec 2024 01:33:37 GMT  
		Size: 19.6 KB (19647 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.20` - linux; riscv64

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

### `memcached:alpine3.20` - unknown; unknown

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

### `memcached:alpine3.20` - linux; s390x

```console
$ docker pull memcached@sha256:2f9e35d548959a8ea66fbb14b4e45db6201bd399fbce7aa6a91ced6724529015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6590517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e59cf784613df48eaa8bb5d47ccb40bb41263090034725c38a1d343c40fdc98b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd586bc77f5fb181172c996290db7374e9c10d57409c2b44fd564414325e007`  
		Last Modified: Fri, 06 Dec 2024 01:36:13 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0fcd80ecbef8175a68d824552ed0f114429b0267802305d4c7d844c3577627e`  
		Last Modified: Fri, 06 Dec 2024 01:36:13 GMT  
		Size: 112.8 KB (112750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec43a227c373cac7def72eaec9a32204740c8000aa305974e2bdb1684ee66532`  
		Last Modified: Fri, 06 Dec 2024 01:36:13 GMT  
		Size: 3.0 MB (3014795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c4d2f183090b5a127cca23a337b895f3cf87bf67d4f7753457dda9b9e71179`  
		Last Modified: Fri, 06 Dec 2024 01:36:14 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e27bc505bddda3fa278b4085496625d324fb6e550b22e4eed35b931033473d7`  
		Last Modified: Fri, 06 Dec 2024 01:36:14 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:19d143dfb5e455c347101473ad04cdac2e988e4db9be4af04174526f0d488453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185266b3e1c500c32f3ce16d81debe696e90be32f272cd58900e7e79549f53f4`

```dockerfile
```

-	Layers:
	-	`sha256:cb583c39b213e1d44b5dc21216421e4b8ff1f212376d783788f7ecec530ffbdd`  
		Last Modified: Fri, 06 Dec 2024 01:36:13 GMT  
		Size: 86.0 KB (86043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d788cea57935c2cb3c0e8b4293caec6b1447956196a6739ddf9264bcb76563a9`  
		Last Modified: Fri, 06 Dec 2024 01:36:13 GMT  
		Size: 19.6 KB (19574 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:bookworm`

```console
$ docker pull memcached@sha256:b8cb0ed0bf5d3d38f9606fc847c9a21baa68952472ea29a5a685f82a1efc2987
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
$ docker pull memcached@sha256:1e2854f49ddb3fc0103bf7b8fcd80ed47c6f72e2aa74ad0848acc1274e4f98f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31984433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04abd86d309da60dfe2b7f4f4e20226dd5f87fe17482740074bbc2c6865d6987`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977f47ceef0f8173cff02fe737b3fd37efab540ec727c2a20869e90ab8279920`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1599032aa7639a9095e216c0b122c7eb2cf54392a6e7bf2d191ff3e086bb478a`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 2.5 MB (2491759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:034904c659cc08a9f86d31858f173bfc3a20727cb5fb51319eb9478c29151562`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 1.3 MB (1259579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbc04f1662c41c4314f0f2a27cbf319464d441170360aee7702dd51be327e76`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4e9ce09f9de3f7835981235d8000bd031663f2328a8e4ffb2f6b6e9d1a1e0d`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:fb6b716e55ea5a7353f965101017052ad92d603abfbd05eb49dc5aeceea69dfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2312843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2806c278d65e027e6b4619f466776331a5efde1eb1992a4a013a5e85ae769111`

```dockerfile
```

-	Layers:
	-	`sha256:a489ae83eb749729e07a801603bdc10563b8508b7272d035a9f58304ea805e5c`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 2.3 MB (2291621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbb57e1ba346b719e10354837a9bef89546f505a248a0977af44ec554c92262a`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:91ab868f687f5d84ed97501641c6276629ba558cf3b893411d4bff8ddf3b7a20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29090498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddac0a9030226a9353757b40367ccad4e58abf3df5f1cecab9445504a7141a50`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:25d432086d20067bebfff2b163f22d49e7da8528782652615fe170bf8c39194d`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 25.8 MB (25754926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29864ebc65411065e6cc80afcb839ecd53357c5d8accb084195a861ffe331f0c`  
		Last Modified: Tue, 03 Dec 2024 02:34:22 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17b8bb45df912fe349545bf67aeee395da8a6bbd8c9fd4b4bba4ab37d4c46e6`  
		Last Modified: Tue, 03 Dec 2024 02:34:23 GMT  
		Size: 2.1 MB (2096040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f971acf6335510d8cd95bbf08ed1b82d5ccdbb6a46d5cc4004f4d3f17f79ad22`  
		Last Modified: Fri, 06 Dec 2024 01:31:23 GMT  
		Size: 1.2 MB (1238020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d2f4b78825fe502c36e4f1340340617bc5d281e1a4d0bfd9c29b683505190d`  
		Last Modified: Fri, 06 Dec 2024 01:31:23 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0b278088431fe97844cee08594eb17b8a478179969a38c2138afcc8635209b`  
		Last Modified: Fri, 06 Dec 2024 01:31:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:33b0db124591dec0a6fd5c81068992c08e8cb9a2f4e0f7c8dd8474b34525c0f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2316527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59492fefec6386be99693d0d6d513a6c53fd5cc3e197beb39bcce988752d934b`

```dockerfile
```

-	Layers:
	-	`sha256:3183c33c304bb139731b8181094f3cedf637a75d2c2b46a39117b249bcbf9a94`  
		Last Modified: Fri, 06 Dec 2024 01:31:23 GMT  
		Size: 2.3 MB (2295158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe9afff481d34963c12864f80d0a8758b8462fbfbdf815070d7b572ba117476b`  
		Last Modified: Fri, 06 Dec 2024 01:31:23 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:4b50248c9ebc50990818eb60f6c506e07a29315de1cf92f8089ce198db55f78f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31670277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae090e1fc19e90d2a650cdd682ddd6cebff3ef4c472411c422c7b772f9c7844a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78a410ea91650a45f4516634a8253fbca2d2238ebd376ee434a91c97add0d41`  
		Last Modified: Tue, 03 Dec 2024 02:56:13 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3651f43c686dcae90b2bb5bfaafb1c1e92231bce87f7c2a4f7f92606b3f6048`  
		Last Modified: Tue, 03 Dec 2024 02:56:14 GMT  
		Size: 2.4 MB (2355349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1974b3b5f9215ed5e7c38499590f73f9d2cc9f0eab4b5bfc835e795f011b6ec`  
		Last Modified: Fri, 06 Dec 2024 01:31:13 GMT  
		Size: 1.3 MB (1254605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0d87f19f5dcc124861cef54d5060fdddf78285679e5e18c5c228a649873178`  
		Last Modified: Fri, 06 Dec 2024 01:31:12 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4e9ce09f9de3f7835981235d8000bd031663f2328a8e4ffb2f6b6e9d1a1e0d`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:65ec047e972b106c4dccd5e7db2375b427183eaa0a17d24a87733f0781a6f4cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2313354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6be2bd8ba74100235eb2a7790cd07be00c97e00f811e0074913d8ef6bce12587`

```dockerfile
```

-	Layers:
	-	`sha256:aea7e31a5ac097dbe2c1f459e15d324e0b4c270652bc090fc7bb75b32d29171f`  
		Last Modified: Fri, 06 Dec 2024 01:31:13 GMT  
		Size: 2.3 MB (2291935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72554d4560a983cd304f173578e432f68442018a3d2f900c20e8692c7507475d`  
		Last Modified: Fri, 06 Dec 2024 01:31:12 GMT  
		Size: 21.4 KB (21419 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; 386

```console
$ docker pull memcached@sha256:2ee1837e5180933d5ce36c27a48671480a1269845d9fe11427b429f7ddcb89e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32967293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa8709f96acad9a15c63279cf937b75d01dd91a1585ac5ca41256e80e432a0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ae6c80ee852fcccae85579165042a3767dcd1190112e87c9f22fa3e76a624c73`  
		Last Modified: Tue, 03 Dec 2024 01:27:10 GMT  
		Size: 29.2 MB (29205487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580dd662e45fd4b251d3406f5a1ea8962e3e4e1d2520efbb737df740b7e957f2`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3f1598f54c5456764cfdadbb7074ec777bd66ed0fab6c8fdfa5e8a435c5ae8`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 2.5 MB (2500687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd3aa7547e95a174e12f01b948f1c39aee54d184931a433b0ea5f3e180259de`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 1.3 MB (1259605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b9d8a09b833489a3bf75e47d6fc9c98a4f688e73ae311ff2277c461dc66a85`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6fe54f00cf7e2bebef13e9698cee799c63127f12560807f4bf87fda6395baf`  
		Last Modified: Fri, 06 Dec 2024 01:31:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:2029c4c3e23c8bfb7b5f3992ef8057fc969eca5273a1f436d6d8605b3ba6f081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2309883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025c0e1e5fec67ce720fae6f7e5aaaa9c8217653956e512bf60be97cb2294914`

```dockerfile
```

-	Layers:
	-	`sha256:3f7aef5b25a76a78ebdd73ae22cef84f68f0d0a920a1e0a89dab2aa1fa5accdd`  
		Last Modified: Fri, 06 Dec 2024 01:31:11 GMT  
		Size: 2.3 MB (2288719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:551482c681545d405b9f1d3139dcf0fb74b2fecfd0e7d9d54de6e57a981c3d71`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:b398c51c3b2d91d0274741650d383d12bb8dd65d4acdb202d0a7063d6e4b8b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31705243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4838f50554bb3277090b0aa55a3191c3489fc05113546999725b9c946e1a954e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:29ac4ae2849b0c84c0ef17659082268617abeb406402ef46b6fa9140e6d2064d`  
		Last Modified: Tue, 03 Dec 2024 01:28:15 GMT  
		Size: 28.5 MB (28505909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f398f0ee699c887dba3a51e3212be4320212ed287d33cdd1df41e7fd72240a7`  
		Last Modified: Fri, 06 Dec 2024 01:35:13 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7ddb249939dc734c215bc1be4a564dacdb2495a3ca51100084126ecd662f02`  
		Last Modified: Fri, 06 Dec 2024 01:35:14 GMT  
		Size: 1.9 MB (1943197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d087c96f4f05d81a987f0812e9c7c28cca806e5aa40786761696d7bd547b926a`  
		Last Modified: Fri, 06 Dec 2024 01:35:14 GMT  
		Size: 1.3 MB (1254620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec32257bb4a1a2d1b3c027ae74afbc31c03aec77c3aec28b9f546843aa638ab`  
		Last Modified: Fri, 06 Dec 2024 01:35:13 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4f728769ae3f10d5ef679ac778b45c6992248d4a8e853760525c3c24041f6f`  
		Last Modified: Fri, 06 Dec 2024 01:35:14 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f528c619723b1b912a572178e808db3bf0968e4baf6ef920992198b60a50bd7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00565dc210c91f04967e0e4b932ca263ef440c9803d1fb47313d6524c29b26f3`

```dockerfile
```

-	Layers:
	-	`sha256:4fe7144715458a1e421c93fd64b7134c4f3738eb832551e549e822b1ba66523d`  
		Last Modified: Fri, 06 Dec 2024 01:35:13 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:01b87270745db075ed8b996a903bbb03e1ce8e91a1492c6763e8e0184098bf0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36096936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca502cddeb618d1bc49dc5bc8d6538584dd37bf9fdef22011502443d817f36aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e62b6946337cc6b72ec307008f1acc46e12a4f98e6f0e29c92b5538bbafd7ce6`  
		Last Modified: Tue, 03 Dec 2024 01:28:28 GMT  
		Size: 32.1 MB (32063265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8e81ffdbb3a1a0871b7d927a02d62e2ce4eb8b6f7bbc76e4bba93c799b9075`  
		Last Modified: Tue, 03 Dec 2024 02:42:07 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0276e7f6ce6bb384613f81bb9a596143583bdbf5cac2714170243761daa43b7`  
		Last Modified: Tue, 03 Dec 2024 02:42:08 GMT  
		Size: 2.7 MB (2708555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb84fa77333d98470bc633574f7b051132ca9675ff7d781c3cce4a079186907b`  
		Last Modified: Fri, 06 Dec 2024 01:30:50 GMT  
		Size: 1.3 MB (1323604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ecb320c4cc5c4e8e57c37ce8e39a4136d2ef053377f6bc3812880eeab6f20f`  
		Last Modified: Fri, 06 Dec 2024 01:30:50 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b9e76d0bac4875861b1d66e91f0dd7273347b172785e7659835a862b71c9e2`  
		Last Modified: Fri, 06 Dec 2024 01:30:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:2416ac25dc3bb76b01b44fb54d535ad95f9e7d3f8c5cc714c15e381a4d35d0ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2317287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48fe760f47f1bdadfdc6584c4f1802c30ff05ebb44d44b931211aac3a762993f`

```dockerfile
```

-	Layers:
	-	`sha256:5f182f9c7a52c9256109712b419bb1efe3847e993e342af008724d31754d7b58`  
		Last Modified: Fri, 06 Dec 2024 01:30:50 GMT  
		Size: 2.3 MB (2295992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:373a3417f812a3143655df1a9b4ee6893a0b627316005c587b3c5ddacd6cdd6d`  
		Last Modified: Fri, 06 Dec 2024 01:30:50 GMT  
		Size: 21.3 KB (21295 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:2a204d42b50b0598b0ce8900e8bde20bcbf35f9c5cd4bbb38186b48cdac2d4d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30274542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:154623d34f127ea2636384bc7205519ccf3b1aad97280ebcdb64b7662a374040`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9378ae44108012049addde60d193467e2b15a247b2f953ad5c27e073c4573d42`  
		Last Modified: Tue, 03 Dec 2024 01:28:18 GMT  
		Size: 26.9 MB (26878971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214d47b5512f1991eb09046f46526e464102115476ac71ca1c8e7bd9439c4a5b`  
		Last Modified: Tue, 03 Dec 2024 02:32:32 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc13e1c57cbb046f722e07c9a375af936eb9f47e47a86a2435b54dc393da6657`  
		Last Modified: Tue, 03 Dec 2024 02:32:32 GMT  
		Size: 2.2 MB (2156364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cecb2200496ee18d3c1d0287a623829849840935d625131d9dded26f2bd67478`  
		Last Modified: Fri, 06 Dec 2024 01:32:17 GMT  
		Size: 1.2 MB (1237695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06048c152c70476e77823ded2b6e26aaa36538ae99b655fed345f19eacdccb3`  
		Last Modified: Fri, 06 Dec 2024 01:32:17 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad2217a2f73e7c40ee3dda6f84683bbf529af0a6c88a2f8509a8c6236fab9b3`  
		Last Modified: Fri, 06 Dec 2024 01:32:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:9633d4f6d1ceb311422b86502f057cfd400959e6fa3f9fa28d6848bb6cdc9055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2312558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b9c4fe1473e54d45f0c30ca2bdaa8200d0f9e10d811703e74c27232d288313`

```dockerfile
```

-	Layers:
	-	`sha256:470d0c1e3b27df7cc86c281b0b437958b8b4742962b109311219d1d5c8d199e7`  
		Last Modified: Fri, 06 Dec 2024 01:32:17 GMT  
		Size: 2.3 MB (2291336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d21968c91e92936985a4af7a988f292a75a85b6f014bbb668a0e336ff3f0966`  
		Last Modified: Fri, 06 Dec 2024 01:32:17 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:latest`

```console
$ docker pull memcached@sha256:b8cb0ed0bf5d3d38f9606fc847c9a21baa68952472ea29a5a685f82a1efc2987
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
$ docker pull memcached@sha256:1e2854f49ddb3fc0103bf7b8fcd80ed47c6f72e2aa74ad0848acc1274e4f98f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31984433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04abd86d309da60dfe2b7f4f4e20226dd5f87fe17482740074bbc2c6865d6987`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977f47ceef0f8173cff02fe737b3fd37efab540ec727c2a20869e90ab8279920`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1599032aa7639a9095e216c0b122c7eb2cf54392a6e7bf2d191ff3e086bb478a`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 2.5 MB (2491759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:034904c659cc08a9f86d31858f173bfc3a20727cb5fb51319eb9478c29151562`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 1.3 MB (1259579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbc04f1662c41c4314f0f2a27cbf319464d441170360aee7702dd51be327e76`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4e9ce09f9de3f7835981235d8000bd031663f2328a8e4ffb2f6b6e9d1a1e0d`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:fb6b716e55ea5a7353f965101017052ad92d603abfbd05eb49dc5aeceea69dfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2312843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2806c278d65e027e6b4619f466776331a5efde1eb1992a4a013a5e85ae769111`

```dockerfile
```

-	Layers:
	-	`sha256:a489ae83eb749729e07a801603bdc10563b8508b7272d035a9f58304ea805e5c`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 2.3 MB (2291621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbb57e1ba346b719e10354837a9bef89546f505a248a0977af44ec554c92262a`  
		Last Modified: Fri, 06 Dec 2024 01:31:08 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:91ab868f687f5d84ed97501641c6276629ba558cf3b893411d4bff8ddf3b7a20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29090498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddac0a9030226a9353757b40367ccad4e58abf3df5f1cecab9445504a7141a50`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:25d432086d20067bebfff2b163f22d49e7da8528782652615fe170bf8c39194d`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 25.8 MB (25754926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29864ebc65411065e6cc80afcb839ecd53357c5d8accb084195a861ffe331f0c`  
		Last Modified: Tue, 03 Dec 2024 02:34:22 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17b8bb45df912fe349545bf67aeee395da8a6bbd8c9fd4b4bba4ab37d4c46e6`  
		Last Modified: Tue, 03 Dec 2024 02:34:23 GMT  
		Size: 2.1 MB (2096040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f971acf6335510d8cd95bbf08ed1b82d5ccdbb6a46d5cc4004f4d3f17f79ad22`  
		Last Modified: Fri, 06 Dec 2024 01:31:23 GMT  
		Size: 1.2 MB (1238020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d2f4b78825fe502c36e4f1340340617bc5d281e1a4d0bfd9c29b683505190d`  
		Last Modified: Fri, 06 Dec 2024 01:31:23 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0b278088431fe97844cee08594eb17b8a478179969a38c2138afcc8635209b`  
		Last Modified: Fri, 06 Dec 2024 01:31:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:33b0db124591dec0a6fd5c81068992c08e8cb9a2f4e0f7c8dd8474b34525c0f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2316527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59492fefec6386be99693d0d6d513a6c53fd5cc3e197beb39bcce988752d934b`

```dockerfile
```

-	Layers:
	-	`sha256:3183c33c304bb139731b8181094f3cedf637a75d2c2b46a39117b249bcbf9a94`  
		Last Modified: Fri, 06 Dec 2024 01:31:23 GMT  
		Size: 2.3 MB (2295158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe9afff481d34963c12864f80d0a8758b8462fbfbdf815070d7b572ba117476b`  
		Last Modified: Fri, 06 Dec 2024 01:31:23 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:4b50248c9ebc50990818eb60f6c506e07a29315de1cf92f8089ce198db55f78f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31670277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae090e1fc19e90d2a650cdd682ddd6cebff3ef4c472411c422c7b772f9c7844a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78a410ea91650a45f4516634a8253fbca2d2238ebd376ee434a91c97add0d41`  
		Last Modified: Tue, 03 Dec 2024 02:56:13 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3651f43c686dcae90b2bb5bfaafb1c1e92231bce87f7c2a4f7f92606b3f6048`  
		Last Modified: Tue, 03 Dec 2024 02:56:14 GMT  
		Size: 2.4 MB (2355349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1974b3b5f9215ed5e7c38499590f73f9d2cc9f0eab4b5bfc835e795f011b6ec`  
		Last Modified: Fri, 06 Dec 2024 01:31:13 GMT  
		Size: 1.3 MB (1254605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0d87f19f5dcc124861cef54d5060fdddf78285679e5e18c5c228a649873178`  
		Last Modified: Fri, 06 Dec 2024 01:31:12 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4e9ce09f9de3f7835981235d8000bd031663f2328a8e4ffb2f6b6e9d1a1e0d`  
		Last Modified: Fri, 06 Dec 2024 01:31:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:65ec047e972b106c4dccd5e7db2375b427183eaa0a17d24a87733f0781a6f4cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2313354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6be2bd8ba74100235eb2a7790cd07be00c97e00f811e0074913d8ef6bce12587`

```dockerfile
```

-	Layers:
	-	`sha256:aea7e31a5ac097dbe2c1f459e15d324e0b4c270652bc090fc7bb75b32d29171f`  
		Last Modified: Fri, 06 Dec 2024 01:31:13 GMT  
		Size: 2.3 MB (2291935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72554d4560a983cd304f173578e432f68442018a3d2f900c20e8692c7507475d`  
		Last Modified: Fri, 06 Dec 2024 01:31:12 GMT  
		Size: 21.4 KB (21419 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:2ee1837e5180933d5ce36c27a48671480a1269845d9fe11427b429f7ddcb89e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32967293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa8709f96acad9a15c63279cf937b75d01dd91a1585ac5ca41256e80e432a0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ae6c80ee852fcccae85579165042a3767dcd1190112e87c9f22fa3e76a624c73`  
		Last Modified: Tue, 03 Dec 2024 01:27:10 GMT  
		Size: 29.2 MB (29205487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580dd662e45fd4b251d3406f5a1ea8962e3e4e1d2520efbb737df740b7e957f2`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3f1598f54c5456764cfdadbb7074ec777bd66ed0fab6c8fdfa5e8a435c5ae8`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 2.5 MB (2500687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd3aa7547e95a174e12f01b948f1c39aee54d184931a433b0ea5f3e180259de`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 1.3 MB (1259605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b9d8a09b833489a3bf75e47d6fc9c98a4f688e73ae311ff2277c461dc66a85`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6fe54f00cf7e2bebef13e9698cee799c63127f12560807f4bf87fda6395baf`  
		Last Modified: Fri, 06 Dec 2024 01:31:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:2029c4c3e23c8bfb7b5f3992ef8057fc969eca5273a1f436d6d8605b3ba6f081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2309883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025c0e1e5fec67ce720fae6f7e5aaaa9c8217653956e512bf60be97cb2294914`

```dockerfile
```

-	Layers:
	-	`sha256:3f7aef5b25a76a78ebdd73ae22cef84f68f0d0a920a1e0a89dab2aa1fa5accdd`  
		Last Modified: Fri, 06 Dec 2024 01:31:11 GMT  
		Size: 2.3 MB (2288719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:551482c681545d405b9f1d3139dcf0fb74b2fecfd0e7d9d54de6e57a981c3d71`  
		Last Modified: Fri, 06 Dec 2024 01:31:10 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; mips64le

```console
$ docker pull memcached@sha256:b398c51c3b2d91d0274741650d383d12bb8dd65d4acdb202d0a7063d6e4b8b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31705243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4838f50554bb3277090b0aa55a3191c3489fc05113546999725b9c946e1a954e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:29ac4ae2849b0c84c0ef17659082268617abeb406402ef46b6fa9140e6d2064d`  
		Last Modified: Tue, 03 Dec 2024 01:28:15 GMT  
		Size: 28.5 MB (28505909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f398f0ee699c887dba3a51e3212be4320212ed287d33cdd1df41e7fd72240a7`  
		Last Modified: Fri, 06 Dec 2024 01:35:13 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7ddb249939dc734c215bc1be4a564dacdb2495a3ca51100084126ecd662f02`  
		Last Modified: Fri, 06 Dec 2024 01:35:14 GMT  
		Size: 1.9 MB (1943197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d087c96f4f05d81a987f0812e9c7c28cca806e5aa40786761696d7bd547b926a`  
		Last Modified: Fri, 06 Dec 2024 01:35:14 GMT  
		Size: 1.3 MB (1254620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec32257bb4a1a2d1b3c027ae74afbc31c03aec77c3aec28b9f546843aa638ab`  
		Last Modified: Fri, 06 Dec 2024 01:35:13 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4f728769ae3f10d5ef679ac778b45c6992248d4a8e853760525c3c24041f6f`  
		Last Modified: Fri, 06 Dec 2024 01:35:14 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:f528c619723b1b912a572178e808db3bf0968e4baf6ef920992198b60a50bd7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00565dc210c91f04967e0e4b932ca263ef440c9803d1fb47313d6524c29b26f3`

```dockerfile
```

-	Layers:
	-	`sha256:4fe7144715458a1e421c93fd64b7134c4f3738eb832551e549e822b1ba66523d`  
		Last Modified: Fri, 06 Dec 2024 01:35:13 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:01b87270745db075ed8b996a903bbb03e1ce8e91a1492c6763e8e0184098bf0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36096936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca502cddeb618d1bc49dc5bc8d6538584dd37bf9fdef22011502443d817f36aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e62b6946337cc6b72ec307008f1acc46e12a4f98e6f0e29c92b5538bbafd7ce6`  
		Last Modified: Tue, 03 Dec 2024 01:28:28 GMT  
		Size: 32.1 MB (32063265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8e81ffdbb3a1a0871b7d927a02d62e2ce4eb8b6f7bbc76e4bba93c799b9075`  
		Last Modified: Tue, 03 Dec 2024 02:42:07 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0276e7f6ce6bb384613f81bb9a596143583bdbf5cac2714170243761daa43b7`  
		Last Modified: Tue, 03 Dec 2024 02:42:08 GMT  
		Size: 2.7 MB (2708555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb84fa77333d98470bc633574f7b051132ca9675ff7d781c3cce4a079186907b`  
		Last Modified: Fri, 06 Dec 2024 01:30:50 GMT  
		Size: 1.3 MB (1323604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ecb320c4cc5c4e8e57c37ce8e39a4136d2ef053377f6bc3812880eeab6f20f`  
		Last Modified: Fri, 06 Dec 2024 01:30:50 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b9e76d0bac4875861b1d66e91f0dd7273347b172785e7659835a862b71c9e2`  
		Last Modified: Fri, 06 Dec 2024 01:30:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:2416ac25dc3bb76b01b44fb54d535ad95f9e7d3f8c5cc714c15e381a4d35d0ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2317287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48fe760f47f1bdadfdc6584c4f1802c30ff05ebb44d44b931211aac3a762993f`

```dockerfile
```

-	Layers:
	-	`sha256:5f182f9c7a52c9256109712b419bb1efe3847e993e342af008724d31754d7b58`  
		Last Modified: Fri, 06 Dec 2024 01:30:50 GMT  
		Size: 2.3 MB (2295992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:373a3417f812a3143655df1a9b4ee6893a0b627316005c587b3c5ddacd6cdd6d`  
		Last Modified: Fri, 06 Dec 2024 01:30:50 GMT  
		Size: 21.3 KB (21295 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:2a204d42b50b0598b0ce8900e8bde20bcbf35f9c5cd4bbb38186b48cdac2d4d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30274542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:154623d34f127ea2636384bc7205519ccf3b1aad97280ebcdb64b7662a374040`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1733097600'
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_VERSION=1.6.33
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.33.tar.gz
# Thu, 05 Dec 2024 07:54:10 GMT
ENV MEMCACHED_SHA1=e884ea1778494a3c57a78fab845ab468679329a1
# Thu, 05 Dec 2024 07:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Dec 2024 07:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 07:54:10 GMT
USER memcache
# Thu, 05 Dec 2024 07:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 05 Dec 2024 07:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9378ae44108012049addde60d193467e2b15a247b2f953ad5c27e073c4573d42`  
		Last Modified: Tue, 03 Dec 2024 01:28:18 GMT  
		Size: 26.9 MB (26878971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214d47b5512f1991eb09046f46526e464102115476ac71ca1c8e7bd9439c4a5b`  
		Last Modified: Tue, 03 Dec 2024 02:32:32 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc13e1c57cbb046f722e07c9a375af936eb9f47e47a86a2435b54dc393da6657`  
		Last Modified: Tue, 03 Dec 2024 02:32:32 GMT  
		Size: 2.2 MB (2156364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cecb2200496ee18d3c1d0287a623829849840935d625131d9dded26f2bd67478`  
		Last Modified: Fri, 06 Dec 2024 01:32:17 GMT  
		Size: 1.2 MB (1237695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06048c152c70476e77823ded2b6e26aaa36538ae99b655fed345f19eacdccb3`  
		Last Modified: Fri, 06 Dec 2024 01:32:17 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad2217a2f73e7c40ee3dda6f84683bbf529af0a6c88a2f8509a8c6236fab9b3`  
		Last Modified: Fri, 06 Dec 2024 01:32:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:9633d4f6d1ceb311422b86502f057cfd400959e6fa3f9fa28d6848bb6cdc9055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2312558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b9c4fe1473e54d45f0c30ca2bdaa8200d0f9e10d811703e74c27232d288313`

```dockerfile
```

-	Layers:
	-	`sha256:470d0c1e3b27df7cc86c281b0b437958b8b4742962b109311219d1d5c8d199e7`  
		Last Modified: Fri, 06 Dec 2024 01:32:17 GMT  
		Size: 2.3 MB (2291336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d21968c91e92936985a4af7a988f292a75a85b6f014bbb668a0e336ff3f0966`  
		Last Modified: Fri, 06 Dec 2024 01:32:17 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json
