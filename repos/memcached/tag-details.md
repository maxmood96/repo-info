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
-	[`memcached:1.6.26`](#memcached1626)
-	[`memcached:1.6.26-alpine`](#memcached1626-alpine)
-	[`memcached:1.6.26-alpine3.19`](#memcached1626-alpine319)
-	[`memcached:1.6.26-bookworm`](#memcached1626-bookworm)
-	[`memcached:alpine`](#memcachedalpine)
-	[`memcached:alpine3.19`](#memcachedalpine319)
-	[`memcached:bookworm`](#memcachedbookworm)
-	[`memcached:latest`](#memcachedlatest)

## `memcached:1`

```console
$ docker pull memcached@sha256:9eb572b94abad82c04f1329c97e72684931b1dda2cb5c0ee6c4d115f76d6b037
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
$ docker pull memcached@sha256:2967dc980ac80883003061c899102ed6c8749ed50712d4cf592b7c53efd7a498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32872677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7787f9f0d27b97ee6da8b7b2fdf9dec18a1c0fa6c05b0d4a454cc84138bfceb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131f56ef3fe0a1487206d17cc66325f94d97854c231561697099f0162c37a033`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa35112bf68c5c494491a4c7fbbb8ba5e4d9d410ce9150f1b3238414cbc091b0`  
		Last Modified: Wed, 10 Apr 2024 02:57:19 GMT  
		Size: 2.5 MB (2488500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a672c032d4a7b7c0de949d9fe1d4896cc7da42256b16e1daba353de964968b8`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 1.3 MB (1251305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01135bb689569cd15c6a2b8d8e115947652e4d61a01127729ea24513d1f57d2`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48f53906ef45e3138f6a1f1ee8ebd01ca24a3c3a2c15301afe932077984afbb`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:ace7b79050b8d00e7046345e319209248f2ce44b7b3a67968e6662d559b4cebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0612146bf8ed0f19690c2070f49b81b2f59f0df0c0aee6b38606b04c32b3b1bc`

```dockerfile
```

-	Layers:
	-	`sha256:cbbd757e27c72cb57f0f51a89cb3d65360e0afa594c47eff406c9db9d3a27de0`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 2.3 MB (2261161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d398ef36731f34f7e28948dd252f5bd1ec36dbc3a4f7b23dd7fc9d195992db2`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 21.1 KB (21142 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v5

```console
$ docker pull memcached@sha256:794b039b86010e20defef81d8fe493212a10d4c4f774d39e7c09aaaf8a9e3ebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30212760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:916c48be9c03801f4162ac2f2e46c0e5d0c8ffa27e110dff6f876cfe88d992ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:bfe2e0ed45dd2920845bd9283b7d13266c82fe9f48ba261b6529c28dc246d3e4 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:60d288182f6883c1ed662f82d32316348aac8ca45c943f1093aed5c0ed01b45c`  
		Last Modified: Wed, 10 Apr 2024 00:54:34 GMT  
		Size: 26.9 MB (26890564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2034ec998bbde42652af813854ab5c0f1dd9c547b6b0c4680f48b2f545ede0ef`  
		Last Modified: Wed, 10 Apr 2024 16:31:49 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d77e350a8c89faec28416a879441cd67ed9d418f318b1426c3961607be04f57`  
		Last Modified: Wed, 10 Apr 2024 16:31:50 GMT  
		Size: 2.1 MB (2089485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3b43e6036c3e47e9bde8e1b23b2e18ae3881bd6963c58d7378f7ea5b298be8`  
		Last Modified: Wed, 10 Apr 2024 16:31:50 GMT  
		Size: 1.2 MB (1231197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e69525c68188c9fb6f58a63eaf9f54f84812c92027f0fd1def2d187df8c8e68`  
		Last Modified: Wed, 10 Apr 2024 16:31:49 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7c08a590703b057ce8910c40bac6339e039354b046cf91903f72c731edbbe2`  
		Last Modified: Wed, 10 Apr 2024 16:31:51 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:29852f9ed352544975a85e04cce00288b41a6e90c67436126f390bb83a3973af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a23719172438c0c0276e696803f232d54be8c0b6efd0c247d70df9a191177ef6`

```dockerfile
```

-	Layers:
	-	`sha256:9a4464980ebe9ed988705320869e004e29ee47a94854bddf2950f9528b4ea70c`  
		Last Modified: Wed, 10 Apr 2024 16:31:50 GMT  
		Size: 2.3 MB (2264449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65343e5170f1bd22aadd1c65fe274b6156e6fd966337aa0b2e81b58234c21b69`  
		Last Modified: Wed, 10 Apr 2024 16:31:49 GMT  
		Size: 21.1 KB (21114 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:7fed5d02aeac33c3df4a133ce97a03c71d8a3f2713f2ff5c4788cf9096f02162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32758363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2fefeb31b86fb36b67e5a920329724ed9519c1ffeca7fa3cc86b26b876237c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc8e58118ea2b587de344fc120829e4086cf15fa1bfa009c58f17ba08203688`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc85ab0a8a03257329849592bd06635db2c84ae701f76df4c27d15306ea0737`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 2.3 MB (2346212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ebd2971429766b668a79b73696f698513334995b9470c9f9f21da0ca81dfdd`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 1.2 MB (1248481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864c041bfe7d835cabb73fb214a8a4b7a7931b18ba532835f043f470dcd3c81e`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c33e09275e854d41d4c12ccef30c6e4e9997e08df5cbcfe520940eb1edb7884`  
		Last Modified: Wed, 10 Apr 2024 16:40:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:57f39faf16f4225d453c30ea64aeb39b90c82cda39549ab0136192c33fc6fcdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a812ba1f091b4c27268db9e91ddb70c1e855cdc46b49936787eee43df1fa371e`

```dockerfile
```

-	Layers:
	-	`sha256:c70324d70390ac933db840ed30afe02f56c58c7eaabbd1ab134e1fc87513fcff`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 2.3 MB (2261390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0535f7d789eaa3f63c11e92d1af4881c5a73f879e664b3109c1f470ad28dd71b`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 21.0 KB (20993 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:34f5ef517d7f54cc5f88ce0834b5a2d2285b7e453e648114404c375ed5bb5657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33893284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b6a893f1366a34486ca1a3011cdde9de38d5b7635c1227cf0faddfe53bb312`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:d160efeeb02e2200784dd8312a13a11d9d791581efc7756ed999f76c79445b54 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8a3830119a16769024de35d2dfa3d32147da5ea747ec336166bdca1049655803`  
		Last Modified: Wed, 10 Apr 2024 01:02:04 GMT  
		Size: 30.1 MB (30146515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4020925217af165e208be472fc2fcd518c37967f238cbcba0dbec12d20b685`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45dff0ba396ced9bb0bb69ffd5456f2a5cc783b7908bc10f4c194aa328ec3036`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 2.5 MB (2492670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9498280a2172ecdd190d1e4d3e001d55b64bbec93f4eccb039870ebbedd40f64`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 1.3 MB (1252590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf4eb265fb60a5b2351156ea6f2eccf92d961585ba20be18d7e6d3294511507`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a379f21df665e12ab146aebcf0a1cc7e55cbd7a9bbc4d17a209c7a5ba03eeb1`  
		Last Modified: Wed, 10 Apr 2024 01:55:17 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:e3e28c19c9f28d8dfee9784913c92b2a01df26c25a575a77a4f83c23281d8cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e29f55fbf81fc47ec484ab81a55a69d9c1eb3874c9eb08b813638198b69361e`

```dockerfile
```

-	Layers:
	-	`sha256:be647ca90ccc7f88e1eb3a88b1acd85aaac94d593fedbe2cebeee872c8a3b26b`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 2.3 MB (2258259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f2ac7f006c3cff208ffd83fa9513a6b12cf39a1ec192a9f01a088d0240d858b`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 21.1 KB (21087 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; mips64le

```console
$ docker pull memcached@sha256:fc8892b557a9bdb7b41273e3403bc2fdb3d04f99fb56a3874e9081d8dfa128d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32306668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a48487cefaf60f8ad4d3a059b0db4796bee3adbf408393dcc4c49da664f723`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 01:06:19 GMT
ADD file:c03c59e261bb08f39e6a97df2fd4b82f1e11b49a62d1859a8f8efac680b80a88 in / 
# Tue, 12 Mar 2024 01:06:23 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aad79459a0f767fcded51c9547150a1cfd96638972389ab8621b5f3eb4a9c280`  
		Last Modified: Tue, 12 Mar 2024 01:17:09 GMT  
		Size: 29.1 MB (29119205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460befff49885c738329c53c06bca553e2869317c73b0b5f76661a7053f578ad`  
		Last Modified: Tue, 09 Apr 2024 15:25:07 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6dc8cf2380155c1bacde757237b8551c77167e46ac5393332be9deb2b8dbc5`  
		Last Modified: Tue, 09 Apr 2024 15:25:07 GMT  
		Size: 1.9 MB (1937657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66db33dc07294fd7ecc848862384efa6b829c96c8939643a7098e35bbbe81d8f`  
		Last Modified: Tue, 09 Apr 2024 15:25:07 GMT  
		Size: 1.2 MB (1248284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1650df259f3af60ff6184e164ac094f261bffea30679d803c7cff2759e001699`  
		Last Modified: Tue, 09 Apr 2024 15:25:07 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51c337d2a6d822be89d42ae3e0ae8472dbd1673e648f8cdf1c769309105aaca`  
		Last Modified: Tue, 09 Apr 2024 15:25:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:831ec04c94a8b50c1aff4f18c97c8cae1d537c32821a0b8aeca9b0a1aecacae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7033955a79b1242de9912088e5d0f703e2133fce52308636758ba5ce2059d38c`

```dockerfile
```

-	Layers:
	-	`sha256:abd2f28a59a5e89ae224244ff2945a51f564194853e6abaaa8f5648413960325`  
		Last Modified: Tue, 09 Apr 2024 15:25:07 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:dc36455fb79f84d62ac6d34100afc15f0a238192dfa3224e93f753cd67d74798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37135966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:430a51910c252bd83b91329bef7a7f1a2344a5bc6b42075d419bb0facc468286`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:30:19 GMT
ADD file:9273ef56d086dbc93b46b7e8ae424eb04096fb00c693dd6cda1f48346290d4d5 in / 
# Tue, 12 Mar 2024 00:30:24 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c28cd0e276dcdeb4d44f5cc5bb958610750ff902a081b668e3863c2f38eef054`  
		Last Modified: Tue, 12 Mar 2024 00:38:06 GMT  
		Size: 33.1 MB (33119023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708b42bb3654f69ef8bfee96e8cd256f668ec36c0c79dffa3833c5a717f9eb5f`  
		Last Modified: Wed, 20 Mar 2024 21:57:50 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66c4756024ccda97c6fbe022e48d010bf3335191ef2516ace6ee30de5e87389`  
		Last Modified: Wed, 20 Mar 2024 21:57:51 GMT  
		Size: 2.7 MB (2698368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ea5604f0c8a697cb056d47640ff8d8852849f35d9a26e62b42036629bcaf9c`  
		Last Modified: Tue, 09 Apr 2024 05:05:54 GMT  
		Size: 1.3 MB (1317055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810d9546da33f92c2106ed1bbfc26223b8bef8f8e2be48b862a0270380818526`  
		Last Modified: Tue, 09 Apr 2024 05:05:54 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c78ea7da271614754f4fdc7e7d86c64da966e871cce4bab839266e27bd62912`  
		Last Modified: Tue, 09 Apr 2024 05:05:54 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:a78edf1158eed48cbec064a641fcac3c873e1b1fee26b1d8407a0269870baa23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2287859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618f6dcb01dc21ed0cc62f7efaeabc4c883f32d56e5f51a66cba2e87b31ed783`

```dockerfile
```

-	Layers:
	-	`sha256:13692af6f7d1860a31d9a8610f75d0d12eaa87131aef9b5615a57c5aaad34643`  
		Last Modified: Tue, 09 Apr 2024 05:05:54 GMT  
		Size: 2.3 MB (2266816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eae96d76b66c8c2450ce3e926ee185c9043ceff0f51f91e18694e094fd6d91af`  
		Last Modified: Tue, 09 Apr 2024 05:05:53 GMT  
		Size: 21.0 KB (21043 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:3af0cb7bc651113fdea970716a6f0a534823c322990bacbde20cc166648bb952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30873795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d9bcea2e734469166d18b5a96ac76cdcd310b4c95140b542777073e6158051`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:54:02 GMT
ADD file:80ab985d4871ca6a72156bedfe1038e6b1a89591fc2fd86c4ef778d293223aff in / 
# Tue, 12 Mar 2024 00:54:03 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9cada496cd2b8a88571bf23d513e7fce34888d13321fcf23c6613bffe4c37297`  
		Last Modified: Tue, 12 Mar 2024 01:21:14 GMT  
		Size: 27.5 MB (27488684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c430faffa085700d40355ac1aea08d429376e112bef3b9c00780b1ede56859c2`  
		Last Modified: Wed, 20 Mar 2024 22:17:08 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf1db148a80e9f25b06fe946c697ba8fa83bc46c13515904d4ceceaeb2a4eeb`  
		Last Modified: Wed, 20 Mar 2024 22:17:12 GMT  
		Size: 2.2 MB (2152657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400f8ed9afb04b498a060de1a774c9272cec70272754126b664985cd98414623`  
		Last Modified: Tue, 09 Apr 2024 14:59:31 GMT  
		Size: 1.2 MB (1230937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ca205adef44fe63941fcd64a5ea1c792c297534b81b7c23838857081d464f6`  
		Last Modified: Tue, 09 Apr 2024 14:59:31 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b24165a664a9007bca136f51d3c60c906ddf8626c9ab9403969454d4c0c47ac`  
		Last Modified: Tue, 09 Apr 2024 14:59:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:e8a1f799f3a7047f3ea6db5f3bebbdcf84726e7a0b3b45157df167d441495d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee48fbaae81e8e950ac399f89ee0eb0f7ad3e7da77d66ce435def816b3814ca`

```dockerfile
```

-	Layers:
	-	`sha256:bda232575879bf9ee6d85b64ea286f2469deccdb87ecc3991ba0fd95a508d8fa`  
		Last Modified: Tue, 09 Apr 2024 14:59:30 GMT  
		Size: 2.3 MB (2262266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13f17df99c3a427fb2b41aa30a6b4f13b2de20e1567da419bc3c6f2febb08832`  
		Last Modified: Tue, 09 Apr 2024 14:59:31 GMT  
		Size: 20.9 KB (20938 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:9177d35a8e2b4224b2b99ec2930a8dc58f7c5af74a6b8143ae907fe9b11463d4
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
$ docker pull memcached@sha256:6209860fadd758c1ff8287829c97198233d086836a8b9fbf1d08125ba71666b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b686fb4e394c572a1980b134344b94d4673fcf49dd492838d7ee6a22c4c73466`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4ca62cc3e912d97d5818cdb2c21bfd6ef17fb2a46bb9ff37ef80b46aeb7579`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873fcbe9681f30840a11a64dc6ef9dfef47f40b1181e1c876969a13e35b6f5b4`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 104.2 KB (104205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2a65ada68aba9def3ee64975e1d20608c30fbb31babe05bf0a052fd5b9e631`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 952.1 KB (952136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9ac090217572c7ea3a76702db6866b9c0c35dd85d2a2bad5a50ca438050b67`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b997d515984ace5a566abec5f367a569bf51dcb5c860f5f1868154d8d61ca54`  
		Last Modified: Thu, 28 Mar 2024 18:53:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:a3837912bae62cedd588361c1fd7f24dedff8326ee89d994b188f146b2e45cdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048a973a594205e1bb5d398cc6e6d289c18ca8bd7b73c56d883080501a45af67`

```dockerfile
```

-	Layers:
	-	`sha256:fd986e4f48564cc23fae84c6c205ad8bac1f5f7733c03683ce10edf2580aed7c`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d1c90f2da382eb7f6f0edeab7ce48b9f24941fc542612204b5e38600d91d209`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 19.5 KB (19468 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:46208d1529b365696f517731af2230117072d9b61892276113308a9446932698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4425171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b581ee26004a99ed42270719e1ba6c1cc43728d706d223b58f1ded5911100ccb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bfa7663dcfe59a8997ca6332c380cce69151aeff2a9a10b71d5d655460cc3a`  
		Last Modified: Sat, 16 Mar 2024 15:47:28 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0f8117ff80fc4d046d3bf71fc57dd04a8020db6c8c4e9786b1d94d29bd1cc0`  
		Last Modified: Sat, 16 Mar 2024 15:47:28 GMT  
		Size: 120.9 KB (120902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af942211259cead4688eb0d347be9713995f1ee94d1ba1037b0ba392d4a3cdc6`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 954.9 KB (954910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e9c7aae0c99531c564569b2c18c751c8ccf729706ee0d94bbad57a1f44f0c2`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea48c501ddc68741eb04b337b84674ad57f0b41a67064a0b03ebd3003b573352`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:6dc666e80bf78a2d0c87939b02f96bedfa495d9920a7ebc747196b1cd02e2697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b89445ac664e88d593bab80bee2d0d5655c7e8514df793507272c4d185b5f98`

```dockerfile
```

-	Layers:
	-	`sha256:b6ebaa8df2f60e22d5c7a27d50ba950bb848bc48e2ad39eaafcf18f5841306f4`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:744d3c8bb078a1a54e7eff756816d1210742e1b96aea3127f6dbe2dca46c143e`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 19.3 KB (19320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:cb29d2fb5915af23e62234ec3e061ccb9bf0e09ab3146bc5275cb93d06ac2002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4300923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff0463afaa58ff4bd1755643f08e532a20be67f1c75cf31f6f4485c82ebf085`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7101892b4f7a0ec7e893a31b4c4b241666261700594b70af05e5bbde39e1ac`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2a8397306302beb9cd1c51c03f7a33b34efe159dc5423bf0450396a416aa88`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 109.3 KB (109321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6f6638920128a5138269a00784e6e731705c4aa9d114bbbcf0a94fead17efb`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 945.9 KB (945864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d19b89060fd32f477577dfc686f44f32da930716d3e5321a51c36c29b166ece`  
		Last Modified: Thu, 28 Mar 2024 18:53:12 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8ebfbbb8e7bd6745fd67fa4e70d9198ee1a540ce3b792770a1a528feb27510`  
		Last Modified: Thu, 28 Mar 2024 18:53:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:616aed5f6c6e59b28e9b940db41af823662139db453fd3dabfd0a3e4cfe27515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b397ca537b8b98807e225f556a891ee088375459e2b0560dee27496238a6f6bb`

```dockerfile
```

-	Layers:
	-	`sha256:f7c2a6ba891f879d55d2617d901135ce44cc45cb607f46af268d688d06fe6cbe`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:215e98388857b167196047f4301650abb69008e97eb82a06a1a1c1284cd18990`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 19.4 KB (19413 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:fb33bde5c5ef29f5ac1d0ead06479dff74c42b27086fe8c54f0649cce4617709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4473831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4ff16a5d7a50717ec61b2a0456c7ce9e733cf60d44539d4fed95ad3f66e754`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af93c876610139b595b7416c41cc6df9ebba87f0706b7ee1ece6a69ab0bebaa`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fb01a7e673842ded65bdcdcced99c281575743751ca219336ceb9e95b4a0e8`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 123.4 KB (123407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae3717877baa442ae7c73c0af98315cfe57d21554f2647739c792bf44240aa8`  
		Last Modified: Thu, 28 Mar 2024 19:21:45 GMT  
		Size: 990.4 KB (990428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf73c888928175612d13f100f21e51e61f22d752972c4e4c9ca9a412a53f920b`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9be9099f9a93e9d3488286c04ef2fa0350242d4207f50af77a17f89ef7e177`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:0322fdfe59a4b8ee20d7127136f42eefcff450ad57400408c51a88cb7e9914b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf6e6d6ee32aa7b5d034fdd864b17f953c8d03ffbf532b9cf455978c4a87aed`

```dockerfile
```

-	Layers:
	-	`sha256:ab3fad68489df68281f8819ef71a7a4108466ee4b9edc0a5b75db897e14ae32e`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d73a67a0c37803124f85e66364544db0aed3f07ca52ecf082733da70ec9284e1`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 19.4 KB (19370 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:62dab6a9b0b7245477027221202f878ec8ca2b57f0e7b73cd8fd87ddd835c38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4332854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5558373c07611e5d9c5f065de41425c65fcb4edafee9c73f7471e20ecd1c63a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
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
	-	`sha256:f8ad24edb46ae1f03842b15a18bed8c9459caf47c9b44ac9e9f8ceba287a2d99`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 975.4 KB (975434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72add78eac56e24383a18f968c20868c803c6abfde9560e6df8a55ce9ac8420`  
		Last Modified: Thu, 28 Mar 2024 19:28:29 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7415f1d9d4bf360b03d79bc7084a83a370483d24310a700a4dca754c6e3972`  
		Last Modified: Thu, 28 Mar 2024 19:28:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ecba7487095ee7d9a4ab5dc74ce4e434f1a2d8056d87a5a2ddd6b74e82fa3b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32fcbd9dbbf02e688908e774ab684beff7ef28a6afaf60dd34855dd53e199caa`

```dockerfile
```

-	Layers:
	-	`sha256:777960c66626abacd0c8e4e899960921e1a9e3b55adac8dd3c822e7df8945bee`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d43a6b7e3f38d4afafbea91c4b713749a30e42109508da2f9d64a72cd1db3a43`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 19.3 KB (19302 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine3.19`

```console
$ docker pull memcached@sha256:9177d35a8e2b4224b2b99ec2930a8dc58f7c5af74a6b8143ae907fe9b11463d4
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
$ docker pull memcached@sha256:6209860fadd758c1ff8287829c97198233d086836a8b9fbf1d08125ba71666b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b686fb4e394c572a1980b134344b94d4673fcf49dd492838d7ee6a22c4c73466`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4ca62cc3e912d97d5818cdb2c21bfd6ef17fb2a46bb9ff37ef80b46aeb7579`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873fcbe9681f30840a11a64dc6ef9dfef47f40b1181e1c876969a13e35b6f5b4`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 104.2 KB (104205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2a65ada68aba9def3ee64975e1d20608c30fbb31babe05bf0a052fd5b9e631`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 952.1 KB (952136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9ac090217572c7ea3a76702db6866b9c0c35dd85d2a2bad5a50ca438050b67`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b997d515984ace5a566abec5f367a569bf51dcb5c860f5f1868154d8d61ca54`  
		Last Modified: Thu, 28 Mar 2024 18:53:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:a3837912bae62cedd588361c1fd7f24dedff8326ee89d994b188f146b2e45cdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048a973a594205e1bb5d398cc6e6d289c18ca8bd7b73c56d883080501a45af67`

```dockerfile
```

-	Layers:
	-	`sha256:fd986e4f48564cc23fae84c6c205ad8bac1f5f7733c03683ce10edf2580aed7c`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d1c90f2da382eb7f6f0edeab7ce48b9f24941fc542612204b5e38600d91d209`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 19.5 KB (19468 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:46208d1529b365696f517731af2230117072d9b61892276113308a9446932698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4425171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b581ee26004a99ed42270719e1ba6c1cc43728d706d223b58f1ded5911100ccb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bfa7663dcfe59a8997ca6332c380cce69151aeff2a9a10b71d5d655460cc3a`  
		Last Modified: Sat, 16 Mar 2024 15:47:28 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0f8117ff80fc4d046d3bf71fc57dd04a8020db6c8c4e9786b1d94d29bd1cc0`  
		Last Modified: Sat, 16 Mar 2024 15:47:28 GMT  
		Size: 120.9 KB (120902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af942211259cead4688eb0d347be9713995f1ee94d1ba1037b0ba392d4a3cdc6`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 954.9 KB (954910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e9c7aae0c99531c564569b2c18c751c8ccf729706ee0d94bbad57a1f44f0c2`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea48c501ddc68741eb04b337b84674ad57f0b41a67064a0b03ebd3003b573352`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:6dc666e80bf78a2d0c87939b02f96bedfa495d9920a7ebc747196b1cd02e2697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b89445ac664e88d593bab80bee2d0d5655c7e8514df793507272c4d185b5f98`

```dockerfile
```

-	Layers:
	-	`sha256:b6ebaa8df2f60e22d5c7a27d50ba950bb848bc48e2ad39eaafcf18f5841306f4`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:744d3c8bb078a1a54e7eff756816d1210742e1b96aea3127f6dbe2dca46c143e`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 19.3 KB (19320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.19` - linux; 386

```console
$ docker pull memcached@sha256:cb29d2fb5915af23e62234ec3e061ccb9bf0e09ab3146bc5275cb93d06ac2002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4300923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff0463afaa58ff4bd1755643f08e532a20be67f1c75cf31f6f4485c82ebf085`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7101892b4f7a0ec7e893a31b4c4b241666261700594b70af05e5bbde39e1ac`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2a8397306302beb9cd1c51c03f7a33b34efe159dc5423bf0450396a416aa88`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 109.3 KB (109321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6f6638920128a5138269a00784e6e731705c4aa9d114bbbcf0a94fead17efb`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 945.9 KB (945864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d19b89060fd32f477577dfc686f44f32da930716d3e5321a51c36c29b166ece`  
		Last Modified: Thu, 28 Mar 2024 18:53:12 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8ebfbbb8e7bd6745fd67fa4e70d9198ee1a540ce3b792770a1a528feb27510`  
		Last Modified: Thu, 28 Mar 2024 18:53:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:616aed5f6c6e59b28e9b940db41af823662139db453fd3dabfd0a3e4cfe27515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b397ca537b8b98807e225f556a891ee088375459e2b0560dee27496238a6f6bb`

```dockerfile
```

-	Layers:
	-	`sha256:f7c2a6ba891f879d55d2617d901135ce44cc45cb607f46af268d688d06fe6cbe`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:215e98388857b167196047f4301650abb69008e97eb82a06a1a1c1284cd18990`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 19.4 KB (19413 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.19` - linux; ppc64le

```console
$ docker pull memcached@sha256:fb33bde5c5ef29f5ac1d0ead06479dff74c42b27086fe8c54f0649cce4617709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4473831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4ff16a5d7a50717ec61b2a0456c7ce9e733cf60d44539d4fed95ad3f66e754`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af93c876610139b595b7416c41cc6df9ebba87f0706b7ee1ece6a69ab0bebaa`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fb01a7e673842ded65bdcdcced99c281575743751ca219336ceb9e95b4a0e8`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 123.4 KB (123407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae3717877baa442ae7c73c0af98315cfe57d21554f2647739c792bf44240aa8`  
		Last Modified: Thu, 28 Mar 2024 19:21:45 GMT  
		Size: 990.4 KB (990428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf73c888928175612d13f100f21e51e61f22d752972c4e4c9ca9a412a53f920b`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9be9099f9a93e9d3488286c04ef2fa0350242d4207f50af77a17f89ef7e177`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:0322fdfe59a4b8ee20d7127136f42eefcff450ad57400408c51a88cb7e9914b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf6e6d6ee32aa7b5d034fdd864b17f953c8d03ffbf532b9cf455978c4a87aed`

```dockerfile
```

-	Layers:
	-	`sha256:ab3fad68489df68281f8819ef71a7a4108466ee4b9edc0a5b75db897e14ae32e`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d73a67a0c37803124f85e66364544db0aed3f07ca52ecf082733da70ec9284e1`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 19.4 KB (19370 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.19` - linux; s390x

```console
$ docker pull memcached@sha256:62dab6a9b0b7245477027221202f878ec8ca2b57f0e7b73cd8fd87ddd835c38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4332854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5558373c07611e5d9c5f065de41425c65fcb4edafee9c73f7471e20ecd1c63a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
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
	-	`sha256:f8ad24edb46ae1f03842b15a18bed8c9459caf47c9b44ac9e9f8ceba287a2d99`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 975.4 KB (975434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72add78eac56e24383a18f968c20868c803c6abfde9560e6df8a55ce9ac8420`  
		Last Modified: Thu, 28 Mar 2024 19:28:29 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7415f1d9d4bf360b03d79bc7084a83a370483d24310a700a4dca754c6e3972`  
		Last Modified: Thu, 28 Mar 2024 19:28:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:ecba7487095ee7d9a4ab5dc74ce4e434f1a2d8056d87a5a2ddd6b74e82fa3b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32fcbd9dbbf02e688908e774ab684beff7ef28a6afaf60dd34855dd53e199caa`

```dockerfile
```

-	Layers:
	-	`sha256:777960c66626abacd0c8e4e899960921e1a9e3b55adac8dd3c822e7df8945bee`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d43a6b7e3f38d4afafbea91c4b713749a30e42109508da2f9d64a72cd1db3a43`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 19.3 KB (19302 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-bookworm`

```console
$ docker pull memcached@sha256:9eb572b94abad82c04f1329c97e72684931b1dda2cb5c0ee6c4d115f76d6b037
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
$ docker pull memcached@sha256:2967dc980ac80883003061c899102ed6c8749ed50712d4cf592b7c53efd7a498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32872677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7787f9f0d27b97ee6da8b7b2fdf9dec18a1c0fa6c05b0d4a454cc84138bfceb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131f56ef3fe0a1487206d17cc66325f94d97854c231561697099f0162c37a033`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa35112bf68c5c494491a4c7fbbb8ba5e4d9d410ce9150f1b3238414cbc091b0`  
		Last Modified: Wed, 10 Apr 2024 02:57:19 GMT  
		Size: 2.5 MB (2488500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a672c032d4a7b7c0de949d9fe1d4896cc7da42256b16e1daba353de964968b8`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 1.3 MB (1251305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01135bb689569cd15c6a2b8d8e115947652e4d61a01127729ea24513d1f57d2`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48f53906ef45e3138f6a1f1ee8ebd01ca24a3c3a2c15301afe932077984afbb`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:ace7b79050b8d00e7046345e319209248f2ce44b7b3a67968e6662d559b4cebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0612146bf8ed0f19690c2070f49b81b2f59f0df0c0aee6b38606b04c32b3b1bc`

```dockerfile
```

-	Layers:
	-	`sha256:cbbd757e27c72cb57f0f51a89cb3d65360e0afa594c47eff406c9db9d3a27de0`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 2.3 MB (2261161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d398ef36731f34f7e28948dd252f5bd1ec36dbc3a4f7b23dd7fc9d195992db2`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 21.1 KB (21142 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:794b039b86010e20defef81d8fe493212a10d4c4f774d39e7c09aaaf8a9e3ebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30212760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:916c48be9c03801f4162ac2f2e46c0e5d0c8ffa27e110dff6f876cfe88d992ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:bfe2e0ed45dd2920845bd9283b7d13266c82fe9f48ba261b6529c28dc246d3e4 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:60d288182f6883c1ed662f82d32316348aac8ca45c943f1093aed5c0ed01b45c`  
		Last Modified: Wed, 10 Apr 2024 00:54:34 GMT  
		Size: 26.9 MB (26890564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2034ec998bbde42652af813854ab5c0f1dd9c547b6b0c4680f48b2f545ede0ef`  
		Last Modified: Wed, 10 Apr 2024 16:31:49 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d77e350a8c89faec28416a879441cd67ed9d418f318b1426c3961607be04f57`  
		Last Modified: Wed, 10 Apr 2024 16:31:50 GMT  
		Size: 2.1 MB (2089485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3b43e6036c3e47e9bde8e1b23b2e18ae3881bd6963c58d7378f7ea5b298be8`  
		Last Modified: Wed, 10 Apr 2024 16:31:50 GMT  
		Size: 1.2 MB (1231197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e69525c68188c9fb6f58a63eaf9f54f84812c92027f0fd1def2d187df8c8e68`  
		Last Modified: Wed, 10 Apr 2024 16:31:49 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7c08a590703b057ce8910c40bac6339e039354b046cf91903f72c731edbbe2`  
		Last Modified: Wed, 10 Apr 2024 16:31:51 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:29852f9ed352544975a85e04cce00288b41a6e90c67436126f390bb83a3973af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a23719172438c0c0276e696803f232d54be8c0b6efd0c247d70df9a191177ef6`

```dockerfile
```

-	Layers:
	-	`sha256:9a4464980ebe9ed988705320869e004e29ee47a94854bddf2950f9528b4ea70c`  
		Last Modified: Wed, 10 Apr 2024 16:31:50 GMT  
		Size: 2.3 MB (2264449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65343e5170f1bd22aadd1c65fe274b6156e6fd966337aa0b2e81b58234c21b69`  
		Last Modified: Wed, 10 Apr 2024 16:31:49 GMT  
		Size: 21.1 KB (21114 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:7fed5d02aeac33c3df4a133ce97a03c71d8a3f2713f2ff5c4788cf9096f02162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32758363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2fefeb31b86fb36b67e5a920329724ed9519c1ffeca7fa3cc86b26b876237c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc8e58118ea2b587de344fc120829e4086cf15fa1bfa009c58f17ba08203688`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc85ab0a8a03257329849592bd06635db2c84ae701f76df4c27d15306ea0737`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 2.3 MB (2346212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ebd2971429766b668a79b73696f698513334995b9470c9f9f21da0ca81dfdd`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 1.2 MB (1248481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864c041bfe7d835cabb73fb214a8a4b7a7931b18ba532835f043f470dcd3c81e`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c33e09275e854d41d4c12ccef30c6e4e9997e08df5cbcfe520940eb1edb7884`  
		Last Modified: Wed, 10 Apr 2024 16:40:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:57f39faf16f4225d453c30ea64aeb39b90c82cda39549ab0136192c33fc6fcdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a812ba1f091b4c27268db9e91ddb70c1e855cdc46b49936787eee43df1fa371e`

```dockerfile
```

-	Layers:
	-	`sha256:c70324d70390ac933db840ed30afe02f56c58c7eaabbd1ab134e1fc87513fcff`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 2.3 MB (2261390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0535f7d789eaa3f63c11e92d1af4881c5a73f879e664b3109c1f470ad28dd71b`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 21.0 KB (20993 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:34f5ef517d7f54cc5f88ce0834b5a2d2285b7e453e648114404c375ed5bb5657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33893284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b6a893f1366a34486ca1a3011cdde9de38d5b7635c1227cf0faddfe53bb312`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:d160efeeb02e2200784dd8312a13a11d9d791581efc7756ed999f76c79445b54 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8a3830119a16769024de35d2dfa3d32147da5ea747ec336166bdca1049655803`  
		Last Modified: Wed, 10 Apr 2024 01:02:04 GMT  
		Size: 30.1 MB (30146515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4020925217af165e208be472fc2fcd518c37967f238cbcba0dbec12d20b685`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45dff0ba396ced9bb0bb69ffd5456f2a5cc783b7908bc10f4c194aa328ec3036`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 2.5 MB (2492670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9498280a2172ecdd190d1e4d3e001d55b64bbec93f4eccb039870ebbedd40f64`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 1.3 MB (1252590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf4eb265fb60a5b2351156ea6f2eccf92d961585ba20be18d7e6d3294511507`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a379f21df665e12ab146aebcf0a1cc7e55cbd7a9bbc4d17a209c7a5ba03eeb1`  
		Last Modified: Wed, 10 Apr 2024 01:55:17 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:e3e28c19c9f28d8dfee9784913c92b2a01df26c25a575a77a4f83c23281d8cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e29f55fbf81fc47ec484ab81a55a69d9c1eb3874c9eb08b813638198b69361e`

```dockerfile
```

-	Layers:
	-	`sha256:be647ca90ccc7f88e1eb3a88b1acd85aaac94d593fedbe2cebeee872c8a3b26b`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 2.3 MB (2258259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f2ac7f006c3cff208ffd83fa9513a6b12cf39a1ec192a9f01a088d0240d858b`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 21.1 KB (21087 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:fc8892b557a9bdb7b41273e3403bc2fdb3d04f99fb56a3874e9081d8dfa128d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32306668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a48487cefaf60f8ad4d3a059b0db4796bee3adbf408393dcc4c49da664f723`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 01:06:19 GMT
ADD file:c03c59e261bb08f39e6a97df2fd4b82f1e11b49a62d1859a8f8efac680b80a88 in / 
# Tue, 12 Mar 2024 01:06:23 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aad79459a0f767fcded51c9547150a1cfd96638972389ab8621b5f3eb4a9c280`  
		Last Modified: Tue, 12 Mar 2024 01:17:09 GMT  
		Size: 29.1 MB (29119205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460befff49885c738329c53c06bca553e2869317c73b0b5f76661a7053f578ad`  
		Last Modified: Tue, 09 Apr 2024 15:25:07 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6dc8cf2380155c1bacde757237b8551c77167e46ac5393332be9deb2b8dbc5`  
		Last Modified: Tue, 09 Apr 2024 15:25:07 GMT  
		Size: 1.9 MB (1937657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66db33dc07294fd7ecc848862384efa6b829c96c8939643a7098e35bbbe81d8f`  
		Last Modified: Tue, 09 Apr 2024 15:25:07 GMT  
		Size: 1.2 MB (1248284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1650df259f3af60ff6184e164ac094f261bffea30679d803c7cff2759e001699`  
		Last Modified: Tue, 09 Apr 2024 15:25:07 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51c337d2a6d822be89d42ae3e0ae8472dbd1673e648f8cdf1c769309105aaca`  
		Last Modified: Tue, 09 Apr 2024 15:25:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:831ec04c94a8b50c1aff4f18c97c8cae1d537c32821a0b8aeca9b0a1aecacae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7033955a79b1242de9912088e5d0f703e2133fce52308636758ba5ce2059d38c`

```dockerfile
```

-	Layers:
	-	`sha256:abd2f28a59a5e89ae224244ff2945a51f564194853e6abaaa8f5648413960325`  
		Last Modified: Tue, 09 Apr 2024 15:25:07 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:dc36455fb79f84d62ac6d34100afc15f0a238192dfa3224e93f753cd67d74798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37135966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:430a51910c252bd83b91329bef7a7f1a2344a5bc6b42075d419bb0facc468286`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:30:19 GMT
ADD file:9273ef56d086dbc93b46b7e8ae424eb04096fb00c693dd6cda1f48346290d4d5 in / 
# Tue, 12 Mar 2024 00:30:24 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c28cd0e276dcdeb4d44f5cc5bb958610750ff902a081b668e3863c2f38eef054`  
		Last Modified: Tue, 12 Mar 2024 00:38:06 GMT  
		Size: 33.1 MB (33119023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708b42bb3654f69ef8bfee96e8cd256f668ec36c0c79dffa3833c5a717f9eb5f`  
		Last Modified: Wed, 20 Mar 2024 21:57:50 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66c4756024ccda97c6fbe022e48d010bf3335191ef2516ace6ee30de5e87389`  
		Last Modified: Wed, 20 Mar 2024 21:57:51 GMT  
		Size: 2.7 MB (2698368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ea5604f0c8a697cb056d47640ff8d8852849f35d9a26e62b42036629bcaf9c`  
		Last Modified: Tue, 09 Apr 2024 05:05:54 GMT  
		Size: 1.3 MB (1317055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810d9546da33f92c2106ed1bbfc26223b8bef8f8e2be48b862a0270380818526`  
		Last Modified: Tue, 09 Apr 2024 05:05:54 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c78ea7da271614754f4fdc7e7d86c64da966e871cce4bab839266e27bd62912`  
		Last Modified: Tue, 09 Apr 2024 05:05:54 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:a78edf1158eed48cbec064a641fcac3c873e1b1fee26b1d8407a0269870baa23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2287859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618f6dcb01dc21ed0cc62f7efaeabc4c883f32d56e5f51a66cba2e87b31ed783`

```dockerfile
```

-	Layers:
	-	`sha256:13692af6f7d1860a31d9a8610f75d0d12eaa87131aef9b5615a57c5aaad34643`  
		Last Modified: Tue, 09 Apr 2024 05:05:54 GMT  
		Size: 2.3 MB (2266816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eae96d76b66c8c2450ce3e926ee185c9043ceff0f51f91e18694e094fd6d91af`  
		Last Modified: Tue, 09 Apr 2024 05:05:53 GMT  
		Size: 21.0 KB (21043 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:3af0cb7bc651113fdea970716a6f0a534823c322990bacbde20cc166648bb952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30873795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d9bcea2e734469166d18b5a96ac76cdcd310b4c95140b542777073e6158051`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:54:02 GMT
ADD file:80ab985d4871ca6a72156bedfe1038e6b1a89591fc2fd86c4ef778d293223aff in / 
# Tue, 12 Mar 2024 00:54:03 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9cada496cd2b8a88571bf23d513e7fce34888d13321fcf23c6613bffe4c37297`  
		Last Modified: Tue, 12 Mar 2024 01:21:14 GMT  
		Size: 27.5 MB (27488684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c430faffa085700d40355ac1aea08d429376e112bef3b9c00780b1ede56859c2`  
		Last Modified: Wed, 20 Mar 2024 22:17:08 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf1db148a80e9f25b06fe946c697ba8fa83bc46c13515904d4ceceaeb2a4eeb`  
		Last Modified: Wed, 20 Mar 2024 22:17:12 GMT  
		Size: 2.2 MB (2152657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400f8ed9afb04b498a060de1a774c9272cec70272754126b664985cd98414623`  
		Last Modified: Tue, 09 Apr 2024 14:59:31 GMT  
		Size: 1.2 MB (1230937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ca205adef44fe63941fcd64a5ea1c792c297534b81b7c23838857081d464f6`  
		Last Modified: Tue, 09 Apr 2024 14:59:31 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b24165a664a9007bca136f51d3c60c906ddf8626c9ab9403969454d4c0c47ac`  
		Last Modified: Tue, 09 Apr 2024 14:59:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:e8a1f799f3a7047f3ea6db5f3bebbdcf84726e7a0b3b45157df167d441495d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee48fbaae81e8e950ac399f89ee0eb0f7ad3e7da77d66ce435def816b3814ca`

```dockerfile
```

-	Layers:
	-	`sha256:bda232575879bf9ee6d85b64ea286f2469deccdb87ecc3991ba0fd95a508d8fa`  
		Last Modified: Tue, 09 Apr 2024 14:59:30 GMT  
		Size: 2.3 MB (2262266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13f17df99c3a427fb2b41aa30a6b4f13b2de20e1567da419bc3c6f2febb08832`  
		Last Modified: Tue, 09 Apr 2024 14:59:31 GMT  
		Size: 20.9 KB (20938 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6`

```console
$ docker pull memcached@sha256:9eb572b94abad82c04f1329c97e72684931b1dda2cb5c0ee6c4d115f76d6b037
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
$ docker pull memcached@sha256:2967dc980ac80883003061c899102ed6c8749ed50712d4cf592b7c53efd7a498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32872677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7787f9f0d27b97ee6da8b7b2fdf9dec18a1c0fa6c05b0d4a454cc84138bfceb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131f56ef3fe0a1487206d17cc66325f94d97854c231561697099f0162c37a033`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa35112bf68c5c494491a4c7fbbb8ba5e4d9d410ce9150f1b3238414cbc091b0`  
		Last Modified: Wed, 10 Apr 2024 02:57:19 GMT  
		Size: 2.5 MB (2488500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a672c032d4a7b7c0de949d9fe1d4896cc7da42256b16e1daba353de964968b8`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 1.3 MB (1251305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01135bb689569cd15c6a2b8d8e115947652e4d61a01127729ea24513d1f57d2`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48f53906ef45e3138f6a1f1ee8ebd01ca24a3c3a2c15301afe932077984afbb`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:ace7b79050b8d00e7046345e319209248f2ce44b7b3a67968e6662d559b4cebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0612146bf8ed0f19690c2070f49b81b2f59f0df0c0aee6b38606b04c32b3b1bc`

```dockerfile
```

-	Layers:
	-	`sha256:cbbd757e27c72cb57f0f51a89cb3d65360e0afa594c47eff406c9db9d3a27de0`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 2.3 MB (2261161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d398ef36731f34f7e28948dd252f5bd1ec36dbc3a4f7b23dd7fc9d195992db2`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 21.1 KB (21142 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:794b039b86010e20defef81d8fe493212a10d4c4f774d39e7c09aaaf8a9e3ebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30212760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:916c48be9c03801f4162ac2f2e46c0e5d0c8ffa27e110dff6f876cfe88d992ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:bfe2e0ed45dd2920845bd9283b7d13266c82fe9f48ba261b6529c28dc246d3e4 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:60d288182f6883c1ed662f82d32316348aac8ca45c943f1093aed5c0ed01b45c`  
		Last Modified: Wed, 10 Apr 2024 00:54:34 GMT  
		Size: 26.9 MB (26890564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2034ec998bbde42652af813854ab5c0f1dd9c547b6b0c4680f48b2f545ede0ef`  
		Last Modified: Wed, 10 Apr 2024 16:31:49 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d77e350a8c89faec28416a879441cd67ed9d418f318b1426c3961607be04f57`  
		Last Modified: Wed, 10 Apr 2024 16:31:50 GMT  
		Size: 2.1 MB (2089485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3b43e6036c3e47e9bde8e1b23b2e18ae3881bd6963c58d7378f7ea5b298be8`  
		Last Modified: Wed, 10 Apr 2024 16:31:50 GMT  
		Size: 1.2 MB (1231197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e69525c68188c9fb6f58a63eaf9f54f84812c92027f0fd1def2d187df8c8e68`  
		Last Modified: Wed, 10 Apr 2024 16:31:49 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7c08a590703b057ce8910c40bac6339e039354b046cf91903f72c731edbbe2`  
		Last Modified: Wed, 10 Apr 2024 16:31:51 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:29852f9ed352544975a85e04cce00288b41a6e90c67436126f390bb83a3973af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a23719172438c0c0276e696803f232d54be8c0b6efd0c247d70df9a191177ef6`

```dockerfile
```

-	Layers:
	-	`sha256:9a4464980ebe9ed988705320869e004e29ee47a94854bddf2950f9528b4ea70c`  
		Last Modified: Wed, 10 Apr 2024 16:31:50 GMT  
		Size: 2.3 MB (2264449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65343e5170f1bd22aadd1c65fe274b6156e6fd966337aa0b2e81b58234c21b69`  
		Last Modified: Wed, 10 Apr 2024 16:31:49 GMT  
		Size: 21.1 KB (21114 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:7fed5d02aeac33c3df4a133ce97a03c71d8a3f2713f2ff5c4788cf9096f02162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32758363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2fefeb31b86fb36b67e5a920329724ed9519c1ffeca7fa3cc86b26b876237c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc8e58118ea2b587de344fc120829e4086cf15fa1bfa009c58f17ba08203688`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc85ab0a8a03257329849592bd06635db2c84ae701f76df4c27d15306ea0737`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 2.3 MB (2346212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ebd2971429766b668a79b73696f698513334995b9470c9f9f21da0ca81dfdd`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 1.2 MB (1248481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864c041bfe7d835cabb73fb214a8a4b7a7931b18ba532835f043f470dcd3c81e`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c33e09275e854d41d4c12ccef30c6e4e9997e08df5cbcfe520940eb1edb7884`  
		Last Modified: Wed, 10 Apr 2024 16:40:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:57f39faf16f4225d453c30ea64aeb39b90c82cda39549ab0136192c33fc6fcdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a812ba1f091b4c27268db9e91ddb70c1e855cdc46b49936787eee43df1fa371e`

```dockerfile
```

-	Layers:
	-	`sha256:c70324d70390ac933db840ed30afe02f56c58c7eaabbd1ab134e1fc87513fcff`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 2.3 MB (2261390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0535f7d789eaa3f63c11e92d1af4881c5a73f879e664b3109c1f470ad28dd71b`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 21.0 KB (20993 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; 386

```console
$ docker pull memcached@sha256:34f5ef517d7f54cc5f88ce0834b5a2d2285b7e453e648114404c375ed5bb5657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33893284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b6a893f1366a34486ca1a3011cdde9de38d5b7635c1227cf0faddfe53bb312`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:d160efeeb02e2200784dd8312a13a11d9d791581efc7756ed999f76c79445b54 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8a3830119a16769024de35d2dfa3d32147da5ea747ec336166bdca1049655803`  
		Last Modified: Wed, 10 Apr 2024 01:02:04 GMT  
		Size: 30.1 MB (30146515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4020925217af165e208be472fc2fcd518c37967f238cbcba0dbec12d20b685`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45dff0ba396ced9bb0bb69ffd5456f2a5cc783b7908bc10f4c194aa328ec3036`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 2.5 MB (2492670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9498280a2172ecdd190d1e4d3e001d55b64bbec93f4eccb039870ebbedd40f64`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 1.3 MB (1252590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf4eb265fb60a5b2351156ea6f2eccf92d961585ba20be18d7e6d3294511507`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a379f21df665e12ab146aebcf0a1cc7e55cbd7a9bbc4d17a209c7a5ba03eeb1`  
		Last Modified: Wed, 10 Apr 2024 01:55:17 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:e3e28c19c9f28d8dfee9784913c92b2a01df26c25a575a77a4f83c23281d8cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e29f55fbf81fc47ec484ab81a55a69d9c1eb3874c9eb08b813638198b69361e`

```dockerfile
```

-	Layers:
	-	`sha256:be647ca90ccc7f88e1eb3a88b1acd85aaac94d593fedbe2cebeee872c8a3b26b`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 2.3 MB (2258259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f2ac7f006c3cff208ffd83fa9513a6b12cf39a1ec192a9f01a088d0240d858b`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 21.1 KB (21087 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; mips64le

```console
$ docker pull memcached@sha256:fc8892b557a9bdb7b41273e3403bc2fdb3d04f99fb56a3874e9081d8dfa128d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32306668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a48487cefaf60f8ad4d3a059b0db4796bee3adbf408393dcc4c49da664f723`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 01:06:19 GMT
ADD file:c03c59e261bb08f39e6a97df2fd4b82f1e11b49a62d1859a8f8efac680b80a88 in / 
# Tue, 12 Mar 2024 01:06:23 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aad79459a0f767fcded51c9547150a1cfd96638972389ab8621b5f3eb4a9c280`  
		Last Modified: Tue, 12 Mar 2024 01:17:09 GMT  
		Size: 29.1 MB (29119205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460befff49885c738329c53c06bca553e2869317c73b0b5f76661a7053f578ad`  
		Last Modified: Tue, 09 Apr 2024 15:25:07 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6dc8cf2380155c1bacde757237b8551c77167e46ac5393332be9deb2b8dbc5`  
		Last Modified: Tue, 09 Apr 2024 15:25:07 GMT  
		Size: 1.9 MB (1937657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66db33dc07294fd7ecc848862384efa6b829c96c8939643a7098e35bbbe81d8f`  
		Last Modified: Tue, 09 Apr 2024 15:25:07 GMT  
		Size: 1.2 MB (1248284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1650df259f3af60ff6184e164ac094f261bffea30679d803c7cff2759e001699`  
		Last Modified: Tue, 09 Apr 2024 15:25:07 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51c337d2a6d822be89d42ae3e0ae8472dbd1673e648f8cdf1c769309105aaca`  
		Last Modified: Tue, 09 Apr 2024 15:25:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:831ec04c94a8b50c1aff4f18c97c8cae1d537c32821a0b8aeca9b0a1aecacae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7033955a79b1242de9912088e5d0f703e2133fce52308636758ba5ce2059d38c`

```dockerfile
```

-	Layers:
	-	`sha256:abd2f28a59a5e89ae224244ff2945a51f564194853e6abaaa8f5648413960325`  
		Last Modified: Tue, 09 Apr 2024 15:25:07 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:dc36455fb79f84d62ac6d34100afc15f0a238192dfa3224e93f753cd67d74798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37135966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:430a51910c252bd83b91329bef7a7f1a2344a5bc6b42075d419bb0facc468286`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:30:19 GMT
ADD file:9273ef56d086dbc93b46b7e8ae424eb04096fb00c693dd6cda1f48346290d4d5 in / 
# Tue, 12 Mar 2024 00:30:24 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c28cd0e276dcdeb4d44f5cc5bb958610750ff902a081b668e3863c2f38eef054`  
		Last Modified: Tue, 12 Mar 2024 00:38:06 GMT  
		Size: 33.1 MB (33119023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708b42bb3654f69ef8bfee96e8cd256f668ec36c0c79dffa3833c5a717f9eb5f`  
		Last Modified: Wed, 20 Mar 2024 21:57:50 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66c4756024ccda97c6fbe022e48d010bf3335191ef2516ace6ee30de5e87389`  
		Last Modified: Wed, 20 Mar 2024 21:57:51 GMT  
		Size: 2.7 MB (2698368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ea5604f0c8a697cb056d47640ff8d8852849f35d9a26e62b42036629bcaf9c`  
		Last Modified: Tue, 09 Apr 2024 05:05:54 GMT  
		Size: 1.3 MB (1317055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810d9546da33f92c2106ed1bbfc26223b8bef8f8e2be48b862a0270380818526`  
		Last Modified: Tue, 09 Apr 2024 05:05:54 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c78ea7da271614754f4fdc7e7d86c64da966e871cce4bab839266e27bd62912`  
		Last Modified: Tue, 09 Apr 2024 05:05:54 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:a78edf1158eed48cbec064a641fcac3c873e1b1fee26b1d8407a0269870baa23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2287859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618f6dcb01dc21ed0cc62f7efaeabc4c883f32d56e5f51a66cba2e87b31ed783`

```dockerfile
```

-	Layers:
	-	`sha256:13692af6f7d1860a31d9a8610f75d0d12eaa87131aef9b5615a57c5aaad34643`  
		Last Modified: Tue, 09 Apr 2024 05:05:54 GMT  
		Size: 2.3 MB (2266816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eae96d76b66c8c2450ce3e926ee185c9043ceff0f51f91e18694e094fd6d91af`  
		Last Modified: Tue, 09 Apr 2024 05:05:53 GMT  
		Size: 21.0 KB (21043 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; s390x

```console
$ docker pull memcached@sha256:3af0cb7bc651113fdea970716a6f0a534823c322990bacbde20cc166648bb952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30873795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d9bcea2e734469166d18b5a96ac76cdcd310b4c95140b542777073e6158051`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:54:02 GMT
ADD file:80ab985d4871ca6a72156bedfe1038e6b1a89591fc2fd86c4ef778d293223aff in / 
# Tue, 12 Mar 2024 00:54:03 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9cada496cd2b8a88571bf23d513e7fce34888d13321fcf23c6613bffe4c37297`  
		Last Modified: Tue, 12 Mar 2024 01:21:14 GMT  
		Size: 27.5 MB (27488684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c430faffa085700d40355ac1aea08d429376e112bef3b9c00780b1ede56859c2`  
		Last Modified: Wed, 20 Mar 2024 22:17:08 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf1db148a80e9f25b06fe946c697ba8fa83bc46c13515904d4ceceaeb2a4eeb`  
		Last Modified: Wed, 20 Mar 2024 22:17:12 GMT  
		Size: 2.2 MB (2152657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400f8ed9afb04b498a060de1a774c9272cec70272754126b664985cd98414623`  
		Last Modified: Tue, 09 Apr 2024 14:59:31 GMT  
		Size: 1.2 MB (1230937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ca205adef44fe63941fcd64a5ea1c792c297534b81b7c23838857081d464f6`  
		Last Modified: Tue, 09 Apr 2024 14:59:31 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b24165a664a9007bca136f51d3c60c906ddf8626c9ab9403969454d4c0c47ac`  
		Last Modified: Tue, 09 Apr 2024 14:59:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:e8a1f799f3a7047f3ea6db5f3bebbdcf84726e7a0b3b45157df167d441495d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee48fbaae81e8e950ac399f89ee0eb0f7ad3e7da77d66ce435def816b3814ca`

```dockerfile
```

-	Layers:
	-	`sha256:bda232575879bf9ee6d85b64ea286f2469deccdb87ecc3991ba0fd95a508d8fa`  
		Last Modified: Tue, 09 Apr 2024 14:59:30 GMT  
		Size: 2.3 MB (2262266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13f17df99c3a427fb2b41aa30a6b4f13b2de20e1567da419bc3c6f2febb08832`  
		Last Modified: Tue, 09 Apr 2024 14:59:31 GMT  
		Size: 20.9 KB (20938 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine`

```console
$ docker pull memcached@sha256:9177d35a8e2b4224b2b99ec2930a8dc58f7c5af74a6b8143ae907fe9b11463d4
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
$ docker pull memcached@sha256:6209860fadd758c1ff8287829c97198233d086836a8b9fbf1d08125ba71666b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b686fb4e394c572a1980b134344b94d4673fcf49dd492838d7ee6a22c4c73466`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4ca62cc3e912d97d5818cdb2c21bfd6ef17fb2a46bb9ff37ef80b46aeb7579`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873fcbe9681f30840a11a64dc6ef9dfef47f40b1181e1c876969a13e35b6f5b4`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 104.2 KB (104205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2a65ada68aba9def3ee64975e1d20608c30fbb31babe05bf0a052fd5b9e631`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 952.1 KB (952136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9ac090217572c7ea3a76702db6866b9c0c35dd85d2a2bad5a50ca438050b67`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b997d515984ace5a566abec5f367a569bf51dcb5c860f5f1868154d8d61ca54`  
		Last Modified: Thu, 28 Mar 2024 18:53:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:a3837912bae62cedd588361c1fd7f24dedff8326ee89d994b188f146b2e45cdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048a973a594205e1bb5d398cc6e6d289c18ca8bd7b73c56d883080501a45af67`

```dockerfile
```

-	Layers:
	-	`sha256:fd986e4f48564cc23fae84c6c205ad8bac1f5f7733c03683ce10edf2580aed7c`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d1c90f2da382eb7f6f0edeab7ce48b9f24941fc542612204b5e38600d91d209`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 19.5 KB (19468 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:46208d1529b365696f517731af2230117072d9b61892276113308a9446932698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4425171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b581ee26004a99ed42270719e1ba6c1cc43728d706d223b58f1ded5911100ccb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bfa7663dcfe59a8997ca6332c380cce69151aeff2a9a10b71d5d655460cc3a`  
		Last Modified: Sat, 16 Mar 2024 15:47:28 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0f8117ff80fc4d046d3bf71fc57dd04a8020db6c8c4e9786b1d94d29bd1cc0`  
		Last Modified: Sat, 16 Mar 2024 15:47:28 GMT  
		Size: 120.9 KB (120902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af942211259cead4688eb0d347be9713995f1ee94d1ba1037b0ba392d4a3cdc6`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 954.9 KB (954910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e9c7aae0c99531c564569b2c18c751c8ccf729706ee0d94bbad57a1f44f0c2`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea48c501ddc68741eb04b337b84674ad57f0b41a67064a0b03ebd3003b573352`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:6dc666e80bf78a2d0c87939b02f96bedfa495d9920a7ebc747196b1cd02e2697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b89445ac664e88d593bab80bee2d0d5655c7e8514df793507272c4d185b5f98`

```dockerfile
```

-	Layers:
	-	`sha256:b6ebaa8df2f60e22d5c7a27d50ba950bb848bc48e2ad39eaafcf18f5841306f4`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:744d3c8bb078a1a54e7eff756816d1210742e1b96aea3127f6dbe2dca46c143e`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 19.3 KB (19320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:cb29d2fb5915af23e62234ec3e061ccb9bf0e09ab3146bc5275cb93d06ac2002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4300923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff0463afaa58ff4bd1755643f08e532a20be67f1c75cf31f6f4485c82ebf085`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7101892b4f7a0ec7e893a31b4c4b241666261700594b70af05e5bbde39e1ac`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2a8397306302beb9cd1c51c03f7a33b34efe159dc5423bf0450396a416aa88`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 109.3 KB (109321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6f6638920128a5138269a00784e6e731705c4aa9d114bbbcf0a94fead17efb`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 945.9 KB (945864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d19b89060fd32f477577dfc686f44f32da930716d3e5321a51c36c29b166ece`  
		Last Modified: Thu, 28 Mar 2024 18:53:12 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8ebfbbb8e7bd6745fd67fa4e70d9198ee1a540ce3b792770a1a528feb27510`  
		Last Modified: Thu, 28 Mar 2024 18:53:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:616aed5f6c6e59b28e9b940db41af823662139db453fd3dabfd0a3e4cfe27515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b397ca537b8b98807e225f556a891ee088375459e2b0560dee27496238a6f6bb`

```dockerfile
```

-	Layers:
	-	`sha256:f7c2a6ba891f879d55d2617d901135ce44cc45cb607f46af268d688d06fe6cbe`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:215e98388857b167196047f4301650abb69008e97eb82a06a1a1c1284cd18990`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 19.4 KB (19413 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:fb33bde5c5ef29f5ac1d0ead06479dff74c42b27086fe8c54f0649cce4617709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4473831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4ff16a5d7a50717ec61b2a0456c7ce9e733cf60d44539d4fed95ad3f66e754`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af93c876610139b595b7416c41cc6df9ebba87f0706b7ee1ece6a69ab0bebaa`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fb01a7e673842ded65bdcdcced99c281575743751ca219336ceb9e95b4a0e8`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 123.4 KB (123407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae3717877baa442ae7c73c0af98315cfe57d21554f2647739c792bf44240aa8`  
		Last Modified: Thu, 28 Mar 2024 19:21:45 GMT  
		Size: 990.4 KB (990428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf73c888928175612d13f100f21e51e61f22d752972c4e4c9ca9a412a53f920b`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9be9099f9a93e9d3488286c04ef2fa0350242d4207f50af77a17f89ef7e177`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:0322fdfe59a4b8ee20d7127136f42eefcff450ad57400408c51a88cb7e9914b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf6e6d6ee32aa7b5d034fdd864b17f953c8d03ffbf532b9cf455978c4a87aed`

```dockerfile
```

-	Layers:
	-	`sha256:ab3fad68489df68281f8819ef71a7a4108466ee4b9edc0a5b75db897e14ae32e`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d73a67a0c37803124f85e66364544db0aed3f07ca52ecf082733da70ec9284e1`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 19.4 KB (19370 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:62dab6a9b0b7245477027221202f878ec8ca2b57f0e7b73cd8fd87ddd835c38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4332854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5558373c07611e5d9c5f065de41425c65fcb4edafee9c73f7471e20ecd1c63a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
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
	-	`sha256:f8ad24edb46ae1f03842b15a18bed8c9459caf47c9b44ac9e9f8ceba287a2d99`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 975.4 KB (975434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72add78eac56e24383a18f968c20868c803c6abfde9560e6df8a55ce9ac8420`  
		Last Modified: Thu, 28 Mar 2024 19:28:29 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7415f1d9d4bf360b03d79bc7084a83a370483d24310a700a4dca754c6e3972`  
		Last Modified: Thu, 28 Mar 2024 19:28:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ecba7487095ee7d9a4ab5dc74ce4e434f1a2d8056d87a5a2ddd6b74e82fa3b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32fcbd9dbbf02e688908e774ab684beff7ef28a6afaf60dd34855dd53e199caa`

```dockerfile
```

-	Layers:
	-	`sha256:777960c66626abacd0c8e4e899960921e1a9e3b55adac8dd3c822e7df8945bee`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d43a6b7e3f38d4afafbea91c4b713749a30e42109508da2f9d64a72cd1db3a43`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 19.3 KB (19302 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine3.19`

```console
$ docker pull memcached@sha256:9177d35a8e2b4224b2b99ec2930a8dc58f7c5af74a6b8143ae907fe9b11463d4
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
$ docker pull memcached@sha256:6209860fadd758c1ff8287829c97198233d086836a8b9fbf1d08125ba71666b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b686fb4e394c572a1980b134344b94d4673fcf49dd492838d7ee6a22c4c73466`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4ca62cc3e912d97d5818cdb2c21bfd6ef17fb2a46bb9ff37ef80b46aeb7579`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873fcbe9681f30840a11a64dc6ef9dfef47f40b1181e1c876969a13e35b6f5b4`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 104.2 KB (104205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2a65ada68aba9def3ee64975e1d20608c30fbb31babe05bf0a052fd5b9e631`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 952.1 KB (952136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9ac090217572c7ea3a76702db6866b9c0c35dd85d2a2bad5a50ca438050b67`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b997d515984ace5a566abec5f367a569bf51dcb5c860f5f1868154d8d61ca54`  
		Last Modified: Thu, 28 Mar 2024 18:53:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:a3837912bae62cedd588361c1fd7f24dedff8326ee89d994b188f146b2e45cdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048a973a594205e1bb5d398cc6e6d289c18ca8bd7b73c56d883080501a45af67`

```dockerfile
```

-	Layers:
	-	`sha256:fd986e4f48564cc23fae84c6c205ad8bac1f5f7733c03683ce10edf2580aed7c`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d1c90f2da382eb7f6f0edeab7ce48b9f24941fc542612204b5e38600d91d209`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 19.5 KB (19468 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:46208d1529b365696f517731af2230117072d9b61892276113308a9446932698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4425171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b581ee26004a99ed42270719e1ba6c1cc43728d706d223b58f1ded5911100ccb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bfa7663dcfe59a8997ca6332c380cce69151aeff2a9a10b71d5d655460cc3a`  
		Last Modified: Sat, 16 Mar 2024 15:47:28 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0f8117ff80fc4d046d3bf71fc57dd04a8020db6c8c4e9786b1d94d29bd1cc0`  
		Last Modified: Sat, 16 Mar 2024 15:47:28 GMT  
		Size: 120.9 KB (120902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af942211259cead4688eb0d347be9713995f1ee94d1ba1037b0ba392d4a3cdc6`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 954.9 KB (954910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e9c7aae0c99531c564569b2c18c751c8ccf729706ee0d94bbad57a1f44f0c2`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea48c501ddc68741eb04b337b84674ad57f0b41a67064a0b03ebd3003b573352`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:6dc666e80bf78a2d0c87939b02f96bedfa495d9920a7ebc747196b1cd02e2697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b89445ac664e88d593bab80bee2d0d5655c7e8514df793507272c4d185b5f98`

```dockerfile
```

-	Layers:
	-	`sha256:b6ebaa8df2f60e22d5c7a27d50ba950bb848bc48e2ad39eaafcf18f5841306f4`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:744d3c8bb078a1a54e7eff756816d1210742e1b96aea3127f6dbe2dca46c143e`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 19.3 KB (19320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.19` - linux; 386

```console
$ docker pull memcached@sha256:cb29d2fb5915af23e62234ec3e061ccb9bf0e09ab3146bc5275cb93d06ac2002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4300923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff0463afaa58ff4bd1755643f08e532a20be67f1c75cf31f6f4485c82ebf085`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7101892b4f7a0ec7e893a31b4c4b241666261700594b70af05e5bbde39e1ac`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2a8397306302beb9cd1c51c03f7a33b34efe159dc5423bf0450396a416aa88`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 109.3 KB (109321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6f6638920128a5138269a00784e6e731705c4aa9d114bbbcf0a94fead17efb`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 945.9 KB (945864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d19b89060fd32f477577dfc686f44f32da930716d3e5321a51c36c29b166ece`  
		Last Modified: Thu, 28 Mar 2024 18:53:12 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8ebfbbb8e7bd6745fd67fa4e70d9198ee1a540ce3b792770a1a528feb27510`  
		Last Modified: Thu, 28 Mar 2024 18:53:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:616aed5f6c6e59b28e9b940db41af823662139db453fd3dabfd0a3e4cfe27515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b397ca537b8b98807e225f556a891ee088375459e2b0560dee27496238a6f6bb`

```dockerfile
```

-	Layers:
	-	`sha256:f7c2a6ba891f879d55d2617d901135ce44cc45cb607f46af268d688d06fe6cbe`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:215e98388857b167196047f4301650abb69008e97eb82a06a1a1c1284cd18990`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 19.4 KB (19413 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.19` - linux; ppc64le

```console
$ docker pull memcached@sha256:fb33bde5c5ef29f5ac1d0ead06479dff74c42b27086fe8c54f0649cce4617709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4473831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4ff16a5d7a50717ec61b2a0456c7ce9e733cf60d44539d4fed95ad3f66e754`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af93c876610139b595b7416c41cc6df9ebba87f0706b7ee1ece6a69ab0bebaa`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fb01a7e673842ded65bdcdcced99c281575743751ca219336ceb9e95b4a0e8`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 123.4 KB (123407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae3717877baa442ae7c73c0af98315cfe57d21554f2647739c792bf44240aa8`  
		Last Modified: Thu, 28 Mar 2024 19:21:45 GMT  
		Size: 990.4 KB (990428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf73c888928175612d13f100f21e51e61f22d752972c4e4c9ca9a412a53f920b`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9be9099f9a93e9d3488286c04ef2fa0350242d4207f50af77a17f89ef7e177`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:0322fdfe59a4b8ee20d7127136f42eefcff450ad57400408c51a88cb7e9914b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf6e6d6ee32aa7b5d034fdd864b17f953c8d03ffbf532b9cf455978c4a87aed`

```dockerfile
```

-	Layers:
	-	`sha256:ab3fad68489df68281f8819ef71a7a4108466ee4b9edc0a5b75db897e14ae32e`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d73a67a0c37803124f85e66364544db0aed3f07ca52ecf082733da70ec9284e1`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 19.4 KB (19370 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.19` - linux; s390x

```console
$ docker pull memcached@sha256:62dab6a9b0b7245477027221202f878ec8ca2b57f0e7b73cd8fd87ddd835c38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4332854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5558373c07611e5d9c5f065de41425c65fcb4edafee9c73f7471e20ecd1c63a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
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
	-	`sha256:f8ad24edb46ae1f03842b15a18bed8c9459caf47c9b44ac9e9f8ceba287a2d99`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 975.4 KB (975434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72add78eac56e24383a18f968c20868c803c6abfde9560e6df8a55ce9ac8420`  
		Last Modified: Thu, 28 Mar 2024 19:28:29 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7415f1d9d4bf360b03d79bc7084a83a370483d24310a700a4dca754c6e3972`  
		Last Modified: Thu, 28 Mar 2024 19:28:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:ecba7487095ee7d9a4ab5dc74ce4e434f1a2d8056d87a5a2ddd6b74e82fa3b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32fcbd9dbbf02e688908e774ab684beff7ef28a6afaf60dd34855dd53e199caa`

```dockerfile
```

-	Layers:
	-	`sha256:777960c66626abacd0c8e4e899960921e1a9e3b55adac8dd3c822e7df8945bee`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d43a6b7e3f38d4afafbea91c4b713749a30e42109508da2f9d64a72cd1db3a43`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 19.3 KB (19302 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-bookworm`

```console
$ docker pull memcached@sha256:9eb572b94abad82c04f1329c97e72684931b1dda2cb5c0ee6c4d115f76d6b037
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
$ docker pull memcached@sha256:2967dc980ac80883003061c899102ed6c8749ed50712d4cf592b7c53efd7a498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32872677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7787f9f0d27b97ee6da8b7b2fdf9dec18a1c0fa6c05b0d4a454cc84138bfceb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131f56ef3fe0a1487206d17cc66325f94d97854c231561697099f0162c37a033`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa35112bf68c5c494491a4c7fbbb8ba5e4d9d410ce9150f1b3238414cbc091b0`  
		Last Modified: Wed, 10 Apr 2024 02:57:19 GMT  
		Size: 2.5 MB (2488500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a672c032d4a7b7c0de949d9fe1d4896cc7da42256b16e1daba353de964968b8`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 1.3 MB (1251305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01135bb689569cd15c6a2b8d8e115947652e4d61a01127729ea24513d1f57d2`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48f53906ef45e3138f6a1f1ee8ebd01ca24a3c3a2c15301afe932077984afbb`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:ace7b79050b8d00e7046345e319209248f2ce44b7b3a67968e6662d559b4cebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0612146bf8ed0f19690c2070f49b81b2f59f0df0c0aee6b38606b04c32b3b1bc`

```dockerfile
```

-	Layers:
	-	`sha256:cbbd757e27c72cb57f0f51a89cb3d65360e0afa594c47eff406c9db9d3a27de0`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 2.3 MB (2261161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d398ef36731f34f7e28948dd252f5bd1ec36dbc3a4f7b23dd7fc9d195992db2`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 21.1 KB (21142 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:794b039b86010e20defef81d8fe493212a10d4c4f774d39e7c09aaaf8a9e3ebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30212760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:916c48be9c03801f4162ac2f2e46c0e5d0c8ffa27e110dff6f876cfe88d992ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:bfe2e0ed45dd2920845bd9283b7d13266c82fe9f48ba261b6529c28dc246d3e4 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:60d288182f6883c1ed662f82d32316348aac8ca45c943f1093aed5c0ed01b45c`  
		Last Modified: Wed, 10 Apr 2024 00:54:34 GMT  
		Size: 26.9 MB (26890564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2034ec998bbde42652af813854ab5c0f1dd9c547b6b0c4680f48b2f545ede0ef`  
		Last Modified: Wed, 10 Apr 2024 16:31:49 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d77e350a8c89faec28416a879441cd67ed9d418f318b1426c3961607be04f57`  
		Last Modified: Wed, 10 Apr 2024 16:31:50 GMT  
		Size: 2.1 MB (2089485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3b43e6036c3e47e9bde8e1b23b2e18ae3881bd6963c58d7378f7ea5b298be8`  
		Last Modified: Wed, 10 Apr 2024 16:31:50 GMT  
		Size: 1.2 MB (1231197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e69525c68188c9fb6f58a63eaf9f54f84812c92027f0fd1def2d187df8c8e68`  
		Last Modified: Wed, 10 Apr 2024 16:31:49 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7c08a590703b057ce8910c40bac6339e039354b046cf91903f72c731edbbe2`  
		Last Modified: Wed, 10 Apr 2024 16:31:51 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:29852f9ed352544975a85e04cce00288b41a6e90c67436126f390bb83a3973af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a23719172438c0c0276e696803f232d54be8c0b6efd0c247d70df9a191177ef6`

```dockerfile
```

-	Layers:
	-	`sha256:9a4464980ebe9ed988705320869e004e29ee47a94854bddf2950f9528b4ea70c`  
		Last Modified: Wed, 10 Apr 2024 16:31:50 GMT  
		Size: 2.3 MB (2264449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65343e5170f1bd22aadd1c65fe274b6156e6fd966337aa0b2e81b58234c21b69`  
		Last Modified: Wed, 10 Apr 2024 16:31:49 GMT  
		Size: 21.1 KB (21114 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:7fed5d02aeac33c3df4a133ce97a03c71d8a3f2713f2ff5c4788cf9096f02162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32758363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2fefeb31b86fb36b67e5a920329724ed9519c1ffeca7fa3cc86b26b876237c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc8e58118ea2b587de344fc120829e4086cf15fa1bfa009c58f17ba08203688`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc85ab0a8a03257329849592bd06635db2c84ae701f76df4c27d15306ea0737`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 2.3 MB (2346212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ebd2971429766b668a79b73696f698513334995b9470c9f9f21da0ca81dfdd`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 1.2 MB (1248481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864c041bfe7d835cabb73fb214a8a4b7a7931b18ba532835f043f470dcd3c81e`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c33e09275e854d41d4c12ccef30c6e4e9997e08df5cbcfe520940eb1edb7884`  
		Last Modified: Wed, 10 Apr 2024 16:40:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:57f39faf16f4225d453c30ea64aeb39b90c82cda39549ab0136192c33fc6fcdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a812ba1f091b4c27268db9e91ddb70c1e855cdc46b49936787eee43df1fa371e`

```dockerfile
```

-	Layers:
	-	`sha256:c70324d70390ac933db840ed30afe02f56c58c7eaabbd1ab134e1fc87513fcff`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 2.3 MB (2261390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0535f7d789eaa3f63c11e92d1af4881c5a73f879e664b3109c1f470ad28dd71b`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 21.0 KB (20993 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:34f5ef517d7f54cc5f88ce0834b5a2d2285b7e453e648114404c375ed5bb5657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33893284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b6a893f1366a34486ca1a3011cdde9de38d5b7635c1227cf0faddfe53bb312`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:d160efeeb02e2200784dd8312a13a11d9d791581efc7756ed999f76c79445b54 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8a3830119a16769024de35d2dfa3d32147da5ea747ec336166bdca1049655803`  
		Last Modified: Wed, 10 Apr 2024 01:02:04 GMT  
		Size: 30.1 MB (30146515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4020925217af165e208be472fc2fcd518c37967f238cbcba0dbec12d20b685`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45dff0ba396ced9bb0bb69ffd5456f2a5cc783b7908bc10f4c194aa328ec3036`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 2.5 MB (2492670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9498280a2172ecdd190d1e4d3e001d55b64bbec93f4eccb039870ebbedd40f64`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 1.3 MB (1252590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf4eb265fb60a5b2351156ea6f2eccf92d961585ba20be18d7e6d3294511507`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a379f21df665e12ab146aebcf0a1cc7e55cbd7a9bbc4d17a209c7a5ba03eeb1`  
		Last Modified: Wed, 10 Apr 2024 01:55:17 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:e3e28c19c9f28d8dfee9784913c92b2a01df26c25a575a77a4f83c23281d8cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e29f55fbf81fc47ec484ab81a55a69d9c1eb3874c9eb08b813638198b69361e`

```dockerfile
```

-	Layers:
	-	`sha256:be647ca90ccc7f88e1eb3a88b1acd85aaac94d593fedbe2cebeee872c8a3b26b`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 2.3 MB (2258259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f2ac7f006c3cff208ffd83fa9513a6b12cf39a1ec192a9f01a088d0240d858b`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 21.1 KB (21087 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:fc8892b557a9bdb7b41273e3403bc2fdb3d04f99fb56a3874e9081d8dfa128d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32306668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a48487cefaf60f8ad4d3a059b0db4796bee3adbf408393dcc4c49da664f723`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 01:06:19 GMT
ADD file:c03c59e261bb08f39e6a97df2fd4b82f1e11b49a62d1859a8f8efac680b80a88 in / 
# Tue, 12 Mar 2024 01:06:23 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aad79459a0f767fcded51c9547150a1cfd96638972389ab8621b5f3eb4a9c280`  
		Last Modified: Tue, 12 Mar 2024 01:17:09 GMT  
		Size: 29.1 MB (29119205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460befff49885c738329c53c06bca553e2869317c73b0b5f76661a7053f578ad`  
		Last Modified: Tue, 09 Apr 2024 15:25:07 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6dc8cf2380155c1bacde757237b8551c77167e46ac5393332be9deb2b8dbc5`  
		Last Modified: Tue, 09 Apr 2024 15:25:07 GMT  
		Size: 1.9 MB (1937657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66db33dc07294fd7ecc848862384efa6b829c96c8939643a7098e35bbbe81d8f`  
		Last Modified: Tue, 09 Apr 2024 15:25:07 GMT  
		Size: 1.2 MB (1248284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1650df259f3af60ff6184e164ac094f261bffea30679d803c7cff2759e001699`  
		Last Modified: Tue, 09 Apr 2024 15:25:07 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51c337d2a6d822be89d42ae3e0ae8472dbd1673e648f8cdf1c769309105aaca`  
		Last Modified: Tue, 09 Apr 2024 15:25:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:831ec04c94a8b50c1aff4f18c97c8cae1d537c32821a0b8aeca9b0a1aecacae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7033955a79b1242de9912088e5d0f703e2133fce52308636758ba5ce2059d38c`

```dockerfile
```

-	Layers:
	-	`sha256:abd2f28a59a5e89ae224244ff2945a51f564194853e6abaaa8f5648413960325`  
		Last Modified: Tue, 09 Apr 2024 15:25:07 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:dc36455fb79f84d62ac6d34100afc15f0a238192dfa3224e93f753cd67d74798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37135966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:430a51910c252bd83b91329bef7a7f1a2344a5bc6b42075d419bb0facc468286`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:30:19 GMT
ADD file:9273ef56d086dbc93b46b7e8ae424eb04096fb00c693dd6cda1f48346290d4d5 in / 
# Tue, 12 Mar 2024 00:30:24 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c28cd0e276dcdeb4d44f5cc5bb958610750ff902a081b668e3863c2f38eef054`  
		Last Modified: Tue, 12 Mar 2024 00:38:06 GMT  
		Size: 33.1 MB (33119023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708b42bb3654f69ef8bfee96e8cd256f668ec36c0c79dffa3833c5a717f9eb5f`  
		Last Modified: Wed, 20 Mar 2024 21:57:50 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66c4756024ccda97c6fbe022e48d010bf3335191ef2516ace6ee30de5e87389`  
		Last Modified: Wed, 20 Mar 2024 21:57:51 GMT  
		Size: 2.7 MB (2698368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ea5604f0c8a697cb056d47640ff8d8852849f35d9a26e62b42036629bcaf9c`  
		Last Modified: Tue, 09 Apr 2024 05:05:54 GMT  
		Size: 1.3 MB (1317055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810d9546da33f92c2106ed1bbfc26223b8bef8f8e2be48b862a0270380818526`  
		Last Modified: Tue, 09 Apr 2024 05:05:54 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c78ea7da271614754f4fdc7e7d86c64da966e871cce4bab839266e27bd62912`  
		Last Modified: Tue, 09 Apr 2024 05:05:54 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:a78edf1158eed48cbec064a641fcac3c873e1b1fee26b1d8407a0269870baa23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2287859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618f6dcb01dc21ed0cc62f7efaeabc4c883f32d56e5f51a66cba2e87b31ed783`

```dockerfile
```

-	Layers:
	-	`sha256:13692af6f7d1860a31d9a8610f75d0d12eaa87131aef9b5615a57c5aaad34643`  
		Last Modified: Tue, 09 Apr 2024 05:05:54 GMT  
		Size: 2.3 MB (2266816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eae96d76b66c8c2450ce3e926ee185c9043ceff0f51f91e18694e094fd6d91af`  
		Last Modified: Tue, 09 Apr 2024 05:05:53 GMT  
		Size: 21.0 KB (21043 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:3af0cb7bc651113fdea970716a6f0a534823c322990bacbde20cc166648bb952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30873795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d9bcea2e734469166d18b5a96ac76cdcd310b4c95140b542777073e6158051`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:54:02 GMT
ADD file:80ab985d4871ca6a72156bedfe1038e6b1a89591fc2fd86c4ef778d293223aff in / 
# Tue, 12 Mar 2024 00:54:03 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9cada496cd2b8a88571bf23d513e7fce34888d13321fcf23c6613bffe4c37297`  
		Last Modified: Tue, 12 Mar 2024 01:21:14 GMT  
		Size: 27.5 MB (27488684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c430faffa085700d40355ac1aea08d429376e112bef3b9c00780b1ede56859c2`  
		Last Modified: Wed, 20 Mar 2024 22:17:08 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf1db148a80e9f25b06fe946c697ba8fa83bc46c13515904d4ceceaeb2a4eeb`  
		Last Modified: Wed, 20 Mar 2024 22:17:12 GMT  
		Size: 2.2 MB (2152657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400f8ed9afb04b498a060de1a774c9272cec70272754126b664985cd98414623`  
		Last Modified: Tue, 09 Apr 2024 14:59:31 GMT  
		Size: 1.2 MB (1230937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ca205adef44fe63941fcd64a5ea1c792c297534b81b7c23838857081d464f6`  
		Last Modified: Tue, 09 Apr 2024 14:59:31 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b24165a664a9007bca136f51d3c60c906ddf8626c9ab9403969454d4c0c47ac`  
		Last Modified: Tue, 09 Apr 2024 14:59:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:e8a1f799f3a7047f3ea6db5f3bebbdcf84726e7a0b3b45157df167d441495d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee48fbaae81e8e950ac399f89ee0eb0f7ad3e7da77d66ce435def816b3814ca`

```dockerfile
```

-	Layers:
	-	`sha256:bda232575879bf9ee6d85b64ea286f2469deccdb87ecc3991ba0fd95a508d8fa`  
		Last Modified: Tue, 09 Apr 2024 14:59:30 GMT  
		Size: 2.3 MB (2262266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13f17df99c3a427fb2b41aa30a6b4f13b2de20e1567da419bc3c6f2febb08832`  
		Last Modified: Tue, 09 Apr 2024 14:59:31 GMT  
		Size: 20.9 KB (20938 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.26`

```console
$ docker pull memcached@sha256:9eb572b94abad82c04f1329c97e72684931b1dda2cb5c0ee6c4d115f76d6b037
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

### `memcached:1.6.26` - linux; amd64

```console
$ docker pull memcached@sha256:2967dc980ac80883003061c899102ed6c8749ed50712d4cf592b7c53efd7a498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32872677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7787f9f0d27b97ee6da8b7b2fdf9dec18a1c0fa6c05b0d4a454cc84138bfceb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131f56ef3fe0a1487206d17cc66325f94d97854c231561697099f0162c37a033`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa35112bf68c5c494491a4c7fbbb8ba5e4d9d410ce9150f1b3238414cbc091b0`  
		Last Modified: Wed, 10 Apr 2024 02:57:19 GMT  
		Size: 2.5 MB (2488500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a672c032d4a7b7c0de949d9fe1d4896cc7da42256b16e1daba353de964968b8`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 1.3 MB (1251305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01135bb689569cd15c6a2b8d8e115947652e4d61a01127729ea24513d1f57d2`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48f53906ef45e3138f6a1f1ee8ebd01ca24a3c3a2c15301afe932077984afbb`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26` - unknown; unknown

```console
$ docker pull memcached@sha256:ace7b79050b8d00e7046345e319209248f2ce44b7b3a67968e6662d559b4cebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0612146bf8ed0f19690c2070f49b81b2f59f0df0c0aee6b38606b04c32b3b1bc`

```dockerfile
```

-	Layers:
	-	`sha256:cbbd757e27c72cb57f0f51a89cb3d65360e0afa594c47eff406c9db9d3a27de0`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 2.3 MB (2261161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d398ef36731f34f7e28948dd252f5bd1ec36dbc3a4f7b23dd7fc9d195992db2`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 21.1 KB (21142 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.26` - linux; arm variant v5

```console
$ docker pull memcached@sha256:794b039b86010e20defef81d8fe493212a10d4c4f774d39e7c09aaaf8a9e3ebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30212760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:916c48be9c03801f4162ac2f2e46c0e5d0c8ffa27e110dff6f876cfe88d992ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:bfe2e0ed45dd2920845bd9283b7d13266c82fe9f48ba261b6529c28dc246d3e4 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:60d288182f6883c1ed662f82d32316348aac8ca45c943f1093aed5c0ed01b45c`  
		Last Modified: Wed, 10 Apr 2024 00:54:34 GMT  
		Size: 26.9 MB (26890564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2034ec998bbde42652af813854ab5c0f1dd9c547b6b0c4680f48b2f545ede0ef`  
		Last Modified: Wed, 10 Apr 2024 16:31:49 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d77e350a8c89faec28416a879441cd67ed9d418f318b1426c3961607be04f57`  
		Last Modified: Wed, 10 Apr 2024 16:31:50 GMT  
		Size: 2.1 MB (2089485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3b43e6036c3e47e9bde8e1b23b2e18ae3881bd6963c58d7378f7ea5b298be8`  
		Last Modified: Wed, 10 Apr 2024 16:31:50 GMT  
		Size: 1.2 MB (1231197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e69525c68188c9fb6f58a63eaf9f54f84812c92027f0fd1def2d187df8c8e68`  
		Last Modified: Wed, 10 Apr 2024 16:31:49 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7c08a590703b057ce8910c40bac6339e039354b046cf91903f72c731edbbe2`  
		Last Modified: Wed, 10 Apr 2024 16:31:51 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26` - unknown; unknown

```console
$ docker pull memcached@sha256:29852f9ed352544975a85e04cce00288b41a6e90c67436126f390bb83a3973af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a23719172438c0c0276e696803f232d54be8c0b6efd0c247d70df9a191177ef6`

```dockerfile
```

-	Layers:
	-	`sha256:9a4464980ebe9ed988705320869e004e29ee47a94854bddf2950f9528b4ea70c`  
		Last Modified: Wed, 10 Apr 2024 16:31:50 GMT  
		Size: 2.3 MB (2264449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65343e5170f1bd22aadd1c65fe274b6156e6fd966337aa0b2e81b58234c21b69`  
		Last Modified: Wed, 10 Apr 2024 16:31:49 GMT  
		Size: 21.1 KB (21114 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.26` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:7fed5d02aeac33c3df4a133ce97a03c71d8a3f2713f2ff5c4788cf9096f02162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32758363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2fefeb31b86fb36b67e5a920329724ed9519c1ffeca7fa3cc86b26b876237c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc8e58118ea2b587de344fc120829e4086cf15fa1bfa009c58f17ba08203688`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc85ab0a8a03257329849592bd06635db2c84ae701f76df4c27d15306ea0737`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 2.3 MB (2346212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ebd2971429766b668a79b73696f698513334995b9470c9f9f21da0ca81dfdd`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 1.2 MB (1248481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864c041bfe7d835cabb73fb214a8a4b7a7931b18ba532835f043f470dcd3c81e`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c33e09275e854d41d4c12ccef30c6e4e9997e08df5cbcfe520940eb1edb7884`  
		Last Modified: Wed, 10 Apr 2024 16:40:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26` - unknown; unknown

```console
$ docker pull memcached@sha256:57f39faf16f4225d453c30ea64aeb39b90c82cda39549ab0136192c33fc6fcdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a812ba1f091b4c27268db9e91ddb70c1e855cdc46b49936787eee43df1fa371e`

```dockerfile
```

-	Layers:
	-	`sha256:c70324d70390ac933db840ed30afe02f56c58c7eaabbd1ab134e1fc87513fcff`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 2.3 MB (2261390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0535f7d789eaa3f63c11e92d1af4881c5a73f879e664b3109c1f470ad28dd71b`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 21.0 KB (20993 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.26` - linux; 386

```console
$ docker pull memcached@sha256:34f5ef517d7f54cc5f88ce0834b5a2d2285b7e453e648114404c375ed5bb5657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33893284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b6a893f1366a34486ca1a3011cdde9de38d5b7635c1227cf0faddfe53bb312`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:d160efeeb02e2200784dd8312a13a11d9d791581efc7756ed999f76c79445b54 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8a3830119a16769024de35d2dfa3d32147da5ea747ec336166bdca1049655803`  
		Last Modified: Wed, 10 Apr 2024 01:02:04 GMT  
		Size: 30.1 MB (30146515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4020925217af165e208be472fc2fcd518c37967f238cbcba0dbec12d20b685`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45dff0ba396ced9bb0bb69ffd5456f2a5cc783b7908bc10f4c194aa328ec3036`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 2.5 MB (2492670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9498280a2172ecdd190d1e4d3e001d55b64bbec93f4eccb039870ebbedd40f64`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 1.3 MB (1252590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf4eb265fb60a5b2351156ea6f2eccf92d961585ba20be18d7e6d3294511507`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a379f21df665e12ab146aebcf0a1cc7e55cbd7a9bbc4d17a209c7a5ba03eeb1`  
		Last Modified: Wed, 10 Apr 2024 01:55:17 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26` - unknown; unknown

```console
$ docker pull memcached@sha256:e3e28c19c9f28d8dfee9784913c92b2a01df26c25a575a77a4f83c23281d8cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e29f55fbf81fc47ec484ab81a55a69d9c1eb3874c9eb08b813638198b69361e`

```dockerfile
```

-	Layers:
	-	`sha256:be647ca90ccc7f88e1eb3a88b1acd85aaac94d593fedbe2cebeee872c8a3b26b`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 2.3 MB (2258259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f2ac7f006c3cff208ffd83fa9513a6b12cf39a1ec192a9f01a088d0240d858b`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 21.1 KB (21087 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.26` - linux; mips64le

```console
$ docker pull memcached@sha256:fc8892b557a9bdb7b41273e3403bc2fdb3d04f99fb56a3874e9081d8dfa128d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32306668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a48487cefaf60f8ad4d3a059b0db4796bee3adbf408393dcc4c49da664f723`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 01:06:19 GMT
ADD file:c03c59e261bb08f39e6a97df2fd4b82f1e11b49a62d1859a8f8efac680b80a88 in / 
# Tue, 12 Mar 2024 01:06:23 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aad79459a0f767fcded51c9547150a1cfd96638972389ab8621b5f3eb4a9c280`  
		Last Modified: Tue, 12 Mar 2024 01:17:09 GMT  
		Size: 29.1 MB (29119205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460befff49885c738329c53c06bca553e2869317c73b0b5f76661a7053f578ad`  
		Last Modified: Tue, 09 Apr 2024 15:25:07 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6dc8cf2380155c1bacde757237b8551c77167e46ac5393332be9deb2b8dbc5`  
		Last Modified: Tue, 09 Apr 2024 15:25:07 GMT  
		Size: 1.9 MB (1937657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66db33dc07294fd7ecc848862384efa6b829c96c8939643a7098e35bbbe81d8f`  
		Last Modified: Tue, 09 Apr 2024 15:25:07 GMT  
		Size: 1.2 MB (1248284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1650df259f3af60ff6184e164ac094f261bffea30679d803c7cff2759e001699`  
		Last Modified: Tue, 09 Apr 2024 15:25:07 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51c337d2a6d822be89d42ae3e0ae8472dbd1673e648f8cdf1c769309105aaca`  
		Last Modified: Tue, 09 Apr 2024 15:25:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26` - unknown; unknown

```console
$ docker pull memcached@sha256:831ec04c94a8b50c1aff4f18c97c8cae1d537c32821a0b8aeca9b0a1aecacae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7033955a79b1242de9912088e5d0f703e2133fce52308636758ba5ce2059d38c`

```dockerfile
```

-	Layers:
	-	`sha256:abd2f28a59a5e89ae224244ff2945a51f564194853e6abaaa8f5648413960325`  
		Last Modified: Tue, 09 Apr 2024 15:25:07 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.26` - linux; ppc64le

```console
$ docker pull memcached@sha256:dc36455fb79f84d62ac6d34100afc15f0a238192dfa3224e93f753cd67d74798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37135966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:430a51910c252bd83b91329bef7a7f1a2344a5bc6b42075d419bb0facc468286`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:30:19 GMT
ADD file:9273ef56d086dbc93b46b7e8ae424eb04096fb00c693dd6cda1f48346290d4d5 in / 
# Tue, 12 Mar 2024 00:30:24 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c28cd0e276dcdeb4d44f5cc5bb958610750ff902a081b668e3863c2f38eef054`  
		Last Modified: Tue, 12 Mar 2024 00:38:06 GMT  
		Size: 33.1 MB (33119023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708b42bb3654f69ef8bfee96e8cd256f668ec36c0c79dffa3833c5a717f9eb5f`  
		Last Modified: Wed, 20 Mar 2024 21:57:50 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66c4756024ccda97c6fbe022e48d010bf3335191ef2516ace6ee30de5e87389`  
		Last Modified: Wed, 20 Mar 2024 21:57:51 GMT  
		Size: 2.7 MB (2698368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ea5604f0c8a697cb056d47640ff8d8852849f35d9a26e62b42036629bcaf9c`  
		Last Modified: Tue, 09 Apr 2024 05:05:54 GMT  
		Size: 1.3 MB (1317055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810d9546da33f92c2106ed1bbfc26223b8bef8f8e2be48b862a0270380818526`  
		Last Modified: Tue, 09 Apr 2024 05:05:54 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c78ea7da271614754f4fdc7e7d86c64da966e871cce4bab839266e27bd62912`  
		Last Modified: Tue, 09 Apr 2024 05:05:54 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26` - unknown; unknown

```console
$ docker pull memcached@sha256:a78edf1158eed48cbec064a641fcac3c873e1b1fee26b1d8407a0269870baa23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2287859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618f6dcb01dc21ed0cc62f7efaeabc4c883f32d56e5f51a66cba2e87b31ed783`

```dockerfile
```

-	Layers:
	-	`sha256:13692af6f7d1860a31d9a8610f75d0d12eaa87131aef9b5615a57c5aaad34643`  
		Last Modified: Tue, 09 Apr 2024 05:05:54 GMT  
		Size: 2.3 MB (2266816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eae96d76b66c8c2450ce3e926ee185c9043ceff0f51f91e18694e094fd6d91af`  
		Last Modified: Tue, 09 Apr 2024 05:05:53 GMT  
		Size: 21.0 KB (21043 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.26` - linux; s390x

```console
$ docker pull memcached@sha256:3af0cb7bc651113fdea970716a6f0a534823c322990bacbde20cc166648bb952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30873795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d9bcea2e734469166d18b5a96ac76cdcd310b4c95140b542777073e6158051`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:54:02 GMT
ADD file:80ab985d4871ca6a72156bedfe1038e6b1a89591fc2fd86c4ef778d293223aff in / 
# Tue, 12 Mar 2024 00:54:03 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9cada496cd2b8a88571bf23d513e7fce34888d13321fcf23c6613bffe4c37297`  
		Last Modified: Tue, 12 Mar 2024 01:21:14 GMT  
		Size: 27.5 MB (27488684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c430faffa085700d40355ac1aea08d429376e112bef3b9c00780b1ede56859c2`  
		Last Modified: Wed, 20 Mar 2024 22:17:08 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf1db148a80e9f25b06fe946c697ba8fa83bc46c13515904d4ceceaeb2a4eeb`  
		Last Modified: Wed, 20 Mar 2024 22:17:12 GMT  
		Size: 2.2 MB (2152657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400f8ed9afb04b498a060de1a774c9272cec70272754126b664985cd98414623`  
		Last Modified: Tue, 09 Apr 2024 14:59:31 GMT  
		Size: 1.2 MB (1230937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ca205adef44fe63941fcd64a5ea1c792c297534b81b7c23838857081d464f6`  
		Last Modified: Tue, 09 Apr 2024 14:59:31 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b24165a664a9007bca136f51d3c60c906ddf8626c9ab9403969454d4c0c47ac`  
		Last Modified: Tue, 09 Apr 2024 14:59:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26` - unknown; unknown

```console
$ docker pull memcached@sha256:e8a1f799f3a7047f3ea6db5f3bebbdcf84726e7a0b3b45157df167d441495d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee48fbaae81e8e950ac399f89ee0eb0f7ad3e7da77d66ce435def816b3814ca`

```dockerfile
```

-	Layers:
	-	`sha256:bda232575879bf9ee6d85b64ea286f2469deccdb87ecc3991ba0fd95a508d8fa`  
		Last Modified: Tue, 09 Apr 2024 14:59:30 GMT  
		Size: 2.3 MB (2262266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13f17df99c3a427fb2b41aa30a6b4f13b2de20e1567da419bc3c6f2febb08832`  
		Last Modified: Tue, 09 Apr 2024 14:59:31 GMT  
		Size: 20.9 KB (20938 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.26-alpine`

```console
$ docker pull memcached@sha256:9177d35a8e2b4224b2b99ec2930a8dc58f7c5af74a6b8143ae907fe9b11463d4
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

### `memcached:1.6.26-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:6209860fadd758c1ff8287829c97198233d086836a8b9fbf1d08125ba71666b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b686fb4e394c572a1980b134344b94d4673fcf49dd492838d7ee6a22c4c73466`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4ca62cc3e912d97d5818cdb2c21bfd6ef17fb2a46bb9ff37ef80b46aeb7579`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873fcbe9681f30840a11a64dc6ef9dfef47f40b1181e1c876969a13e35b6f5b4`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 104.2 KB (104205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2a65ada68aba9def3ee64975e1d20608c30fbb31babe05bf0a052fd5b9e631`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 952.1 KB (952136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9ac090217572c7ea3a76702db6866b9c0c35dd85d2a2bad5a50ca438050b67`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b997d515984ace5a566abec5f367a569bf51dcb5c860f5f1868154d8d61ca54`  
		Last Modified: Thu, 28 Mar 2024 18:53:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:a3837912bae62cedd588361c1fd7f24dedff8326ee89d994b188f146b2e45cdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048a973a594205e1bb5d398cc6e6d289c18ca8bd7b73c56d883080501a45af67`

```dockerfile
```

-	Layers:
	-	`sha256:fd986e4f48564cc23fae84c6c205ad8bac1f5f7733c03683ce10edf2580aed7c`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d1c90f2da382eb7f6f0edeab7ce48b9f24941fc542612204b5e38600d91d209`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 19.5 KB (19468 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.26-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:46208d1529b365696f517731af2230117072d9b61892276113308a9446932698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4425171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b581ee26004a99ed42270719e1ba6c1cc43728d706d223b58f1ded5911100ccb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bfa7663dcfe59a8997ca6332c380cce69151aeff2a9a10b71d5d655460cc3a`  
		Last Modified: Sat, 16 Mar 2024 15:47:28 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0f8117ff80fc4d046d3bf71fc57dd04a8020db6c8c4e9786b1d94d29bd1cc0`  
		Last Modified: Sat, 16 Mar 2024 15:47:28 GMT  
		Size: 120.9 KB (120902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af942211259cead4688eb0d347be9713995f1ee94d1ba1037b0ba392d4a3cdc6`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 954.9 KB (954910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e9c7aae0c99531c564569b2c18c751c8ccf729706ee0d94bbad57a1f44f0c2`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea48c501ddc68741eb04b337b84674ad57f0b41a67064a0b03ebd3003b573352`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:6dc666e80bf78a2d0c87939b02f96bedfa495d9920a7ebc747196b1cd02e2697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b89445ac664e88d593bab80bee2d0d5655c7e8514df793507272c4d185b5f98`

```dockerfile
```

-	Layers:
	-	`sha256:b6ebaa8df2f60e22d5c7a27d50ba950bb848bc48e2ad39eaafcf18f5841306f4`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:744d3c8bb078a1a54e7eff756816d1210742e1b96aea3127f6dbe2dca46c143e`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 19.3 KB (19320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.26-alpine` - linux; 386

```console
$ docker pull memcached@sha256:cb29d2fb5915af23e62234ec3e061ccb9bf0e09ab3146bc5275cb93d06ac2002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4300923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff0463afaa58ff4bd1755643f08e532a20be67f1c75cf31f6f4485c82ebf085`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7101892b4f7a0ec7e893a31b4c4b241666261700594b70af05e5bbde39e1ac`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2a8397306302beb9cd1c51c03f7a33b34efe159dc5423bf0450396a416aa88`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 109.3 KB (109321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6f6638920128a5138269a00784e6e731705c4aa9d114bbbcf0a94fead17efb`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 945.9 KB (945864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d19b89060fd32f477577dfc686f44f32da930716d3e5321a51c36c29b166ece`  
		Last Modified: Thu, 28 Mar 2024 18:53:12 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8ebfbbb8e7bd6745fd67fa4e70d9198ee1a540ce3b792770a1a528feb27510`  
		Last Modified: Thu, 28 Mar 2024 18:53:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:616aed5f6c6e59b28e9b940db41af823662139db453fd3dabfd0a3e4cfe27515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b397ca537b8b98807e225f556a891ee088375459e2b0560dee27496238a6f6bb`

```dockerfile
```

-	Layers:
	-	`sha256:f7c2a6ba891f879d55d2617d901135ce44cc45cb607f46af268d688d06fe6cbe`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:215e98388857b167196047f4301650abb69008e97eb82a06a1a1c1284cd18990`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 19.4 KB (19413 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.26-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:fb33bde5c5ef29f5ac1d0ead06479dff74c42b27086fe8c54f0649cce4617709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4473831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4ff16a5d7a50717ec61b2a0456c7ce9e733cf60d44539d4fed95ad3f66e754`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af93c876610139b595b7416c41cc6df9ebba87f0706b7ee1ece6a69ab0bebaa`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fb01a7e673842ded65bdcdcced99c281575743751ca219336ceb9e95b4a0e8`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 123.4 KB (123407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae3717877baa442ae7c73c0af98315cfe57d21554f2647739c792bf44240aa8`  
		Last Modified: Thu, 28 Mar 2024 19:21:45 GMT  
		Size: 990.4 KB (990428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf73c888928175612d13f100f21e51e61f22d752972c4e4c9ca9a412a53f920b`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9be9099f9a93e9d3488286c04ef2fa0350242d4207f50af77a17f89ef7e177`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:0322fdfe59a4b8ee20d7127136f42eefcff450ad57400408c51a88cb7e9914b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf6e6d6ee32aa7b5d034fdd864b17f953c8d03ffbf532b9cf455978c4a87aed`

```dockerfile
```

-	Layers:
	-	`sha256:ab3fad68489df68281f8819ef71a7a4108466ee4b9edc0a5b75db897e14ae32e`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d73a67a0c37803124f85e66364544db0aed3f07ca52ecf082733da70ec9284e1`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 19.4 KB (19370 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.26-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:62dab6a9b0b7245477027221202f878ec8ca2b57f0e7b73cd8fd87ddd835c38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4332854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5558373c07611e5d9c5f065de41425c65fcb4edafee9c73f7471e20ecd1c63a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
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
	-	`sha256:f8ad24edb46ae1f03842b15a18bed8c9459caf47c9b44ac9e9f8ceba287a2d99`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 975.4 KB (975434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72add78eac56e24383a18f968c20868c803c6abfde9560e6df8a55ce9ac8420`  
		Last Modified: Thu, 28 Mar 2024 19:28:29 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7415f1d9d4bf360b03d79bc7084a83a370483d24310a700a4dca754c6e3972`  
		Last Modified: Thu, 28 Mar 2024 19:28:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ecba7487095ee7d9a4ab5dc74ce4e434f1a2d8056d87a5a2ddd6b74e82fa3b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32fcbd9dbbf02e688908e774ab684beff7ef28a6afaf60dd34855dd53e199caa`

```dockerfile
```

-	Layers:
	-	`sha256:777960c66626abacd0c8e4e899960921e1a9e3b55adac8dd3c822e7df8945bee`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d43a6b7e3f38d4afafbea91c4b713749a30e42109508da2f9d64a72cd1db3a43`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 19.3 KB (19302 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.26-alpine3.19`

```console
$ docker pull memcached@sha256:9177d35a8e2b4224b2b99ec2930a8dc58f7c5af74a6b8143ae907fe9b11463d4
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

### `memcached:1.6.26-alpine3.19` - linux; amd64

```console
$ docker pull memcached@sha256:6209860fadd758c1ff8287829c97198233d086836a8b9fbf1d08125ba71666b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b686fb4e394c572a1980b134344b94d4673fcf49dd492838d7ee6a22c4c73466`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4ca62cc3e912d97d5818cdb2c21bfd6ef17fb2a46bb9ff37ef80b46aeb7579`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873fcbe9681f30840a11a64dc6ef9dfef47f40b1181e1c876969a13e35b6f5b4`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 104.2 KB (104205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2a65ada68aba9def3ee64975e1d20608c30fbb31babe05bf0a052fd5b9e631`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 952.1 KB (952136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9ac090217572c7ea3a76702db6866b9c0c35dd85d2a2bad5a50ca438050b67`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b997d515984ace5a566abec5f367a569bf51dcb5c860f5f1868154d8d61ca54`  
		Last Modified: Thu, 28 Mar 2024 18:53:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:a3837912bae62cedd588361c1fd7f24dedff8326ee89d994b188f146b2e45cdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048a973a594205e1bb5d398cc6e6d289c18ca8bd7b73c56d883080501a45af67`

```dockerfile
```

-	Layers:
	-	`sha256:fd986e4f48564cc23fae84c6c205ad8bac1f5f7733c03683ce10edf2580aed7c`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d1c90f2da382eb7f6f0edeab7ce48b9f24941fc542612204b5e38600d91d209`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 19.5 KB (19468 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.26-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:46208d1529b365696f517731af2230117072d9b61892276113308a9446932698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4425171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b581ee26004a99ed42270719e1ba6c1cc43728d706d223b58f1ded5911100ccb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bfa7663dcfe59a8997ca6332c380cce69151aeff2a9a10b71d5d655460cc3a`  
		Last Modified: Sat, 16 Mar 2024 15:47:28 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0f8117ff80fc4d046d3bf71fc57dd04a8020db6c8c4e9786b1d94d29bd1cc0`  
		Last Modified: Sat, 16 Mar 2024 15:47:28 GMT  
		Size: 120.9 KB (120902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af942211259cead4688eb0d347be9713995f1ee94d1ba1037b0ba392d4a3cdc6`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 954.9 KB (954910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e9c7aae0c99531c564569b2c18c751c8ccf729706ee0d94bbad57a1f44f0c2`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea48c501ddc68741eb04b337b84674ad57f0b41a67064a0b03ebd3003b573352`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:6dc666e80bf78a2d0c87939b02f96bedfa495d9920a7ebc747196b1cd02e2697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b89445ac664e88d593bab80bee2d0d5655c7e8514df793507272c4d185b5f98`

```dockerfile
```

-	Layers:
	-	`sha256:b6ebaa8df2f60e22d5c7a27d50ba950bb848bc48e2ad39eaafcf18f5841306f4`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:744d3c8bb078a1a54e7eff756816d1210742e1b96aea3127f6dbe2dca46c143e`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 19.3 KB (19320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.26-alpine3.19` - linux; 386

```console
$ docker pull memcached@sha256:cb29d2fb5915af23e62234ec3e061ccb9bf0e09ab3146bc5275cb93d06ac2002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4300923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff0463afaa58ff4bd1755643f08e532a20be67f1c75cf31f6f4485c82ebf085`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7101892b4f7a0ec7e893a31b4c4b241666261700594b70af05e5bbde39e1ac`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2a8397306302beb9cd1c51c03f7a33b34efe159dc5423bf0450396a416aa88`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 109.3 KB (109321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6f6638920128a5138269a00784e6e731705c4aa9d114bbbcf0a94fead17efb`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 945.9 KB (945864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d19b89060fd32f477577dfc686f44f32da930716d3e5321a51c36c29b166ece`  
		Last Modified: Thu, 28 Mar 2024 18:53:12 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8ebfbbb8e7bd6745fd67fa4e70d9198ee1a540ce3b792770a1a528feb27510`  
		Last Modified: Thu, 28 Mar 2024 18:53:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:616aed5f6c6e59b28e9b940db41af823662139db453fd3dabfd0a3e4cfe27515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b397ca537b8b98807e225f556a891ee088375459e2b0560dee27496238a6f6bb`

```dockerfile
```

-	Layers:
	-	`sha256:f7c2a6ba891f879d55d2617d901135ce44cc45cb607f46af268d688d06fe6cbe`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:215e98388857b167196047f4301650abb69008e97eb82a06a1a1c1284cd18990`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 19.4 KB (19413 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.26-alpine3.19` - linux; ppc64le

```console
$ docker pull memcached@sha256:fb33bde5c5ef29f5ac1d0ead06479dff74c42b27086fe8c54f0649cce4617709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4473831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4ff16a5d7a50717ec61b2a0456c7ce9e733cf60d44539d4fed95ad3f66e754`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af93c876610139b595b7416c41cc6df9ebba87f0706b7ee1ece6a69ab0bebaa`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fb01a7e673842ded65bdcdcced99c281575743751ca219336ceb9e95b4a0e8`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 123.4 KB (123407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae3717877baa442ae7c73c0af98315cfe57d21554f2647739c792bf44240aa8`  
		Last Modified: Thu, 28 Mar 2024 19:21:45 GMT  
		Size: 990.4 KB (990428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf73c888928175612d13f100f21e51e61f22d752972c4e4c9ca9a412a53f920b`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9be9099f9a93e9d3488286c04ef2fa0350242d4207f50af77a17f89ef7e177`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:0322fdfe59a4b8ee20d7127136f42eefcff450ad57400408c51a88cb7e9914b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf6e6d6ee32aa7b5d034fdd864b17f953c8d03ffbf532b9cf455978c4a87aed`

```dockerfile
```

-	Layers:
	-	`sha256:ab3fad68489df68281f8819ef71a7a4108466ee4b9edc0a5b75db897e14ae32e`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d73a67a0c37803124f85e66364544db0aed3f07ca52ecf082733da70ec9284e1`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 19.4 KB (19370 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.26-alpine3.19` - linux; s390x

```console
$ docker pull memcached@sha256:62dab6a9b0b7245477027221202f878ec8ca2b57f0e7b73cd8fd87ddd835c38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4332854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5558373c07611e5d9c5f065de41425c65fcb4edafee9c73f7471e20ecd1c63a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
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
	-	`sha256:f8ad24edb46ae1f03842b15a18bed8c9459caf47c9b44ac9e9f8ceba287a2d99`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 975.4 KB (975434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72add78eac56e24383a18f968c20868c803c6abfde9560e6df8a55ce9ac8420`  
		Last Modified: Thu, 28 Mar 2024 19:28:29 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7415f1d9d4bf360b03d79bc7084a83a370483d24310a700a4dca754c6e3972`  
		Last Modified: Thu, 28 Mar 2024 19:28:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:ecba7487095ee7d9a4ab5dc74ce4e434f1a2d8056d87a5a2ddd6b74e82fa3b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32fcbd9dbbf02e688908e774ab684beff7ef28a6afaf60dd34855dd53e199caa`

```dockerfile
```

-	Layers:
	-	`sha256:777960c66626abacd0c8e4e899960921e1a9e3b55adac8dd3c822e7df8945bee`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d43a6b7e3f38d4afafbea91c4b713749a30e42109508da2f9d64a72cd1db3a43`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 19.3 KB (19302 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.26-bookworm`

```console
$ docker pull memcached@sha256:9eb572b94abad82c04f1329c97e72684931b1dda2cb5c0ee6c4d115f76d6b037
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

### `memcached:1.6.26-bookworm` - linux; amd64

```console
$ docker pull memcached@sha256:2967dc980ac80883003061c899102ed6c8749ed50712d4cf592b7c53efd7a498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32872677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7787f9f0d27b97ee6da8b7b2fdf9dec18a1c0fa6c05b0d4a454cc84138bfceb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131f56ef3fe0a1487206d17cc66325f94d97854c231561697099f0162c37a033`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa35112bf68c5c494491a4c7fbbb8ba5e4d9d410ce9150f1b3238414cbc091b0`  
		Last Modified: Wed, 10 Apr 2024 02:57:19 GMT  
		Size: 2.5 MB (2488500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a672c032d4a7b7c0de949d9fe1d4896cc7da42256b16e1daba353de964968b8`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 1.3 MB (1251305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01135bb689569cd15c6a2b8d8e115947652e4d61a01127729ea24513d1f57d2`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48f53906ef45e3138f6a1f1ee8ebd01ca24a3c3a2c15301afe932077984afbb`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:ace7b79050b8d00e7046345e319209248f2ce44b7b3a67968e6662d559b4cebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0612146bf8ed0f19690c2070f49b81b2f59f0df0c0aee6b38606b04c32b3b1bc`

```dockerfile
```

-	Layers:
	-	`sha256:cbbd757e27c72cb57f0f51a89cb3d65360e0afa594c47eff406c9db9d3a27de0`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 2.3 MB (2261161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d398ef36731f34f7e28948dd252f5bd1ec36dbc3a4f7b23dd7fc9d195992db2`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 21.1 KB (21142 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.26-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:794b039b86010e20defef81d8fe493212a10d4c4f774d39e7c09aaaf8a9e3ebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30212760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:916c48be9c03801f4162ac2f2e46c0e5d0c8ffa27e110dff6f876cfe88d992ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:bfe2e0ed45dd2920845bd9283b7d13266c82fe9f48ba261b6529c28dc246d3e4 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:60d288182f6883c1ed662f82d32316348aac8ca45c943f1093aed5c0ed01b45c`  
		Last Modified: Wed, 10 Apr 2024 00:54:34 GMT  
		Size: 26.9 MB (26890564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2034ec998bbde42652af813854ab5c0f1dd9c547b6b0c4680f48b2f545ede0ef`  
		Last Modified: Wed, 10 Apr 2024 16:31:49 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d77e350a8c89faec28416a879441cd67ed9d418f318b1426c3961607be04f57`  
		Last Modified: Wed, 10 Apr 2024 16:31:50 GMT  
		Size: 2.1 MB (2089485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3b43e6036c3e47e9bde8e1b23b2e18ae3881bd6963c58d7378f7ea5b298be8`  
		Last Modified: Wed, 10 Apr 2024 16:31:50 GMT  
		Size: 1.2 MB (1231197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e69525c68188c9fb6f58a63eaf9f54f84812c92027f0fd1def2d187df8c8e68`  
		Last Modified: Wed, 10 Apr 2024 16:31:49 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7c08a590703b057ce8910c40bac6339e039354b046cf91903f72c731edbbe2`  
		Last Modified: Wed, 10 Apr 2024 16:31:51 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:29852f9ed352544975a85e04cce00288b41a6e90c67436126f390bb83a3973af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a23719172438c0c0276e696803f232d54be8c0b6efd0c247d70df9a191177ef6`

```dockerfile
```

-	Layers:
	-	`sha256:9a4464980ebe9ed988705320869e004e29ee47a94854bddf2950f9528b4ea70c`  
		Last Modified: Wed, 10 Apr 2024 16:31:50 GMT  
		Size: 2.3 MB (2264449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65343e5170f1bd22aadd1c65fe274b6156e6fd966337aa0b2e81b58234c21b69`  
		Last Modified: Wed, 10 Apr 2024 16:31:49 GMT  
		Size: 21.1 KB (21114 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.26-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:7fed5d02aeac33c3df4a133ce97a03c71d8a3f2713f2ff5c4788cf9096f02162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32758363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2fefeb31b86fb36b67e5a920329724ed9519c1ffeca7fa3cc86b26b876237c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc8e58118ea2b587de344fc120829e4086cf15fa1bfa009c58f17ba08203688`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc85ab0a8a03257329849592bd06635db2c84ae701f76df4c27d15306ea0737`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 2.3 MB (2346212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ebd2971429766b668a79b73696f698513334995b9470c9f9f21da0ca81dfdd`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 1.2 MB (1248481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864c041bfe7d835cabb73fb214a8a4b7a7931b18ba532835f043f470dcd3c81e`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c33e09275e854d41d4c12ccef30c6e4e9997e08df5cbcfe520940eb1edb7884`  
		Last Modified: Wed, 10 Apr 2024 16:40:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:57f39faf16f4225d453c30ea64aeb39b90c82cda39549ab0136192c33fc6fcdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a812ba1f091b4c27268db9e91ddb70c1e855cdc46b49936787eee43df1fa371e`

```dockerfile
```

-	Layers:
	-	`sha256:c70324d70390ac933db840ed30afe02f56c58c7eaabbd1ab134e1fc87513fcff`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 2.3 MB (2261390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0535f7d789eaa3f63c11e92d1af4881c5a73f879e664b3109c1f470ad28dd71b`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 21.0 KB (20993 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.26-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:34f5ef517d7f54cc5f88ce0834b5a2d2285b7e453e648114404c375ed5bb5657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33893284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b6a893f1366a34486ca1a3011cdde9de38d5b7635c1227cf0faddfe53bb312`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:d160efeeb02e2200784dd8312a13a11d9d791581efc7756ed999f76c79445b54 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8a3830119a16769024de35d2dfa3d32147da5ea747ec336166bdca1049655803`  
		Last Modified: Wed, 10 Apr 2024 01:02:04 GMT  
		Size: 30.1 MB (30146515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4020925217af165e208be472fc2fcd518c37967f238cbcba0dbec12d20b685`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45dff0ba396ced9bb0bb69ffd5456f2a5cc783b7908bc10f4c194aa328ec3036`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 2.5 MB (2492670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9498280a2172ecdd190d1e4d3e001d55b64bbec93f4eccb039870ebbedd40f64`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 1.3 MB (1252590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf4eb265fb60a5b2351156ea6f2eccf92d961585ba20be18d7e6d3294511507`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a379f21df665e12ab146aebcf0a1cc7e55cbd7a9bbc4d17a209c7a5ba03eeb1`  
		Last Modified: Wed, 10 Apr 2024 01:55:17 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:e3e28c19c9f28d8dfee9784913c92b2a01df26c25a575a77a4f83c23281d8cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e29f55fbf81fc47ec484ab81a55a69d9c1eb3874c9eb08b813638198b69361e`

```dockerfile
```

-	Layers:
	-	`sha256:be647ca90ccc7f88e1eb3a88b1acd85aaac94d593fedbe2cebeee872c8a3b26b`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 2.3 MB (2258259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f2ac7f006c3cff208ffd83fa9513a6b12cf39a1ec192a9f01a088d0240d858b`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 21.1 KB (21087 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.26-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:fc8892b557a9bdb7b41273e3403bc2fdb3d04f99fb56a3874e9081d8dfa128d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32306668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a48487cefaf60f8ad4d3a059b0db4796bee3adbf408393dcc4c49da664f723`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 01:06:19 GMT
ADD file:c03c59e261bb08f39e6a97df2fd4b82f1e11b49a62d1859a8f8efac680b80a88 in / 
# Tue, 12 Mar 2024 01:06:23 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aad79459a0f767fcded51c9547150a1cfd96638972389ab8621b5f3eb4a9c280`  
		Last Modified: Tue, 12 Mar 2024 01:17:09 GMT  
		Size: 29.1 MB (29119205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460befff49885c738329c53c06bca553e2869317c73b0b5f76661a7053f578ad`  
		Last Modified: Tue, 09 Apr 2024 15:25:07 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6dc8cf2380155c1bacde757237b8551c77167e46ac5393332be9deb2b8dbc5`  
		Last Modified: Tue, 09 Apr 2024 15:25:07 GMT  
		Size: 1.9 MB (1937657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66db33dc07294fd7ecc848862384efa6b829c96c8939643a7098e35bbbe81d8f`  
		Last Modified: Tue, 09 Apr 2024 15:25:07 GMT  
		Size: 1.2 MB (1248284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1650df259f3af60ff6184e164ac094f261bffea30679d803c7cff2759e001699`  
		Last Modified: Tue, 09 Apr 2024 15:25:07 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51c337d2a6d822be89d42ae3e0ae8472dbd1673e648f8cdf1c769309105aaca`  
		Last Modified: Tue, 09 Apr 2024 15:25:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:831ec04c94a8b50c1aff4f18c97c8cae1d537c32821a0b8aeca9b0a1aecacae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7033955a79b1242de9912088e5d0f703e2133fce52308636758ba5ce2059d38c`

```dockerfile
```

-	Layers:
	-	`sha256:abd2f28a59a5e89ae224244ff2945a51f564194853e6abaaa8f5648413960325`  
		Last Modified: Tue, 09 Apr 2024 15:25:07 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.26-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:dc36455fb79f84d62ac6d34100afc15f0a238192dfa3224e93f753cd67d74798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37135966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:430a51910c252bd83b91329bef7a7f1a2344a5bc6b42075d419bb0facc468286`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:30:19 GMT
ADD file:9273ef56d086dbc93b46b7e8ae424eb04096fb00c693dd6cda1f48346290d4d5 in / 
# Tue, 12 Mar 2024 00:30:24 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c28cd0e276dcdeb4d44f5cc5bb958610750ff902a081b668e3863c2f38eef054`  
		Last Modified: Tue, 12 Mar 2024 00:38:06 GMT  
		Size: 33.1 MB (33119023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708b42bb3654f69ef8bfee96e8cd256f668ec36c0c79dffa3833c5a717f9eb5f`  
		Last Modified: Wed, 20 Mar 2024 21:57:50 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66c4756024ccda97c6fbe022e48d010bf3335191ef2516ace6ee30de5e87389`  
		Last Modified: Wed, 20 Mar 2024 21:57:51 GMT  
		Size: 2.7 MB (2698368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ea5604f0c8a697cb056d47640ff8d8852849f35d9a26e62b42036629bcaf9c`  
		Last Modified: Tue, 09 Apr 2024 05:05:54 GMT  
		Size: 1.3 MB (1317055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810d9546da33f92c2106ed1bbfc26223b8bef8f8e2be48b862a0270380818526`  
		Last Modified: Tue, 09 Apr 2024 05:05:54 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c78ea7da271614754f4fdc7e7d86c64da966e871cce4bab839266e27bd62912`  
		Last Modified: Tue, 09 Apr 2024 05:05:54 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:a78edf1158eed48cbec064a641fcac3c873e1b1fee26b1d8407a0269870baa23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2287859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618f6dcb01dc21ed0cc62f7efaeabc4c883f32d56e5f51a66cba2e87b31ed783`

```dockerfile
```

-	Layers:
	-	`sha256:13692af6f7d1860a31d9a8610f75d0d12eaa87131aef9b5615a57c5aaad34643`  
		Last Modified: Tue, 09 Apr 2024 05:05:54 GMT  
		Size: 2.3 MB (2266816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eae96d76b66c8c2450ce3e926ee185c9043ceff0f51f91e18694e094fd6d91af`  
		Last Modified: Tue, 09 Apr 2024 05:05:53 GMT  
		Size: 21.0 KB (21043 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.26-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:3af0cb7bc651113fdea970716a6f0a534823c322990bacbde20cc166648bb952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30873795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d9bcea2e734469166d18b5a96ac76cdcd310b4c95140b542777073e6158051`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:54:02 GMT
ADD file:80ab985d4871ca6a72156bedfe1038e6b1a89591fc2fd86c4ef778d293223aff in / 
# Tue, 12 Mar 2024 00:54:03 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9cada496cd2b8a88571bf23d513e7fce34888d13321fcf23c6613bffe4c37297`  
		Last Modified: Tue, 12 Mar 2024 01:21:14 GMT  
		Size: 27.5 MB (27488684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c430faffa085700d40355ac1aea08d429376e112bef3b9c00780b1ede56859c2`  
		Last Modified: Wed, 20 Mar 2024 22:17:08 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf1db148a80e9f25b06fe946c697ba8fa83bc46c13515904d4ceceaeb2a4eeb`  
		Last Modified: Wed, 20 Mar 2024 22:17:12 GMT  
		Size: 2.2 MB (2152657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400f8ed9afb04b498a060de1a774c9272cec70272754126b664985cd98414623`  
		Last Modified: Tue, 09 Apr 2024 14:59:31 GMT  
		Size: 1.2 MB (1230937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ca205adef44fe63941fcd64a5ea1c792c297534b81b7c23838857081d464f6`  
		Last Modified: Tue, 09 Apr 2024 14:59:31 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b24165a664a9007bca136f51d3c60c906ddf8626c9ab9403969454d4c0c47ac`  
		Last Modified: Tue, 09 Apr 2024 14:59:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.26-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:e8a1f799f3a7047f3ea6db5f3bebbdcf84726e7a0b3b45157df167d441495d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee48fbaae81e8e950ac399f89ee0eb0f7ad3e7da77d66ce435def816b3814ca`

```dockerfile
```

-	Layers:
	-	`sha256:bda232575879bf9ee6d85b64ea286f2469deccdb87ecc3991ba0fd95a508d8fa`  
		Last Modified: Tue, 09 Apr 2024 14:59:30 GMT  
		Size: 2.3 MB (2262266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13f17df99c3a427fb2b41aa30a6b4f13b2de20e1567da419bc3c6f2febb08832`  
		Last Modified: Tue, 09 Apr 2024 14:59:31 GMT  
		Size: 20.9 KB (20938 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine`

```console
$ docker pull memcached@sha256:9177d35a8e2b4224b2b99ec2930a8dc58f7c5af74a6b8143ae907fe9b11463d4
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
$ docker pull memcached@sha256:6209860fadd758c1ff8287829c97198233d086836a8b9fbf1d08125ba71666b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b686fb4e394c572a1980b134344b94d4673fcf49dd492838d7ee6a22c4c73466`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4ca62cc3e912d97d5818cdb2c21bfd6ef17fb2a46bb9ff37ef80b46aeb7579`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873fcbe9681f30840a11a64dc6ef9dfef47f40b1181e1c876969a13e35b6f5b4`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 104.2 KB (104205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2a65ada68aba9def3ee64975e1d20608c30fbb31babe05bf0a052fd5b9e631`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 952.1 KB (952136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9ac090217572c7ea3a76702db6866b9c0c35dd85d2a2bad5a50ca438050b67`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b997d515984ace5a566abec5f367a569bf51dcb5c860f5f1868154d8d61ca54`  
		Last Modified: Thu, 28 Mar 2024 18:53:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:a3837912bae62cedd588361c1fd7f24dedff8326ee89d994b188f146b2e45cdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048a973a594205e1bb5d398cc6e6d289c18ca8bd7b73c56d883080501a45af67`

```dockerfile
```

-	Layers:
	-	`sha256:fd986e4f48564cc23fae84c6c205ad8bac1f5f7733c03683ce10edf2580aed7c`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d1c90f2da382eb7f6f0edeab7ce48b9f24941fc542612204b5e38600d91d209`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 19.5 KB (19468 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:46208d1529b365696f517731af2230117072d9b61892276113308a9446932698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4425171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b581ee26004a99ed42270719e1ba6c1cc43728d706d223b58f1ded5911100ccb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bfa7663dcfe59a8997ca6332c380cce69151aeff2a9a10b71d5d655460cc3a`  
		Last Modified: Sat, 16 Mar 2024 15:47:28 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0f8117ff80fc4d046d3bf71fc57dd04a8020db6c8c4e9786b1d94d29bd1cc0`  
		Last Modified: Sat, 16 Mar 2024 15:47:28 GMT  
		Size: 120.9 KB (120902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af942211259cead4688eb0d347be9713995f1ee94d1ba1037b0ba392d4a3cdc6`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 954.9 KB (954910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e9c7aae0c99531c564569b2c18c751c8ccf729706ee0d94bbad57a1f44f0c2`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea48c501ddc68741eb04b337b84674ad57f0b41a67064a0b03ebd3003b573352`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:6dc666e80bf78a2d0c87939b02f96bedfa495d9920a7ebc747196b1cd02e2697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b89445ac664e88d593bab80bee2d0d5655c7e8514df793507272c4d185b5f98`

```dockerfile
```

-	Layers:
	-	`sha256:b6ebaa8df2f60e22d5c7a27d50ba950bb848bc48e2ad39eaafcf18f5841306f4`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:744d3c8bb078a1a54e7eff756816d1210742e1b96aea3127f6dbe2dca46c143e`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 19.3 KB (19320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:cb29d2fb5915af23e62234ec3e061ccb9bf0e09ab3146bc5275cb93d06ac2002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4300923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff0463afaa58ff4bd1755643f08e532a20be67f1c75cf31f6f4485c82ebf085`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7101892b4f7a0ec7e893a31b4c4b241666261700594b70af05e5bbde39e1ac`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2a8397306302beb9cd1c51c03f7a33b34efe159dc5423bf0450396a416aa88`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 109.3 KB (109321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6f6638920128a5138269a00784e6e731705c4aa9d114bbbcf0a94fead17efb`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 945.9 KB (945864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d19b89060fd32f477577dfc686f44f32da930716d3e5321a51c36c29b166ece`  
		Last Modified: Thu, 28 Mar 2024 18:53:12 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8ebfbbb8e7bd6745fd67fa4e70d9198ee1a540ce3b792770a1a528feb27510`  
		Last Modified: Thu, 28 Mar 2024 18:53:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:616aed5f6c6e59b28e9b940db41af823662139db453fd3dabfd0a3e4cfe27515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b397ca537b8b98807e225f556a891ee088375459e2b0560dee27496238a6f6bb`

```dockerfile
```

-	Layers:
	-	`sha256:f7c2a6ba891f879d55d2617d901135ce44cc45cb607f46af268d688d06fe6cbe`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:215e98388857b167196047f4301650abb69008e97eb82a06a1a1c1284cd18990`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 19.4 KB (19413 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:fb33bde5c5ef29f5ac1d0ead06479dff74c42b27086fe8c54f0649cce4617709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4473831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4ff16a5d7a50717ec61b2a0456c7ce9e733cf60d44539d4fed95ad3f66e754`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af93c876610139b595b7416c41cc6df9ebba87f0706b7ee1ece6a69ab0bebaa`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fb01a7e673842ded65bdcdcced99c281575743751ca219336ceb9e95b4a0e8`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 123.4 KB (123407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae3717877baa442ae7c73c0af98315cfe57d21554f2647739c792bf44240aa8`  
		Last Modified: Thu, 28 Mar 2024 19:21:45 GMT  
		Size: 990.4 KB (990428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf73c888928175612d13f100f21e51e61f22d752972c4e4c9ca9a412a53f920b`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9be9099f9a93e9d3488286c04ef2fa0350242d4207f50af77a17f89ef7e177`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:0322fdfe59a4b8ee20d7127136f42eefcff450ad57400408c51a88cb7e9914b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf6e6d6ee32aa7b5d034fdd864b17f953c8d03ffbf532b9cf455978c4a87aed`

```dockerfile
```

-	Layers:
	-	`sha256:ab3fad68489df68281f8819ef71a7a4108466ee4b9edc0a5b75db897e14ae32e`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d73a67a0c37803124f85e66364544db0aed3f07ca52ecf082733da70ec9284e1`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 19.4 KB (19370 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; s390x

```console
$ docker pull memcached@sha256:62dab6a9b0b7245477027221202f878ec8ca2b57f0e7b73cd8fd87ddd835c38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4332854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5558373c07611e5d9c5f065de41425c65fcb4edafee9c73f7471e20ecd1c63a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
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
	-	`sha256:f8ad24edb46ae1f03842b15a18bed8c9459caf47c9b44ac9e9f8ceba287a2d99`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 975.4 KB (975434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72add78eac56e24383a18f968c20868c803c6abfde9560e6df8a55ce9ac8420`  
		Last Modified: Thu, 28 Mar 2024 19:28:29 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7415f1d9d4bf360b03d79bc7084a83a370483d24310a700a4dca754c6e3972`  
		Last Modified: Thu, 28 Mar 2024 19:28:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ecba7487095ee7d9a4ab5dc74ce4e434f1a2d8056d87a5a2ddd6b74e82fa3b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32fcbd9dbbf02e688908e774ab684beff7ef28a6afaf60dd34855dd53e199caa`

```dockerfile
```

-	Layers:
	-	`sha256:777960c66626abacd0c8e4e899960921e1a9e3b55adac8dd3c822e7df8945bee`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d43a6b7e3f38d4afafbea91c4b713749a30e42109508da2f9d64a72cd1db3a43`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 19.3 KB (19302 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine3.19`

```console
$ docker pull memcached@sha256:9177d35a8e2b4224b2b99ec2930a8dc58f7c5af74a6b8143ae907fe9b11463d4
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
$ docker pull memcached@sha256:6209860fadd758c1ff8287829c97198233d086836a8b9fbf1d08125ba71666b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b686fb4e394c572a1980b134344b94d4673fcf49dd492838d7ee6a22c4c73466`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4ca62cc3e912d97d5818cdb2c21bfd6ef17fb2a46bb9ff37ef80b46aeb7579`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873fcbe9681f30840a11a64dc6ef9dfef47f40b1181e1c876969a13e35b6f5b4`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 104.2 KB (104205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2a65ada68aba9def3ee64975e1d20608c30fbb31babe05bf0a052fd5b9e631`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 952.1 KB (952136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9ac090217572c7ea3a76702db6866b9c0c35dd85d2a2bad5a50ca438050b67`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b997d515984ace5a566abec5f367a569bf51dcb5c860f5f1868154d8d61ca54`  
		Last Modified: Thu, 28 Mar 2024 18:53:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:a3837912bae62cedd588361c1fd7f24dedff8326ee89d994b188f146b2e45cdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048a973a594205e1bb5d398cc6e6d289c18ca8bd7b73c56d883080501a45af67`

```dockerfile
```

-	Layers:
	-	`sha256:fd986e4f48564cc23fae84c6c205ad8bac1f5f7733c03683ce10edf2580aed7c`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d1c90f2da382eb7f6f0edeab7ce48b9f24941fc542612204b5e38600d91d209`  
		Last Modified: Thu, 28 Mar 2024 18:53:08 GMT  
		Size: 19.5 KB (19468 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:46208d1529b365696f517731af2230117072d9b61892276113308a9446932698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4425171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b581ee26004a99ed42270719e1ba6c1cc43728d706d223b58f1ded5911100ccb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bfa7663dcfe59a8997ca6332c380cce69151aeff2a9a10b71d5d655460cc3a`  
		Last Modified: Sat, 16 Mar 2024 15:47:28 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0f8117ff80fc4d046d3bf71fc57dd04a8020db6c8c4e9786b1d94d29bd1cc0`  
		Last Modified: Sat, 16 Mar 2024 15:47:28 GMT  
		Size: 120.9 KB (120902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af942211259cead4688eb0d347be9713995f1ee94d1ba1037b0ba392d4a3cdc6`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 954.9 KB (954910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e9c7aae0c99531c564569b2c18c751c8ccf729706ee0d94bbad57a1f44f0c2`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea48c501ddc68741eb04b337b84674ad57f0b41a67064a0b03ebd3003b573352`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:6dc666e80bf78a2d0c87939b02f96bedfa495d9920a7ebc747196b1cd02e2697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b89445ac664e88d593bab80bee2d0d5655c7e8514df793507272c4d185b5f98`

```dockerfile
```

-	Layers:
	-	`sha256:b6ebaa8df2f60e22d5c7a27d50ba950bb848bc48e2ad39eaafcf18f5841306f4`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:744d3c8bb078a1a54e7eff756816d1210742e1b96aea3127f6dbe2dca46c143e`  
		Last Modified: Thu, 28 Mar 2024 18:56:47 GMT  
		Size: 19.3 KB (19320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.19` - linux; 386

```console
$ docker pull memcached@sha256:cb29d2fb5915af23e62234ec3e061ccb9bf0e09ab3146bc5275cb93d06ac2002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4300923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff0463afaa58ff4bd1755643f08e532a20be67f1c75cf31f6f4485c82ebf085`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7101892b4f7a0ec7e893a31b4c4b241666261700594b70af05e5bbde39e1ac`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2a8397306302beb9cd1c51c03f7a33b34efe159dc5423bf0450396a416aa88`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 109.3 KB (109321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6f6638920128a5138269a00784e6e731705c4aa9d114bbbcf0a94fead17efb`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 945.9 KB (945864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d19b89060fd32f477577dfc686f44f32da930716d3e5321a51c36c29b166ece`  
		Last Modified: Thu, 28 Mar 2024 18:53:12 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8ebfbbb8e7bd6745fd67fa4e70d9198ee1a540ce3b792770a1a528feb27510`  
		Last Modified: Thu, 28 Mar 2024 18:53:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:616aed5f6c6e59b28e9b940db41af823662139db453fd3dabfd0a3e4cfe27515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b397ca537b8b98807e225f556a891ee088375459e2b0560dee27496238a6f6bb`

```dockerfile
```

-	Layers:
	-	`sha256:f7c2a6ba891f879d55d2617d901135ce44cc45cb607f46af268d688d06fe6cbe`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:215e98388857b167196047f4301650abb69008e97eb82a06a1a1c1284cd18990`  
		Last Modified: Thu, 28 Mar 2024 18:53:11 GMT  
		Size: 19.4 KB (19413 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.19` - linux; ppc64le

```console
$ docker pull memcached@sha256:fb33bde5c5ef29f5ac1d0ead06479dff74c42b27086fe8c54f0649cce4617709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4473831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4ff16a5d7a50717ec61b2a0456c7ce9e733cf60d44539d4fed95ad3f66e754`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af93c876610139b595b7416c41cc6df9ebba87f0706b7ee1ece6a69ab0bebaa`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fb01a7e673842ded65bdcdcced99c281575743751ca219336ceb9e95b4a0e8`  
		Last Modified: Sat, 16 Mar 2024 10:30:18 GMT  
		Size: 123.4 KB (123407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae3717877baa442ae7c73c0af98315cfe57d21554f2647739c792bf44240aa8`  
		Last Modified: Thu, 28 Mar 2024 19:21:45 GMT  
		Size: 990.4 KB (990428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf73c888928175612d13f100f21e51e61f22d752972c4e4c9ca9a412a53f920b`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9be9099f9a93e9d3488286c04ef2fa0350242d4207f50af77a17f89ef7e177`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:0322fdfe59a4b8ee20d7127136f42eefcff450ad57400408c51a88cb7e9914b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf6e6d6ee32aa7b5d034fdd864b17f953c8d03ffbf532b9cf455978c4a87aed`

```dockerfile
```

-	Layers:
	-	`sha256:ab3fad68489df68281f8819ef71a7a4108466ee4b9edc0a5b75db897e14ae32e`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d73a67a0c37803124f85e66364544db0aed3f07ca52ecf082733da70ec9284e1`  
		Last Modified: Thu, 28 Mar 2024 19:21:44 GMT  
		Size: 19.4 KB (19370 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.19` - linux; s390x

```console
$ docker pull memcached@sha256:62dab6a9b0b7245477027221202f878ec8ca2b57f0e7b73cd8fd87ddd835c38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4332854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5558373c07611e5d9c5f065de41425c65fcb4edafee9c73f7471e20ecd1c63a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.26
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Thu, 28 Mar 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Thu, 28 Mar 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 28 Mar 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 00:54:11 GMT
USER memcache
# Thu, 28 Mar 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 28 Mar 2024 00:54:11 GMT
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
	-	`sha256:f8ad24edb46ae1f03842b15a18bed8c9459caf47c9b44ac9e9f8ceba287a2d99`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 975.4 KB (975434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72add78eac56e24383a18f968c20868c803c6abfde9560e6df8a55ce9ac8420`  
		Last Modified: Thu, 28 Mar 2024 19:28:29 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7415f1d9d4bf360b03d79bc7084a83a370483d24310a700a4dca754c6e3972`  
		Last Modified: Thu, 28 Mar 2024 19:28:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:ecba7487095ee7d9a4ab5dc74ce4e434f1a2d8056d87a5a2ddd6b74e82fa3b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32fcbd9dbbf02e688908e774ab684beff7ef28a6afaf60dd34855dd53e199caa`

```dockerfile
```

-	Layers:
	-	`sha256:777960c66626abacd0c8e4e899960921e1a9e3b55adac8dd3c822e7df8945bee`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d43a6b7e3f38d4afafbea91c4b713749a30e42109508da2f9d64a72cd1db3a43`  
		Last Modified: Thu, 28 Mar 2024 19:28:28 GMT  
		Size: 19.3 KB (19302 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:bookworm`

```console
$ docker pull memcached@sha256:9eb572b94abad82c04f1329c97e72684931b1dda2cb5c0ee6c4d115f76d6b037
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
$ docker pull memcached@sha256:2967dc980ac80883003061c899102ed6c8749ed50712d4cf592b7c53efd7a498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32872677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7787f9f0d27b97ee6da8b7b2fdf9dec18a1c0fa6c05b0d4a454cc84138bfceb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131f56ef3fe0a1487206d17cc66325f94d97854c231561697099f0162c37a033`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa35112bf68c5c494491a4c7fbbb8ba5e4d9d410ce9150f1b3238414cbc091b0`  
		Last Modified: Wed, 10 Apr 2024 02:57:19 GMT  
		Size: 2.5 MB (2488500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a672c032d4a7b7c0de949d9fe1d4896cc7da42256b16e1daba353de964968b8`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 1.3 MB (1251305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01135bb689569cd15c6a2b8d8e115947652e4d61a01127729ea24513d1f57d2`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48f53906ef45e3138f6a1f1ee8ebd01ca24a3c3a2c15301afe932077984afbb`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:ace7b79050b8d00e7046345e319209248f2ce44b7b3a67968e6662d559b4cebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0612146bf8ed0f19690c2070f49b81b2f59f0df0c0aee6b38606b04c32b3b1bc`

```dockerfile
```

-	Layers:
	-	`sha256:cbbd757e27c72cb57f0f51a89cb3d65360e0afa594c47eff406c9db9d3a27de0`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 2.3 MB (2261161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d398ef36731f34f7e28948dd252f5bd1ec36dbc3a4f7b23dd7fc9d195992db2`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 21.1 KB (21142 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:794b039b86010e20defef81d8fe493212a10d4c4f774d39e7c09aaaf8a9e3ebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30212760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:916c48be9c03801f4162ac2f2e46c0e5d0c8ffa27e110dff6f876cfe88d992ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:bfe2e0ed45dd2920845bd9283b7d13266c82fe9f48ba261b6529c28dc246d3e4 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:60d288182f6883c1ed662f82d32316348aac8ca45c943f1093aed5c0ed01b45c`  
		Last Modified: Wed, 10 Apr 2024 00:54:34 GMT  
		Size: 26.9 MB (26890564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2034ec998bbde42652af813854ab5c0f1dd9c547b6b0c4680f48b2f545ede0ef`  
		Last Modified: Wed, 10 Apr 2024 16:31:49 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d77e350a8c89faec28416a879441cd67ed9d418f318b1426c3961607be04f57`  
		Last Modified: Wed, 10 Apr 2024 16:31:50 GMT  
		Size: 2.1 MB (2089485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3b43e6036c3e47e9bde8e1b23b2e18ae3881bd6963c58d7378f7ea5b298be8`  
		Last Modified: Wed, 10 Apr 2024 16:31:50 GMT  
		Size: 1.2 MB (1231197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e69525c68188c9fb6f58a63eaf9f54f84812c92027f0fd1def2d187df8c8e68`  
		Last Modified: Wed, 10 Apr 2024 16:31:49 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7c08a590703b057ce8910c40bac6339e039354b046cf91903f72c731edbbe2`  
		Last Modified: Wed, 10 Apr 2024 16:31:51 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:29852f9ed352544975a85e04cce00288b41a6e90c67436126f390bb83a3973af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a23719172438c0c0276e696803f232d54be8c0b6efd0c247d70df9a191177ef6`

```dockerfile
```

-	Layers:
	-	`sha256:9a4464980ebe9ed988705320869e004e29ee47a94854bddf2950f9528b4ea70c`  
		Last Modified: Wed, 10 Apr 2024 16:31:50 GMT  
		Size: 2.3 MB (2264449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65343e5170f1bd22aadd1c65fe274b6156e6fd966337aa0b2e81b58234c21b69`  
		Last Modified: Wed, 10 Apr 2024 16:31:49 GMT  
		Size: 21.1 KB (21114 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:7fed5d02aeac33c3df4a133ce97a03c71d8a3f2713f2ff5c4788cf9096f02162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32758363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2fefeb31b86fb36b67e5a920329724ed9519c1ffeca7fa3cc86b26b876237c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc8e58118ea2b587de344fc120829e4086cf15fa1bfa009c58f17ba08203688`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc85ab0a8a03257329849592bd06635db2c84ae701f76df4c27d15306ea0737`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 2.3 MB (2346212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ebd2971429766b668a79b73696f698513334995b9470c9f9f21da0ca81dfdd`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 1.2 MB (1248481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864c041bfe7d835cabb73fb214a8a4b7a7931b18ba532835f043f470dcd3c81e`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c33e09275e854d41d4c12ccef30c6e4e9997e08df5cbcfe520940eb1edb7884`  
		Last Modified: Wed, 10 Apr 2024 16:40:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:57f39faf16f4225d453c30ea64aeb39b90c82cda39549ab0136192c33fc6fcdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a812ba1f091b4c27268db9e91ddb70c1e855cdc46b49936787eee43df1fa371e`

```dockerfile
```

-	Layers:
	-	`sha256:c70324d70390ac933db840ed30afe02f56c58c7eaabbd1ab134e1fc87513fcff`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 2.3 MB (2261390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0535f7d789eaa3f63c11e92d1af4881c5a73f879e664b3109c1f470ad28dd71b`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 21.0 KB (20993 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; 386

```console
$ docker pull memcached@sha256:34f5ef517d7f54cc5f88ce0834b5a2d2285b7e453e648114404c375ed5bb5657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33893284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b6a893f1366a34486ca1a3011cdde9de38d5b7635c1227cf0faddfe53bb312`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:d160efeeb02e2200784dd8312a13a11d9d791581efc7756ed999f76c79445b54 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8a3830119a16769024de35d2dfa3d32147da5ea747ec336166bdca1049655803`  
		Last Modified: Wed, 10 Apr 2024 01:02:04 GMT  
		Size: 30.1 MB (30146515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4020925217af165e208be472fc2fcd518c37967f238cbcba0dbec12d20b685`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45dff0ba396ced9bb0bb69ffd5456f2a5cc783b7908bc10f4c194aa328ec3036`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 2.5 MB (2492670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9498280a2172ecdd190d1e4d3e001d55b64bbec93f4eccb039870ebbedd40f64`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 1.3 MB (1252590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf4eb265fb60a5b2351156ea6f2eccf92d961585ba20be18d7e6d3294511507`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a379f21df665e12ab146aebcf0a1cc7e55cbd7a9bbc4d17a209c7a5ba03eeb1`  
		Last Modified: Wed, 10 Apr 2024 01:55:17 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:e3e28c19c9f28d8dfee9784913c92b2a01df26c25a575a77a4f83c23281d8cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e29f55fbf81fc47ec484ab81a55a69d9c1eb3874c9eb08b813638198b69361e`

```dockerfile
```

-	Layers:
	-	`sha256:be647ca90ccc7f88e1eb3a88b1acd85aaac94d593fedbe2cebeee872c8a3b26b`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 2.3 MB (2258259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f2ac7f006c3cff208ffd83fa9513a6b12cf39a1ec192a9f01a088d0240d858b`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 21.1 KB (21087 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:fc8892b557a9bdb7b41273e3403bc2fdb3d04f99fb56a3874e9081d8dfa128d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32306668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a48487cefaf60f8ad4d3a059b0db4796bee3adbf408393dcc4c49da664f723`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 01:06:19 GMT
ADD file:c03c59e261bb08f39e6a97df2fd4b82f1e11b49a62d1859a8f8efac680b80a88 in / 
# Tue, 12 Mar 2024 01:06:23 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aad79459a0f767fcded51c9547150a1cfd96638972389ab8621b5f3eb4a9c280`  
		Last Modified: Tue, 12 Mar 2024 01:17:09 GMT  
		Size: 29.1 MB (29119205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460befff49885c738329c53c06bca553e2869317c73b0b5f76661a7053f578ad`  
		Last Modified: Tue, 09 Apr 2024 15:25:07 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6dc8cf2380155c1bacde757237b8551c77167e46ac5393332be9deb2b8dbc5`  
		Last Modified: Tue, 09 Apr 2024 15:25:07 GMT  
		Size: 1.9 MB (1937657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66db33dc07294fd7ecc848862384efa6b829c96c8939643a7098e35bbbe81d8f`  
		Last Modified: Tue, 09 Apr 2024 15:25:07 GMT  
		Size: 1.2 MB (1248284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1650df259f3af60ff6184e164ac094f261bffea30679d803c7cff2759e001699`  
		Last Modified: Tue, 09 Apr 2024 15:25:07 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51c337d2a6d822be89d42ae3e0ae8472dbd1673e648f8cdf1c769309105aaca`  
		Last Modified: Tue, 09 Apr 2024 15:25:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:831ec04c94a8b50c1aff4f18c97c8cae1d537c32821a0b8aeca9b0a1aecacae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7033955a79b1242de9912088e5d0f703e2133fce52308636758ba5ce2059d38c`

```dockerfile
```

-	Layers:
	-	`sha256:abd2f28a59a5e89ae224244ff2945a51f564194853e6abaaa8f5648413960325`  
		Last Modified: Tue, 09 Apr 2024 15:25:07 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:dc36455fb79f84d62ac6d34100afc15f0a238192dfa3224e93f753cd67d74798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37135966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:430a51910c252bd83b91329bef7a7f1a2344a5bc6b42075d419bb0facc468286`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:30:19 GMT
ADD file:9273ef56d086dbc93b46b7e8ae424eb04096fb00c693dd6cda1f48346290d4d5 in / 
# Tue, 12 Mar 2024 00:30:24 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c28cd0e276dcdeb4d44f5cc5bb958610750ff902a081b668e3863c2f38eef054`  
		Last Modified: Tue, 12 Mar 2024 00:38:06 GMT  
		Size: 33.1 MB (33119023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708b42bb3654f69ef8bfee96e8cd256f668ec36c0c79dffa3833c5a717f9eb5f`  
		Last Modified: Wed, 20 Mar 2024 21:57:50 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66c4756024ccda97c6fbe022e48d010bf3335191ef2516ace6ee30de5e87389`  
		Last Modified: Wed, 20 Mar 2024 21:57:51 GMT  
		Size: 2.7 MB (2698368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ea5604f0c8a697cb056d47640ff8d8852849f35d9a26e62b42036629bcaf9c`  
		Last Modified: Tue, 09 Apr 2024 05:05:54 GMT  
		Size: 1.3 MB (1317055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810d9546da33f92c2106ed1bbfc26223b8bef8f8e2be48b862a0270380818526`  
		Last Modified: Tue, 09 Apr 2024 05:05:54 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c78ea7da271614754f4fdc7e7d86c64da966e871cce4bab839266e27bd62912`  
		Last Modified: Tue, 09 Apr 2024 05:05:54 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:a78edf1158eed48cbec064a641fcac3c873e1b1fee26b1d8407a0269870baa23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2287859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618f6dcb01dc21ed0cc62f7efaeabc4c883f32d56e5f51a66cba2e87b31ed783`

```dockerfile
```

-	Layers:
	-	`sha256:13692af6f7d1860a31d9a8610f75d0d12eaa87131aef9b5615a57c5aaad34643`  
		Last Modified: Tue, 09 Apr 2024 05:05:54 GMT  
		Size: 2.3 MB (2266816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eae96d76b66c8c2450ce3e926ee185c9043ceff0f51f91e18694e094fd6d91af`  
		Last Modified: Tue, 09 Apr 2024 05:05:53 GMT  
		Size: 21.0 KB (21043 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:3af0cb7bc651113fdea970716a6f0a534823c322990bacbde20cc166648bb952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30873795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d9bcea2e734469166d18b5a96ac76cdcd310b4c95140b542777073e6158051`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:54:02 GMT
ADD file:80ab985d4871ca6a72156bedfe1038e6b1a89591fc2fd86c4ef778d293223aff in / 
# Tue, 12 Mar 2024 00:54:03 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9cada496cd2b8a88571bf23d513e7fce34888d13321fcf23c6613bffe4c37297`  
		Last Modified: Tue, 12 Mar 2024 01:21:14 GMT  
		Size: 27.5 MB (27488684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c430faffa085700d40355ac1aea08d429376e112bef3b9c00780b1ede56859c2`  
		Last Modified: Wed, 20 Mar 2024 22:17:08 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf1db148a80e9f25b06fe946c697ba8fa83bc46c13515904d4ceceaeb2a4eeb`  
		Last Modified: Wed, 20 Mar 2024 22:17:12 GMT  
		Size: 2.2 MB (2152657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400f8ed9afb04b498a060de1a774c9272cec70272754126b664985cd98414623`  
		Last Modified: Tue, 09 Apr 2024 14:59:31 GMT  
		Size: 1.2 MB (1230937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ca205adef44fe63941fcd64a5ea1c792c297534b81b7c23838857081d464f6`  
		Last Modified: Tue, 09 Apr 2024 14:59:31 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b24165a664a9007bca136f51d3c60c906ddf8626c9ab9403969454d4c0c47ac`  
		Last Modified: Tue, 09 Apr 2024 14:59:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:e8a1f799f3a7047f3ea6db5f3bebbdcf84726e7a0b3b45157df167d441495d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee48fbaae81e8e950ac399f89ee0eb0f7ad3e7da77d66ce435def816b3814ca`

```dockerfile
```

-	Layers:
	-	`sha256:bda232575879bf9ee6d85b64ea286f2469deccdb87ecc3991ba0fd95a508d8fa`  
		Last Modified: Tue, 09 Apr 2024 14:59:30 GMT  
		Size: 2.3 MB (2262266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13f17df99c3a427fb2b41aa30a6b4f13b2de20e1567da419bc3c6f2febb08832`  
		Last Modified: Tue, 09 Apr 2024 14:59:31 GMT  
		Size: 20.9 KB (20938 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:latest`

```console
$ docker pull memcached@sha256:9eb572b94abad82c04f1329c97e72684931b1dda2cb5c0ee6c4d115f76d6b037
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
$ docker pull memcached@sha256:2967dc980ac80883003061c899102ed6c8749ed50712d4cf592b7c53efd7a498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32872677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7787f9f0d27b97ee6da8b7b2fdf9dec18a1c0fa6c05b0d4a454cc84138bfceb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131f56ef3fe0a1487206d17cc66325f94d97854c231561697099f0162c37a033`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa35112bf68c5c494491a4c7fbbb8ba5e4d9d410ce9150f1b3238414cbc091b0`  
		Last Modified: Wed, 10 Apr 2024 02:57:19 GMT  
		Size: 2.5 MB (2488500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a672c032d4a7b7c0de949d9fe1d4896cc7da42256b16e1daba353de964968b8`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 1.3 MB (1251305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01135bb689569cd15c6a2b8d8e115947652e4d61a01127729ea24513d1f57d2`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48f53906ef45e3138f6a1f1ee8ebd01ca24a3c3a2c15301afe932077984afbb`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:ace7b79050b8d00e7046345e319209248f2ce44b7b3a67968e6662d559b4cebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0612146bf8ed0f19690c2070f49b81b2f59f0df0c0aee6b38606b04c32b3b1bc`

```dockerfile
```

-	Layers:
	-	`sha256:cbbd757e27c72cb57f0f51a89cb3d65360e0afa594c47eff406c9db9d3a27de0`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 2.3 MB (2261161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d398ef36731f34f7e28948dd252f5bd1ec36dbc3a4f7b23dd7fc9d195992db2`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 21.1 KB (21142 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:794b039b86010e20defef81d8fe493212a10d4c4f774d39e7c09aaaf8a9e3ebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30212760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:916c48be9c03801f4162ac2f2e46c0e5d0c8ffa27e110dff6f876cfe88d992ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:bfe2e0ed45dd2920845bd9283b7d13266c82fe9f48ba261b6529c28dc246d3e4 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:60d288182f6883c1ed662f82d32316348aac8ca45c943f1093aed5c0ed01b45c`  
		Last Modified: Wed, 10 Apr 2024 00:54:34 GMT  
		Size: 26.9 MB (26890564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2034ec998bbde42652af813854ab5c0f1dd9c547b6b0c4680f48b2f545ede0ef`  
		Last Modified: Wed, 10 Apr 2024 16:31:49 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d77e350a8c89faec28416a879441cd67ed9d418f318b1426c3961607be04f57`  
		Last Modified: Wed, 10 Apr 2024 16:31:50 GMT  
		Size: 2.1 MB (2089485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3b43e6036c3e47e9bde8e1b23b2e18ae3881bd6963c58d7378f7ea5b298be8`  
		Last Modified: Wed, 10 Apr 2024 16:31:50 GMT  
		Size: 1.2 MB (1231197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e69525c68188c9fb6f58a63eaf9f54f84812c92027f0fd1def2d187df8c8e68`  
		Last Modified: Wed, 10 Apr 2024 16:31:49 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7c08a590703b057ce8910c40bac6339e039354b046cf91903f72c731edbbe2`  
		Last Modified: Wed, 10 Apr 2024 16:31:51 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:29852f9ed352544975a85e04cce00288b41a6e90c67436126f390bb83a3973af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a23719172438c0c0276e696803f232d54be8c0b6efd0c247d70df9a191177ef6`

```dockerfile
```

-	Layers:
	-	`sha256:9a4464980ebe9ed988705320869e004e29ee47a94854bddf2950f9528b4ea70c`  
		Last Modified: Wed, 10 Apr 2024 16:31:50 GMT  
		Size: 2.3 MB (2264449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65343e5170f1bd22aadd1c65fe274b6156e6fd966337aa0b2e81b58234c21b69`  
		Last Modified: Wed, 10 Apr 2024 16:31:49 GMT  
		Size: 21.1 KB (21114 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:7fed5d02aeac33c3df4a133ce97a03c71d8a3f2713f2ff5c4788cf9096f02162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32758363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2fefeb31b86fb36b67e5a920329724ed9519c1ffeca7fa3cc86b26b876237c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc8e58118ea2b587de344fc120829e4086cf15fa1bfa009c58f17ba08203688`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc85ab0a8a03257329849592bd06635db2c84ae701f76df4c27d15306ea0737`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 2.3 MB (2346212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ebd2971429766b668a79b73696f698513334995b9470c9f9f21da0ca81dfdd`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 1.2 MB (1248481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864c041bfe7d835cabb73fb214a8a4b7a7931b18ba532835f043f470dcd3c81e`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c33e09275e854d41d4c12ccef30c6e4e9997e08df5cbcfe520940eb1edb7884`  
		Last Modified: Wed, 10 Apr 2024 16:40:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:57f39faf16f4225d453c30ea64aeb39b90c82cda39549ab0136192c33fc6fcdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a812ba1f091b4c27268db9e91ddb70c1e855cdc46b49936787eee43df1fa371e`

```dockerfile
```

-	Layers:
	-	`sha256:c70324d70390ac933db840ed30afe02f56c58c7eaabbd1ab134e1fc87513fcff`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 2.3 MB (2261390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0535f7d789eaa3f63c11e92d1af4881c5a73f879e664b3109c1f470ad28dd71b`  
		Last Modified: Wed, 10 Apr 2024 16:40:32 GMT  
		Size: 21.0 KB (20993 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:34f5ef517d7f54cc5f88ce0834b5a2d2285b7e453e648114404c375ed5bb5657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33893284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b6a893f1366a34486ca1a3011cdde9de38d5b7635c1227cf0faddfe53bb312`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:d160efeeb02e2200784dd8312a13a11d9d791581efc7756ed999f76c79445b54 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8a3830119a16769024de35d2dfa3d32147da5ea747ec336166bdca1049655803`  
		Last Modified: Wed, 10 Apr 2024 01:02:04 GMT  
		Size: 30.1 MB (30146515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4020925217af165e208be472fc2fcd518c37967f238cbcba0dbec12d20b685`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45dff0ba396ced9bb0bb69ffd5456f2a5cc783b7908bc10f4c194aa328ec3036`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 2.5 MB (2492670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9498280a2172ecdd190d1e4d3e001d55b64bbec93f4eccb039870ebbedd40f64`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 1.3 MB (1252590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf4eb265fb60a5b2351156ea6f2eccf92d961585ba20be18d7e6d3294511507`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a379f21df665e12ab146aebcf0a1cc7e55cbd7a9bbc4d17a209c7a5ba03eeb1`  
		Last Modified: Wed, 10 Apr 2024 01:55:17 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:e3e28c19c9f28d8dfee9784913c92b2a01df26c25a575a77a4f83c23281d8cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e29f55fbf81fc47ec484ab81a55a69d9c1eb3874c9eb08b813638198b69361e`

```dockerfile
```

-	Layers:
	-	`sha256:be647ca90ccc7f88e1eb3a88b1acd85aaac94d593fedbe2cebeee872c8a3b26b`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 2.3 MB (2258259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f2ac7f006c3cff208ffd83fa9513a6b12cf39a1ec192a9f01a088d0240d858b`  
		Last Modified: Wed, 10 Apr 2024 01:55:16 GMT  
		Size: 21.1 KB (21087 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; mips64le

```console
$ docker pull memcached@sha256:fc8892b557a9bdb7b41273e3403bc2fdb3d04f99fb56a3874e9081d8dfa128d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32306668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a48487cefaf60f8ad4d3a059b0db4796bee3adbf408393dcc4c49da664f723`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 01:06:19 GMT
ADD file:c03c59e261bb08f39e6a97df2fd4b82f1e11b49a62d1859a8f8efac680b80a88 in / 
# Tue, 12 Mar 2024 01:06:23 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aad79459a0f767fcded51c9547150a1cfd96638972389ab8621b5f3eb4a9c280`  
		Last Modified: Tue, 12 Mar 2024 01:17:09 GMT  
		Size: 29.1 MB (29119205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460befff49885c738329c53c06bca553e2869317c73b0b5f76661a7053f578ad`  
		Last Modified: Tue, 09 Apr 2024 15:25:07 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6dc8cf2380155c1bacde757237b8551c77167e46ac5393332be9deb2b8dbc5`  
		Last Modified: Tue, 09 Apr 2024 15:25:07 GMT  
		Size: 1.9 MB (1937657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66db33dc07294fd7ecc848862384efa6b829c96c8939643a7098e35bbbe81d8f`  
		Last Modified: Tue, 09 Apr 2024 15:25:07 GMT  
		Size: 1.2 MB (1248284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1650df259f3af60ff6184e164ac094f261bffea30679d803c7cff2759e001699`  
		Last Modified: Tue, 09 Apr 2024 15:25:07 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51c337d2a6d822be89d42ae3e0ae8472dbd1673e648f8cdf1c769309105aaca`  
		Last Modified: Tue, 09 Apr 2024 15:25:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:831ec04c94a8b50c1aff4f18c97c8cae1d537c32821a0b8aeca9b0a1aecacae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7033955a79b1242de9912088e5d0f703e2133fce52308636758ba5ce2059d38c`

```dockerfile
```

-	Layers:
	-	`sha256:abd2f28a59a5e89ae224244ff2945a51f564194853e6abaaa8f5648413960325`  
		Last Modified: Tue, 09 Apr 2024 15:25:07 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:dc36455fb79f84d62ac6d34100afc15f0a238192dfa3224e93f753cd67d74798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37135966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:430a51910c252bd83b91329bef7a7f1a2344a5bc6b42075d419bb0facc468286`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:30:19 GMT
ADD file:9273ef56d086dbc93b46b7e8ae424eb04096fb00c693dd6cda1f48346290d4d5 in / 
# Tue, 12 Mar 2024 00:30:24 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c28cd0e276dcdeb4d44f5cc5bb958610750ff902a081b668e3863c2f38eef054`  
		Last Modified: Tue, 12 Mar 2024 00:38:06 GMT  
		Size: 33.1 MB (33119023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708b42bb3654f69ef8bfee96e8cd256f668ec36c0c79dffa3833c5a717f9eb5f`  
		Last Modified: Wed, 20 Mar 2024 21:57:50 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66c4756024ccda97c6fbe022e48d010bf3335191ef2516ace6ee30de5e87389`  
		Last Modified: Wed, 20 Mar 2024 21:57:51 GMT  
		Size: 2.7 MB (2698368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ea5604f0c8a697cb056d47640ff8d8852849f35d9a26e62b42036629bcaf9c`  
		Last Modified: Tue, 09 Apr 2024 05:05:54 GMT  
		Size: 1.3 MB (1317055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810d9546da33f92c2106ed1bbfc26223b8bef8f8e2be48b862a0270380818526`  
		Last Modified: Tue, 09 Apr 2024 05:05:54 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c78ea7da271614754f4fdc7e7d86c64da966e871cce4bab839266e27bd62912`  
		Last Modified: Tue, 09 Apr 2024 05:05:54 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:a78edf1158eed48cbec064a641fcac3c873e1b1fee26b1d8407a0269870baa23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2287859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618f6dcb01dc21ed0cc62f7efaeabc4c883f32d56e5f51a66cba2e87b31ed783`

```dockerfile
```

-	Layers:
	-	`sha256:13692af6f7d1860a31d9a8610f75d0d12eaa87131aef9b5615a57c5aaad34643`  
		Last Modified: Tue, 09 Apr 2024 05:05:54 GMT  
		Size: 2.3 MB (2266816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eae96d76b66c8c2450ce3e926ee185c9043ceff0f51f91e18694e094fd6d91af`  
		Last Modified: Tue, 09 Apr 2024 05:05:53 GMT  
		Size: 21.0 KB (21043 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:3af0cb7bc651113fdea970716a6f0a534823c322990bacbde20cc166648bb952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30873795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d9bcea2e734469166d18b5a96ac76cdcd310b4c95140b542777073e6158051`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:54:02 GMT
ADD file:80ab985d4871ca6a72156bedfe1038e6b1a89591fc2fd86c4ef778d293223aff in / 
# Tue, 12 Mar 2024 00:54:03 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9cada496cd2b8a88571bf23d513e7fce34888d13321fcf23c6613bffe4c37297`  
		Last Modified: Tue, 12 Mar 2024 01:21:14 GMT  
		Size: 27.5 MB (27488684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c430faffa085700d40355ac1aea08d429376e112bef3b9c00780b1ede56859c2`  
		Last Modified: Wed, 20 Mar 2024 22:17:08 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf1db148a80e9f25b06fe946c697ba8fa83bc46c13515904d4ceceaeb2a4eeb`  
		Last Modified: Wed, 20 Mar 2024 22:17:12 GMT  
		Size: 2.2 MB (2152657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400f8ed9afb04b498a060de1a774c9272cec70272754126b664985cd98414623`  
		Last Modified: Tue, 09 Apr 2024 14:59:31 GMT  
		Size: 1.2 MB (1230937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ca205adef44fe63941fcd64a5ea1c792c297534b81b7c23838857081d464f6`  
		Last Modified: Tue, 09 Apr 2024 14:59:31 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b24165a664a9007bca136f51d3c60c906ddf8626c9ab9403969454d4c0c47ac`  
		Last Modified: Tue, 09 Apr 2024 14:59:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:e8a1f799f3a7047f3ea6db5f3bebbdcf84726e7a0b3b45157df167d441495d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee48fbaae81e8e950ac399f89ee0eb0f7ad3e7da77d66ce435def816b3814ca`

```dockerfile
```

-	Layers:
	-	`sha256:bda232575879bf9ee6d85b64ea286f2469deccdb87ecc3991ba0fd95a508d8fa`  
		Last Modified: Tue, 09 Apr 2024 14:59:30 GMT  
		Size: 2.3 MB (2262266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13f17df99c3a427fb2b41aa30a6b4f13b2de20e1567da419bc3c6f2febb08832`  
		Last Modified: Tue, 09 Apr 2024 14:59:31 GMT  
		Size: 20.9 KB (20938 bytes)  
		MIME: application/vnd.in-toto+json
