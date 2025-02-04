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
-	[`memcached:1.6.35`](#memcached1635)
-	[`memcached:1.6.35-alpine`](#memcached1635-alpine)
-	[`memcached:1.6.35-alpine3.21`](#memcached1635-alpine321)
-	[`memcached:1.6.35-bookworm`](#memcached1635-bookworm)
-	[`memcached:alpine`](#memcachedalpine)
-	[`memcached:alpine3.21`](#memcachedalpine321)
-	[`memcached:bookworm`](#memcachedbookworm)
-	[`memcached:latest`](#memcachedlatest)

## `memcached:1`

```console
$ docker pull memcached@sha256:e099ebae6550a39ef5f780dc869ac48f17d87b09381a38ab0bc256a28a9e5d13
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
$ docker pull memcached@sha256:dfd99fb6fbe04b3121b1213ae0116e8d3703d1d329acc9b57ec40fe212c3d159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31972808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca71139ab2ab780916cc2410aeed46bd583f7d5b2f02e1df59647c913e1d933`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda7d6399fc25890be33d8e323a35feb9051c4a87322b3208defbca52c54b3be`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c0be3187b2dee7a02dfd52f423dc252930e248c53682a6a882a103aa3eec3a`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 2.5 MB (2491797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5808fec11b221c18511c8299b00aff12cf1fe592c5b7373edfd4c148480cb7f`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 1.3 MB (1267080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8745b39a0f5680ef45825db431aaa46b60468a8cdd43fed4fc477a4bffd35bbe`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d828e056dad95d08aea41b29d33fb1a2961ae61a4ce685a1b79a02a2569b7b0`  
		Last Modified: Mon, 03 Feb 2025 23:29:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:6b285e2b8239906b90664744391f1a4b6c3a3da8cae91273f01297a854b0b2aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18097e9c39f7331f3c6935c455fb1eeb3c8e451903fc73c9bdfae63c74cd99f8`

```dockerfile
```

-	Layers:
	-	`sha256:5be7ae24c2c09eaa07fd11802534cc38c1b5c8c6e32197189c0f2ece969e78b8`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 2.3 MB (2289307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce1fc3a95808478b79eae466f1bd195255ed42e1964471932ef4fa504b1a09ef`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v5

```console
$ docker pull memcached@sha256:19cea7f4ef8974d31946d26f29af52dac2ef01f7839f9b18dc8a5c153dbb57bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29079481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8148d94dfb620e9b264755a021f81a0997844649fe9eef185c47837e87bdf9a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7a3fc1134bc1af98e13c0b7ea743c863d5a17f830a5fbd5a7002f750500e76c2`  
		Last Modified: Tue, 14 Jan 2025 01:33:27 GMT  
		Size: 25.7 MB (25736665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a566614fdcf63df3667efc0e44ef3a55e3691eced03cf22a308d708142f7c6`  
		Last Modified: Tue, 14 Jan 2025 02:34:26 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92a25a27c2144d0ab56f557820ebe289d1620f435ddb83f14c5e48b8d08cfa5`  
		Last Modified: Tue, 14 Jan 2025 02:34:27 GMT  
		Size: 2.1 MB (2096089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8889c18344163aeaea76936cd52029ec9bb42c2e16e0f26f48a664f00c3b7694`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 1.2 MB (1245215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68b0d4672ce5cd7584f0b15c42f219e41de7fb1f28644186a8a0f9788d2c96b`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbe1e74de797ff5b1fd4cf0a27d11ceeaf02347c856cfb5ba74cc13f4de8e6d`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:4af105a2f6c653acc913a722d6b3636c3637fe2718478bab2f4b1abf3a3df4b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb88776c99ff589e69412231781b8d108a5bd931b770d38eb94fdd69f0a97a1a`

```dockerfile
```

-	Layers:
	-	`sha256:f09d82aaa941a644405f9f34074de377bbd24b82df23d0ad6a22113f9aa74e41`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 2.3 MB (2292845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97bf9ecad7b0ab53e19b325ab9725de040ddcb369051fb8205db981408ba2764`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:0f287535bdbb8cfef4d259f59bcf13f2c3441335d3cff34f7d7c78830d4562b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31658415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536cfc0e620927f7137462160084b2211a938273db79693852e1834a3b0d7c0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66214caa62a6aa92636721a38d0e11a5fc383b1f9e4697a0991f5749369033c3`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca115360faf332637b0231cd4f43e98f284331aa2fb9bfbc45ec5d80a9eb57df`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 2.4 MB (2355304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5afe04d2434c6e19998a9fe47bfcf571759106e85ec73dd6ee83420494e2c8`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 1.3 MB (1260566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35e7292944fc376dd9f2578cf538f85a6df80492f5bc136e0024733aaeac8f0`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d44c4ade766e17abf585eb36d6683321ce9a2a26385b582758cda3872122039`  
		Last Modified: Mon, 03 Feb 2025 23:29:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:50321a237d4e2507a4e56d52d627e5ccb079e3bc300cc806390e96d09fb523a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e624df56f2e01bac1680fa105c39d9e35149d5cef920cd68e7266d5b2214f8d`

```dockerfile
```

-	Layers:
	-	`sha256:8be58e9cbbf71c38228da76c2508cdc0fcb85586ccc4b49518cf69e1e5e39b50`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 2.3 MB (2289622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caf4d0d59deb6f3fb187901e3b525ab0c834bb3cb6809eea8fb0c6879572ae3e`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 21.4 KB (21418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:f5be026a6f23f855459f3627e5c4101a938bca13100113b9fe82f28b3cb1cf3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32956119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d4368d3996e2021d38fdf63f7863d74ba28d6a2ef74e5131b0397dc12d442c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9009e1bef14c8af1bf770ff23da94f70dcd286b5f120ec1e71bf467ba40a0152`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f865fc757eeb18e208170c47e11bd3a00afa6eb223213d4007662aa6512c80dd`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 2.5 MB (2500709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34d14b87df5dcc8c799103bf14f9f622bc25c16e005e1e47b6a1306697bdf88`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 1.3 MB (1266299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d338f828cfbf806035a35f4290e62f96efce17c0e99cdf3034490cf047f32e1`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4697356823aab23c184948db8f06aa7c6811e207a99f109d4a0c115be482fb`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:7286999a5f604e3b4cc31c213c4c8d0cfa8b0da817e69563a83d6e14b14b7d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1456afa32760c7ecf3b6aa1f216615797de142ac46f0ee174b33ac71c2ed02a9`

```dockerfile
```

-	Layers:
	-	`sha256:7fe0965b391e043a806dd694395597114730be5687d0427a2011870ec7c674b4`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 2.3 MB (2286406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a6fca6555d8d2e7146c7a1f88c47abe5539931256a2f3990c263cf00390198a`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; mips64le

```console
$ docker pull memcached@sha256:9db344d39627ceb6b7961e5715daa16b063785632772a10a4f8953a4c131d3c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31692251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e517b7e21ed68b2abcdb3c957e98a677c411bf1b72ef4b78aa09b5bbcd0dc9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b08d7e697b04bda8cef97763765ebbbc16790e22945b5ab31d97d448a15c8650`  
		Last Modified: Tue, 14 Jan 2025 01:38:32 GMT  
		Size: 28.5 MB (28486647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda5f653b677ccaab1e67a8e7dce8f1c207af2b166ac4d37ddb395d85cb07a4c`  
		Last Modified: Tue, 14 Jan 2025 03:20:56 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bebcbc9eca024edee3e9bcea840742795d739cc90b447152cd52cf5dd79c442`  
		Last Modified: Mon, 03 Feb 2025 23:34:18 GMT  
		Size: 1.9 MB (1943213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d20ac443403dd981e7eca81d524af67815754bca86f5705e011ca0541a6ec0d`  
		Last Modified: Mon, 03 Feb 2025 23:34:18 GMT  
		Size: 1.3 MB (1260877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3be7f64ea082d115fc02a30fe0fa678d78bee0b27ac846dbdb688550d1908a0`  
		Last Modified: Mon, 03 Feb 2025 23:34:17 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1254936a9326dadc90d0b29d805e446f753a49826f2d9ea9308f5e847d6b7d4`  
		Last Modified: Mon, 03 Feb 2025 23:34:11 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:1ebb48a31e269c5b575e78e45853282855121ca1b723662138823061912b9f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7e22e388cefc5c2c0f77535a596b93848dd4fb8af57e9b54911aeca7ecd4be`

```dockerfile
```

-	Layers:
	-	`sha256:cb8d0d9b1786b7f482fc6383b420cee035f995c0616e30e3cb1699457e8b79da`  
		Last Modified: Mon, 03 Feb 2025 23:34:17 GMT  
		Size: 21.1 KB (21114 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:b02a75a9d8ff16af6610f5a7b1acbfe5021af039c99e973bba0cb4f3fed4983e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36085902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:706acef80ef55c5c88e96b5e797e157747af5331788d51358c2f14a0a32cd977`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80745399e148b36abf9f846b38e2d897d7b6c9d1520cfa9d06841c00dc04ba59`  
		Last Modified: Mon, 03 Feb 2025 23:29:23 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a519eadeb55cab90fe606d287a41791b2c969bf4b1920d8318fab913251b0af`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 2.7 MB (2708612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884edc77561270bf25675edb3ba73142d461c958c1abe45527aef893945b4ec3`  
		Last Modified: Mon, 03 Feb 2025 23:29:23 GMT  
		Size: 1.3 MB (1330930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61db6406d089d1edef82b5f70d15343ea8e4b58f8deec8f793da379e919d46f4`  
		Last Modified: Mon, 03 Feb 2025 23:29:23 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a63ce5f40ffc44148116e4b48c365aa2eeac8feaf8d8e23f6660428fd6e7a3c`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:45e7cede06534d2e9799fae7a25d6dfdf744eb59fa843709ae6110ecd5a0420f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fa7112b112ab20c85705872120dc8f663e550e84cd97fce814e9153e06f53ea`

```dockerfile
```

-	Layers:
	-	`sha256:fc19ce65e6afd53a0af7fa74af472d2396dc69c87a16470c380123077cc173d2`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 2.3 MB (2293679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:501f87cf15042c748d83d0afebfeeb81b7c41a29ed942369564bb6e9d4ef3c19`  
		Last Modified: Mon, 03 Feb 2025 23:29:23 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:6264d50a0c04cdc558dd1afa71b24ccadf6f5693254e7b6b31bdabb3ddb23995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30261786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0faa3849ef7eee7cd9e65ac3d63ddf439ea062c01ca4cc77c93c1753b1169750`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9009e1bef14c8af1bf770ff23da94f70dcd286b5f120ec1e71bf467ba40a0152`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c02ae601ee0bb3684ac021219c34b71a1227f865794041d376a31389166800`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 2.2 MB (2156339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489cc4b7fa1a8d54bdb06261a5300d09f429439845ae9fca4df8222ac8192830`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 1.2 MB (1245194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa1370e45fc434b599dcc2c02b0f1bec90d080c3af5176313cbd678095b5155`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f034bc901164b6d57bac0a9c94c66e4b96c53fe8af3fea3aee2c74897b480cf7`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:9d8033d81506e7fc653921e3a4c4f23fc13a05f43c5496885c9010f5af0891f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eb0e2cd949a02fe68968891360bbbc13a1fe4e5bdc90f6203a8941b43cca427`

```dockerfile
```

-	Layers:
	-	`sha256:2860febfb3de6c8ffc7c08113a3aaf7f61d254e27d8c2309f5ef39a476925888`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 2.3 MB (2289021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18b61144281568e7ddee023aac2c6947e14e31c547727eb355fa003ca1de66be`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:b093f7f64a39f20b8f4a671f9c6656eff26821a3c97037a8019448040d6298bd
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
$ docker pull memcached@sha256:c497fc5a323c178e0914eca2500dcf9fa3b21ca2f9932dbc92b51ef6145cf2be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4716328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d2b29f4542cd1fc099ca3146ac53cc0eab71776ce1c029fee5d58a57c38a52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9604a91067e8818541aa31757690c9f8ebf60c58be004baded0767c0999267b8`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592b1cc3d47258eaa3cb466a887cb58e0b2a4176818d1c9a721698abf9337d94`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 104.7 KB (104686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5a55a29aba2a2a27962f2b36f259f5fac81a49009fc7c06020fc992eb6d5da`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 968.6 KB (968568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4786022d0e1453ad1d978f79f50839ba76e4f7c73310640921e5bc212537d6e`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da16032c7fbc5aedc09cd3d43a996943828a731b3ed781664abcf257bdfb65c`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:f4b6389438043b9d6191b9e22e19659d23258e22f0e414f51cb0945287141162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e696a02855f507b1b926a60cf07265433c5ab415467633243c2536753b3090`

```dockerfile
```

-	Layers:
	-	`sha256:16a139d5ff76ba43b3c520a2be58514f36e0ad4a7b0f9adfb6b9c80acb97219d`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 93.6 KB (93627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d8f0efc7a1d5a7dc78219efc6849e55d842b9a5e34ff6bee956735b7cbe2967`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:4d52a91c9cf3612ab9f44d1ecc192f150659288c8826932187c7ab3ed5f8dc9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5082815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef0a8813bf35c3ce3d0d0f9967d27c56db3fb8dc2fd7f31ab4cd3fc1f7cd209`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a202407430ec08b7a5bfb94689fc70aed855fbc1cd8b62ce145147fc5278b7a8`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82c0f1024964e8e055db8178bb0d2595a4a66f7398bffe83d6176cc192ac77e`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 120.8 KB (120783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46624d73285a34a525d44fb1f293cdb9fc95ebfb5b305918bc6a1ff77019fda`  
		Last Modified: Mon, 03 Feb 2025 23:32:18 GMT  
		Size: 968.3 KB (968310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099e6e9c12eb4dfbd63c3bc7cec8de6eb251173a42983594f30413921e56380a`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348cf5001affc34a6f03be6a7f413a6cc377fa11350026995dd53f7db78b85a1`  
		Last Modified: Mon, 03 Feb 2025 23:32:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:631105e348c97a01de96919b82284f666d3283712a23e1b5670c31c88810f40c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff4582dcb2cdec3cfb7590e5b6ade8162439d38a001ff6c08fa81f7d08c669e`

```dockerfile
```

-	Layers:
	-	`sha256:8f4375fd6e27a5ee655f47249469c2214b367ec0146b4e8769a97c6afa3d2829`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 93.7 KB (93731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4bf5d12011dbaae039aec13c76a68a64809e478a3b79d0090ba407f1d4f7c61`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:1f1e5941bca8da9b3aeabcc13c55fe90fc40f9c6476645c19172e508e5302723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4534153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2936f0dd081882d9f0da9ea6113e9780627d3a665a9d909de817c696fac9620`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300aaa75d91b0206b7556a721baaed9f7000ccf73ab8deda59e1cb428ec870f9`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ac94f71cda4f155944d630f60f3e31780c4a97ced13f6c61385dc7e95df429`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 109.5 KB (109465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73b7528b6c4fdfdf4075a75f9e28334049f5461f39426f3b2f983792188c971`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 960.2 KB (960204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb441509973ed0be28152c5ef6c85917a0de941839cd68559be4ecfcc273b17`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e6efaa8bc767e6ef9d48f3b7547a57b7d72964bbb765d7a66481f3f3b36dd1`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:0de21b11722d02a9d2cfc6acf661c6d755de360f4c1f70e7af549cac29e5aef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10be0a79af6bc5d121d12aa89f8e2191eb25f2533cfb4e1de067b3e0bbe82834`

```dockerfile
```

-	Layers:
	-	`sha256:c57cf3137ea2641a839877ddcf3a6065504f38c2ea4f2b7671c1776008e2cfcf`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 93.6 KB (93582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdf7d0d4ee2052676f3563869639942945b1cba543484223915cb33df997a5f0`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 19.5 KB (19512 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:913b5bd251bfe9202c3f0302d3c8c5a4ea3fb7f40f73e8561542c93db1c9d6c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4706076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8083b854e648814b258458b24e3039ade25fa9e63e50b6fb79db7cb05d2ee3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a841f248cda34139a77fd6ab9691e34b7d7dae6dfaedc45a2304aa25c07536`  
		Last Modified: Mon, 03 Feb 2025 23:32:07 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ccea169aa483a5ea29ebe89aa46469affffa54252ac8df2ee75acc10eca2e0`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 124.3 KB (124280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f40e8d115f7e602d9931eaa3e7f41c17dc35a40994befa787615cbd877d430`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 1.0 MB (1006836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf17c8f5e90551f91b3474eb46d197d4ac28e21bf5cb9aaa79eea5b851db371`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9971977dd87dcc447ad6eccbe529fc3c7d6b7dc6b74a4d74fb519c86565318f4`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:04513dfc421f21abd4cd316a69b57cdbfd9d92844a16e9d55eec6a4592cd22d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569bb3d3624a47ed75650ef0a92bfc59d63af78afe540637c817793e9cf4b6d6`

```dockerfile
```

-	Layers:
	-	`sha256:ba709bd16c5785bcfce6f9a8fd6e1d834e101c00d1ed2e018a68a999ec43825b`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 91.7 KB (91734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bc2aa4695d41b4a46d039e0e91f623f3f7aadfd866f0e477637054a37fc5127`  
		Last Modified: Mon, 03 Feb 2025 23:32:07 GMT  
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
$ docker pull memcached@sha256:624036093e557f56a4d500c780f34193af25d5c3b73f8bb08329b579e72b7d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4570369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e3d248b914c5043ad7dc370403b9ea51bf62f972a6f7cf694a023ce14ac2d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223127e71140d5e120db85abbcc459b2ca368e042d165466a1ab8b72ada743f8`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf0ecced8267cdc41066ee8044aa4a0e35e951cba2f51a411ecbfb2cee29819`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 113.5 KB (113450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b7e62f8ce2395ffab9dff807ea14960a2cfa247d7c8a418a5e92d3b4d883f8`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 988.7 KB (988692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed293040c38a686b287b82c3a47615ca2f9034912964f5ce7e832241db526879`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1254936a9326dadc90d0b29d805e446f753a49826f2d9ea9308f5e847d6b7d4`  
		Last Modified: Mon, 03 Feb 2025 23:34:11 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:51c253df33d2a17a62bac93fdc69e4be991e6f4b9e6015eff29ad965c1e58628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 KB (111245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4b6a687d069c6e737d3a9cfa50af30753d0165aa04019517f2f6951bad7feb6`

```dockerfile
```

-	Layers:
	-	`sha256:4e1be19ae90b5f3b2e2b65ad7605851c11804d593bec1671c444bd7aadc3063d`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 91.7 KB (91676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:415673db52745ddb45aa4c05424023581f2903f3acd2578ac008e4857c8ca11b`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 19.6 KB (19569 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine3.21`

```console
$ docker pull memcached@sha256:918f8d596494e94538b93f92d629c3d20efa4d5ca8b0302bf672b65f974c5617
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
$ docker pull memcached@sha256:c497fc5a323c178e0914eca2500dcf9fa3b21ca2f9932dbc92b51ef6145cf2be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4716328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d2b29f4542cd1fc099ca3146ac53cc0eab71776ce1c029fee5d58a57c38a52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9604a91067e8818541aa31757690c9f8ebf60c58be004baded0767c0999267b8`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592b1cc3d47258eaa3cb466a887cb58e0b2a4176818d1c9a721698abf9337d94`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 104.7 KB (104686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5a55a29aba2a2a27962f2b36f259f5fac81a49009fc7c06020fc992eb6d5da`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 968.6 KB (968568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4786022d0e1453ad1d978f79f50839ba76e4f7c73310640921e5bc212537d6e`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da16032c7fbc5aedc09cd3d43a996943828a731b3ed781664abcf257bdfb65c`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:f4b6389438043b9d6191b9e22e19659d23258e22f0e414f51cb0945287141162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e696a02855f507b1b926a60cf07265433c5ab415467633243c2536753b3090`

```dockerfile
```

-	Layers:
	-	`sha256:16a139d5ff76ba43b3c520a2be58514f36e0ad4a7b0f9adfb6b9c80acb97219d`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 93.6 KB (93627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d8f0efc7a1d5a7dc78219efc6849e55d842b9a5e34ff6bee956735b7cbe2967`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:4d52a91c9cf3612ab9f44d1ecc192f150659288c8826932187c7ab3ed5f8dc9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5082815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef0a8813bf35c3ce3d0d0f9967d27c56db3fb8dc2fd7f31ab4cd3fc1f7cd209`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a202407430ec08b7a5bfb94689fc70aed855fbc1cd8b62ce145147fc5278b7a8`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82c0f1024964e8e055db8178bb0d2595a4a66f7398bffe83d6176cc192ac77e`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 120.8 KB (120783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46624d73285a34a525d44fb1f293cdb9fc95ebfb5b305918bc6a1ff77019fda`  
		Last Modified: Mon, 03 Feb 2025 23:32:18 GMT  
		Size: 968.3 KB (968310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099e6e9c12eb4dfbd63c3bc7cec8de6eb251173a42983594f30413921e56380a`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348cf5001affc34a6f03be6a7f413a6cc377fa11350026995dd53f7db78b85a1`  
		Last Modified: Mon, 03 Feb 2025 23:32:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:631105e348c97a01de96919b82284f666d3283712a23e1b5670c31c88810f40c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff4582dcb2cdec3cfb7590e5b6ade8162439d38a001ff6c08fa81f7d08c669e`

```dockerfile
```

-	Layers:
	-	`sha256:8f4375fd6e27a5ee655f47249469c2214b367ec0146b4e8769a97c6afa3d2829`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 93.7 KB (93731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4bf5d12011dbaae039aec13c76a68a64809e478a3b79d0090ba407f1d4f7c61`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; 386

```console
$ docker pull memcached@sha256:1f1e5941bca8da9b3aeabcc13c55fe90fc40f9c6476645c19172e508e5302723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4534153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2936f0dd081882d9f0da9ea6113e9780627d3a665a9d909de817c696fac9620`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300aaa75d91b0206b7556a721baaed9f7000ccf73ab8deda59e1cb428ec870f9`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ac94f71cda4f155944d630f60f3e31780c4a97ced13f6c61385dc7e95df429`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 109.5 KB (109465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73b7528b6c4fdfdf4075a75f9e28334049f5461f39426f3b2f983792188c971`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 960.2 KB (960204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb441509973ed0be28152c5ef6c85917a0de941839cd68559be4ecfcc273b17`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e6efaa8bc767e6ef9d48f3b7547a57b7d72964bbb765d7a66481f3f3b36dd1`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:0de21b11722d02a9d2cfc6acf661c6d755de360f4c1f70e7af549cac29e5aef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10be0a79af6bc5d121d12aa89f8e2191eb25f2533cfb4e1de067b3e0bbe82834`

```dockerfile
```

-	Layers:
	-	`sha256:c57cf3137ea2641a839877ddcf3a6065504f38c2ea4f2b7671c1776008e2cfcf`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 93.6 KB (93582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdf7d0d4ee2052676f3563869639942945b1cba543484223915cb33df997a5f0`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 19.5 KB (19512 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; ppc64le

```console
$ docker pull memcached@sha256:913b5bd251bfe9202c3f0302d3c8c5a4ea3fb7f40f73e8561542c93db1c9d6c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4706076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8083b854e648814b258458b24e3039ade25fa9e63e50b6fb79db7cb05d2ee3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a841f248cda34139a77fd6ab9691e34b7d7dae6dfaedc45a2304aa25c07536`  
		Last Modified: Mon, 03 Feb 2025 23:32:07 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ccea169aa483a5ea29ebe89aa46469affffa54252ac8df2ee75acc10eca2e0`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 124.3 KB (124280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f40e8d115f7e602d9931eaa3e7f41c17dc35a40994befa787615cbd877d430`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 1.0 MB (1006836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf17c8f5e90551f91b3474eb46d197d4ac28e21bf5cb9aaa79eea5b851db371`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9971977dd87dcc447ad6eccbe529fc3c7d6b7dc6b74a4d74fb519c86565318f4`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:04513dfc421f21abd4cd316a69b57cdbfd9d92844a16e9d55eec6a4592cd22d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569bb3d3624a47ed75650ef0a92bfc59d63af78afe540637c817793e9cf4b6d6`

```dockerfile
```

-	Layers:
	-	`sha256:ba709bd16c5785bcfce6f9a8fd6e1d834e101c00d1ed2e018a68a999ec43825b`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 91.7 KB (91734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bc2aa4695d41b4a46d039e0e91f623f3f7aadfd866f0e477637054a37fc5127`  
		Last Modified: Mon, 03 Feb 2025 23:32:07 GMT  
		Size: 19.6 KB (19648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; s390x

```console
$ docker pull memcached@sha256:624036093e557f56a4d500c780f34193af25d5c3b73f8bb08329b579e72b7d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4570369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e3d248b914c5043ad7dc370403b9ea51bf62f972a6f7cf694a023ce14ac2d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223127e71140d5e120db85abbcc459b2ca368e042d165466a1ab8b72ada743f8`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf0ecced8267cdc41066ee8044aa4a0e35e951cba2f51a411ecbfb2cee29819`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 113.5 KB (113450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b7e62f8ce2395ffab9dff807ea14960a2cfa247d7c8a418a5e92d3b4d883f8`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 988.7 KB (988692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed293040c38a686b287b82c3a47615ca2f9034912964f5ce7e832241db526879`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1254936a9326dadc90d0b29d805e446f753a49826f2d9ea9308f5e847d6b7d4`  
		Last Modified: Mon, 03 Feb 2025 23:34:11 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:51c253df33d2a17a62bac93fdc69e4be991e6f4b9e6015eff29ad965c1e58628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 KB (111245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4b6a687d069c6e737d3a9cfa50af30753d0165aa04019517f2f6951bad7feb6`

```dockerfile
```

-	Layers:
	-	`sha256:4e1be19ae90b5f3b2e2b65ad7605851c11804d593bec1671c444bd7aadc3063d`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 91.7 KB (91676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:415673db52745ddb45aa4c05424023581f2903f3acd2578ac008e4857c8ca11b`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 19.6 KB (19569 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-bookworm`

```console
$ docker pull memcached@sha256:e099ebae6550a39ef5f780dc869ac48f17d87b09381a38ab0bc256a28a9e5d13
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
$ docker pull memcached@sha256:dfd99fb6fbe04b3121b1213ae0116e8d3703d1d329acc9b57ec40fe212c3d159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31972808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca71139ab2ab780916cc2410aeed46bd583f7d5b2f02e1df59647c913e1d933`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda7d6399fc25890be33d8e323a35feb9051c4a87322b3208defbca52c54b3be`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c0be3187b2dee7a02dfd52f423dc252930e248c53682a6a882a103aa3eec3a`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 2.5 MB (2491797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5808fec11b221c18511c8299b00aff12cf1fe592c5b7373edfd4c148480cb7f`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 1.3 MB (1267080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8745b39a0f5680ef45825db431aaa46b60468a8cdd43fed4fc477a4bffd35bbe`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d828e056dad95d08aea41b29d33fb1a2961ae61a4ce685a1b79a02a2569b7b0`  
		Last Modified: Mon, 03 Feb 2025 23:29:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:6b285e2b8239906b90664744391f1a4b6c3a3da8cae91273f01297a854b0b2aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18097e9c39f7331f3c6935c455fb1eeb3c8e451903fc73c9bdfae63c74cd99f8`

```dockerfile
```

-	Layers:
	-	`sha256:5be7ae24c2c09eaa07fd11802534cc38c1b5c8c6e32197189c0f2ece969e78b8`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 2.3 MB (2289307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce1fc3a95808478b79eae466f1bd195255ed42e1964471932ef4fa504b1a09ef`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:19cea7f4ef8974d31946d26f29af52dac2ef01f7839f9b18dc8a5c153dbb57bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29079481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8148d94dfb620e9b264755a021f81a0997844649fe9eef185c47837e87bdf9a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7a3fc1134bc1af98e13c0b7ea743c863d5a17f830a5fbd5a7002f750500e76c2`  
		Last Modified: Tue, 14 Jan 2025 01:33:27 GMT  
		Size: 25.7 MB (25736665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a566614fdcf63df3667efc0e44ef3a55e3691eced03cf22a308d708142f7c6`  
		Last Modified: Tue, 14 Jan 2025 02:34:26 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92a25a27c2144d0ab56f557820ebe289d1620f435ddb83f14c5e48b8d08cfa5`  
		Last Modified: Tue, 14 Jan 2025 02:34:27 GMT  
		Size: 2.1 MB (2096089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8889c18344163aeaea76936cd52029ec9bb42c2e16e0f26f48a664f00c3b7694`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 1.2 MB (1245215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68b0d4672ce5cd7584f0b15c42f219e41de7fb1f28644186a8a0f9788d2c96b`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbe1e74de797ff5b1fd4cf0a27d11ceeaf02347c856cfb5ba74cc13f4de8e6d`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:4af105a2f6c653acc913a722d6b3636c3637fe2718478bab2f4b1abf3a3df4b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb88776c99ff589e69412231781b8d108a5bd931b770d38eb94fdd69f0a97a1a`

```dockerfile
```

-	Layers:
	-	`sha256:f09d82aaa941a644405f9f34074de377bbd24b82df23d0ad6a22113f9aa74e41`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 2.3 MB (2292845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97bf9ecad7b0ab53e19b325ab9725de040ddcb369051fb8205db981408ba2764`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:0f287535bdbb8cfef4d259f59bcf13f2c3441335d3cff34f7d7c78830d4562b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31658415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536cfc0e620927f7137462160084b2211a938273db79693852e1834a3b0d7c0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66214caa62a6aa92636721a38d0e11a5fc383b1f9e4697a0991f5749369033c3`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca115360faf332637b0231cd4f43e98f284331aa2fb9bfbc45ec5d80a9eb57df`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 2.4 MB (2355304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5afe04d2434c6e19998a9fe47bfcf571759106e85ec73dd6ee83420494e2c8`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 1.3 MB (1260566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35e7292944fc376dd9f2578cf538f85a6df80492f5bc136e0024733aaeac8f0`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d44c4ade766e17abf585eb36d6683321ce9a2a26385b582758cda3872122039`  
		Last Modified: Mon, 03 Feb 2025 23:29:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:50321a237d4e2507a4e56d52d627e5ccb079e3bc300cc806390e96d09fb523a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e624df56f2e01bac1680fa105c39d9e35149d5cef920cd68e7266d5b2214f8d`

```dockerfile
```

-	Layers:
	-	`sha256:8be58e9cbbf71c38228da76c2508cdc0fcb85586ccc4b49518cf69e1e5e39b50`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 2.3 MB (2289622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caf4d0d59deb6f3fb187901e3b525ab0c834bb3cb6809eea8fb0c6879572ae3e`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 21.4 KB (21418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:f5be026a6f23f855459f3627e5c4101a938bca13100113b9fe82f28b3cb1cf3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32956119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d4368d3996e2021d38fdf63f7863d74ba28d6a2ef74e5131b0397dc12d442c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9009e1bef14c8af1bf770ff23da94f70dcd286b5f120ec1e71bf467ba40a0152`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f865fc757eeb18e208170c47e11bd3a00afa6eb223213d4007662aa6512c80dd`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 2.5 MB (2500709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34d14b87df5dcc8c799103bf14f9f622bc25c16e005e1e47b6a1306697bdf88`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 1.3 MB (1266299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d338f828cfbf806035a35f4290e62f96efce17c0e99cdf3034490cf047f32e1`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4697356823aab23c184948db8f06aa7c6811e207a99f109d4a0c115be482fb`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:7286999a5f604e3b4cc31c213c4c8d0cfa8b0da817e69563a83d6e14b14b7d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1456afa32760c7ecf3b6aa1f216615797de142ac46f0ee174b33ac71c2ed02a9`

```dockerfile
```

-	Layers:
	-	`sha256:7fe0965b391e043a806dd694395597114730be5687d0427a2011870ec7c674b4`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 2.3 MB (2286406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a6fca6555d8d2e7146c7a1f88c47abe5539931256a2f3990c263cf00390198a`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:9db344d39627ceb6b7961e5715daa16b063785632772a10a4f8953a4c131d3c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31692251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e517b7e21ed68b2abcdb3c957e98a677c411bf1b72ef4b78aa09b5bbcd0dc9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b08d7e697b04bda8cef97763765ebbbc16790e22945b5ab31d97d448a15c8650`  
		Last Modified: Tue, 14 Jan 2025 01:38:32 GMT  
		Size: 28.5 MB (28486647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda5f653b677ccaab1e67a8e7dce8f1c207af2b166ac4d37ddb395d85cb07a4c`  
		Last Modified: Tue, 14 Jan 2025 03:20:56 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bebcbc9eca024edee3e9bcea840742795d739cc90b447152cd52cf5dd79c442`  
		Last Modified: Mon, 03 Feb 2025 23:34:18 GMT  
		Size: 1.9 MB (1943213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d20ac443403dd981e7eca81d524af67815754bca86f5705e011ca0541a6ec0d`  
		Last Modified: Mon, 03 Feb 2025 23:34:18 GMT  
		Size: 1.3 MB (1260877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3be7f64ea082d115fc02a30fe0fa678d78bee0b27ac846dbdb688550d1908a0`  
		Last Modified: Mon, 03 Feb 2025 23:34:17 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1254936a9326dadc90d0b29d805e446f753a49826f2d9ea9308f5e847d6b7d4`  
		Last Modified: Mon, 03 Feb 2025 23:34:11 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:1ebb48a31e269c5b575e78e45853282855121ca1b723662138823061912b9f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7e22e388cefc5c2c0f77535a596b93848dd4fb8af57e9b54911aeca7ecd4be`

```dockerfile
```

-	Layers:
	-	`sha256:cb8d0d9b1786b7f482fc6383b420cee035f995c0616e30e3cb1699457e8b79da`  
		Last Modified: Mon, 03 Feb 2025 23:34:17 GMT  
		Size: 21.1 KB (21114 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:b02a75a9d8ff16af6610f5a7b1acbfe5021af039c99e973bba0cb4f3fed4983e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36085902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:706acef80ef55c5c88e96b5e797e157747af5331788d51358c2f14a0a32cd977`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80745399e148b36abf9f846b38e2d897d7b6c9d1520cfa9d06841c00dc04ba59`  
		Last Modified: Mon, 03 Feb 2025 23:29:23 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a519eadeb55cab90fe606d287a41791b2c969bf4b1920d8318fab913251b0af`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 2.7 MB (2708612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884edc77561270bf25675edb3ba73142d461c958c1abe45527aef893945b4ec3`  
		Last Modified: Mon, 03 Feb 2025 23:29:23 GMT  
		Size: 1.3 MB (1330930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61db6406d089d1edef82b5f70d15343ea8e4b58f8deec8f793da379e919d46f4`  
		Last Modified: Mon, 03 Feb 2025 23:29:23 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a63ce5f40ffc44148116e4b48c365aa2eeac8feaf8d8e23f6660428fd6e7a3c`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:45e7cede06534d2e9799fae7a25d6dfdf744eb59fa843709ae6110ecd5a0420f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fa7112b112ab20c85705872120dc8f663e550e84cd97fce814e9153e06f53ea`

```dockerfile
```

-	Layers:
	-	`sha256:fc19ce65e6afd53a0af7fa74af472d2396dc69c87a16470c380123077cc173d2`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 2.3 MB (2293679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:501f87cf15042c748d83d0afebfeeb81b7c41a29ed942369564bb6e9d4ef3c19`  
		Last Modified: Mon, 03 Feb 2025 23:29:23 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:6264d50a0c04cdc558dd1afa71b24ccadf6f5693254e7b6b31bdabb3ddb23995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30261786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0faa3849ef7eee7cd9e65ac3d63ddf439ea062c01ca4cc77c93c1753b1169750`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9009e1bef14c8af1bf770ff23da94f70dcd286b5f120ec1e71bf467ba40a0152`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c02ae601ee0bb3684ac021219c34b71a1227f865794041d376a31389166800`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 2.2 MB (2156339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489cc4b7fa1a8d54bdb06261a5300d09f429439845ae9fca4df8222ac8192830`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 1.2 MB (1245194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa1370e45fc434b599dcc2c02b0f1bec90d080c3af5176313cbd678095b5155`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f034bc901164b6d57bac0a9c94c66e4b96c53fe8af3fea3aee2c74897b480cf7`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:9d8033d81506e7fc653921e3a4c4f23fc13a05f43c5496885c9010f5af0891f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eb0e2cd949a02fe68968891360bbbc13a1fe4e5bdc90f6203a8941b43cca427`

```dockerfile
```

-	Layers:
	-	`sha256:2860febfb3de6c8ffc7c08113a3aaf7f61d254e27d8c2309f5ef39a476925888`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 2.3 MB (2289021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18b61144281568e7ddee023aac2c6947e14e31c547727eb355fa003ca1de66be`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6`

```console
$ docker pull memcached@sha256:e099ebae6550a39ef5f780dc869ac48f17d87b09381a38ab0bc256a28a9e5d13
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
$ docker pull memcached@sha256:dfd99fb6fbe04b3121b1213ae0116e8d3703d1d329acc9b57ec40fe212c3d159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31972808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca71139ab2ab780916cc2410aeed46bd583f7d5b2f02e1df59647c913e1d933`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda7d6399fc25890be33d8e323a35feb9051c4a87322b3208defbca52c54b3be`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c0be3187b2dee7a02dfd52f423dc252930e248c53682a6a882a103aa3eec3a`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 2.5 MB (2491797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5808fec11b221c18511c8299b00aff12cf1fe592c5b7373edfd4c148480cb7f`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 1.3 MB (1267080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8745b39a0f5680ef45825db431aaa46b60468a8cdd43fed4fc477a4bffd35bbe`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d828e056dad95d08aea41b29d33fb1a2961ae61a4ce685a1b79a02a2569b7b0`  
		Last Modified: Mon, 03 Feb 2025 23:29:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:6b285e2b8239906b90664744391f1a4b6c3a3da8cae91273f01297a854b0b2aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18097e9c39f7331f3c6935c455fb1eeb3c8e451903fc73c9bdfae63c74cd99f8`

```dockerfile
```

-	Layers:
	-	`sha256:5be7ae24c2c09eaa07fd11802534cc38c1b5c8c6e32197189c0f2ece969e78b8`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 2.3 MB (2289307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce1fc3a95808478b79eae466f1bd195255ed42e1964471932ef4fa504b1a09ef`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:19cea7f4ef8974d31946d26f29af52dac2ef01f7839f9b18dc8a5c153dbb57bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29079481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8148d94dfb620e9b264755a021f81a0997844649fe9eef185c47837e87bdf9a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7a3fc1134bc1af98e13c0b7ea743c863d5a17f830a5fbd5a7002f750500e76c2`  
		Last Modified: Tue, 14 Jan 2025 01:33:27 GMT  
		Size: 25.7 MB (25736665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a566614fdcf63df3667efc0e44ef3a55e3691eced03cf22a308d708142f7c6`  
		Last Modified: Tue, 14 Jan 2025 02:34:26 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92a25a27c2144d0ab56f557820ebe289d1620f435ddb83f14c5e48b8d08cfa5`  
		Last Modified: Tue, 14 Jan 2025 02:34:27 GMT  
		Size: 2.1 MB (2096089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8889c18344163aeaea76936cd52029ec9bb42c2e16e0f26f48a664f00c3b7694`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 1.2 MB (1245215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68b0d4672ce5cd7584f0b15c42f219e41de7fb1f28644186a8a0f9788d2c96b`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbe1e74de797ff5b1fd4cf0a27d11ceeaf02347c856cfb5ba74cc13f4de8e6d`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:4af105a2f6c653acc913a722d6b3636c3637fe2718478bab2f4b1abf3a3df4b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb88776c99ff589e69412231781b8d108a5bd931b770d38eb94fdd69f0a97a1a`

```dockerfile
```

-	Layers:
	-	`sha256:f09d82aaa941a644405f9f34074de377bbd24b82df23d0ad6a22113f9aa74e41`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 2.3 MB (2292845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97bf9ecad7b0ab53e19b325ab9725de040ddcb369051fb8205db981408ba2764`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:0f287535bdbb8cfef4d259f59bcf13f2c3441335d3cff34f7d7c78830d4562b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31658415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536cfc0e620927f7137462160084b2211a938273db79693852e1834a3b0d7c0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66214caa62a6aa92636721a38d0e11a5fc383b1f9e4697a0991f5749369033c3`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca115360faf332637b0231cd4f43e98f284331aa2fb9bfbc45ec5d80a9eb57df`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 2.4 MB (2355304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5afe04d2434c6e19998a9fe47bfcf571759106e85ec73dd6ee83420494e2c8`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 1.3 MB (1260566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35e7292944fc376dd9f2578cf538f85a6df80492f5bc136e0024733aaeac8f0`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d44c4ade766e17abf585eb36d6683321ce9a2a26385b582758cda3872122039`  
		Last Modified: Mon, 03 Feb 2025 23:29:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:50321a237d4e2507a4e56d52d627e5ccb079e3bc300cc806390e96d09fb523a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e624df56f2e01bac1680fa105c39d9e35149d5cef920cd68e7266d5b2214f8d`

```dockerfile
```

-	Layers:
	-	`sha256:8be58e9cbbf71c38228da76c2508cdc0fcb85586ccc4b49518cf69e1e5e39b50`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 2.3 MB (2289622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caf4d0d59deb6f3fb187901e3b525ab0c834bb3cb6809eea8fb0c6879572ae3e`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 21.4 KB (21418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; 386

```console
$ docker pull memcached@sha256:f5be026a6f23f855459f3627e5c4101a938bca13100113b9fe82f28b3cb1cf3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32956119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d4368d3996e2021d38fdf63f7863d74ba28d6a2ef74e5131b0397dc12d442c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9009e1bef14c8af1bf770ff23da94f70dcd286b5f120ec1e71bf467ba40a0152`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f865fc757eeb18e208170c47e11bd3a00afa6eb223213d4007662aa6512c80dd`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 2.5 MB (2500709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34d14b87df5dcc8c799103bf14f9f622bc25c16e005e1e47b6a1306697bdf88`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 1.3 MB (1266299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d338f828cfbf806035a35f4290e62f96efce17c0e99cdf3034490cf047f32e1`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4697356823aab23c184948db8f06aa7c6811e207a99f109d4a0c115be482fb`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:7286999a5f604e3b4cc31c213c4c8d0cfa8b0da817e69563a83d6e14b14b7d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1456afa32760c7ecf3b6aa1f216615797de142ac46f0ee174b33ac71c2ed02a9`

```dockerfile
```

-	Layers:
	-	`sha256:7fe0965b391e043a806dd694395597114730be5687d0427a2011870ec7c674b4`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 2.3 MB (2286406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a6fca6555d8d2e7146c7a1f88c47abe5539931256a2f3990c263cf00390198a`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; mips64le

```console
$ docker pull memcached@sha256:9db344d39627ceb6b7961e5715daa16b063785632772a10a4f8953a4c131d3c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31692251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e517b7e21ed68b2abcdb3c957e98a677c411bf1b72ef4b78aa09b5bbcd0dc9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b08d7e697b04bda8cef97763765ebbbc16790e22945b5ab31d97d448a15c8650`  
		Last Modified: Tue, 14 Jan 2025 01:38:32 GMT  
		Size: 28.5 MB (28486647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda5f653b677ccaab1e67a8e7dce8f1c207af2b166ac4d37ddb395d85cb07a4c`  
		Last Modified: Tue, 14 Jan 2025 03:20:56 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bebcbc9eca024edee3e9bcea840742795d739cc90b447152cd52cf5dd79c442`  
		Last Modified: Mon, 03 Feb 2025 23:34:18 GMT  
		Size: 1.9 MB (1943213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d20ac443403dd981e7eca81d524af67815754bca86f5705e011ca0541a6ec0d`  
		Last Modified: Mon, 03 Feb 2025 23:34:18 GMT  
		Size: 1.3 MB (1260877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3be7f64ea082d115fc02a30fe0fa678d78bee0b27ac846dbdb688550d1908a0`  
		Last Modified: Mon, 03 Feb 2025 23:34:17 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1254936a9326dadc90d0b29d805e446f753a49826f2d9ea9308f5e847d6b7d4`  
		Last Modified: Mon, 03 Feb 2025 23:34:11 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:1ebb48a31e269c5b575e78e45853282855121ca1b723662138823061912b9f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7e22e388cefc5c2c0f77535a596b93848dd4fb8af57e9b54911aeca7ecd4be`

```dockerfile
```

-	Layers:
	-	`sha256:cb8d0d9b1786b7f482fc6383b420cee035f995c0616e30e3cb1699457e8b79da`  
		Last Modified: Mon, 03 Feb 2025 23:34:17 GMT  
		Size: 21.1 KB (21114 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:b02a75a9d8ff16af6610f5a7b1acbfe5021af039c99e973bba0cb4f3fed4983e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36085902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:706acef80ef55c5c88e96b5e797e157747af5331788d51358c2f14a0a32cd977`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80745399e148b36abf9f846b38e2d897d7b6c9d1520cfa9d06841c00dc04ba59`  
		Last Modified: Mon, 03 Feb 2025 23:29:23 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a519eadeb55cab90fe606d287a41791b2c969bf4b1920d8318fab913251b0af`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 2.7 MB (2708612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884edc77561270bf25675edb3ba73142d461c958c1abe45527aef893945b4ec3`  
		Last Modified: Mon, 03 Feb 2025 23:29:23 GMT  
		Size: 1.3 MB (1330930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61db6406d089d1edef82b5f70d15343ea8e4b58f8deec8f793da379e919d46f4`  
		Last Modified: Mon, 03 Feb 2025 23:29:23 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a63ce5f40ffc44148116e4b48c365aa2eeac8feaf8d8e23f6660428fd6e7a3c`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:45e7cede06534d2e9799fae7a25d6dfdf744eb59fa843709ae6110ecd5a0420f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fa7112b112ab20c85705872120dc8f663e550e84cd97fce814e9153e06f53ea`

```dockerfile
```

-	Layers:
	-	`sha256:fc19ce65e6afd53a0af7fa74af472d2396dc69c87a16470c380123077cc173d2`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 2.3 MB (2293679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:501f87cf15042c748d83d0afebfeeb81b7c41a29ed942369564bb6e9d4ef3c19`  
		Last Modified: Mon, 03 Feb 2025 23:29:23 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; s390x

```console
$ docker pull memcached@sha256:6264d50a0c04cdc558dd1afa71b24ccadf6f5693254e7b6b31bdabb3ddb23995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30261786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0faa3849ef7eee7cd9e65ac3d63ddf439ea062c01ca4cc77c93c1753b1169750`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9009e1bef14c8af1bf770ff23da94f70dcd286b5f120ec1e71bf467ba40a0152`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c02ae601ee0bb3684ac021219c34b71a1227f865794041d376a31389166800`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 2.2 MB (2156339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489cc4b7fa1a8d54bdb06261a5300d09f429439845ae9fca4df8222ac8192830`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 1.2 MB (1245194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa1370e45fc434b599dcc2c02b0f1bec90d080c3af5176313cbd678095b5155`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f034bc901164b6d57bac0a9c94c66e4b96c53fe8af3fea3aee2c74897b480cf7`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:9d8033d81506e7fc653921e3a4c4f23fc13a05f43c5496885c9010f5af0891f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eb0e2cd949a02fe68968891360bbbc13a1fe4e5bdc90f6203a8941b43cca427`

```dockerfile
```

-	Layers:
	-	`sha256:2860febfb3de6c8ffc7c08113a3aaf7f61d254e27d8c2309f5ef39a476925888`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 2.3 MB (2289021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18b61144281568e7ddee023aac2c6947e14e31c547727eb355fa003ca1de66be`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine`

```console
$ docker pull memcached@sha256:b093f7f64a39f20b8f4a671f9c6656eff26821a3c97037a8019448040d6298bd
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
$ docker pull memcached@sha256:c497fc5a323c178e0914eca2500dcf9fa3b21ca2f9932dbc92b51ef6145cf2be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4716328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d2b29f4542cd1fc099ca3146ac53cc0eab71776ce1c029fee5d58a57c38a52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9604a91067e8818541aa31757690c9f8ebf60c58be004baded0767c0999267b8`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592b1cc3d47258eaa3cb466a887cb58e0b2a4176818d1c9a721698abf9337d94`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 104.7 KB (104686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5a55a29aba2a2a27962f2b36f259f5fac81a49009fc7c06020fc992eb6d5da`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 968.6 KB (968568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4786022d0e1453ad1d978f79f50839ba76e4f7c73310640921e5bc212537d6e`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da16032c7fbc5aedc09cd3d43a996943828a731b3ed781664abcf257bdfb65c`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:f4b6389438043b9d6191b9e22e19659d23258e22f0e414f51cb0945287141162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e696a02855f507b1b926a60cf07265433c5ab415467633243c2536753b3090`

```dockerfile
```

-	Layers:
	-	`sha256:16a139d5ff76ba43b3c520a2be58514f36e0ad4a7b0f9adfb6b9c80acb97219d`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 93.6 KB (93627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d8f0efc7a1d5a7dc78219efc6849e55d842b9a5e34ff6bee956735b7cbe2967`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:4d52a91c9cf3612ab9f44d1ecc192f150659288c8826932187c7ab3ed5f8dc9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5082815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef0a8813bf35c3ce3d0d0f9967d27c56db3fb8dc2fd7f31ab4cd3fc1f7cd209`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a202407430ec08b7a5bfb94689fc70aed855fbc1cd8b62ce145147fc5278b7a8`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82c0f1024964e8e055db8178bb0d2595a4a66f7398bffe83d6176cc192ac77e`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 120.8 KB (120783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46624d73285a34a525d44fb1f293cdb9fc95ebfb5b305918bc6a1ff77019fda`  
		Last Modified: Mon, 03 Feb 2025 23:32:18 GMT  
		Size: 968.3 KB (968310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099e6e9c12eb4dfbd63c3bc7cec8de6eb251173a42983594f30413921e56380a`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348cf5001affc34a6f03be6a7f413a6cc377fa11350026995dd53f7db78b85a1`  
		Last Modified: Mon, 03 Feb 2025 23:32:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:631105e348c97a01de96919b82284f666d3283712a23e1b5670c31c88810f40c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff4582dcb2cdec3cfb7590e5b6ade8162439d38a001ff6c08fa81f7d08c669e`

```dockerfile
```

-	Layers:
	-	`sha256:8f4375fd6e27a5ee655f47249469c2214b367ec0146b4e8769a97c6afa3d2829`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 93.7 KB (93731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4bf5d12011dbaae039aec13c76a68a64809e478a3b79d0090ba407f1d4f7c61`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:1f1e5941bca8da9b3aeabcc13c55fe90fc40f9c6476645c19172e508e5302723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4534153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2936f0dd081882d9f0da9ea6113e9780627d3a665a9d909de817c696fac9620`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300aaa75d91b0206b7556a721baaed9f7000ccf73ab8deda59e1cb428ec870f9`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ac94f71cda4f155944d630f60f3e31780c4a97ced13f6c61385dc7e95df429`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 109.5 KB (109465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73b7528b6c4fdfdf4075a75f9e28334049f5461f39426f3b2f983792188c971`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 960.2 KB (960204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb441509973ed0be28152c5ef6c85917a0de941839cd68559be4ecfcc273b17`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e6efaa8bc767e6ef9d48f3b7547a57b7d72964bbb765d7a66481f3f3b36dd1`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:0de21b11722d02a9d2cfc6acf661c6d755de360f4c1f70e7af549cac29e5aef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10be0a79af6bc5d121d12aa89f8e2191eb25f2533cfb4e1de067b3e0bbe82834`

```dockerfile
```

-	Layers:
	-	`sha256:c57cf3137ea2641a839877ddcf3a6065504f38c2ea4f2b7671c1776008e2cfcf`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 93.6 KB (93582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdf7d0d4ee2052676f3563869639942945b1cba543484223915cb33df997a5f0`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 19.5 KB (19512 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:913b5bd251bfe9202c3f0302d3c8c5a4ea3fb7f40f73e8561542c93db1c9d6c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4706076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8083b854e648814b258458b24e3039ade25fa9e63e50b6fb79db7cb05d2ee3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a841f248cda34139a77fd6ab9691e34b7d7dae6dfaedc45a2304aa25c07536`  
		Last Modified: Mon, 03 Feb 2025 23:32:07 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ccea169aa483a5ea29ebe89aa46469affffa54252ac8df2ee75acc10eca2e0`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 124.3 KB (124280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f40e8d115f7e602d9931eaa3e7f41c17dc35a40994befa787615cbd877d430`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 1.0 MB (1006836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf17c8f5e90551f91b3474eb46d197d4ac28e21bf5cb9aaa79eea5b851db371`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9971977dd87dcc447ad6eccbe529fc3c7d6b7dc6b74a4d74fb519c86565318f4`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:04513dfc421f21abd4cd316a69b57cdbfd9d92844a16e9d55eec6a4592cd22d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569bb3d3624a47ed75650ef0a92bfc59d63af78afe540637c817793e9cf4b6d6`

```dockerfile
```

-	Layers:
	-	`sha256:ba709bd16c5785bcfce6f9a8fd6e1d834e101c00d1ed2e018a68a999ec43825b`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 91.7 KB (91734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bc2aa4695d41b4a46d039e0e91f623f3f7aadfd866f0e477637054a37fc5127`  
		Last Modified: Mon, 03 Feb 2025 23:32:07 GMT  
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
$ docker pull memcached@sha256:624036093e557f56a4d500c780f34193af25d5c3b73f8bb08329b579e72b7d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4570369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e3d248b914c5043ad7dc370403b9ea51bf62f972a6f7cf694a023ce14ac2d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223127e71140d5e120db85abbcc459b2ca368e042d165466a1ab8b72ada743f8`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf0ecced8267cdc41066ee8044aa4a0e35e951cba2f51a411ecbfb2cee29819`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 113.5 KB (113450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b7e62f8ce2395ffab9dff807ea14960a2cfa247d7c8a418a5e92d3b4d883f8`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 988.7 KB (988692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed293040c38a686b287b82c3a47615ca2f9034912964f5ce7e832241db526879`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1254936a9326dadc90d0b29d805e446f753a49826f2d9ea9308f5e847d6b7d4`  
		Last Modified: Mon, 03 Feb 2025 23:34:11 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:51c253df33d2a17a62bac93fdc69e4be991e6f4b9e6015eff29ad965c1e58628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 KB (111245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4b6a687d069c6e737d3a9cfa50af30753d0165aa04019517f2f6951bad7feb6`

```dockerfile
```

-	Layers:
	-	`sha256:4e1be19ae90b5f3b2e2b65ad7605851c11804d593bec1671c444bd7aadc3063d`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 91.7 KB (91676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:415673db52745ddb45aa4c05424023581f2903f3acd2578ac008e4857c8ca11b`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 19.6 KB (19569 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine3.21`

```console
$ docker pull memcached@sha256:918f8d596494e94538b93f92d629c3d20efa4d5ca8b0302bf672b65f974c5617
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
$ docker pull memcached@sha256:c497fc5a323c178e0914eca2500dcf9fa3b21ca2f9932dbc92b51ef6145cf2be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4716328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d2b29f4542cd1fc099ca3146ac53cc0eab71776ce1c029fee5d58a57c38a52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9604a91067e8818541aa31757690c9f8ebf60c58be004baded0767c0999267b8`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592b1cc3d47258eaa3cb466a887cb58e0b2a4176818d1c9a721698abf9337d94`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 104.7 KB (104686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5a55a29aba2a2a27962f2b36f259f5fac81a49009fc7c06020fc992eb6d5da`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 968.6 KB (968568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4786022d0e1453ad1d978f79f50839ba76e4f7c73310640921e5bc212537d6e`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da16032c7fbc5aedc09cd3d43a996943828a731b3ed781664abcf257bdfb65c`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:f4b6389438043b9d6191b9e22e19659d23258e22f0e414f51cb0945287141162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e696a02855f507b1b926a60cf07265433c5ab415467633243c2536753b3090`

```dockerfile
```

-	Layers:
	-	`sha256:16a139d5ff76ba43b3c520a2be58514f36e0ad4a7b0f9adfb6b9c80acb97219d`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 93.6 KB (93627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d8f0efc7a1d5a7dc78219efc6849e55d842b9a5e34ff6bee956735b7cbe2967`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:4d52a91c9cf3612ab9f44d1ecc192f150659288c8826932187c7ab3ed5f8dc9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5082815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef0a8813bf35c3ce3d0d0f9967d27c56db3fb8dc2fd7f31ab4cd3fc1f7cd209`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a202407430ec08b7a5bfb94689fc70aed855fbc1cd8b62ce145147fc5278b7a8`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82c0f1024964e8e055db8178bb0d2595a4a66f7398bffe83d6176cc192ac77e`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 120.8 KB (120783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46624d73285a34a525d44fb1f293cdb9fc95ebfb5b305918bc6a1ff77019fda`  
		Last Modified: Mon, 03 Feb 2025 23:32:18 GMT  
		Size: 968.3 KB (968310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099e6e9c12eb4dfbd63c3bc7cec8de6eb251173a42983594f30413921e56380a`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348cf5001affc34a6f03be6a7f413a6cc377fa11350026995dd53f7db78b85a1`  
		Last Modified: Mon, 03 Feb 2025 23:32:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:631105e348c97a01de96919b82284f666d3283712a23e1b5670c31c88810f40c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff4582dcb2cdec3cfb7590e5b6ade8162439d38a001ff6c08fa81f7d08c669e`

```dockerfile
```

-	Layers:
	-	`sha256:8f4375fd6e27a5ee655f47249469c2214b367ec0146b4e8769a97c6afa3d2829`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 93.7 KB (93731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4bf5d12011dbaae039aec13c76a68a64809e478a3b79d0090ba407f1d4f7c61`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.21` - linux; 386

```console
$ docker pull memcached@sha256:1f1e5941bca8da9b3aeabcc13c55fe90fc40f9c6476645c19172e508e5302723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4534153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2936f0dd081882d9f0da9ea6113e9780627d3a665a9d909de817c696fac9620`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300aaa75d91b0206b7556a721baaed9f7000ccf73ab8deda59e1cb428ec870f9`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ac94f71cda4f155944d630f60f3e31780c4a97ced13f6c61385dc7e95df429`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 109.5 KB (109465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73b7528b6c4fdfdf4075a75f9e28334049f5461f39426f3b2f983792188c971`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 960.2 KB (960204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb441509973ed0be28152c5ef6c85917a0de941839cd68559be4ecfcc273b17`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e6efaa8bc767e6ef9d48f3b7547a57b7d72964bbb765d7a66481f3f3b36dd1`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:0de21b11722d02a9d2cfc6acf661c6d755de360f4c1f70e7af549cac29e5aef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10be0a79af6bc5d121d12aa89f8e2191eb25f2533cfb4e1de067b3e0bbe82834`

```dockerfile
```

-	Layers:
	-	`sha256:c57cf3137ea2641a839877ddcf3a6065504f38c2ea4f2b7671c1776008e2cfcf`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 93.6 KB (93582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdf7d0d4ee2052676f3563869639942945b1cba543484223915cb33df997a5f0`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 19.5 KB (19512 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.21` - linux; ppc64le

```console
$ docker pull memcached@sha256:913b5bd251bfe9202c3f0302d3c8c5a4ea3fb7f40f73e8561542c93db1c9d6c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4706076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8083b854e648814b258458b24e3039ade25fa9e63e50b6fb79db7cb05d2ee3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a841f248cda34139a77fd6ab9691e34b7d7dae6dfaedc45a2304aa25c07536`  
		Last Modified: Mon, 03 Feb 2025 23:32:07 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ccea169aa483a5ea29ebe89aa46469affffa54252ac8df2ee75acc10eca2e0`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 124.3 KB (124280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f40e8d115f7e602d9931eaa3e7f41c17dc35a40994befa787615cbd877d430`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 1.0 MB (1006836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf17c8f5e90551f91b3474eb46d197d4ac28e21bf5cb9aaa79eea5b851db371`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9971977dd87dcc447ad6eccbe529fc3c7d6b7dc6b74a4d74fb519c86565318f4`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:04513dfc421f21abd4cd316a69b57cdbfd9d92844a16e9d55eec6a4592cd22d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569bb3d3624a47ed75650ef0a92bfc59d63af78afe540637c817793e9cf4b6d6`

```dockerfile
```

-	Layers:
	-	`sha256:ba709bd16c5785bcfce6f9a8fd6e1d834e101c00d1ed2e018a68a999ec43825b`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 91.7 KB (91734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bc2aa4695d41b4a46d039e0e91f623f3f7aadfd866f0e477637054a37fc5127`  
		Last Modified: Mon, 03 Feb 2025 23:32:07 GMT  
		Size: 19.6 KB (19648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.21` - linux; s390x

```console
$ docker pull memcached@sha256:624036093e557f56a4d500c780f34193af25d5c3b73f8bb08329b579e72b7d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4570369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e3d248b914c5043ad7dc370403b9ea51bf62f972a6f7cf694a023ce14ac2d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223127e71140d5e120db85abbcc459b2ca368e042d165466a1ab8b72ada743f8`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf0ecced8267cdc41066ee8044aa4a0e35e951cba2f51a411ecbfb2cee29819`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 113.5 KB (113450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b7e62f8ce2395ffab9dff807ea14960a2cfa247d7c8a418a5e92d3b4d883f8`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 988.7 KB (988692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed293040c38a686b287b82c3a47615ca2f9034912964f5ce7e832241db526879`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1254936a9326dadc90d0b29d805e446f753a49826f2d9ea9308f5e847d6b7d4`  
		Last Modified: Mon, 03 Feb 2025 23:34:11 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:51c253df33d2a17a62bac93fdc69e4be991e6f4b9e6015eff29ad965c1e58628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 KB (111245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4b6a687d069c6e737d3a9cfa50af30753d0165aa04019517f2f6951bad7feb6`

```dockerfile
```

-	Layers:
	-	`sha256:4e1be19ae90b5f3b2e2b65ad7605851c11804d593bec1671c444bd7aadc3063d`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 91.7 KB (91676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:415673db52745ddb45aa4c05424023581f2903f3acd2578ac008e4857c8ca11b`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 19.6 KB (19569 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-bookworm`

```console
$ docker pull memcached@sha256:e099ebae6550a39ef5f780dc869ac48f17d87b09381a38ab0bc256a28a9e5d13
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
$ docker pull memcached@sha256:dfd99fb6fbe04b3121b1213ae0116e8d3703d1d329acc9b57ec40fe212c3d159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31972808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca71139ab2ab780916cc2410aeed46bd583f7d5b2f02e1df59647c913e1d933`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda7d6399fc25890be33d8e323a35feb9051c4a87322b3208defbca52c54b3be`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c0be3187b2dee7a02dfd52f423dc252930e248c53682a6a882a103aa3eec3a`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 2.5 MB (2491797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5808fec11b221c18511c8299b00aff12cf1fe592c5b7373edfd4c148480cb7f`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 1.3 MB (1267080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8745b39a0f5680ef45825db431aaa46b60468a8cdd43fed4fc477a4bffd35bbe`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d828e056dad95d08aea41b29d33fb1a2961ae61a4ce685a1b79a02a2569b7b0`  
		Last Modified: Mon, 03 Feb 2025 23:29:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:6b285e2b8239906b90664744391f1a4b6c3a3da8cae91273f01297a854b0b2aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18097e9c39f7331f3c6935c455fb1eeb3c8e451903fc73c9bdfae63c74cd99f8`

```dockerfile
```

-	Layers:
	-	`sha256:5be7ae24c2c09eaa07fd11802534cc38c1b5c8c6e32197189c0f2ece969e78b8`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 2.3 MB (2289307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce1fc3a95808478b79eae466f1bd195255ed42e1964471932ef4fa504b1a09ef`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:19cea7f4ef8974d31946d26f29af52dac2ef01f7839f9b18dc8a5c153dbb57bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29079481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8148d94dfb620e9b264755a021f81a0997844649fe9eef185c47837e87bdf9a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7a3fc1134bc1af98e13c0b7ea743c863d5a17f830a5fbd5a7002f750500e76c2`  
		Last Modified: Tue, 14 Jan 2025 01:33:27 GMT  
		Size: 25.7 MB (25736665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a566614fdcf63df3667efc0e44ef3a55e3691eced03cf22a308d708142f7c6`  
		Last Modified: Tue, 14 Jan 2025 02:34:26 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92a25a27c2144d0ab56f557820ebe289d1620f435ddb83f14c5e48b8d08cfa5`  
		Last Modified: Tue, 14 Jan 2025 02:34:27 GMT  
		Size: 2.1 MB (2096089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8889c18344163aeaea76936cd52029ec9bb42c2e16e0f26f48a664f00c3b7694`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 1.2 MB (1245215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68b0d4672ce5cd7584f0b15c42f219e41de7fb1f28644186a8a0f9788d2c96b`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbe1e74de797ff5b1fd4cf0a27d11ceeaf02347c856cfb5ba74cc13f4de8e6d`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:4af105a2f6c653acc913a722d6b3636c3637fe2718478bab2f4b1abf3a3df4b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb88776c99ff589e69412231781b8d108a5bd931b770d38eb94fdd69f0a97a1a`

```dockerfile
```

-	Layers:
	-	`sha256:f09d82aaa941a644405f9f34074de377bbd24b82df23d0ad6a22113f9aa74e41`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 2.3 MB (2292845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97bf9ecad7b0ab53e19b325ab9725de040ddcb369051fb8205db981408ba2764`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:0f287535bdbb8cfef4d259f59bcf13f2c3441335d3cff34f7d7c78830d4562b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31658415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536cfc0e620927f7137462160084b2211a938273db79693852e1834a3b0d7c0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66214caa62a6aa92636721a38d0e11a5fc383b1f9e4697a0991f5749369033c3`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca115360faf332637b0231cd4f43e98f284331aa2fb9bfbc45ec5d80a9eb57df`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 2.4 MB (2355304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5afe04d2434c6e19998a9fe47bfcf571759106e85ec73dd6ee83420494e2c8`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 1.3 MB (1260566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35e7292944fc376dd9f2578cf538f85a6df80492f5bc136e0024733aaeac8f0`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d44c4ade766e17abf585eb36d6683321ce9a2a26385b582758cda3872122039`  
		Last Modified: Mon, 03 Feb 2025 23:29:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:50321a237d4e2507a4e56d52d627e5ccb079e3bc300cc806390e96d09fb523a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e624df56f2e01bac1680fa105c39d9e35149d5cef920cd68e7266d5b2214f8d`

```dockerfile
```

-	Layers:
	-	`sha256:8be58e9cbbf71c38228da76c2508cdc0fcb85586ccc4b49518cf69e1e5e39b50`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 2.3 MB (2289622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caf4d0d59deb6f3fb187901e3b525ab0c834bb3cb6809eea8fb0c6879572ae3e`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 21.4 KB (21418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:f5be026a6f23f855459f3627e5c4101a938bca13100113b9fe82f28b3cb1cf3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32956119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d4368d3996e2021d38fdf63f7863d74ba28d6a2ef74e5131b0397dc12d442c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9009e1bef14c8af1bf770ff23da94f70dcd286b5f120ec1e71bf467ba40a0152`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f865fc757eeb18e208170c47e11bd3a00afa6eb223213d4007662aa6512c80dd`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 2.5 MB (2500709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34d14b87df5dcc8c799103bf14f9f622bc25c16e005e1e47b6a1306697bdf88`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 1.3 MB (1266299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d338f828cfbf806035a35f4290e62f96efce17c0e99cdf3034490cf047f32e1`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4697356823aab23c184948db8f06aa7c6811e207a99f109d4a0c115be482fb`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:7286999a5f604e3b4cc31c213c4c8d0cfa8b0da817e69563a83d6e14b14b7d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1456afa32760c7ecf3b6aa1f216615797de142ac46f0ee174b33ac71c2ed02a9`

```dockerfile
```

-	Layers:
	-	`sha256:7fe0965b391e043a806dd694395597114730be5687d0427a2011870ec7c674b4`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 2.3 MB (2286406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a6fca6555d8d2e7146c7a1f88c47abe5539931256a2f3990c263cf00390198a`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:9db344d39627ceb6b7961e5715daa16b063785632772a10a4f8953a4c131d3c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31692251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e517b7e21ed68b2abcdb3c957e98a677c411bf1b72ef4b78aa09b5bbcd0dc9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b08d7e697b04bda8cef97763765ebbbc16790e22945b5ab31d97d448a15c8650`  
		Last Modified: Tue, 14 Jan 2025 01:38:32 GMT  
		Size: 28.5 MB (28486647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda5f653b677ccaab1e67a8e7dce8f1c207af2b166ac4d37ddb395d85cb07a4c`  
		Last Modified: Tue, 14 Jan 2025 03:20:56 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bebcbc9eca024edee3e9bcea840742795d739cc90b447152cd52cf5dd79c442`  
		Last Modified: Mon, 03 Feb 2025 23:34:18 GMT  
		Size: 1.9 MB (1943213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d20ac443403dd981e7eca81d524af67815754bca86f5705e011ca0541a6ec0d`  
		Last Modified: Mon, 03 Feb 2025 23:34:18 GMT  
		Size: 1.3 MB (1260877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3be7f64ea082d115fc02a30fe0fa678d78bee0b27ac846dbdb688550d1908a0`  
		Last Modified: Mon, 03 Feb 2025 23:34:17 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1254936a9326dadc90d0b29d805e446f753a49826f2d9ea9308f5e847d6b7d4`  
		Last Modified: Mon, 03 Feb 2025 23:34:11 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:1ebb48a31e269c5b575e78e45853282855121ca1b723662138823061912b9f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7e22e388cefc5c2c0f77535a596b93848dd4fb8af57e9b54911aeca7ecd4be`

```dockerfile
```

-	Layers:
	-	`sha256:cb8d0d9b1786b7f482fc6383b420cee035f995c0616e30e3cb1699457e8b79da`  
		Last Modified: Mon, 03 Feb 2025 23:34:17 GMT  
		Size: 21.1 KB (21114 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:b02a75a9d8ff16af6610f5a7b1acbfe5021af039c99e973bba0cb4f3fed4983e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36085902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:706acef80ef55c5c88e96b5e797e157747af5331788d51358c2f14a0a32cd977`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80745399e148b36abf9f846b38e2d897d7b6c9d1520cfa9d06841c00dc04ba59`  
		Last Modified: Mon, 03 Feb 2025 23:29:23 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a519eadeb55cab90fe606d287a41791b2c969bf4b1920d8318fab913251b0af`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 2.7 MB (2708612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884edc77561270bf25675edb3ba73142d461c958c1abe45527aef893945b4ec3`  
		Last Modified: Mon, 03 Feb 2025 23:29:23 GMT  
		Size: 1.3 MB (1330930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61db6406d089d1edef82b5f70d15343ea8e4b58f8deec8f793da379e919d46f4`  
		Last Modified: Mon, 03 Feb 2025 23:29:23 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a63ce5f40ffc44148116e4b48c365aa2eeac8feaf8d8e23f6660428fd6e7a3c`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:45e7cede06534d2e9799fae7a25d6dfdf744eb59fa843709ae6110ecd5a0420f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fa7112b112ab20c85705872120dc8f663e550e84cd97fce814e9153e06f53ea`

```dockerfile
```

-	Layers:
	-	`sha256:fc19ce65e6afd53a0af7fa74af472d2396dc69c87a16470c380123077cc173d2`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 2.3 MB (2293679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:501f87cf15042c748d83d0afebfeeb81b7c41a29ed942369564bb6e9d4ef3c19`  
		Last Modified: Mon, 03 Feb 2025 23:29:23 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:6264d50a0c04cdc558dd1afa71b24ccadf6f5693254e7b6b31bdabb3ddb23995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30261786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0faa3849ef7eee7cd9e65ac3d63ddf439ea062c01ca4cc77c93c1753b1169750`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9009e1bef14c8af1bf770ff23da94f70dcd286b5f120ec1e71bf467ba40a0152`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c02ae601ee0bb3684ac021219c34b71a1227f865794041d376a31389166800`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 2.2 MB (2156339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489cc4b7fa1a8d54bdb06261a5300d09f429439845ae9fca4df8222ac8192830`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 1.2 MB (1245194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa1370e45fc434b599dcc2c02b0f1bec90d080c3af5176313cbd678095b5155`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f034bc901164b6d57bac0a9c94c66e4b96c53fe8af3fea3aee2c74897b480cf7`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:9d8033d81506e7fc653921e3a4c4f23fc13a05f43c5496885c9010f5af0891f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eb0e2cd949a02fe68968891360bbbc13a1fe4e5bdc90f6203a8941b43cca427`

```dockerfile
```

-	Layers:
	-	`sha256:2860febfb3de6c8ffc7c08113a3aaf7f61d254e27d8c2309f5ef39a476925888`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 2.3 MB (2289021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18b61144281568e7ddee023aac2c6947e14e31c547727eb355fa003ca1de66be`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.35`

```console
$ docker pull memcached@sha256:e099ebae6550a39ef5f780dc869ac48f17d87b09381a38ab0bc256a28a9e5d13
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

### `memcached:1.6.35` - linux; amd64

```console
$ docker pull memcached@sha256:dfd99fb6fbe04b3121b1213ae0116e8d3703d1d329acc9b57ec40fe212c3d159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31972808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca71139ab2ab780916cc2410aeed46bd583f7d5b2f02e1df59647c913e1d933`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda7d6399fc25890be33d8e323a35feb9051c4a87322b3208defbca52c54b3be`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c0be3187b2dee7a02dfd52f423dc252930e248c53682a6a882a103aa3eec3a`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 2.5 MB (2491797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5808fec11b221c18511c8299b00aff12cf1fe592c5b7373edfd4c148480cb7f`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 1.3 MB (1267080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8745b39a0f5680ef45825db431aaa46b60468a8cdd43fed4fc477a4bffd35bbe`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d828e056dad95d08aea41b29d33fb1a2961ae61a4ce685a1b79a02a2569b7b0`  
		Last Modified: Mon, 03 Feb 2025 23:29:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.35` - unknown; unknown

```console
$ docker pull memcached@sha256:6b285e2b8239906b90664744391f1a4b6c3a3da8cae91273f01297a854b0b2aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18097e9c39f7331f3c6935c455fb1eeb3c8e451903fc73c9bdfae63c74cd99f8`

```dockerfile
```

-	Layers:
	-	`sha256:5be7ae24c2c09eaa07fd11802534cc38c1b5c8c6e32197189c0f2ece969e78b8`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 2.3 MB (2289307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce1fc3a95808478b79eae466f1bd195255ed42e1964471932ef4fa504b1a09ef`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.35` - linux; arm variant v5

```console
$ docker pull memcached@sha256:19cea7f4ef8974d31946d26f29af52dac2ef01f7839f9b18dc8a5c153dbb57bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29079481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8148d94dfb620e9b264755a021f81a0997844649fe9eef185c47837e87bdf9a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7a3fc1134bc1af98e13c0b7ea743c863d5a17f830a5fbd5a7002f750500e76c2`  
		Last Modified: Tue, 14 Jan 2025 01:33:27 GMT  
		Size: 25.7 MB (25736665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a566614fdcf63df3667efc0e44ef3a55e3691eced03cf22a308d708142f7c6`  
		Last Modified: Tue, 14 Jan 2025 02:34:26 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92a25a27c2144d0ab56f557820ebe289d1620f435ddb83f14c5e48b8d08cfa5`  
		Last Modified: Tue, 14 Jan 2025 02:34:27 GMT  
		Size: 2.1 MB (2096089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8889c18344163aeaea76936cd52029ec9bb42c2e16e0f26f48a664f00c3b7694`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 1.2 MB (1245215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68b0d4672ce5cd7584f0b15c42f219e41de7fb1f28644186a8a0f9788d2c96b`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbe1e74de797ff5b1fd4cf0a27d11ceeaf02347c856cfb5ba74cc13f4de8e6d`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.35` - unknown; unknown

```console
$ docker pull memcached@sha256:4af105a2f6c653acc913a722d6b3636c3637fe2718478bab2f4b1abf3a3df4b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb88776c99ff589e69412231781b8d108a5bd931b770d38eb94fdd69f0a97a1a`

```dockerfile
```

-	Layers:
	-	`sha256:f09d82aaa941a644405f9f34074de377bbd24b82df23d0ad6a22113f9aa74e41`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 2.3 MB (2292845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97bf9ecad7b0ab53e19b325ab9725de040ddcb369051fb8205db981408ba2764`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.35` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:0f287535bdbb8cfef4d259f59bcf13f2c3441335d3cff34f7d7c78830d4562b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31658415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536cfc0e620927f7137462160084b2211a938273db79693852e1834a3b0d7c0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66214caa62a6aa92636721a38d0e11a5fc383b1f9e4697a0991f5749369033c3`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca115360faf332637b0231cd4f43e98f284331aa2fb9bfbc45ec5d80a9eb57df`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 2.4 MB (2355304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5afe04d2434c6e19998a9fe47bfcf571759106e85ec73dd6ee83420494e2c8`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 1.3 MB (1260566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35e7292944fc376dd9f2578cf538f85a6df80492f5bc136e0024733aaeac8f0`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d44c4ade766e17abf585eb36d6683321ce9a2a26385b582758cda3872122039`  
		Last Modified: Mon, 03 Feb 2025 23:29:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.35` - unknown; unknown

```console
$ docker pull memcached@sha256:50321a237d4e2507a4e56d52d627e5ccb079e3bc300cc806390e96d09fb523a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e624df56f2e01bac1680fa105c39d9e35149d5cef920cd68e7266d5b2214f8d`

```dockerfile
```

-	Layers:
	-	`sha256:8be58e9cbbf71c38228da76c2508cdc0fcb85586ccc4b49518cf69e1e5e39b50`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 2.3 MB (2289622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caf4d0d59deb6f3fb187901e3b525ab0c834bb3cb6809eea8fb0c6879572ae3e`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 21.4 KB (21418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.35` - linux; 386

```console
$ docker pull memcached@sha256:f5be026a6f23f855459f3627e5c4101a938bca13100113b9fe82f28b3cb1cf3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32956119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d4368d3996e2021d38fdf63f7863d74ba28d6a2ef74e5131b0397dc12d442c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9009e1bef14c8af1bf770ff23da94f70dcd286b5f120ec1e71bf467ba40a0152`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f865fc757eeb18e208170c47e11bd3a00afa6eb223213d4007662aa6512c80dd`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 2.5 MB (2500709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34d14b87df5dcc8c799103bf14f9f622bc25c16e005e1e47b6a1306697bdf88`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 1.3 MB (1266299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d338f828cfbf806035a35f4290e62f96efce17c0e99cdf3034490cf047f32e1`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4697356823aab23c184948db8f06aa7c6811e207a99f109d4a0c115be482fb`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.35` - unknown; unknown

```console
$ docker pull memcached@sha256:7286999a5f604e3b4cc31c213c4c8d0cfa8b0da817e69563a83d6e14b14b7d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1456afa32760c7ecf3b6aa1f216615797de142ac46f0ee174b33ac71c2ed02a9`

```dockerfile
```

-	Layers:
	-	`sha256:7fe0965b391e043a806dd694395597114730be5687d0427a2011870ec7c674b4`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 2.3 MB (2286406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a6fca6555d8d2e7146c7a1f88c47abe5539931256a2f3990c263cf00390198a`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.35` - linux; mips64le

```console
$ docker pull memcached@sha256:9db344d39627ceb6b7961e5715daa16b063785632772a10a4f8953a4c131d3c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31692251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e517b7e21ed68b2abcdb3c957e98a677c411bf1b72ef4b78aa09b5bbcd0dc9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b08d7e697b04bda8cef97763765ebbbc16790e22945b5ab31d97d448a15c8650`  
		Last Modified: Tue, 14 Jan 2025 01:38:32 GMT  
		Size: 28.5 MB (28486647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda5f653b677ccaab1e67a8e7dce8f1c207af2b166ac4d37ddb395d85cb07a4c`  
		Last Modified: Tue, 14 Jan 2025 03:20:56 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bebcbc9eca024edee3e9bcea840742795d739cc90b447152cd52cf5dd79c442`  
		Last Modified: Mon, 03 Feb 2025 23:34:18 GMT  
		Size: 1.9 MB (1943213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d20ac443403dd981e7eca81d524af67815754bca86f5705e011ca0541a6ec0d`  
		Last Modified: Mon, 03 Feb 2025 23:34:18 GMT  
		Size: 1.3 MB (1260877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3be7f64ea082d115fc02a30fe0fa678d78bee0b27ac846dbdb688550d1908a0`  
		Last Modified: Mon, 03 Feb 2025 23:34:17 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1254936a9326dadc90d0b29d805e446f753a49826f2d9ea9308f5e847d6b7d4`  
		Last Modified: Mon, 03 Feb 2025 23:34:11 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.35` - unknown; unknown

```console
$ docker pull memcached@sha256:1ebb48a31e269c5b575e78e45853282855121ca1b723662138823061912b9f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7e22e388cefc5c2c0f77535a596b93848dd4fb8af57e9b54911aeca7ecd4be`

```dockerfile
```

-	Layers:
	-	`sha256:cb8d0d9b1786b7f482fc6383b420cee035f995c0616e30e3cb1699457e8b79da`  
		Last Modified: Mon, 03 Feb 2025 23:34:17 GMT  
		Size: 21.1 KB (21114 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.35` - linux; ppc64le

```console
$ docker pull memcached@sha256:b02a75a9d8ff16af6610f5a7b1acbfe5021af039c99e973bba0cb4f3fed4983e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36085902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:706acef80ef55c5c88e96b5e797e157747af5331788d51358c2f14a0a32cd977`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80745399e148b36abf9f846b38e2d897d7b6c9d1520cfa9d06841c00dc04ba59`  
		Last Modified: Mon, 03 Feb 2025 23:29:23 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a519eadeb55cab90fe606d287a41791b2c969bf4b1920d8318fab913251b0af`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 2.7 MB (2708612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884edc77561270bf25675edb3ba73142d461c958c1abe45527aef893945b4ec3`  
		Last Modified: Mon, 03 Feb 2025 23:29:23 GMT  
		Size: 1.3 MB (1330930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61db6406d089d1edef82b5f70d15343ea8e4b58f8deec8f793da379e919d46f4`  
		Last Modified: Mon, 03 Feb 2025 23:29:23 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a63ce5f40ffc44148116e4b48c365aa2eeac8feaf8d8e23f6660428fd6e7a3c`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.35` - unknown; unknown

```console
$ docker pull memcached@sha256:45e7cede06534d2e9799fae7a25d6dfdf744eb59fa843709ae6110ecd5a0420f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fa7112b112ab20c85705872120dc8f663e550e84cd97fce814e9153e06f53ea`

```dockerfile
```

-	Layers:
	-	`sha256:fc19ce65e6afd53a0af7fa74af472d2396dc69c87a16470c380123077cc173d2`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 2.3 MB (2293679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:501f87cf15042c748d83d0afebfeeb81b7c41a29ed942369564bb6e9d4ef3c19`  
		Last Modified: Mon, 03 Feb 2025 23:29:23 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.35` - linux; s390x

```console
$ docker pull memcached@sha256:6264d50a0c04cdc558dd1afa71b24ccadf6f5693254e7b6b31bdabb3ddb23995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30261786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0faa3849ef7eee7cd9e65ac3d63ddf439ea062c01ca4cc77c93c1753b1169750`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9009e1bef14c8af1bf770ff23da94f70dcd286b5f120ec1e71bf467ba40a0152`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c02ae601ee0bb3684ac021219c34b71a1227f865794041d376a31389166800`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 2.2 MB (2156339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489cc4b7fa1a8d54bdb06261a5300d09f429439845ae9fca4df8222ac8192830`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 1.2 MB (1245194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa1370e45fc434b599dcc2c02b0f1bec90d080c3af5176313cbd678095b5155`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f034bc901164b6d57bac0a9c94c66e4b96c53fe8af3fea3aee2c74897b480cf7`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.35` - unknown; unknown

```console
$ docker pull memcached@sha256:9d8033d81506e7fc653921e3a4c4f23fc13a05f43c5496885c9010f5af0891f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eb0e2cd949a02fe68968891360bbbc13a1fe4e5bdc90f6203a8941b43cca427`

```dockerfile
```

-	Layers:
	-	`sha256:2860febfb3de6c8ffc7c08113a3aaf7f61d254e27d8c2309f5ef39a476925888`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 2.3 MB (2289021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18b61144281568e7ddee023aac2c6947e14e31c547727eb355fa003ca1de66be`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.35-alpine`

```console
$ docker pull memcached@sha256:918f8d596494e94538b93f92d629c3d20efa4d5ca8b0302bf672b65f974c5617
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

### `memcached:1.6.35-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:c497fc5a323c178e0914eca2500dcf9fa3b21ca2f9932dbc92b51ef6145cf2be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4716328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d2b29f4542cd1fc099ca3146ac53cc0eab71776ce1c029fee5d58a57c38a52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9604a91067e8818541aa31757690c9f8ebf60c58be004baded0767c0999267b8`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592b1cc3d47258eaa3cb466a887cb58e0b2a4176818d1c9a721698abf9337d94`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 104.7 KB (104686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5a55a29aba2a2a27962f2b36f259f5fac81a49009fc7c06020fc992eb6d5da`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 968.6 KB (968568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4786022d0e1453ad1d978f79f50839ba76e4f7c73310640921e5bc212537d6e`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da16032c7fbc5aedc09cd3d43a996943828a731b3ed781664abcf257bdfb65c`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.35-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:f4b6389438043b9d6191b9e22e19659d23258e22f0e414f51cb0945287141162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e696a02855f507b1b926a60cf07265433c5ab415467633243c2536753b3090`

```dockerfile
```

-	Layers:
	-	`sha256:16a139d5ff76ba43b3c520a2be58514f36e0ad4a7b0f9adfb6b9c80acb97219d`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 93.6 KB (93627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d8f0efc7a1d5a7dc78219efc6849e55d842b9a5e34ff6bee956735b7cbe2967`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.35-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:4d52a91c9cf3612ab9f44d1ecc192f150659288c8826932187c7ab3ed5f8dc9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5082815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef0a8813bf35c3ce3d0d0f9967d27c56db3fb8dc2fd7f31ab4cd3fc1f7cd209`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a202407430ec08b7a5bfb94689fc70aed855fbc1cd8b62ce145147fc5278b7a8`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82c0f1024964e8e055db8178bb0d2595a4a66f7398bffe83d6176cc192ac77e`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 120.8 KB (120783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46624d73285a34a525d44fb1f293cdb9fc95ebfb5b305918bc6a1ff77019fda`  
		Last Modified: Mon, 03 Feb 2025 23:32:18 GMT  
		Size: 968.3 KB (968310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099e6e9c12eb4dfbd63c3bc7cec8de6eb251173a42983594f30413921e56380a`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348cf5001affc34a6f03be6a7f413a6cc377fa11350026995dd53f7db78b85a1`  
		Last Modified: Mon, 03 Feb 2025 23:32:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.35-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:631105e348c97a01de96919b82284f666d3283712a23e1b5670c31c88810f40c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff4582dcb2cdec3cfb7590e5b6ade8162439d38a001ff6c08fa81f7d08c669e`

```dockerfile
```

-	Layers:
	-	`sha256:8f4375fd6e27a5ee655f47249469c2214b367ec0146b4e8769a97c6afa3d2829`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 93.7 KB (93731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4bf5d12011dbaae039aec13c76a68a64809e478a3b79d0090ba407f1d4f7c61`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.35-alpine` - linux; 386

```console
$ docker pull memcached@sha256:1f1e5941bca8da9b3aeabcc13c55fe90fc40f9c6476645c19172e508e5302723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4534153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2936f0dd081882d9f0da9ea6113e9780627d3a665a9d909de817c696fac9620`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300aaa75d91b0206b7556a721baaed9f7000ccf73ab8deda59e1cb428ec870f9`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ac94f71cda4f155944d630f60f3e31780c4a97ced13f6c61385dc7e95df429`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 109.5 KB (109465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73b7528b6c4fdfdf4075a75f9e28334049f5461f39426f3b2f983792188c971`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 960.2 KB (960204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb441509973ed0be28152c5ef6c85917a0de941839cd68559be4ecfcc273b17`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e6efaa8bc767e6ef9d48f3b7547a57b7d72964bbb765d7a66481f3f3b36dd1`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.35-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:0de21b11722d02a9d2cfc6acf661c6d755de360f4c1f70e7af549cac29e5aef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10be0a79af6bc5d121d12aa89f8e2191eb25f2533cfb4e1de067b3e0bbe82834`

```dockerfile
```

-	Layers:
	-	`sha256:c57cf3137ea2641a839877ddcf3a6065504f38c2ea4f2b7671c1776008e2cfcf`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 93.6 KB (93582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdf7d0d4ee2052676f3563869639942945b1cba543484223915cb33df997a5f0`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 19.5 KB (19512 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.35-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:913b5bd251bfe9202c3f0302d3c8c5a4ea3fb7f40f73e8561542c93db1c9d6c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4706076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8083b854e648814b258458b24e3039ade25fa9e63e50b6fb79db7cb05d2ee3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a841f248cda34139a77fd6ab9691e34b7d7dae6dfaedc45a2304aa25c07536`  
		Last Modified: Mon, 03 Feb 2025 23:32:07 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ccea169aa483a5ea29ebe89aa46469affffa54252ac8df2ee75acc10eca2e0`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 124.3 KB (124280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f40e8d115f7e602d9931eaa3e7f41c17dc35a40994befa787615cbd877d430`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 1.0 MB (1006836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf17c8f5e90551f91b3474eb46d197d4ac28e21bf5cb9aaa79eea5b851db371`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9971977dd87dcc447ad6eccbe529fc3c7d6b7dc6b74a4d74fb519c86565318f4`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.35-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:04513dfc421f21abd4cd316a69b57cdbfd9d92844a16e9d55eec6a4592cd22d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569bb3d3624a47ed75650ef0a92bfc59d63af78afe540637c817793e9cf4b6d6`

```dockerfile
```

-	Layers:
	-	`sha256:ba709bd16c5785bcfce6f9a8fd6e1d834e101c00d1ed2e018a68a999ec43825b`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 91.7 KB (91734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bc2aa4695d41b4a46d039e0e91f623f3f7aadfd866f0e477637054a37fc5127`  
		Last Modified: Mon, 03 Feb 2025 23:32:07 GMT  
		Size: 19.6 KB (19648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.35-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:624036093e557f56a4d500c780f34193af25d5c3b73f8bb08329b579e72b7d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4570369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e3d248b914c5043ad7dc370403b9ea51bf62f972a6f7cf694a023ce14ac2d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223127e71140d5e120db85abbcc459b2ca368e042d165466a1ab8b72ada743f8`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf0ecced8267cdc41066ee8044aa4a0e35e951cba2f51a411ecbfb2cee29819`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 113.5 KB (113450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b7e62f8ce2395ffab9dff807ea14960a2cfa247d7c8a418a5e92d3b4d883f8`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 988.7 KB (988692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed293040c38a686b287b82c3a47615ca2f9034912964f5ce7e832241db526879`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1254936a9326dadc90d0b29d805e446f753a49826f2d9ea9308f5e847d6b7d4`  
		Last Modified: Mon, 03 Feb 2025 23:34:11 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.35-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:51c253df33d2a17a62bac93fdc69e4be991e6f4b9e6015eff29ad965c1e58628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 KB (111245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4b6a687d069c6e737d3a9cfa50af30753d0165aa04019517f2f6951bad7feb6`

```dockerfile
```

-	Layers:
	-	`sha256:4e1be19ae90b5f3b2e2b65ad7605851c11804d593bec1671c444bd7aadc3063d`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 91.7 KB (91676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:415673db52745ddb45aa4c05424023581f2903f3acd2578ac008e4857c8ca11b`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 19.6 KB (19569 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.35-alpine3.21`

```console
$ docker pull memcached@sha256:918f8d596494e94538b93f92d629c3d20efa4d5ca8b0302bf672b65f974c5617
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

### `memcached:1.6.35-alpine3.21` - linux; amd64

```console
$ docker pull memcached@sha256:c497fc5a323c178e0914eca2500dcf9fa3b21ca2f9932dbc92b51ef6145cf2be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4716328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d2b29f4542cd1fc099ca3146ac53cc0eab71776ce1c029fee5d58a57c38a52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9604a91067e8818541aa31757690c9f8ebf60c58be004baded0767c0999267b8`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592b1cc3d47258eaa3cb466a887cb58e0b2a4176818d1c9a721698abf9337d94`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 104.7 KB (104686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5a55a29aba2a2a27962f2b36f259f5fac81a49009fc7c06020fc992eb6d5da`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 968.6 KB (968568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4786022d0e1453ad1d978f79f50839ba76e4f7c73310640921e5bc212537d6e`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da16032c7fbc5aedc09cd3d43a996943828a731b3ed781664abcf257bdfb65c`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.35-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:f4b6389438043b9d6191b9e22e19659d23258e22f0e414f51cb0945287141162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e696a02855f507b1b926a60cf07265433c5ab415467633243c2536753b3090`

```dockerfile
```

-	Layers:
	-	`sha256:16a139d5ff76ba43b3c520a2be58514f36e0ad4a7b0f9adfb6b9c80acb97219d`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 93.6 KB (93627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d8f0efc7a1d5a7dc78219efc6849e55d842b9a5e34ff6bee956735b7cbe2967`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.35-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:4d52a91c9cf3612ab9f44d1ecc192f150659288c8826932187c7ab3ed5f8dc9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5082815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef0a8813bf35c3ce3d0d0f9967d27c56db3fb8dc2fd7f31ab4cd3fc1f7cd209`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a202407430ec08b7a5bfb94689fc70aed855fbc1cd8b62ce145147fc5278b7a8`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82c0f1024964e8e055db8178bb0d2595a4a66f7398bffe83d6176cc192ac77e`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 120.8 KB (120783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46624d73285a34a525d44fb1f293cdb9fc95ebfb5b305918bc6a1ff77019fda`  
		Last Modified: Mon, 03 Feb 2025 23:32:18 GMT  
		Size: 968.3 KB (968310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099e6e9c12eb4dfbd63c3bc7cec8de6eb251173a42983594f30413921e56380a`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348cf5001affc34a6f03be6a7f413a6cc377fa11350026995dd53f7db78b85a1`  
		Last Modified: Mon, 03 Feb 2025 23:32:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.35-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:631105e348c97a01de96919b82284f666d3283712a23e1b5670c31c88810f40c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff4582dcb2cdec3cfb7590e5b6ade8162439d38a001ff6c08fa81f7d08c669e`

```dockerfile
```

-	Layers:
	-	`sha256:8f4375fd6e27a5ee655f47249469c2214b367ec0146b4e8769a97c6afa3d2829`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 93.7 KB (93731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4bf5d12011dbaae039aec13c76a68a64809e478a3b79d0090ba407f1d4f7c61`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.35-alpine3.21` - linux; 386

```console
$ docker pull memcached@sha256:1f1e5941bca8da9b3aeabcc13c55fe90fc40f9c6476645c19172e508e5302723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4534153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2936f0dd081882d9f0da9ea6113e9780627d3a665a9d909de817c696fac9620`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300aaa75d91b0206b7556a721baaed9f7000ccf73ab8deda59e1cb428ec870f9`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ac94f71cda4f155944d630f60f3e31780c4a97ced13f6c61385dc7e95df429`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 109.5 KB (109465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73b7528b6c4fdfdf4075a75f9e28334049f5461f39426f3b2f983792188c971`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 960.2 KB (960204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb441509973ed0be28152c5ef6c85917a0de941839cd68559be4ecfcc273b17`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e6efaa8bc767e6ef9d48f3b7547a57b7d72964bbb765d7a66481f3f3b36dd1`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.35-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:0de21b11722d02a9d2cfc6acf661c6d755de360f4c1f70e7af549cac29e5aef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10be0a79af6bc5d121d12aa89f8e2191eb25f2533cfb4e1de067b3e0bbe82834`

```dockerfile
```

-	Layers:
	-	`sha256:c57cf3137ea2641a839877ddcf3a6065504f38c2ea4f2b7671c1776008e2cfcf`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 93.6 KB (93582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdf7d0d4ee2052676f3563869639942945b1cba543484223915cb33df997a5f0`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 19.5 KB (19512 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.35-alpine3.21` - linux; ppc64le

```console
$ docker pull memcached@sha256:913b5bd251bfe9202c3f0302d3c8c5a4ea3fb7f40f73e8561542c93db1c9d6c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4706076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8083b854e648814b258458b24e3039ade25fa9e63e50b6fb79db7cb05d2ee3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a841f248cda34139a77fd6ab9691e34b7d7dae6dfaedc45a2304aa25c07536`  
		Last Modified: Mon, 03 Feb 2025 23:32:07 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ccea169aa483a5ea29ebe89aa46469affffa54252ac8df2ee75acc10eca2e0`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 124.3 KB (124280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f40e8d115f7e602d9931eaa3e7f41c17dc35a40994befa787615cbd877d430`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 1.0 MB (1006836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf17c8f5e90551f91b3474eb46d197d4ac28e21bf5cb9aaa79eea5b851db371`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9971977dd87dcc447ad6eccbe529fc3c7d6b7dc6b74a4d74fb519c86565318f4`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.35-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:04513dfc421f21abd4cd316a69b57cdbfd9d92844a16e9d55eec6a4592cd22d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569bb3d3624a47ed75650ef0a92bfc59d63af78afe540637c817793e9cf4b6d6`

```dockerfile
```

-	Layers:
	-	`sha256:ba709bd16c5785bcfce6f9a8fd6e1d834e101c00d1ed2e018a68a999ec43825b`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 91.7 KB (91734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bc2aa4695d41b4a46d039e0e91f623f3f7aadfd866f0e477637054a37fc5127`  
		Last Modified: Mon, 03 Feb 2025 23:32:07 GMT  
		Size: 19.6 KB (19648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.35-alpine3.21` - linux; s390x

```console
$ docker pull memcached@sha256:624036093e557f56a4d500c780f34193af25d5c3b73f8bb08329b579e72b7d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4570369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e3d248b914c5043ad7dc370403b9ea51bf62f972a6f7cf694a023ce14ac2d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223127e71140d5e120db85abbcc459b2ca368e042d165466a1ab8b72ada743f8`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf0ecced8267cdc41066ee8044aa4a0e35e951cba2f51a411ecbfb2cee29819`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 113.5 KB (113450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b7e62f8ce2395ffab9dff807ea14960a2cfa247d7c8a418a5e92d3b4d883f8`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 988.7 KB (988692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed293040c38a686b287b82c3a47615ca2f9034912964f5ce7e832241db526879`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1254936a9326dadc90d0b29d805e446f753a49826f2d9ea9308f5e847d6b7d4`  
		Last Modified: Mon, 03 Feb 2025 23:34:11 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.35-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:51c253df33d2a17a62bac93fdc69e4be991e6f4b9e6015eff29ad965c1e58628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 KB (111245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4b6a687d069c6e737d3a9cfa50af30753d0165aa04019517f2f6951bad7feb6`

```dockerfile
```

-	Layers:
	-	`sha256:4e1be19ae90b5f3b2e2b65ad7605851c11804d593bec1671c444bd7aadc3063d`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 91.7 KB (91676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:415673db52745ddb45aa4c05424023581f2903f3acd2578ac008e4857c8ca11b`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 19.6 KB (19569 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.35-bookworm`

```console
$ docker pull memcached@sha256:e099ebae6550a39ef5f780dc869ac48f17d87b09381a38ab0bc256a28a9e5d13
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

### `memcached:1.6.35-bookworm` - linux; amd64

```console
$ docker pull memcached@sha256:dfd99fb6fbe04b3121b1213ae0116e8d3703d1d329acc9b57ec40fe212c3d159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31972808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca71139ab2ab780916cc2410aeed46bd583f7d5b2f02e1df59647c913e1d933`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda7d6399fc25890be33d8e323a35feb9051c4a87322b3208defbca52c54b3be`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c0be3187b2dee7a02dfd52f423dc252930e248c53682a6a882a103aa3eec3a`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 2.5 MB (2491797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5808fec11b221c18511c8299b00aff12cf1fe592c5b7373edfd4c148480cb7f`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 1.3 MB (1267080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8745b39a0f5680ef45825db431aaa46b60468a8cdd43fed4fc477a4bffd35bbe`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d828e056dad95d08aea41b29d33fb1a2961ae61a4ce685a1b79a02a2569b7b0`  
		Last Modified: Mon, 03 Feb 2025 23:29:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.35-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:6b285e2b8239906b90664744391f1a4b6c3a3da8cae91273f01297a854b0b2aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18097e9c39f7331f3c6935c455fb1eeb3c8e451903fc73c9bdfae63c74cd99f8`

```dockerfile
```

-	Layers:
	-	`sha256:5be7ae24c2c09eaa07fd11802534cc38c1b5c8c6e32197189c0f2ece969e78b8`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 2.3 MB (2289307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce1fc3a95808478b79eae466f1bd195255ed42e1964471932ef4fa504b1a09ef`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.35-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:19cea7f4ef8974d31946d26f29af52dac2ef01f7839f9b18dc8a5c153dbb57bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29079481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8148d94dfb620e9b264755a021f81a0997844649fe9eef185c47837e87bdf9a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7a3fc1134bc1af98e13c0b7ea743c863d5a17f830a5fbd5a7002f750500e76c2`  
		Last Modified: Tue, 14 Jan 2025 01:33:27 GMT  
		Size: 25.7 MB (25736665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a566614fdcf63df3667efc0e44ef3a55e3691eced03cf22a308d708142f7c6`  
		Last Modified: Tue, 14 Jan 2025 02:34:26 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92a25a27c2144d0ab56f557820ebe289d1620f435ddb83f14c5e48b8d08cfa5`  
		Last Modified: Tue, 14 Jan 2025 02:34:27 GMT  
		Size: 2.1 MB (2096089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8889c18344163aeaea76936cd52029ec9bb42c2e16e0f26f48a664f00c3b7694`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 1.2 MB (1245215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68b0d4672ce5cd7584f0b15c42f219e41de7fb1f28644186a8a0f9788d2c96b`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbe1e74de797ff5b1fd4cf0a27d11ceeaf02347c856cfb5ba74cc13f4de8e6d`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.35-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:4af105a2f6c653acc913a722d6b3636c3637fe2718478bab2f4b1abf3a3df4b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb88776c99ff589e69412231781b8d108a5bd931b770d38eb94fdd69f0a97a1a`

```dockerfile
```

-	Layers:
	-	`sha256:f09d82aaa941a644405f9f34074de377bbd24b82df23d0ad6a22113f9aa74e41`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 2.3 MB (2292845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97bf9ecad7b0ab53e19b325ab9725de040ddcb369051fb8205db981408ba2764`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.35-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:0f287535bdbb8cfef4d259f59bcf13f2c3441335d3cff34f7d7c78830d4562b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31658415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536cfc0e620927f7137462160084b2211a938273db79693852e1834a3b0d7c0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66214caa62a6aa92636721a38d0e11a5fc383b1f9e4697a0991f5749369033c3`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca115360faf332637b0231cd4f43e98f284331aa2fb9bfbc45ec5d80a9eb57df`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 2.4 MB (2355304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5afe04d2434c6e19998a9fe47bfcf571759106e85ec73dd6ee83420494e2c8`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 1.3 MB (1260566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35e7292944fc376dd9f2578cf538f85a6df80492f5bc136e0024733aaeac8f0`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d44c4ade766e17abf585eb36d6683321ce9a2a26385b582758cda3872122039`  
		Last Modified: Mon, 03 Feb 2025 23:29:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.35-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:50321a237d4e2507a4e56d52d627e5ccb079e3bc300cc806390e96d09fb523a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e624df56f2e01bac1680fa105c39d9e35149d5cef920cd68e7266d5b2214f8d`

```dockerfile
```

-	Layers:
	-	`sha256:8be58e9cbbf71c38228da76c2508cdc0fcb85586ccc4b49518cf69e1e5e39b50`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 2.3 MB (2289622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caf4d0d59deb6f3fb187901e3b525ab0c834bb3cb6809eea8fb0c6879572ae3e`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 21.4 KB (21418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.35-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:f5be026a6f23f855459f3627e5c4101a938bca13100113b9fe82f28b3cb1cf3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32956119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d4368d3996e2021d38fdf63f7863d74ba28d6a2ef74e5131b0397dc12d442c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9009e1bef14c8af1bf770ff23da94f70dcd286b5f120ec1e71bf467ba40a0152`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f865fc757eeb18e208170c47e11bd3a00afa6eb223213d4007662aa6512c80dd`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 2.5 MB (2500709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34d14b87df5dcc8c799103bf14f9f622bc25c16e005e1e47b6a1306697bdf88`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 1.3 MB (1266299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d338f828cfbf806035a35f4290e62f96efce17c0e99cdf3034490cf047f32e1`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4697356823aab23c184948db8f06aa7c6811e207a99f109d4a0c115be482fb`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.35-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:7286999a5f604e3b4cc31c213c4c8d0cfa8b0da817e69563a83d6e14b14b7d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1456afa32760c7ecf3b6aa1f216615797de142ac46f0ee174b33ac71c2ed02a9`

```dockerfile
```

-	Layers:
	-	`sha256:7fe0965b391e043a806dd694395597114730be5687d0427a2011870ec7c674b4`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 2.3 MB (2286406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a6fca6555d8d2e7146c7a1f88c47abe5539931256a2f3990c263cf00390198a`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.35-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:9db344d39627ceb6b7961e5715daa16b063785632772a10a4f8953a4c131d3c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31692251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e517b7e21ed68b2abcdb3c957e98a677c411bf1b72ef4b78aa09b5bbcd0dc9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b08d7e697b04bda8cef97763765ebbbc16790e22945b5ab31d97d448a15c8650`  
		Last Modified: Tue, 14 Jan 2025 01:38:32 GMT  
		Size: 28.5 MB (28486647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda5f653b677ccaab1e67a8e7dce8f1c207af2b166ac4d37ddb395d85cb07a4c`  
		Last Modified: Tue, 14 Jan 2025 03:20:56 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bebcbc9eca024edee3e9bcea840742795d739cc90b447152cd52cf5dd79c442`  
		Last Modified: Mon, 03 Feb 2025 23:34:18 GMT  
		Size: 1.9 MB (1943213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d20ac443403dd981e7eca81d524af67815754bca86f5705e011ca0541a6ec0d`  
		Last Modified: Mon, 03 Feb 2025 23:34:18 GMT  
		Size: 1.3 MB (1260877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3be7f64ea082d115fc02a30fe0fa678d78bee0b27ac846dbdb688550d1908a0`  
		Last Modified: Mon, 03 Feb 2025 23:34:17 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1254936a9326dadc90d0b29d805e446f753a49826f2d9ea9308f5e847d6b7d4`  
		Last Modified: Mon, 03 Feb 2025 23:34:11 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.35-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:1ebb48a31e269c5b575e78e45853282855121ca1b723662138823061912b9f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7e22e388cefc5c2c0f77535a596b93848dd4fb8af57e9b54911aeca7ecd4be`

```dockerfile
```

-	Layers:
	-	`sha256:cb8d0d9b1786b7f482fc6383b420cee035f995c0616e30e3cb1699457e8b79da`  
		Last Modified: Mon, 03 Feb 2025 23:34:17 GMT  
		Size: 21.1 KB (21114 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.35-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:b02a75a9d8ff16af6610f5a7b1acbfe5021af039c99e973bba0cb4f3fed4983e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36085902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:706acef80ef55c5c88e96b5e797e157747af5331788d51358c2f14a0a32cd977`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80745399e148b36abf9f846b38e2d897d7b6c9d1520cfa9d06841c00dc04ba59`  
		Last Modified: Mon, 03 Feb 2025 23:29:23 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a519eadeb55cab90fe606d287a41791b2c969bf4b1920d8318fab913251b0af`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 2.7 MB (2708612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884edc77561270bf25675edb3ba73142d461c958c1abe45527aef893945b4ec3`  
		Last Modified: Mon, 03 Feb 2025 23:29:23 GMT  
		Size: 1.3 MB (1330930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61db6406d089d1edef82b5f70d15343ea8e4b58f8deec8f793da379e919d46f4`  
		Last Modified: Mon, 03 Feb 2025 23:29:23 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a63ce5f40ffc44148116e4b48c365aa2eeac8feaf8d8e23f6660428fd6e7a3c`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.35-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:45e7cede06534d2e9799fae7a25d6dfdf744eb59fa843709ae6110ecd5a0420f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fa7112b112ab20c85705872120dc8f663e550e84cd97fce814e9153e06f53ea`

```dockerfile
```

-	Layers:
	-	`sha256:fc19ce65e6afd53a0af7fa74af472d2396dc69c87a16470c380123077cc173d2`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 2.3 MB (2293679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:501f87cf15042c748d83d0afebfeeb81b7c41a29ed942369564bb6e9d4ef3c19`  
		Last Modified: Mon, 03 Feb 2025 23:29:23 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.35-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:6264d50a0c04cdc558dd1afa71b24ccadf6f5693254e7b6b31bdabb3ddb23995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30261786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0faa3849ef7eee7cd9e65ac3d63ddf439ea062c01ca4cc77c93c1753b1169750`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9009e1bef14c8af1bf770ff23da94f70dcd286b5f120ec1e71bf467ba40a0152`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c02ae601ee0bb3684ac021219c34b71a1227f865794041d376a31389166800`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 2.2 MB (2156339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489cc4b7fa1a8d54bdb06261a5300d09f429439845ae9fca4df8222ac8192830`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 1.2 MB (1245194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa1370e45fc434b599dcc2c02b0f1bec90d080c3af5176313cbd678095b5155`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f034bc901164b6d57bac0a9c94c66e4b96c53fe8af3fea3aee2c74897b480cf7`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.35-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:9d8033d81506e7fc653921e3a4c4f23fc13a05f43c5496885c9010f5af0891f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eb0e2cd949a02fe68968891360bbbc13a1fe4e5bdc90f6203a8941b43cca427`

```dockerfile
```

-	Layers:
	-	`sha256:2860febfb3de6c8ffc7c08113a3aaf7f61d254e27d8c2309f5ef39a476925888`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 2.3 MB (2289021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18b61144281568e7ddee023aac2c6947e14e31c547727eb355fa003ca1de66be`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine`

```console
$ docker pull memcached@sha256:b093f7f64a39f20b8f4a671f9c6656eff26821a3c97037a8019448040d6298bd
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
$ docker pull memcached@sha256:c497fc5a323c178e0914eca2500dcf9fa3b21ca2f9932dbc92b51ef6145cf2be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4716328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d2b29f4542cd1fc099ca3146ac53cc0eab71776ce1c029fee5d58a57c38a52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9604a91067e8818541aa31757690c9f8ebf60c58be004baded0767c0999267b8`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592b1cc3d47258eaa3cb466a887cb58e0b2a4176818d1c9a721698abf9337d94`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 104.7 KB (104686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5a55a29aba2a2a27962f2b36f259f5fac81a49009fc7c06020fc992eb6d5da`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 968.6 KB (968568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4786022d0e1453ad1d978f79f50839ba76e4f7c73310640921e5bc212537d6e`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da16032c7fbc5aedc09cd3d43a996943828a731b3ed781664abcf257bdfb65c`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:f4b6389438043b9d6191b9e22e19659d23258e22f0e414f51cb0945287141162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e696a02855f507b1b926a60cf07265433c5ab415467633243c2536753b3090`

```dockerfile
```

-	Layers:
	-	`sha256:16a139d5ff76ba43b3c520a2be58514f36e0ad4a7b0f9adfb6b9c80acb97219d`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 93.6 KB (93627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d8f0efc7a1d5a7dc78219efc6849e55d842b9a5e34ff6bee956735b7cbe2967`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:4d52a91c9cf3612ab9f44d1ecc192f150659288c8826932187c7ab3ed5f8dc9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5082815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef0a8813bf35c3ce3d0d0f9967d27c56db3fb8dc2fd7f31ab4cd3fc1f7cd209`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a202407430ec08b7a5bfb94689fc70aed855fbc1cd8b62ce145147fc5278b7a8`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82c0f1024964e8e055db8178bb0d2595a4a66f7398bffe83d6176cc192ac77e`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 120.8 KB (120783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46624d73285a34a525d44fb1f293cdb9fc95ebfb5b305918bc6a1ff77019fda`  
		Last Modified: Mon, 03 Feb 2025 23:32:18 GMT  
		Size: 968.3 KB (968310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099e6e9c12eb4dfbd63c3bc7cec8de6eb251173a42983594f30413921e56380a`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348cf5001affc34a6f03be6a7f413a6cc377fa11350026995dd53f7db78b85a1`  
		Last Modified: Mon, 03 Feb 2025 23:32:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:631105e348c97a01de96919b82284f666d3283712a23e1b5670c31c88810f40c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff4582dcb2cdec3cfb7590e5b6ade8162439d38a001ff6c08fa81f7d08c669e`

```dockerfile
```

-	Layers:
	-	`sha256:8f4375fd6e27a5ee655f47249469c2214b367ec0146b4e8769a97c6afa3d2829`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 93.7 KB (93731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4bf5d12011dbaae039aec13c76a68a64809e478a3b79d0090ba407f1d4f7c61`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:1f1e5941bca8da9b3aeabcc13c55fe90fc40f9c6476645c19172e508e5302723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4534153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2936f0dd081882d9f0da9ea6113e9780627d3a665a9d909de817c696fac9620`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300aaa75d91b0206b7556a721baaed9f7000ccf73ab8deda59e1cb428ec870f9`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ac94f71cda4f155944d630f60f3e31780c4a97ced13f6c61385dc7e95df429`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 109.5 KB (109465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73b7528b6c4fdfdf4075a75f9e28334049f5461f39426f3b2f983792188c971`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 960.2 KB (960204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb441509973ed0be28152c5ef6c85917a0de941839cd68559be4ecfcc273b17`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e6efaa8bc767e6ef9d48f3b7547a57b7d72964bbb765d7a66481f3f3b36dd1`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:0de21b11722d02a9d2cfc6acf661c6d755de360f4c1f70e7af549cac29e5aef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10be0a79af6bc5d121d12aa89f8e2191eb25f2533cfb4e1de067b3e0bbe82834`

```dockerfile
```

-	Layers:
	-	`sha256:c57cf3137ea2641a839877ddcf3a6065504f38c2ea4f2b7671c1776008e2cfcf`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 93.6 KB (93582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdf7d0d4ee2052676f3563869639942945b1cba543484223915cb33df997a5f0`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 19.5 KB (19512 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:913b5bd251bfe9202c3f0302d3c8c5a4ea3fb7f40f73e8561542c93db1c9d6c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4706076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8083b854e648814b258458b24e3039ade25fa9e63e50b6fb79db7cb05d2ee3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a841f248cda34139a77fd6ab9691e34b7d7dae6dfaedc45a2304aa25c07536`  
		Last Modified: Mon, 03 Feb 2025 23:32:07 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ccea169aa483a5ea29ebe89aa46469affffa54252ac8df2ee75acc10eca2e0`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 124.3 KB (124280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f40e8d115f7e602d9931eaa3e7f41c17dc35a40994befa787615cbd877d430`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 1.0 MB (1006836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf17c8f5e90551f91b3474eb46d197d4ac28e21bf5cb9aaa79eea5b851db371`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9971977dd87dcc447ad6eccbe529fc3c7d6b7dc6b74a4d74fb519c86565318f4`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:04513dfc421f21abd4cd316a69b57cdbfd9d92844a16e9d55eec6a4592cd22d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569bb3d3624a47ed75650ef0a92bfc59d63af78afe540637c817793e9cf4b6d6`

```dockerfile
```

-	Layers:
	-	`sha256:ba709bd16c5785bcfce6f9a8fd6e1d834e101c00d1ed2e018a68a999ec43825b`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 91.7 KB (91734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bc2aa4695d41b4a46d039e0e91f623f3f7aadfd866f0e477637054a37fc5127`  
		Last Modified: Mon, 03 Feb 2025 23:32:07 GMT  
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
$ docker pull memcached@sha256:624036093e557f56a4d500c780f34193af25d5c3b73f8bb08329b579e72b7d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4570369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e3d248b914c5043ad7dc370403b9ea51bf62f972a6f7cf694a023ce14ac2d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223127e71140d5e120db85abbcc459b2ca368e042d165466a1ab8b72ada743f8`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf0ecced8267cdc41066ee8044aa4a0e35e951cba2f51a411ecbfb2cee29819`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 113.5 KB (113450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b7e62f8ce2395ffab9dff807ea14960a2cfa247d7c8a418a5e92d3b4d883f8`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 988.7 KB (988692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed293040c38a686b287b82c3a47615ca2f9034912964f5ce7e832241db526879`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1254936a9326dadc90d0b29d805e446f753a49826f2d9ea9308f5e847d6b7d4`  
		Last Modified: Mon, 03 Feb 2025 23:34:11 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:51c253df33d2a17a62bac93fdc69e4be991e6f4b9e6015eff29ad965c1e58628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 KB (111245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4b6a687d069c6e737d3a9cfa50af30753d0165aa04019517f2f6951bad7feb6`

```dockerfile
```

-	Layers:
	-	`sha256:4e1be19ae90b5f3b2e2b65ad7605851c11804d593bec1671c444bd7aadc3063d`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 91.7 KB (91676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:415673db52745ddb45aa4c05424023581f2903f3acd2578ac008e4857c8ca11b`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 19.6 KB (19569 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine3.21`

```console
$ docker pull memcached@sha256:918f8d596494e94538b93f92d629c3d20efa4d5ca8b0302bf672b65f974c5617
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
$ docker pull memcached@sha256:c497fc5a323c178e0914eca2500dcf9fa3b21ca2f9932dbc92b51ef6145cf2be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4716328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d2b29f4542cd1fc099ca3146ac53cc0eab71776ce1c029fee5d58a57c38a52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9604a91067e8818541aa31757690c9f8ebf60c58be004baded0767c0999267b8`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592b1cc3d47258eaa3cb466a887cb58e0b2a4176818d1c9a721698abf9337d94`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 104.7 KB (104686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5a55a29aba2a2a27962f2b36f259f5fac81a49009fc7c06020fc992eb6d5da`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 968.6 KB (968568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4786022d0e1453ad1d978f79f50839ba76e4f7c73310640921e5bc212537d6e`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da16032c7fbc5aedc09cd3d43a996943828a731b3ed781664abcf257bdfb65c`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:f4b6389438043b9d6191b9e22e19659d23258e22f0e414f51cb0945287141162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e696a02855f507b1b926a60cf07265433c5ab415467633243c2536753b3090`

```dockerfile
```

-	Layers:
	-	`sha256:16a139d5ff76ba43b3c520a2be58514f36e0ad4a7b0f9adfb6b9c80acb97219d`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 93.6 KB (93627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d8f0efc7a1d5a7dc78219efc6849e55d842b9a5e34ff6bee956735b7cbe2967`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:4d52a91c9cf3612ab9f44d1ecc192f150659288c8826932187c7ab3ed5f8dc9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5082815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef0a8813bf35c3ce3d0d0f9967d27c56db3fb8dc2fd7f31ab4cd3fc1f7cd209`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a202407430ec08b7a5bfb94689fc70aed855fbc1cd8b62ce145147fc5278b7a8`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82c0f1024964e8e055db8178bb0d2595a4a66f7398bffe83d6176cc192ac77e`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 120.8 KB (120783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46624d73285a34a525d44fb1f293cdb9fc95ebfb5b305918bc6a1ff77019fda`  
		Last Modified: Mon, 03 Feb 2025 23:32:18 GMT  
		Size: 968.3 KB (968310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099e6e9c12eb4dfbd63c3bc7cec8de6eb251173a42983594f30413921e56380a`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348cf5001affc34a6f03be6a7f413a6cc377fa11350026995dd53f7db78b85a1`  
		Last Modified: Mon, 03 Feb 2025 23:32:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:631105e348c97a01de96919b82284f666d3283712a23e1b5670c31c88810f40c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff4582dcb2cdec3cfb7590e5b6ade8162439d38a001ff6c08fa81f7d08c669e`

```dockerfile
```

-	Layers:
	-	`sha256:8f4375fd6e27a5ee655f47249469c2214b367ec0146b4e8769a97c6afa3d2829`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 93.7 KB (93731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4bf5d12011dbaae039aec13c76a68a64809e478a3b79d0090ba407f1d4f7c61`  
		Last Modified: Mon, 03 Feb 2025 23:32:17 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.21` - linux; 386

```console
$ docker pull memcached@sha256:1f1e5941bca8da9b3aeabcc13c55fe90fc40f9c6476645c19172e508e5302723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4534153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2936f0dd081882d9f0da9ea6113e9780627d3a665a9d909de817c696fac9620`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300aaa75d91b0206b7556a721baaed9f7000ccf73ab8deda59e1cb428ec870f9`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ac94f71cda4f155944d630f60f3e31780c4a97ced13f6c61385dc7e95df429`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 109.5 KB (109465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73b7528b6c4fdfdf4075a75f9e28334049f5461f39426f3b2f983792188c971`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 960.2 KB (960204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb441509973ed0be28152c5ef6c85917a0de941839cd68559be4ecfcc273b17`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e6efaa8bc767e6ef9d48f3b7547a57b7d72964bbb765d7a66481f3f3b36dd1`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:0de21b11722d02a9d2cfc6acf661c6d755de360f4c1f70e7af549cac29e5aef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10be0a79af6bc5d121d12aa89f8e2191eb25f2533cfb4e1de067b3e0bbe82834`

```dockerfile
```

-	Layers:
	-	`sha256:c57cf3137ea2641a839877ddcf3a6065504f38c2ea4f2b7671c1776008e2cfcf`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 93.6 KB (93582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdf7d0d4ee2052676f3563869639942945b1cba543484223915cb33df997a5f0`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 19.5 KB (19512 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.21` - linux; ppc64le

```console
$ docker pull memcached@sha256:913b5bd251bfe9202c3f0302d3c8c5a4ea3fb7f40f73e8561542c93db1c9d6c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4706076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8083b854e648814b258458b24e3039ade25fa9e63e50b6fb79db7cb05d2ee3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a841f248cda34139a77fd6ab9691e34b7d7dae6dfaedc45a2304aa25c07536`  
		Last Modified: Mon, 03 Feb 2025 23:32:07 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ccea169aa483a5ea29ebe89aa46469affffa54252ac8df2ee75acc10eca2e0`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 124.3 KB (124280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f40e8d115f7e602d9931eaa3e7f41c17dc35a40994befa787615cbd877d430`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 1.0 MB (1006836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf17c8f5e90551f91b3474eb46d197d4ac28e21bf5cb9aaa79eea5b851db371`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9971977dd87dcc447ad6eccbe529fc3c7d6b7dc6b74a4d74fb519c86565318f4`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:04513dfc421f21abd4cd316a69b57cdbfd9d92844a16e9d55eec6a4592cd22d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569bb3d3624a47ed75650ef0a92bfc59d63af78afe540637c817793e9cf4b6d6`

```dockerfile
```

-	Layers:
	-	`sha256:ba709bd16c5785bcfce6f9a8fd6e1d834e101c00d1ed2e018a68a999ec43825b`  
		Last Modified: Mon, 03 Feb 2025 23:32:08 GMT  
		Size: 91.7 KB (91734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bc2aa4695d41b4a46d039e0e91f623f3f7aadfd866f0e477637054a37fc5127`  
		Last Modified: Mon, 03 Feb 2025 23:32:07 GMT  
		Size: 19.6 KB (19648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.21` - linux; s390x

```console
$ docker pull memcached@sha256:624036093e557f56a4d500c780f34193af25d5c3b73f8bb08329b579e72b7d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4570369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e3d248b914c5043ad7dc370403b9ea51bf62f972a6f7cf694a023ce14ac2d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223127e71140d5e120db85abbcc459b2ca368e042d165466a1ab8b72ada743f8`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf0ecced8267cdc41066ee8044aa4a0e35e951cba2f51a411ecbfb2cee29819`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 113.5 KB (113450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b7e62f8ce2395ffab9dff807ea14960a2cfa247d7c8a418a5e92d3b4d883f8`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 988.7 KB (988692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed293040c38a686b287b82c3a47615ca2f9034912964f5ce7e832241db526879`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1254936a9326dadc90d0b29d805e446f753a49826f2d9ea9308f5e847d6b7d4`  
		Last Modified: Mon, 03 Feb 2025 23:34:11 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:51c253df33d2a17a62bac93fdc69e4be991e6f4b9e6015eff29ad965c1e58628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 KB (111245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4b6a687d069c6e737d3a9cfa50af30753d0165aa04019517f2f6951bad7feb6`

```dockerfile
```

-	Layers:
	-	`sha256:4e1be19ae90b5f3b2e2b65ad7605851c11804d593bec1671c444bd7aadc3063d`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 91.7 KB (91676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:415673db52745ddb45aa4c05424023581f2903f3acd2578ac008e4857c8ca11b`  
		Last Modified: Mon, 03 Feb 2025 23:34:10 GMT  
		Size: 19.6 KB (19569 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:bookworm`

```console
$ docker pull memcached@sha256:e099ebae6550a39ef5f780dc869ac48f17d87b09381a38ab0bc256a28a9e5d13
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
$ docker pull memcached@sha256:dfd99fb6fbe04b3121b1213ae0116e8d3703d1d329acc9b57ec40fe212c3d159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31972808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca71139ab2ab780916cc2410aeed46bd583f7d5b2f02e1df59647c913e1d933`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda7d6399fc25890be33d8e323a35feb9051c4a87322b3208defbca52c54b3be`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c0be3187b2dee7a02dfd52f423dc252930e248c53682a6a882a103aa3eec3a`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 2.5 MB (2491797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5808fec11b221c18511c8299b00aff12cf1fe592c5b7373edfd4c148480cb7f`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 1.3 MB (1267080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8745b39a0f5680ef45825db431aaa46b60468a8cdd43fed4fc477a4bffd35bbe`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d828e056dad95d08aea41b29d33fb1a2961ae61a4ce685a1b79a02a2569b7b0`  
		Last Modified: Mon, 03 Feb 2025 23:29:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:6b285e2b8239906b90664744391f1a4b6c3a3da8cae91273f01297a854b0b2aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18097e9c39f7331f3c6935c455fb1eeb3c8e451903fc73c9bdfae63c74cd99f8`

```dockerfile
```

-	Layers:
	-	`sha256:5be7ae24c2c09eaa07fd11802534cc38c1b5c8c6e32197189c0f2ece969e78b8`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 2.3 MB (2289307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce1fc3a95808478b79eae466f1bd195255ed42e1964471932ef4fa504b1a09ef`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:19cea7f4ef8974d31946d26f29af52dac2ef01f7839f9b18dc8a5c153dbb57bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29079481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8148d94dfb620e9b264755a021f81a0997844649fe9eef185c47837e87bdf9a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7a3fc1134bc1af98e13c0b7ea743c863d5a17f830a5fbd5a7002f750500e76c2`  
		Last Modified: Tue, 14 Jan 2025 01:33:27 GMT  
		Size: 25.7 MB (25736665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a566614fdcf63df3667efc0e44ef3a55e3691eced03cf22a308d708142f7c6`  
		Last Modified: Tue, 14 Jan 2025 02:34:26 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92a25a27c2144d0ab56f557820ebe289d1620f435ddb83f14c5e48b8d08cfa5`  
		Last Modified: Tue, 14 Jan 2025 02:34:27 GMT  
		Size: 2.1 MB (2096089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8889c18344163aeaea76936cd52029ec9bb42c2e16e0f26f48a664f00c3b7694`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 1.2 MB (1245215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68b0d4672ce5cd7584f0b15c42f219e41de7fb1f28644186a8a0f9788d2c96b`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbe1e74de797ff5b1fd4cf0a27d11ceeaf02347c856cfb5ba74cc13f4de8e6d`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:4af105a2f6c653acc913a722d6b3636c3637fe2718478bab2f4b1abf3a3df4b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb88776c99ff589e69412231781b8d108a5bd931b770d38eb94fdd69f0a97a1a`

```dockerfile
```

-	Layers:
	-	`sha256:f09d82aaa941a644405f9f34074de377bbd24b82df23d0ad6a22113f9aa74e41`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 2.3 MB (2292845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97bf9ecad7b0ab53e19b325ab9725de040ddcb369051fb8205db981408ba2764`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:0f287535bdbb8cfef4d259f59bcf13f2c3441335d3cff34f7d7c78830d4562b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31658415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536cfc0e620927f7137462160084b2211a938273db79693852e1834a3b0d7c0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66214caa62a6aa92636721a38d0e11a5fc383b1f9e4697a0991f5749369033c3`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca115360faf332637b0231cd4f43e98f284331aa2fb9bfbc45ec5d80a9eb57df`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 2.4 MB (2355304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5afe04d2434c6e19998a9fe47bfcf571759106e85ec73dd6ee83420494e2c8`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 1.3 MB (1260566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35e7292944fc376dd9f2578cf538f85a6df80492f5bc136e0024733aaeac8f0`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d44c4ade766e17abf585eb36d6683321ce9a2a26385b582758cda3872122039`  
		Last Modified: Mon, 03 Feb 2025 23:29:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:50321a237d4e2507a4e56d52d627e5ccb079e3bc300cc806390e96d09fb523a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e624df56f2e01bac1680fa105c39d9e35149d5cef920cd68e7266d5b2214f8d`

```dockerfile
```

-	Layers:
	-	`sha256:8be58e9cbbf71c38228da76c2508cdc0fcb85586ccc4b49518cf69e1e5e39b50`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 2.3 MB (2289622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caf4d0d59deb6f3fb187901e3b525ab0c834bb3cb6809eea8fb0c6879572ae3e`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 21.4 KB (21418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; 386

```console
$ docker pull memcached@sha256:f5be026a6f23f855459f3627e5c4101a938bca13100113b9fe82f28b3cb1cf3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32956119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d4368d3996e2021d38fdf63f7863d74ba28d6a2ef74e5131b0397dc12d442c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9009e1bef14c8af1bf770ff23da94f70dcd286b5f120ec1e71bf467ba40a0152`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f865fc757eeb18e208170c47e11bd3a00afa6eb223213d4007662aa6512c80dd`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 2.5 MB (2500709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34d14b87df5dcc8c799103bf14f9f622bc25c16e005e1e47b6a1306697bdf88`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 1.3 MB (1266299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d338f828cfbf806035a35f4290e62f96efce17c0e99cdf3034490cf047f32e1`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4697356823aab23c184948db8f06aa7c6811e207a99f109d4a0c115be482fb`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:7286999a5f604e3b4cc31c213c4c8d0cfa8b0da817e69563a83d6e14b14b7d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1456afa32760c7ecf3b6aa1f216615797de142ac46f0ee174b33ac71c2ed02a9`

```dockerfile
```

-	Layers:
	-	`sha256:7fe0965b391e043a806dd694395597114730be5687d0427a2011870ec7c674b4`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 2.3 MB (2286406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a6fca6555d8d2e7146c7a1f88c47abe5539931256a2f3990c263cf00390198a`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:9db344d39627ceb6b7961e5715daa16b063785632772a10a4f8953a4c131d3c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31692251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e517b7e21ed68b2abcdb3c957e98a677c411bf1b72ef4b78aa09b5bbcd0dc9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b08d7e697b04bda8cef97763765ebbbc16790e22945b5ab31d97d448a15c8650`  
		Last Modified: Tue, 14 Jan 2025 01:38:32 GMT  
		Size: 28.5 MB (28486647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda5f653b677ccaab1e67a8e7dce8f1c207af2b166ac4d37ddb395d85cb07a4c`  
		Last Modified: Tue, 14 Jan 2025 03:20:56 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bebcbc9eca024edee3e9bcea840742795d739cc90b447152cd52cf5dd79c442`  
		Last Modified: Mon, 03 Feb 2025 23:34:18 GMT  
		Size: 1.9 MB (1943213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d20ac443403dd981e7eca81d524af67815754bca86f5705e011ca0541a6ec0d`  
		Last Modified: Mon, 03 Feb 2025 23:34:18 GMT  
		Size: 1.3 MB (1260877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3be7f64ea082d115fc02a30fe0fa678d78bee0b27ac846dbdb688550d1908a0`  
		Last Modified: Mon, 03 Feb 2025 23:34:17 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1254936a9326dadc90d0b29d805e446f753a49826f2d9ea9308f5e847d6b7d4`  
		Last Modified: Mon, 03 Feb 2025 23:34:11 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:1ebb48a31e269c5b575e78e45853282855121ca1b723662138823061912b9f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7e22e388cefc5c2c0f77535a596b93848dd4fb8af57e9b54911aeca7ecd4be`

```dockerfile
```

-	Layers:
	-	`sha256:cb8d0d9b1786b7f482fc6383b420cee035f995c0616e30e3cb1699457e8b79da`  
		Last Modified: Mon, 03 Feb 2025 23:34:17 GMT  
		Size: 21.1 KB (21114 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:b02a75a9d8ff16af6610f5a7b1acbfe5021af039c99e973bba0cb4f3fed4983e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36085902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:706acef80ef55c5c88e96b5e797e157747af5331788d51358c2f14a0a32cd977`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80745399e148b36abf9f846b38e2d897d7b6c9d1520cfa9d06841c00dc04ba59`  
		Last Modified: Mon, 03 Feb 2025 23:29:23 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a519eadeb55cab90fe606d287a41791b2c969bf4b1920d8318fab913251b0af`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 2.7 MB (2708612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884edc77561270bf25675edb3ba73142d461c958c1abe45527aef893945b4ec3`  
		Last Modified: Mon, 03 Feb 2025 23:29:23 GMT  
		Size: 1.3 MB (1330930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61db6406d089d1edef82b5f70d15343ea8e4b58f8deec8f793da379e919d46f4`  
		Last Modified: Mon, 03 Feb 2025 23:29:23 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a63ce5f40ffc44148116e4b48c365aa2eeac8feaf8d8e23f6660428fd6e7a3c`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:45e7cede06534d2e9799fae7a25d6dfdf744eb59fa843709ae6110ecd5a0420f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fa7112b112ab20c85705872120dc8f663e550e84cd97fce814e9153e06f53ea`

```dockerfile
```

-	Layers:
	-	`sha256:fc19ce65e6afd53a0af7fa74af472d2396dc69c87a16470c380123077cc173d2`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 2.3 MB (2293679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:501f87cf15042c748d83d0afebfeeb81b7c41a29ed942369564bb6e9d4ef3c19`  
		Last Modified: Mon, 03 Feb 2025 23:29:23 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:6264d50a0c04cdc558dd1afa71b24ccadf6f5693254e7b6b31bdabb3ddb23995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30261786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0faa3849ef7eee7cd9e65ac3d63ddf439ea062c01ca4cc77c93c1753b1169750`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9009e1bef14c8af1bf770ff23da94f70dcd286b5f120ec1e71bf467ba40a0152`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c02ae601ee0bb3684ac021219c34b71a1227f865794041d376a31389166800`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 2.2 MB (2156339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489cc4b7fa1a8d54bdb06261a5300d09f429439845ae9fca4df8222ac8192830`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 1.2 MB (1245194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa1370e45fc434b599dcc2c02b0f1bec90d080c3af5176313cbd678095b5155`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f034bc901164b6d57bac0a9c94c66e4b96c53fe8af3fea3aee2c74897b480cf7`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:9d8033d81506e7fc653921e3a4c4f23fc13a05f43c5496885c9010f5af0891f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eb0e2cd949a02fe68968891360bbbc13a1fe4e5bdc90f6203a8941b43cca427`

```dockerfile
```

-	Layers:
	-	`sha256:2860febfb3de6c8ffc7c08113a3aaf7f61d254e27d8c2309f5ef39a476925888`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 2.3 MB (2289021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18b61144281568e7ddee023aac2c6947e14e31c547727eb355fa003ca1de66be`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:latest`

```console
$ docker pull memcached@sha256:e099ebae6550a39ef5f780dc869ac48f17d87b09381a38ab0bc256a28a9e5d13
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
$ docker pull memcached@sha256:dfd99fb6fbe04b3121b1213ae0116e8d3703d1d329acc9b57ec40fe212c3d159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31972808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca71139ab2ab780916cc2410aeed46bd583f7d5b2f02e1df59647c913e1d933`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda7d6399fc25890be33d8e323a35feb9051c4a87322b3208defbca52c54b3be`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c0be3187b2dee7a02dfd52f423dc252930e248c53682a6a882a103aa3eec3a`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 2.5 MB (2491797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5808fec11b221c18511c8299b00aff12cf1fe592c5b7373edfd4c148480cb7f`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 1.3 MB (1267080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8745b39a0f5680ef45825db431aaa46b60468a8cdd43fed4fc477a4bffd35bbe`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d828e056dad95d08aea41b29d33fb1a2961ae61a4ce685a1b79a02a2569b7b0`  
		Last Modified: Mon, 03 Feb 2025 23:29:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:6b285e2b8239906b90664744391f1a4b6c3a3da8cae91273f01297a854b0b2aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18097e9c39f7331f3c6935c455fb1eeb3c8e451903fc73c9bdfae63c74cd99f8`

```dockerfile
```

-	Layers:
	-	`sha256:5be7ae24c2c09eaa07fd11802534cc38c1b5c8c6e32197189c0f2ece969e78b8`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 2.3 MB (2289307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce1fc3a95808478b79eae466f1bd195255ed42e1964471932ef4fa504b1a09ef`  
		Last Modified: Mon, 03 Feb 2025 23:29:55 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:19cea7f4ef8974d31946d26f29af52dac2ef01f7839f9b18dc8a5c153dbb57bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29079481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8148d94dfb620e9b264755a021f81a0997844649fe9eef185c47837e87bdf9a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7a3fc1134bc1af98e13c0b7ea743c863d5a17f830a5fbd5a7002f750500e76c2`  
		Last Modified: Tue, 14 Jan 2025 01:33:27 GMT  
		Size: 25.7 MB (25736665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a566614fdcf63df3667efc0e44ef3a55e3691eced03cf22a308d708142f7c6`  
		Last Modified: Tue, 14 Jan 2025 02:34:26 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92a25a27c2144d0ab56f557820ebe289d1620f435ddb83f14c5e48b8d08cfa5`  
		Last Modified: Tue, 14 Jan 2025 02:34:27 GMT  
		Size: 2.1 MB (2096089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8889c18344163aeaea76936cd52029ec9bb42c2e16e0f26f48a664f00c3b7694`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 1.2 MB (1245215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68b0d4672ce5cd7584f0b15c42f219e41de7fb1f28644186a8a0f9788d2c96b`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbe1e74de797ff5b1fd4cf0a27d11ceeaf02347c856cfb5ba74cc13f4de8e6d`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:4af105a2f6c653acc913a722d6b3636c3637fe2718478bab2f4b1abf3a3df4b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb88776c99ff589e69412231781b8d108a5bd931b770d38eb94fdd69f0a97a1a`

```dockerfile
```

-	Layers:
	-	`sha256:f09d82aaa941a644405f9f34074de377bbd24b82df23d0ad6a22113f9aa74e41`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 2.3 MB (2292845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97bf9ecad7b0ab53e19b325ab9725de040ddcb369051fb8205db981408ba2764`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:0f287535bdbb8cfef4d259f59bcf13f2c3441335d3cff34f7d7c78830d4562b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31658415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536cfc0e620927f7137462160084b2211a938273db79693852e1834a3b0d7c0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66214caa62a6aa92636721a38d0e11a5fc383b1f9e4697a0991f5749369033c3`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca115360faf332637b0231cd4f43e98f284331aa2fb9bfbc45ec5d80a9eb57df`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 2.4 MB (2355304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5afe04d2434c6e19998a9fe47bfcf571759106e85ec73dd6ee83420494e2c8`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 1.3 MB (1260566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35e7292944fc376dd9f2578cf538f85a6df80492f5bc136e0024733aaeac8f0`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d44c4ade766e17abf585eb36d6683321ce9a2a26385b582758cda3872122039`  
		Last Modified: Mon, 03 Feb 2025 23:29:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:50321a237d4e2507a4e56d52d627e5ccb079e3bc300cc806390e96d09fb523a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e624df56f2e01bac1680fa105c39d9e35149d5cef920cd68e7266d5b2214f8d`

```dockerfile
```

-	Layers:
	-	`sha256:8be58e9cbbf71c38228da76c2508cdc0fcb85586ccc4b49518cf69e1e5e39b50`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 2.3 MB (2289622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caf4d0d59deb6f3fb187901e3b525ab0c834bb3cb6809eea8fb0c6879572ae3e`  
		Last Modified: Mon, 03 Feb 2025 23:29:27 GMT  
		Size: 21.4 KB (21418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:f5be026a6f23f855459f3627e5c4101a938bca13100113b9fe82f28b3cb1cf3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32956119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d4368d3996e2021d38fdf63f7863d74ba28d6a2ef74e5131b0397dc12d442c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9009e1bef14c8af1bf770ff23da94f70dcd286b5f120ec1e71bf467ba40a0152`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f865fc757eeb18e208170c47e11bd3a00afa6eb223213d4007662aa6512c80dd`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 2.5 MB (2500709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34d14b87df5dcc8c799103bf14f9f622bc25c16e005e1e47b6a1306697bdf88`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 1.3 MB (1266299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d338f828cfbf806035a35f4290e62f96efce17c0e99cdf3034490cf047f32e1`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4697356823aab23c184948db8f06aa7c6811e207a99f109d4a0c115be482fb`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:7286999a5f604e3b4cc31c213c4c8d0cfa8b0da817e69563a83d6e14b14b7d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1456afa32760c7ecf3b6aa1f216615797de142ac46f0ee174b33ac71c2ed02a9`

```dockerfile
```

-	Layers:
	-	`sha256:7fe0965b391e043a806dd694395597114730be5687d0427a2011870ec7c674b4`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 2.3 MB (2286406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a6fca6555d8d2e7146c7a1f88c47abe5539931256a2f3990c263cf00390198a`  
		Last Modified: Mon, 03 Feb 2025 23:30:18 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; mips64le

```console
$ docker pull memcached@sha256:9db344d39627ceb6b7961e5715daa16b063785632772a10a4f8953a4c131d3c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31692251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e517b7e21ed68b2abcdb3c957e98a677c411bf1b72ef4b78aa09b5bbcd0dc9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b08d7e697b04bda8cef97763765ebbbc16790e22945b5ab31d97d448a15c8650`  
		Last Modified: Tue, 14 Jan 2025 01:38:32 GMT  
		Size: 28.5 MB (28486647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda5f653b677ccaab1e67a8e7dce8f1c207af2b166ac4d37ddb395d85cb07a4c`  
		Last Modified: Tue, 14 Jan 2025 03:20:56 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bebcbc9eca024edee3e9bcea840742795d739cc90b447152cd52cf5dd79c442`  
		Last Modified: Mon, 03 Feb 2025 23:34:18 GMT  
		Size: 1.9 MB (1943213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d20ac443403dd981e7eca81d524af67815754bca86f5705e011ca0541a6ec0d`  
		Last Modified: Mon, 03 Feb 2025 23:34:18 GMT  
		Size: 1.3 MB (1260877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3be7f64ea082d115fc02a30fe0fa678d78bee0b27ac846dbdb688550d1908a0`  
		Last Modified: Mon, 03 Feb 2025 23:34:17 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1254936a9326dadc90d0b29d805e446f753a49826f2d9ea9308f5e847d6b7d4`  
		Last Modified: Mon, 03 Feb 2025 23:34:11 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:1ebb48a31e269c5b575e78e45853282855121ca1b723662138823061912b9f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7e22e388cefc5c2c0f77535a596b93848dd4fb8af57e9b54911aeca7ecd4be`

```dockerfile
```

-	Layers:
	-	`sha256:cb8d0d9b1786b7f482fc6383b420cee035f995c0616e30e3cb1699457e8b79da`  
		Last Modified: Mon, 03 Feb 2025 23:34:17 GMT  
		Size: 21.1 KB (21114 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:b02a75a9d8ff16af6610f5a7b1acbfe5021af039c99e973bba0cb4f3fed4983e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36085902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:706acef80ef55c5c88e96b5e797e157747af5331788d51358c2f14a0a32cd977`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80745399e148b36abf9f846b38e2d897d7b6c9d1520cfa9d06841c00dc04ba59`  
		Last Modified: Mon, 03 Feb 2025 23:29:23 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a519eadeb55cab90fe606d287a41791b2c969bf4b1920d8318fab913251b0af`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 2.7 MB (2708612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884edc77561270bf25675edb3ba73142d461c958c1abe45527aef893945b4ec3`  
		Last Modified: Mon, 03 Feb 2025 23:29:23 GMT  
		Size: 1.3 MB (1330930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61db6406d089d1edef82b5f70d15343ea8e4b58f8deec8f793da379e919d46f4`  
		Last Modified: Mon, 03 Feb 2025 23:29:23 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a63ce5f40ffc44148116e4b48c365aa2eeac8feaf8d8e23f6660428fd6e7a3c`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:45e7cede06534d2e9799fae7a25d6dfdf744eb59fa843709ae6110ecd5a0420f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fa7112b112ab20c85705872120dc8f663e550e84cd97fce814e9153e06f53ea`

```dockerfile
```

-	Layers:
	-	`sha256:fc19ce65e6afd53a0af7fa74af472d2396dc69c87a16470c380123077cc173d2`  
		Last Modified: Mon, 03 Feb 2025 23:29:24 GMT  
		Size: 2.3 MB (2293679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:501f87cf15042c748d83d0afebfeeb81b7c41a29ed942369564bb6e9d4ef3c19`  
		Last Modified: Mon, 03 Feb 2025 23:29:23 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:6264d50a0c04cdc558dd1afa71b24ccadf6f5693254e7b6b31bdabb3ddb23995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30261786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0faa3849ef7eee7cd9e65ac3d63ddf439ea062c01ca4cc77c93c1753b1169750`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_VERSION=1.6.35
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.35.tar.gz
# Sun, 02 Feb 2025 07:54:12 GMT
ENV MEMCACHED_SHA1=4f6f6fc3bc058fce579679c28f117866c2c25e55
# Sun, 02 Feb 2025 07:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sun, 02 Feb 2025 07:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 07:54:12 GMT
USER memcache
# Sun, 02 Feb 2025 07:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Sun, 02 Feb 2025 07:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9009e1bef14c8af1bf770ff23da94f70dcd286b5f120ec1e71bf467ba40a0152`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c02ae601ee0bb3684ac021219c34b71a1227f865794041d376a31389166800`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 2.2 MB (2156339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489cc4b7fa1a8d54bdb06261a5300d09f429439845ae9fca4df8222ac8192830`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 1.2 MB (1245194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa1370e45fc434b599dcc2c02b0f1bec90d080c3af5176313cbd678095b5155`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f034bc901164b6d57bac0a9c94c66e4b96c53fe8af3fea3aee2c74897b480cf7`  
		Last Modified: Mon, 03 Feb 2025 23:30:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:9d8033d81506e7fc653921e3a4c4f23fc13a05f43c5496885c9010f5af0891f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eb0e2cd949a02fe68968891360bbbc13a1fe4e5bdc90f6203a8941b43cca427`

```dockerfile
```

-	Layers:
	-	`sha256:2860febfb3de6c8ffc7c08113a3aaf7f61d254e27d8c2309f5ef39a476925888`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 2.3 MB (2289021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18b61144281568e7ddee023aac2c6947e14e31c547727eb355fa003ca1de66be`  
		Last Modified: Mon, 03 Feb 2025 23:30:12 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json
