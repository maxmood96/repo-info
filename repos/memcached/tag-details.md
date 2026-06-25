<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `memcached`

-	[`memcached:1`](#memcached1)
-	[`memcached:1-alpine`](#memcached1-alpine)
-	[`memcached:1-alpine3.24`](#memcached1-alpine324)
-	[`memcached:1-trixie`](#memcached1-trixie)
-	[`memcached:1.6`](#memcached16)
-	[`memcached:1.6-alpine`](#memcached16-alpine)
-	[`memcached:1.6-alpine3.24`](#memcached16-alpine324)
-	[`memcached:1.6-trixie`](#memcached16-trixie)
-	[`memcached:1.6.42`](#memcached1642)
-	[`memcached:1.6.42-alpine`](#memcached1642-alpine)
-	[`memcached:1.6.42-alpine3.24`](#memcached1642-alpine324)
-	[`memcached:1.6.42-trixie`](#memcached1642-trixie)
-	[`memcached:alpine`](#memcachedalpine)
-	[`memcached:alpine3.24`](#memcachedalpine324)
-	[`memcached:latest`](#memcachedlatest)
-	[`memcached:trixie`](#memcachedtrixie)

## `memcached:1`

```console
$ docker pull memcached@sha256:e2a8683c7fbb73d12dce8082525adf9df857765970e639bd9f4705acc31dfcba
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
$ docker pull memcached@sha256:3e079a2fc4232b10565b9bc19139292f16ef304297d4560f08f642f5f2d7a6a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32204836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ab1d39869e17aa04a25df4af0b5bf28a973d4f965635b067471bb44adbdc01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:21:34 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:21:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:24:28 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:24:28 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:24:28 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:24:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:24:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:24:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:24:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:24:28 GMT
USER memcache
# Wed, 24 Jun 2026 01:24:28 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:24:28 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1213ec9c2c2febafa221ff6195f27ea10c675acbc71d21fcc0d2b2ade3f5f74b`  
		Last Modified: Wed, 24 Jun 2026 01:24:34 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3266f17f87ca1b46b5c4fde9dd99707e3827b91b70059e7031ef53abd47fb12c`  
		Last Modified: Wed, 24 Jun 2026 01:24:34 GMT  
		Size: 136.7 KB (136688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a006226c9ea4b6f900685ceec0bda7162e03f436f1b312db9c6ba0d5b47919c7`  
		Last Modified: Wed, 24 Jun 2026 01:24:35 GMT  
		Size: 2.3 MB (2281216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3fd586859c95b544309532471aaabcf797408c5d017bd900b8e4c56c911367`  
		Last Modified: Wed, 24 Jun 2026 01:24:34 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2160167316cd327104547209c9d482373032078e07bb8a6a1e807f7e415571`  
		Last Modified: Wed, 24 Jun 2026 01:24:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:78b554b9b0edb7e45697fbdc7fb7bd3b9facbf500f3f955b3e21628a2469b659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97077f9e00ac4cde9ecb4dba83482ab83cfb8c9378171bf96fc076cc86a64a7`

```dockerfile
```

-	Layers:
	-	`sha256:0f81896f32bd3f922ecc9c3921e78406158e32af9b86b0bc711b5381f977f1e1`  
		Last Modified: Wed, 24 Jun 2026 01:24:35 GMT  
		Size: 2.0 MB (2008368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2714f45af9d9661f076eb378c43b8c30b2b1556e38d5573a646c9df3faae7740`  
		Last Modified: Wed, 24 Jun 2026 01:24:34 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v5

```console
$ docker pull memcached@sha256:07d3a299e990256fef486b7259267b9140a71a6003c6b138f0629c06e8eab05a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30316687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3763f93158d93525ae099ec31b8c33c6f309d88e3e96f8e6e18ba87c3f5c18`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:14:31 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:14:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:17:52 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:17:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:17:52 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:17:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:17:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:17:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:17:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:17:52 GMT
USER memcache
# Wed, 24 Jun 2026 01:17:52 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:17:52 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:da43bc6a07a9cd7cc23faa538adc0797482747316b5a85b9f3f94ed17f6c1a2a`  
		Last Modified: Wed, 24 Jun 2026 00:28:12 GMT  
		Size: 28.0 MB (27959221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72b0a4d36a2a621f7921b07bce6fd125f5f5dcef47bd823dc4e31290e3e2399`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4e24ea733891c84a840e31af3fb0b9c15056a407cdc805d54c8cfd3e6ef6f0`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 144.2 KB (144157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64639d0df1b35e7dbd196efee0fd423d0a736ac6c863e17f7d6986420c041af8`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 2.2 MB (2211796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090c9d3495cd22555152f5b251e3f1fe30e588646fcac43f30a778eb73470f8e`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02db167b638147d6fc9f87b04a310ffd4b96fc41da3f61194b9525811486129`  
		Last Modified: Wed, 24 Jun 2026 01:18:00 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:b276ce09ef33302e7b98984a8b1515cd0c83190274b6163f2a28f2d539cc4a7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:390cd34082323b589abd9a85a9cf2513c80fd64085a0a6aa744e0b297aa7a4b5`

```dockerfile
```

-	Layers:
	-	`sha256:259590638c0e780d766f685e7f3a057b89c4575e1736e106d88bcbd2e7c345cb`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 2.0 MB (2011371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd7d6f82a916ba666327037ebdcdce8491adee8668fde99a67161383e1bdaf64`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v7

```console
$ docker pull memcached@sha256:e2be04c60636f94c2c1555f324fd58c8ed1cca98bfc5721d5d00a8357a7df461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28513245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc5b22192f1fe06b621ee612a1428f71028d4702873f593a6e3f1896b5c7edfd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:19:26 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:19:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:22:38 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:22:38 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:22:38 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:22:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:22:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:22:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:22:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:22:38 GMT
USER memcache
# Wed, 24 Jun 2026 01:22:38 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:22:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:81c84b0273952340067af970e1fe77a42ea83b4ed1a53319e258d5f1077848f0`  
		Last Modified: Wed, 24 Jun 2026 00:28:38 GMT  
		Size: 26.2 MB (26211051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0642cf323abcb26caa4c3ff3b7e80d0d7d6d9f6d9d9accdcf6d336f41426f102`  
		Last Modified: Wed, 24 Jun 2026 01:22:44 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2360e1299ad9a74124543c81dfb5655cf827191bca3b68df2bfa35cef12ff4c6`  
		Last Modified: Wed, 24 Jun 2026 01:22:44 GMT  
		Size: 135.4 KB (135381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa1e7d2a4dedc5e64f5906cba5d754b8a704705fc6875aa2c6e19fbf32e80d0`  
		Last Modified: Wed, 24 Jun 2026 01:22:45 GMT  
		Size: 2.2 MB (2165300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1110dbe0eb2a934122b522315e135c97a24e58dfe0d85799fa581bed83010517`  
		Last Modified: Wed, 24 Jun 2026 01:22:44 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6a4eee2665c4591534d0fb4f767664091dd2025201db5c28be41b6cde451d4`  
		Last Modified: Wed, 24 Jun 2026 01:22:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:69daaf7d08ee571ea31fa5ba2bbed9ee75e05eaa0e828fec25bcbbb5db45e674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ce76762dc893723cf043776255f735aa512c188d67735932b74d4347be6e02d`

```dockerfile
```

-	Layers:
	-	`sha256:bd51ee9d8e158fbc8c58b5d3ec9bb91d9e9adb533d51ef67ba795e241a2a1486`  
		Last Modified: Wed, 24 Jun 2026 01:22:45 GMT  
		Size: 2.0 MB (2009828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce07aa39f2cbf08f3885676ecfd34bf02f971dd10ba62db2f161f39e032df30d`  
		Last Modified: Wed, 24 Jun 2026 01:22:44 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ce9daf8b2144b701cf7e968ab341768bb2d3efa2a4c64d02da0a0de42c56f1bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32566611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cc2b42a078d89f4b7328abbd61b2cc235e3c733db4c018c8c232c8e3c8dac40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:22:00 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:22:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:25:00 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:25:00 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:25:00 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:25:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:25:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:25:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:25:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:25:00 GMT
USER memcache
# Wed, 24 Jun 2026 01:25:00 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:25:00 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45863abe59cf630e20caf87380378a813615419b3e0f3a8f6649855538dd606`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b7dfd57d8e29e17a7f5191adae69420144fe599879e351b48979971c36f465`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 153.5 KB (153487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be9b72bcf7171564f265414becff9bc077025e30b3f602008e49e51af592400`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 2.3 MB (2263062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff542c356a684239a022d62e5a51aa3f8884a5a1c5a7125cd5d4133c8bac04a`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf0b844cb30e05fdae9181c546555144b913389d03c3ed5549c809d6d4f5cb5`  
		Last Modified: Wed, 24 Jun 2026 01:25:07 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:4b6ea06e8e33c13f6ed836c0f565b1bb81217e79880acaac6b7ad6c4ae57a35d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d49fd2b1e37fca3ad0e2c2747ad1ffa5e40f4dac971d3d382bb685ad2cbeb75`

```dockerfile
```

-	Layers:
	-	`sha256:0749a7c57e354ea8640b297fd510a9c6b05145e740a4d1747f3d832d71878a63`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 2.0 MB (2008676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31dad526561e0628b5270544aa1a9c883fbecd2e25a9770bf262407c2e0bf810`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:b2916cadce1269827ce2769d75e850a06fa02e2b29d606a5300c10859def3696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33675687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c903111eaced6eb842f558accf95d8d210049b93dfdce69195cb596a9295aa2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:17:36 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:17:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:20:39 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:20:39 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:20:39 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:20:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:20:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:20:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:20:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:20:39 GMT
USER memcache
# Wed, 24 Jun 2026 01:20:39 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:20:39 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:984d3baa100eb8c4d7c83b7c23b4748e508aa6ed5903297f02be90a681f52d41`  
		Last Modified: Wed, 24 Jun 2026 00:28:38 GMT  
		Size: 31.3 MB (31301210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e88a5ba508193f8a40b67d411ba88b51522122e991c5e579f718f03a7b827d5`  
		Last Modified: Wed, 24 Jun 2026 01:20:45 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13a37bd401d9e6fe5c150251a68821160273feb13462cbe401715d4c50bbcee`  
		Last Modified: Wed, 24 Jun 2026 01:20:45 GMT  
		Size: 147.5 KB (147522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f7f30bf297b5062f967e9d807b67dbfcbd20800b75c6daae0ad7fff1edf46e`  
		Last Modified: Wed, 24 Jun 2026 01:20:46 GMT  
		Size: 2.2 MB (2225442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1687fae458633e2c28615b4a2b32841cea0191dc6777aa4ad23de450a9f898e4`  
		Last Modified: Wed, 24 Jun 2026 01:20:45 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc431901c24b9ea4ccb36149baa5b10a412da5738b7f7af9808c7a408caebc12`  
		Last Modified: Wed, 24 Jun 2026 01:20:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:ceb7723388cb240f2eff890796603dfa6d63cb5e7f9e9774cf291a70411779ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596e979ff6ae6cf65094d2e268ad30ecd052f4cb73e4dddeb3644a8b5d4e00b7`

```dockerfile
```

-	Layers:
	-	`sha256:f42e4ebf214a33a305d64952d73fd7dd183f7a9b3c1ee3618be109170351a6f2`  
		Last Modified: Wed, 24 Jun 2026 01:20:45 GMT  
		Size: 2.0 MB (2005525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd85722eeac2901ebcdc4b4970759b139e69583f42cc4b4f5f84fc21347082c0`  
		Last Modified: Wed, 24 Jun 2026 01:20:45 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:f26a6eb2688cfd1f4cf236c411f9988f840b8e69f0d81f925c8c5b375608a5b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36173798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683edb23fb2832c336aa1334780707e8e429ee767b084b9c4ebf1a76eee13670`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:32:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:32:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:35:52 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:35:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:35:52 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:35:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:35:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:35:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:35:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:35:52 GMT
USER memcache
# Wed, 24 Jun 2026 01:35:52 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:35:52 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:639e1c13483ea279c94219be2736856262d8dd2efeff3e6d309f11a66aba21fb`  
		Last Modified: Wed, 24 Jun 2026 00:30:29 GMT  
		Size: 33.6 MB (33606388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d700e36837a63da25a34bd9fef9f7937541cbe617e8c1e9c4a785cc37d6e2e29`  
		Last Modified: Wed, 24 Jun 2026 01:36:14 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7456d8868d48e0b53288836b26930c6efe02b67c099dcefa481778870fc15df`  
		Last Modified: Wed, 24 Jun 2026 01:36:15 GMT  
		Size: 170.4 KB (170375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7daaa467c3a42eb0ea458c5771839433b7c4f773537351a10e30789f995f63`  
		Last Modified: Wed, 24 Jun 2026 01:36:15 GMT  
		Size: 2.4 MB (2395518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a6999cbf05638c0554accc7e8f9d8acd435888a52ad68267fcbd567d8fdce0`  
		Last Modified: Wed, 24 Jun 2026 01:36:14 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5f81262c7fc9478a7854e6dcf5e83a4d09732948b63b45b5d138da7fd57d8c`  
		Last Modified: Wed, 24 Jun 2026 01:36:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:1db8703b08d0d14737d40156d6a09384027af9d6806c94c63763d4b5cd08bc31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9df60db9b699e1540eb1b1a65a79dfffa825cdb8a5c9ce191b5cd53055af17e2`

```dockerfile
```

-	Layers:
	-	`sha256:d207552f6be1ed5a92472733946f240471025ee31516d22f4e4e1710136a5df9`  
		Last Modified: Wed, 24 Jun 2026 01:36:15 GMT  
		Size: 2.0 MB (2011969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2777dc1115238cc20388367ecc331281ddd19f28aafede9028ceb87baaf56ed`  
		Last Modified: Wed, 24 Jun 2026 01:36:14 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; riscv64

```console
$ docker pull memcached@sha256:1d09cc6da0fcd7fbfd1eb9a04ab9aeb8557f8a977d85bc7758ddc33f1fae7e8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30626877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e932fab34f25980444b8d9d4042f4f019d633ae41731c4d58de9d0425aacbb5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 20:53:15 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 20:53:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jun 2026 19:11:35 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 25 Jun 2026 19:11:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 25 Jun 2026 19:11:35 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 25 Jun 2026 19:11:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 25 Jun 2026 19:11:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 25 Jun 2026 19:11:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 25 Jun 2026 19:11:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Jun 2026 19:11:35 GMT
USER memcache
# Thu, 25 Jun 2026 19:11:35 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 25 Jun 2026 19:11:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:58bface994ba631e609596a2ca5032d9d75de27f1b6476034b581e226205adab`  
		Last Modified: Wed, 24 Jun 2026 03:41:42 GMT  
		Size: 28.3 MB (28282378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88be0d85b1f48be753592f62cac7ef80c23a61c7848026bd2d489c40d2214a58`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5924e63da94311a18a309f02e655774d7a7dd21bf3dc267215c524167fb7ca02`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 133.1 KB (133093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfa9af5e6df6f7145e6f80ab61869e6613b9f5caa0cfa94788cbf01b3041add`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 2.2 MB (2209890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ace1c66f882f3224670cc80ac0c47197433c688d59a6bad4e5e137d6947a7d9`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470dc087e4a89d9d58d8fa29a67ac089e3c4b569f1c1c79265bfe24ba39500d2`  
		Last Modified: Thu, 25 Jun 2026 19:12:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:10dc6cdb2cd2787d533382c9b0e6ae2f8f3b637c254e1b54762fc75d6b7c2066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173dffb05aa61f0096ec844832f392e17573e61865ef528ee8b742faa7e4b6db`

```dockerfile
```

-	Layers:
	-	`sha256:69ed82bb373c86c8fbec635b83221f89933079ee40e6fcf48418d1a69ca5bb89`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 2.0 MB (2002332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cea64cfdecc1c5a9f3c417e6a679e88cd0613790ff8f658ca9e3ec73325fa9cc`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:6bcf745c9e84c923ee6794f31fd61c321c07e98208661f8f96267b959b19322c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32291924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfeb11440a0b99b60cfece211ea4a2d19eb4c5aa0e27cc119d9930da48bb4a23`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:17:57 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:18:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:21:15 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:21:15 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:21:15 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:21:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:21:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:21:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:21:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:21:16 GMT
USER memcache
# Wed, 24 Jun 2026 01:21:16 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:21:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b6a0af2ceb4b698210b8776157288a3fb06e46aaf75d641139449fcc50ce430d`  
		Last Modified: Wed, 24 Jun 2026 00:28:43 GMT  
		Size: 29.9 MB (29851381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3bba39c5a45464aeb0d1fa775a329c0c537439ee4814281c4fc08a68d8cd584`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a60267637fa53d628133884b458b9c84464d66f87fb587bd54667d3e7c6c0f8`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 140.5 KB (140541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009a2f1905baeb2174621049e700d37eaaf68cda0912ab76762452f73537af8e`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 2.3 MB (2298488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5127e016f9d2a0554de486521914b692af85186039386e058a7e61c9754ef414`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf617d16473cca6af3500948111afc2fce546cd4db4d94441113555d9a9da08`  
		Last Modified: Wed, 24 Jun 2026 01:21:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:2721a3c701c85fd239ef39e576be9973f43c9655cc6cb66fd5bc3dc3ce206166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c4f64b3eb5d1eccd239a9a42a97ae1477a0b589f61e823181e9ab7271116da`

```dockerfile
```

-	Layers:
	-	`sha256:26bfdc43fc003330338d918e59f990463e9e8ceae7dbef48f43cdcb95e0f9b4e`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 2.0 MB (2009805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b9c877b5a220dabf32e1e097a3fb26dc36bad47b1978fb4b39ce7ae5415394f`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:7381333da6d6ae06e02d8dfc87ee6f2c7cd0a19f7ba048d5efc538d2100e2208
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
$ docker pull memcached@sha256:ce375dd48f976d33bf35beb966cc37f202fd840a90891e58b9e71171fc74174d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5921579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d284e7a8445d8dc70e97c673a8a0175d18f39d5336ccbdfa8b240c0ef3ce4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:15:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:15:18 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:54 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:54 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:54 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb73756dcbbebc424eab53d3adda4d9f64001e7a91272a7b2a834622c08b093`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f0d6a5291334f2b54ec652193cd4e17ee22455b2f3ff3bd9b66acff6436c7b`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 106.1 KB (106066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ac11a8307528096ac745e0ef681b64854bbd012ffdfbce85587153eec73563`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 2.0 MB (1967772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3626493aad85d70a212bc66e9d45db8aef43b4bc662259563f916398165f1e64`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cdcd3f20e3aa439838f5491e6f457a42bad6c80ed9b099313bf79b57a721ea8`  
		Last Modified: Tue, 16 Jun 2026 00:18:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:bb948800301f1cae8e18e317f2b9e85636c86c4a1924ee85e125da37cb1333e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c3e084937eb543038244e151b03b8d9a0dce0b4d5bf87c2d471fa397ed5702`

```dockerfile
```

-	Layers:
	-	`sha256:9d05a792212c92363a76bb6a8205a6e7f386113b3efc1b5d600f93d4e237c975`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 94.9 KB (94897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee0e7e70ef03205f55c68bc1b74ac7854183aee4e871112794975dc852761b19`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:4b144cdbc67c11035b3d0f0c812b590ee694977f2f6a32321e538237bd2f841c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5573158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e9bb70df1535a2f8ca960f733a4404cbde900a13156a1f4446c2fd110258e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:25 GMT
ADD alpine-minirootfs-3.24.1-armhf.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:25 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:14:43 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:14:44 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:47 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:47 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3c4836a46d600cfe9a422adf7a80205cb534097e6213325e0176c51f6e5cc02e`  
		Last Modified: Sun, 14 Jun 2026 06:44:57 GMT  
		Size: 3.6 MB (3553450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e732a60042adf5cff5fe4fe0de83f937f6e5c8896500f7023e8bf68ed0670d65`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad86d1fea29db061a5ae896a0a595b144edcdb4af59deac2b75b0fb8f5fa2d4c`  
		Last Modified: Tue, 16 Jun 2026 00:17:50 GMT  
		Size: 102.6 KB (102624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f26dd2445dbf4d5624417ca290f5ae2e5774fa7fec4f5655cd2377ee3147e4`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 1.9 MB (1915730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080a186f0ca6beb06a5ce4a86fbc71f5b9995713fcc899c73f995f251ef7c987`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c4d4f455f9a2b633cca28e3aa2190e4c42ca83ca6e3ea88ea4abe16944d238`  
		Last Modified: Tue, 16 Jun 2026 00:17:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d6b7abf6ef34abf12ab2c7f84bd29ac2461eb3271d1c4070456ed9b94e4b41a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a767571287c8ca227e321ee8d65f9da82e558098bedbb15888434dcc1ce9fa`

```dockerfile
```

-	Layers:
	-	`sha256:1794ccef4392c0db4ba36ad7fde22cdacbda40f4d56f0adbef802163c87e066c`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:848c5e0ced69b802cca72c23bec05a4c6f23136212a4a1d5cc22b7c8f0154bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286f62a53a8947036e39f2b79567b31d38309fd84c7a39e43de8c5f9817a2f64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:26 GMT
ADD alpine-minirootfs-3.24.1-armv7.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:17:59 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:17:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:20:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:20:56 GMT
USER memcache
# Tue, 16 Jun 2026 00:20:56 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:20:56 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bc03a9e5b4dd452551f246e199537fe7afc1765f53f510bc81d26df9845e4008`  
		Last Modified: Sun, 14 Jun 2026 06:45:22 GMT  
		Size: 3.3 MB (3260615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f0249bacfc8953b72899bf7b6c904c8750482fce4c93108f57b2c64228b279`  
		Last Modified: Tue, 16 Jun 2026 00:21:00 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95e1b321ffc31d01e766d5d1d054967d613940563406fc54ee981926b7f6049`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 92.4 KB (92366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce112e60c1b15077277c233a7707831818dff0a15f1fc977ebebc93f817dad43`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 1.9 MB (1875183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32fa6ed5b14fd6fcf96a7cde2996063f10b8efe802c386479288a232af826027`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6648f8180a4eea1f5197f2fa2d356fbbf4e5f65345e189e720e227af64a5e31`  
		Last Modified: Tue, 16 Jun 2026 00:21:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:59387f31eff7cfb3166c5e6d4bad92e255705affcc15c84c4a06c86ecb1a9890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:174eb460b1df4523a4f71ba5a996f2285fa845fe8ef76d2df3ea8c4962c6b6ca`

```dockerfile
```

-	Layers:
	-	`sha256:4ff5e70775e819cab551295c56b58fdb0c44c105cdc4f72247e3968accd2ab2f`  
		Last Modified: Tue, 16 Jun 2026 00:21:00 GMT  
		Size: 94.3 KB (94315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00f10e1301c7e61396658f7e3ed330e400a9f304c6a0323de8ff644aba987474`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:33261748facce282dbe4dbb4d9f875139680fce4cefc13cb9ad8e1ced23f9557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6250475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1614bb2865c8f849c2bc5bf77703a1ab711695c607a8bc6edb013a076ec16d6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:18 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:16:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:16:06 GMT
USER memcache
# Tue, 16 Jun 2026 00:16:06 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:16:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5faa19f06c4d5e26332739c7f08fd3dcd2c81817471c62029a6d99af6be8748`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377a35d28f00766e2679c788b95b0a67b9aa5a76c8ef701a2a9604e2a00c3b46`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 121.8 KB (121841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0b819e89558d70f1401ca58cbc19c58ae13e15be8184fd9b2733e022f318a4`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 1.9 MB (1944247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca539cef48ff8c3f723ab23506b6786c9ed26a9cac713601b71de2dc775d26a`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4c456deed244daa6d7076f40a1cf0364d294059bb43e533677a89027843b15`  
		Last Modified: Tue, 16 Jun 2026 00:16:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:4d25960abc53b5ba1896b8f5ee04ba5ac1389900ab9b413eb62285af7281aedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d1a4b7ad428a08c8a174d5ecd9763d530e849f54a2d9b90aef934e54b9477d4`

```dockerfile
```

-	Layers:
	-	`sha256:9c0a8e5e07390fae6abe9204450009671011c4d2d5aa5fe4afdd82324fdb49b9`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 94.4 KB (94351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ee01158358d01c082867cf46a5225cf101013e4d5b7eae18fc7853e277ff0f4`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 20.7 KB (20727 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:5436d0ef6e12f2f8e454384ff4a703132b3fe820c41a55336f520bb5d1622574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5702329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8946be3d97c7b9825159f58cbf832b131c75cb90b3fb46a40d5429b9ffe32bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:19 GMT
ADD alpine-minirootfs-3.24.1-x86.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:19 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:59 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:16:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:16:46 GMT
USER memcache
# Tue, 16 Jun 2026 00:16:46 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:16:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f86df9d778509895efbf9363d8fcb0cbe0b772de536c7218e4c4c947f0be879f`  
		Last Modified: Sun, 14 Jun 2026 06:45:46 GMT  
		Size: 3.7 MB (3670141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043137360442e605bc150f28f20e1fa2d23d90131370bc405ad7d35309594491`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900ce6eeaece12033b12f1c8641c33dcf62ff2525584411911368cfcd0b38224`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 110.7 KB (110729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e8cc1c8f6bc6391eb1a43a46f0b55ca7845f824fc0f2fc7ae7587a7715814e`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 1.9 MB (1920111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94f6e4d3be92188fc182a3557fe43af5bc9f3e768a7f265977743a56eea527e`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f8a19f18dfff271426de7a17ab6780788fa4345d5fa0120e6d03720d552bd4`  
		Last Modified: Tue, 16 Jun 2026 00:16:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:00dc6a7f29b7f2f5ac46fc5678b80c43c7b1e46b4ca3c84c5597034180aeb644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de04019c7775544db9adbb4c4558d0e7c842c279e5d70532b2ac0b988ac1345`

```dockerfile
```

-	Layers:
	-	`sha256:80895f8f5e9c9b015e419096426322f4c86c33d55ca8860ee046b61d52782847`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 94.9 KB (94852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c69be8c1f82a066b46cc389712508e85c1dcd77e649c922dba46ace64b343ae`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:c7857941a51b85b136781035703afcc8854a2d70fa2091208a51f8bb7e71f934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5998515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b02b2222212c64e444ac1a2227b19f0cfb1282c8a8ced386c1b79ae48c641b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:15 GMT
ADD alpine-minirootfs-3.24.1-ppc64le.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:15 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:15:37 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:15:38 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:18:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:18:22 GMT
USER memcache
# Tue, 16 Jun 2026 00:18:22 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:18:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3ebcdcd395ccee658b9200e4b27d7699e5d6ed9f6c1858dea12781aac519ff59`  
		Last Modified: Sun, 14 Jun 2026 06:46:36 GMT  
		Size: 3.8 MB (3813400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b108e2058722fb0fb5a9310e8ebe82ab4b9c021228a94b3125ba49d318e9667`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb8160ed736eda8513164d5d703082fb0c9af9e037472ab70a02579caa3eb99`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 126.3 KB (126252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5cb88dd03ce07ecf1613c2aff220fb392763d8f22edc900c4ad032ee7103d34`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 2.1 MB (2057508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12fd57420ca797ab383c58a488044d324c4d43b3c94a848f86a0524ed3064b4`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c0c7b7a77e9375d8a75fb825fa274d9127ca96de79107550517be29501c817`  
		Last Modified: Tue, 16 Jun 2026 00:18:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:851f463d4778539d5e4981f972420f9a57ec2559488f8a59fba6abab6065032f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734dd3d91f2d6cf217233f7a9dacc3c20ff0590246adb790f95713fb21c115de`

```dockerfile
```

-	Layers:
	-	`sha256:c0d4c203ef9f66cf827ec62098d7801e1c49f1187e0fe047fd32fc2a3271f636`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 94.3 KB (94304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b734d170b5463fa77dd77072e06d51a28efe59a53600d47435b015ebcadae92`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:ba5bf40b4adc1fe04f32e2e239fa9c0020d4e89bf4079493f8bc11a92c8f4b51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5738070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d12fbf86d6880aaa9d517425d9cecddcf545ba87e577a039dea9ea99ad53d8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 05:59:15 GMT
ADD alpine-minirootfs-3.24.1-riscv64.tar.gz / # buildkit
# Tue, 16 Jun 2026 05:59:15 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 08:28:27 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 19 Jun 2026 08:28:31 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_VERSION=1.6.42
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Fri, 19 Jun 2026 08:41:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 19 Jun 2026 08:41:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 08:41:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 19 Jun 2026 08:41:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 08:41:53 GMT
USER memcache
# Fri, 19 Jun 2026 08:41:53 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 19 Jun 2026 08:41:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c34e5222b29b86391cdae95b0473ef789493ff1a0068a3a30b5d66f544bd7cf6`  
		Last Modified: Sun, 14 Jun 2026 06:47:00 GMT  
		Size: 3.6 MB (3574358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09d95a0f414638430c0cd3ecfdcce75606201917a27c7cb2ce1e34cb928b26a`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5335c7af79a1b08af55862ba77644afdae5544d9a7871e45c91b364bd4f71d`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 108.9 KB (108888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3622a6ea71515db1ef566afdbb121daed1f408aacf1519f4173b40dabe2ae627`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 2.1 MB (2053467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1db0e3e31ca3f2830f5404436e92b1862a4078adefacacec09a9580a3ad0a2`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1463b0fd26a37659aaad7f99696e5213764ad03bb094f40836c3309713d7a60`  
		Last Modified: Fri, 19 Jun 2026 08:42:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:aadb3b9338400b87692f95e00931e43940f8d6ddd13f046bd256848dd825e458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde4b5a4a468d795a5f58dd934b371adfe72cd2ae24e166e1258ad65aa455a56`

```dockerfile
```

-	Layers:
	-	`sha256:debb70180cf674562f7ca321270e3dfa350c5d1596c05dbfcc27b38c65652528`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 94.3 KB (94300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a895bbe0bfec24678c1c92ddd283cb7392e0e8d229f31c769a23c95224c0d371`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:e1b640e8d192055e5c3ccd05b077776a0f4d35664191596f7a8230b2cd7ef0f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5823313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ef6221f9c2854683b0633325a98a0e7a0d3b7d865b02d7cdf4c1d49d2e5090`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:21 GMT
ADD alpine-minirootfs-3.24.1-s390x.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:21 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:46 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:12 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:da43be6afaaa3ec1b607461ce64380942a6d76c3d52cda4337b0770d9a96fa89`  
		Last Modified: Sun, 14 Jun 2026 06:47:25 GMT  
		Size: 3.7 MB (3709320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757d04238e02c9bbe1cfd4030cc19e29421650a1b1562a8ca4090d90e9ae17b0`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1949e0fa71fc91bebf4f2e4293108b27de8357d98f98b673bc4f3ed1980b52c`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 114.3 KB (114289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f0e22966bce79fbc8a20f7c27aa07ce63229bb50181319c810ca29f1fb4032`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 2.0 MB (1998350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15eb5e912ef8ec6e3abe76c361cdddb568d20a60be21be379d4d8d7d0ebaa11e`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a549d59ad0d4761ac6f4cca272c4bea521471ed091d0e79143bfda8ff29cf9ce`  
		Last Modified: Tue, 16 Jun 2026 00:17:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:6dbf7c8a98f02a949769403ad1c92583b34a28dccc66b7d83d91863785a6dad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a89d23372d19daf2d6d4e1c4de732f7864316ed5e7713b1103918303873683e`

```dockerfile
```

-	Layers:
	-	`sha256:099ab2d711ef73783b01895824a4664c7d65e2a333e81237b4766cf053a8f6f0`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 94.2 KB (94246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eccbabf44891af00e622624c5cfd5a295656f82f1c15073b240ac34d47af96c`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine3.24`

```console
$ docker pull memcached@sha256:7381333da6d6ae06e02d8dfc87ee6f2c7cd0a19f7ba048d5efc538d2100e2208
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

### `memcached:1-alpine3.24` - linux; amd64

```console
$ docker pull memcached@sha256:ce375dd48f976d33bf35beb966cc37f202fd840a90891e58b9e71171fc74174d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5921579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d284e7a8445d8dc70e97c673a8a0175d18f39d5336ccbdfa8b240c0ef3ce4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:15:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:15:18 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:54 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:54 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:54 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb73756dcbbebc424eab53d3adda4d9f64001e7a91272a7b2a834622c08b093`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f0d6a5291334f2b54ec652193cd4e17ee22455b2f3ff3bd9b66acff6436c7b`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 106.1 KB (106066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ac11a8307528096ac745e0ef681b64854bbd012ffdfbce85587153eec73563`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 2.0 MB (1967772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3626493aad85d70a212bc66e9d45db8aef43b4bc662259563f916398165f1e64`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cdcd3f20e3aa439838f5491e6f457a42bad6c80ed9b099313bf79b57a721ea8`  
		Last Modified: Tue, 16 Jun 2026 00:18:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:bb948800301f1cae8e18e317f2b9e85636c86c4a1924ee85e125da37cb1333e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c3e084937eb543038244e151b03b8d9a0dce0b4d5bf87c2d471fa397ed5702`

```dockerfile
```

-	Layers:
	-	`sha256:9d05a792212c92363a76bb6a8205a6e7f386113b3efc1b5d600f93d4e237c975`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 94.9 KB (94897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee0e7e70ef03205f55c68bc1b74ac7854183aee4e871112794975dc852761b19`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.24` - linux; arm variant v6

```console
$ docker pull memcached@sha256:4b144cdbc67c11035b3d0f0c812b590ee694977f2f6a32321e538237bd2f841c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5573158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e9bb70df1535a2f8ca960f733a4404cbde900a13156a1f4446c2fd110258e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:25 GMT
ADD alpine-minirootfs-3.24.1-armhf.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:25 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:14:43 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:14:44 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:47 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:47 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3c4836a46d600cfe9a422adf7a80205cb534097e6213325e0176c51f6e5cc02e`  
		Last Modified: Sun, 14 Jun 2026 06:44:57 GMT  
		Size: 3.6 MB (3553450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e732a60042adf5cff5fe4fe0de83f937f6e5c8896500f7023e8bf68ed0670d65`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad86d1fea29db061a5ae896a0a595b144edcdb4af59deac2b75b0fb8f5fa2d4c`  
		Last Modified: Tue, 16 Jun 2026 00:17:50 GMT  
		Size: 102.6 KB (102624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f26dd2445dbf4d5624417ca290f5ae2e5774fa7fec4f5655cd2377ee3147e4`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 1.9 MB (1915730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080a186f0ca6beb06a5ce4a86fbc71f5b9995713fcc899c73f995f251ef7c987`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c4d4f455f9a2b633cca28e3aa2190e4c42ca83ca6e3ea88ea4abe16944d238`  
		Last Modified: Tue, 16 Jun 2026 00:17:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:d6b7abf6ef34abf12ab2c7f84bd29ac2461eb3271d1c4070456ed9b94e4b41a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a767571287c8ca227e321ee8d65f9da82e558098bedbb15888434dcc1ce9fa`

```dockerfile
```

-	Layers:
	-	`sha256:1794ccef4392c0db4ba36ad7fde22cdacbda40f4d56f0adbef802163c87e066c`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.24` - linux; arm variant v7

```console
$ docker pull memcached@sha256:848c5e0ced69b802cca72c23bec05a4c6f23136212a4a1d5cc22b7c8f0154bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286f62a53a8947036e39f2b79567b31d38309fd84c7a39e43de8c5f9817a2f64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:26 GMT
ADD alpine-minirootfs-3.24.1-armv7.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:17:59 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:17:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:20:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:20:56 GMT
USER memcache
# Tue, 16 Jun 2026 00:20:56 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:20:56 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bc03a9e5b4dd452551f246e199537fe7afc1765f53f510bc81d26df9845e4008`  
		Last Modified: Sun, 14 Jun 2026 06:45:22 GMT  
		Size: 3.3 MB (3260615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f0249bacfc8953b72899bf7b6c904c8750482fce4c93108f57b2c64228b279`  
		Last Modified: Tue, 16 Jun 2026 00:21:00 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95e1b321ffc31d01e766d5d1d054967d613940563406fc54ee981926b7f6049`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 92.4 KB (92366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce112e60c1b15077277c233a7707831818dff0a15f1fc977ebebc93f817dad43`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 1.9 MB (1875183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32fa6ed5b14fd6fcf96a7cde2996063f10b8efe802c386479288a232af826027`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6648f8180a4eea1f5197f2fa2d356fbbf4e5f65345e189e720e227af64a5e31`  
		Last Modified: Tue, 16 Jun 2026 00:21:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:59387f31eff7cfb3166c5e6d4bad92e255705affcc15c84c4a06c86ecb1a9890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:174eb460b1df4523a4f71ba5a996f2285fa845fe8ef76d2df3ea8c4962c6b6ca`

```dockerfile
```

-	Layers:
	-	`sha256:4ff5e70775e819cab551295c56b58fdb0c44c105cdc4f72247e3968accd2ab2f`  
		Last Modified: Tue, 16 Jun 2026 00:21:00 GMT  
		Size: 94.3 KB (94315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00f10e1301c7e61396658f7e3ed330e400a9f304c6a0323de8ff644aba987474`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.24` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:33261748facce282dbe4dbb4d9f875139680fce4cefc13cb9ad8e1ced23f9557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6250475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1614bb2865c8f849c2bc5bf77703a1ab711695c607a8bc6edb013a076ec16d6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:18 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:16:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:16:06 GMT
USER memcache
# Tue, 16 Jun 2026 00:16:06 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:16:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5faa19f06c4d5e26332739c7f08fd3dcd2c81817471c62029a6d99af6be8748`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377a35d28f00766e2679c788b95b0a67b9aa5a76c8ef701a2a9604e2a00c3b46`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 121.8 KB (121841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0b819e89558d70f1401ca58cbc19c58ae13e15be8184fd9b2733e022f318a4`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 1.9 MB (1944247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca539cef48ff8c3f723ab23506b6786c9ed26a9cac713601b71de2dc775d26a`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4c456deed244daa6d7076f40a1cf0364d294059bb43e533677a89027843b15`  
		Last Modified: Tue, 16 Jun 2026 00:16:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:4d25960abc53b5ba1896b8f5ee04ba5ac1389900ab9b413eb62285af7281aedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d1a4b7ad428a08c8a174d5ecd9763d530e849f54a2d9b90aef934e54b9477d4`

```dockerfile
```

-	Layers:
	-	`sha256:9c0a8e5e07390fae6abe9204450009671011c4d2d5aa5fe4afdd82324fdb49b9`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 94.4 KB (94351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ee01158358d01c082867cf46a5225cf101013e4d5b7eae18fc7853e277ff0f4`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 20.7 KB (20727 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.24` - linux; 386

```console
$ docker pull memcached@sha256:5436d0ef6e12f2f8e454384ff4a703132b3fe820c41a55336f520bb5d1622574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5702329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8946be3d97c7b9825159f58cbf832b131c75cb90b3fb46a40d5429b9ffe32bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:19 GMT
ADD alpine-minirootfs-3.24.1-x86.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:19 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:59 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:16:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:16:46 GMT
USER memcache
# Tue, 16 Jun 2026 00:16:46 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:16:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f86df9d778509895efbf9363d8fcb0cbe0b772de536c7218e4c4c947f0be879f`  
		Last Modified: Sun, 14 Jun 2026 06:45:46 GMT  
		Size: 3.7 MB (3670141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043137360442e605bc150f28f20e1fa2d23d90131370bc405ad7d35309594491`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900ce6eeaece12033b12f1c8641c33dcf62ff2525584411911368cfcd0b38224`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 110.7 KB (110729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e8cc1c8f6bc6391eb1a43a46f0b55ca7845f824fc0f2fc7ae7587a7715814e`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 1.9 MB (1920111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94f6e4d3be92188fc182a3557fe43af5bc9f3e768a7f265977743a56eea527e`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f8a19f18dfff271426de7a17ab6780788fa4345d5fa0120e6d03720d552bd4`  
		Last Modified: Tue, 16 Jun 2026 00:16:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:00dc6a7f29b7f2f5ac46fc5678b80c43c7b1e46b4ca3c84c5597034180aeb644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de04019c7775544db9adbb4c4558d0e7c842c279e5d70532b2ac0b988ac1345`

```dockerfile
```

-	Layers:
	-	`sha256:80895f8f5e9c9b015e419096426322f4c86c33d55ca8860ee046b61d52782847`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 94.9 KB (94852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c69be8c1f82a066b46cc389712508e85c1dcd77e649c922dba46ace64b343ae`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.24` - linux; ppc64le

```console
$ docker pull memcached@sha256:c7857941a51b85b136781035703afcc8854a2d70fa2091208a51f8bb7e71f934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5998515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b02b2222212c64e444ac1a2227b19f0cfb1282c8a8ced386c1b79ae48c641b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:15 GMT
ADD alpine-minirootfs-3.24.1-ppc64le.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:15 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:15:37 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:15:38 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:18:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:18:22 GMT
USER memcache
# Tue, 16 Jun 2026 00:18:22 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:18:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3ebcdcd395ccee658b9200e4b27d7699e5d6ed9f6c1858dea12781aac519ff59`  
		Last Modified: Sun, 14 Jun 2026 06:46:36 GMT  
		Size: 3.8 MB (3813400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b108e2058722fb0fb5a9310e8ebe82ab4b9c021228a94b3125ba49d318e9667`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb8160ed736eda8513164d5d703082fb0c9af9e037472ab70a02579caa3eb99`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 126.3 KB (126252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5cb88dd03ce07ecf1613c2aff220fb392763d8f22edc900c4ad032ee7103d34`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 2.1 MB (2057508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12fd57420ca797ab383c58a488044d324c4d43b3c94a848f86a0524ed3064b4`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c0c7b7a77e9375d8a75fb825fa274d9127ca96de79107550517be29501c817`  
		Last Modified: Tue, 16 Jun 2026 00:18:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:851f463d4778539d5e4981f972420f9a57ec2559488f8a59fba6abab6065032f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734dd3d91f2d6cf217233f7a9dacc3c20ff0590246adb790f95713fb21c115de`

```dockerfile
```

-	Layers:
	-	`sha256:c0d4c203ef9f66cf827ec62098d7801e1c49f1187e0fe047fd32fc2a3271f636`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 94.3 KB (94304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b734d170b5463fa77dd77072e06d51a28efe59a53600d47435b015ebcadae92`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.24` - linux; riscv64

```console
$ docker pull memcached@sha256:ba5bf40b4adc1fe04f32e2e239fa9c0020d4e89bf4079493f8bc11a92c8f4b51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5738070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d12fbf86d6880aaa9d517425d9cecddcf545ba87e577a039dea9ea99ad53d8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 05:59:15 GMT
ADD alpine-minirootfs-3.24.1-riscv64.tar.gz / # buildkit
# Tue, 16 Jun 2026 05:59:15 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 08:28:27 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 19 Jun 2026 08:28:31 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_VERSION=1.6.42
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Fri, 19 Jun 2026 08:41:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 19 Jun 2026 08:41:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 08:41:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 19 Jun 2026 08:41:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 08:41:53 GMT
USER memcache
# Fri, 19 Jun 2026 08:41:53 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 19 Jun 2026 08:41:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c34e5222b29b86391cdae95b0473ef789493ff1a0068a3a30b5d66f544bd7cf6`  
		Last Modified: Sun, 14 Jun 2026 06:47:00 GMT  
		Size: 3.6 MB (3574358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09d95a0f414638430c0cd3ecfdcce75606201917a27c7cb2ce1e34cb928b26a`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5335c7af79a1b08af55862ba77644afdae5544d9a7871e45c91b364bd4f71d`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 108.9 KB (108888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3622a6ea71515db1ef566afdbb121daed1f408aacf1519f4173b40dabe2ae627`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 2.1 MB (2053467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1db0e3e31ca3f2830f5404436e92b1862a4078adefacacec09a9580a3ad0a2`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1463b0fd26a37659aaad7f99696e5213764ad03bb094f40836c3309713d7a60`  
		Last Modified: Fri, 19 Jun 2026 08:42:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:aadb3b9338400b87692f95e00931e43940f8d6ddd13f046bd256848dd825e458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde4b5a4a468d795a5f58dd934b371adfe72cd2ae24e166e1258ad65aa455a56`

```dockerfile
```

-	Layers:
	-	`sha256:debb70180cf674562f7ca321270e3dfa350c5d1596c05dbfcc27b38c65652528`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 94.3 KB (94300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a895bbe0bfec24678c1c92ddd283cb7392e0e8d229f31c769a23c95224c0d371`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.24` - linux; s390x

```console
$ docker pull memcached@sha256:e1b640e8d192055e5c3ccd05b077776a0f4d35664191596f7a8230b2cd7ef0f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5823313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ef6221f9c2854683b0633325a98a0e7a0d3b7d865b02d7cdf4c1d49d2e5090`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:21 GMT
ADD alpine-minirootfs-3.24.1-s390x.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:21 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:46 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:12 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:da43be6afaaa3ec1b607461ce64380942a6d76c3d52cda4337b0770d9a96fa89`  
		Last Modified: Sun, 14 Jun 2026 06:47:25 GMT  
		Size: 3.7 MB (3709320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757d04238e02c9bbe1cfd4030cc19e29421650a1b1562a8ca4090d90e9ae17b0`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1949e0fa71fc91bebf4f2e4293108b27de8357d98f98b673bc4f3ed1980b52c`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 114.3 KB (114289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f0e22966bce79fbc8a20f7c27aa07ce63229bb50181319c810ca29f1fb4032`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 2.0 MB (1998350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15eb5e912ef8ec6e3abe76c361cdddb568d20a60be21be379d4d8d7d0ebaa11e`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a549d59ad0d4761ac6f4cca272c4bea521471ed091d0e79143bfda8ff29cf9ce`  
		Last Modified: Tue, 16 Jun 2026 00:17:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:6dbf7c8a98f02a949769403ad1c92583b34a28dccc66b7d83d91863785a6dad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a89d23372d19daf2d6d4e1c4de732f7864316ed5e7713b1103918303873683e`

```dockerfile
```

-	Layers:
	-	`sha256:099ab2d711ef73783b01895824a4664c7d65e2a333e81237b4766cf053a8f6f0`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 94.2 KB (94246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eccbabf44891af00e622624c5cfd5a295656f82f1c15073b240ac34d47af96c`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-trixie`

```console
$ docker pull memcached@sha256:e2a8683c7fbb73d12dce8082525adf9df857765970e639bd9f4705acc31dfcba
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
$ docker pull memcached@sha256:3e079a2fc4232b10565b9bc19139292f16ef304297d4560f08f642f5f2d7a6a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32204836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ab1d39869e17aa04a25df4af0b5bf28a973d4f965635b067471bb44adbdc01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:21:34 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:21:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:24:28 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:24:28 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:24:28 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:24:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:24:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:24:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:24:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:24:28 GMT
USER memcache
# Wed, 24 Jun 2026 01:24:28 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:24:28 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1213ec9c2c2febafa221ff6195f27ea10c675acbc71d21fcc0d2b2ade3f5f74b`  
		Last Modified: Wed, 24 Jun 2026 01:24:34 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3266f17f87ca1b46b5c4fde9dd99707e3827b91b70059e7031ef53abd47fb12c`  
		Last Modified: Wed, 24 Jun 2026 01:24:34 GMT  
		Size: 136.7 KB (136688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a006226c9ea4b6f900685ceec0bda7162e03f436f1b312db9c6ba0d5b47919c7`  
		Last Modified: Wed, 24 Jun 2026 01:24:35 GMT  
		Size: 2.3 MB (2281216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3fd586859c95b544309532471aaabcf797408c5d017bd900b8e4c56c911367`  
		Last Modified: Wed, 24 Jun 2026 01:24:34 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2160167316cd327104547209c9d482373032078e07bb8a6a1e807f7e415571`  
		Last Modified: Wed, 24 Jun 2026 01:24:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:78b554b9b0edb7e45697fbdc7fb7bd3b9facbf500f3f955b3e21628a2469b659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97077f9e00ac4cde9ecb4dba83482ab83cfb8c9378171bf96fc076cc86a64a7`

```dockerfile
```

-	Layers:
	-	`sha256:0f81896f32bd3f922ecc9c3921e78406158e32af9b86b0bc711b5381f977f1e1`  
		Last Modified: Wed, 24 Jun 2026 01:24:35 GMT  
		Size: 2.0 MB (2008368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2714f45af9d9661f076eb378c43b8c30b2b1556e38d5573a646c9df3faae7740`  
		Last Modified: Wed, 24 Jun 2026 01:24:34 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:07d3a299e990256fef486b7259267b9140a71a6003c6b138f0629c06e8eab05a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30316687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3763f93158d93525ae099ec31b8c33c6f309d88e3e96f8e6e18ba87c3f5c18`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:14:31 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:14:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:17:52 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:17:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:17:52 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:17:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:17:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:17:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:17:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:17:52 GMT
USER memcache
# Wed, 24 Jun 2026 01:17:52 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:17:52 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:da43bc6a07a9cd7cc23faa538adc0797482747316b5a85b9f3f94ed17f6c1a2a`  
		Last Modified: Wed, 24 Jun 2026 00:28:12 GMT  
		Size: 28.0 MB (27959221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72b0a4d36a2a621f7921b07bce6fd125f5f5dcef47bd823dc4e31290e3e2399`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4e24ea733891c84a840e31af3fb0b9c15056a407cdc805d54c8cfd3e6ef6f0`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 144.2 KB (144157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64639d0df1b35e7dbd196efee0fd423d0a736ac6c863e17f7d6986420c041af8`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 2.2 MB (2211796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090c9d3495cd22555152f5b251e3f1fe30e588646fcac43f30a778eb73470f8e`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02db167b638147d6fc9f87b04a310ffd4b96fc41da3f61194b9525811486129`  
		Last Modified: Wed, 24 Jun 2026 01:18:00 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:b276ce09ef33302e7b98984a8b1515cd0c83190274b6163f2a28f2d539cc4a7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:390cd34082323b589abd9a85a9cf2513c80fd64085a0a6aa744e0b297aa7a4b5`

```dockerfile
```

-	Layers:
	-	`sha256:259590638c0e780d766f685e7f3a057b89c4575e1736e106d88bcbd2e7c345cb`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 2.0 MB (2011371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd7d6f82a916ba666327037ebdcdce8491adee8668fde99a67161383e1bdaf64`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:e2be04c60636f94c2c1555f324fd58c8ed1cca98bfc5721d5d00a8357a7df461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28513245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc5b22192f1fe06b621ee612a1428f71028d4702873f593a6e3f1896b5c7edfd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:19:26 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:19:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:22:38 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:22:38 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:22:38 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:22:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:22:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:22:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:22:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:22:38 GMT
USER memcache
# Wed, 24 Jun 2026 01:22:38 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:22:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:81c84b0273952340067af970e1fe77a42ea83b4ed1a53319e258d5f1077848f0`  
		Last Modified: Wed, 24 Jun 2026 00:28:38 GMT  
		Size: 26.2 MB (26211051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0642cf323abcb26caa4c3ff3b7e80d0d7d6d9f6d9d9accdcf6d336f41426f102`  
		Last Modified: Wed, 24 Jun 2026 01:22:44 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2360e1299ad9a74124543c81dfb5655cf827191bca3b68df2bfa35cef12ff4c6`  
		Last Modified: Wed, 24 Jun 2026 01:22:44 GMT  
		Size: 135.4 KB (135381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa1e7d2a4dedc5e64f5906cba5d754b8a704705fc6875aa2c6e19fbf32e80d0`  
		Last Modified: Wed, 24 Jun 2026 01:22:45 GMT  
		Size: 2.2 MB (2165300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1110dbe0eb2a934122b522315e135c97a24e58dfe0d85799fa581bed83010517`  
		Last Modified: Wed, 24 Jun 2026 01:22:44 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6a4eee2665c4591534d0fb4f767664091dd2025201db5c28be41b6cde451d4`  
		Last Modified: Wed, 24 Jun 2026 01:22:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:69daaf7d08ee571ea31fa5ba2bbed9ee75e05eaa0e828fec25bcbbb5db45e674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ce76762dc893723cf043776255f735aa512c188d67735932b74d4347be6e02d`

```dockerfile
```

-	Layers:
	-	`sha256:bd51ee9d8e158fbc8c58b5d3ec9bb91d9e9adb533d51ef67ba795e241a2a1486`  
		Last Modified: Wed, 24 Jun 2026 01:22:45 GMT  
		Size: 2.0 MB (2009828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce07aa39f2cbf08f3885676ecfd34bf02f971dd10ba62db2f161f39e032df30d`  
		Last Modified: Wed, 24 Jun 2026 01:22:44 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ce9daf8b2144b701cf7e968ab341768bb2d3efa2a4c64d02da0a0de42c56f1bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32566611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cc2b42a078d89f4b7328abbd61b2cc235e3c733db4c018c8c232c8e3c8dac40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:22:00 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:22:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:25:00 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:25:00 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:25:00 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:25:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:25:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:25:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:25:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:25:00 GMT
USER memcache
# Wed, 24 Jun 2026 01:25:00 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:25:00 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45863abe59cf630e20caf87380378a813615419b3e0f3a8f6649855538dd606`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b7dfd57d8e29e17a7f5191adae69420144fe599879e351b48979971c36f465`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 153.5 KB (153487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be9b72bcf7171564f265414becff9bc077025e30b3f602008e49e51af592400`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 2.3 MB (2263062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff542c356a684239a022d62e5a51aa3f8884a5a1c5a7125cd5d4133c8bac04a`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf0b844cb30e05fdae9181c546555144b913389d03c3ed5549c809d6d4f5cb5`  
		Last Modified: Wed, 24 Jun 2026 01:25:07 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:4b6ea06e8e33c13f6ed836c0f565b1bb81217e79880acaac6b7ad6c4ae57a35d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d49fd2b1e37fca3ad0e2c2747ad1ffa5e40f4dac971d3d382bb685ad2cbeb75`

```dockerfile
```

-	Layers:
	-	`sha256:0749a7c57e354ea8640b297fd510a9c6b05145e740a4d1747f3d832d71878a63`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 2.0 MB (2008676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31dad526561e0628b5270544aa1a9c883fbecd2e25a9770bf262407c2e0bf810`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; 386

```console
$ docker pull memcached@sha256:b2916cadce1269827ce2769d75e850a06fa02e2b29d606a5300c10859def3696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33675687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c903111eaced6eb842f558accf95d8d210049b93dfdce69195cb596a9295aa2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:17:36 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:17:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:20:39 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:20:39 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:20:39 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:20:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:20:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:20:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:20:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:20:39 GMT
USER memcache
# Wed, 24 Jun 2026 01:20:39 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:20:39 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:984d3baa100eb8c4d7c83b7c23b4748e508aa6ed5903297f02be90a681f52d41`  
		Last Modified: Wed, 24 Jun 2026 00:28:38 GMT  
		Size: 31.3 MB (31301210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e88a5ba508193f8a40b67d411ba88b51522122e991c5e579f718f03a7b827d5`  
		Last Modified: Wed, 24 Jun 2026 01:20:45 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13a37bd401d9e6fe5c150251a68821160273feb13462cbe401715d4c50bbcee`  
		Last Modified: Wed, 24 Jun 2026 01:20:45 GMT  
		Size: 147.5 KB (147522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f7f30bf297b5062f967e9d807b67dbfcbd20800b75c6daae0ad7fff1edf46e`  
		Last Modified: Wed, 24 Jun 2026 01:20:46 GMT  
		Size: 2.2 MB (2225442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1687fae458633e2c28615b4a2b32841cea0191dc6777aa4ad23de450a9f898e4`  
		Last Modified: Wed, 24 Jun 2026 01:20:45 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc431901c24b9ea4ccb36149baa5b10a412da5738b7f7af9808c7a408caebc12`  
		Last Modified: Wed, 24 Jun 2026 01:20:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:ceb7723388cb240f2eff890796603dfa6d63cb5e7f9e9774cf291a70411779ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596e979ff6ae6cf65094d2e268ad30ecd052f4cb73e4dddeb3644a8b5d4e00b7`

```dockerfile
```

-	Layers:
	-	`sha256:f42e4ebf214a33a305d64952d73fd7dd183f7a9b3c1ee3618be109170351a6f2`  
		Last Modified: Wed, 24 Jun 2026 01:20:45 GMT  
		Size: 2.0 MB (2005525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd85722eeac2901ebcdc4b4970759b139e69583f42cc4b4f5f84fc21347082c0`  
		Last Modified: Wed, 24 Jun 2026 01:20:45 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:f26a6eb2688cfd1f4cf236c411f9988f840b8e69f0d81f925c8c5b375608a5b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36173798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683edb23fb2832c336aa1334780707e8e429ee767b084b9c4ebf1a76eee13670`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:32:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:32:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:35:52 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:35:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:35:52 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:35:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:35:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:35:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:35:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:35:52 GMT
USER memcache
# Wed, 24 Jun 2026 01:35:52 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:35:52 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:639e1c13483ea279c94219be2736856262d8dd2efeff3e6d309f11a66aba21fb`  
		Last Modified: Wed, 24 Jun 2026 00:30:29 GMT  
		Size: 33.6 MB (33606388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d700e36837a63da25a34bd9fef9f7937541cbe617e8c1e9c4a785cc37d6e2e29`  
		Last Modified: Wed, 24 Jun 2026 01:36:14 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7456d8868d48e0b53288836b26930c6efe02b67c099dcefa481778870fc15df`  
		Last Modified: Wed, 24 Jun 2026 01:36:15 GMT  
		Size: 170.4 KB (170375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7daaa467c3a42eb0ea458c5771839433b7c4f773537351a10e30789f995f63`  
		Last Modified: Wed, 24 Jun 2026 01:36:15 GMT  
		Size: 2.4 MB (2395518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a6999cbf05638c0554accc7e8f9d8acd435888a52ad68267fcbd567d8fdce0`  
		Last Modified: Wed, 24 Jun 2026 01:36:14 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5f81262c7fc9478a7854e6dcf5e83a4d09732948b63b45b5d138da7fd57d8c`  
		Last Modified: Wed, 24 Jun 2026 01:36:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:1db8703b08d0d14737d40156d6a09384027af9d6806c94c63763d4b5cd08bc31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9df60db9b699e1540eb1b1a65a79dfffa825cdb8a5c9ce191b5cd53055af17e2`

```dockerfile
```

-	Layers:
	-	`sha256:d207552f6be1ed5a92472733946f240471025ee31516d22f4e4e1710136a5df9`  
		Last Modified: Wed, 24 Jun 2026 01:36:15 GMT  
		Size: 2.0 MB (2011969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2777dc1115238cc20388367ecc331281ddd19f28aafede9028ceb87baaf56ed`  
		Last Modified: Wed, 24 Jun 2026 01:36:14 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:1d09cc6da0fcd7fbfd1eb9a04ab9aeb8557f8a977d85bc7758ddc33f1fae7e8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30626877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e932fab34f25980444b8d9d4042f4f019d633ae41731c4d58de9d0425aacbb5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 20:53:15 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 20:53:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jun 2026 19:11:35 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 25 Jun 2026 19:11:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 25 Jun 2026 19:11:35 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 25 Jun 2026 19:11:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 25 Jun 2026 19:11:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 25 Jun 2026 19:11:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 25 Jun 2026 19:11:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Jun 2026 19:11:35 GMT
USER memcache
# Thu, 25 Jun 2026 19:11:35 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 25 Jun 2026 19:11:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:58bface994ba631e609596a2ca5032d9d75de27f1b6476034b581e226205adab`  
		Last Modified: Wed, 24 Jun 2026 03:41:42 GMT  
		Size: 28.3 MB (28282378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88be0d85b1f48be753592f62cac7ef80c23a61c7848026bd2d489c40d2214a58`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5924e63da94311a18a309f02e655774d7a7dd21bf3dc267215c524167fb7ca02`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 133.1 KB (133093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfa9af5e6df6f7145e6f80ab61869e6613b9f5caa0cfa94788cbf01b3041add`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 2.2 MB (2209890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ace1c66f882f3224670cc80ac0c47197433c688d59a6bad4e5e137d6947a7d9`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470dc087e4a89d9d58d8fa29a67ac089e3c4b569f1c1c79265bfe24ba39500d2`  
		Last Modified: Thu, 25 Jun 2026 19:12:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:10dc6cdb2cd2787d533382c9b0e6ae2f8f3b637c254e1b54762fc75d6b7c2066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173dffb05aa61f0096ec844832f392e17573e61865ef528ee8b742faa7e4b6db`

```dockerfile
```

-	Layers:
	-	`sha256:69ed82bb373c86c8fbec635b83221f89933079ee40e6fcf48418d1a69ca5bb89`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 2.0 MB (2002332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cea64cfdecc1c5a9f3c417e6a679e88cd0613790ff8f658ca9e3ec73325fa9cc`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:6bcf745c9e84c923ee6794f31fd61c321c07e98208661f8f96267b959b19322c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32291924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfeb11440a0b99b60cfece211ea4a2d19eb4c5aa0e27cc119d9930da48bb4a23`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:17:57 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:18:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:21:15 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:21:15 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:21:15 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:21:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:21:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:21:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:21:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:21:16 GMT
USER memcache
# Wed, 24 Jun 2026 01:21:16 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:21:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b6a0af2ceb4b698210b8776157288a3fb06e46aaf75d641139449fcc50ce430d`  
		Last Modified: Wed, 24 Jun 2026 00:28:43 GMT  
		Size: 29.9 MB (29851381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3bba39c5a45464aeb0d1fa775a329c0c537439ee4814281c4fc08a68d8cd584`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a60267637fa53d628133884b458b9c84464d66f87fb587bd54667d3e7c6c0f8`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 140.5 KB (140541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009a2f1905baeb2174621049e700d37eaaf68cda0912ab76762452f73537af8e`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 2.3 MB (2298488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5127e016f9d2a0554de486521914b692af85186039386e058a7e61c9754ef414`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf617d16473cca6af3500948111afc2fce546cd4db4d94441113555d9a9da08`  
		Last Modified: Wed, 24 Jun 2026 01:21:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:2721a3c701c85fd239ef39e576be9973f43c9655cc6cb66fd5bc3dc3ce206166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c4f64b3eb5d1eccd239a9a42a97ae1477a0b589f61e823181e9ab7271116da`

```dockerfile
```

-	Layers:
	-	`sha256:26bfdc43fc003330338d918e59f990463e9e8ceae7dbef48f43cdcb95e0f9b4e`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 2.0 MB (2009805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b9c877b5a220dabf32e1e097a3fb26dc36bad47b1978fb4b39ce7ae5415394f`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6`

```console
$ docker pull memcached@sha256:e2a8683c7fbb73d12dce8082525adf9df857765970e639bd9f4705acc31dfcba
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
$ docker pull memcached@sha256:3e079a2fc4232b10565b9bc19139292f16ef304297d4560f08f642f5f2d7a6a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32204836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ab1d39869e17aa04a25df4af0b5bf28a973d4f965635b067471bb44adbdc01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:21:34 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:21:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:24:28 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:24:28 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:24:28 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:24:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:24:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:24:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:24:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:24:28 GMT
USER memcache
# Wed, 24 Jun 2026 01:24:28 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:24:28 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1213ec9c2c2febafa221ff6195f27ea10c675acbc71d21fcc0d2b2ade3f5f74b`  
		Last Modified: Wed, 24 Jun 2026 01:24:34 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3266f17f87ca1b46b5c4fde9dd99707e3827b91b70059e7031ef53abd47fb12c`  
		Last Modified: Wed, 24 Jun 2026 01:24:34 GMT  
		Size: 136.7 KB (136688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a006226c9ea4b6f900685ceec0bda7162e03f436f1b312db9c6ba0d5b47919c7`  
		Last Modified: Wed, 24 Jun 2026 01:24:35 GMT  
		Size: 2.3 MB (2281216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3fd586859c95b544309532471aaabcf797408c5d017bd900b8e4c56c911367`  
		Last Modified: Wed, 24 Jun 2026 01:24:34 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2160167316cd327104547209c9d482373032078e07bb8a6a1e807f7e415571`  
		Last Modified: Wed, 24 Jun 2026 01:24:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:78b554b9b0edb7e45697fbdc7fb7bd3b9facbf500f3f955b3e21628a2469b659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97077f9e00ac4cde9ecb4dba83482ab83cfb8c9378171bf96fc076cc86a64a7`

```dockerfile
```

-	Layers:
	-	`sha256:0f81896f32bd3f922ecc9c3921e78406158e32af9b86b0bc711b5381f977f1e1`  
		Last Modified: Wed, 24 Jun 2026 01:24:35 GMT  
		Size: 2.0 MB (2008368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2714f45af9d9661f076eb378c43b8c30b2b1556e38d5573a646c9df3faae7740`  
		Last Modified: Wed, 24 Jun 2026 01:24:34 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:07d3a299e990256fef486b7259267b9140a71a6003c6b138f0629c06e8eab05a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30316687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3763f93158d93525ae099ec31b8c33c6f309d88e3e96f8e6e18ba87c3f5c18`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:14:31 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:14:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:17:52 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:17:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:17:52 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:17:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:17:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:17:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:17:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:17:52 GMT
USER memcache
# Wed, 24 Jun 2026 01:17:52 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:17:52 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:da43bc6a07a9cd7cc23faa538adc0797482747316b5a85b9f3f94ed17f6c1a2a`  
		Last Modified: Wed, 24 Jun 2026 00:28:12 GMT  
		Size: 28.0 MB (27959221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72b0a4d36a2a621f7921b07bce6fd125f5f5dcef47bd823dc4e31290e3e2399`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4e24ea733891c84a840e31af3fb0b9c15056a407cdc805d54c8cfd3e6ef6f0`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 144.2 KB (144157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64639d0df1b35e7dbd196efee0fd423d0a736ac6c863e17f7d6986420c041af8`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 2.2 MB (2211796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090c9d3495cd22555152f5b251e3f1fe30e588646fcac43f30a778eb73470f8e`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02db167b638147d6fc9f87b04a310ffd4b96fc41da3f61194b9525811486129`  
		Last Modified: Wed, 24 Jun 2026 01:18:00 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:b276ce09ef33302e7b98984a8b1515cd0c83190274b6163f2a28f2d539cc4a7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:390cd34082323b589abd9a85a9cf2513c80fd64085a0a6aa744e0b297aa7a4b5`

```dockerfile
```

-	Layers:
	-	`sha256:259590638c0e780d766f685e7f3a057b89c4575e1736e106d88bcbd2e7c345cb`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 2.0 MB (2011371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd7d6f82a916ba666327037ebdcdce8491adee8668fde99a67161383e1bdaf64`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v7

```console
$ docker pull memcached@sha256:e2be04c60636f94c2c1555f324fd58c8ed1cca98bfc5721d5d00a8357a7df461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28513245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc5b22192f1fe06b621ee612a1428f71028d4702873f593a6e3f1896b5c7edfd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:19:26 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:19:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:22:38 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:22:38 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:22:38 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:22:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:22:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:22:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:22:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:22:38 GMT
USER memcache
# Wed, 24 Jun 2026 01:22:38 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:22:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:81c84b0273952340067af970e1fe77a42ea83b4ed1a53319e258d5f1077848f0`  
		Last Modified: Wed, 24 Jun 2026 00:28:38 GMT  
		Size: 26.2 MB (26211051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0642cf323abcb26caa4c3ff3b7e80d0d7d6d9f6d9d9accdcf6d336f41426f102`  
		Last Modified: Wed, 24 Jun 2026 01:22:44 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2360e1299ad9a74124543c81dfb5655cf827191bca3b68df2bfa35cef12ff4c6`  
		Last Modified: Wed, 24 Jun 2026 01:22:44 GMT  
		Size: 135.4 KB (135381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa1e7d2a4dedc5e64f5906cba5d754b8a704705fc6875aa2c6e19fbf32e80d0`  
		Last Modified: Wed, 24 Jun 2026 01:22:45 GMT  
		Size: 2.2 MB (2165300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1110dbe0eb2a934122b522315e135c97a24e58dfe0d85799fa581bed83010517`  
		Last Modified: Wed, 24 Jun 2026 01:22:44 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6a4eee2665c4591534d0fb4f767664091dd2025201db5c28be41b6cde451d4`  
		Last Modified: Wed, 24 Jun 2026 01:22:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:69daaf7d08ee571ea31fa5ba2bbed9ee75e05eaa0e828fec25bcbbb5db45e674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ce76762dc893723cf043776255f735aa512c188d67735932b74d4347be6e02d`

```dockerfile
```

-	Layers:
	-	`sha256:bd51ee9d8e158fbc8c58b5d3ec9bb91d9e9adb533d51ef67ba795e241a2a1486`  
		Last Modified: Wed, 24 Jun 2026 01:22:45 GMT  
		Size: 2.0 MB (2009828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce07aa39f2cbf08f3885676ecfd34bf02f971dd10ba62db2f161f39e032df30d`  
		Last Modified: Wed, 24 Jun 2026 01:22:44 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ce9daf8b2144b701cf7e968ab341768bb2d3efa2a4c64d02da0a0de42c56f1bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32566611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cc2b42a078d89f4b7328abbd61b2cc235e3c733db4c018c8c232c8e3c8dac40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:22:00 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:22:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:25:00 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:25:00 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:25:00 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:25:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:25:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:25:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:25:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:25:00 GMT
USER memcache
# Wed, 24 Jun 2026 01:25:00 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:25:00 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45863abe59cf630e20caf87380378a813615419b3e0f3a8f6649855538dd606`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b7dfd57d8e29e17a7f5191adae69420144fe599879e351b48979971c36f465`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 153.5 KB (153487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be9b72bcf7171564f265414becff9bc077025e30b3f602008e49e51af592400`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 2.3 MB (2263062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff542c356a684239a022d62e5a51aa3f8884a5a1c5a7125cd5d4133c8bac04a`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf0b844cb30e05fdae9181c546555144b913389d03c3ed5549c809d6d4f5cb5`  
		Last Modified: Wed, 24 Jun 2026 01:25:07 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:4b6ea06e8e33c13f6ed836c0f565b1bb81217e79880acaac6b7ad6c4ae57a35d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d49fd2b1e37fca3ad0e2c2747ad1ffa5e40f4dac971d3d382bb685ad2cbeb75`

```dockerfile
```

-	Layers:
	-	`sha256:0749a7c57e354ea8640b297fd510a9c6b05145e740a4d1747f3d832d71878a63`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 2.0 MB (2008676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31dad526561e0628b5270544aa1a9c883fbecd2e25a9770bf262407c2e0bf810`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; 386

```console
$ docker pull memcached@sha256:b2916cadce1269827ce2769d75e850a06fa02e2b29d606a5300c10859def3696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33675687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c903111eaced6eb842f558accf95d8d210049b93dfdce69195cb596a9295aa2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:17:36 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:17:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:20:39 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:20:39 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:20:39 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:20:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:20:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:20:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:20:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:20:39 GMT
USER memcache
# Wed, 24 Jun 2026 01:20:39 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:20:39 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:984d3baa100eb8c4d7c83b7c23b4748e508aa6ed5903297f02be90a681f52d41`  
		Last Modified: Wed, 24 Jun 2026 00:28:38 GMT  
		Size: 31.3 MB (31301210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e88a5ba508193f8a40b67d411ba88b51522122e991c5e579f718f03a7b827d5`  
		Last Modified: Wed, 24 Jun 2026 01:20:45 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13a37bd401d9e6fe5c150251a68821160273feb13462cbe401715d4c50bbcee`  
		Last Modified: Wed, 24 Jun 2026 01:20:45 GMT  
		Size: 147.5 KB (147522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f7f30bf297b5062f967e9d807b67dbfcbd20800b75c6daae0ad7fff1edf46e`  
		Last Modified: Wed, 24 Jun 2026 01:20:46 GMT  
		Size: 2.2 MB (2225442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1687fae458633e2c28615b4a2b32841cea0191dc6777aa4ad23de450a9f898e4`  
		Last Modified: Wed, 24 Jun 2026 01:20:45 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc431901c24b9ea4ccb36149baa5b10a412da5738b7f7af9808c7a408caebc12`  
		Last Modified: Wed, 24 Jun 2026 01:20:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:ceb7723388cb240f2eff890796603dfa6d63cb5e7f9e9774cf291a70411779ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596e979ff6ae6cf65094d2e268ad30ecd052f4cb73e4dddeb3644a8b5d4e00b7`

```dockerfile
```

-	Layers:
	-	`sha256:f42e4ebf214a33a305d64952d73fd7dd183f7a9b3c1ee3618be109170351a6f2`  
		Last Modified: Wed, 24 Jun 2026 01:20:45 GMT  
		Size: 2.0 MB (2005525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd85722eeac2901ebcdc4b4970759b139e69583f42cc4b4f5f84fc21347082c0`  
		Last Modified: Wed, 24 Jun 2026 01:20:45 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:f26a6eb2688cfd1f4cf236c411f9988f840b8e69f0d81f925c8c5b375608a5b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36173798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683edb23fb2832c336aa1334780707e8e429ee767b084b9c4ebf1a76eee13670`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:32:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:32:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:35:52 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:35:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:35:52 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:35:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:35:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:35:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:35:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:35:52 GMT
USER memcache
# Wed, 24 Jun 2026 01:35:52 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:35:52 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:639e1c13483ea279c94219be2736856262d8dd2efeff3e6d309f11a66aba21fb`  
		Last Modified: Wed, 24 Jun 2026 00:30:29 GMT  
		Size: 33.6 MB (33606388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d700e36837a63da25a34bd9fef9f7937541cbe617e8c1e9c4a785cc37d6e2e29`  
		Last Modified: Wed, 24 Jun 2026 01:36:14 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7456d8868d48e0b53288836b26930c6efe02b67c099dcefa481778870fc15df`  
		Last Modified: Wed, 24 Jun 2026 01:36:15 GMT  
		Size: 170.4 KB (170375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7daaa467c3a42eb0ea458c5771839433b7c4f773537351a10e30789f995f63`  
		Last Modified: Wed, 24 Jun 2026 01:36:15 GMT  
		Size: 2.4 MB (2395518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a6999cbf05638c0554accc7e8f9d8acd435888a52ad68267fcbd567d8fdce0`  
		Last Modified: Wed, 24 Jun 2026 01:36:14 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5f81262c7fc9478a7854e6dcf5e83a4d09732948b63b45b5d138da7fd57d8c`  
		Last Modified: Wed, 24 Jun 2026 01:36:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:1db8703b08d0d14737d40156d6a09384027af9d6806c94c63763d4b5cd08bc31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9df60db9b699e1540eb1b1a65a79dfffa825cdb8a5c9ce191b5cd53055af17e2`

```dockerfile
```

-	Layers:
	-	`sha256:d207552f6be1ed5a92472733946f240471025ee31516d22f4e4e1710136a5df9`  
		Last Modified: Wed, 24 Jun 2026 01:36:15 GMT  
		Size: 2.0 MB (2011969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2777dc1115238cc20388367ecc331281ddd19f28aafede9028ceb87baaf56ed`  
		Last Modified: Wed, 24 Jun 2026 01:36:14 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; riscv64

```console
$ docker pull memcached@sha256:1d09cc6da0fcd7fbfd1eb9a04ab9aeb8557f8a977d85bc7758ddc33f1fae7e8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30626877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e932fab34f25980444b8d9d4042f4f019d633ae41731c4d58de9d0425aacbb5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 20:53:15 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 20:53:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jun 2026 19:11:35 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 25 Jun 2026 19:11:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 25 Jun 2026 19:11:35 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 25 Jun 2026 19:11:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 25 Jun 2026 19:11:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 25 Jun 2026 19:11:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 25 Jun 2026 19:11:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Jun 2026 19:11:35 GMT
USER memcache
# Thu, 25 Jun 2026 19:11:35 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 25 Jun 2026 19:11:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:58bface994ba631e609596a2ca5032d9d75de27f1b6476034b581e226205adab`  
		Last Modified: Wed, 24 Jun 2026 03:41:42 GMT  
		Size: 28.3 MB (28282378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88be0d85b1f48be753592f62cac7ef80c23a61c7848026bd2d489c40d2214a58`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5924e63da94311a18a309f02e655774d7a7dd21bf3dc267215c524167fb7ca02`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 133.1 KB (133093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfa9af5e6df6f7145e6f80ab61869e6613b9f5caa0cfa94788cbf01b3041add`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 2.2 MB (2209890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ace1c66f882f3224670cc80ac0c47197433c688d59a6bad4e5e137d6947a7d9`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470dc087e4a89d9d58d8fa29a67ac089e3c4b569f1c1c79265bfe24ba39500d2`  
		Last Modified: Thu, 25 Jun 2026 19:12:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:10dc6cdb2cd2787d533382c9b0e6ae2f8f3b637c254e1b54762fc75d6b7c2066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173dffb05aa61f0096ec844832f392e17573e61865ef528ee8b742faa7e4b6db`

```dockerfile
```

-	Layers:
	-	`sha256:69ed82bb373c86c8fbec635b83221f89933079ee40e6fcf48418d1a69ca5bb89`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 2.0 MB (2002332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cea64cfdecc1c5a9f3c417e6a679e88cd0613790ff8f658ca9e3ec73325fa9cc`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; s390x

```console
$ docker pull memcached@sha256:6bcf745c9e84c923ee6794f31fd61c321c07e98208661f8f96267b959b19322c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32291924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfeb11440a0b99b60cfece211ea4a2d19eb4c5aa0e27cc119d9930da48bb4a23`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:17:57 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:18:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:21:15 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:21:15 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:21:15 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:21:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:21:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:21:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:21:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:21:16 GMT
USER memcache
# Wed, 24 Jun 2026 01:21:16 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:21:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b6a0af2ceb4b698210b8776157288a3fb06e46aaf75d641139449fcc50ce430d`  
		Last Modified: Wed, 24 Jun 2026 00:28:43 GMT  
		Size: 29.9 MB (29851381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3bba39c5a45464aeb0d1fa775a329c0c537439ee4814281c4fc08a68d8cd584`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a60267637fa53d628133884b458b9c84464d66f87fb587bd54667d3e7c6c0f8`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 140.5 KB (140541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009a2f1905baeb2174621049e700d37eaaf68cda0912ab76762452f73537af8e`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 2.3 MB (2298488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5127e016f9d2a0554de486521914b692af85186039386e058a7e61c9754ef414`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf617d16473cca6af3500948111afc2fce546cd4db4d94441113555d9a9da08`  
		Last Modified: Wed, 24 Jun 2026 01:21:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:2721a3c701c85fd239ef39e576be9973f43c9655cc6cb66fd5bc3dc3ce206166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c4f64b3eb5d1eccd239a9a42a97ae1477a0b589f61e823181e9ab7271116da`

```dockerfile
```

-	Layers:
	-	`sha256:26bfdc43fc003330338d918e59f990463e9e8ceae7dbef48f43cdcb95e0f9b4e`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 2.0 MB (2009805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b9c877b5a220dabf32e1e097a3fb26dc36bad47b1978fb4b39ce7ae5415394f`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine`

```console
$ docker pull memcached@sha256:7381333da6d6ae06e02d8dfc87ee6f2c7cd0a19f7ba048d5efc538d2100e2208
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
$ docker pull memcached@sha256:ce375dd48f976d33bf35beb966cc37f202fd840a90891e58b9e71171fc74174d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5921579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d284e7a8445d8dc70e97c673a8a0175d18f39d5336ccbdfa8b240c0ef3ce4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:15:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:15:18 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:54 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:54 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:54 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb73756dcbbebc424eab53d3adda4d9f64001e7a91272a7b2a834622c08b093`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f0d6a5291334f2b54ec652193cd4e17ee22455b2f3ff3bd9b66acff6436c7b`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 106.1 KB (106066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ac11a8307528096ac745e0ef681b64854bbd012ffdfbce85587153eec73563`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 2.0 MB (1967772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3626493aad85d70a212bc66e9d45db8aef43b4bc662259563f916398165f1e64`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cdcd3f20e3aa439838f5491e6f457a42bad6c80ed9b099313bf79b57a721ea8`  
		Last Modified: Tue, 16 Jun 2026 00:18:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:bb948800301f1cae8e18e317f2b9e85636c86c4a1924ee85e125da37cb1333e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c3e084937eb543038244e151b03b8d9a0dce0b4d5bf87c2d471fa397ed5702`

```dockerfile
```

-	Layers:
	-	`sha256:9d05a792212c92363a76bb6a8205a6e7f386113b3efc1b5d600f93d4e237c975`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 94.9 KB (94897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee0e7e70ef03205f55c68bc1b74ac7854183aee4e871112794975dc852761b19`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:4b144cdbc67c11035b3d0f0c812b590ee694977f2f6a32321e538237bd2f841c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5573158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e9bb70df1535a2f8ca960f733a4404cbde900a13156a1f4446c2fd110258e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:25 GMT
ADD alpine-minirootfs-3.24.1-armhf.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:25 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:14:43 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:14:44 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:47 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:47 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3c4836a46d600cfe9a422adf7a80205cb534097e6213325e0176c51f6e5cc02e`  
		Last Modified: Sun, 14 Jun 2026 06:44:57 GMT  
		Size: 3.6 MB (3553450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e732a60042adf5cff5fe4fe0de83f937f6e5c8896500f7023e8bf68ed0670d65`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad86d1fea29db061a5ae896a0a595b144edcdb4af59deac2b75b0fb8f5fa2d4c`  
		Last Modified: Tue, 16 Jun 2026 00:17:50 GMT  
		Size: 102.6 KB (102624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f26dd2445dbf4d5624417ca290f5ae2e5774fa7fec4f5655cd2377ee3147e4`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 1.9 MB (1915730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080a186f0ca6beb06a5ce4a86fbc71f5b9995713fcc899c73f995f251ef7c987`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c4d4f455f9a2b633cca28e3aa2190e4c42ca83ca6e3ea88ea4abe16944d238`  
		Last Modified: Tue, 16 Jun 2026 00:17:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d6b7abf6ef34abf12ab2c7f84bd29ac2461eb3271d1c4070456ed9b94e4b41a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a767571287c8ca227e321ee8d65f9da82e558098bedbb15888434dcc1ce9fa`

```dockerfile
```

-	Layers:
	-	`sha256:1794ccef4392c0db4ba36ad7fde22cdacbda40f4d56f0adbef802163c87e066c`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:848c5e0ced69b802cca72c23bec05a4c6f23136212a4a1d5cc22b7c8f0154bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286f62a53a8947036e39f2b79567b31d38309fd84c7a39e43de8c5f9817a2f64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:26 GMT
ADD alpine-minirootfs-3.24.1-armv7.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:17:59 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:17:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:20:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:20:56 GMT
USER memcache
# Tue, 16 Jun 2026 00:20:56 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:20:56 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bc03a9e5b4dd452551f246e199537fe7afc1765f53f510bc81d26df9845e4008`  
		Last Modified: Sun, 14 Jun 2026 06:45:22 GMT  
		Size: 3.3 MB (3260615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f0249bacfc8953b72899bf7b6c904c8750482fce4c93108f57b2c64228b279`  
		Last Modified: Tue, 16 Jun 2026 00:21:00 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95e1b321ffc31d01e766d5d1d054967d613940563406fc54ee981926b7f6049`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 92.4 KB (92366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce112e60c1b15077277c233a7707831818dff0a15f1fc977ebebc93f817dad43`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 1.9 MB (1875183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32fa6ed5b14fd6fcf96a7cde2996063f10b8efe802c386479288a232af826027`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6648f8180a4eea1f5197f2fa2d356fbbf4e5f65345e189e720e227af64a5e31`  
		Last Modified: Tue, 16 Jun 2026 00:21:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:59387f31eff7cfb3166c5e6d4bad92e255705affcc15c84c4a06c86ecb1a9890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:174eb460b1df4523a4f71ba5a996f2285fa845fe8ef76d2df3ea8c4962c6b6ca`

```dockerfile
```

-	Layers:
	-	`sha256:4ff5e70775e819cab551295c56b58fdb0c44c105cdc4f72247e3968accd2ab2f`  
		Last Modified: Tue, 16 Jun 2026 00:21:00 GMT  
		Size: 94.3 KB (94315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00f10e1301c7e61396658f7e3ed330e400a9f304c6a0323de8ff644aba987474`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:33261748facce282dbe4dbb4d9f875139680fce4cefc13cb9ad8e1ced23f9557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6250475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1614bb2865c8f849c2bc5bf77703a1ab711695c607a8bc6edb013a076ec16d6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:18 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:16:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:16:06 GMT
USER memcache
# Tue, 16 Jun 2026 00:16:06 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:16:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5faa19f06c4d5e26332739c7f08fd3dcd2c81817471c62029a6d99af6be8748`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377a35d28f00766e2679c788b95b0a67b9aa5a76c8ef701a2a9604e2a00c3b46`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 121.8 KB (121841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0b819e89558d70f1401ca58cbc19c58ae13e15be8184fd9b2733e022f318a4`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 1.9 MB (1944247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca539cef48ff8c3f723ab23506b6786c9ed26a9cac713601b71de2dc775d26a`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4c456deed244daa6d7076f40a1cf0364d294059bb43e533677a89027843b15`  
		Last Modified: Tue, 16 Jun 2026 00:16:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:4d25960abc53b5ba1896b8f5ee04ba5ac1389900ab9b413eb62285af7281aedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d1a4b7ad428a08c8a174d5ecd9763d530e849f54a2d9b90aef934e54b9477d4`

```dockerfile
```

-	Layers:
	-	`sha256:9c0a8e5e07390fae6abe9204450009671011c4d2d5aa5fe4afdd82324fdb49b9`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 94.4 KB (94351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ee01158358d01c082867cf46a5225cf101013e4d5b7eae18fc7853e277ff0f4`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 20.7 KB (20727 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:5436d0ef6e12f2f8e454384ff4a703132b3fe820c41a55336f520bb5d1622574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5702329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8946be3d97c7b9825159f58cbf832b131c75cb90b3fb46a40d5429b9ffe32bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:19 GMT
ADD alpine-minirootfs-3.24.1-x86.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:19 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:59 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:16:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:16:46 GMT
USER memcache
# Tue, 16 Jun 2026 00:16:46 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:16:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f86df9d778509895efbf9363d8fcb0cbe0b772de536c7218e4c4c947f0be879f`  
		Last Modified: Sun, 14 Jun 2026 06:45:46 GMT  
		Size: 3.7 MB (3670141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043137360442e605bc150f28f20e1fa2d23d90131370bc405ad7d35309594491`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900ce6eeaece12033b12f1c8641c33dcf62ff2525584411911368cfcd0b38224`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 110.7 KB (110729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e8cc1c8f6bc6391eb1a43a46f0b55ca7845f824fc0f2fc7ae7587a7715814e`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 1.9 MB (1920111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94f6e4d3be92188fc182a3557fe43af5bc9f3e768a7f265977743a56eea527e`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f8a19f18dfff271426de7a17ab6780788fa4345d5fa0120e6d03720d552bd4`  
		Last Modified: Tue, 16 Jun 2026 00:16:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:00dc6a7f29b7f2f5ac46fc5678b80c43c7b1e46b4ca3c84c5597034180aeb644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de04019c7775544db9adbb4c4558d0e7c842c279e5d70532b2ac0b988ac1345`

```dockerfile
```

-	Layers:
	-	`sha256:80895f8f5e9c9b015e419096426322f4c86c33d55ca8860ee046b61d52782847`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 94.9 KB (94852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c69be8c1f82a066b46cc389712508e85c1dcd77e649c922dba46ace64b343ae`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:c7857941a51b85b136781035703afcc8854a2d70fa2091208a51f8bb7e71f934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5998515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b02b2222212c64e444ac1a2227b19f0cfb1282c8a8ced386c1b79ae48c641b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:15 GMT
ADD alpine-minirootfs-3.24.1-ppc64le.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:15 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:15:37 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:15:38 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:18:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:18:22 GMT
USER memcache
# Tue, 16 Jun 2026 00:18:22 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:18:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3ebcdcd395ccee658b9200e4b27d7699e5d6ed9f6c1858dea12781aac519ff59`  
		Last Modified: Sun, 14 Jun 2026 06:46:36 GMT  
		Size: 3.8 MB (3813400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b108e2058722fb0fb5a9310e8ebe82ab4b9c021228a94b3125ba49d318e9667`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb8160ed736eda8513164d5d703082fb0c9af9e037472ab70a02579caa3eb99`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 126.3 KB (126252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5cb88dd03ce07ecf1613c2aff220fb392763d8f22edc900c4ad032ee7103d34`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 2.1 MB (2057508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12fd57420ca797ab383c58a488044d324c4d43b3c94a848f86a0524ed3064b4`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c0c7b7a77e9375d8a75fb825fa274d9127ca96de79107550517be29501c817`  
		Last Modified: Tue, 16 Jun 2026 00:18:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:851f463d4778539d5e4981f972420f9a57ec2559488f8a59fba6abab6065032f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734dd3d91f2d6cf217233f7a9dacc3c20ff0590246adb790f95713fb21c115de`

```dockerfile
```

-	Layers:
	-	`sha256:c0d4c203ef9f66cf827ec62098d7801e1c49f1187e0fe047fd32fc2a3271f636`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 94.3 KB (94304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b734d170b5463fa77dd77072e06d51a28efe59a53600d47435b015ebcadae92`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:ba5bf40b4adc1fe04f32e2e239fa9c0020d4e89bf4079493f8bc11a92c8f4b51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5738070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d12fbf86d6880aaa9d517425d9cecddcf545ba87e577a039dea9ea99ad53d8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 05:59:15 GMT
ADD alpine-minirootfs-3.24.1-riscv64.tar.gz / # buildkit
# Tue, 16 Jun 2026 05:59:15 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 08:28:27 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 19 Jun 2026 08:28:31 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_VERSION=1.6.42
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Fri, 19 Jun 2026 08:41:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 19 Jun 2026 08:41:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 08:41:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 19 Jun 2026 08:41:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 08:41:53 GMT
USER memcache
# Fri, 19 Jun 2026 08:41:53 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 19 Jun 2026 08:41:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c34e5222b29b86391cdae95b0473ef789493ff1a0068a3a30b5d66f544bd7cf6`  
		Last Modified: Sun, 14 Jun 2026 06:47:00 GMT  
		Size: 3.6 MB (3574358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09d95a0f414638430c0cd3ecfdcce75606201917a27c7cb2ce1e34cb928b26a`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5335c7af79a1b08af55862ba77644afdae5544d9a7871e45c91b364bd4f71d`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 108.9 KB (108888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3622a6ea71515db1ef566afdbb121daed1f408aacf1519f4173b40dabe2ae627`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 2.1 MB (2053467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1db0e3e31ca3f2830f5404436e92b1862a4078adefacacec09a9580a3ad0a2`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1463b0fd26a37659aaad7f99696e5213764ad03bb094f40836c3309713d7a60`  
		Last Modified: Fri, 19 Jun 2026 08:42:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:aadb3b9338400b87692f95e00931e43940f8d6ddd13f046bd256848dd825e458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde4b5a4a468d795a5f58dd934b371adfe72cd2ae24e166e1258ad65aa455a56`

```dockerfile
```

-	Layers:
	-	`sha256:debb70180cf674562f7ca321270e3dfa350c5d1596c05dbfcc27b38c65652528`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 94.3 KB (94300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a895bbe0bfec24678c1c92ddd283cb7392e0e8d229f31c769a23c95224c0d371`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:e1b640e8d192055e5c3ccd05b077776a0f4d35664191596f7a8230b2cd7ef0f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5823313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ef6221f9c2854683b0633325a98a0e7a0d3b7d865b02d7cdf4c1d49d2e5090`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:21 GMT
ADD alpine-minirootfs-3.24.1-s390x.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:21 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:46 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:12 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:da43be6afaaa3ec1b607461ce64380942a6d76c3d52cda4337b0770d9a96fa89`  
		Last Modified: Sun, 14 Jun 2026 06:47:25 GMT  
		Size: 3.7 MB (3709320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757d04238e02c9bbe1cfd4030cc19e29421650a1b1562a8ca4090d90e9ae17b0`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1949e0fa71fc91bebf4f2e4293108b27de8357d98f98b673bc4f3ed1980b52c`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 114.3 KB (114289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f0e22966bce79fbc8a20f7c27aa07ce63229bb50181319c810ca29f1fb4032`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 2.0 MB (1998350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15eb5e912ef8ec6e3abe76c361cdddb568d20a60be21be379d4d8d7d0ebaa11e`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a549d59ad0d4761ac6f4cca272c4bea521471ed091d0e79143bfda8ff29cf9ce`  
		Last Modified: Tue, 16 Jun 2026 00:17:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:6dbf7c8a98f02a949769403ad1c92583b34a28dccc66b7d83d91863785a6dad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a89d23372d19daf2d6d4e1c4de732f7864316ed5e7713b1103918303873683e`

```dockerfile
```

-	Layers:
	-	`sha256:099ab2d711ef73783b01895824a4664c7d65e2a333e81237b4766cf053a8f6f0`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 94.2 KB (94246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eccbabf44891af00e622624c5cfd5a295656f82f1c15073b240ac34d47af96c`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine3.24`

```console
$ docker pull memcached@sha256:7381333da6d6ae06e02d8dfc87ee6f2c7cd0a19f7ba048d5efc538d2100e2208
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

### `memcached:1.6-alpine3.24` - linux; amd64

```console
$ docker pull memcached@sha256:ce375dd48f976d33bf35beb966cc37f202fd840a90891e58b9e71171fc74174d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5921579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d284e7a8445d8dc70e97c673a8a0175d18f39d5336ccbdfa8b240c0ef3ce4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:15:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:15:18 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:54 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:54 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:54 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb73756dcbbebc424eab53d3adda4d9f64001e7a91272a7b2a834622c08b093`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f0d6a5291334f2b54ec652193cd4e17ee22455b2f3ff3bd9b66acff6436c7b`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 106.1 KB (106066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ac11a8307528096ac745e0ef681b64854bbd012ffdfbce85587153eec73563`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 2.0 MB (1967772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3626493aad85d70a212bc66e9d45db8aef43b4bc662259563f916398165f1e64`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cdcd3f20e3aa439838f5491e6f457a42bad6c80ed9b099313bf79b57a721ea8`  
		Last Modified: Tue, 16 Jun 2026 00:18:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:bb948800301f1cae8e18e317f2b9e85636c86c4a1924ee85e125da37cb1333e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c3e084937eb543038244e151b03b8d9a0dce0b4d5bf87c2d471fa397ed5702`

```dockerfile
```

-	Layers:
	-	`sha256:9d05a792212c92363a76bb6a8205a6e7f386113b3efc1b5d600f93d4e237c975`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 94.9 KB (94897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee0e7e70ef03205f55c68bc1b74ac7854183aee4e871112794975dc852761b19`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.24` - linux; arm variant v6

```console
$ docker pull memcached@sha256:4b144cdbc67c11035b3d0f0c812b590ee694977f2f6a32321e538237bd2f841c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5573158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e9bb70df1535a2f8ca960f733a4404cbde900a13156a1f4446c2fd110258e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:25 GMT
ADD alpine-minirootfs-3.24.1-armhf.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:25 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:14:43 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:14:44 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:47 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:47 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3c4836a46d600cfe9a422adf7a80205cb534097e6213325e0176c51f6e5cc02e`  
		Last Modified: Sun, 14 Jun 2026 06:44:57 GMT  
		Size: 3.6 MB (3553450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e732a60042adf5cff5fe4fe0de83f937f6e5c8896500f7023e8bf68ed0670d65`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad86d1fea29db061a5ae896a0a595b144edcdb4af59deac2b75b0fb8f5fa2d4c`  
		Last Modified: Tue, 16 Jun 2026 00:17:50 GMT  
		Size: 102.6 KB (102624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f26dd2445dbf4d5624417ca290f5ae2e5774fa7fec4f5655cd2377ee3147e4`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 1.9 MB (1915730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080a186f0ca6beb06a5ce4a86fbc71f5b9995713fcc899c73f995f251ef7c987`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c4d4f455f9a2b633cca28e3aa2190e4c42ca83ca6e3ea88ea4abe16944d238`  
		Last Modified: Tue, 16 Jun 2026 00:17:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:d6b7abf6ef34abf12ab2c7f84bd29ac2461eb3271d1c4070456ed9b94e4b41a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a767571287c8ca227e321ee8d65f9da82e558098bedbb15888434dcc1ce9fa`

```dockerfile
```

-	Layers:
	-	`sha256:1794ccef4392c0db4ba36ad7fde22cdacbda40f4d56f0adbef802163c87e066c`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.24` - linux; arm variant v7

```console
$ docker pull memcached@sha256:848c5e0ced69b802cca72c23bec05a4c6f23136212a4a1d5cc22b7c8f0154bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286f62a53a8947036e39f2b79567b31d38309fd84c7a39e43de8c5f9817a2f64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:26 GMT
ADD alpine-minirootfs-3.24.1-armv7.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:17:59 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:17:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:20:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:20:56 GMT
USER memcache
# Tue, 16 Jun 2026 00:20:56 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:20:56 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bc03a9e5b4dd452551f246e199537fe7afc1765f53f510bc81d26df9845e4008`  
		Last Modified: Sun, 14 Jun 2026 06:45:22 GMT  
		Size: 3.3 MB (3260615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f0249bacfc8953b72899bf7b6c904c8750482fce4c93108f57b2c64228b279`  
		Last Modified: Tue, 16 Jun 2026 00:21:00 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95e1b321ffc31d01e766d5d1d054967d613940563406fc54ee981926b7f6049`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 92.4 KB (92366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce112e60c1b15077277c233a7707831818dff0a15f1fc977ebebc93f817dad43`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 1.9 MB (1875183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32fa6ed5b14fd6fcf96a7cde2996063f10b8efe802c386479288a232af826027`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6648f8180a4eea1f5197f2fa2d356fbbf4e5f65345e189e720e227af64a5e31`  
		Last Modified: Tue, 16 Jun 2026 00:21:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:59387f31eff7cfb3166c5e6d4bad92e255705affcc15c84c4a06c86ecb1a9890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:174eb460b1df4523a4f71ba5a996f2285fa845fe8ef76d2df3ea8c4962c6b6ca`

```dockerfile
```

-	Layers:
	-	`sha256:4ff5e70775e819cab551295c56b58fdb0c44c105cdc4f72247e3968accd2ab2f`  
		Last Modified: Tue, 16 Jun 2026 00:21:00 GMT  
		Size: 94.3 KB (94315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00f10e1301c7e61396658f7e3ed330e400a9f304c6a0323de8ff644aba987474`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.24` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:33261748facce282dbe4dbb4d9f875139680fce4cefc13cb9ad8e1ced23f9557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6250475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1614bb2865c8f849c2bc5bf77703a1ab711695c607a8bc6edb013a076ec16d6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:18 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:16:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:16:06 GMT
USER memcache
# Tue, 16 Jun 2026 00:16:06 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:16:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5faa19f06c4d5e26332739c7f08fd3dcd2c81817471c62029a6d99af6be8748`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377a35d28f00766e2679c788b95b0a67b9aa5a76c8ef701a2a9604e2a00c3b46`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 121.8 KB (121841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0b819e89558d70f1401ca58cbc19c58ae13e15be8184fd9b2733e022f318a4`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 1.9 MB (1944247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca539cef48ff8c3f723ab23506b6786c9ed26a9cac713601b71de2dc775d26a`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4c456deed244daa6d7076f40a1cf0364d294059bb43e533677a89027843b15`  
		Last Modified: Tue, 16 Jun 2026 00:16:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:4d25960abc53b5ba1896b8f5ee04ba5ac1389900ab9b413eb62285af7281aedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d1a4b7ad428a08c8a174d5ecd9763d530e849f54a2d9b90aef934e54b9477d4`

```dockerfile
```

-	Layers:
	-	`sha256:9c0a8e5e07390fae6abe9204450009671011c4d2d5aa5fe4afdd82324fdb49b9`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 94.4 KB (94351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ee01158358d01c082867cf46a5225cf101013e4d5b7eae18fc7853e277ff0f4`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 20.7 KB (20727 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.24` - linux; 386

```console
$ docker pull memcached@sha256:5436d0ef6e12f2f8e454384ff4a703132b3fe820c41a55336f520bb5d1622574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5702329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8946be3d97c7b9825159f58cbf832b131c75cb90b3fb46a40d5429b9ffe32bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:19 GMT
ADD alpine-minirootfs-3.24.1-x86.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:19 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:59 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:16:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:16:46 GMT
USER memcache
# Tue, 16 Jun 2026 00:16:46 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:16:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f86df9d778509895efbf9363d8fcb0cbe0b772de536c7218e4c4c947f0be879f`  
		Last Modified: Sun, 14 Jun 2026 06:45:46 GMT  
		Size: 3.7 MB (3670141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043137360442e605bc150f28f20e1fa2d23d90131370bc405ad7d35309594491`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900ce6eeaece12033b12f1c8641c33dcf62ff2525584411911368cfcd0b38224`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 110.7 KB (110729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e8cc1c8f6bc6391eb1a43a46f0b55ca7845f824fc0f2fc7ae7587a7715814e`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 1.9 MB (1920111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94f6e4d3be92188fc182a3557fe43af5bc9f3e768a7f265977743a56eea527e`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f8a19f18dfff271426de7a17ab6780788fa4345d5fa0120e6d03720d552bd4`  
		Last Modified: Tue, 16 Jun 2026 00:16:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:00dc6a7f29b7f2f5ac46fc5678b80c43c7b1e46b4ca3c84c5597034180aeb644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de04019c7775544db9adbb4c4558d0e7c842c279e5d70532b2ac0b988ac1345`

```dockerfile
```

-	Layers:
	-	`sha256:80895f8f5e9c9b015e419096426322f4c86c33d55ca8860ee046b61d52782847`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 94.9 KB (94852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c69be8c1f82a066b46cc389712508e85c1dcd77e649c922dba46ace64b343ae`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.24` - linux; ppc64le

```console
$ docker pull memcached@sha256:c7857941a51b85b136781035703afcc8854a2d70fa2091208a51f8bb7e71f934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5998515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b02b2222212c64e444ac1a2227b19f0cfb1282c8a8ced386c1b79ae48c641b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:15 GMT
ADD alpine-minirootfs-3.24.1-ppc64le.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:15 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:15:37 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:15:38 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:18:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:18:22 GMT
USER memcache
# Tue, 16 Jun 2026 00:18:22 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:18:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3ebcdcd395ccee658b9200e4b27d7699e5d6ed9f6c1858dea12781aac519ff59`  
		Last Modified: Sun, 14 Jun 2026 06:46:36 GMT  
		Size: 3.8 MB (3813400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b108e2058722fb0fb5a9310e8ebe82ab4b9c021228a94b3125ba49d318e9667`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb8160ed736eda8513164d5d703082fb0c9af9e037472ab70a02579caa3eb99`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 126.3 KB (126252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5cb88dd03ce07ecf1613c2aff220fb392763d8f22edc900c4ad032ee7103d34`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 2.1 MB (2057508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12fd57420ca797ab383c58a488044d324c4d43b3c94a848f86a0524ed3064b4`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c0c7b7a77e9375d8a75fb825fa274d9127ca96de79107550517be29501c817`  
		Last Modified: Tue, 16 Jun 2026 00:18:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:851f463d4778539d5e4981f972420f9a57ec2559488f8a59fba6abab6065032f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734dd3d91f2d6cf217233f7a9dacc3c20ff0590246adb790f95713fb21c115de`

```dockerfile
```

-	Layers:
	-	`sha256:c0d4c203ef9f66cf827ec62098d7801e1c49f1187e0fe047fd32fc2a3271f636`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 94.3 KB (94304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b734d170b5463fa77dd77072e06d51a28efe59a53600d47435b015ebcadae92`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.24` - linux; riscv64

```console
$ docker pull memcached@sha256:ba5bf40b4adc1fe04f32e2e239fa9c0020d4e89bf4079493f8bc11a92c8f4b51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5738070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d12fbf86d6880aaa9d517425d9cecddcf545ba87e577a039dea9ea99ad53d8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 05:59:15 GMT
ADD alpine-minirootfs-3.24.1-riscv64.tar.gz / # buildkit
# Tue, 16 Jun 2026 05:59:15 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 08:28:27 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 19 Jun 2026 08:28:31 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_VERSION=1.6.42
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Fri, 19 Jun 2026 08:41:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 19 Jun 2026 08:41:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 08:41:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 19 Jun 2026 08:41:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 08:41:53 GMT
USER memcache
# Fri, 19 Jun 2026 08:41:53 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 19 Jun 2026 08:41:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c34e5222b29b86391cdae95b0473ef789493ff1a0068a3a30b5d66f544bd7cf6`  
		Last Modified: Sun, 14 Jun 2026 06:47:00 GMT  
		Size: 3.6 MB (3574358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09d95a0f414638430c0cd3ecfdcce75606201917a27c7cb2ce1e34cb928b26a`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5335c7af79a1b08af55862ba77644afdae5544d9a7871e45c91b364bd4f71d`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 108.9 KB (108888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3622a6ea71515db1ef566afdbb121daed1f408aacf1519f4173b40dabe2ae627`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 2.1 MB (2053467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1db0e3e31ca3f2830f5404436e92b1862a4078adefacacec09a9580a3ad0a2`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1463b0fd26a37659aaad7f99696e5213764ad03bb094f40836c3309713d7a60`  
		Last Modified: Fri, 19 Jun 2026 08:42:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:aadb3b9338400b87692f95e00931e43940f8d6ddd13f046bd256848dd825e458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde4b5a4a468d795a5f58dd934b371adfe72cd2ae24e166e1258ad65aa455a56`

```dockerfile
```

-	Layers:
	-	`sha256:debb70180cf674562f7ca321270e3dfa350c5d1596c05dbfcc27b38c65652528`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 94.3 KB (94300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a895bbe0bfec24678c1c92ddd283cb7392e0e8d229f31c769a23c95224c0d371`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.24` - linux; s390x

```console
$ docker pull memcached@sha256:e1b640e8d192055e5c3ccd05b077776a0f4d35664191596f7a8230b2cd7ef0f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5823313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ef6221f9c2854683b0633325a98a0e7a0d3b7d865b02d7cdf4c1d49d2e5090`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:21 GMT
ADD alpine-minirootfs-3.24.1-s390x.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:21 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:46 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:12 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:da43be6afaaa3ec1b607461ce64380942a6d76c3d52cda4337b0770d9a96fa89`  
		Last Modified: Sun, 14 Jun 2026 06:47:25 GMT  
		Size: 3.7 MB (3709320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757d04238e02c9bbe1cfd4030cc19e29421650a1b1562a8ca4090d90e9ae17b0`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1949e0fa71fc91bebf4f2e4293108b27de8357d98f98b673bc4f3ed1980b52c`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 114.3 KB (114289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f0e22966bce79fbc8a20f7c27aa07ce63229bb50181319c810ca29f1fb4032`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 2.0 MB (1998350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15eb5e912ef8ec6e3abe76c361cdddb568d20a60be21be379d4d8d7d0ebaa11e`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a549d59ad0d4761ac6f4cca272c4bea521471ed091d0e79143bfda8ff29cf9ce`  
		Last Modified: Tue, 16 Jun 2026 00:17:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:6dbf7c8a98f02a949769403ad1c92583b34a28dccc66b7d83d91863785a6dad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a89d23372d19daf2d6d4e1c4de732f7864316ed5e7713b1103918303873683e`

```dockerfile
```

-	Layers:
	-	`sha256:099ab2d711ef73783b01895824a4664c7d65e2a333e81237b4766cf053a8f6f0`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 94.2 KB (94246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eccbabf44891af00e622624c5cfd5a295656f82f1c15073b240ac34d47af96c`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-trixie`

```console
$ docker pull memcached@sha256:e2a8683c7fbb73d12dce8082525adf9df857765970e639bd9f4705acc31dfcba
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
$ docker pull memcached@sha256:3e079a2fc4232b10565b9bc19139292f16ef304297d4560f08f642f5f2d7a6a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32204836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ab1d39869e17aa04a25df4af0b5bf28a973d4f965635b067471bb44adbdc01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:21:34 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:21:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:24:28 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:24:28 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:24:28 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:24:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:24:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:24:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:24:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:24:28 GMT
USER memcache
# Wed, 24 Jun 2026 01:24:28 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:24:28 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1213ec9c2c2febafa221ff6195f27ea10c675acbc71d21fcc0d2b2ade3f5f74b`  
		Last Modified: Wed, 24 Jun 2026 01:24:34 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3266f17f87ca1b46b5c4fde9dd99707e3827b91b70059e7031ef53abd47fb12c`  
		Last Modified: Wed, 24 Jun 2026 01:24:34 GMT  
		Size: 136.7 KB (136688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a006226c9ea4b6f900685ceec0bda7162e03f436f1b312db9c6ba0d5b47919c7`  
		Last Modified: Wed, 24 Jun 2026 01:24:35 GMT  
		Size: 2.3 MB (2281216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3fd586859c95b544309532471aaabcf797408c5d017bd900b8e4c56c911367`  
		Last Modified: Wed, 24 Jun 2026 01:24:34 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2160167316cd327104547209c9d482373032078e07bb8a6a1e807f7e415571`  
		Last Modified: Wed, 24 Jun 2026 01:24:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:78b554b9b0edb7e45697fbdc7fb7bd3b9facbf500f3f955b3e21628a2469b659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97077f9e00ac4cde9ecb4dba83482ab83cfb8c9378171bf96fc076cc86a64a7`

```dockerfile
```

-	Layers:
	-	`sha256:0f81896f32bd3f922ecc9c3921e78406158e32af9b86b0bc711b5381f977f1e1`  
		Last Modified: Wed, 24 Jun 2026 01:24:35 GMT  
		Size: 2.0 MB (2008368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2714f45af9d9661f076eb378c43b8c30b2b1556e38d5573a646c9df3faae7740`  
		Last Modified: Wed, 24 Jun 2026 01:24:34 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:07d3a299e990256fef486b7259267b9140a71a6003c6b138f0629c06e8eab05a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30316687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3763f93158d93525ae099ec31b8c33c6f309d88e3e96f8e6e18ba87c3f5c18`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:14:31 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:14:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:17:52 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:17:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:17:52 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:17:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:17:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:17:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:17:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:17:52 GMT
USER memcache
# Wed, 24 Jun 2026 01:17:52 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:17:52 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:da43bc6a07a9cd7cc23faa538adc0797482747316b5a85b9f3f94ed17f6c1a2a`  
		Last Modified: Wed, 24 Jun 2026 00:28:12 GMT  
		Size: 28.0 MB (27959221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72b0a4d36a2a621f7921b07bce6fd125f5f5dcef47bd823dc4e31290e3e2399`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4e24ea733891c84a840e31af3fb0b9c15056a407cdc805d54c8cfd3e6ef6f0`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 144.2 KB (144157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64639d0df1b35e7dbd196efee0fd423d0a736ac6c863e17f7d6986420c041af8`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 2.2 MB (2211796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090c9d3495cd22555152f5b251e3f1fe30e588646fcac43f30a778eb73470f8e`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02db167b638147d6fc9f87b04a310ffd4b96fc41da3f61194b9525811486129`  
		Last Modified: Wed, 24 Jun 2026 01:18:00 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:b276ce09ef33302e7b98984a8b1515cd0c83190274b6163f2a28f2d539cc4a7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:390cd34082323b589abd9a85a9cf2513c80fd64085a0a6aa744e0b297aa7a4b5`

```dockerfile
```

-	Layers:
	-	`sha256:259590638c0e780d766f685e7f3a057b89c4575e1736e106d88bcbd2e7c345cb`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 2.0 MB (2011371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd7d6f82a916ba666327037ebdcdce8491adee8668fde99a67161383e1bdaf64`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:e2be04c60636f94c2c1555f324fd58c8ed1cca98bfc5721d5d00a8357a7df461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28513245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc5b22192f1fe06b621ee612a1428f71028d4702873f593a6e3f1896b5c7edfd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:19:26 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:19:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:22:38 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:22:38 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:22:38 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:22:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:22:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:22:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:22:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:22:38 GMT
USER memcache
# Wed, 24 Jun 2026 01:22:38 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:22:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:81c84b0273952340067af970e1fe77a42ea83b4ed1a53319e258d5f1077848f0`  
		Last Modified: Wed, 24 Jun 2026 00:28:38 GMT  
		Size: 26.2 MB (26211051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0642cf323abcb26caa4c3ff3b7e80d0d7d6d9f6d9d9accdcf6d336f41426f102`  
		Last Modified: Wed, 24 Jun 2026 01:22:44 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2360e1299ad9a74124543c81dfb5655cf827191bca3b68df2bfa35cef12ff4c6`  
		Last Modified: Wed, 24 Jun 2026 01:22:44 GMT  
		Size: 135.4 KB (135381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa1e7d2a4dedc5e64f5906cba5d754b8a704705fc6875aa2c6e19fbf32e80d0`  
		Last Modified: Wed, 24 Jun 2026 01:22:45 GMT  
		Size: 2.2 MB (2165300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1110dbe0eb2a934122b522315e135c97a24e58dfe0d85799fa581bed83010517`  
		Last Modified: Wed, 24 Jun 2026 01:22:44 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6a4eee2665c4591534d0fb4f767664091dd2025201db5c28be41b6cde451d4`  
		Last Modified: Wed, 24 Jun 2026 01:22:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:69daaf7d08ee571ea31fa5ba2bbed9ee75e05eaa0e828fec25bcbbb5db45e674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ce76762dc893723cf043776255f735aa512c188d67735932b74d4347be6e02d`

```dockerfile
```

-	Layers:
	-	`sha256:bd51ee9d8e158fbc8c58b5d3ec9bb91d9e9adb533d51ef67ba795e241a2a1486`  
		Last Modified: Wed, 24 Jun 2026 01:22:45 GMT  
		Size: 2.0 MB (2009828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce07aa39f2cbf08f3885676ecfd34bf02f971dd10ba62db2f161f39e032df30d`  
		Last Modified: Wed, 24 Jun 2026 01:22:44 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ce9daf8b2144b701cf7e968ab341768bb2d3efa2a4c64d02da0a0de42c56f1bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32566611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cc2b42a078d89f4b7328abbd61b2cc235e3c733db4c018c8c232c8e3c8dac40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:22:00 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:22:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:25:00 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:25:00 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:25:00 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:25:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:25:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:25:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:25:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:25:00 GMT
USER memcache
# Wed, 24 Jun 2026 01:25:00 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:25:00 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45863abe59cf630e20caf87380378a813615419b3e0f3a8f6649855538dd606`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b7dfd57d8e29e17a7f5191adae69420144fe599879e351b48979971c36f465`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 153.5 KB (153487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be9b72bcf7171564f265414becff9bc077025e30b3f602008e49e51af592400`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 2.3 MB (2263062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff542c356a684239a022d62e5a51aa3f8884a5a1c5a7125cd5d4133c8bac04a`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf0b844cb30e05fdae9181c546555144b913389d03c3ed5549c809d6d4f5cb5`  
		Last Modified: Wed, 24 Jun 2026 01:25:07 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:4b6ea06e8e33c13f6ed836c0f565b1bb81217e79880acaac6b7ad6c4ae57a35d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d49fd2b1e37fca3ad0e2c2747ad1ffa5e40f4dac971d3d382bb685ad2cbeb75`

```dockerfile
```

-	Layers:
	-	`sha256:0749a7c57e354ea8640b297fd510a9c6b05145e740a4d1747f3d832d71878a63`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 2.0 MB (2008676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31dad526561e0628b5270544aa1a9c883fbecd2e25a9770bf262407c2e0bf810`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; 386

```console
$ docker pull memcached@sha256:b2916cadce1269827ce2769d75e850a06fa02e2b29d606a5300c10859def3696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33675687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c903111eaced6eb842f558accf95d8d210049b93dfdce69195cb596a9295aa2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:17:36 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:17:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:20:39 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:20:39 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:20:39 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:20:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:20:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:20:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:20:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:20:39 GMT
USER memcache
# Wed, 24 Jun 2026 01:20:39 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:20:39 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:984d3baa100eb8c4d7c83b7c23b4748e508aa6ed5903297f02be90a681f52d41`  
		Last Modified: Wed, 24 Jun 2026 00:28:38 GMT  
		Size: 31.3 MB (31301210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e88a5ba508193f8a40b67d411ba88b51522122e991c5e579f718f03a7b827d5`  
		Last Modified: Wed, 24 Jun 2026 01:20:45 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13a37bd401d9e6fe5c150251a68821160273feb13462cbe401715d4c50bbcee`  
		Last Modified: Wed, 24 Jun 2026 01:20:45 GMT  
		Size: 147.5 KB (147522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f7f30bf297b5062f967e9d807b67dbfcbd20800b75c6daae0ad7fff1edf46e`  
		Last Modified: Wed, 24 Jun 2026 01:20:46 GMT  
		Size: 2.2 MB (2225442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1687fae458633e2c28615b4a2b32841cea0191dc6777aa4ad23de450a9f898e4`  
		Last Modified: Wed, 24 Jun 2026 01:20:45 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc431901c24b9ea4ccb36149baa5b10a412da5738b7f7af9808c7a408caebc12`  
		Last Modified: Wed, 24 Jun 2026 01:20:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:ceb7723388cb240f2eff890796603dfa6d63cb5e7f9e9774cf291a70411779ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596e979ff6ae6cf65094d2e268ad30ecd052f4cb73e4dddeb3644a8b5d4e00b7`

```dockerfile
```

-	Layers:
	-	`sha256:f42e4ebf214a33a305d64952d73fd7dd183f7a9b3c1ee3618be109170351a6f2`  
		Last Modified: Wed, 24 Jun 2026 01:20:45 GMT  
		Size: 2.0 MB (2005525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd85722eeac2901ebcdc4b4970759b139e69583f42cc4b4f5f84fc21347082c0`  
		Last Modified: Wed, 24 Jun 2026 01:20:45 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:f26a6eb2688cfd1f4cf236c411f9988f840b8e69f0d81f925c8c5b375608a5b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36173798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683edb23fb2832c336aa1334780707e8e429ee767b084b9c4ebf1a76eee13670`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:32:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:32:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:35:52 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:35:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:35:52 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:35:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:35:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:35:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:35:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:35:52 GMT
USER memcache
# Wed, 24 Jun 2026 01:35:52 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:35:52 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:639e1c13483ea279c94219be2736856262d8dd2efeff3e6d309f11a66aba21fb`  
		Last Modified: Wed, 24 Jun 2026 00:30:29 GMT  
		Size: 33.6 MB (33606388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d700e36837a63da25a34bd9fef9f7937541cbe617e8c1e9c4a785cc37d6e2e29`  
		Last Modified: Wed, 24 Jun 2026 01:36:14 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7456d8868d48e0b53288836b26930c6efe02b67c099dcefa481778870fc15df`  
		Last Modified: Wed, 24 Jun 2026 01:36:15 GMT  
		Size: 170.4 KB (170375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7daaa467c3a42eb0ea458c5771839433b7c4f773537351a10e30789f995f63`  
		Last Modified: Wed, 24 Jun 2026 01:36:15 GMT  
		Size: 2.4 MB (2395518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a6999cbf05638c0554accc7e8f9d8acd435888a52ad68267fcbd567d8fdce0`  
		Last Modified: Wed, 24 Jun 2026 01:36:14 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5f81262c7fc9478a7854e6dcf5e83a4d09732948b63b45b5d138da7fd57d8c`  
		Last Modified: Wed, 24 Jun 2026 01:36:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:1db8703b08d0d14737d40156d6a09384027af9d6806c94c63763d4b5cd08bc31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9df60db9b699e1540eb1b1a65a79dfffa825cdb8a5c9ce191b5cd53055af17e2`

```dockerfile
```

-	Layers:
	-	`sha256:d207552f6be1ed5a92472733946f240471025ee31516d22f4e4e1710136a5df9`  
		Last Modified: Wed, 24 Jun 2026 01:36:15 GMT  
		Size: 2.0 MB (2011969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2777dc1115238cc20388367ecc331281ddd19f28aafede9028ceb87baaf56ed`  
		Last Modified: Wed, 24 Jun 2026 01:36:14 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:1d09cc6da0fcd7fbfd1eb9a04ab9aeb8557f8a977d85bc7758ddc33f1fae7e8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30626877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e932fab34f25980444b8d9d4042f4f019d633ae41731c4d58de9d0425aacbb5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 20:53:15 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 20:53:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jun 2026 19:11:35 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 25 Jun 2026 19:11:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 25 Jun 2026 19:11:35 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 25 Jun 2026 19:11:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 25 Jun 2026 19:11:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 25 Jun 2026 19:11:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 25 Jun 2026 19:11:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Jun 2026 19:11:35 GMT
USER memcache
# Thu, 25 Jun 2026 19:11:35 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 25 Jun 2026 19:11:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:58bface994ba631e609596a2ca5032d9d75de27f1b6476034b581e226205adab`  
		Last Modified: Wed, 24 Jun 2026 03:41:42 GMT  
		Size: 28.3 MB (28282378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88be0d85b1f48be753592f62cac7ef80c23a61c7848026bd2d489c40d2214a58`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5924e63da94311a18a309f02e655774d7a7dd21bf3dc267215c524167fb7ca02`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 133.1 KB (133093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfa9af5e6df6f7145e6f80ab61869e6613b9f5caa0cfa94788cbf01b3041add`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 2.2 MB (2209890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ace1c66f882f3224670cc80ac0c47197433c688d59a6bad4e5e137d6947a7d9`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470dc087e4a89d9d58d8fa29a67ac089e3c4b569f1c1c79265bfe24ba39500d2`  
		Last Modified: Thu, 25 Jun 2026 19:12:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:10dc6cdb2cd2787d533382c9b0e6ae2f8f3b637c254e1b54762fc75d6b7c2066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173dffb05aa61f0096ec844832f392e17573e61865ef528ee8b742faa7e4b6db`

```dockerfile
```

-	Layers:
	-	`sha256:69ed82bb373c86c8fbec635b83221f89933079ee40e6fcf48418d1a69ca5bb89`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 2.0 MB (2002332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cea64cfdecc1c5a9f3c417e6a679e88cd0613790ff8f658ca9e3ec73325fa9cc`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:6bcf745c9e84c923ee6794f31fd61c321c07e98208661f8f96267b959b19322c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32291924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfeb11440a0b99b60cfece211ea4a2d19eb4c5aa0e27cc119d9930da48bb4a23`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:17:57 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:18:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:21:15 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:21:15 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:21:15 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:21:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:21:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:21:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:21:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:21:16 GMT
USER memcache
# Wed, 24 Jun 2026 01:21:16 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:21:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b6a0af2ceb4b698210b8776157288a3fb06e46aaf75d641139449fcc50ce430d`  
		Last Modified: Wed, 24 Jun 2026 00:28:43 GMT  
		Size: 29.9 MB (29851381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3bba39c5a45464aeb0d1fa775a329c0c537439ee4814281c4fc08a68d8cd584`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a60267637fa53d628133884b458b9c84464d66f87fb587bd54667d3e7c6c0f8`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 140.5 KB (140541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009a2f1905baeb2174621049e700d37eaaf68cda0912ab76762452f73537af8e`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 2.3 MB (2298488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5127e016f9d2a0554de486521914b692af85186039386e058a7e61c9754ef414`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf617d16473cca6af3500948111afc2fce546cd4db4d94441113555d9a9da08`  
		Last Modified: Wed, 24 Jun 2026 01:21:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:2721a3c701c85fd239ef39e576be9973f43c9655cc6cb66fd5bc3dc3ce206166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c4f64b3eb5d1eccd239a9a42a97ae1477a0b589f61e823181e9ab7271116da`

```dockerfile
```

-	Layers:
	-	`sha256:26bfdc43fc003330338d918e59f990463e9e8ceae7dbef48f43cdcb95e0f9b4e`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 2.0 MB (2009805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b9c877b5a220dabf32e1e097a3fb26dc36bad47b1978fb4b39ce7ae5415394f`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.42`

```console
$ docker pull memcached@sha256:e2a8683c7fbb73d12dce8082525adf9df857765970e639bd9f4705acc31dfcba
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

### `memcached:1.6.42` - linux; amd64

```console
$ docker pull memcached@sha256:3e079a2fc4232b10565b9bc19139292f16ef304297d4560f08f642f5f2d7a6a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32204836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ab1d39869e17aa04a25df4af0b5bf28a973d4f965635b067471bb44adbdc01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:21:34 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:21:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:24:28 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:24:28 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:24:28 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:24:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:24:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:24:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:24:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:24:28 GMT
USER memcache
# Wed, 24 Jun 2026 01:24:28 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:24:28 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1213ec9c2c2febafa221ff6195f27ea10c675acbc71d21fcc0d2b2ade3f5f74b`  
		Last Modified: Wed, 24 Jun 2026 01:24:34 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3266f17f87ca1b46b5c4fde9dd99707e3827b91b70059e7031ef53abd47fb12c`  
		Last Modified: Wed, 24 Jun 2026 01:24:34 GMT  
		Size: 136.7 KB (136688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a006226c9ea4b6f900685ceec0bda7162e03f436f1b312db9c6ba0d5b47919c7`  
		Last Modified: Wed, 24 Jun 2026 01:24:35 GMT  
		Size: 2.3 MB (2281216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3fd586859c95b544309532471aaabcf797408c5d017bd900b8e4c56c911367`  
		Last Modified: Wed, 24 Jun 2026 01:24:34 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2160167316cd327104547209c9d482373032078e07bb8a6a1e807f7e415571`  
		Last Modified: Wed, 24 Jun 2026 01:24:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42` - unknown; unknown

```console
$ docker pull memcached@sha256:78b554b9b0edb7e45697fbdc7fb7bd3b9facbf500f3f955b3e21628a2469b659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97077f9e00ac4cde9ecb4dba83482ab83cfb8c9378171bf96fc076cc86a64a7`

```dockerfile
```

-	Layers:
	-	`sha256:0f81896f32bd3f922ecc9c3921e78406158e32af9b86b0bc711b5381f977f1e1`  
		Last Modified: Wed, 24 Jun 2026 01:24:35 GMT  
		Size: 2.0 MB (2008368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2714f45af9d9661f076eb378c43b8c30b2b1556e38d5573a646c9df3faae7740`  
		Last Modified: Wed, 24 Jun 2026 01:24:34 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42` - linux; arm variant v5

```console
$ docker pull memcached@sha256:07d3a299e990256fef486b7259267b9140a71a6003c6b138f0629c06e8eab05a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30316687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3763f93158d93525ae099ec31b8c33c6f309d88e3e96f8e6e18ba87c3f5c18`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:14:31 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:14:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:17:52 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:17:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:17:52 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:17:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:17:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:17:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:17:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:17:52 GMT
USER memcache
# Wed, 24 Jun 2026 01:17:52 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:17:52 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:da43bc6a07a9cd7cc23faa538adc0797482747316b5a85b9f3f94ed17f6c1a2a`  
		Last Modified: Wed, 24 Jun 2026 00:28:12 GMT  
		Size: 28.0 MB (27959221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72b0a4d36a2a621f7921b07bce6fd125f5f5dcef47bd823dc4e31290e3e2399`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4e24ea733891c84a840e31af3fb0b9c15056a407cdc805d54c8cfd3e6ef6f0`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 144.2 KB (144157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64639d0df1b35e7dbd196efee0fd423d0a736ac6c863e17f7d6986420c041af8`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 2.2 MB (2211796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090c9d3495cd22555152f5b251e3f1fe30e588646fcac43f30a778eb73470f8e`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02db167b638147d6fc9f87b04a310ffd4b96fc41da3f61194b9525811486129`  
		Last Modified: Wed, 24 Jun 2026 01:18:00 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42` - unknown; unknown

```console
$ docker pull memcached@sha256:b276ce09ef33302e7b98984a8b1515cd0c83190274b6163f2a28f2d539cc4a7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:390cd34082323b589abd9a85a9cf2513c80fd64085a0a6aa744e0b297aa7a4b5`

```dockerfile
```

-	Layers:
	-	`sha256:259590638c0e780d766f685e7f3a057b89c4575e1736e106d88bcbd2e7c345cb`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 2.0 MB (2011371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd7d6f82a916ba666327037ebdcdce8491adee8668fde99a67161383e1bdaf64`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42` - linux; arm variant v7

```console
$ docker pull memcached@sha256:e2be04c60636f94c2c1555f324fd58c8ed1cca98bfc5721d5d00a8357a7df461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28513245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc5b22192f1fe06b621ee612a1428f71028d4702873f593a6e3f1896b5c7edfd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:19:26 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:19:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:22:38 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:22:38 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:22:38 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:22:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:22:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:22:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:22:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:22:38 GMT
USER memcache
# Wed, 24 Jun 2026 01:22:38 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:22:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:81c84b0273952340067af970e1fe77a42ea83b4ed1a53319e258d5f1077848f0`  
		Last Modified: Wed, 24 Jun 2026 00:28:38 GMT  
		Size: 26.2 MB (26211051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0642cf323abcb26caa4c3ff3b7e80d0d7d6d9f6d9d9accdcf6d336f41426f102`  
		Last Modified: Wed, 24 Jun 2026 01:22:44 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2360e1299ad9a74124543c81dfb5655cf827191bca3b68df2bfa35cef12ff4c6`  
		Last Modified: Wed, 24 Jun 2026 01:22:44 GMT  
		Size: 135.4 KB (135381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa1e7d2a4dedc5e64f5906cba5d754b8a704705fc6875aa2c6e19fbf32e80d0`  
		Last Modified: Wed, 24 Jun 2026 01:22:45 GMT  
		Size: 2.2 MB (2165300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1110dbe0eb2a934122b522315e135c97a24e58dfe0d85799fa581bed83010517`  
		Last Modified: Wed, 24 Jun 2026 01:22:44 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6a4eee2665c4591534d0fb4f767664091dd2025201db5c28be41b6cde451d4`  
		Last Modified: Wed, 24 Jun 2026 01:22:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42` - unknown; unknown

```console
$ docker pull memcached@sha256:69daaf7d08ee571ea31fa5ba2bbed9ee75e05eaa0e828fec25bcbbb5db45e674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ce76762dc893723cf043776255f735aa512c188d67735932b74d4347be6e02d`

```dockerfile
```

-	Layers:
	-	`sha256:bd51ee9d8e158fbc8c58b5d3ec9bb91d9e9adb533d51ef67ba795e241a2a1486`  
		Last Modified: Wed, 24 Jun 2026 01:22:45 GMT  
		Size: 2.0 MB (2009828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce07aa39f2cbf08f3885676ecfd34bf02f971dd10ba62db2f161f39e032df30d`  
		Last Modified: Wed, 24 Jun 2026 01:22:44 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ce9daf8b2144b701cf7e968ab341768bb2d3efa2a4c64d02da0a0de42c56f1bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32566611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cc2b42a078d89f4b7328abbd61b2cc235e3c733db4c018c8c232c8e3c8dac40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:22:00 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:22:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:25:00 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:25:00 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:25:00 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:25:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:25:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:25:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:25:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:25:00 GMT
USER memcache
# Wed, 24 Jun 2026 01:25:00 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:25:00 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45863abe59cf630e20caf87380378a813615419b3e0f3a8f6649855538dd606`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b7dfd57d8e29e17a7f5191adae69420144fe599879e351b48979971c36f465`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 153.5 KB (153487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be9b72bcf7171564f265414becff9bc077025e30b3f602008e49e51af592400`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 2.3 MB (2263062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff542c356a684239a022d62e5a51aa3f8884a5a1c5a7125cd5d4133c8bac04a`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf0b844cb30e05fdae9181c546555144b913389d03c3ed5549c809d6d4f5cb5`  
		Last Modified: Wed, 24 Jun 2026 01:25:07 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42` - unknown; unknown

```console
$ docker pull memcached@sha256:4b6ea06e8e33c13f6ed836c0f565b1bb81217e79880acaac6b7ad6c4ae57a35d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d49fd2b1e37fca3ad0e2c2747ad1ffa5e40f4dac971d3d382bb685ad2cbeb75`

```dockerfile
```

-	Layers:
	-	`sha256:0749a7c57e354ea8640b297fd510a9c6b05145e740a4d1747f3d832d71878a63`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 2.0 MB (2008676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31dad526561e0628b5270544aa1a9c883fbecd2e25a9770bf262407c2e0bf810`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42` - linux; 386

```console
$ docker pull memcached@sha256:b2916cadce1269827ce2769d75e850a06fa02e2b29d606a5300c10859def3696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33675687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c903111eaced6eb842f558accf95d8d210049b93dfdce69195cb596a9295aa2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:17:36 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:17:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:20:39 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:20:39 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:20:39 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:20:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:20:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:20:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:20:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:20:39 GMT
USER memcache
# Wed, 24 Jun 2026 01:20:39 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:20:39 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:984d3baa100eb8c4d7c83b7c23b4748e508aa6ed5903297f02be90a681f52d41`  
		Last Modified: Wed, 24 Jun 2026 00:28:38 GMT  
		Size: 31.3 MB (31301210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e88a5ba508193f8a40b67d411ba88b51522122e991c5e579f718f03a7b827d5`  
		Last Modified: Wed, 24 Jun 2026 01:20:45 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13a37bd401d9e6fe5c150251a68821160273feb13462cbe401715d4c50bbcee`  
		Last Modified: Wed, 24 Jun 2026 01:20:45 GMT  
		Size: 147.5 KB (147522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f7f30bf297b5062f967e9d807b67dbfcbd20800b75c6daae0ad7fff1edf46e`  
		Last Modified: Wed, 24 Jun 2026 01:20:46 GMT  
		Size: 2.2 MB (2225442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1687fae458633e2c28615b4a2b32841cea0191dc6777aa4ad23de450a9f898e4`  
		Last Modified: Wed, 24 Jun 2026 01:20:45 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc431901c24b9ea4ccb36149baa5b10a412da5738b7f7af9808c7a408caebc12`  
		Last Modified: Wed, 24 Jun 2026 01:20:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42` - unknown; unknown

```console
$ docker pull memcached@sha256:ceb7723388cb240f2eff890796603dfa6d63cb5e7f9e9774cf291a70411779ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596e979ff6ae6cf65094d2e268ad30ecd052f4cb73e4dddeb3644a8b5d4e00b7`

```dockerfile
```

-	Layers:
	-	`sha256:f42e4ebf214a33a305d64952d73fd7dd183f7a9b3c1ee3618be109170351a6f2`  
		Last Modified: Wed, 24 Jun 2026 01:20:45 GMT  
		Size: 2.0 MB (2005525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd85722eeac2901ebcdc4b4970759b139e69583f42cc4b4f5f84fc21347082c0`  
		Last Modified: Wed, 24 Jun 2026 01:20:45 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42` - linux; ppc64le

```console
$ docker pull memcached@sha256:f26a6eb2688cfd1f4cf236c411f9988f840b8e69f0d81f925c8c5b375608a5b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36173798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683edb23fb2832c336aa1334780707e8e429ee767b084b9c4ebf1a76eee13670`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:32:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:32:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:35:52 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:35:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:35:52 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:35:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:35:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:35:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:35:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:35:52 GMT
USER memcache
# Wed, 24 Jun 2026 01:35:52 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:35:52 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:639e1c13483ea279c94219be2736856262d8dd2efeff3e6d309f11a66aba21fb`  
		Last Modified: Wed, 24 Jun 2026 00:30:29 GMT  
		Size: 33.6 MB (33606388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d700e36837a63da25a34bd9fef9f7937541cbe617e8c1e9c4a785cc37d6e2e29`  
		Last Modified: Wed, 24 Jun 2026 01:36:14 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7456d8868d48e0b53288836b26930c6efe02b67c099dcefa481778870fc15df`  
		Last Modified: Wed, 24 Jun 2026 01:36:15 GMT  
		Size: 170.4 KB (170375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7daaa467c3a42eb0ea458c5771839433b7c4f773537351a10e30789f995f63`  
		Last Modified: Wed, 24 Jun 2026 01:36:15 GMT  
		Size: 2.4 MB (2395518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a6999cbf05638c0554accc7e8f9d8acd435888a52ad68267fcbd567d8fdce0`  
		Last Modified: Wed, 24 Jun 2026 01:36:14 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5f81262c7fc9478a7854e6dcf5e83a4d09732948b63b45b5d138da7fd57d8c`  
		Last Modified: Wed, 24 Jun 2026 01:36:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42` - unknown; unknown

```console
$ docker pull memcached@sha256:1db8703b08d0d14737d40156d6a09384027af9d6806c94c63763d4b5cd08bc31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9df60db9b699e1540eb1b1a65a79dfffa825cdb8a5c9ce191b5cd53055af17e2`

```dockerfile
```

-	Layers:
	-	`sha256:d207552f6be1ed5a92472733946f240471025ee31516d22f4e4e1710136a5df9`  
		Last Modified: Wed, 24 Jun 2026 01:36:15 GMT  
		Size: 2.0 MB (2011969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2777dc1115238cc20388367ecc331281ddd19f28aafede9028ceb87baaf56ed`  
		Last Modified: Wed, 24 Jun 2026 01:36:14 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42` - linux; riscv64

```console
$ docker pull memcached@sha256:1d09cc6da0fcd7fbfd1eb9a04ab9aeb8557f8a977d85bc7758ddc33f1fae7e8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30626877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e932fab34f25980444b8d9d4042f4f019d633ae41731c4d58de9d0425aacbb5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 20:53:15 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 20:53:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jun 2026 19:11:35 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 25 Jun 2026 19:11:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 25 Jun 2026 19:11:35 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 25 Jun 2026 19:11:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 25 Jun 2026 19:11:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 25 Jun 2026 19:11:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 25 Jun 2026 19:11:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Jun 2026 19:11:35 GMT
USER memcache
# Thu, 25 Jun 2026 19:11:35 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 25 Jun 2026 19:11:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:58bface994ba631e609596a2ca5032d9d75de27f1b6476034b581e226205adab`  
		Last Modified: Wed, 24 Jun 2026 03:41:42 GMT  
		Size: 28.3 MB (28282378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88be0d85b1f48be753592f62cac7ef80c23a61c7848026bd2d489c40d2214a58`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5924e63da94311a18a309f02e655774d7a7dd21bf3dc267215c524167fb7ca02`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 133.1 KB (133093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfa9af5e6df6f7145e6f80ab61869e6613b9f5caa0cfa94788cbf01b3041add`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 2.2 MB (2209890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ace1c66f882f3224670cc80ac0c47197433c688d59a6bad4e5e137d6947a7d9`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470dc087e4a89d9d58d8fa29a67ac089e3c4b569f1c1c79265bfe24ba39500d2`  
		Last Modified: Thu, 25 Jun 2026 19:12:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42` - unknown; unknown

```console
$ docker pull memcached@sha256:10dc6cdb2cd2787d533382c9b0e6ae2f8f3b637c254e1b54762fc75d6b7c2066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173dffb05aa61f0096ec844832f392e17573e61865ef528ee8b742faa7e4b6db`

```dockerfile
```

-	Layers:
	-	`sha256:69ed82bb373c86c8fbec635b83221f89933079ee40e6fcf48418d1a69ca5bb89`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 2.0 MB (2002332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cea64cfdecc1c5a9f3c417e6a679e88cd0613790ff8f658ca9e3ec73325fa9cc`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42` - linux; s390x

```console
$ docker pull memcached@sha256:6bcf745c9e84c923ee6794f31fd61c321c07e98208661f8f96267b959b19322c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32291924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfeb11440a0b99b60cfece211ea4a2d19eb4c5aa0e27cc119d9930da48bb4a23`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:17:57 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:18:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:21:15 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:21:15 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:21:15 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:21:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:21:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:21:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:21:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:21:16 GMT
USER memcache
# Wed, 24 Jun 2026 01:21:16 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:21:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b6a0af2ceb4b698210b8776157288a3fb06e46aaf75d641139449fcc50ce430d`  
		Last Modified: Wed, 24 Jun 2026 00:28:43 GMT  
		Size: 29.9 MB (29851381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3bba39c5a45464aeb0d1fa775a329c0c537439ee4814281c4fc08a68d8cd584`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a60267637fa53d628133884b458b9c84464d66f87fb587bd54667d3e7c6c0f8`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 140.5 KB (140541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009a2f1905baeb2174621049e700d37eaaf68cda0912ab76762452f73537af8e`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 2.3 MB (2298488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5127e016f9d2a0554de486521914b692af85186039386e058a7e61c9754ef414`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf617d16473cca6af3500948111afc2fce546cd4db4d94441113555d9a9da08`  
		Last Modified: Wed, 24 Jun 2026 01:21:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42` - unknown; unknown

```console
$ docker pull memcached@sha256:2721a3c701c85fd239ef39e576be9973f43c9655cc6cb66fd5bc3dc3ce206166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c4f64b3eb5d1eccd239a9a42a97ae1477a0b589f61e823181e9ab7271116da`

```dockerfile
```

-	Layers:
	-	`sha256:26bfdc43fc003330338d918e59f990463e9e8ceae7dbef48f43cdcb95e0f9b4e`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 2.0 MB (2009805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b9c877b5a220dabf32e1e097a3fb26dc36bad47b1978fb4b39ce7ae5415394f`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.42-alpine`

```console
$ docker pull memcached@sha256:7381333da6d6ae06e02d8dfc87ee6f2c7cd0a19f7ba048d5efc538d2100e2208
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

### `memcached:1.6.42-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:ce375dd48f976d33bf35beb966cc37f202fd840a90891e58b9e71171fc74174d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5921579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d284e7a8445d8dc70e97c673a8a0175d18f39d5336ccbdfa8b240c0ef3ce4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:15:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:15:18 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:54 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:54 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:54 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb73756dcbbebc424eab53d3adda4d9f64001e7a91272a7b2a834622c08b093`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f0d6a5291334f2b54ec652193cd4e17ee22455b2f3ff3bd9b66acff6436c7b`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 106.1 KB (106066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ac11a8307528096ac745e0ef681b64854bbd012ffdfbce85587153eec73563`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 2.0 MB (1967772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3626493aad85d70a212bc66e9d45db8aef43b4bc662259563f916398165f1e64`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cdcd3f20e3aa439838f5491e6f457a42bad6c80ed9b099313bf79b57a721ea8`  
		Last Modified: Tue, 16 Jun 2026 00:18:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:bb948800301f1cae8e18e317f2b9e85636c86c4a1924ee85e125da37cb1333e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c3e084937eb543038244e151b03b8d9a0dce0b4d5bf87c2d471fa397ed5702`

```dockerfile
```

-	Layers:
	-	`sha256:9d05a792212c92363a76bb6a8205a6e7f386113b3efc1b5d600f93d4e237c975`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 94.9 KB (94897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee0e7e70ef03205f55c68bc1b74ac7854183aee4e871112794975dc852761b19`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:4b144cdbc67c11035b3d0f0c812b590ee694977f2f6a32321e538237bd2f841c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5573158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e9bb70df1535a2f8ca960f733a4404cbde900a13156a1f4446c2fd110258e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:25 GMT
ADD alpine-minirootfs-3.24.1-armhf.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:25 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:14:43 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:14:44 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:47 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:47 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3c4836a46d600cfe9a422adf7a80205cb534097e6213325e0176c51f6e5cc02e`  
		Last Modified: Sun, 14 Jun 2026 06:44:57 GMT  
		Size: 3.6 MB (3553450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e732a60042adf5cff5fe4fe0de83f937f6e5c8896500f7023e8bf68ed0670d65`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad86d1fea29db061a5ae896a0a595b144edcdb4af59deac2b75b0fb8f5fa2d4c`  
		Last Modified: Tue, 16 Jun 2026 00:17:50 GMT  
		Size: 102.6 KB (102624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f26dd2445dbf4d5624417ca290f5ae2e5774fa7fec4f5655cd2377ee3147e4`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 1.9 MB (1915730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080a186f0ca6beb06a5ce4a86fbc71f5b9995713fcc899c73f995f251ef7c987`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c4d4f455f9a2b633cca28e3aa2190e4c42ca83ca6e3ea88ea4abe16944d238`  
		Last Modified: Tue, 16 Jun 2026 00:17:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d6b7abf6ef34abf12ab2c7f84bd29ac2461eb3271d1c4070456ed9b94e4b41a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a767571287c8ca227e321ee8d65f9da82e558098bedbb15888434dcc1ce9fa`

```dockerfile
```

-	Layers:
	-	`sha256:1794ccef4392c0db4ba36ad7fde22cdacbda40f4d56f0adbef802163c87e066c`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:848c5e0ced69b802cca72c23bec05a4c6f23136212a4a1d5cc22b7c8f0154bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286f62a53a8947036e39f2b79567b31d38309fd84c7a39e43de8c5f9817a2f64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:26 GMT
ADD alpine-minirootfs-3.24.1-armv7.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:17:59 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:17:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:20:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:20:56 GMT
USER memcache
# Tue, 16 Jun 2026 00:20:56 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:20:56 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bc03a9e5b4dd452551f246e199537fe7afc1765f53f510bc81d26df9845e4008`  
		Last Modified: Sun, 14 Jun 2026 06:45:22 GMT  
		Size: 3.3 MB (3260615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f0249bacfc8953b72899bf7b6c904c8750482fce4c93108f57b2c64228b279`  
		Last Modified: Tue, 16 Jun 2026 00:21:00 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95e1b321ffc31d01e766d5d1d054967d613940563406fc54ee981926b7f6049`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 92.4 KB (92366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce112e60c1b15077277c233a7707831818dff0a15f1fc977ebebc93f817dad43`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 1.9 MB (1875183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32fa6ed5b14fd6fcf96a7cde2996063f10b8efe802c386479288a232af826027`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6648f8180a4eea1f5197f2fa2d356fbbf4e5f65345e189e720e227af64a5e31`  
		Last Modified: Tue, 16 Jun 2026 00:21:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:59387f31eff7cfb3166c5e6d4bad92e255705affcc15c84c4a06c86ecb1a9890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:174eb460b1df4523a4f71ba5a996f2285fa845fe8ef76d2df3ea8c4962c6b6ca`

```dockerfile
```

-	Layers:
	-	`sha256:4ff5e70775e819cab551295c56b58fdb0c44c105cdc4f72247e3968accd2ab2f`  
		Last Modified: Tue, 16 Jun 2026 00:21:00 GMT  
		Size: 94.3 KB (94315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00f10e1301c7e61396658f7e3ed330e400a9f304c6a0323de8ff644aba987474`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:33261748facce282dbe4dbb4d9f875139680fce4cefc13cb9ad8e1ced23f9557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6250475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1614bb2865c8f849c2bc5bf77703a1ab711695c607a8bc6edb013a076ec16d6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:18 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:16:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:16:06 GMT
USER memcache
# Tue, 16 Jun 2026 00:16:06 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:16:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5faa19f06c4d5e26332739c7f08fd3dcd2c81817471c62029a6d99af6be8748`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377a35d28f00766e2679c788b95b0a67b9aa5a76c8ef701a2a9604e2a00c3b46`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 121.8 KB (121841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0b819e89558d70f1401ca58cbc19c58ae13e15be8184fd9b2733e022f318a4`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 1.9 MB (1944247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca539cef48ff8c3f723ab23506b6786c9ed26a9cac713601b71de2dc775d26a`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4c456deed244daa6d7076f40a1cf0364d294059bb43e533677a89027843b15`  
		Last Modified: Tue, 16 Jun 2026 00:16:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:4d25960abc53b5ba1896b8f5ee04ba5ac1389900ab9b413eb62285af7281aedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d1a4b7ad428a08c8a174d5ecd9763d530e849f54a2d9b90aef934e54b9477d4`

```dockerfile
```

-	Layers:
	-	`sha256:9c0a8e5e07390fae6abe9204450009671011c4d2d5aa5fe4afdd82324fdb49b9`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 94.4 KB (94351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ee01158358d01c082867cf46a5225cf101013e4d5b7eae18fc7853e277ff0f4`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 20.7 KB (20727 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-alpine` - linux; 386

```console
$ docker pull memcached@sha256:5436d0ef6e12f2f8e454384ff4a703132b3fe820c41a55336f520bb5d1622574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5702329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8946be3d97c7b9825159f58cbf832b131c75cb90b3fb46a40d5429b9ffe32bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:19 GMT
ADD alpine-minirootfs-3.24.1-x86.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:19 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:59 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:16:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:16:46 GMT
USER memcache
# Tue, 16 Jun 2026 00:16:46 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:16:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f86df9d778509895efbf9363d8fcb0cbe0b772de536c7218e4c4c947f0be879f`  
		Last Modified: Sun, 14 Jun 2026 06:45:46 GMT  
		Size: 3.7 MB (3670141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043137360442e605bc150f28f20e1fa2d23d90131370bc405ad7d35309594491`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900ce6eeaece12033b12f1c8641c33dcf62ff2525584411911368cfcd0b38224`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 110.7 KB (110729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e8cc1c8f6bc6391eb1a43a46f0b55ca7845f824fc0f2fc7ae7587a7715814e`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 1.9 MB (1920111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94f6e4d3be92188fc182a3557fe43af5bc9f3e768a7f265977743a56eea527e`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f8a19f18dfff271426de7a17ab6780788fa4345d5fa0120e6d03720d552bd4`  
		Last Modified: Tue, 16 Jun 2026 00:16:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:00dc6a7f29b7f2f5ac46fc5678b80c43c7b1e46b4ca3c84c5597034180aeb644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de04019c7775544db9adbb4c4558d0e7c842c279e5d70532b2ac0b988ac1345`

```dockerfile
```

-	Layers:
	-	`sha256:80895f8f5e9c9b015e419096426322f4c86c33d55ca8860ee046b61d52782847`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 94.9 KB (94852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c69be8c1f82a066b46cc389712508e85c1dcd77e649c922dba46ace64b343ae`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:c7857941a51b85b136781035703afcc8854a2d70fa2091208a51f8bb7e71f934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5998515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b02b2222212c64e444ac1a2227b19f0cfb1282c8a8ced386c1b79ae48c641b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:15 GMT
ADD alpine-minirootfs-3.24.1-ppc64le.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:15 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:15:37 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:15:38 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:18:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:18:22 GMT
USER memcache
# Tue, 16 Jun 2026 00:18:22 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:18:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3ebcdcd395ccee658b9200e4b27d7699e5d6ed9f6c1858dea12781aac519ff59`  
		Last Modified: Sun, 14 Jun 2026 06:46:36 GMT  
		Size: 3.8 MB (3813400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b108e2058722fb0fb5a9310e8ebe82ab4b9c021228a94b3125ba49d318e9667`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb8160ed736eda8513164d5d703082fb0c9af9e037472ab70a02579caa3eb99`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 126.3 KB (126252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5cb88dd03ce07ecf1613c2aff220fb392763d8f22edc900c4ad032ee7103d34`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 2.1 MB (2057508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12fd57420ca797ab383c58a488044d324c4d43b3c94a848f86a0524ed3064b4`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c0c7b7a77e9375d8a75fb825fa274d9127ca96de79107550517be29501c817`  
		Last Modified: Tue, 16 Jun 2026 00:18:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:851f463d4778539d5e4981f972420f9a57ec2559488f8a59fba6abab6065032f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734dd3d91f2d6cf217233f7a9dacc3c20ff0590246adb790f95713fb21c115de`

```dockerfile
```

-	Layers:
	-	`sha256:c0d4c203ef9f66cf827ec62098d7801e1c49f1187e0fe047fd32fc2a3271f636`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 94.3 KB (94304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b734d170b5463fa77dd77072e06d51a28efe59a53600d47435b015ebcadae92`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:ba5bf40b4adc1fe04f32e2e239fa9c0020d4e89bf4079493f8bc11a92c8f4b51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5738070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d12fbf86d6880aaa9d517425d9cecddcf545ba87e577a039dea9ea99ad53d8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 05:59:15 GMT
ADD alpine-minirootfs-3.24.1-riscv64.tar.gz / # buildkit
# Tue, 16 Jun 2026 05:59:15 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 08:28:27 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 19 Jun 2026 08:28:31 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_VERSION=1.6.42
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Fri, 19 Jun 2026 08:41:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 19 Jun 2026 08:41:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 08:41:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 19 Jun 2026 08:41:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 08:41:53 GMT
USER memcache
# Fri, 19 Jun 2026 08:41:53 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 19 Jun 2026 08:41:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c34e5222b29b86391cdae95b0473ef789493ff1a0068a3a30b5d66f544bd7cf6`  
		Last Modified: Sun, 14 Jun 2026 06:47:00 GMT  
		Size: 3.6 MB (3574358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09d95a0f414638430c0cd3ecfdcce75606201917a27c7cb2ce1e34cb928b26a`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5335c7af79a1b08af55862ba77644afdae5544d9a7871e45c91b364bd4f71d`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 108.9 KB (108888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3622a6ea71515db1ef566afdbb121daed1f408aacf1519f4173b40dabe2ae627`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 2.1 MB (2053467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1db0e3e31ca3f2830f5404436e92b1862a4078adefacacec09a9580a3ad0a2`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1463b0fd26a37659aaad7f99696e5213764ad03bb094f40836c3309713d7a60`  
		Last Modified: Fri, 19 Jun 2026 08:42:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:aadb3b9338400b87692f95e00931e43940f8d6ddd13f046bd256848dd825e458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde4b5a4a468d795a5f58dd934b371adfe72cd2ae24e166e1258ad65aa455a56`

```dockerfile
```

-	Layers:
	-	`sha256:debb70180cf674562f7ca321270e3dfa350c5d1596c05dbfcc27b38c65652528`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 94.3 KB (94300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a895bbe0bfec24678c1c92ddd283cb7392e0e8d229f31c769a23c95224c0d371`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:e1b640e8d192055e5c3ccd05b077776a0f4d35664191596f7a8230b2cd7ef0f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5823313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ef6221f9c2854683b0633325a98a0e7a0d3b7d865b02d7cdf4c1d49d2e5090`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:21 GMT
ADD alpine-minirootfs-3.24.1-s390x.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:21 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:46 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:12 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:da43be6afaaa3ec1b607461ce64380942a6d76c3d52cda4337b0770d9a96fa89`  
		Last Modified: Sun, 14 Jun 2026 06:47:25 GMT  
		Size: 3.7 MB (3709320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757d04238e02c9bbe1cfd4030cc19e29421650a1b1562a8ca4090d90e9ae17b0`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1949e0fa71fc91bebf4f2e4293108b27de8357d98f98b673bc4f3ed1980b52c`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 114.3 KB (114289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f0e22966bce79fbc8a20f7c27aa07ce63229bb50181319c810ca29f1fb4032`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 2.0 MB (1998350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15eb5e912ef8ec6e3abe76c361cdddb568d20a60be21be379d4d8d7d0ebaa11e`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a549d59ad0d4761ac6f4cca272c4bea521471ed091d0e79143bfda8ff29cf9ce`  
		Last Modified: Tue, 16 Jun 2026 00:17:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:6dbf7c8a98f02a949769403ad1c92583b34a28dccc66b7d83d91863785a6dad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a89d23372d19daf2d6d4e1c4de732f7864316ed5e7713b1103918303873683e`

```dockerfile
```

-	Layers:
	-	`sha256:099ab2d711ef73783b01895824a4664c7d65e2a333e81237b4766cf053a8f6f0`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 94.2 KB (94246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eccbabf44891af00e622624c5cfd5a295656f82f1c15073b240ac34d47af96c`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.42-alpine3.24`

```console
$ docker pull memcached@sha256:7381333da6d6ae06e02d8dfc87ee6f2c7cd0a19f7ba048d5efc538d2100e2208
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

### `memcached:1.6.42-alpine3.24` - linux; amd64

```console
$ docker pull memcached@sha256:ce375dd48f976d33bf35beb966cc37f202fd840a90891e58b9e71171fc74174d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5921579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d284e7a8445d8dc70e97c673a8a0175d18f39d5336ccbdfa8b240c0ef3ce4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:15:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:15:18 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:54 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:54 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:54 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb73756dcbbebc424eab53d3adda4d9f64001e7a91272a7b2a834622c08b093`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f0d6a5291334f2b54ec652193cd4e17ee22455b2f3ff3bd9b66acff6436c7b`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 106.1 KB (106066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ac11a8307528096ac745e0ef681b64854bbd012ffdfbce85587153eec73563`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 2.0 MB (1967772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3626493aad85d70a212bc66e9d45db8aef43b4bc662259563f916398165f1e64`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cdcd3f20e3aa439838f5491e6f457a42bad6c80ed9b099313bf79b57a721ea8`  
		Last Modified: Tue, 16 Jun 2026 00:18:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:bb948800301f1cae8e18e317f2b9e85636c86c4a1924ee85e125da37cb1333e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c3e084937eb543038244e151b03b8d9a0dce0b4d5bf87c2d471fa397ed5702`

```dockerfile
```

-	Layers:
	-	`sha256:9d05a792212c92363a76bb6a8205a6e7f386113b3efc1b5d600f93d4e237c975`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 94.9 KB (94897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee0e7e70ef03205f55c68bc1b74ac7854183aee4e871112794975dc852761b19`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-alpine3.24` - linux; arm variant v6

```console
$ docker pull memcached@sha256:4b144cdbc67c11035b3d0f0c812b590ee694977f2f6a32321e538237bd2f841c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5573158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e9bb70df1535a2f8ca960f733a4404cbde900a13156a1f4446c2fd110258e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:25 GMT
ADD alpine-minirootfs-3.24.1-armhf.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:25 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:14:43 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:14:44 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:47 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:47 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3c4836a46d600cfe9a422adf7a80205cb534097e6213325e0176c51f6e5cc02e`  
		Last Modified: Sun, 14 Jun 2026 06:44:57 GMT  
		Size: 3.6 MB (3553450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e732a60042adf5cff5fe4fe0de83f937f6e5c8896500f7023e8bf68ed0670d65`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad86d1fea29db061a5ae896a0a595b144edcdb4af59deac2b75b0fb8f5fa2d4c`  
		Last Modified: Tue, 16 Jun 2026 00:17:50 GMT  
		Size: 102.6 KB (102624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f26dd2445dbf4d5624417ca290f5ae2e5774fa7fec4f5655cd2377ee3147e4`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 1.9 MB (1915730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080a186f0ca6beb06a5ce4a86fbc71f5b9995713fcc899c73f995f251ef7c987`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c4d4f455f9a2b633cca28e3aa2190e4c42ca83ca6e3ea88ea4abe16944d238`  
		Last Modified: Tue, 16 Jun 2026 00:17:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:d6b7abf6ef34abf12ab2c7f84bd29ac2461eb3271d1c4070456ed9b94e4b41a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a767571287c8ca227e321ee8d65f9da82e558098bedbb15888434dcc1ce9fa`

```dockerfile
```

-	Layers:
	-	`sha256:1794ccef4392c0db4ba36ad7fde22cdacbda40f4d56f0adbef802163c87e066c`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-alpine3.24` - linux; arm variant v7

```console
$ docker pull memcached@sha256:848c5e0ced69b802cca72c23bec05a4c6f23136212a4a1d5cc22b7c8f0154bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286f62a53a8947036e39f2b79567b31d38309fd84c7a39e43de8c5f9817a2f64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:26 GMT
ADD alpine-minirootfs-3.24.1-armv7.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:17:59 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:17:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:20:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:20:56 GMT
USER memcache
# Tue, 16 Jun 2026 00:20:56 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:20:56 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bc03a9e5b4dd452551f246e199537fe7afc1765f53f510bc81d26df9845e4008`  
		Last Modified: Sun, 14 Jun 2026 06:45:22 GMT  
		Size: 3.3 MB (3260615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f0249bacfc8953b72899bf7b6c904c8750482fce4c93108f57b2c64228b279`  
		Last Modified: Tue, 16 Jun 2026 00:21:00 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95e1b321ffc31d01e766d5d1d054967d613940563406fc54ee981926b7f6049`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 92.4 KB (92366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce112e60c1b15077277c233a7707831818dff0a15f1fc977ebebc93f817dad43`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 1.9 MB (1875183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32fa6ed5b14fd6fcf96a7cde2996063f10b8efe802c386479288a232af826027`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6648f8180a4eea1f5197f2fa2d356fbbf4e5f65345e189e720e227af64a5e31`  
		Last Modified: Tue, 16 Jun 2026 00:21:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:59387f31eff7cfb3166c5e6d4bad92e255705affcc15c84c4a06c86ecb1a9890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:174eb460b1df4523a4f71ba5a996f2285fa845fe8ef76d2df3ea8c4962c6b6ca`

```dockerfile
```

-	Layers:
	-	`sha256:4ff5e70775e819cab551295c56b58fdb0c44c105cdc4f72247e3968accd2ab2f`  
		Last Modified: Tue, 16 Jun 2026 00:21:00 GMT  
		Size: 94.3 KB (94315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00f10e1301c7e61396658f7e3ed330e400a9f304c6a0323de8ff644aba987474`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-alpine3.24` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:33261748facce282dbe4dbb4d9f875139680fce4cefc13cb9ad8e1ced23f9557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6250475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1614bb2865c8f849c2bc5bf77703a1ab711695c607a8bc6edb013a076ec16d6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:18 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:16:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:16:06 GMT
USER memcache
# Tue, 16 Jun 2026 00:16:06 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:16:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5faa19f06c4d5e26332739c7f08fd3dcd2c81817471c62029a6d99af6be8748`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377a35d28f00766e2679c788b95b0a67b9aa5a76c8ef701a2a9604e2a00c3b46`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 121.8 KB (121841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0b819e89558d70f1401ca58cbc19c58ae13e15be8184fd9b2733e022f318a4`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 1.9 MB (1944247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca539cef48ff8c3f723ab23506b6786c9ed26a9cac713601b71de2dc775d26a`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4c456deed244daa6d7076f40a1cf0364d294059bb43e533677a89027843b15`  
		Last Modified: Tue, 16 Jun 2026 00:16:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:4d25960abc53b5ba1896b8f5ee04ba5ac1389900ab9b413eb62285af7281aedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d1a4b7ad428a08c8a174d5ecd9763d530e849f54a2d9b90aef934e54b9477d4`

```dockerfile
```

-	Layers:
	-	`sha256:9c0a8e5e07390fae6abe9204450009671011c4d2d5aa5fe4afdd82324fdb49b9`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 94.4 KB (94351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ee01158358d01c082867cf46a5225cf101013e4d5b7eae18fc7853e277ff0f4`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 20.7 KB (20727 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-alpine3.24` - linux; 386

```console
$ docker pull memcached@sha256:5436d0ef6e12f2f8e454384ff4a703132b3fe820c41a55336f520bb5d1622574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5702329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8946be3d97c7b9825159f58cbf832b131c75cb90b3fb46a40d5429b9ffe32bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:19 GMT
ADD alpine-minirootfs-3.24.1-x86.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:19 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:59 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:16:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:16:46 GMT
USER memcache
# Tue, 16 Jun 2026 00:16:46 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:16:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f86df9d778509895efbf9363d8fcb0cbe0b772de536c7218e4c4c947f0be879f`  
		Last Modified: Sun, 14 Jun 2026 06:45:46 GMT  
		Size: 3.7 MB (3670141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043137360442e605bc150f28f20e1fa2d23d90131370bc405ad7d35309594491`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900ce6eeaece12033b12f1c8641c33dcf62ff2525584411911368cfcd0b38224`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 110.7 KB (110729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e8cc1c8f6bc6391eb1a43a46f0b55ca7845f824fc0f2fc7ae7587a7715814e`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 1.9 MB (1920111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94f6e4d3be92188fc182a3557fe43af5bc9f3e768a7f265977743a56eea527e`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f8a19f18dfff271426de7a17ab6780788fa4345d5fa0120e6d03720d552bd4`  
		Last Modified: Tue, 16 Jun 2026 00:16:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:00dc6a7f29b7f2f5ac46fc5678b80c43c7b1e46b4ca3c84c5597034180aeb644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de04019c7775544db9adbb4c4558d0e7c842c279e5d70532b2ac0b988ac1345`

```dockerfile
```

-	Layers:
	-	`sha256:80895f8f5e9c9b015e419096426322f4c86c33d55ca8860ee046b61d52782847`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 94.9 KB (94852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c69be8c1f82a066b46cc389712508e85c1dcd77e649c922dba46ace64b343ae`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-alpine3.24` - linux; ppc64le

```console
$ docker pull memcached@sha256:c7857941a51b85b136781035703afcc8854a2d70fa2091208a51f8bb7e71f934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5998515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b02b2222212c64e444ac1a2227b19f0cfb1282c8a8ced386c1b79ae48c641b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:15 GMT
ADD alpine-minirootfs-3.24.1-ppc64le.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:15 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:15:37 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:15:38 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:18:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:18:22 GMT
USER memcache
# Tue, 16 Jun 2026 00:18:22 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:18:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3ebcdcd395ccee658b9200e4b27d7699e5d6ed9f6c1858dea12781aac519ff59`  
		Last Modified: Sun, 14 Jun 2026 06:46:36 GMT  
		Size: 3.8 MB (3813400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b108e2058722fb0fb5a9310e8ebe82ab4b9c021228a94b3125ba49d318e9667`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb8160ed736eda8513164d5d703082fb0c9af9e037472ab70a02579caa3eb99`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 126.3 KB (126252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5cb88dd03ce07ecf1613c2aff220fb392763d8f22edc900c4ad032ee7103d34`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 2.1 MB (2057508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12fd57420ca797ab383c58a488044d324c4d43b3c94a848f86a0524ed3064b4`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c0c7b7a77e9375d8a75fb825fa274d9127ca96de79107550517be29501c817`  
		Last Modified: Tue, 16 Jun 2026 00:18:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:851f463d4778539d5e4981f972420f9a57ec2559488f8a59fba6abab6065032f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734dd3d91f2d6cf217233f7a9dacc3c20ff0590246adb790f95713fb21c115de`

```dockerfile
```

-	Layers:
	-	`sha256:c0d4c203ef9f66cf827ec62098d7801e1c49f1187e0fe047fd32fc2a3271f636`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 94.3 KB (94304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b734d170b5463fa77dd77072e06d51a28efe59a53600d47435b015ebcadae92`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-alpine3.24` - linux; riscv64

```console
$ docker pull memcached@sha256:ba5bf40b4adc1fe04f32e2e239fa9c0020d4e89bf4079493f8bc11a92c8f4b51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5738070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d12fbf86d6880aaa9d517425d9cecddcf545ba87e577a039dea9ea99ad53d8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 05:59:15 GMT
ADD alpine-minirootfs-3.24.1-riscv64.tar.gz / # buildkit
# Tue, 16 Jun 2026 05:59:15 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 08:28:27 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 19 Jun 2026 08:28:31 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_VERSION=1.6.42
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Fri, 19 Jun 2026 08:41:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 19 Jun 2026 08:41:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 08:41:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 19 Jun 2026 08:41:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 08:41:53 GMT
USER memcache
# Fri, 19 Jun 2026 08:41:53 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 19 Jun 2026 08:41:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c34e5222b29b86391cdae95b0473ef789493ff1a0068a3a30b5d66f544bd7cf6`  
		Last Modified: Sun, 14 Jun 2026 06:47:00 GMT  
		Size: 3.6 MB (3574358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09d95a0f414638430c0cd3ecfdcce75606201917a27c7cb2ce1e34cb928b26a`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5335c7af79a1b08af55862ba77644afdae5544d9a7871e45c91b364bd4f71d`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 108.9 KB (108888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3622a6ea71515db1ef566afdbb121daed1f408aacf1519f4173b40dabe2ae627`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 2.1 MB (2053467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1db0e3e31ca3f2830f5404436e92b1862a4078adefacacec09a9580a3ad0a2`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1463b0fd26a37659aaad7f99696e5213764ad03bb094f40836c3309713d7a60`  
		Last Modified: Fri, 19 Jun 2026 08:42:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:aadb3b9338400b87692f95e00931e43940f8d6ddd13f046bd256848dd825e458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde4b5a4a468d795a5f58dd934b371adfe72cd2ae24e166e1258ad65aa455a56`

```dockerfile
```

-	Layers:
	-	`sha256:debb70180cf674562f7ca321270e3dfa350c5d1596c05dbfcc27b38c65652528`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 94.3 KB (94300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a895bbe0bfec24678c1c92ddd283cb7392e0e8d229f31c769a23c95224c0d371`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-alpine3.24` - linux; s390x

```console
$ docker pull memcached@sha256:e1b640e8d192055e5c3ccd05b077776a0f4d35664191596f7a8230b2cd7ef0f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5823313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ef6221f9c2854683b0633325a98a0e7a0d3b7d865b02d7cdf4c1d49d2e5090`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:21 GMT
ADD alpine-minirootfs-3.24.1-s390x.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:21 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:46 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:12 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:da43be6afaaa3ec1b607461ce64380942a6d76c3d52cda4337b0770d9a96fa89`  
		Last Modified: Sun, 14 Jun 2026 06:47:25 GMT  
		Size: 3.7 MB (3709320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757d04238e02c9bbe1cfd4030cc19e29421650a1b1562a8ca4090d90e9ae17b0`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1949e0fa71fc91bebf4f2e4293108b27de8357d98f98b673bc4f3ed1980b52c`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 114.3 KB (114289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f0e22966bce79fbc8a20f7c27aa07ce63229bb50181319c810ca29f1fb4032`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 2.0 MB (1998350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15eb5e912ef8ec6e3abe76c361cdddb568d20a60be21be379d4d8d7d0ebaa11e`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a549d59ad0d4761ac6f4cca272c4bea521471ed091d0e79143bfda8ff29cf9ce`  
		Last Modified: Tue, 16 Jun 2026 00:17:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:6dbf7c8a98f02a949769403ad1c92583b34a28dccc66b7d83d91863785a6dad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a89d23372d19daf2d6d4e1c4de732f7864316ed5e7713b1103918303873683e`

```dockerfile
```

-	Layers:
	-	`sha256:099ab2d711ef73783b01895824a4664c7d65e2a333e81237b4766cf053a8f6f0`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 94.2 KB (94246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eccbabf44891af00e622624c5cfd5a295656f82f1c15073b240ac34d47af96c`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.42-trixie`

```console
$ docker pull memcached@sha256:e2a8683c7fbb73d12dce8082525adf9df857765970e639bd9f4705acc31dfcba
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

### `memcached:1.6.42-trixie` - linux; amd64

```console
$ docker pull memcached@sha256:3e079a2fc4232b10565b9bc19139292f16ef304297d4560f08f642f5f2d7a6a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32204836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ab1d39869e17aa04a25df4af0b5bf28a973d4f965635b067471bb44adbdc01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:21:34 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:21:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:24:28 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:24:28 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:24:28 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:24:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:24:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:24:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:24:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:24:28 GMT
USER memcache
# Wed, 24 Jun 2026 01:24:28 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:24:28 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1213ec9c2c2febafa221ff6195f27ea10c675acbc71d21fcc0d2b2ade3f5f74b`  
		Last Modified: Wed, 24 Jun 2026 01:24:34 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3266f17f87ca1b46b5c4fde9dd99707e3827b91b70059e7031ef53abd47fb12c`  
		Last Modified: Wed, 24 Jun 2026 01:24:34 GMT  
		Size: 136.7 KB (136688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a006226c9ea4b6f900685ceec0bda7162e03f436f1b312db9c6ba0d5b47919c7`  
		Last Modified: Wed, 24 Jun 2026 01:24:35 GMT  
		Size: 2.3 MB (2281216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3fd586859c95b544309532471aaabcf797408c5d017bd900b8e4c56c911367`  
		Last Modified: Wed, 24 Jun 2026 01:24:34 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2160167316cd327104547209c9d482373032078e07bb8a6a1e807f7e415571`  
		Last Modified: Wed, 24 Jun 2026 01:24:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:78b554b9b0edb7e45697fbdc7fb7bd3b9facbf500f3f955b3e21628a2469b659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97077f9e00ac4cde9ecb4dba83482ab83cfb8c9378171bf96fc076cc86a64a7`

```dockerfile
```

-	Layers:
	-	`sha256:0f81896f32bd3f922ecc9c3921e78406158e32af9b86b0bc711b5381f977f1e1`  
		Last Modified: Wed, 24 Jun 2026 01:24:35 GMT  
		Size: 2.0 MB (2008368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2714f45af9d9661f076eb378c43b8c30b2b1556e38d5573a646c9df3faae7740`  
		Last Modified: Wed, 24 Jun 2026 01:24:34 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:07d3a299e990256fef486b7259267b9140a71a6003c6b138f0629c06e8eab05a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30316687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3763f93158d93525ae099ec31b8c33c6f309d88e3e96f8e6e18ba87c3f5c18`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:14:31 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:14:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:17:52 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:17:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:17:52 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:17:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:17:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:17:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:17:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:17:52 GMT
USER memcache
# Wed, 24 Jun 2026 01:17:52 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:17:52 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:da43bc6a07a9cd7cc23faa538adc0797482747316b5a85b9f3f94ed17f6c1a2a`  
		Last Modified: Wed, 24 Jun 2026 00:28:12 GMT  
		Size: 28.0 MB (27959221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72b0a4d36a2a621f7921b07bce6fd125f5f5dcef47bd823dc4e31290e3e2399`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4e24ea733891c84a840e31af3fb0b9c15056a407cdc805d54c8cfd3e6ef6f0`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 144.2 KB (144157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64639d0df1b35e7dbd196efee0fd423d0a736ac6c863e17f7d6986420c041af8`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 2.2 MB (2211796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090c9d3495cd22555152f5b251e3f1fe30e588646fcac43f30a778eb73470f8e`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02db167b638147d6fc9f87b04a310ffd4b96fc41da3f61194b9525811486129`  
		Last Modified: Wed, 24 Jun 2026 01:18:00 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:b276ce09ef33302e7b98984a8b1515cd0c83190274b6163f2a28f2d539cc4a7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:390cd34082323b589abd9a85a9cf2513c80fd64085a0a6aa744e0b297aa7a4b5`

```dockerfile
```

-	Layers:
	-	`sha256:259590638c0e780d766f685e7f3a057b89c4575e1736e106d88bcbd2e7c345cb`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 2.0 MB (2011371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd7d6f82a916ba666327037ebdcdce8491adee8668fde99a67161383e1bdaf64`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:e2be04c60636f94c2c1555f324fd58c8ed1cca98bfc5721d5d00a8357a7df461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28513245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc5b22192f1fe06b621ee612a1428f71028d4702873f593a6e3f1896b5c7edfd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:19:26 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:19:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:22:38 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:22:38 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:22:38 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:22:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:22:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:22:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:22:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:22:38 GMT
USER memcache
# Wed, 24 Jun 2026 01:22:38 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:22:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:81c84b0273952340067af970e1fe77a42ea83b4ed1a53319e258d5f1077848f0`  
		Last Modified: Wed, 24 Jun 2026 00:28:38 GMT  
		Size: 26.2 MB (26211051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0642cf323abcb26caa4c3ff3b7e80d0d7d6d9f6d9d9accdcf6d336f41426f102`  
		Last Modified: Wed, 24 Jun 2026 01:22:44 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2360e1299ad9a74124543c81dfb5655cf827191bca3b68df2bfa35cef12ff4c6`  
		Last Modified: Wed, 24 Jun 2026 01:22:44 GMT  
		Size: 135.4 KB (135381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa1e7d2a4dedc5e64f5906cba5d754b8a704705fc6875aa2c6e19fbf32e80d0`  
		Last Modified: Wed, 24 Jun 2026 01:22:45 GMT  
		Size: 2.2 MB (2165300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1110dbe0eb2a934122b522315e135c97a24e58dfe0d85799fa581bed83010517`  
		Last Modified: Wed, 24 Jun 2026 01:22:44 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6a4eee2665c4591534d0fb4f767664091dd2025201db5c28be41b6cde451d4`  
		Last Modified: Wed, 24 Jun 2026 01:22:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:69daaf7d08ee571ea31fa5ba2bbed9ee75e05eaa0e828fec25bcbbb5db45e674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ce76762dc893723cf043776255f735aa512c188d67735932b74d4347be6e02d`

```dockerfile
```

-	Layers:
	-	`sha256:bd51ee9d8e158fbc8c58b5d3ec9bb91d9e9adb533d51ef67ba795e241a2a1486`  
		Last Modified: Wed, 24 Jun 2026 01:22:45 GMT  
		Size: 2.0 MB (2009828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce07aa39f2cbf08f3885676ecfd34bf02f971dd10ba62db2f161f39e032df30d`  
		Last Modified: Wed, 24 Jun 2026 01:22:44 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ce9daf8b2144b701cf7e968ab341768bb2d3efa2a4c64d02da0a0de42c56f1bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32566611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cc2b42a078d89f4b7328abbd61b2cc235e3c733db4c018c8c232c8e3c8dac40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:22:00 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:22:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:25:00 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:25:00 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:25:00 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:25:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:25:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:25:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:25:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:25:00 GMT
USER memcache
# Wed, 24 Jun 2026 01:25:00 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:25:00 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45863abe59cf630e20caf87380378a813615419b3e0f3a8f6649855538dd606`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b7dfd57d8e29e17a7f5191adae69420144fe599879e351b48979971c36f465`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 153.5 KB (153487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be9b72bcf7171564f265414becff9bc077025e30b3f602008e49e51af592400`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 2.3 MB (2263062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff542c356a684239a022d62e5a51aa3f8884a5a1c5a7125cd5d4133c8bac04a`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf0b844cb30e05fdae9181c546555144b913389d03c3ed5549c809d6d4f5cb5`  
		Last Modified: Wed, 24 Jun 2026 01:25:07 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:4b6ea06e8e33c13f6ed836c0f565b1bb81217e79880acaac6b7ad6c4ae57a35d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d49fd2b1e37fca3ad0e2c2747ad1ffa5e40f4dac971d3d382bb685ad2cbeb75`

```dockerfile
```

-	Layers:
	-	`sha256:0749a7c57e354ea8640b297fd510a9c6b05145e740a4d1747f3d832d71878a63`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 2.0 MB (2008676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31dad526561e0628b5270544aa1a9c883fbecd2e25a9770bf262407c2e0bf810`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-trixie` - linux; 386

```console
$ docker pull memcached@sha256:b2916cadce1269827ce2769d75e850a06fa02e2b29d606a5300c10859def3696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33675687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c903111eaced6eb842f558accf95d8d210049b93dfdce69195cb596a9295aa2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:17:36 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:17:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:20:39 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:20:39 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:20:39 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:20:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:20:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:20:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:20:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:20:39 GMT
USER memcache
# Wed, 24 Jun 2026 01:20:39 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:20:39 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:984d3baa100eb8c4d7c83b7c23b4748e508aa6ed5903297f02be90a681f52d41`  
		Last Modified: Wed, 24 Jun 2026 00:28:38 GMT  
		Size: 31.3 MB (31301210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e88a5ba508193f8a40b67d411ba88b51522122e991c5e579f718f03a7b827d5`  
		Last Modified: Wed, 24 Jun 2026 01:20:45 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13a37bd401d9e6fe5c150251a68821160273feb13462cbe401715d4c50bbcee`  
		Last Modified: Wed, 24 Jun 2026 01:20:45 GMT  
		Size: 147.5 KB (147522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f7f30bf297b5062f967e9d807b67dbfcbd20800b75c6daae0ad7fff1edf46e`  
		Last Modified: Wed, 24 Jun 2026 01:20:46 GMT  
		Size: 2.2 MB (2225442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1687fae458633e2c28615b4a2b32841cea0191dc6777aa4ad23de450a9f898e4`  
		Last Modified: Wed, 24 Jun 2026 01:20:45 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc431901c24b9ea4ccb36149baa5b10a412da5738b7f7af9808c7a408caebc12`  
		Last Modified: Wed, 24 Jun 2026 01:20:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:ceb7723388cb240f2eff890796603dfa6d63cb5e7f9e9774cf291a70411779ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596e979ff6ae6cf65094d2e268ad30ecd052f4cb73e4dddeb3644a8b5d4e00b7`

```dockerfile
```

-	Layers:
	-	`sha256:f42e4ebf214a33a305d64952d73fd7dd183f7a9b3c1ee3618be109170351a6f2`  
		Last Modified: Wed, 24 Jun 2026 01:20:45 GMT  
		Size: 2.0 MB (2005525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd85722eeac2901ebcdc4b4970759b139e69583f42cc4b4f5f84fc21347082c0`  
		Last Modified: Wed, 24 Jun 2026 01:20:45 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:f26a6eb2688cfd1f4cf236c411f9988f840b8e69f0d81f925c8c5b375608a5b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36173798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683edb23fb2832c336aa1334780707e8e429ee767b084b9c4ebf1a76eee13670`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:32:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:32:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:35:52 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:35:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:35:52 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:35:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:35:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:35:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:35:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:35:52 GMT
USER memcache
# Wed, 24 Jun 2026 01:35:52 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:35:52 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:639e1c13483ea279c94219be2736856262d8dd2efeff3e6d309f11a66aba21fb`  
		Last Modified: Wed, 24 Jun 2026 00:30:29 GMT  
		Size: 33.6 MB (33606388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d700e36837a63da25a34bd9fef9f7937541cbe617e8c1e9c4a785cc37d6e2e29`  
		Last Modified: Wed, 24 Jun 2026 01:36:14 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7456d8868d48e0b53288836b26930c6efe02b67c099dcefa481778870fc15df`  
		Last Modified: Wed, 24 Jun 2026 01:36:15 GMT  
		Size: 170.4 KB (170375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7daaa467c3a42eb0ea458c5771839433b7c4f773537351a10e30789f995f63`  
		Last Modified: Wed, 24 Jun 2026 01:36:15 GMT  
		Size: 2.4 MB (2395518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a6999cbf05638c0554accc7e8f9d8acd435888a52ad68267fcbd567d8fdce0`  
		Last Modified: Wed, 24 Jun 2026 01:36:14 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5f81262c7fc9478a7854e6dcf5e83a4d09732948b63b45b5d138da7fd57d8c`  
		Last Modified: Wed, 24 Jun 2026 01:36:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:1db8703b08d0d14737d40156d6a09384027af9d6806c94c63763d4b5cd08bc31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9df60db9b699e1540eb1b1a65a79dfffa825cdb8a5c9ce191b5cd53055af17e2`

```dockerfile
```

-	Layers:
	-	`sha256:d207552f6be1ed5a92472733946f240471025ee31516d22f4e4e1710136a5df9`  
		Last Modified: Wed, 24 Jun 2026 01:36:15 GMT  
		Size: 2.0 MB (2011969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2777dc1115238cc20388367ecc331281ddd19f28aafede9028ceb87baaf56ed`  
		Last Modified: Wed, 24 Jun 2026 01:36:14 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:1d09cc6da0fcd7fbfd1eb9a04ab9aeb8557f8a977d85bc7758ddc33f1fae7e8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30626877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e932fab34f25980444b8d9d4042f4f019d633ae41731c4d58de9d0425aacbb5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 20:53:15 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 20:53:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jun 2026 19:11:35 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 25 Jun 2026 19:11:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 25 Jun 2026 19:11:35 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 25 Jun 2026 19:11:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 25 Jun 2026 19:11:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 25 Jun 2026 19:11:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 25 Jun 2026 19:11:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Jun 2026 19:11:35 GMT
USER memcache
# Thu, 25 Jun 2026 19:11:35 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 25 Jun 2026 19:11:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:58bface994ba631e609596a2ca5032d9d75de27f1b6476034b581e226205adab`  
		Last Modified: Wed, 24 Jun 2026 03:41:42 GMT  
		Size: 28.3 MB (28282378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88be0d85b1f48be753592f62cac7ef80c23a61c7848026bd2d489c40d2214a58`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5924e63da94311a18a309f02e655774d7a7dd21bf3dc267215c524167fb7ca02`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 133.1 KB (133093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfa9af5e6df6f7145e6f80ab61869e6613b9f5caa0cfa94788cbf01b3041add`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 2.2 MB (2209890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ace1c66f882f3224670cc80ac0c47197433c688d59a6bad4e5e137d6947a7d9`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470dc087e4a89d9d58d8fa29a67ac089e3c4b569f1c1c79265bfe24ba39500d2`  
		Last Modified: Thu, 25 Jun 2026 19:12:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:10dc6cdb2cd2787d533382c9b0e6ae2f8f3b637c254e1b54762fc75d6b7c2066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173dffb05aa61f0096ec844832f392e17573e61865ef528ee8b742faa7e4b6db`

```dockerfile
```

-	Layers:
	-	`sha256:69ed82bb373c86c8fbec635b83221f89933079ee40e6fcf48418d1a69ca5bb89`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 2.0 MB (2002332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cea64cfdecc1c5a9f3c417e6a679e88cd0613790ff8f658ca9e3ec73325fa9cc`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:6bcf745c9e84c923ee6794f31fd61c321c07e98208661f8f96267b959b19322c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32291924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfeb11440a0b99b60cfece211ea4a2d19eb4c5aa0e27cc119d9930da48bb4a23`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:17:57 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:18:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:21:15 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:21:15 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:21:15 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:21:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:21:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:21:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:21:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:21:16 GMT
USER memcache
# Wed, 24 Jun 2026 01:21:16 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:21:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b6a0af2ceb4b698210b8776157288a3fb06e46aaf75d641139449fcc50ce430d`  
		Last Modified: Wed, 24 Jun 2026 00:28:43 GMT  
		Size: 29.9 MB (29851381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3bba39c5a45464aeb0d1fa775a329c0c537439ee4814281c4fc08a68d8cd584`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a60267637fa53d628133884b458b9c84464d66f87fb587bd54667d3e7c6c0f8`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 140.5 KB (140541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009a2f1905baeb2174621049e700d37eaaf68cda0912ab76762452f73537af8e`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 2.3 MB (2298488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5127e016f9d2a0554de486521914b692af85186039386e058a7e61c9754ef414`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf617d16473cca6af3500948111afc2fce546cd4db4d94441113555d9a9da08`  
		Last Modified: Wed, 24 Jun 2026 01:21:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:2721a3c701c85fd239ef39e576be9973f43c9655cc6cb66fd5bc3dc3ce206166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c4f64b3eb5d1eccd239a9a42a97ae1477a0b589f61e823181e9ab7271116da`

```dockerfile
```

-	Layers:
	-	`sha256:26bfdc43fc003330338d918e59f990463e9e8ceae7dbef48f43cdcb95e0f9b4e`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 2.0 MB (2009805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b9c877b5a220dabf32e1e097a3fb26dc36bad47b1978fb4b39ce7ae5415394f`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine`

```console
$ docker pull memcached@sha256:7381333da6d6ae06e02d8dfc87ee6f2c7cd0a19f7ba048d5efc538d2100e2208
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
$ docker pull memcached@sha256:ce375dd48f976d33bf35beb966cc37f202fd840a90891e58b9e71171fc74174d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5921579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d284e7a8445d8dc70e97c673a8a0175d18f39d5336ccbdfa8b240c0ef3ce4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:15:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:15:18 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:54 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:54 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:54 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb73756dcbbebc424eab53d3adda4d9f64001e7a91272a7b2a834622c08b093`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f0d6a5291334f2b54ec652193cd4e17ee22455b2f3ff3bd9b66acff6436c7b`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 106.1 KB (106066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ac11a8307528096ac745e0ef681b64854bbd012ffdfbce85587153eec73563`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 2.0 MB (1967772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3626493aad85d70a212bc66e9d45db8aef43b4bc662259563f916398165f1e64`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cdcd3f20e3aa439838f5491e6f457a42bad6c80ed9b099313bf79b57a721ea8`  
		Last Modified: Tue, 16 Jun 2026 00:18:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:bb948800301f1cae8e18e317f2b9e85636c86c4a1924ee85e125da37cb1333e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c3e084937eb543038244e151b03b8d9a0dce0b4d5bf87c2d471fa397ed5702`

```dockerfile
```

-	Layers:
	-	`sha256:9d05a792212c92363a76bb6a8205a6e7f386113b3efc1b5d600f93d4e237c975`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 94.9 KB (94897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee0e7e70ef03205f55c68bc1b74ac7854183aee4e871112794975dc852761b19`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:4b144cdbc67c11035b3d0f0c812b590ee694977f2f6a32321e538237bd2f841c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5573158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e9bb70df1535a2f8ca960f733a4404cbde900a13156a1f4446c2fd110258e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:25 GMT
ADD alpine-minirootfs-3.24.1-armhf.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:25 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:14:43 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:14:44 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:47 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:47 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3c4836a46d600cfe9a422adf7a80205cb534097e6213325e0176c51f6e5cc02e`  
		Last Modified: Sun, 14 Jun 2026 06:44:57 GMT  
		Size: 3.6 MB (3553450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e732a60042adf5cff5fe4fe0de83f937f6e5c8896500f7023e8bf68ed0670d65`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad86d1fea29db061a5ae896a0a595b144edcdb4af59deac2b75b0fb8f5fa2d4c`  
		Last Modified: Tue, 16 Jun 2026 00:17:50 GMT  
		Size: 102.6 KB (102624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f26dd2445dbf4d5624417ca290f5ae2e5774fa7fec4f5655cd2377ee3147e4`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 1.9 MB (1915730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080a186f0ca6beb06a5ce4a86fbc71f5b9995713fcc899c73f995f251ef7c987`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c4d4f455f9a2b633cca28e3aa2190e4c42ca83ca6e3ea88ea4abe16944d238`  
		Last Modified: Tue, 16 Jun 2026 00:17:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d6b7abf6ef34abf12ab2c7f84bd29ac2461eb3271d1c4070456ed9b94e4b41a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a767571287c8ca227e321ee8d65f9da82e558098bedbb15888434dcc1ce9fa`

```dockerfile
```

-	Layers:
	-	`sha256:1794ccef4392c0db4ba36ad7fde22cdacbda40f4d56f0adbef802163c87e066c`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:848c5e0ced69b802cca72c23bec05a4c6f23136212a4a1d5cc22b7c8f0154bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286f62a53a8947036e39f2b79567b31d38309fd84c7a39e43de8c5f9817a2f64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:26 GMT
ADD alpine-minirootfs-3.24.1-armv7.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:17:59 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:17:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:20:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:20:56 GMT
USER memcache
# Tue, 16 Jun 2026 00:20:56 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:20:56 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bc03a9e5b4dd452551f246e199537fe7afc1765f53f510bc81d26df9845e4008`  
		Last Modified: Sun, 14 Jun 2026 06:45:22 GMT  
		Size: 3.3 MB (3260615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f0249bacfc8953b72899bf7b6c904c8750482fce4c93108f57b2c64228b279`  
		Last Modified: Tue, 16 Jun 2026 00:21:00 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95e1b321ffc31d01e766d5d1d054967d613940563406fc54ee981926b7f6049`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 92.4 KB (92366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce112e60c1b15077277c233a7707831818dff0a15f1fc977ebebc93f817dad43`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 1.9 MB (1875183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32fa6ed5b14fd6fcf96a7cde2996063f10b8efe802c386479288a232af826027`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6648f8180a4eea1f5197f2fa2d356fbbf4e5f65345e189e720e227af64a5e31`  
		Last Modified: Tue, 16 Jun 2026 00:21:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:59387f31eff7cfb3166c5e6d4bad92e255705affcc15c84c4a06c86ecb1a9890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:174eb460b1df4523a4f71ba5a996f2285fa845fe8ef76d2df3ea8c4962c6b6ca`

```dockerfile
```

-	Layers:
	-	`sha256:4ff5e70775e819cab551295c56b58fdb0c44c105cdc4f72247e3968accd2ab2f`  
		Last Modified: Tue, 16 Jun 2026 00:21:00 GMT  
		Size: 94.3 KB (94315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00f10e1301c7e61396658f7e3ed330e400a9f304c6a0323de8ff644aba987474`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:33261748facce282dbe4dbb4d9f875139680fce4cefc13cb9ad8e1ced23f9557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6250475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1614bb2865c8f849c2bc5bf77703a1ab711695c607a8bc6edb013a076ec16d6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:18 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:16:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:16:06 GMT
USER memcache
# Tue, 16 Jun 2026 00:16:06 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:16:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5faa19f06c4d5e26332739c7f08fd3dcd2c81817471c62029a6d99af6be8748`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377a35d28f00766e2679c788b95b0a67b9aa5a76c8ef701a2a9604e2a00c3b46`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 121.8 KB (121841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0b819e89558d70f1401ca58cbc19c58ae13e15be8184fd9b2733e022f318a4`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 1.9 MB (1944247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca539cef48ff8c3f723ab23506b6786c9ed26a9cac713601b71de2dc775d26a`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4c456deed244daa6d7076f40a1cf0364d294059bb43e533677a89027843b15`  
		Last Modified: Tue, 16 Jun 2026 00:16:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:4d25960abc53b5ba1896b8f5ee04ba5ac1389900ab9b413eb62285af7281aedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d1a4b7ad428a08c8a174d5ecd9763d530e849f54a2d9b90aef934e54b9477d4`

```dockerfile
```

-	Layers:
	-	`sha256:9c0a8e5e07390fae6abe9204450009671011c4d2d5aa5fe4afdd82324fdb49b9`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 94.4 KB (94351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ee01158358d01c082867cf46a5225cf101013e4d5b7eae18fc7853e277ff0f4`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 20.7 KB (20727 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:5436d0ef6e12f2f8e454384ff4a703132b3fe820c41a55336f520bb5d1622574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5702329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8946be3d97c7b9825159f58cbf832b131c75cb90b3fb46a40d5429b9ffe32bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:19 GMT
ADD alpine-minirootfs-3.24.1-x86.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:19 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:59 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:16:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:16:46 GMT
USER memcache
# Tue, 16 Jun 2026 00:16:46 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:16:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f86df9d778509895efbf9363d8fcb0cbe0b772de536c7218e4c4c947f0be879f`  
		Last Modified: Sun, 14 Jun 2026 06:45:46 GMT  
		Size: 3.7 MB (3670141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043137360442e605bc150f28f20e1fa2d23d90131370bc405ad7d35309594491`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900ce6eeaece12033b12f1c8641c33dcf62ff2525584411911368cfcd0b38224`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 110.7 KB (110729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e8cc1c8f6bc6391eb1a43a46f0b55ca7845f824fc0f2fc7ae7587a7715814e`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 1.9 MB (1920111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94f6e4d3be92188fc182a3557fe43af5bc9f3e768a7f265977743a56eea527e`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f8a19f18dfff271426de7a17ab6780788fa4345d5fa0120e6d03720d552bd4`  
		Last Modified: Tue, 16 Jun 2026 00:16:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:00dc6a7f29b7f2f5ac46fc5678b80c43c7b1e46b4ca3c84c5597034180aeb644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de04019c7775544db9adbb4c4558d0e7c842c279e5d70532b2ac0b988ac1345`

```dockerfile
```

-	Layers:
	-	`sha256:80895f8f5e9c9b015e419096426322f4c86c33d55ca8860ee046b61d52782847`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 94.9 KB (94852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c69be8c1f82a066b46cc389712508e85c1dcd77e649c922dba46ace64b343ae`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:c7857941a51b85b136781035703afcc8854a2d70fa2091208a51f8bb7e71f934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5998515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b02b2222212c64e444ac1a2227b19f0cfb1282c8a8ced386c1b79ae48c641b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:15 GMT
ADD alpine-minirootfs-3.24.1-ppc64le.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:15 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:15:37 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:15:38 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:18:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:18:22 GMT
USER memcache
# Tue, 16 Jun 2026 00:18:22 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:18:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3ebcdcd395ccee658b9200e4b27d7699e5d6ed9f6c1858dea12781aac519ff59`  
		Last Modified: Sun, 14 Jun 2026 06:46:36 GMT  
		Size: 3.8 MB (3813400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b108e2058722fb0fb5a9310e8ebe82ab4b9c021228a94b3125ba49d318e9667`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb8160ed736eda8513164d5d703082fb0c9af9e037472ab70a02579caa3eb99`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 126.3 KB (126252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5cb88dd03ce07ecf1613c2aff220fb392763d8f22edc900c4ad032ee7103d34`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 2.1 MB (2057508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12fd57420ca797ab383c58a488044d324c4d43b3c94a848f86a0524ed3064b4`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c0c7b7a77e9375d8a75fb825fa274d9127ca96de79107550517be29501c817`  
		Last Modified: Tue, 16 Jun 2026 00:18:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:851f463d4778539d5e4981f972420f9a57ec2559488f8a59fba6abab6065032f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734dd3d91f2d6cf217233f7a9dacc3c20ff0590246adb790f95713fb21c115de`

```dockerfile
```

-	Layers:
	-	`sha256:c0d4c203ef9f66cf827ec62098d7801e1c49f1187e0fe047fd32fc2a3271f636`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 94.3 KB (94304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b734d170b5463fa77dd77072e06d51a28efe59a53600d47435b015ebcadae92`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:ba5bf40b4adc1fe04f32e2e239fa9c0020d4e89bf4079493f8bc11a92c8f4b51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5738070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d12fbf86d6880aaa9d517425d9cecddcf545ba87e577a039dea9ea99ad53d8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 05:59:15 GMT
ADD alpine-minirootfs-3.24.1-riscv64.tar.gz / # buildkit
# Tue, 16 Jun 2026 05:59:15 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 08:28:27 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 19 Jun 2026 08:28:31 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_VERSION=1.6.42
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Fri, 19 Jun 2026 08:41:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 19 Jun 2026 08:41:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 08:41:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 19 Jun 2026 08:41:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 08:41:53 GMT
USER memcache
# Fri, 19 Jun 2026 08:41:53 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 19 Jun 2026 08:41:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c34e5222b29b86391cdae95b0473ef789493ff1a0068a3a30b5d66f544bd7cf6`  
		Last Modified: Sun, 14 Jun 2026 06:47:00 GMT  
		Size: 3.6 MB (3574358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09d95a0f414638430c0cd3ecfdcce75606201917a27c7cb2ce1e34cb928b26a`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5335c7af79a1b08af55862ba77644afdae5544d9a7871e45c91b364bd4f71d`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 108.9 KB (108888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3622a6ea71515db1ef566afdbb121daed1f408aacf1519f4173b40dabe2ae627`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 2.1 MB (2053467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1db0e3e31ca3f2830f5404436e92b1862a4078adefacacec09a9580a3ad0a2`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1463b0fd26a37659aaad7f99696e5213764ad03bb094f40836c3309713d7a60`  
		Last Modified: Fri, 19 Jun 2026 08:42:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:aadb3b9338400b87692f95e00931e43940f8d6ddd13f046bd256848dd825e458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde4b5a4a468d795a5f58dd934b371adfe72cd2ae24e166e1258ad65aa455a56`

```dockerfile
```

-	Layers:
	-	`sha256:debb70180cf674562f7ca321270e3dfa350c5d1596c05dbfcc27b38c65652528`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 94.3 KB (94300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a895bbe0bfec24678c1c92ddd283cb7392e0e8d229f31c769a23c95224c0d371`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; s390x

```console
$ docker pull memcached@sha256:e1b640e8d192055e5c3ccd05b077776a0f4d35664191596f7a8230b2cd7ef0f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5823313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ef6221f9c2854683b0633325a98a0e7a0d3b7d865b02d7cdf4c1d49d2e5090`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:21 GMT
ADD alpine-minirootfs-3.24.1-s390x.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:21 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:46 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:12 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:da43be6afaaa3ec1b607461ce64380942a6d76c3d52cda4337b0770d9a96fa89`  
		Last Modified: Sun, 14 Jun 2026 06:47:25 GMT  
		Size: 3.7 MB (3709320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757d04238e02c9bbe1cfd4030cc19e29421650a1b1562a8ca4090d90e9ae17b0`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1949e0fa71fc91bebf4f2e4293108b27de8357d98f98b673bc4f3ed1980b52c`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 114.3 KB (114289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f0e22966bce79fbc8a20f7c27aa07ce63229bb50181319c810ca29f1fb4032`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 2.0 MB (1998350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15eb5e912ef8ec6e3abe76c361cdddb568d20a60be21be379d4d8d7d0ebaa11e`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a549d59ad0d4761ac6f4cca272c4bea521471ed091d0e79143bfda8ff29cf9ce`  
		Last Modified: Tue, 16 Jun 2026 00:17:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:6dbf7c8a98f02a949769403ad1c92583b34a28dccc66b7d83d91863785a6dad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a89d23372d19daf2d6d4e1c4de732f7864316ed5e7713b1103918303873683e`

```dockerfile
```

-	Layers:
	-	`sha256:099ab2d711ef73783b01895824a4664c7d65e2a333e81237b4766cf053a8f6f0`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 94.2 KB (94246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eccbabf44891af00e622624c5cfd5a295656f82f1c15073b240ac34d47af96c`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine3.24`

```console
$ docker pull memcached@sha256:7381333da6d6ae06e02d8dfc87ee6f2c7cd0a19f7ba048d5efc538d2100e2208
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

### `memcached:alpine3.24` - linux; amd64

```console
$ docker pull memcached@sha256:ce375dd48f976d33bf35beb966cc37f202fd840a90891e58b9e71171fc74174d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5921579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d284e7a8445d8dc70e97c673a8a0175d18f39d5336ccbdfa8b240c0ef3ce4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:15:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:15:18 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:54 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:54 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:54 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb73756dcbbebc424eab53d3adda4d9f64001e7a91272a7b2a834622c08b093`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f0d6a5291334f2b54ec652193cd4e17ee22455b2f3ff3bd9b66acff6436c7b`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 106.1 KB (106066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ac11a8307528096ac745e0ef681b64854bbd012ffdfbce85587153eec73563`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 2.0 MB (1967772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3626493aad85d70a212bc66e9d45db8aef43b4bc662259563f916398165f1e64`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cdcd3f20e3aa439838f5491e6f457a42bad6c80ed9b099313bf79b57a721ea8`  
		Last Modified: Tue, 16 Jun 2026 00:18:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:bb948800301f1cae8e18e317f2b9e85636c86c4a1924ee85e125da37cb1333e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c3e084937eb543038244e151b03b8d9a0dce0b4d5bf87c2d471fa397ed5702`

```dockerfile
```

-	Layers:
	-	`sha256:9d05a792212c92363a76bb6a8205a6e7f386113b3efc1b5d600f93d4e237c975`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 94.9 KB (94897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee0e7e70ef03205f55c68bc1b74ac7854183aee4e871112794975dc852761b19`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.24` - linux; arm variant v6

```console
$ docker pull memcached@sha256:4b144cdbc67c11035b3d0f0c812b590ee694977f2f6a32321e538237bd2f841c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5573158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e9bb70df1535a2f8ca960f733a4404cbde900a13156a1f4446c2fd110258e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:25 GMT
ADD alpine-minirootfs-3.24.1-armhf.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:25 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:14:43 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:14:44 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:47 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:47 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3c4836a46d600cfe9a422adf7a80205cb534097e6213325e0176c51f6e5cc02e`  
		Last Modified: Sun, 14 Jun 2026 06:44:57 GMT  
		Size: 3.6 MB (3553450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e732a60042adf5cff5fe4fe0de83f937f6e5c8896500f7023e8bf68ed0670d65`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad86d1fea29db061a5ae896a0a595b144edcdb4af59deac2b75b0fb8f5fa2d4c`  
		Last Modified: Tue, 16 Jun 2026 00:17:50 GMT  
		Size: 102.6 KB (102624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f26dd2445dbf4d5624417ca290f5ae2e5774fa7fec4f5655cd2377ee3147e4`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 1.9 MB (1915730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080a186f0ca6beb06a5ce4a86fbc71f5b9995713fcc899c73f995f251ef7c987`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c4d4f455f9a2b633cca28e3aa2190e4c42ca83ca6e3ea88ea4abe16944d238`  
		Last Modified: Tue, 16 Jun 2026 00:17:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:d6b7abf6ef34abf12ab2c7f84bd29ac2461eb3271d1c4070456ed9b94e4b41a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a767571287c8ca227e321ee8d65f9da82e558098bedbb15888434dcc1ce9fa`

```dockerfile
```

-	Layers:
	-	`sha256:1794ccef4392c0db4ba36ad7fde22cdacbda40f4d56f0adbef802163c87e066c`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.24` - linux; arm variant v7

```console
$ docker pull memcached@sha256:848c5e0ced69b802cca72c23bec05a4c6f23136212a4a1d5cc22b7c8f0154bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286f62a53a8947036e39f2b79567b31d38309fd84c7a39e43de8c5f9817a2f64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:26 GMT
ADD alpine-minirootfs-3.24.1-armv7.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:17:59 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:17:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:20:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:20:56 GMT
USER memcache
# Tue, 16 Jun 2026 00:20:56 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:20:56 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bc03a9e5b4dd452551f246e199537fe7afc1765f53f510bc81d26df9845e4008`  
		Last Modified: Sun, 14 Jun 2026 06:45:22 GMT  
		Size: 3.3 MB (3260615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f0249bacfc8953b72899bf7b6c904c8750482fce4c93108f57b2c64228b279`  
		Last Modified: Tue, 16 Jun 2026 00:21:00 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95e1b321ffc31d01e766d5d1d054967d613940563406fc54ee981926b7f6049`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 92.4 KB (92366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce112e60c1b15077277c233a7707831818dff0a15f1fc977ebebc93f817dad43`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 1.9 MB (1875183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32fa6ed5b14fd6fcf96a7cde2996063f10b8efe802c386479288a232af826027`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6648f8180a4eea1f5197f2fa2d356fbbf4e5f65345e189e720e227af64a5e31`  
		Last Modified: Tue, 16 Jun 2026 00:21:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:59387f31eff7cfb3166c5e6d4bad92e255705affcc15c84c4a06c86ecb1a9890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:174eb460b1df4523a4f71ba5a996f2285fa845fe8ef76d2df3ea8c4962c6b6ca`

```dockerfile
```

-	Layers:
	-	`sha256:4ff5e70775e819cab551295c56b58fdb0c44c105cdc4f72247e3968accd2ab2f`  
		Last Modified: Tue, 16 Jun 2026 00:21:00 GMT  
		Size: 94.3 KB (94315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00f10e1301c7e61396658f7e3ed330e400a9f304c6a0323de8ff644aba987474`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.24` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:33261748facce282dbe4dbb4d9f875139680fce4cefc13cb9ad8e1ced23f9557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6250475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1614bb2865c8f849c2bc5bf77703a1ab711695c607a8bc6edb013a076ec16d6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:18 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:16:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:16:06 GMT
USER memcache
# Tue, 16 Jun 2026 00:16:06 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:16:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5faa19f06c4d5e26332739c7f08fd3dcd2c81817471c62029a6d99af6be8748`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377a35d28f00766e2679c788b95b0a67b9aa5a76c8ef701a2a9604e2a00c3b46`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 121.8 KB (121841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0b819e89558d70f1401ca58cbc19c58ae13e15be8184fd9b2733e022f318a4`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 1.9 MB (1944247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca539cef48ff8c3f723ab23506b6786c9ed26a9cac713601b71de2dc775d26a`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4c456deed244daa6d7076f40a1cf0364d294059bb43e533677a89027843b15`  
		Last Modified: Tue, 16 Jun 2026 00:16:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:4d25960abc53b5ba1896b8f5ee04ba5ac1389900ab9b413eb62285af7281aedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d1a4b7ad428a08c8a174d5ecd9763d530e849f54a2d9b90aef934e54b9477d4`

```dockerfile
```

-	Layers:
	-	`sha256:9c0a8e5e07390fae6abe9204450009671011c4d2d5aa5fe4afdd82324fdb49b9`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 94.4 KB (94351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ee01158358d01c082867cf46a5225cf101013e4d5b7eae18fc7853e277ff0f4`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 20.7 KB (20727 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.24` - linux; 386

```console
$ docker pull memcached@sha256:5436d0ef6e12f2f8e454384ff4a703132b3fe820c41a55336f520bb5d1622574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5702329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8946be3d97c7b9825159f58cbf832b131c75cb90b3fb46a40d5429b9ffe32bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:19 GMT
ADD alpine-minirootfs-3.24.1-x86.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:19 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:59 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:16:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:16:46 GMT
USER memcache
# Tue, 16 Jun 2026 00:16:46 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:16:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f86df9d778509895efbf9363d8fcb0cbe0b772de536c7218e4c4c947f0be879f`  
		Last Modified: Sun, 14 Jun 2026 06:45:46 GMT  
		Size: 3.7 MB (3670141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043137360442e605bc150f28f20e1fa2d23d90131370bc405ad7d35309594491`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900ce6eeaece12033b12f1c8641c33dcf62ff2525584411911368cfcd0b38224`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 110.7 KB (110729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e8cc1c8f6bc6391eb1a43a46f0b55ca7845f824fc0f2fc7ae7587a7715814e`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 1.9 MB (1920111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94f6e4d3be92188fc182a3557fe43af5bc9f3e768a7f265977743a56eea527e`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f8a19f18dfff271426de7a17ab6780788fa4345d5fa0120e6d03720d552bd4`  
		Last Modified: Tue, 16 Jun 2026 00:16:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:00dc6a7f29b7f2f5ac46fc5678b80c43c7b1e46b4ca3c84c5597034180aeb644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de04019c7775544db9adbb4c4558d0e7c842c279e5d70532b2ac0b988ac1345`

```dockerfile
```

-	Layers:
	-	`sha256:80895f8f5e9c9b015e419096426322f4c86c33d55ca8860ee046b61d52782847`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 94.9 KB (94852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c69be8c1f82a066b46cc389712508e85c1dcd77e649c922dba46ace64b343ae`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.24` - linux; ppc64le

```console
$ docker pull memcached@sha256:c7857941a51b85b136781035703afcc8854a2d70fa2091208a51f8bb7e71f934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5998515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b02b2222212c64e444ac1a2227b19f0cfb1282c8a8ced386c1b79ae48c641b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:15 GMT
ADD alpine-minirootfs-3.24.1-ppc64le.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:15 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:15:37 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:15:38 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:18:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:18:22 GMT
USER memcache
# Tue, 16 Jun 2026 00:18:22 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:18:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3ebcdcd395ccee658b9200e4b27d7699e5d6ed9f6c1858dea12781aac519ff59`  
		Last Modified: Sun, 14 Jun 2026 06:46:36 GMT  
		Size: 3.8 MB (3813400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b108e2058722fb0fb5a9310e8ebe82ab4b9c021228a94b3125ba49d318e9667`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb8160ed736eda8513164d5d703082fb0c9af9e037472ab70a02579caa3eb99`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 126.3 KB (126252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5cb88dd03ce07ecf1613c2aff220fb392763d8f22edc900c4ad032ee7103d34`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 2.1 MB (2057508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12fd57420ca797ab383c58a488044d324c4d43b3c94a848f86a0524ed3064b4`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c0c7b7a77e9375d8a75fb825fa274d9127ca96de79107550517be29501c817`  
		Last Modified: Tue, 16 Jun 2026 00:18:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:851f463d4778539d5e4981f972420f9a57ec2559488f8a59fba6abab6065032f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734dd3d91f2d6cf217233f7a9dacc3c20ff0590246adb790f95713fb21c115de`

```dockerfile
```

-	Layers:
	-	`sha256:c0d4c203ef9f66cf827ec62098d7801e1c49f1187e0fe047fd32fc2a3271f636`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 94.3 KB (94304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b734d170b5463fa77dd77072e06d51a28efe59a53600d47435b015ebcadae92`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.24` - linux; riscv64

```console
$ docker pull memcached@sha256:ba5bf40b4adc1fe04f32e2e239fa9c0020d4e89bf4079493f8bc11a92c8f4b51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5738070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d12fbf86d6880aaa9d517425d9cecddcf545ba87e577a039dea9ea99ad53d8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 05:59:15 GMT
ADD alpine-minirootfs-3.24.1-riscv64.tar.gz / # buildkit
# Tue, 16 Jun 2026 05:59:15 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 08:28:27 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 19 Jun 2026 08:28:31 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_VERSION=1.6.42
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Fri, 19 Jun 2026 08:41:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 19 Jun 2026 08:41:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 08:41:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 19 Jun 2026 08:41:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 08:41:53 GMT
USER memcache
# Fri, 19 Jun 2026 08:41:53 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 19 Jun 2026 08:41:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c34e5222b29b86391cdae95b0473ef789493ff1a0068a3a30b5d66f544bd7cf6`  
		Last Modified: Sun, 14 Jun 2026 06:47:00 GMT  
		Size: 3.6 MB (3574358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09d95a0f414638430c0cd3ecfdcce75606201917a27c7cb2ce1e34cb928b26a`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5335c7af79a1b08af55862ba77644afdae5544d9a7871e45c91b364bd4f71d`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 108.9 KB (108888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3622a6ea71515db1ef566afdbb121daed1f408aacf1519f4173b40dabe2ae627`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 2.1 MB (2053467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1db0e3e31ca3f2830f5404436e92b1862a4078adefacacec09a9580a3ad0a2`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1463b0fd26a37659aaad7f99696e5213764ad03bb094f40836c3309713d7a60`  
		Last Modified: Fri, 19 Jun 2026 08:42:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:aadb3b9338400b87692f95e00931e43940f8d6ddd13f046bd256848dd825e458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde4b5a4a468d795a5f58dd934b371adfe72cd2ae24e166e1258ad65aa455a56`

```dockerfile
```

-	Layers:
	-	`sha256:debb70180cf674562f7ca321270e3dfa350c5d1596c05dbfcc27b38c65652528`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 94.3 KB (94300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a895bbe0bfec24678c1c92ddd283cb7392e0e8d229f31c769a23c95224c0d371`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.24` - linux; s390x

```console
$ docker pull memcached@sha256:e1b640e8d192055e5c3ccd05b077776a0f4d35664191596f7a8230b2cd7ef0f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5823313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ef6221f9c2854683b0633325a98a0e7a0d3b7d865b02d7cdf4c1d49d2e5090`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:21 GMT
ADD alpine-minirootfs-3.24.1-s390x.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:21 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:46 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:12 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:da43be6afaaa3ec1b607461ce64380942a6d76c3d52cda4337b0770d9a96fa89`  
		Last Modified: Sun, 14 Jun 2026 06:47:25 GMT  
		Size: 3.7 MB (3709320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757d04238e02c9bbe1cfd4030cc19e29421650a1b1562a8ca4090d90e9ae17b0`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1949e0fa71fc91bebf4f2e4293108b27de8357d98f98b673bc4f3ed1980b52c`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 114.3 KB (114289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f0e22966bce79fbc8a20f7c27aa07ce63229bb50181319c810ca29f1fb4032`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 2.0 MB (1998350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15eb5e912ef8ec6e3abe76c361cdddb568d20a60be21be379d4d8d7d0ebaa11e`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a549d59ad0d4761ac6f4cca272c4bea521471ed091d0e79143bfda8ff29cf9ce`  
		Last Modified: Tue, 16 Jun 2026 00:17:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:6dbf7c8a98f02a949769403ad1c92583b34a28dccc66b7d83d91863785a6dad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a89d23372d19daf2d6d4e1c4de732f7864316ed5e7713b1103918303873683e`

```dockerfile
```

-	Layers:
	-	`sha256:099ab2d711ef73783b01895824a4664c7d65e2a333e81237b4766cf053a8f6f0`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 94.2 KB (94246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eccbabf44891af00e622624c5cfd5a295656f82f1c15073b240ac34d47af96c`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:latest`

```console
$ docker pull memcached@sha256:e2a8683c7fbb73d12dce8082525adf9df857765970e639bd9f4705acc31dfcba
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
$ docker pull memcached@sha256:3e079a2fc4232b10565b9bc19139292f16ef304297d4560f08f642f5f2d7a6a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32204836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ab1d39869e17aa04a25df4af0b5bf28a973d4f965635b067471bb44adbdc01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:21:34 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:21:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:24:28 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:24:28 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:24:28 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:24:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:24:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:24:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:24:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:24:28 GMT
USER memcache
# Wed, 24 Jun 2026 01:24:28 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:24:28 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1213ec9c2c2febafa221ff6195f27ea10c675acbc71d21fcc0d2b2ade3f5f74b`  
		Last Modified: Wed, 24 Jun 2026 01:24:34 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3266f17f87ca1b46b5c4fde9dd99707e3827b91b70059e7031ef53abd47fb12c`  
		Last Modified: Wed, 24 Jun 2026 01:24:34 GMT  
		Size: 136.7 KB (136688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a006226c9ea4b6f900685ceec0bda7162e03f436f1b312db9c6ba0d5b47919c7`  
		Last Modified: Wed, 24 Jun 2026 01:24:35 GMT  
		Size: 2.3 MB (2281216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3fd586859c95b544309532471aaabcf797408c5d017bd900b8e4c56c911367`  
		Last Modified: Wed, 24 Jun 2026 01:24:34 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2160167316cd327104547209c9d482373032078e07bb8a6a1e807f7e415571`  
		Last Modified: Wed, 24 Jun 2026 01:24:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:78b554b9b0edb7e45697fbdc7fb7bd3b9facbf500f3f955b3e21628a2469b659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97077f9e00ac4cde9ecb4dba83482ab83cfb8c9378171bf96fc076cc86a64a7`

```dockerfile
```

-	Layers:
	-	`sha256:0f81896f32bd3f922ecc9c3921e78406158e32af9b86b0bc711b5381f977f1e1`  
		Last Modified: Wed, 24 Jun 2026 01:24:35 GMT  
		Size: 2.0 MB (2008368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2714f45af9d9661f076eb378c43b8c30b2b1556e38d5573a646c9df3faae7740`  
		Last Modified: Wed, 24 Jun 2026 01:24:34 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:07d3a299e990256fef486b7259267b9140a71a6003c6b138f0629c06e8eab05a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30316687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3763f93158d93525ae099ec31b8c33c6f309d88e3e96f8e6e18ba87c3f5c18`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:14:31 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:14:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:17:52 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:17:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:17:52 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:17:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:17:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:17:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:17:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:17:52 GMT
USER memcache
# Wed, 24 Jun 2026 01:17:52 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:17:52 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:da43bc6a07a9cd7cc23faa538adc0797482747316b5a85b9f3f94ed17f6c1a2a`  
		Last Modified: Wed, 24 Jun 2026 00:28:12 GMT  
		Size: 28.0 MB (27959221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72b0a4d36a2a621f7921b07bce6fd125f5f5dcef47bd823dc4e31290e3e2399`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4e24ea733891c84a840e31af3fb0b9c15056a407cdc805d54c8cfd3e6ef6f0`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 144.2 KB (144157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64639d0df1b35e7dbd196efee0fd423d0a736ac6c863e17f7d6986420c041af8`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 2.2 MB (2211796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090c9d3495cd22555152f5b251e3f1fe30e588646fcac43f30a778eb73470f8e`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02db167b638147d6fc9f87b04a310ffd4b96fc41da3f61194b9525811486129`  
		Last Modified: Wed, 24 Jun 2026 01:18:00 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:b276ce09ef33302e7b98984a8b1515cd0c83190274b6163f2a28f2d539cc4a7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:390cd34082323b589abd9a85a9cf2513c80fd64085a0a6aa744e0b297aa7a4b5`

```dockerfile
```

-	Layers:
	-	`sha256:259590638c0e780d766f685e7f3a057b89c4575e1736e106d88bcbd2e7c345cb`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 2.0 MB (2011371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd7d6f82a916ba666327037ebdcdce8491adee8668fde99a67161383e1bdaf64`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v7

```console
$ docker pull memcached@sha256:e2be04c60636f94c2c1555f324fd58c8ed1cca98bfc5721d5d00a8357a7df461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28513245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc5b22192f1fe06b621ee612a1428f71028d4702873f593a6e3f1896b5c7edfd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:19:26 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:19:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:22:38 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:22:38 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:22:38 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:22:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:22:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:22:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:22:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:22:38 GMT
USER memcache
# Wed, 24 Jun 2026 01:22:38 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:22:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:81c84b0273952340067af970e1fe77a42ea83b4ed1a53319e258d5f1077848f0`  
		Last Modified: Wed, 24 Jun 2026 00:28:38 GMT  
		Size: 26.2 MB (26211051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0642cf323abcb26caa4c3ff3b7e80d0d7d6d9f6d9d9accdcf6d336f41426f102`  
		Last Modified: Wed, 24 Jun 2026 01:22:44 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2360e1299ad9a74124543c81dfb5655cf827191bca3b68df2bfa35cef12ff4c6`  
		Last Modified: Wed, 24 Jun 2026 01:22:44 GMT  
		Size: 135.4 KB (135381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa1e7d2a4dedc5e64f5906cba5d754b8a704705fc6875aa2c6e19fbf32e80d0`  
		Last Modified: Wed, 24 Jun 2026 01:22:45 GMT  
		Size: 2.2 MB (2165300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1110dbe0eb2a934122b522315e135c97a24e58dfe0d85799fa581bed83010517`  
		Last Modified: Wed, 24 Jun 2026 01:22:44 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6a4eee2665c4591534d0fb4f767664091dd2025201db5c28be41b6cde451d4`  
		Last Modified: Wed, 24 Jun 2026 01:22:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:69daaf7d08ee571ea31fa5ba2bbed9ee75e05eaa0e828fec25bcbbb5db45e674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ce76762dc893723cf043776255f735aa512c188d67735932b74d4347be6e02d`

```dockerfile
```

-	Layers:
	-	`sha256:bd51ee9d8e158fbc8c58b5d3ec9bb91d9e9adb533d51ef67ba795e241a2a1486`  
		Last Modified: Wed, 24 Jun 2026 01:22:45 GMT  
		Size: 2.0 MB (2009828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce07aa39f2cbf08f3885676ecfd34bf02f971dd10ba62db2f161f39e032df30d`  
		Last Modified: Wed, 24 Jun 2026 01:22:44 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ce9daf8b2144b701cf7e968ab341768bb2d3efa2a4c64d02da0a0de42c56f1bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32566611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cc2b42a078d89f4b7328abbd61b2cc235e3c733db4c018c8c232c8e3c8dac40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:22:00 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:22:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:25:00 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:25:00 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:25:00 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:25:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:25:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:25:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:25:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:25:00 GMT
USER memcache
# Wed, 24 Jun 2026 01:25:00 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:25:00 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45863abe59cf630e20caf87380378a813615419b3e0f3a8f6649855538dd606`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b7dfd57d8e29e17a7f5191adae69420144fe599879e351b48979971c36f465`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 153.5 KB (153487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be9b72bcf7171564f265414becff9bc077025e30b3f602008e49e51af592400`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 2.3 MB (2263062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff542c356a684239a022d62e5a51aa3f8884a5a1c5a7125cd5d4133c8bac04a`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf0b844cb30e05fdae9181c546555144b913389d03c3ed5549c809d6d4f5cb5`  
		Last Modified: Wed, 24 Jun 2026 01:25:07 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:4b6ea06e8e33c13f6ed836c0f565b1bb81217e79880acaac6b7ad6c4ae57a35d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d49fd2b1e37fca3ad0e2c2747ad1ffa5e40f4dac971d3d382bb685ad2cbeb75`

```dockerfile
```

-	Layers:
	-	`sha256:0749a7c57e354ea8640b297fd510a9c6b05145e740a4d1747f3d832d71878a63`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 2.0 MB (2008676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31dad526561e0628b5270544aa1a9c883fbecd2e25a9770bf262407c2e0bf810`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:b2916cadce1269827ce2769d75e850a06fa02e2b29d606a5300c10859def3696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33675687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c903111eaced6eb842f558accf95d8d210049b93dfdce69195cb596a9295aa2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:17:36 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:17:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:20:39 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:20:39 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:20:39 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:20:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:20:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:20:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:20:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:20:39 GMT
USER memcache
# Wed, 24 Jun 2026 01:20:39 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:20:39 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:984d3baa100eb8c4d7c83b7c23b4748e508aa6ed5903297f02be90a681f52d41`  
		Last Modified: Wed, 24 Jun 2026 00:28:38 GMT  
		Size: 31.3 MB (31301210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e88a5ba508193f8a40b67d411ba88b51522122e991c5e579f718f03a7b827d5`  
		Last Modified: Wed, 24 Jun 2026 01:20:45 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13a37bd401d9e6fe5c150251a68821160273feb13462cbe401715d4c50bbcee`  
		Last Modified: Wed, 24 Jun 2026 01:20:45 GMT  
		Size: 147.5 KB (147522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f7f30bf297b5062f967e9d807b67dbfcbd20800b75c6daae0ad7fff1edf46e`  
		Last Modified: Wed, 24 Jun 2026 01:20:46 GMT  
		Size: 2.2 MB (2225442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1687fae458633e2c28615b4a2b32841cea0191dc6777aa4ad23de450a9f898e4`  
		Last Modified: Wed, 24 Jun 2026 01:20:45 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc431901c24b9ea4ccb36149baa5b10a412da5738b7f7af9808c7a408caebc12`  
		Last Modified: Wed, 24 Jun 2026 01:20:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:ceb7723388cb240f2eff890796603dfa6d63cb5e7f9e9774cf291a70411779ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596e979ff6ae6cf65094d2e268ad30ecd052f4cb73e4dddeb3644a8b5d4e00b7`

```dockerfile
```

-	Layers:
	-	`sha256:f42e4ebf214a33a305d64952d73fd7dd183f7a9b3c1ee3618be109170351a6f2`  
		Last Modified: Wed, 24 Jun 2026 01:20:45 GMT  
		Size: 2.0 MB (2005525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd85722eeac2901ebcdc4b4970759b139e69583f42cc4b4f5f84fc21347082c0`  
		Last Modified: Wed, 24 Jun 2026 01:20:45 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:f26a6eb2688cfd1f4cf236c411f9988f840b8e69f0d81f925c8c5b375608a5b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36173798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683edb23fb2832c336aa1334780707e8e429ee767b084b9c4ebf1a76eee13670`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:32:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:32:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:35:52 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:35:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:35:52 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:35:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:35:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:35:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:35:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:35:52 GMT
USER memcache
# Wed, 24 Jun 2026 01:35:52 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:35:52 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:639e1c13483ea279c94219be2736856262d8dd2efeff3e6d309f11a66aba21fb`  
		Last Modified: Wed, 24 Jun 2026 00:30:29 GMT  
		Size: 33.6 MB (33606388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d700e36837a63da25a34bd9fef9f7937541cbe617e8c1e9c4a785cc37d6e2e29`  
		Last Modified: Wed, 24 Jun 2026 01:36:14 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7456d8868d48e0b53288836b26930c6efe02b67c099dcefa481778870fc15df`  
		Last Modified: Wed, 24 Jun 2026 01:36:15 GMT  
		Size: 170.4 KB (170375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7daaa467c3a42eb0ea458c5771839433b7c4f773537351a10e30789f995f63`  
		Last Modified: Wed, 24 Jun 2026 01:36:15 GMT  
		Size: 2.4 MB (2395518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a6999cbf05638c0554accc7e8f9d8acd435888a52ad68267fcbd567d8fdce0`  
		Last Modified: Wed, 24 Jun 2026 01:36:14 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5f81262c7fc9478a7854e6dcf5e83a4d09732948b63b45b5d138da7fd57d8c`  
		Last Modified: Wed, 24 Jun 2026 01:36:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:1db8703b08d0d14737d40156d6a09384027af9d6806c94c63763d4b5cd08bc31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9df60db9b699e1540eb1b1a65a79dfffa825cdb8a5c9ce191b5cd53055af17e2`

```dockerfile
```

-	Layers:
	-	`sha256:d207552f6be1ed5a92472733946f240471025ee31516d22f4e4e1710136a5df9`  
		Last Modified: Wed, 24 Jun 2026 01:36:15 GMT  
		Size: 2.0 MB (2011969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2777dc1115238cc20388367ecc331281ddd19f28aafede9028ceb87baaf56ed`  
		Last Modified: Wed, 24 Jun 2026 01:36:14 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; riscv64

```console
$ docker pull memcached@sha256:1d09cc6da0fcd7fbfd1eb9a04ab9aeb8557f8a977d85bc7758ddc33f1fae7e8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30626877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e932fab34f25980444b8d9d4042f4f019d633ae41731c4d58de9d0425aacbb5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 20:53:15 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 20:53:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jun 2026 19:11:35 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 25 Jun 2026 19:11:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 25 Jun 2026 19:11:35 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 25 Jun 2026 19:11:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 25 Jun 2026 19:11:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 25 Jun 2026 19:11:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 25 Jun 2026 19:11:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Jun 2026 19:11:35 GMT
USER memcache
# Thu, 25 Jun 2026 19:11:35 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 25 Jun 2026 19:11:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:58bface994ba631e609596a2ca5032d9d75de27f1b6476034b581e226205adab`  
		Last Modified: Wed, 24 Jun 2026 03:41:42 GMT  
		Size: 28.3 MB (28282378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88be0d85b1f48be753592f62cac7ef80c23a61c7848026bd2d489c40d2214a58`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5924e63da94311a18a309f02e655774d7a7dd21bf3dc267215c524167fb7ca02`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 133.1 KB (133093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfa9af5e6df6f7145e6f80ab61869e6613b9f5caa0cfa94788cbf01b3041add`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 2.2 MB (2209890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ace1c66f882f3224670cc80ac0c47197433c688d59a6bad4e5e137d6947a7d9`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470dc087e4a89d9d58d8fa29a67ac089e3c4b569f1c1c79265bfe24ba39500d2`  
		Last Modified: Thu, 25 Jun 2026 19:12:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:10dc6cdb2cd2787d533382c9b0e6ae2f8f3b637c254e1b54762fc75d6b7c2066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173dffb05aa61f0096ec844832f392e17573e61865ef528ee8b742faa7e4b6db`

```dockerfile
```

-	Layers:
	-	`sha256:69ed82bb373c86c8fbec635b83221f89933079ee40e6fcf48418d1a69ca5bb89`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 2.0 MB (2002332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cea64cfdecc1c5a9f3c417e6a679e88cd0613790ff8f658ca9e3ec73325fa9cc`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:6bcf745c9e84c923ee6794f31fd61c321c07e98208661f8f96267b959b19322c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32291924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfeb11440a0b99b60cfece211ea4a2d19eb4c5aa0e27cc119d9930da48bb4a23`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:17:57 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:18:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:21:15 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:21:15 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:21:15 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:21:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:21:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:21:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:21:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:21:16 GMT
USER memcache
# Wed, 24 Jun 2026 01:21:16 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:21:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b6a0af2ceb4b698210b8776157288a3fb06e46aaf75d641139449fcc50ce430d`  
		Last Modified: Wed, 24 Jun 2026 00:28:43 GMT  
		Size: 29.9 MB (29851381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3bba39c5a45464aeb0d1fa775a329c0c537439ee4814281c4fc08a68d8cd584`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a60267637fa53d628133884b458b9c84464d66f87fb587bd54667d3e7c6c0f8`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 140.5 KB (140541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009a2f1905baeb2174621049e700d37eaaf68cda0912ab76762452f73537af8e`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 2.3 MB (2298488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5127e016f9d2a0554de486521914b692af85186039386e058a7e61c9754ef414`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf617d16473cca6af3500948111afc2fce546cd4db4d94441113555d9a9da08`  
		Last Modified: Wed, 24 Jun 2026 01:21:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:2721a3c701c85fd239ef39e576be9973f43c9655cc6cb66fd5bc3dc3ce206166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c4f64b3eb5d1eccd239a9a42a97ae1477a0b589f61e823181e9ab7271116da`

```dockerfile
```

-	Layers:
	-	`sha256:26bfdc43fc003330338d918e59f990463e9e8ceae7dbef48f43cdcb95e0f9b4e`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 2.0 MB (2009805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b9c877b5a220dabf32e1e097a3fb26dc36bad47b1978fb4b39ce7ae5415394f`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:trixie`

```console
$ docker pull memcached@sha256:e2a8683c7fbb73d12dce8082525adf9df857765970e639bd9f4705acc31dfcba
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
$ docker pull memcached@sha256:3e079a2fc4232b10565b9bc19139292f16ef304297d4560f08f642f5f2d7a6a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32204836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ab1d39869e17aa04a25df4af0b5bf28a973d4f965635b067471bb44adbdc01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:21:34 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:21:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:24:28 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:24:28 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:24:28 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:24:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:24:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:24:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:24:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:24:28 GMT
USER memcache
# Wed, 24 Jun 2026 01:24:28 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:24:28 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1213ec9c2c2febafa221ff6195f27ea10c675acbc71d21fcc0d2b2ade3f5f74b`  
		Last Modified: Wed, 24 Jun 2026 01:24:34 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3266f17f87ca1b46b5c4fde9dd99707e3827b91b70059e7031ef53abd47fb12c`  
		Last Modified: Wed, 24 Jun 2026 01:24:34 GMT  
		Size: 136.7 KB (136688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a006226c9ea4b6f900685ceec0bda7162e03f436f1b312db9c6ba0d5b47919c7`  
		Last Modified: Wed, 24 Jun 2026 01:24:35 GMT  
		Size: 2.3 MB (2281216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3fd586859c95b544309532471aaabcf797408c5d017bd900b8e4c56c911367`  
		Last Modified: Wed, 24 Jun 2026 01:24:34 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2160167316cd327104547209c9d482373032078e07bb8a6a1e807f7e415571`  
		Last Modified: Wed, 24 Jun 2026 01:24:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:78b554b9b0edb7e45697fbdc7fb7bd3b9facbf500f3f955b3e21628a2469b659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97077f9e00ac4cde9ecb4dba83482ab83cfb8c9378171bf96fc076cc86a64a7`

```dockerfile
```

-	Layers:
	-	`sha256:0f81896f32bd3f922ecc9c3921e78406158e32af9b86b0bc711b5381f977f1e1`  
		Last Modified: Wed, 24 Jun 2026 01:24:35 GMT  
		Size: 2.0 MB (2008368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2714f45af9d9661f076eb378c43b8c30b2b1556e38d5573a646c9df3faae7740`  
		Last Modified: Wed, 24 Jun 2026 01:24:34 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:07d3a299e990256fef486b7259267b9140a71a6003c6b138f0629c06e8eab05a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30316687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3763f93158d93525ae099ec31b8c33c6f309d88e3e96f8e6e18ba87c3f5c18`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:14:31 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:14:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:17:52 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:17:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:17:52 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:17:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:17:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:17:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:17:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:17:52 GMT
USER memcache
# Wed, 24 Jun 2026 01:17:52 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:17:52 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:da43bc6a07a9cd7cc23faa538adc0797482747316b5a85b9f3f94ed17f6c1a2a`  
		Last Modified: Wed, 24 Jun 2026 00:28:12 GMT  
		Size: 28.0 MB (27959221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72b0a4d36a2a621f7921b07bce6fd125f5f5dcef47bd823dc4e31290e3e2399`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4e24ea733891c84a840e31af3fb0b9c15056a407cdc805d54c8cfd3e6ef6f0`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 144.2 KB (144157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64639d0df1b35e7dbd196efee0fd423d0a736ac6c863e17f7d6986420c041af8`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 2.2 MB (2211796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090c9d3495cd22555152f5b251e3f1fe30e588646fcac43f30a778eb73470f8e`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02db167b638147d6fc9f87b04a310ffd4b96fc41da3f61194b9525811486129`  
		Last Modified: Wed, 24 Jun 2026 01:18:00 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:b276ce09ef33302e7b98984a8b1515cd0c83190274b6163f2a28f2d539cc4a7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:390cd34082323b589abd9a85a9cf2513c80fd64085a0a6aa744e0b297aa7a4b5`

```dockerfile
```

-	Layers:
	-	`sha256:259590638c0e780d766f685e7f3a057b89c4575e1736e106d88bcbd2e7c345cb`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 2.0 MB (2011371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd7d6f82a916ba666327037ebdcdce8491adee8668fde99a67161383e1bdaf64`  
		Last Modified: Wed, 24 Jun 2026 01:17:59 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:e2be04c60636f94c2c1555f324fd58c8ed1cca98bfc5721d5d00a8357a7df461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28513245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc5b22192f1fe06b621ee612a1428f71028d4702873f593a6e3f1896b5c7edfd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:19:26 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:19:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:22:38 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:22:38 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:22:38 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:22:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:22:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:22:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:22:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:22:38 GMT
USER memcache
# Wed, 24 Jun 2026 01:22:38 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:22:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:81c84b0273952340067af970e1fe77a42ea83b4ed1a53319e258d5f1077848f0`  
		Last Modified: Wed, 24 Jun 2026 00:28:38 GMT  
		Size: 26.2 MB (26211051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0642cf323abcb26caa4c3ff3b7e80d0d7d6d9f6d9d9accdcf6d336f41426f102`  
		Last Modified: Wed, 24 Jun 2026 01:22:44 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2360e1299ad9a74124543c81dfb5655cf827191bca3b68df2bfa35cef12ff4c6`  
		Last Modified: Wed, 24 Jun 2026 01:22:44 GMT  
		Size: 135.4 KB (135381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa1e7d2a4dedc5e64f5906cba5d754b8a704705fc6875aa2c6e19fbf32e80d0`  
		Last Modified: Wed, 24 Jun 2026 01:22:45 GMT  
		Size: 2.2 MB (2165300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1110dbe0eb2a934122b522315e135c97a24e58dfe0d85799fa581bed83010517`  
		Last Modified: Wed, 24 Jun 2026 01:22:44 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6a4eee2665c4591534d0fb4f767664091dd2025201db5c28be41b6cde451d4`  
		Last Modified: Wed, 24 Jun 2026 01:22:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:69daaf7d08ee571ea31fa5ba2bbed9ee75e05eaa0e828fec25bcbbb5db45e674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ce76762dc893723cf043776255f735aa512c188d67735932b74d4347be6e02d`

```dockerfile
```

-	Layers:
	-	`sha256:bd51ee9d8e158fbc8c58b5d3ec9bb91d9e9adb533d51ef67ba795e241a2a1486`  
		Last Modified: Wed, 24 Jun 2026 01:22:45 GMT  
		Size: 2.0 MB (2009828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce07aa39f2cbf08f3885676ecfd34bf02f971dd10ba62db2f161f39e032df30d`  
		Last Modified: Wed, 24 Jun 2026 01:22:44 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ce9daf8b2144b701cf7e968ab341768bb2d3efa2a4c64d02da0a0de42c56f1bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32566611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cc2b42a078d89f4b7328abbd61b2cc235e3c733db4c018c8c232c8e3c8dac40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:22:00 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:22:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:25:00 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:25:00 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:25:00 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:25:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:25:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:25:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:25:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:25:00 GMT
USER memcache
# Wed, 24 Jun 2026 01:25:00 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:25:00 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45863abe59cf630e20caf87380378a813615419b3e0f3a8f6649855538dd606`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b7dfd57d8e29e17a7f5191adae69420144fe599879e351b48979971c36f465`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 153.5 KB (153487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be9b72bcf7171564f265414becff9bc077025e30b3f602008e49e51af592400`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 2.3 MB (2263062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff542c356a684239a022d62e5a51aa3f8884a5a1c5a7125cd5d4133c8bac04a`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf0b844cb30e05fdae9181c546555144b913389d03c3ed5549c809d6d4f5cb5`  
		Last Modified: Wed, 24 Jun 2026 01:25:07 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:4b6ea06e8e33c13f6ed836c0f565b1bb81217e79880acaac6b7ad6c4ae57a35d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d49fd2b1e37fca3ad0e2c2747ad1ffa5e40f4dac971d3d382bb685ad2cbeb75`

```dockerfile
```

-	Layers:
	-	`sha256:0749a7c57e354ea8640b297fd510a9c6b05145e740a4d1747f3d832d71878a63`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 2.0 MB (2008676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31dad526561e0628b5270544aa1a9c883fbecd2e25a9770bf262407c2e0bf810`  
		Last Modified: Wed, 24 Jun 2026 01:25:06 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; 386

```console
$ docker pull memcached@sha256:b2916cadce1269827ce2769d75e850a06fa02e2b29d606a5300c10859def3696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33675687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c903111eaced6eb842f558accf95d8d210049b93dfdce69195cb596a9295aa2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:17:36 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:17:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:20:39 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:20:39 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:20:39 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:20:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:20:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:20:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:20:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:20:39 GMT
USER memcache
# Wed, 24 Jun 2026 01:20:39 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:20:39 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:984d3baa100eb8c4d7c83b7c23b4748e508aa6ed5903297f02be90a681f52d41`  
		Last Modified: Wed, 24 Jun 2026 00:28:38 GMT  
		Size: 31.3 MB (31301210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e88a5ba508193f8a40b67d411ba88b51522122e991c5e579f718f03a7b827d5`  
		Last Modified: Wed, 24 Jun 2026 01:20:45 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13a37bd401d9e6fe5c150251a68821160273feb13462cbe401715d4c50bbcee`  
		Last Modified: Wed, 24 Jun 2026 01:20:45 GMT  
		Size: 147.5 KB (147522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f7f30bf297b5062f967e9d807b67dbfcbd20800b75c6daae0ad7fff1edf46e`  
		Last Modified: Wed, 24 Jun 2026 01:20:46 GMT  
		Size: 2.2 MB (2225442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1687fae458633e2c28615b4a2b32841cea0191dc6777aa4ad23de450a9f898e4`  
		Last Modified: Wed, 24 Jun 2026 01:20:45 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc431901c24b9ea4ccb36149baa5b10a412da5738b7f7af9808c7a408caebc12`  
		Last Modified: Wed, 24 Jun 2026 01:20:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:ceb7723388cb240f2eff890796603dfa6d63cb5e7f9e9774cf291a70411779ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596e979ff6ae6cf65094d2e268ad30ecd052f4cb73e4dddeb3644a8b5d4e00b7`

```dockerfile
```

-	Layers:
	-	`sha256:f42e4ebf214a33a305d64952d73fd7dd183f7a9b3c1ee3618be109170351a6f2`  
		Last Modified: Wed, 24 Jun 2026 01:20:45 GMT  
		Size: 2.0 MB (2005525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd85722eeac2901ebcdc4b4970759b139e69583f42cc4b4f5f84fc21347082c0`  
		Last Modified: Wed, 24 Jun 2026 01:20:45 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:f26a6eb2688cfd1f4cf236c411f9988f840b8e69f0d81f925c8c5b375608a5b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36173798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683edb23fb2832c336aa1334780707e8e429ee767b084b9c4ebf1a76eee13670`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:32:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:32:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:35:52 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:35:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:35:52 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:35:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:35:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:35:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:35:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:35:52 GMT
USER memcache
# Wed, 24 Jun 2026 01:35:52 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:35:52 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:639e1c13483ea279c94219be2736856262d8dd2efeff3e6d309f11a66aba21fb`  
		Last Modified: Wed, 24 Jun 2026 00:30:29 GMT  
		Size: 33.6 MB (33606388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d700e36837a63da25a34bd9fef9f7937541cbe617e8c1e9c4a785cc37d6e2e29`  
		Last Modified: Wed, 24 Jun 2026 01:36:14 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7456d8868d48e0b53288836b26930c6efe02b67c099dcefa481778870fc15df`  
		Last Modified: Wed, 24 Jun 2026 01:36:15 GMT  
		Size: 170.4 KB (170375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7daaa467c3a42eb0ea458c5771839433b7c4f773537351a10e30789f995f63`  
		Last Modified: Wed, 24 Jun 2026 01:36:15 GMT  
		Size: 2.4 MB (2395518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a6999cbf05638c0554accc7e8f9d8acd435888a52ad68267fcbd567d8fdce0`  
		Last Modified: Wed, 24 Jun 2026 01:36:14 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5f81262c7fc9478a7854e6dcf5e83a4d09732948b63b45b5d138da7fd57d8c`  
		Last Modified: Wed, 24 Jun 2026 01:36:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:1db8703b08d0d14737d40156d6a09384027af9d6806c94c63763d4b5cd08bc31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9df60db9b699e1540eb1b1a65a79dfffa825cdb8a5c9ce191b5cd53055af17e2`

```dockerfile
```

-	Layers:
	-	`sha256:d207552f6be1ed5a92472733946f240471025ee31516d22f4e4e1710136a5df9`  
		Last Modified: Wed, 24 Jun 2026 01:36:15 GMT  
		Size: 2.0 MB (2011969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2777dc1115238cc20388367ecc331281ddd19f28aafede9028ceb87baaf56ed`  
		Last Modified: Wed, 24 Jun 2026 01:36:14 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:1d09cc6da0fcd7fbfd1eb9a04ab9aeb8557f8a977d85bc7758ddc33f1fae7e8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30626877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e932fab34f25980444b8d9d4042f4f019d633ae41731c4d58de9d0425aacbb5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 20:53:15 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 20:53:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jun 2026 19:11:35 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 25 Jun 2026 19:11:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 25 Jun 2026 19:11:35 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 25 Jun 2026 19:11:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 25 Jun 2026 19:11:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 25 Jun 2026 19:11:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 25 Jun 2026 19:11:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Jun 2026 19:11:35 GMT
USER memcache
# Thu, 25 Jun 2026 19:11:35 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 25 Jun 2026 19:11:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:58bface994ba631e609596a2ca5032d9d75de27f1b6476034b581e226205adab`  
		Last Modified: Wed, 24 Jun 2026 03:41:42 GMT  
		Size: 28.3 MB (28282378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88be0d85b1f48be753592f62cac7ef80c23a61c7848026bd2d489c40d2214a58`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5924e63da94311a18a309f02e655774d7a7dd21bf3dc267215c524167fb7ca02`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 133.1 KB (133093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfa9af5e6df6f7145e6f80ab61869e6613b9f5caa0cfa94788cbf01b3041add`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 2.2 MB (2209890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ace1c66f882f3224670cc80ac0c47197433c688d59a6bad4e5e137d6947a7d9`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470dc087e4a89d9d58d8fa29a67ac089e3c4b569f1c1c79265bfe24ba39500d2`  
		Last Modified: Thu, 25 Jun 2026 19:12:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:10dc6cdb2cd2787d533382c9b0e6ae2f8f3b637c254e1b54762fc75d6b7c2066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173dffb05aa61f0096ec844832f392e17573e61865ef528ee8b742faa7e4b6db`

```dockerfile
```

-	Layers:
	-	`sha256:69ed82bb373c86c8fbec635b83221f89933079ee40e6fcf48418d1a69ca5bb89`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 2.0 MB (2002332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cea64cfdecc1c5a9f3c417e6a679e88cd0613790ff8f658ca9e3ec73325fa9cc`  
		Last Modified: Thu, 25 Jun 2026 19:12:23 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; s390x

```console
$ docker pull memcached@sha256:6bcf745c9e84c923ee6794f31fd61c321c07e98208661f8f96267b959b19322c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32291924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfeb11440a0b99b60cfece211ea4a2d19eb4c5aa0e27cc119d9930da48bb4a23`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:17:57 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 24 Jun 2026 01:18:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:21:15 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 24 Jun 2026 01:21:15 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 24 Jun 2026 01:21:15 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 24 Jun 2026 01:21:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 24 Jun 2026 01:21:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:21:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:21:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:21:16 GMT
USER memcache
# Wed, 24 Jun 2026 01:21:16 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 24 Jun 2026 01:21:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b6a0af2ceb4b698210b8776157288a3fb06e46aaf75d641139449fcc50ce430d`  
		Last Modified: Wed, 24 Jun 2026 00:28:43 GMT  
		Size: 29.9 MB (29851381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3bba39c5a45464aeb0d1fa775a329c0c537439ee4814281c4fc08a68d8cd584`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a60267637fa53d628133884b458b9c84464d66f87fb587bd54667d3e7c6c0f8`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 140.5 KB (140541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009a2f1905baeb2174621049e700d37eaaf68cda0912ab76762452f73537af8e`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 2.3 MB (2298488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5127e016f9d2a0554de486521914b692af85186039386e058a7e61c9754ef414`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf617d16473cca6af3500948111afc2fce546cd4db4d94441113555d9a9da08`  
		Last Modified: Wed, 24 Jun 2026 01:21:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:2721a3c701c85fd239ef39e576be9973f43c9655cc6cb66fd5bc3dc3ce206166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c4f64b3eb5d1eccd239a9a42a97ae1477a0b589f61e823181e9ab7271116da`

```dockerfile
```

-	Layers:
	-	`sha256:26bfdc43fc003330338d918e59f990463e9e8ceae7dbef48f43cdcb95e0f9b4e`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 2.0 MB (2009805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b9c877b5a220dabf32e1e097a3fb26dc36bad47b1978fb4b39ce7ae5415394f`  
		Last Modified: Wed, 24 Jun 2026 01:21:26 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json
